## LiteLLM

LiteLLM is an OpenAI-compatible gateway for calling 100+ LLM providers through a single, consistent API. Use it as a central LLM service to standardize access, enforce guardrails, track costs, and operate multiple providers and deployments behind one endpoint.

### Features

- OpenAI-compatible API across 100+ providers (chat/completions, embeddings, image generation)
- Consistent responses
- Router with retry, fallback, and multi-deployment failover
- Centralized proxy (LLM gateway) with hooks for auth, logging, caching, and guardrails per project
- Cost tracking with spend limits and budgets by project/tenant
- Rate limiting and usage controls
- Pluggable and extensible provider support

### Notice

- Secrets required by this template:
  - Master key: You can change this after setup
  - Salt key: Cryptographic salt. You cannot change this after adding a model
- Use strong, random keys. The LiteLLM team recommends using a generator like 1Password.
- Resource sizing: LiteLLM recommends 2 vCPU and 4 GB RAM. This template uses minimal resources by default, scale as needed.
- Rotate the master key periodically. Recommended flow by LiteLLM:
  1) Back up your database.
  2) Re-encrypt with a new master key:
     ```bash
     curl -L -X POST 'http://<host>:4000/key/regenerate' \
       -H 'Authorization: Bearer <current_master_key>' \
       -H 'Content-Type: application/json' \
       -d '{
         "key": "<current_master_key>",
         "new_master_key": "<new_master_key>"
       }'
     ```
     You may see decryption errors until the environment is updated.
  3) Update the `LITELLM_MASTER_KEY` environment variable to the new master key.
  4) Test a request to confirm decryption works:
     ```bash
     curl -L -X POST 'http://<host>:4000/v1/chat/completions' \
       -H 'Content-Type: application/json' \
       -H 'Authorization: Bearer <new_master_key_or_virtual_key>' \
       -d '{
         "model": "gpt-4o-mini",
         "messages": [{"role":"user","content":"Hello"}]
       }'
     ```
