# 04 – Apache Web Server Deployment

## Objective
To deploy an Apache web server on Ubuntu Server and host a basic webpage.

## What is Apache?

Apache HTTP Server is open-source web server software used to deliver web pages and other web content to clients over HTTP and HTTPS.

## Installation

Installed Apache2 using:

```bash
sudo apt install apache2 -y
```

## Starting and Enabling Apache

Started the Apache service:

```bash
sudo systemctl start apache2
```

Enabled Apache to start automatically when the server boots:

```bash
sudo systemctl enable apache2
```

## Verification

Checked the Apache service status:

```bash
sudo systemctl status apache2
```

The output displayed:

`Active (running)`

This confirmed that Apache was running successfully.

## Network Configuration

Apache uses TCP port 80 by default for HTTP traffic.

VirtualBox NAT port forwarding was configured:

| Host Port | Guest Port |
|---|---|
| 8080 | 80 |

## Result

Apache2 was successfully installed and started on the Ubuntu Server.

The default Apache webpage was made accessible through the Windows host browser.

## Screenshot Evidence

See the Apache service status screenshot in the `screenshots` directory.
