# Crontinel

**Open-source monitoring for cron jobs, queues, workers, and background tasks.**

Crontinel catches what generic uptime tools miss: the job that crashed silently, the worker that stopped processing, the queue that started backing up at 2am. A URL returning 200 does not mean your background tasks are healthy.

[![Website](https://img.shields.io/badge/Web-crontinel.com-brightgreen)](https://crontinel.com)
[![Docs](https://img.shields.io/badge/Docs-docs.crontinel.com-blue)](https://docs.crontinel.com)
[![SaaS](https://img.shields.io/badge/SaaS-app.crontinel.com-purple)](https://app.crontinel.com)
[![Status](https://img.shields.io/badge/Status-status.crontinel.com-green)](https://status.crontinel.com)
[![X](https://img.shields.io/badge/X-%40crontinel-black)](https://x.com/crontinel)
[![License](https://img.shields.io/badge/License-MIT-yellow)](https://github.com/crontinel/crontinel/blob/main/LICENSE)
[![CI](https://github.com/crontinel/laravel/actions/workflows/ci.yml/badge.svg)](https://github.com/crontinel/laravel/actions/workflows/ci.yml)

---

## Why Crontinel?

Most monitoring tools check if your website is up. Crontinel checks if your **background jobs are actually running**.

| What breaks | What you see | Crontinel sees |
|-------------|-------------|----------------|
| Horizon supervisor paused | "Site is up" | Supervisor status, failed jobs/min |
| Queue backing up | "Site is up" | Depth per queue, oldest job age |
| Cron job crashing | "Site is up" | Exit code, duration, late detection |
| Worker stopped | "Site is up" | Worker status, heartbeat missed |

---

## Ecosystem

Every package installs in one command. All are MIT licensed.

| Package | Language | Install |
|---------|----------|---------|
| [laravel](https://github.com/crontinel/laravel) | PHP (Laravel) | `composer require crontinel/laravel` |
| [php](https://github.com/crontinel/php) | PHP (core) | `composer require crontinel/php` |
| [node](https://github.com/crontinel/node) | Node.js | `npm i @crontinel/node` |
| [python](https://github.com/crontinel/python) | Python | `pip install crontinel` |
| [go](https://github.com/crontinel/go) | Go | `go get github.com/crontinel/go` |
| [ruby](https://github.com/crontinel/ruby) | Ruby | `gem install crontinel` |
| [mcp-server](https://github.com/crontinel/mcp-server) | MCP Server | AI agent monitoring |
| [app](https://github.com/crontinel/app) | SaaS App | Laravel + Livewire |

---

## Quick Start (Laravel)

```bash
composer require crontinel/laravel
php artisan crontinel:install
```

Visit `/crontinel` in your browser. That's it.

**What you get:**
- Horizon supervisor monitoring
- Queue depth tracking (Redis & database drivers)
- Cron job run history with late detection
- Slack/email alerts with auto-resolve
- CLI health check for CI/CD

---

## Quick Start (Node.js)

```javascript
import Crontinel from '@crontinel/node';

const crontinel = new Crontinel({ apiKey: 'your-key' });

// Track a cron job
await crontinel.track('daily-report', async () => {
  await generateReport();
});
```

---

## What Crontinel Monitors

### Horizon (Laravel)
- Supervisor status per supervisor (not just "Horizon is running")
- Paused state detection
- Failed jobs per minute

### Queues
- Depth per queue
- Failed job count
- Oldest job age
- Redis and database driver support

### Cron Jobs
- Every scheduled command run
- Exit code and duration
- Late detection (missed run windows)

---

## Links

| Resource | URL |
|----------|-----|
| [Website](https://crontinel.com) | Marketing site & signup |
| [App](https://app.crontinel.com) | Hosted SaaS dashboard (free tier) |
| [Docs](https://docs.crontinel.com) | Setup guides & API reference |
| [Status](https://status.crontinel.com) | System status page |
| [X/Twitter](https://x.com/crontinel) | Product updates |
| [Blog](https://crontinel.com/blog) | Tutorials & guides |

---

## Contributing

We welcome contributions! See our [contributing guide](https://github.com/crontinel/crontinel/blob/main/CONTRIBUTING.md) for details.

## License

MIT — free forever. See [LICENSE](https://github.com/crontinel/crontinel/blob/main/LICENSE).

---

<p align="center">
  Built by <a href="https://github.com/HarunRRayhan">Harun R Rayhan</a> · 
  <a href="https://crontinel.com">crontinel.com</a>
</p>
