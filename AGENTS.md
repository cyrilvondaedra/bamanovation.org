# AGENTS.md

## Cursor Cloud specific instructions

This is a **zero-dependency static HTML/CSS website** (Bamanovation — business consulting firm). There is no package manager, build step, test framework, or linting tool.

### Serving locally

Run from the repo root:

```
python3 -m http.server 8080
```

Then open `http://localhost:8080/` in a browser. All pages (`index.html`, `portfolio.html`, `private-equity.html`, `admin/index.html`) are served directly.

### Key notes

- No `package.json`, `requirements.txt`, or other dependency manifest exists — there is nothing to install.
- The Decap CMS admin panel (`/admin/`) loads from CDN and requires Netlify Identity + Git Gateway to function; it is non-functional in local dev.
- External images (Unsplash, bambite.co) and Google Fonts require internet access.
- The contact form and newsletter form are non-functional HTML (no backend `action`).
- The site is deployed to GitHub Pages via the `CNAME` file (`bamanovation.org`).
