# Crontinel

**Completed is not done.** Crontinel is an outcome monitor for background jobs. It tells you when a job finished with exit code 0 but did no work.

[![Website](https://img.shields.io/badge/Web-crontinel.com-brightgreen)](https://crontinel.com)
[![Docs](https://img.shields.io/badge/Docs-docs.crontinel.com-blue)](https://docs.crontinel.com)
[![App](https://img.shields.io/badge/App-app.crontinel.com-purple)](https://app.crontinel.com)
[![Status](https://img.shields.io/badge/Status-status.crontinel.com-green)](https://status.crontinel.com)
[![X](https://img.shields.io/badge/X-%40crontinel-black)](https://x.com/crontinel)

---

## How it works

Every runtime sends the same HTTP receipt when a job ends. Crontinel checks it against your rules (for example, "processed at least one record") and alerts by email, Slack or webhook.

```bash
curl -X POST https://app.crontinel.com/api/v1/ingest/cron \
  -H "Authorization: Bearer $CRONTINEL_INGEST_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "request_key": "run-1",
    "command": "reports:generate",
    "status": "completed",
    "exit_code": 0,
    "started_at": "2026-10-06T12:00:00Z",
    "finished_at": "2026-10-06T12:00:05Z",
    "outcomes": { "metrics": { "processed_records": 0 } }
  }'
```

Recipes for **curl, Node.js, Python, Sidekiq and GitHub Actions** are in the [check-in docs](https://docs.crontinel.com/check-in/recipes/). Any other scheduler can post the same body.

## Repositories

| Repo | What it is |
|------|------------|
| [laravel](https://github.com/crontinel/laravel) | Laravel package. Attaches the receipt to the scheduler and adds queue depth and Horizon freshness. MIT. |
| [mcp-server](https://github.com/crontinel/mcp-server) | `@crontinel/mcp-server`. Lets your AI assistant read and manage your monitors. |
| [terraform-provider-crontinel](https://github.com/crontinel/terraform-provider-crontinel) | Terraform provider for schedules, heartbeats and outcome rules. On the [Terraform Registry](https://registry.terraform.io/providers/crontinel/crontinel). |
| [cli](https://github.com/crontinel/cli) | Command-line tool. |
| [docs](https://github.com/crontinel/docs) | Source of [docs.crontinel.com](https://docs.crontinel.com). |
| [landing](https://github.com/crontinel/landing) | Source of [crontinel.com](https://crontinel.com). |
| [php](https://github.com/crontinel/php) | PHP library. |

Other language repos in this organization (Node, Python, Go, Ruby, Rails, Rust, .NET) are **not maintained** for outcome monitoring. Use the HTTP receipt above instead.

## Contributing

We love open source. Issues and pull requests are welcome on any repo above.

## License

The open-source repositories are MIT licensed. The hosted app at [app.crontinel.com](https://app.crontinel.com) is the commercial product.

---

<p align="center">
  Built by <a href="https://github.com/HarunRRayhan">Harun R Rayhan</a> ·
  <a href="https://crontinel.com">crontinel.com</a>
</p>
