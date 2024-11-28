# Monitoring v2
Containerized Grafana stack configured to retrieve host and ~~container~~ metrics from a Linux server. The steps to run the containers are the following:
1. Install Docker (Ubuntu): [Docker](https://docs.docker.com/engine/install/ubuntu/)
2. Install Docker Compose plugin: [Compose](https://docs.docker.com/compose/install/linux/)
3. Clone this repo: `git clone https://github.com/exgolden/Monitoring.git`
4. Move into the Linux directory: `cd Monitoring/Linux`
    
    ~~You can remove the other stacks with `rm -rf Windows`~~
5. Start the Docker Compose file: `docker compose up -d`
6. Check that all containers are healthy: `docker ps` It should return something like this:
    ```
    CONTAINER ID   IMAGE                             COMMAND               CREATED    STATUS       PORTS              NAMES
    xxxx   prom/prometheus:v2.43.0                   "/bin/prometheus --c…"   x ago   Up x   0.0.0.0:9090->9090/tcp   prometheus
    xxxx   grafana/grafana:11.3.1                    "/run.sh"                x ago   Up x   0.0.0.0:3000->3000/tcp   grafana
    xxxx   quay.io/prometheus/node-exporter:v1.8.2   "/bin/node_exporter …"   x ago   Up x   0.0.0.0:9100->9100/tcp   node_exporter
    ```
7. Main components:
    - Grafana: \<ipAddress\>:3000 _default credentials are admin:admin change them ASAP_
    - Prometheus: \<ipAddress\>:9090 _you can check the status of each target inside Status>Targets, it may take a while to load_
    - Node Exporter: \<ipAddress\>:9100 _you can look for specific metrics at \<ipAddress\>:9100/metrics_

---
### Notes
1. Node Simplified may have an error on Disk Total
2. Container monitoring currently on development