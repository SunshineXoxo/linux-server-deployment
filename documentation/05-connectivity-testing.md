# 05 – Connectivity Testing

## Objective
To verify communication between the Windows host machine and the Ubuntu Server through VirtualBox NAT port forwarding.

## Network Configuration

The virtual machine used Network Address Translation (NAT).

Port forwarding rules were configured in VirtualBox to allow the host machine to access services running inside the virtual machine.

## Port Forwarding Configuration

| Service | Protocol | Host Port | Guest Port |
|---|---|---:|---:|
| SSH | TCP | 2222 | 22 |
| Apache HTTP | TCP | 8080 | 80 |

## Apache Connectivity Test

1. Started the Ubuntu Server virtual machine.
2. Confirmed that the Apache2 service was running.
3. Opened a web browser on the Windows host machine.
4. Entered the following address:

   `http://localhost:8080`

5. Pressed Enter to access the webpage.

## Test Result

The Apache2 Ubuntu Default Page loaded successfully in the Windows browser.

This confirmed that:

- Apache was running on the Ubuntu Server.
- VirtualBox NAT port forwarding was configured correctly.
- HTTP traffic was successfully forwarded from host port 8080 to guest port 80.

## Conclusion

The connectivity test was successful. The Windows host machine was able to access the webpage hosted by the Ubuntu Server.

This demonstrated successful Linux server deployment and service accessibility.

## Screenshot Evidence

See the successful Apache browser test screenshot in the `screenshots` directory.
