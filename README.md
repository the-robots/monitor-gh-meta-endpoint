# monitor-gh-meta-endpoint

This repository contains a GitHub Actions workflow that continuously monitors the [GitHub Meta API](https://api.github.com/meta) for changes to IP address ranges used by GitHub services (e.g., Actions, Webhooks, API, Pages, etc.).

When a change is detected, the workflow:
- Generates a detailed summary of added and removed IPs.
- Creates an issue documenting the changes (with optional Slack/webhook support).
- Updates a local snapshot (`.meta.last.json`) to serve as the new baseline for future comparisons.

This tool is useful for teams managing:
- Network firewall rules
- GitHub Actions runner IP allowlists
- Webhook IP filtering and whitelisting

## Features

- Hourly scheduled polling of the GitHub Meta API
- Inline IP diff report with change summary
- Issue auto-creation with labels
- Baseline management via committed snapshots
- Easily extensible to notify via Slack, Discord, or other systems

> Designed for operational awareness and automated response to GitHub infrastructure IP changes.
