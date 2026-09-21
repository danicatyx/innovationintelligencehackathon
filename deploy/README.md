# Innovation Intelligence Hackathon — site

Static site. No build step: every file here is served as-is.

## Files
- index.html — the whole site (home, apply, organizers, terms)
- support.js — runtime the page loads
- _ds/ — design system stylesheet + bundle
- assets/ — host logos
- CNAME — your custom domain (edit before pushing)

## Deploy to GitHub Pages
1. Create a repo, e.g. `innovation-intelligence`.
2. Copy the contents of this folder into the repo root and push to `main`.
3. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, Folder: `/ (root)`. Save.
4. Live at `https://<user>.github.io/<repo>/` within a minute or two.

## Custom domain
1. Buy the domain (Namecheap, Cloudflare, Porkbun — ~$12/yr for .com; .org and .xyz are cheaper).
2. Edit `CNAME` in this folder to your domain, e.g. `innovationintelligence.org`. One line, no https://.
3. At your registrar's DNS panel add:
   - Four A records for the apex (@): 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - One CNAME record for `www` → `<user>.github.io`
4. Repo → Settings → Pages → Custom domain: enter the same domain, Save. Tick "Enforce HTTPS" once the certificate is issued (can take up to an hour).

## Updating
Re-export index.html from the design file and commit over the old one. Nothing else changes.
