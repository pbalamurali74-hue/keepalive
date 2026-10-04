# 🟢 GitHub Keepalive Automation

A lightweight GitHub Actions workflow that maintains a daily **heartbeat log** by automatically committing a dated entry to the repository.

## How it works
1. GitHub Actions runs on a daily cron schedule.
2. The workflow appends the current UTC date to `.keepalive`.
3. GitHub Actions commits and pushes the change.
4. The workflow can also be triggered manually with `workflow_dispatch`.

## Tech
GitHub Actions • YAML • Git

## Configuration
Edit:
```
.github/workflows/keep-streak-green.yml
```

The cron schedule can be changed using standard GitHub Actions cron syntax.

## Important note
This repository demonstrates **workflow automation and CI/CD mechanics**. It should not be presented as evidence of active software development by itself.

> Useful as an automation/DevOps learning project; lower priority than the AI/ML projects in my portfolio.