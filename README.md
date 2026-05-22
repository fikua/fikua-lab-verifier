# Fikua Lab — Verifier

OID4VP Verifier frontend for the Fikua Lab. Served at
**<https://verifier.lab.fikua.com>**.

The static UI talks to the lab backend over `/oid4vp/*`. The verifier
URL (`https://verifier.lab.fikua.com`) is referenced by every
presentation request and by every wallet that has trusted this verifier.

## What lives here

```text
.
├── index.html
├── style.css
├── app.js
├── favicon.svg
└── shared/         Vendored shared assets (consent banner, error pages)
```

Pure static — no build step.

## Hosting

- **Production:** Cloudflare Workers Static Assets (project
  `fikua-lab-verifier`), custom domain `verifier.lab.fikua.com`.
- **Backend reverse-proxy:** `/oid4vp/*` and `/health` are proxied to
  the lab backend at the edge.

## Architecture decisions

- ADR 0008 — Fikua Lab frontends on Cloudflare Workers.

## License

Apache-2.0. See [LICENSE](LICENSE).
