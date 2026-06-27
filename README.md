# clibo-site

Landing page for **Clibo** — a private, native macOS clipboard workbench.
Static site (plain HTML/CSS, no build step), hosted on GitHub Pages at **clibo.us**.

## Files
- `index.html` — main landing page
- `privacy.html` — privacy promise
- `styles.css` — shared styles
- `favicon.svg` — logo / favicon
- `CNAME` — custom domain (`clibo.us`)
- `.nojekyll` — serve files as-is (no Jekyll processing)

## Local preview
Just open `index.html` in a browser, or:
```bash
cd clibo-site && python3 -m http.server 8080
# visit http://localhost:8080
```

## Deploy (GitHub Pages)
1. Create an empty GitHub repo named `clibo-site`.
2. Push this folder to it (see commands below).
3. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / root → Save.
4. The `CNAME` file points the site at **clibo.us**. In your domain registrar, add DNS records:
   - Apex `clibo.us` → four `A` records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (optional) `www` → `CNAME` to `<your-username>.github.io`
5. In Settings → Pages, set the custom domain to `clibo.us` and enable **Enforce HTTPS**.

## TODO before launch (search for `data-todo` in index.html)
- Wire **Download** button to the latest notarized DMG (e.g. a GitHub Release asset).
- Wire **Buy** button to the Dodo Payments checkout URL.
- Add real screenshots / a short demo video.
- Replace the "Coming soon" tag on BYOK AI once that feature ships.
