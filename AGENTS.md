# AGENTS.md

## Repository Overview

This is a **pre-built static website** directory (compiled Jekyll output). It contains only HTML, CSS, and assets—no source files, build scripts, or configuration.

- **Purpose**: Maïwen Demeulle's personal portfolio site
- **Technology**: Jekyll (v4.4.1, indicated by HTML meta tags)
- **Build state**: Already compiled; no source markdown or `_config.yml` present

## Structure

```
/
├── index.html, 404.html, feed.xml    (entry points)
├── /about/index.html                  (about page)
├── /projects/index.html               (projects listing)
├── /projects/*.html                   (individual project pages)
├── /works/index.html                  (works page)
└── /assets/
    ├── /css/                          (stylesheets, including custom.css, project.css)
    ├── /images/                       (project & content images)
    └── /docs/                         (documentation assets)
```

## Key Facts for Agents

1. **No local build process** — All HTML is pre-rendered. Edits to `.html` files directly affect the live site.
2. **No source control visible** — Not a git repository; no `.git` or `.github/` directory.
3. **No NPM/Ruby dependencies** — No `package.json`, `Gemfile`, or dependency managers to install.
4. **CSS is compiled** — Source SCSS exists on disk as `.css.map` but only minified CSS is present; editing CSS requires rebuild tools not in this directory.
5. **Page structure** — Each section (about, projects, works) has its own folder with an `index.html`; Jekyll SEO tags are pre-injected.

## Common Tasks

### Editing content
- **HTML pages**: Edit `.html` files directly; changes are live on next serve.
- **CSS styles**: Edit `/assets/css/*.css` (custom.css for global tweaks, project.css for project pages).
- **Images & assets**: Add to `/assets/images/` and reference in HTML.

### Testing locally
If you have Jekyll installed:
```bash
jekyll serve --source . --destination .
```
Otherwise, use any local HTTP server (e.g., `python -m http.server`).

### Deployment
No CI/CD configured in this directory. Deploy by copying entire directory to hosting.

## Known Quirks

- **HTML is verbose** — Jekyll-generated HTML includes inline SEO metadata and full stylesheet links on every page (not minimized for readability).
- **feed.xml is static** — Atom feed is pre-built; updates require Jekyll rebuild.
- **Favicon set but not all variants** — `/favicon.svg` exists but also older `.ico` and `.png` formats for compatibility.
