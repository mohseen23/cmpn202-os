# Week 4 – SSH Hardening and Secure Access

## Objective
I secured administration of server by strong authentication controls.

## SSH Key-Based Authentication

An ED25519 key pair was generated and copied to the server and stored in `~/.ssh/authorized_keys` file which allowed SSh access without use of password.

## SSH Configuration Hardening
The SSH daemon configuration was modified to disable insecure access methods and enforce best practices for remote administration.

The following setting was applied:

```bash
sudo sshd -T | grep -E "passwordauthentication|permitrootlogin|pubkeyauthentication"

permitrootlogin no
pubkeyauthentication yes
passwordauthentication no
```


