# Description

If you have multiple Ubuntu prod instances, How would you monitor them? What would be your monitoring strategy?

I would use Prometheus and Grafana to monitor multiple Ubuntu instances in the cloud.
This repository aims to represent a small example on how I would do it, on this repository I am only monitoring my local computer but in a real world use case I would use different prometheus targets to monitor multiple VM instances.

This tool uses docker compose to spawn a grafana, prometheus and a node-exporter instance, the node-exporter is gathering metrics like CPU, Memoery usage from my local computer and then are scraped by prometheus and Grafana queries them to display them in a Dashboard.

![Alt text](arch.png?raw=true "Architecture")

# Usage

1. `docker compose -f docker-compose.yaml up`
2. Navigate to `http://127.0.0.1:3000`
2. Login in with `admin` & `admin`

Once inside Grafana you can go to Dashbaords -> dashboard.json -> Ubuntu server monitoring
This will dispaly all the metrics from your localc omputer
