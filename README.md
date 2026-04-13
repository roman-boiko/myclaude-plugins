# Datadog Pricing Agents

Claude Code custom skills for Datadog pricing estimation and technical expertise.

## Skills

### Datadog Pricing Calculator (`/calculate-pricing`)

Estimates Datadog costs based on your infrastructure specifications. Provide your resource details (hosts, containers, log volume, APM spans, etc.) and get a detailed pricing breakdown across tiers and billing periods.

### Datadog Expert (`/datadog-expert`)

Answers technical questions about the Datadog platform — monitoring setup, APM configuration, log management, dashboards, alerts, integrations, query syntax, best practices, and more.

## Usage

These skills run inside [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Invoke them directly with slash commands or ask a Datadog-related question and the appropriate skill will be invoked automatically.

```
# Pricing example
/calculate-pricing 50 hosts, 200 containers, and 15GB/day of log ingestion

# Technical example
/datadog-expert How do I configure the Datadog Agent to collect custom metrics from a Python app?
```

## Data

`ddprice.csv` contains Datadog's product pricing across all SKUs, tiers, and billing models. Referenced by the pricing calculator skill for accurate estimates.

## License

[MIT](LICENSE)
