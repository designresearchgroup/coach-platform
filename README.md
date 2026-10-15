# The Bold Life Platform

**An off-the-shelf coaching website you buy once, customize, and own — no monthly
subscription.** Built and provided by [The Bold Life](https://www.theboldlife.coach/).

This repo holds two things:

1. **The sales page** (`index.html` at the root) — the white-label pitch:
   "Kajabi, simplified. And you own it." Comparison, how-it-works, pricing, and
   **The Bold Life as the live case study**.
2. **The product** (`template/`) — the self-contained, re-brandable coaching site a
   coach makes their own in ~30 minutes and hosts anywhere for free.

- **Sales page:** https://designresearchgroup.github.io/coach-platform/
- **Starter / demo:** https://designresearchgroup.github.io/coach-platform/template/
- **Case study:** https://designresearchgroup.github.io/bold-life/
- **Make it yours:** see [`template/CUSTOMIZE.md`](template/CUSTOMIZE.md).

## Why it exists

Coaches rent platforms like Kajabi at ~$150/month — ~$1,800/year, forever, and they
never own anything. The Bold Life Platform flips that: **a one-time $500 lifetime
license** for a site you own and customize. Bookings, payments, and video ride on
your own tools (Calendly, Stripe, Zoom) that you already control. Native desktop
apps (Windows / macOS) are on the roadmap.

## What's here

```
index.html              The SALES page (white-label pitch; burgundy provider brand)
img/og.png              1200×630 share card for the sales page
img/casestudy-boldlife.png   Screenshot of the live Bold Life case study
img/favicon.svg         Provider favicon

template/               THE PRODUCT a buyer receives:
  index.html            The coaching site (structural scaffold embedded inline)
  brand.css             THE ONE FILE a buyer edits to re-brand (colour + fonts)
  CUSTOMIZE.md          Step-by-step: make it yours
  img/favicon.svg · img/og.png

robots.txt · sitemap.xml
.github/workflows/deploy.yml   CI/CD → GitHub Pages (free hosting)
```

No build step. Both the sales page and the template are static — edit and push.

## How it's put together (for the curious)

Two layers:

1. **Scaffold** — a proven component system (grids, cards, type, spacing,
   light/dark, responsive, accessibility) embedded inline. You don't edit it.
2. **Brand layer** — `brand.css` overrides the scaffold's colour and font tokens.
   Change one file, re-brand the whole site. That separation is what makes it a
   clean, ownable, off-the-shelf product rather than a one-off.

## Accessibility & quality

Mobile-first, keyboard-navigable (skip link, visible focus), honors
`prefers-reduced-motion`, works without JavaScript, and ships with correct
Open Graph / canonical tags for link previews and SEO.

## License / ownership

Sold as a **one-time lifetime license** per buyer: you own your copy and your site
outright. (Provider terms and support are set by The Bold Life.)
