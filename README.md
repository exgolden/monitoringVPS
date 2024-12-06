# Monitoring VPS

Containerized Grafana stack configured to retrieve host and ~~container~~ metrics from a Linux server.
The main components are:

- Grafana: http://grafana:3000 - Prometheus: http://prometheus:9090

- Node Exporter: http://node*exporter:9100 \_you can look for specific metrics at http:node_exporter:9100/metrics*
  _Address are under the docker network, to acces each component outside the
  network you need to use http://localhost:\<port\>_

---

### Notes

1. Node Simplified may have an error on Disk Total
2. Container monitoring currently on development

