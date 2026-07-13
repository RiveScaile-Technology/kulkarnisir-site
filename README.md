# KulkarniSir — Landing Page

Static landing page for **KulkarniSir** private tuitions (Physics, Chemistry,
Maths & Engineering — Prakash Kulkarni, IIT Bombay, Mulund, Mumbai).

The whole site is a single self-contained `index.html` (all assets inlined).

## Deployment

Every push to `main` triggers `.github/workflows/deploy-pages.yml`, which
publishes the site to GitHub Pages. No build step — the HTML is served as-is.

## Updating the site

Replace `index.html` and push to `main`. Pages redeploys automatically.

## Custom domain (later)

When the domain is registered, add a `CNAME` file at the repo root containing
just the domain (e.g. `kulkarnisir.com`), then set the DNS records GitHub
provides under Settings → Pages.
