# Introduction to Vaultwarden

Vaultwarden is a lightweight, self-hosted password management solution that serves as an unofficial Bitwarden-compatible server. Designed for simplicity and efficiency, it offers users the ability to host their own password vault without relying on third-party services. By implementing the Bitwarden API, Vaultwarden ensures seamless compatibility with official Bitwarden clients while minimizing resource usage, making it ideal for personal or small-scale deployments.

## Key Features

- **Bitwarden Compatibility**: Fully supports the Bitwarden API, ensuring smooth integration with official Bitwarden client applications across various platforms.
  
- **Lightweight Design**: Built with minimal resource consumption in mind, Vaultwarden is optimized for low-memory and low-CPU environments, making it suitable for hosting on modest hardware or containers.

- **Self-Hosted Security**: Empowers users to retain full control over their data by hosting the password vault on their own infrastructure, eliminating reliance on third-party servers.

- **SQLite Database Support**: Utilizes SQLite as the default database backend, simplifying setup and maintenance while maintaining performance for most use cases.

- **Optional Features via Environment Variables**: Provides flexibility through configurable features such as disabling user registration, enabling admin pages, and setting up SMTP for email notifications.

- **Web Interface**: Includes a built-in web interface for managing the server, allowing administrators to configure settings and oversee operations directly from their browser.

- **Two-Factor Authentication (2FA)**: Supports robust 2FA methods, including TOTP and FIDO2/WebAuthn, enhancing the security of user accounts.

- **Active Development and Community Support**: Regular updates and contributions from a vibrant open-source community ensure ongoing improvements and timely bug fixes.

- **Cross-Platform Clients**: Compatible with all official Bitwarden clients, including desktop, mobile, and browser extensions, ensuring a consistent and reliable user experience.

Vaultwarden is an excellent choice for individuals or organizations seeking a secure, cost-effective, and customizable password management solution. Its focus on simplicity, compatibility, and resource efficiency makes it a standout option for self-hosted environments.

### Notice

1.  Protect the login address: Set access restrictions to prevent unauthorized direct access.
    
2.  Use a complex password: Create a password that includes uppercase letters, lowercase letters, numbers, and special characters to increase cracking difficulty.
    
3.  Avoid common usernames: Refrain from using common usernames like "admin" or "root" to reduce the risk of brute-force attacks.
    
4.  Regularly change passwords: It is recommended to update your password periodically to mitigate security risks associated with long-term usage of the same password.
    
5.  Enable multi-factor authentication: Adopt two-factor authentication to add an extra layer of security beyond just the password.
    
6.  Limit login attempts: Set a maximum number of failed login attempts, and temporarily lock the account once it is exceeded to prevent brute-force attacks.
    
7.  Configure unusual login notifications: Set up alerts for abnormal login activity to be informed and respond promptly to potential security issues.
    
8.  Conduct regular security audits: Periodically review account security logs and system configurations to quickly identify and fix potential vulnerabilities.
        