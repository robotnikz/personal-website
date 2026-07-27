# halbei.com — Personal Website

The personal portfolio website of **Tobias Halbei** — Release Train Engineer and IT Project Manager — live at [www.halbei.com](https://www.halbei.com).

The site presents the full professional profile: delivery leadership experience, certifications, hands-on AI experience, independent software projects, and homelab work. It is written for recruiters and hiring managers looking for project leadership in technical environments.

## Sections

| Section | Content |
| --- | --- |
| Hero | Positioning, portrait, quick facts (experience, certifications, shipped apps) |
| About | Career story plus interactive skill tabs (Delivery / Technical / AI & Automation) |
| Experience | Timeline of roles at IQSIGHT, Bosch Security, MEKRA Lang, Branofilter + certification strip |
| AI experience | Agentic development, AI in enterprise workflows, self-hosted models, working principles |
| Projects | ClipROI (SaaS), WinBorg, Sentinel-DNS, DockWatch (open source) + four iOS apps |
| Homelab | Virtualization, automation, security & monitoring, backup discipline |
| Contact | Email, LinkedIn, GitHub |

## Tech

- Static HTML + CSS + vanilla JavaScript — no framework, no build step
- Light/dark theme toggle (persisted in `localStorage`, respects `prefers-color-scheme`)
- Scroll progress bar, scroll-spy navigation, reveal animations (`prefers-reduced-motion` aware)
- Accessible tabs, skip link, semantic markup, JSON-LD person schema
- Fonts: Space Grotesk (display) + Inter (body) via Google Fonts

## Repository layout & deployment

```
index.html, site.css, favicon.svg   ← working copies (edit these)
images/, previews/                  ← assets (portrait, project visuals, og:image)
docs/                               ← GitHub Pages deploy folder (served at www.halbei.com)
```

GitHub Pages serves the site **from the `docs/` folder** (the custom domain is configured via `docs/CNAME`). After changing any site file, sync it into `docs/` before pushing:

```bash
cp index.html site.css favicon.svg docs/
cp images/* docs/images/
cp previews/* docs/previews/
```

> If root and `docs/` drift apart, the live site silently lags behind — this has happened before, so always sync.

## Local development

No tooling required — open `index.html` in a browser. External assets (Google Fonts, GitHub project screenshots, star badges) need an internet connection.

## Social preview

`previews/portfolio-preview-1.jpg` (the `og:image`) is a 1200×630 screenshot of the hero section. Regenerate it after significant design changes so link previews stay current.
