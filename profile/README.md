<div align="center">
    <br>
    <a href="https://buggregator.dev" target="_blank">
        <picture>
            <source media="(prefers-color-scheme: dark)" srcset="https://github.com/buggregator/.github/blob/master/logo/logo-dark-theme.svg?raw=true">
            <img width="50%" align="center" src="https://github.com/buggregator/.github/blob/master/logo/logo-light-theme.svg?raw=true" alt="Buggregator Logo">
        </picture>
    </a>
    <br>
    <br>
</div>

<h3 align="center">Debug everything in your PHP app. Install nothing.</h3>

<p align="center">
One <code>docker run</code> command gives you exceptions, logs, emails, profiling, dumps, and more — all in one real-time UI.<br>
No cloud account. No code changes. No new dependencies. <b>Free forever.</b>
</p>

<div align="center">

[![Stars](https://img.shields.io/github/stars/buggregator?style=flat-square&label=Stars&color=yellow)](https://github.com/buggregator/server)
[![Twitter](https://img.shields.io/badge/-Follow-black?style=flat-square&logo=X)](https://x.com/intent/follow?screen_name=buggregator)
[![Discord](https://img.shields.io/discord/1172942458598985738?style=flat-square&logo=discord&labelColor=7289d9&logoColor=white&color=39456d)](https://discord.gg/vDsCD3EKUB)
[![Support](https://img.shields.io/static/v1?style=flat-square&label=Support&message=%E2%9D%A4&logo=GitHub&color=%23fe4e86)](https://github.com/sponsors/buggregator)

</div>

<br>

```bash
docker run -p 8000:8000 -p 1025:1025 -p 9912:9912 -p 9913:9913 -p 9914:9914 ghcr.io/buggregator/server:latest
```

<p align="center">Open <a href="http://127.0.0.1:8000">http://127.0.0.1:8000</a> — that's it. No login, no setup, no registration.</p>

---

## Replaces your local dev stack — for free

Buggregator is a **standalone debugging server** that runs *beside* your application, not inside it. Your app's `composer.json` stays untouched. You just redirect your existing SDKs to a local address.

| Instead of | You get |
|---|---|
| Sentry (local) | Exception tracking with full stack traces |
| Mailhog / Mailtrap | Email capture and HTML preview |
| Ray (Spatie) | Variable dumps, queries, models, jobs |
| Blackfire / XHProf UI | Performance profiling with call graphs |
| Log viewers | Real-time Monolog aggregation |
| RequestBin | HTTP request inspection |
| Inspector.dev (local) | Application performance monitoring |
| SMS gateways (dev) | SMS interception for 40+ providers |

**All of this. One command. Zero cost.**

---

## The Buggregator ecosystem

### Core products

| | Repository | Description |
|---|---|---|
| **Server** | [`buggregator/server`](https://github.com/buggregator/server) | Full-featured debugging server as a Docker container. Built on Spiral Framework + RoadRunner. The main product for most developers. |
| **Go Server** | [`buggregator/go-server`](https://github.com/buggregator/go-server) | Drop-in replacement — single ~30 MB binary, ~50 MB RAM. No PHP, no RoadRunner, no external database. Built-in MCP server for AI tools. |
| **Trap** | [`buggregator/trap`](https://github.com/buggregator/trap) | Lightweight PHP CLI alternative. `composer require --dev buggregator/trap` — no Docker needed. Covers dumps, profiler, logs, SMTP, and more. |
| **Frontend** | [`buggregator/frontend`](https://github.com/buggregator/frontend) | Vue 3 + TypeScript web UI shared between Server and Go Server. Real-time event streaming via WebSockets. |
| **PhpStorm Plugin** | [`buggregator/phpstorm-plugin`](https://github.com/buggregator/phpstorm-plugin) | Brings debug data directly into your IDE. Never leave PhpStorm. |

### Infrastructure & Plugins

| Repository | Description |
|---|---|
| [`helm-chart`](https://github.com/buggregator/helm-chart) | Kubernetes Helm chart for production deployment |
| [`docker`](https://github.com/buggregator/docker) | Base Docker image |
| [`smtp-server`](https://github.com/buggregator/smtp-server) | SMTP server plugin for RoadRunner |
| [`monolog-server`](https://github.com/buggregator/monolog-server) | Monolog TCP receiver plugin for RoadRunner |
| [`profiler-server`](https://github.com/buggregator/profiler-server) | XHProf profiling data processor for RoadRunner |
| [`var-dumper-server`](https://github.com/buggregator/var-dumper-server) | Symfony VarDumper TCP receiver for RoadRunner |

---

## Works with your stack

**Frameworks:** Laravel, Symfony, Spiral, WordPress, Yii3, Drupal — and anything that uses standard PHP debugging SDKs.

**Async runtimes:** RoadRunner, FrankenPHP, Swoole, Laravel Octane — where tools like Telescope don't work, Buggregator does.

**Beyond PHP:** JavaScript, Python, Ruby, Go — via Sentry SDK.

---

## Enterprise-ready when you need it

- SSO Authentication (Auth0, Kinde)
- External Database (PostgreSQL, MySQL)
- Kubernetes deployment
- Webhooks
- Prometheus metrics
- Multi-project support

---

## Resources

- [**Documentation**](https://docs.buggregator.dev) — Installation, configuration, integration guides
- [**Website**](https://buggregator.dev) — Product overview and demos
- [**Examples**](https://github.com/buggregator/examples) — Sample applications and usage patterns

---

## Contributing

- **Report bugs:** [Open an issue](https://github.com/buggregator/server/issues/new)
- **Suggest features:** [Start a discussion](https://github.com/buggregator/server/issues)
- **Submit code:** Fork, change, PR — contributions welcome across all repos
- **Improve docs:** [Edit documentation](https://github.com/buggregator/docs)
- **Join the community:** [Discord](https://discord.gg/vDsCD3EKUB)

---

<div align="center">

**Buggregator is free forever. Sponsors make that possible.**

[Become a Sponsor](https://github.com/sponsors/buggregator)

</div>
