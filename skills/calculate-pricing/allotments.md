# Product Allotments Reference

Many Datadog products include baseline allotments that are bundled with the parent product at no extra cost. When calculating pricing, you MUST subtract included allotments before pricing any overages. Allotments are calculated account-wide (not per-host). For example, 50 Infrastructure Pro hosts include 250 total containers (50 × 5) — only containers above 250 are billed separately.

Source: https://www.datadoghq.com/pricing/allotments/

## Infrastructure Monitoring

| Parent Product | Allotment | Monthly (per host) | Hourly (per host) |
|---|---|---|---|
| Infrastructure Pro | Custom Metrics | 100 | 100 |
| Infrastructure Pro | Ingested Custom Metrics | 100 | 100 |
| Infrastructure Pro | Containers | 5 | 5 |
| Infrastructure Pro | Custom Events | 500 | 0.68 |
| Infrastructure Enterprise | Custom Metrics | 200 | 200 |
| Infrastructure Enterprise | Ingested Custom Metrics | 200 | 200 |
| Infrastructure Enterprise | Containers | 10 | 10 |
| Infrastructure Enterprise | Custom Events | 1,000 | 1.37 |

## Infrastructure DevSecOps

| Parent Product | Allotment | Monthly (per host) | Hourly (per host) |
|---|---|---|---|
| DevSecOps Pro | Custom Metrics | 100 | 100 |
| DevSecOps Pro | Ingested Custom Metrics | 100 | 100 |
| DevSecOps Pro | Containers | 5 | 5 |
| DevSecOps Pro | Custom Events | 500 | 0.68 |
| DevSecOps Pro | Workflow Automation | 5 | 0.0068 |
| DevSecOps Enterprise | Custom Metrics | 200 | 200 |
| DevSecOps Enterprise | Ingested Custom Metrics | 200 | 200 |
| DevSecOps Enterprise | Containers | 10 | 10 |
| DevSecOps Enterprise | Custom Events | 1,000 | 1.37 |
| DevSecOps Enterprise | Workflow Automation | 20 | 0.027 |

## IoT

| Parent Product | Allotment | Monthly (per device) | Hourly (per device) |
|---|---|---|---|
| IoT | Custom Metrics | 20 | 20 |
| IoT | Ingested Custom Metrics | 20 | 20 |

## APM

| Parent Product | Allotment | Monthly (per APM host) | Hourly (per APM host) |
|---|---|---|---|
| APM | Indexed Spans | 1,000,000 | 1,370 |
| APM | Ingested Spans | 150 GB | 0.205 GB |
| APM Pro | Indexed Spans | 1,000,000 | 1,370 |
| APM Pro | Ingested Spans | 150 GB | 0.205 GB |
| APM Pro | Data Streams Monitoring | 1 DSM host | 1 DSM host |
| APM Enterprise | Indexed Spans | 1,000,000 | 1,370 |
| APM Enterprise | Ingested Spans | 150 GB | 0.205 GB |
| APM Enterprise | Data Streams Monitoring | 1 DSM host | 1 DSM host |
| APM Enterprise | Continuous Profiler | 1 profiled host | 1 profiled host |
| APM Enterprise | Profiled Containers | 4 | 4 |

## Fargate

| Parent Product | Allotment | Monthly (per task) | Hourly (per task) |
|---|---|---|---|
| Fargate (APM) | Indexed Spans | 65,000 | 89.04 |
| Fargate (APM) | Ingested Spans | 10 GB | 0.0137 GB |
| Fargate (APM Enterprise) | Indexed Spans | 65,000 | 89.04 |
| Fargate (APM Enterprise) | Ingested Spans | 10 GB | 0.0137 GB |
| Fargate Task (Continuous Profiler) | Profiled Task | 1 | 1 |

## Serverless

| Parent Product | Allotment | Monthly (per unit) | Hourly (per unit) |
|---|---|---|---|
| Serverless Functions APM | Indexed Spans | 300,000 per 1M invocations | 300,000 per 1M invocations |
| Serverless Functions APM | Ingested Spans | 50 GB per 1M invocations | 50 GB per 1M invocations |
| Serverless Workload Monitoring - Functions | Custom Metrics | 5 per function | 5 per function |
| Serverless Workload Monitoring - Functions | Ingested Custom Metrics | 5 per function | 5 per function |
| Serverless Workload Monitoring - Apps | Custom Metrics | 20 per instance app | 20 per instance app |
| Serverless Workload Monitoring - Apps | Ingested Custom Metrics | 20 per instance app | 20 per instance app |
| Serverless Application APM | Indexed Spans | 195,000 per app | 195,000 per app |
| Serverless Application APM | Ingested Spans | 30 GB per app | 30 GB per app |
| Serverless App and API Protection | Indexed Spans | 300,000 per instance app | 300,000 per instance app |
| Serverless App and API Protection | Ingested Spans | 50 GB per instance app | 50 GB per instance app |

## Profiling & Database Monitoring

| Parent Product | Allotment | Monthly (per unit) | Hourly (per unit) |
|---|---|---|---|
| Continuous Profiler | Profiled Containers | 4 per profiled host | 4 per profiled host |
| Database Monitoring | Normalized Queries | 200 per database host | 200 per database host |

## Software Delivery

| Parent Product | Allotment | Monthly (per committer) | Hourly (per committer) |
|---|---|---|---|
| Pipeline Visibility | Pipeline Spans | 400,000 | 547.95 |
| Test Optimization | Test Spans | 1,000,000 | 1,370 |
| Code Coverage | Committer | 1 | 1 |
| Static Code Analysis (SAST) | Code Coverage | 1 | 1 |
| Code Security Bundle | Code Coverage | 1 | 1 |

## Cloud Security Management (CSM)

| Parent Product | Allotment | Monthly (per host) | Hourly (per host) |
|---|---|---|---|
| CSM Pro | CSM Pro Containers | 5 | 5 |
| CSM Pro | Workflow Automation | 5 | 0.0068 |
| CSM Enterprise | CSM Enterprise Containers | 20 | 20 |
| CSM Enterprise | Workflow Automation | 20 | 0.027 |
| Workload Protection | Workload Protection Containers | 4 | 4 |

## Allotment Calculation Rules

1. **Account-wide aggregation**: Allotments pool across all hosts/units on the account. Example: 50 Pro hosts = 250 total container allotment, regardless of per-host distribution.
2. **Overage billing**: Usage above the allotment is billed at the applicable on-demand or committed rate from `ddprice.csv`.
3. **Excluded from counts**: Datadog Agent containers and Kubernetes pause containers (Agent v7.20+) do not count against container allotments.
4. **Containers use hourly metering**: Container allotments are measured hourly, not monthly.
5. **Always show allotments in output**: When generating estimates, always show the user their total allotment, their usage, and whether they are within or over the allotment for each applicable product.
