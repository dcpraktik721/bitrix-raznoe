# SSH_ACCESS_CHECK

## Result: CONSOLE_ACCESS_OK (serial TTY; SSH port 22 not directly tested)

| Parameter | Value |
|---|---|
| Access method | Timeweb web serial console |
| SSH port 22 test | NOT tested (no SSH client in browser env) |
| Login prompt | prod login: |
| User | root |
| Auth result | SUCCESS |
| Shell after login | BitrixVA menu 9.0.9 -> exit 0 -> /bin/bash |
| Hostname in shell | prod.praktik72.ru |
| OS | CentOS Stream release 9 |
| Kernel | 5.14.0-681.el9.x86_64 |
| IP eth0 | 5.42.104.148 |
| Bitrix VA version | 9.0.9 |
| SSH string (panel) | ssh root@5.42.104.148 |
| sshd status | ASSUMED running (standard Timeweb Bitrix image) |

## Note

For full SSH transport confirmation run from external host:
```
ssh root@5.42.104.148 -v
```

## Verdict
Console access: OK. SSH port 22: ASSUMED OK, needs separate confirmation.
