# Innovation Intelligence Hackathon — site

Static site. No build step: every file here is served as-is.

## Files
- index.html — the whole site (home, apply, organizers, terms)
- support.js — runtime the page loads
- _ds/ — design system stylesheet + bundle
- assets/ — host logos

## Deploy to GitHub Pages
Deployment is automatic. Every push to `main` runs `.github/workflows/pages.yml`,
which publishes this `deploy/` folder to GitHub Pages.

Live at `https://danicatyx.github.io/innovationintelligencehackathon/` a minute or two
after each push. Progress is under the repo's Actions tab.

## Custom domain
1. Buy the domain (Namecheap, Cloudflare, Porkbun — ~$12/yr for .com; .org and .xyz are cheaper).
2. Add a file named `CNAME` in this folder containing just your domain, e.g. `innovationintelligence.org`. One line, no https://.
3. At your registrar's DNS panel add:
   - Four A records for the apex (@): 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - One CNAME record for `www` → `<user>.github.io`
4. Repo → Settings → Pages → Custom domain: enter the same domain, Save. Tick "Enforce HTTPS" once the certificate is issued (can take up to an hour).

## Updating
Re-export index.html from the design file and commit over the old one. Nothing else changes.
