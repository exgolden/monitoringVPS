# Observability stack
This repository contains a Docker based monitoring stack built around Prometheus 
and Grafana, extended with log monitoring using Loki.

The stack provides:
- Metrics collection (Prometheus)
- Host metrics (Node Exporter)
- Container metrics (cAdvisor)
- HTTP/endpoint monitoring (Blackbox Exporter)
- Log aggregation (Loki)
- Log shipping from Docker (Promtail)
- Visualization & alerting (Grafana)

All services run inside a shared external Docker network: **saas_network**.

### Persistent volumes
- prometheus-data → Prometheus TSDB
- grafana-data → Dashboards, alert rules, state
- ./loki/data → Log storage


### Notes

1. Node Simplified may have an error on Disk Total
2. Container monitoring currently on development
3. Only Grafana service is accesibñe to general public
4. Should i add user: "1001" to grafana? i think this is for security reasons
