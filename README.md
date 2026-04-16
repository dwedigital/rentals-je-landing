# Rentals.je Landing Page

Pre-launch landing page for [rentals.je](https://rentals.je) — a rental compliance platform for Jersey landlords and tenants.

Hosted on GitHub Pages with DNS via Cloudflare.

## Pages

| Page | Path | Purpose |
|------|------|---------|
| Homepage | `/` | Product overview, feature list, email sign-up |
| Privacy Policy | `/privacy.html` | DPJL 2018 compliant privacy policy |
| Terms & Conditions | `/terms.html` | Site usage terms, Jersey jurisdiction |

## Analytics

- **Plausible** — cookieless, no consent required, tracks all visitors. `Form: Submission` goal tracks email sign-ups.
- **Google Analytics** (via GTM `GTM-PXL85J5D`) — only fires after cookie consent is accepted. Uses Google Consent Mode v2 with `analytics_storage` defaulting to `denied`.

## Cookie Consent

A banner appears on first visit. Choice is stored in `localStorage` (`cookie_consent` key). Plausible loads regardless (no cookies). GTM/GA4 tags only fire when the user accepts.

## Email Sign-up

Submissions go to [Formspree](https://formspree.io) (form ID: `xnjljbrk`). Log in at formspree.io to view submissions.

## Legal

- Operated by **DWE Digital Ltd**, Jersey
- JOIC registration: **67559**
- Sub-processor: Formspree (form submissions), Google Analytics (consented analytics)

## Deployment

Pushes to `main` auto-deploy via GitHub Pages. Domain `rentals.je` is configured via the `CNAME` file and Cloudflare DNS (DNS-only mode, no proxy).
