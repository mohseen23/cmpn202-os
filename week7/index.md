# Week 7 – Security Audit and Evaluation

## Lynis audit (installation attempt)
I tried to intsall it:

```bash
sudo apt install lynis
```

But the installation failed due to Host-only network configuration

---

## Running services review
```bash
sudo ss -tulpn
```

```bash
sudo systemctl --type=service --state=running --no-pager
```

Minimizing the exposed services to reduce attack.

---

## Network exposure assessment (nmap)
A nmap scan within the Host only network was done

```bash
nmap -sS 192.168.56.101
```
The scan showed that only SSH is rechable.


---

## Risk evaluation
Key controls implemented:
- SSH key-based authentication
- Password authentication disabled
- Root SSH login disabled
- Minimal exposed services

Remaining risks are becaues of pending updates due to network issues.
