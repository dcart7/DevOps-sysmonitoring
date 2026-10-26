# Linux Server Monitoring

I’m building this project to learn how server monitoring works in practice and get more familiar with DevOps tools.

#### The goal is to collect system metrics, visualize them in Grafana, and check whether external websites are available.

Tools

* Docker & Docker Compose
* Prometheus
* Grafana
* Node Exporter
* Blackbox Exporter

## What’s implemented

* Prometheus setup
* Node Exporter metrics collection
* Grafana dashboard
* CPU and RAM monitoring
* Disk usage monitoring
* Network traffic monitoring
* Website availability checks
* Website response time monitoring
* Basic Prometheus status panel
* Initial website availability alert rule

## Dashboard

The Grafana dashboard currently includes CPU usage, RAM usage, disk usage, network traffic, Prometheus status, website availability, and website response time.

## Run locally

Make sure Docker Desktop or Docker Engine is running.

### Clone the repository:

git clone https://github.com/dcart7/DevOps-sysmonitoring.git
cd DevOps-sysmonitoring

### Navigate to the directory containing docker-compose.yml and start the services:

docker compose up -d

### Check the running containers:

docker compose ps

#### Local endpoints

Service	URL
Prometheus	http://localhost:9090
Prometheus Targets	http://localhost:9090/targets
Grafana	http://localhost:3000
Node Exporter	http://localhost:9100/metrics
Blackbox Exporter	http://localhost:9115

I’m using this project to get hands-on experience with Docker, Prometheus, Grafana, PromQL, exporters, and basic alerting.

I’m still working on it and plan to improve the alerts, add notifications, and eventually deploy the monitoring stack on a Linux server.

Note

I’m currently developing and testing the stack on macOS using Docker Desktop. Node Exporter metrics come from the Linux environment available to the container and should not be treated as complete native macOS host metrics.
