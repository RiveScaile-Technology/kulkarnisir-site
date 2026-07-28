# KulkarniSir — Landing Page

Static landing page for **KulkarniSir** private tuitions (Physics, Chemistry,
Maths & Engineering — Prakash Kulkarni, IIT Bombay, Mulund, Mumbai).

The whole site is a single self-contained `index.html` (all assets inlined).

## Deployment

Every push to `main` triggers `.github/workflows/deploy-pages.yml`, which
publishes the site to GitHub Pages. No build step — the HTML is served as-is.

## Updating the site

Replace `index.html` and push to `main`. Pages redeploys automatically.

## Custom domain — kulkarnisir.academy

Canonical URL: **https://kulkarnisir.academy/** (apex; `www` redirects to it).
The repo carries a `CNAME` file, and `index.html` sets the canonical/OG tags.

One-time setup after registering the domain:

1. **DNS at the registrar** —
   - Apex `kulkarnisir.academy`: four `A` records →
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
     (optionally `AAAA` → `2606:50c0:8000::153` … `2606:50c0:8003::153`)
   - `www`: `CNAME` → `rivescaile-technology.github.io`
2. **GitHub**: Settings → Pages → Custom domain → `kulkarnisir.academy` → Save.
   Wait for the DNS check, then tick **Enforce HTTPS** (cert takes a few
   minutes to ~1 hour to provision).
3. The old `rivescaile-technology.github.io/kulkarnisir-site/` URL then
   redirects to the custom domain automatically.

Formspree note: if form submissions stop after the switch, check the form's
allowed-domains/restrictions setting in the Formspree dashboard and add
`kulkarnisir.academy`.
