# Turn this into a real, sellable funnel

The sales page is live. To actually take orders you need two things that only you
can set up (they involve your money and your accounts): a **trial sign-up link**
and a **Stripe subscription** ($9/month and $99/year). Plus a **domain**. Here's
the whole path — about 20 minutes.

> The page is already wired for all of this. Until you paste your links, every
> "Try it free" button safely routes to the contact section / email, so nothing is
> ever a dead link.

---

## The offer (how it's framed on the page)

**Free for 30 days → then $9/month, or $99/year.** Everything included, cancel
anytime. We host and maintain the site; the coach just uses it.

## 1. The trial sign-up link (the "Try it free" buttons)

Pick how someone starts a trial, then paste that URL into `index.html`:

- **Simplest (works today):** leave it — the buttons open an email to you, and you
  start the trial by hand. Good for the first few clients.
- **A form** (recommended): make a free [Tally](https://tally.so) or Google Form
  that collects name, email, brand colour, and current website. 
- **A call:** a Calendly link for a 15-minute kickoff.

Then open `index.html`, find this line near the bottom, and paste your URL:

```js
var TRIAL_LINK = ""; // <-- paste your trial sign-up link here
```

Every "Try it free" button instantly points to it. Commit and push — it's live.

## 2. The subscription ($9/mo and $99/yr)

Set up two recurring prices so a trial converts to a paying subscriber:

1. Create a free [Stripe](https://stripe.com) account (this is **your** account —
   payouts go to your bank).
2. **Products → add a product** "The Bold Life Platform," with two recurring
   prices: **$9/month** and **$99/year**.
3. Make a **Payment Link** for it. Turn on a **30-day free trial** on the price so
   nothing is charged until day 30, and enable **collect customer name & email**
   (plus a custom field for their domain).
4. Under **After payment**, set the confirmation redirect to your success page:
   `https://<your-domain>/success.html`.
5. Copy the link (`https://buy.stripe.com/...`) and paste it into `TRIAL_LINK` in
   both `index.html` and `calculator.html` — now "Try it free" starts the trial and
   the subscription in one step. (Or keep `TRIAL_LINK` as a form/Calendly and send
   the Stripe link by hand near day 25.)

> A Stripe subscription with a 30-day trial is exactly the right tool: free for
> 30 days, then $9/month or $99/year, and the customer can cancel anytime.

## 3. Get it on a proper domain

The site runs on GitHub Pages at `designresearchgroup.github.io/coach-platform/`.
To put it on your own domain:

1. Register the domain at any registrar (e.g. Namecheap, Cloudflare).
2. Add a file named `CNAME` at the repo root containing just your domain, e.g.
   `platform.theboldlife.coach` — **or** set it in **Settings → Pages → Custom
   domain**.
3. Point DNS at GitHub Pages:
   - A subdomain (e.g. `platform.theboldlife.coach`): one **CNAME** record →
     `designresearchgroup.github.io`.
   - An apex domain (e.g. `theboldlifeplatform.com`): four **A** records →
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
4. Wait for DNS, then tick **Enforce HTTPS** in Settings → Pages.
5. Once live on the domain, update the `canonical` and `og:` URLs in `index.html`
   (and `success.html`'s links) to the new address so previews and SEO are right.

---

**Tell me your trial link, your $500 Stripe link, and your domain, and I'll wire all
three and redeploy — the whole funnel goes live in one push.**
