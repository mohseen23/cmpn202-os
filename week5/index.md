# Week 5 – Advanced Security Controls

## Objective
This phase is for improving system security through updates.

---

## Automatic Security Updates
We used Ubuntu's upgrades package to aplly security updates automatically.
```bash
sudo apt install unattended-upgrades
sudo dpkg-reconfigure unattended-upgrades
```

Ubuntu was updated without manual intervention.

---

## Intrusion Prevention (Fail2ban)
We selected Fail2ban to protect SSH service against forced logins.
An installation attempt was made using:

```bash
sudo apt install fail2ban
```


---

## Risk Evaluation
SSH access remains protected through
- SSH key-based authentication
- Disabled password authentication
- Disabled root SSH login

These controls reduce risk of forced logins
