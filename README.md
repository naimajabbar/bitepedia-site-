# Bitepedia Support Site

Static support and legal website for the **Bitepedia** mobile app (iOS + Android). This is not the app itself — it's the companion site that provides a landing page, FAQ, terms, privacy policy, and contact info, hosted on GitHub Pages.

## What's inside

```
bitepedia-site-/
├── index.html           # Landing page — app intro and feature highlights
├── support.html         # FAQ and support resources
├── terms.html           # Terms of Use
├── privacy-policy.html  # Privacy Policy
├── contact.html         # Contact page with support email
└── styles.css           # Shared stylesheet — used by all five pages
```

## Tech stack

Plain HTML and CSS. No framework, no build step, no npm install. Open the files and they work.

The only external dependency is Google Fonts (Fredoka + Manrope), loaded via `<link>` in each page's `<head>`. A minimal vanilla JS snippet handles the mobile nav toggle — no libraries.

## Local preview

**Quickest** — open directly in a browser:
```bash
open index.html
```

**Closer to production** — serve over HTTP (macOS ships with Python 3):
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000`.

## Deployment

This site is hosted on GitHub Pages from the `main` branch, root folder.

To configure (one-time, already done):
1. Go to **Settings → Pages** in the GitHub repo
2. Set Source to `Deploy from a branch`
3. Branch: `main` / Folder: `/ (root)`
4. Save

Live URL: `https://naimajabbar.github.io/bitepedia-site-/`

To publish changes: commit and push to `main`. Pages redeploys automatically within ~1 minute.

## Editing the privacy policy

The content in `privacy-policy.html` is sourced from a canonical Google Doc:
`https://docs.google.com/document/d/1N8u1X93gmte3GU2N1aqAiUpBrjblSJxJSQtVydLAX08/edit`

**Do not hand-edit the policy text directly in the HTML** without also updating the source document. The HTML is downstream of the doc — if they drift out of sync, the published page may contradict the authoritative version. Any policy update should start in the Google Doc, then be re-pasted and reformatted into `privacy-policy.html`.

## Brand system

| Role | Value |
|---|---|
| Terracotta (primary) | `#B85C38` |
| Mustard (secondary) | `#E0A73A` |
| Olive (accent) | `#6B7A4F` |
| Cream (background) | `#FBF3E7` |
| Charcoal (text) | `#2E2622` |

**Fonts:** Fredoka (headings/wordmark) · Manrope (body) — both via Google Fonts.

Corner radius: 14–20px on cards and buttons. Icons: thin-line SVG, stroke-width 1.5.

## Contact

Support email: [jabbrixstudio@gmail.com](mailto:jabbrixstudio@gmail.com)
