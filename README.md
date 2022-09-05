## Overview

This is a working concept of shipping logs from ECS tasks to Grafana Loki. It runs two containers in one ecs task. One container running the app and the other to ship the logs to Grafana Loki. The shipper makes use of the docker image `grafana/fluent-bit-plugin-loki` with fluent bit. Solution is built in CloudFormation

![Architecture](https://github.com/jsantias/grafana-loki/blob/main/images/architecture.png)

## CloudFormation Files

- `ecs.yml` - Deploys an ECS Cluster, a service and a task definition in AWS
- `prometheus.yml` - Configures a prometheus workspace (optional)