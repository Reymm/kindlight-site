# Kindlight website

Plain static site — no build step, no framework. Plain HTML + one `styles.css`.
System font stack only; no webfonts, no JavaScript, no dependencies.

## Deploy (Cloudflare Pages)

- **Framework preset:** None
- **Build command:** *(empty)*
- **Build output directory:** this folder (`site/`) — point the Pages project at it as-is
- Production domain: `https://getkindlight.com` (all canonical/OG URLs assume it)

## Structure

- `index.html` — homepage (hero, how it works, moments grid, pricing, safety/ethics, FAQ)
- `moments/<slug>/index.html` — SEO moment guides; directory-style URLs match the
  plan in `../distribution/seo-pages.md` (`/moments/<slug>/`)
- `privacy.html`, `terms.html`, `support.html`
- `styles.css` — shared styling, Palette A "Lantern"
- `icon.png` — app icon (copy of `../branding/icon-a.png`), used as favicon + header mark
- `sitemap.xml`, `robots.txt`

## Placeholders pending app launch

- **App Store buttons** (homepage hero): `href="#"` with a `data-note` attribute and a
  "Coming soon" label. Replace with the real App Store URL at launch (search the HTML
  for `data-note`).
- **Privacy / Terms**: starter drafts for v1 (on-device storage, no account). Each file
  carries a `DRAFT` note in an HTML comment at the top — both need human/legal review
  before public launch.
- Only the first 10 pages of the 50-page SEO priority list in
  `../distribution/seo-pages.md` are built so far; the rest follow the same skeleton
  (see the "Page anatomy" section of that doc).

## Content rules (do not break when editing)

From `../distribution/seo-pages.md` — every moment page keeps: the sudden-change /
delirium banner, sources + review date on-page, the medical disclaimer footer, and
the soft CTA *after* the free guidance. No diagnosis or treatment claims anywhere.
Medication content obeys the hard block: never suggest crushing, hiding, doubling,
skipping, or changing any medicine — pharmacist/prescriber routing only.
