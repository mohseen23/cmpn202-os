# Week 1 – Planning & System Setup

## Architecture Overview
This coursework uses a two-system architecture:
- **Server:** Ubuntu Server 22.04 LTS (headless)
- **Workstation:** Windows host machine
- **Virtualisation:** Oracle VirtualBox
- **Network:** Host-only Adapter

  
The server is administered through ssh from the workstation.

## System Configuration Evidence

### Kernel & OS
```bash
 uname -a
Linux cmpn-server 6.8.0-90-generic #91-Ubuntu SMP PREEMPT_DYNAMIC Tue Nov 18 14:14:30 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux
```

```bash
lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.3 LTS
Release:        24.04
Codename:       noble
```

### Memory Configuration
```bash
free -h
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       312Mi       1.5Gi       1.0Mi       220Mi       1.6Gi
Swap:          1.9Gi          0B       1.9Gi

This server has a ram of 2 GB, and has low memory after initial boot.
```
### Storage Configuration
```bash
df -h
Filesystem                         Size  Used Avail Use% Mounted on
/dev/mapper/ubuntu--vg-ubuntu--lv  9.8G  4.4G  4.9G  48% /
```
The server uese virtual disk for the root filesystem.


### Network Configuraion
```bash
ip addr
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP>
    inet 192.168.56.101/24 scope global dynamic enp0s3
```

The server is connected to Host-only network which enables isolated ssh access from workstation.
