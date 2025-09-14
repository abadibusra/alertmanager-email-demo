# Alertmanager Email Demo (with MailHog)

This project shows how to use **Prometheus + Alertmanager** to send alert notifications as emails.  
It uses [MailHog](https://github.com/mailhog/MailHog), a lightweight SMTP server with a web UI that captures all outgoing mail.  

---

## 🚀 Run the Stack

```bash
git clone https://github.com/abadibusra/alertmanager-email-demo.git
cd alertmanager-email-demo
docker-compose up -d
```

Services:

Prometheus → http://localhost:9090
Alertmanager → http://localhost:9093
MailHog → http://localhost:8025

Defined in rules.yml

High CPU Load (CPU > 80% for 2m)

Out of Disk Space (disk < 10% free)

OOM Kill Detected

You can test it the way you want. For CPU stressing I used:
```
while true; do :; sleep 0; done
```
Alerts will appear in MailHog as FIRING and later RESOLVED emails.

<img width="1428" height="726" alt="image" src="https://github.com/user-attachments/assets/3bc59d6d-b7af-4442-955d-e3a171647374" />


<img width="1459" height="674" alt="image" src="https://github.com/user-attachments/assets/c6f19fb0-f1e8-4bfe-b8dc-b63cb82b513c" />
