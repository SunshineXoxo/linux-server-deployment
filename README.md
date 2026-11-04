# Linux Server Deployment

## Project Overview

This project demonstrates the deployment and configuration of a Linux server using **Ubuntu Server 24.04.1 LTS** running inside Oracle VirtualBox.

The practical covers virtual machine creation, Linux installation, secure remote access using SSH, web server deployment using Apache2, and connectivity testing.

## Project Objectives

The project was completed in five stages:

1. **Create VM:** Create and configure a virtual machine using Oracle VirtualBox.
2. **Configure Linux:** Install and configure Ubuntu Server 24.04.1 LTS.
3. **Secure Access:** Install and configure OpenSSH Server for secure remote access.
4. **Deploy Service:** Install and run the Apache2 web server.
5. **Test Connectivity:** Configure network port forwarding and verify access to the deployed website.

## Technologies Used

| Technology | Purpose |
|---|---|
| Oracle VirtualBox | Virtualisation |
| Ubuntu Server 24.04.1 LTS | Operating system |
| OpenSSH Server | Secure remote access |
| Apache2 | Web server |
| Windows | Host operating system |
| NAT | Virtual machine networking |

## Implementation

### 1. Virtual Machine Creation

A virtual machine named `Linux-Server` was created using Oracle VirtualBox.

The virtual machine was configured with:
- Operating System: Ubuntu Server 64-bit
- RAM: 2 GB
- Storage: 25 GB
- Network Adapter: NAT

### 2. Ubuntu Server Installation

Ubuntu Server 24.04.1 LTS was installed inside the virtual machine.

The installation included:
- Language selection.
- Network configuration.
- Ubuntu archive mirror configuration.
- System installation.
- User account creation.

The installation was completed successfully, and the server was accessed through the Ubuntu terminal.

### 3. Secure Access Using SSH

OpenSSH Server was installed to enable secure remote access.

Installation command:

```bash
sudo apt update
sudo apt install openssh-server -y
```

The SSH service was enabled and started:

```bash
sudo systemctl enable ssh
sudo systemctl start ssh
```

The service was verified using:

```bash
sudo systemctl status ssh
```

The service displayed `active (running)`, confirming successful operation.

SSH listens on port 22.

### 4. Apache Web Server Deployment

Apache2 was installed to host a website on the Ubuntu Server.

Installation command:

```bash
sudo apt install apache2 -y
```

The service was started and enabled:

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

The service status was checked using:

```bash
sudo systemctl status apache2
```

The output confirmed that Apache2 was `active (running)`.

### 5. Connectivity Testing

The virtual machine used NAT networking.

Port forwarding was configured in VirtualBox to allow the Windows host to communicate with services running inside the Ubuntu virtual machine.

| Service | Protocol | Host Port | Guest Port |
|---|---|---:|---:|
| Apache HTTP | TCP | 8080 | 80 |
| SSH | TCP | 2222 | 22 |

The Apache web server was tested through a Windows web browser using:

**http://localhost:8080**

The Apache2 Ubuntu Default Page loaded successfully, confirming that the web server was accessible from the host machine.

## Project Results

All five project objectives were successfully completed.

- Ubuntu Server was installed and configured.
- OpenSSH Server was successfully installed and started.
- Apache2 was successfully deployed.
- VirtualBox NAT port forwarding was configured.
- The Apache default webpage was successfully accessed from Windows.

## Screenshots and Evidence

Screenshots demonstrating the implementation and successful completion of the project are available in the [`screenshots`](screenshots/) directory.

## Conclusion

This practical provided hands-on experience in Linux server deployment, virtualisation, server administration, secure remote access, web hosting, and network connectivity.

The successful deployment and testing of Apache2 demonstrated the ability to configure a Linux server and make its hosted service accessible from another operating system.

---

**Project:** Linux Server Deployment  
**Operating System:** Ubuntu Server 24.04.1 LTS  
**Web Server:** Apache2  
**Remote Access:** OpenSSH
