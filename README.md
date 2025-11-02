# alu-system_engineering-devops
# SSH Project

This project includes Bash scripts for SSH operations, such as connecting to remote servers, generating SSH key pairs, and configuring SSH clients.

## Description

This project is part of the ALU System Engineering & DevOps curriculum. It focuses on understanding and implementing SSH (Secure Shell) connections to remote servers using RSA key pair authentication.

## Learning Objectives

By completing this project, I have learned:

- What a server is and where servers usually live
- What SSH is and how it works
- How to create an SSH RSA key pair
- How to connect to a remote host using an SSH RSA key pair
- The advantage of using `#!/usr/bin/env bash` instead of `/bin/bash`
- How to configure SSH client for passwordless authentication

## Environment

- **Operating System:** Ubuntu 20.04 LTS
- **Editors Used:** vi, vim, emacs
- **Shell:** Bash

## Requirements

- All files end with a new line
- All Bash script files are executable
- First line of all Bash scripts: `#!/usr/bin/env bash`
- Second line of all Bash scripts: A comment explaining what the script does

## Project Structure

```
ssh/
├── README.md
├── 0-use_a_private_key
├── 1-create_ssh_key_pair
└── 2-ssh_config
```

## Tasks

### 0. Use a private key
**File:** `0-use_a_private_key`

A Bash script that uses SSH to connect to a server using the private key `~/.ssh/school` with the user `ubuntu`.

**Usage:**
```bash
./0-use_a_private_key
```

### 1. Create an SSH key pair
**File:** `1-create_ssh_key_pair`

A Bash script that creates an RSA key pair with the following specifications:
- Private key name: `school`
- Key size: 4096 bits
- Passphrase: `betty`

**Usage:**
```bash
./1-create_ssh_key_pair
```

### 2. Client configuration file
**File:** `2-ssh_config`

SSH client configuration file that:
- Uses the private key `~/.ssh/school`
- Refuses to authenticate using a password

**Usage:**
This configuration can be added to `~/.ssh/config` for automatic application.

### 3. Let me in!
Added the provided SSH public key to the server's `~/.ssh/authorized_keys` file to allow connection using the `ubuntu` user.

## Author

ALU Student - System Engineering & DevOps

## Repository

- **GitHub repository:** alu-system_engineering-devops
- **Directory:** ssh
