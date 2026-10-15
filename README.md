# The Bold Life Platform

**An off-the-shelf coaching website you buy once, customize, and own — no monthly
subscription.** Built and provided by [The Bold Life](https://www.theboldlife.coach/).

This repo is the **product**: a self-contained, re-brandable coaching site a coach
can make their own in about 30 minutes and host anywhere for free. This deployment
is the **live demo** (a sample coach, "Avery Rivers"), which doubles as the sales
preview.

- **Live demo:** https://designresearchgroup.github.io/coach-platform/
- **Make it yours:** see [`CUSTOMIZE.md`](CUSTOMIZE.md).

## Why it exists

Coaches rent platforms like Kajabi at ~$150/month — ~$1,800/year, forever, and they
never own anything. The Bold Life Platform flips that: **a one-time $500 lifetime
license** for a site you own and customize. Bookings, payments, and video ride on
your own tools (Calendly, Stripe, Zoom) that you already control. Native desktop
apps (Windows / macOS) are on the roadmap.

## What's here

```
index.html          The whole site (structural scaffold embedded inline)
brand.css           THE ONE FILE you edit to re-brand (colour + fonts)
img/favicon.svg     Browser-tab icon (swap the initials/colour)
img/og.png          1200×630 social share card (swap for your own)
CUSTOMIZE.md        Step-by-step: make it yours
robots.txt · sitemap.xml
.github/workflows/deploy.yml   CI/CD → GitHub Pages (free hosting)
```

No build step. Edit `brand.css` + `index.html`, push, and it's live.

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
