# net.buteranet.com

Source for the **ButeraNet Solutions** company site, served at <https://net.buteranet.com> via GitHub Pages and Cloudflare. Deploys automatically on push to `main`.

## What this is

A static multi-page site. Ten live pages share one stylesheet, `assets/bn.css`, and inline their own SVG diagrams. The root-level `.html` files (`about.html`, `faq.html`, `pricing.html`, and so on) are redirect stubs for the retired single-page layout and point at the current pages.

## Theme (BNS, 2026-09-26)

The palette and type follow the BNS brand board, recorded as clause A1 of `C:\ButeraNet\CLAUDE.md`:

| Token | Value |
|---|---|
| Deep Navy | `#001B31` |
| Gold Accent | `#AE8140` (text on light backgrounds uses `#8E6A33` for contrast) |
| Light Gray | `#C9C8C8` |
| Muted, Panel, Rule | `#5E6672`, `#F4F4F2`, `#D8D7D4` |
| Type | Montserrat 300 / 400 / 600, self-hosted in `assets/fonts/` under the SIL Open Font License |

Logo files live in `assets/brand/`: `bns-logo-primary.svg` (light backgrounds), `bns-logo-reversed.svg` (dark backgrounds), and the `bns-mark` monogram variants for small applications. Favicons and the Open Graph image (`og-image.png`) are generated from the same files.

## Repo contents

| Path | Purpose |
|---|---|
| `index.html`, `services/`, `industries/`, `work/`, `field-notes/`, `about/`, `contact/`, `privacy/`, `terms/` | The live pages |
| `assets/bn.css` | The one stylesheet |
| `assets/brand/`, `assets/fonts/` | Logo set and typefaces |
| `404.html` | Not-found page |
| `CNAME` | GitHub Pages custom-domain binding |
| `robots.txt`, `sitemap.xml` | Crawl directives and sitemap |

## Local development

Serve the folder from its root so absolute asset paths resolve, for example `python -m http.server 8000`, then open <http://localhost:8000/>. No build step.

## Deploy

```bash
git add -A
git commit -m "describe the change"
git push origin main
```
