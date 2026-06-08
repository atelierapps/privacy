# AtelierApps.net

The website for **AtelierApps**, an independent app studio building privacy-first,
offline-friendly mobile apps. Static site deployed via Cloudflare Pages.

## Structure

```
index.html                  Landing page (apps showcase, status, contact)
privacy/citoyen/index.html  Privacy policy for the Citoyen app  → /privacy/citoyen
_redirects                  Cloudflare Pages redirects / aliases
```

## Adding a new app

Duplicate the Citoyen `<article class="app">` card in `index.html`, update the
icon, title, description, status badge (`live` / `soon`) and links. Add the app's
privacy policy under `privacy/<app>/index.html` if needed.

## Notes

- 100% static — no build step. Cloudflare Pages serves the files as-is.
- The Citoyen privacy policy used to live at the site root; it now lives at
  `/privacy/citoyen` (with `/privacy`, `/citoyen`, `/privacy-policy` redirecting
  there). If an app-store listing points at the bare domain for its privacy
  policy, update it to `https://atelierapps.net/privacy/citoyen`.
