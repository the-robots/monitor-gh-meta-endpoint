# monitor-gh-meta-endpoint
This repository uses a scheduled GitHub Actions workflow to track changes to the https://api.github.com/meta endpoint. If any changes are detected, it sends a webhook notification (e.g., to Slack, Discord, or another alerting system). Useful for teams managing firewall rules, webhook IP allow lists, or GitHub Actions runner access.
