# docker-promtail

Promtail is an agent to push logs to a Grafana Loki instance.

https://grafana.com/docs/loki/latest/send-data/promtail/

This repository is a starter docker-compose to deploy a promtail agent to send logs to a remote loki instance.

Instructions:
- Rename '.env-default' to '.env'
```console
foo@bar:~$ mv .env-default .env
```
- Add the IP address of your loki instance to the environment variable HOST_IP_LOKI
