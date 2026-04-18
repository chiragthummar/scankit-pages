# scankit-pages

Static site for ScanKit's Privacy Policy and Terms of Service, hosted on
GitHub Pages.

## Files

- `index.html` — landing page with links to the legal pages.
- `privacy.html` — Privacy Policy.
- `terms.html` — Terms of Service.
- `404.html` — custom not-found page.
- `styles.css` — shared Ink theme tokens (light + dark mode).

## Local preview

```bash
cd scankit-pages
python3 -m http.server 4000
# then visit http://localhost:4000
```

## Publish on GitHub Pages

1. Create a public repo named `scankit-pages` on GitHub.
2. Push this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial Privacy + Terms"
   git branch -M main
   git remote add origin https://github.com/<username>/scankit-pages.git
   git push -u origin main
   ```
3. In the repo on github.com, open **Settings → Pages**.
   - Source: `Deploy from a branch`
   - Branch: `main` / folder: `/ (root)`
   - Save. After ~1 minute the site is live at
     `https://<username>.github.io/scankit-pages/`.
4. Update `LegalURLs.base` in
   `ScanKit/QRScanner/Core/Services/LegalURLs.swift` to match the
   published URL.
