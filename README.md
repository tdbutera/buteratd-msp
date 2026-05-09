# msp.buteranet.com

Source for the **ButeraNet Solutions** managed-services landing page, served at <https://msp.buteranet.com> via GitHub Pages + Cloudflare.

## What this is

Single-file static site — all CSS, JS, and SVG icons inlined. The only external dependency is Google Fonts (Inter). Deploys automatically on push to `main`.

## Repo contents

| File | Purpose |
|---|---|
| `index.html` | The full site (one file, all sections) |
| `404.html` | Branded not-found page |
| `CNAME` | GitHub Pages custom-domain binding (`msp.buteranet.com`) |
| `robots.txt` | Search engine crawl directives |
| `sitemap.xml` | Sitemap for SEO |

## Local development

Open `index.html` in any browser — no build step required.

## Deploy

```bash
git add index.html
git commit -m "describe the change"
git push origin main
```

GitHub Pages picks up the change within a minute. Cloudflare cache (max-age 600) takes up to 10 minutes to clear; manually purge in the Cloudflare dashboard if you need it immediate.

## Branding

- Navy `#1F4E79` · Blue `#2E75B6` · Light Blue `#D5E8F0` · White
- Inter (Google Fonts) with Arial fallback
- Schema.org `LocalBusiness` JSON-LD in the `<head>`
- ARIA-labeled interactive elements; mobile responsive

## About ButeraNet Solutions

Hawaii-based managed IT and AI platform for small organizations — churches, nonprofits, and small businesses. Founded by a U.S. Navy Senior Chief with 18+ years of IT and cybersecurity experience.

- Web: <https://buteranet.com>
- MSP site: <https://msp.buteranet.com>
- Email: <travis@buteranet.com>
- Phone: (812) 304-9813

*Infrastructure. Security. Reliability.*
