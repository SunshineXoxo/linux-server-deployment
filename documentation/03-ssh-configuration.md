# 03 – SSH Configuration

## Objective
To configure Secure Shell (SSH) to allow secure remote access to the Ubuntu Server.

## What is SSH?

Secure Shell (SSH) is a network protocol that allows users to securely access and manage remote computers over a network.

SSH uses encryption to protect communication between the client and server.

## Installation

Updated the Ubuntu package list:

```bash
sudo apt update
```

Installed OpenSSH Server:

```bash
sudo apt install openssh-server -y
```

## Starting and Enabling SSH

Started the SSH service:

```bash
sudo systemctl start ssh
```

Enabled SSH to start automatically during system boot:

```bash
sudo systemctl enable ssh
```

## Verification

Checked the SSH service status:

```bash
sudo systemctl status ssh
```

The output displayed:

`Active (running)`

The server was also listening for incoming connections on port 22.

## Network Configuration

SSH uses TCP port 22 by default.

VirtualBox NAT port forwarding was configured as follows:

| Host Port | Guest Port |
|---|---|
| 2222 | 22 |

## Result

OpenSSH Server was successfully installed, enabled and started, allowing the Ubuntu Server to accept SSH connections.

## Screenshot Evidence

See the SSH service status screenshot in the `screenshots` directory.
