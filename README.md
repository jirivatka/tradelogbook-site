# tradelogbook.app

Static site for Logbook: landing page, support, privacy policy.

Three HTML files and one stylesheet. No build step, no dependencies, no external
assets. That matters more than it sounds: App Review fetches these pages from
unpredictable networks, and a page that depends on a CDN is a page that can fail
review.

## Why these pages exist

⚠️ **App Store submission requires a Support URL and a Privacy Policy URL.**
Both are mandatory. `support.html` and `privacy.html` are those pages.

The support page is built from problems that actually occurred, not imagined
ones — paper keys against a live host, the same value pasted into both fields,
why the realised figure differs from Alpaca's own activities list, IEX-only
prices on the free plan, and the one-stream limit that a user's own bot is
usually holding.

## ⛔ Claims that must stay true

The privacy policy is short because the truth is short: no analytics, no
tracking, no account, no backend. Before editing it, check the claims still
hold.

⚠️ **The site runs Cloudflare Web Analytics (cookieless), and `privacy.html`
says so.** Added 2026-08-19, in the same commit as the disclosure. If the
beacon is ever removed, or swapped for anything that sets a cookie or tracks
across sites, that page changes in the SAME commit. A privacy policy that is
accurate on Tuesday and false on Wednesday is worse than not having one.

⚠️ The beacon is the ONLY external asset on these pages. Everything else is
served from this repo, so a blocked CDN degrades analytics and nothing else.

⚠️ The support page links to `github.com/jirivatka/Logbook-Support/discussions`.
That repo must exist with Discussions enabled before submission, or the Support
URL leads to a 404 and review fails on it.

## Deploy

GitHub Pages from the default branch. `CNAME` pins the custom domain.
