``` bash
 sudo sshd -T | grep -E "passwordauthentication|permitrootlogin|pubkeyauthentication"
[sudo] password for adminuser:
permitrootlogin no
pubkeyauthentication yes
passwordauthentication no
```
