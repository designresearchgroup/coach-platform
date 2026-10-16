# Make it yours

This is the **self-hosted** version of The Bold Life Platform — you run it yourself,
for **$9 a month (or $99 a year)**. Here's how to turn this sample into your own
site in about 30 minutes. You don't need to be a developer.

Everything you need to change lives in **two files**: `brand.css` (how it looks)
and `index.html` (what it says).

---

## 1. Your colour and fonts — `brand.css`

Open `brand.css` and change one line:

```css
--accent:#7A5195;   /* <-- your brand colour */
```

Pick your brand colour (any hex code), set `--accent` to it, and set
`--accent-hover` to a slightly darker shade. The whole site re-tints from those.

To change the fonts, edit `--font` (body) and `--display` (headlines) in the
same file — **then** update the Google Fonts `<link>` near the top of
`index.html` so the new fonts load. (If you keep the defaults — Poppins +
Montserrat — you don't have to touch anything.)

That's the entire look. You don't edit the big stylesheet above it; that's the
scaffold, and leaving it alone is what keeps everything consistent.

## 2. Your words — `index.html`

Open `index.html` and look for the comment markers — `<!-- ===== HERO ===== -->`,
`SERVICES`, `ABOUT`, `CONTACT`, `FOOTER`. Replace the placeholder text with your
own:

- **Your name / logo:** search for `Avery Rivers` and `AR` and replace them.
- **Headline + intro:** in the HERO section.
- **Services:** three cards — edit them, or copy a card to add more.
- **About:** your story and credentials.
- **Contact:** point the buttons at your email, your Calendly, or any booking
  tool. Search for `hello@example.com` and replace it everywhere.
- Remove the **"Live demo · The Bold Life Platform"** flag in the HERO once it's
  yours (and the "powered by" line in the footer, if you prefer — it's your site).

## 3. Your images

- `img/favicon.svg` — the little browser-tab icon. Change the initials and the
  colour to match your brand.
- `img/og.png` — the 1200×630 preview card shown when your link is shared on
  LinkedIn, iMessage, etc. Replace it with your own.

## 4. Put it online (free)

This is a plain static site — it runs anywhere. The simplest free option:

1. Create a free **GitHub** account and a repository, and upload these files.
2. In the repo: **Settings → Pages → Source: GitHub Actions.**
3. Push/commit. The included workflow (`.github/workflows/deploy.yml`) publishes
   your site automatically. Every change you push goes live on its own.

You can also drag the folder onto Netlify, Cloudflare Pages, or any web host —
it's just files. **You run it yourself; hosting is free. The $9/mo (or $99/yr)
licenses the platform.**

## 5. Your own domain (optional)

Buy a domain (e.g. `yourname.coach`), add a `CNAME` file at the repo root
containing that domain, and point its DNS at your host. Your site then lives at
your own address.

---

Need it done for you? That's what **The Bold Life** offers — we'll customize and
launch it for you. See [theboldlife.coach](https://www.theboldlife.coach/).
