Please visit the EasyTier Official Website to view the full documentation.

EasyTier is a simple, safe and decentralized VPN networking solution implemented with the Rust language and Tokio framework.

### Key Features

- **Decentralized**: No need to rely on centralized services, nodes are equal and independent.
- **Safe**: Use WireGuard protocol to encrypt data.
- **High Performance**: Full-link zero-copy, with performance comparable to mainstream networking software.
- **Cross-platform**: Supports MacOS/Linux/Windows/Android, will support IOS in the future. The executable file is statically linked, making deployment simple.
- **Networking without public IP**: Supports networking using shared public nodes, refer to [Configuration Guide](#Networking-without-public-IP)
- **NAT traversal**: Supports UDP-based NAT traversal, able to establish stable connections even in complex network environments.
- **Subnet Proxy (Point-to-Network)**: Nodes can expose accessible network segments as proxies to the VPN subnet, allowing other nodes to access these subnets through the node.
- **Smart Routing**: Selects links based on traffic to reduce latency and increase throughput.
- **TCP Support**: Provides reliable data transmission through concurrent TCP links when UDP is limited, optimizing performance.
- **High Availability**: Supports multi-path and switches to healthy paths when high packet loss or network errors are detected.
- **IPv6 Support**: Supports networking using IPv6.
- **Multiple Protocol Types**: Supports communication between nodes using protocols such as WebSocket and QUIC.
- **Web Management Interface**: Provides a [web-based management](https://easytier.cn/web) interface for easy configuration and monitoring.

### Notice
...