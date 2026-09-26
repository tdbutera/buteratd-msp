# net.buteranet.com

Source for the **ButeraNet Solutions** company site, served at <https://net.buteranet.com> via GitHub Pages and Cloudflare. Deploys automatically on push to `main`.

## What this is

A static multi-page site. Ten live pages share one stylesheet, `assets/bn.css`, and inline their own SVG diagrams. The root-level `.html` files (`about.html`, `faq.html`, `pricing.html`, and so on) are redirect stubs for the retired single-page layout and point at the current pages.

## Theme (BNS, 2026-09-26)

The site follows the BNS brand board. The palette authority is clause A1 of `C:\ButeraNet\CLAUDE.md` (amended 2026-09-25 and 2026-09-26); the CSS custom properties at the top of `assets/bn.css` are the site's copy of it and are the only place the values are set in this repo. Gold text on light backgrounds uses the darker gold token for contrast; the accent tokens keep their v2.0 names (`--blue`, `--blue-l`) as aliases so the pages did not need re-plumbing.

Type is Montserrat 300 / 400 / 600, self-hosted in `assets/fonts/` under the SIL Open Font License. Logo files live in `assets/brand/`: `bns-logo-primary.svg` (light backgrounds), `bns-logo-reversed.svg` (dark backgrounds), and the `bns-mark` monogram variants for small applications. Favicons and the Open Graph image (`og-image.png`) are generated from the same files.

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
