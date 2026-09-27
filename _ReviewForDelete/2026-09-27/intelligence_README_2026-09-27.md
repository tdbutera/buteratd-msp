# intelligence.buteranet.com — Landing Page

ButeraNet Intelligence subdomain landing page.

## Deploy target

Repository: `tdbutera/buteratd-msp` (per Standing Rule 4 — only authorized repo).
Path in repo: `/intelligence/index.html` (subdirectory; root CNAME stays as `msp.buteranet.com`).

## DNS / Cloudflare setup needed

Per Standing Rule 5 — platform subdomains explicitly authorized:

1. **DNS record** in Cloudflare for `buteranet.com` zone:
   - Type: CNAME
   - Name: `intelligence`
   - Target: `tdbutera.github.io` (or wherever Pages serves from)
   - Proxy: ON (orange cloud)
   - TTL: Auto

2. **Routing** — interim solution: Cloudflare Page Rule
   - Match: `intelligence.buteranet.com/*`
   - Action: Forwarding URL (301)
   - Destination: `https://msp.buteranet.com/intelligence/$1`

3. **Long-term cleaner option** — Cloudflare Pages or a Worker reverse-proxy
   so the URL bar stays at `intelligence.buteranet.com` while content is served
   from `buteratd-msp/intelligence/`. Defer to a future session — interim 301
   is fine for the first weeks.

## Files

- `index.html` — single-page landing page, branded ButeraNet Intelligence,
  Navy/Blue/Gold palette, mobile-responsive, no external dependencies.
- `README.md` — this file.

## Conventions per Standing Rules

- Rule 1: never delete files; only update.
- Rule 7: ButeraNet Intelligence branding on every surface.
- Rule 14: GitHub/Cloudflare actions stated explicitly before push.
