# Crontinel 🟢

**Open-source monitoring for cron jobs, queues, workers, and background tasks.**

Crontinel catches what generic uptime tools miss — the job that crashed silently, the worker that stopped processing, the queue that started backing up at 2am.

## 🚀 Ecosystem

| Project | Description |
|---------|-------------|
| [crontinel](https://github.com/crontinel/crontinel) | Core OSS package — CLI, dashboard, local monitoring |
| [laravel](https://github.com/crontinel/laravel) | Laravel SDK — scheduler + Horizon + queue hooks |
| [app](https://github.com/crontinel/app) | SaaS dashboard — multi-app, team access, long history |
| [landing](https://github.com/crontinel/landing) | Marketing site at [crontinel.com](https://crontinel.com) |
| [docs](https://github.com/crontinel/docs) | Documentation at [docs.crontinel.com](https://docs.crontinel.com) |

## ✨ Features

- **Heartbeat** — 60-second detection of missed runs and silent failures
- **Queue monitoring** — depth per queue, failed job counts, oldest job age
- **Worker health** — per-supervisor status, not just "process is running"
- **Agent monitoring** — tool call loops, model latency, token spend
- **Alerts** — Slack, PagerDuty, email, webhook (HMAC-signed)
- **CI/CD** — `crontinel check` in your deploy pipeline

## 🛠️ One SDK per stack

```bash
npm i @crontinel/node       # Node.js
pip install crontinel        # Python
composer require crontinel/laravel  # Laravel
go get github.com/crontinel/go     # Go
```

## 📊 Status

All systems operational — check [status.crontinel.com](https://status.crontinel.com)
