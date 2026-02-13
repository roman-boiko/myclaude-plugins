# Datadog Pricing Agents

Claude Code custom agents for Datadog pricing estimation and technical expertise.

## Agents

### Datadog Pricing Calculator

Estimates Datadog costs based on your infrastructure specifications. Provide your resource details (hosts, containers, log volume, APM spans, etc.) and get a detailed pricing breakdown across tiers and billing periods.

### Datadog Expert

Answers technical questions about the Datadog platform — monitoring setup, APM configuration, log management, dashboards, alerts, integrations, query syntax, best practices, and more.

## Usage

These agents run inside [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Simply ask a Datadog-related question and the appropriate agent will be invoked automatically.

```
# Pricing example
"I have 50 hosts, 200 containers, and need 15GB/day of log ingestion. What would Datadog cost?"

# Technical example
"How do I configure the Datadog Agent to collect custom metrics from a Python app?"
```

## Data

`ddprice.csv` contains Datadog's product pricing across all SKUs, tiers, and billing models. Referenced by the pricing calculator agent for accurate estimates.

## License

[MIT](LICENSE)
