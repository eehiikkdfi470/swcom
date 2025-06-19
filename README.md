# Observability Stack Setup

## Overview

This repository provides a reusable GitOps-aligned observability solution tailored for Kubernetes environments. It is designed for seamless deployment and scalability across multiple clusters with minimal configuration.
Observability stack consists of Open Telemetry and LGTM Stack.

### Key Features

- **Kubernetes Cluster Setup**: Local development and testing using Kind.
- **Demo Application** Java app (Petclinic) instrumented for telemetry.
- **OpenTelemetry Collector**: Configured for scraping metrics, traces, and logs from Demo application and metrics from cluster (Node exporter metrics).
- **Observability Stack**: Includes Loki, Mimir, Tempo, and Grafana.
- **Grafana Cloud Integration**: Centralized observability with export capabilities.
- Create Dashbaords for visualization
- **Infrastructure Alerts**: Predefined alerts with runbooks.
- **Application SLOs and Alerts**: Service-level objectives and alerting mechanisms.

## Prerequisites

- A Kubernetes cluster (Kind is used in this demo, but any Kubernetes cluster is supported).
- `kubectl` installed and configured to interact with your cluster.
- `kustomize` CLI (version 5 or later recommended for Helm support).
- Helm CLI installed (required for certain Helm-based integrations).
- Access to a free Grafana Cloud account (for telemetry visualization).

## Assumptions and Decisions

- **Cluster Choice**: Kind is used for local testing due to its simplicity and reproducibility.
- **Demo Application**: A Java application auto-instrumented with OpenTelemetry for generating real telemetry data.
- **Telemetry Export**: Configured to export telemetry data to Grafana Cloud.
- **GitOps**: Argo CD is used to demonstrate best practices in continuous deployment and configuration management.
- Non HA set up.
