# The simple equation for open onchain markets

Static site: hosted essay + embedded flow animation + carousel + shareable images.

## Structure
- `index.html` — the essay, styled; embeds the flow animation and links all assets
- `assets/flows.html` — interactive tokenised-repo flow (the animation)
- `assets/og-cover.png` — 1200×627 share card (wired into OG/Twitter tags)
- `assets/lineage-banner.png` — 1200×627 lineage banner
- `assets/carousel.pdf` — 8-slide carousel
- `assets/flowryd-lockup.svg` — brand lockup
- `vercel.json` — clean URLs, caching, basic security headers

## Deploy (Vercel)
Option A — drag & drop: zip this folder's contents (not the folder itself) at vercel.com/new → deploy.

Option B — CLI:
```
npm i -g vercel
cd this-folder
vercel        # preview
vercel --prod # production
```

Then add the domain: Vercel project → Settings → Domains → add `flowryd.xyz` (or a subdomain like `venue.flowryd.xyz`) and point DNS as prompted.

## Notes
- Page is public/indexable by design. To keep it private, add `<meta name="robots" content="noindex,nofollow">` in `index.html` and a `Cache-Control: no-store` header.
- Update the LinkedIn share card by replacing `assets/og-cover.png` (keep 1200×627).
- `og:url` in `index.html` is set to `https://flowryd.xyz/` — change if deploying to a subpath.
