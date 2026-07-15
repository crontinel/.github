# Crontinel

Open-source monitoring for cron jobs, queues, workers, and background tasks.

Crontinel catches what generic uptime tools miss: the job that crashed silently, the worker that stopped processing, the queue that started backing up at 2am.

[![Web](https://img.shields.io/badge/Web-crontinel.com-brightgreen)](https://crontinel.com)
[![Docs](https://img.shields.io/badge/Docs-docs.crontinel.com-blue)](https://docs.crontinel.com)
[![SaaS](https://img.shields.io/badge/SaaS-app.crontinel.com-purple)](https://app.crontinel.com)
[![Status](https://img.shields.io/badge/Status-status.crontinel.com-green)](https://status.crontinel.com)
[![X](https://img.shields.io/badge/X-%40crontinel-black)](https://x.com/crontinel)
[![GitHub](https://img.shields.io/badge/Repo-crontinel%2Fcrontinel-181717)](https://github.com/crontinel/crontinel)
[![License](https://img.shields.io/badge/License-MIT-yellow)](https://github.com/crontinel/crontinel/blob/main/LICENSE)

---

## What We Monitor

- Heartbeat - 60 second detection of missed runs
- Queue depth - per-queue counts, oldest job age
- Worker health - per-supervisor status
- Agent runs - tool calls, model latency
- CI/CD - `crontinel check` in your deploy pipeline

## SDKs

```
npm i @crontinel/node       # Node.js
pip install crontinel        # Python
composer require crontinel/laravel  # Laravel
go get github.com/crontinel/go     # Go
```

## Links

- [Website](https://crontinel.com) - Marketing site & signup
- [App](https://app.crontinel.com) - Hosted SaaS dashboard
- [Docs](https://docs.crontinel.com) - Setup guides
- [Status](https://status.crontinel.com) - System status
- [X/Twitter](https://x.com/crontinel) - Product updates
- [Main Repo](https://github.com/crontinel/crontinel) - Full README with all SDKs and ecosystem
