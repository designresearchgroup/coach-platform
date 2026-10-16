# The Bold Life Platform

**Everything a coach needs in one AI-built platform — $9 a month, $99 a year, or $299
forever.** All tiers are the **self-hosted** version: the coach runs it themselves (free
on GitHub Pages, Netlify, or any host); the $9/$99 subscription licenses the software,
and $299 is a one-time forever license. Built and provided by
[The Bold Life](https://www.theboldlife.coach/).

This repo holds two things:

1. **The sales page** (`index.html` at the root) — the pitch: "Software eats software.
   Every time.", a cost comparison, how-it-works, pricing, a cost
   **calculator**, and **The Bold Life as the live case study**.
2. **The self-hosted version** (`template/`) — the re-brandable coaching site a coach
   makes their own in ~30 minutes and runs on free hosting.

- **Sales page:** https://designresearchgroup.github.io/coach-platform/
- **Calculator:** https://designresearchgroup.github.io/coach-platform/calculator.html
- **Live sample (self-hosted version):** https://designresearchgroup.github.io/coach-platform/template/
- **Case study:** https://designresearchgroup.github.io/bold-life/
- **Make it yours:** see [`template/CUSTOMIZE.md`](template/CUSTOMIZE.md).

## Why it exists

Coaches rent legacy coaching suites at **$179+/month** — ~$2,148/year, forever. The
Bold Life Platform gives them the same thing a coach actually needs for **$9 a month,
$99 a year, or $299 forever** — one-twentieth the price. Software eats software, every
time. Bookings, payments, and video ride on their own tools (Calendly, Stripe, Zoom).
These tiers are **self-hosted** (the coach runs it); a managed, done-for-you tier and
native desktop apps (Windows / macOS) are on the roadmap.

## What's here

```
index.html              The SALES page (burgundy brand; $9/mo pitch + calculator links)
calculator.html         "What are you really paying?" — legacy-suite cost vs $9/mo
img/og.png              1200×630 share card for the sales page
img/casestudy-boldlife.png   Screenshot of the live Bold Life case study
img/favicon.svg         Provider favicon

template/               THE SELF-HOSTED VERSION a subscriber runs:
  index.html            The coaching site (structural scaffold embedded inline)
  brand.css             THE ONE FILE you edit to re-brand (colour + fonts)
  CUSTOMIZE.md          Step-by-step: make it yours + run it free
  img/favicon.svg · img/og.png

SETUP-SELLING.md        Operator guide: trial link, Stripe subscription, domain
robots.txt · sitemap.xml
.github/workflows/deploy.yml   CI/CD → GitHub Pages (free hosting)
```

No build step — everything is static. Edit and push.

## How it's put together

Two layers:

1. **Scaffold** — a proven component system (grids, cards, type, spacing,
   light/dark, responsive, accessibility) embedded inline. You don't edit it.
2. **Brand layer** — `brand.css` overrides the scaffold's colour and font tokens.
   Change one file, re-brand the whole site. That separation is what lets one coach's
   site be themed in minutes without touching the system.

## Accessibility & quality

Mobile-first, keyboard-navigable (skip link, visible focus), honors
`prefers-reduced-motion`, works without JavaScript, and ships with correct
Open Graph / canonical tags for link previews and SEO.

## Pricing / license

**$9/month, $99/year, or a $299 one-time forever license**, after a 30-day free trial
— the self-hosted version (the coach runs it; hosting is free). Comparison figures are
typical prices for legacy coaching suites. See [`SETUP-SELLING.md`](SETUP-SELLING.md)
to wire the trial link, the Stripe subscription / one-time price, and a domain.
