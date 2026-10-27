# Sasa Digitals website

Static one-page site (no build step). Files:

- `index.html` — the page
- `assets/` — logo, hero video, poster and project screenshots
- `.nojekyll` — tells GitHub Pages to serve files as-is

## Publish on GitHub Pages

1. Upload these files to the root of the repo's `main` branch.
2. Repo **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → Save.
3. The site goes live at `https://<username>.github.io/sasadigital/` within a minute or two.

## Custom domain (Hostinger)

1. In **Settings → Pages → Custom domain**, enter your domain (e.g. `sasadigital.com`) and save. GitHub adds a `CNAME` file to the repo.
2. In Hostinger DNS:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `<username>.github.io`
   - Remove any old `A`/`CNAME` records for `@`/`www` that point elsewhere (Hostinger parking).
3. Once DNS resolves, tick **Enforce HTTPS** in Settings → Pages.
4. Keep the Zoho Mail `MX`, `SPF` (TXT) and `DKIM` (TXT) records as Zoho's admin console gives them — they don't conflict with the website records.
