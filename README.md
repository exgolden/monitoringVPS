# Monitoring VPS

Containerized Grafana stack configured to retrieve host and ~~container~~ metrics from a Linux server.
The main components _inside docker network_ are:

- Grafana: http://grafana:3000

- Prometheus: http://prometheus:9090

- Node Exporter: http://node_exporter:9100

---

### Notes

1. Node Simplified may have an error on Disk Total
2. Container monitoring currently on development
3. Only Grafana service is accesibñe to general public
4. Should i add user: "1001" to grafana? i think this is for security reasons
