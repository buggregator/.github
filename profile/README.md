<div align="center">
  <br>
  <a href="https://buggregator.dev">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github.com/buggregator/.github/blob/master/logo/logo-dark-theme.svg?raw=true">
      <img width="40%" src="https://github.com/buggregator/.github/blob/master/logo/logo-light-theme.svg?raw=true" alt="Buggregator">
    </picture>
  </a>
  <br><br>
</div>

<h3 align="center">One local server for everything your app sends while you develop</h3>

<p align="center">
Errors, dumps, emails, logs, profiles and HTTP requests — in one window on your machine.<br>
Built for PHP. Node.js, browser JavaScript, Python, Go and Java send errors through their Sentry SDK; mail and HTTP work from any language.<br>
<b>Free, MIT, no account, no cloud.</b>
</p>

<p align="center">
  <a href="https://github.com/buggregator/server/releases/latest"><img src="https://img.shields.io/github/v/release/buggregator/server?style=flat-square&label=server" alt="Latest release"></a>
  <a href="https://github.com/buggregator/server/stargazers"><img src="https://img.shields.io/github/stars/buggregator/server?style=flat-square&color=yellow" alt="Stars"></a>
  <a href="https://hub.docker.com/r/butschster/buggregator"><img src="https://img.shields.io/docker/pulls/butschster/buggregator?style=flat-square" alt="Docker pulls"></a>
  <a href="https://discord.gg/vDsCD3EKUB"><img src="https://img.shields.io/badge/discord-chat-5865F2?style=flat-square&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://x.com/buggregator"><img src="https://img.shields.io/badge/follow-%40buggregator-black?style=flat-square&logo=x" alt="Follow on X"></a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/buggregator/server/master/.github/assets/demo.gif" width="90%" alt="Buggregator in 30 seconds: events arrive, then an exception, an email, dumps and a profile are opened">
</p>

## Run it

```bash
# Linux, macOS — one binary, no sudo
curl -fsSL https://raw.githubusercontent.com/buggregator/server/master/scripts/install.sh | sh
buggregator
```

```powershell
# Windows (PowerShell)
irm https://raw.githubusercontent.com/buggregator/server/master/scripts/install.ps1 | iex
```

```bash
# Docker
docker run --pull always -p 127.0.0.1:8000:8000 -p 127.0.0.1:1025:1025 \
  -p 127.0.0.1:9912:9912 -p 127.0.0.1:9913:9913 ghcr.io/buggregator/server:latest
```

Open http://127.0.0.1:8000, then point your app at it: change addresses in `.env`, not code. [Getting started →](https://docs.buggregator.dev/getting-started.html)

## What it replaces on your machine

| Instead of | Buggregator catches | Sent from |
|---|---|---|
| A cloud Sentry project for local errors | Exceptions, traces, logs, metrics | Sentry SDK (DSN) |
| Mailpit, MailHog, Mailtrap | Emails with HTML preview, plus an API for E2E tests | Any SMTP client |
| The Ray app, for viewing `ray()` calls | Dumps, queries, models, jobs | Symfony VarDumper, Spatie Ray |
| A log viewer | Logs, live | Monolog |
| An XHProf UI | Call graph, flame chart, top functions | XHProf |
| RequestBin, a hand-written stub API | Any HTTP request, outgoing calls via a proxy, a mock server from rules or an OpenAPI spec | curl, webhooks, your app |

Also: SMS in the format of 42 providers, Xdebug in the browser, and a built-in **MCP server** so Claude Code, Cursor or any MCP client can read your errors, dumps and profiles.

For a team or CI: **Kubernetes-ready** — `helm install buggregator oci://ghcr.io/buggregator/helm-chart/buggregator` (one replica, data on a persistent volume, non-root) — plus [SSO for the UI](https://docs.buggregator.dev/config/sso.html), [Prometheus metrics](https://docs.buggregator.dev/config/metrics.html), an [OpenAPI spec of the API](https://github.com/buggregator/server/blob/master/api/openapi.yaml) and a [CI example](https://github.com/buggregator/server/tree/master/examples/ci).

<table>
  <tr>
    <td><img src="https://raw.githubusercontent.com/buggregator/server/master/.github/assets/sentry.webp" alt="A Sentry exception with its stack trace"></td>
    <td><img src="https://raw.githubusercontent.com/buggregator/server/master/.github/assets/smtp.webp" alt="An order confirmation email in the HTML preview"></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/buggregator/server/master/.github/assets/dumps.webp" alt="VarDumper dumps: a boolean, a number, a string and an SQL query"></td>
    <td><img src="https://raw.githubusercontent.com/buggregator/server/master/.github/assets/profiler.webp" alt="A profiler call graph, slow functions in red"></td>
  </tr>
</table>

## Repositories

| | |
|---|---|
| [**server**](https://github.com/buggregator/server) | The server: one Go binary or a Docker image. Start here. |
| [**trap**](https://github.com/buggregator/trap) | A small PHP CLI alternative: `composer require --dev buggregator/trap`, no Docker or binary. |
| [**frontend**](https://github.com/buggregator/frontend) | The web UI (Vue 3, TypeScript), built into every server release. |
| [**docs**](https://github.com/buggregator/docs) | The documentation at [docs.buggregator.dev](https://docs.buggregator.dev). Fixes welcome. |
| [**helm-chart**](https://github.com/buggregator/helm-chart) | The official Helm chart: one `helm install`, data on a persistent volume, non-root. |
| [**phpstorm-plugin**](https://github.com/buggregator/phpstorm-plugin) | Buggregator in PhpStorm. |

## Get involved

- **Something broke or is missing?** [Open an issue](https://github.com/buggregator/server/issues/new) — or a pull request in any repo.
- **Security issue?** Report it privately: [SECURITY.md](https://github.com/buggregator/server/blob/master/SECURITY.md).
- **Questions, ideas:** [Discord](https://discord.gg/vDsCD3EKUB).
- **Saved you time?** [Star the server](https://github.com/buggregator/server/stargazers) — that is how other developers find it. Want to do more: [sponsor the project](https://github.com/sponsors/buggregator).

<p align="center"><a href="https://buggregator.dev">buggregator.dev</a> · <a href="https://docs.buggregator.dev">docs.buggregator.dev</a></p>
