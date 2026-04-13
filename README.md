# Datadog Pricing Plugin for Claude Code

A Claude Code plugin for Datadog pricing estimation and technical expertise.

## Installation

```bash
# From marketplace
/plugin install dd-pricing

# Local testing
claude --plugin-dir /path/to/dd-pricing-agents
```

## Skills

### Pricing Calculator (`/dd-pricing:calculate-pricing`)

Estimates Datadog costs based on your infrastructure specifications. Provide your resource details (hosts, containers, log volume, APM spans, etc.) and get a detailed pricing breakdown across tiers and billing periods.

### Datadog Expert (`/dd-pricing:datadog-expert`)

Answers technical questions about the Datadog platform — monitoring setup, APM configuration, log management, dashboards, alerts, integrations, query syntax, best practices, and more.

## Usage

Invoke skills directly with slash commands or ask a Datadog-related question and the appropriate skill will be invoked automatically.

```
# Pricing example
/dd-pricing:calculate-pricing 50 hosts, 200 containers, and 15GB/day of log ingestion

# Technical example
/dd-pricing:datadog-expert How do I configure the Datadog Agent to collect custom metrics from a Python app?
```

## Data

`ddprice.csv` contains Datadog's product pricing across all SKUs, tiers, and billing models. Referenced by the pricing calculator skill for accurate estimates.

## License

[MIT](LICENSE)
