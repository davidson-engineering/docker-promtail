# docker-promtail

Promtail is an agent to push logs to a Grafana Loki instance.

https://grafana.com/docs/loki/latest/send-data/promtail/

This repository is a starter docker-compose to deploy a promtail agent to send logs to a remote loki instance.

Instructions:
- Add the IP address of your loki instance to the environment variable HOST_IP_LOKI
```console
foo@bar:~$ echo "HOST_IP_LOKI = 10.0.0.1" >> .env
```
- Setup your scrape configs in config/config.yaml

```yaml
scrape_configs:
- job_name: my_logging_job
  static_configs:
  - targets:
      - loki
    labels:
      job: my_logging_job
      __path__: /path/to/logs/*.log
```
