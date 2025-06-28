# 0x08. Networking Basics #2

This project covers basic networking concepts and practical Bash scripting tasks related to networking on Linux systems.

## Learning Objectives

- Understand the concepts of localhost (127.0.0.1) and 0.0.0.0
- Learn about the `/etc/hosts` file and its role in hostname resolution
- Display active network interfaces and attached IPv4 addresses
- Use Bash scripts to configure and inspect network settings
- Use netcat to listen on network ports

## Files

| Filename                      | Description                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------|
| `0-change_your_home_IP`        | Script to modify `/etc/hosts` so that `localhost` resolves to `127.0.0.2` and `facebook.com` to `8.8.8.8` |
| `1-show_attached_IPs`          | Script to display all active IPv4 IP addresses on the machine                                   |
| `100-port_listening_on_localhost` | Script that listens on localhost port 98 and outputs any received text                         |

## Usage

### 0-change_your_home_IP
Modifies `/etc/hosts` entries. Must be run with superuser privileges:
```bash
sudo ./0-change_your_home_IP
