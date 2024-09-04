# Networking Basics 2

This project is focused on further understanding the fundamentals of networking, particularly around hostnames, IP addresses, and network tools. You'll learn how to manipulate network settings on an Ubuntu server, use essential network tools, and configure network connections.

## Resources
Read or watch:
- [What is localhost](https://en.wikipedia.org/wiki/Localhost)
- [What is 0.0.0.0](https://en.wikipedia.org/wiki/0.0.0.0)
- [What is the hosts file](https://en.wikipedia.org/wiki/Hosts_(file))
- [Netcat examples](https://www.lifewire.com/netcat-linux-command-4095916)

Commands to check with `man` or `help`:
- `ifconfig`
- `telnet`
- `nc`
- `cut`

## Learning Objectives
By the end of this project, you should be able to explain the following concepts to anyone:

### General
- What is `localhost` / `127.0.0.1`
- What is `0.0.0.0`
- What is `/etc/hosts`
- How to display your machine’s active network interfaces

## Requirements
- **Allowed editors**: `vi`, `vim`, `emacs`
- All your files will be interpreted on Ubuntu 20.04 LTS
- All your files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- All your Bash script files must be executable
- Your Bash scripts must pass Shellcheck (version 0.7.0 via `apt-get`) without any errors
- The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
- The second line of all your Bash scripts should be a comment explaining what the script does

## Tasks

<details>
<summary><strong>0. Change your home IP</strong> (click to expand)</summary>

Write a Bash script that configures an Ubuntu server with the following requirements:

- `localhost` resolves to `127.0.0.2`
- `facebook.com` resolves to `8.8.8.8`

**Example:**

Before running the script:
```bash
sylvain@ubuntu$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
...

<details>
<summary><strong>1. Show attached IPs</strong> (click to expand)</summary>

Write a Bash script that displays all active IPv4 IPs on the machine it’s executed on.

**Example:**

```bash
sylvain@ubuntu$ ./1-show_attached_IPs | cat -e
10.0.2.15$
127.0.0.1$
sylvain@ubuntu$

<details>
<summary><strong>2. Port listening on localhost</strong> (click to expand)</summary>

Write a Bash script that listens on port 98 on localhost.

### Example:

**Terminal 0: Start the script:**

```bash
sylvain@ubuntu$ sudo ./2-port_listening_on_localhost

