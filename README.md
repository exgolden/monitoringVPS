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
- loki-data → Log storage


### Notes

1. Node Simplified may have an error on Disk Total
2. Should i add user: "1001" to grafana? i think this is for security reasons
3. When I started Grafana there were two loki DS, one was added by config, maybe the other one
    was added by cache.
4. Migration to Grafana Alloy is being planned
5. Stop new users registration (should work on SMTP before)
6. Cap all container logs