# Setup

```bash
docker compose up -d
docker exec -it mosq sh
cd /mosquitto/config
touch mosquitto.passwd
mosquitto_passwd -b mosquitto.passwd user password
exit
docker compose down && docker compose up -d
```
