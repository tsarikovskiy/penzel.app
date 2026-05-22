# Legal — Privacy Policy & Terms of Use

Two standalone HTML files for Penzel's required legal pages:

- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Use

Both are tailored to Penzel's v1 reality:
- Offline-only iOS app
- Zero data collection
- One-time non-consumable IAP at $9.99
- Recipe/diagnostic attribution policy (Goonhammer sources)
- Hobby-paint brand disclaimers (Citadel/Vallejo/AK/Scale75/Army Painter are unaffiliated)

## Before you submit to App Store Connect

App Store Connect requires a **public, hosted Privacy Policy URL** as part of the app metadata. The hosted URL must be reachable when reviewers click it. Terms of Use is optional but strongly recommended for paid apps.

## Hosting options

Pick whichever is fastest. All are free.

### Option A: GitHub Pages (recommended)
1. Create a public repo (e.g. `penzel-legal`) and push `privacy.html` + `terms.html` to its root
2. Repo Settings → Pages → Source: deploy from `main` branch, `/` folder
3. Your URLs become `https://<username>.github.io/penzel-legal/privacy.html` and `.../terms.html`
4. For a cleaner URL, set up a custom domain (`penzel.app`) in Pages settings and point DNS

### Option B: Netlify Drop
1. Visit `https://app.netlify.com/drop`
2. Drag the `legal/` folder onto the page
3. You get a free subdomain instantly: `https://<random>.netlify.app/privacy.html`
4. (Optional) Connect a custom domain

### Option C: Cloudflare Pages
Same idea as Netlify, slightly different UI. Free tier is generous.

## After hosting

1. Note the canonical URLs for `privacy.html` and `terms.html`
2. Update `PaywallView.swift`:
   - `static let termsURL = "https://penzel.app/terms.html"` (or your hosted URL)
   - `static let privacyURL = "https://penzel.app/privacy.html"`
3. Update App Store Connect:
   - App Information → **Privacy Policy URL** = your privacy.html URL
   - (Optional but recommended) App Information → **EULA** = upload `terms.html` text, or leave blank to use Apple's standard EULA

## What you need to update before publishing

These files use `support@penzel.app` as the contact email throughout. Before submitting:

- [ ] Configure email forwarding from `support@penzel.app` to your real inbox, OR
- [ ] Replace `support@penzel.app` with a working email address you control

App Store reviewers may email this address. If it bounces, your submission gets delayed.

## Legal disclaimer

These templates are drafted for an indie iOS app with zero data collection and a simple IAP. They are not a substitute for professional legal advice. If you are in a jurisdiction with strict consumer-protection laws, or if Penzel expands to collect personal data in v1.1+, have a lawyer review the updated versions.
