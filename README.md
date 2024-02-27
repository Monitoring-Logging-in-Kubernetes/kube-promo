# kube-promo
Setup Prometheus Monitoring On Kubernetes Cluster

### About Prometheus 

Prometheus stands as a highly scalable open-source monitoring framework, specifically designed to cater to the needs of the Kubernetes container orchestration platform. Its popularity in the realm of observability is rapidly growing due to its robust metric gathering and alerting capabilities.

#### Key Features of Prometheus:

`Metric Collection:` Prometheus adopts a pull model for fetching metrics via HTTP. Additionally, there exists the option to push metrics to Prometheus through Pushgateway, particularly useful for scenarios where direct metric scraping by Prometheus is not feasible. One such scenario involves gathering custom metrics from ephemeral Kubernetes jobs and Cronjobs.

`Metric Endpoint:` Systems intended for monitoring via Prometheus must expose their metrics on an /metrics endpoint. This endpoint serves as the access point for Prometheus to retrieve metrics at regular intervals.

`PromQL:` Prometheus is equipped with PromQL, a highly versatile query language utilized for querying metrics within the Prometheus dashboard. PromQL queries are instrumental not only for the Prometheus UI but also for visualizing metrics in Grafana.

`Prometheus Exporters:` Exporters function as intermediary libraries that translate metrics from third-party applications into the Prometheus metrics format. An array of official and community-driven Prometheus exporters exists, exemplified by the Prometheus node exporter, which provides Prometheus-formatted access to all Linux system-level metrics.

`TSDB (Time-Series Database):` Prometheus employs a TSDB for efficient data storage. By default, data is stored locally. However, to mitigate single points of failure, provisions exist for integrating remote storage solutions with Prometheus TSDB.

#### Prometheus Monitoring Setup on Kubernetes

Assume that you have a kubernetes cluster up and running with kubectl setup on your workstation.

