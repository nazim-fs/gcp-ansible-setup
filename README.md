# Ansible setup - GCP

## Overview
This repository contains the configurations and scripts used to set up and secure a CentOS 9 instance on Google Cloud Platform (GCP). The following steps were undertaken to ensure proper configuration, security, and access to the instance.

## Report

### DDNS Setup
- **Action**: Registered a free DDNS hostname using No-IP and configured the No-IP DUC client on the server.
- **Explanation**: Dynamic DNS (DDNS) allows you to map a dynamic IP address to a static hostname, making it easier to access your server remotely.

### SSL Certificate
- **Action**: Installed Certbot and obtained a Let’s Encrypt SSL certificate for the domain. Configured Apache to use the SSL certificate and set up automatic renewal.
- **Explanation**: SSL certificates encrypt the data transmitted between the server and clients, ensuring secure communication. Let’s Encrypt provides free SSL certificates, and Certbot automates the process of obtaining and renewing them.

### System Hardening
1. **Updated the System Packages**
   - **Action**: Ensured the system is up to date with the latest security patches and bug fixes.
   - **Explanation**: Regular updates help protect against known vulnerabilities and improve system stability.

2. **Configured the Firewall**
   - **Action**: Configured the firewall to allow only HTTP and HTTPS traffic.
   - **Explanation**: Restricting the firewall to necessary ports minimizes the attack surface and enhances security.

3. **Kernel Hardening**
   - **Action**: Modified kernel parameters to enhance network security.
   - **Explanation**: Kernel hardening settings protect against common network-based attacks and ensure that the system logs suspicious activities.

4. **Auditd Monitoring**
   - **Action**: Installed and configured `auditd` to monitor critical system files and directories.
   - **Explanation**: `auditd` helps track changes to important files, providing an audit trail that can be used to detect and investigate security incidents.

5. **Enabled SELinux**
   - **Action**: Enabled SELinux in enforcing mode.
   - **Explanation**: SELinux enforces mandatory access controls, providing an additional layer of security against unauthorized access.

## Conclusion
The above steps ensure a secure and well-configured CentOS 9 instance, facilitating reliable access and data protection while minimizing potential vulnerabilities. For further details or inquiries, please refer to the individual scripts and configurations present in this repository as well as the terraform configuration in the following respository:

https://github.com/nazim-fs/gcp-terraform-setup
