# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML documentation site for the **Pie & Mash** mobile app — a community check-in app for traditional British pie & mash shops in the UK. No build system, no dependencies, no framework.

## Structure

```
PML_DOCS/
└── docs/
    ├── privacy-policy.html   # App privacy policy (last updated 14 March 2026)
    └── support.html          # Support page with FAQ (expandable accordion via vanilla JS)
```

## Hosting & Deployment

- **Hosted on GitHub Pages** from the `docs/` folder
- **Custom domain:** pml.org.uk — users are routed here from the mobile app
- A `CNAME` file in `docs/` is required for the custom domain (`pml.org.uk`)
- DNS for pml.org.uk must have records pointing to GitHub Pages IPs

## Development

- **No build step** — files are static HTML served directly
- **No package manager or dependencies** — vanilla HTML/CSS/JS only
- Pages link to each other (support → privacy policy)
- JavaScript is minimal: just FAQ accordion toggle in support.html

## Design System

- **Brand color:** #2D5016 (dark green) for headings and links
- **Background:** #f0ede8 (warm beige)
- **Font stack:** system fonts (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, ...`)
- **Layout:** max-width 720px centered container, 40px/32px padding
- **Border radius:** 12px (container), 8px (accent boxes)

When adding or editing pages, match these existing styles. All styling is embedded (no external CSS files).
