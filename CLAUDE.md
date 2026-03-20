# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is **scottcan-glitch.github.io**, a GitHub Pages personal site for Scott Cann. The repository is hosted at `scottcan-glitch/scottcan-glitch.github.io` and deploys automatically via GitHub Pages from the `main` branch.

## Current State

The site is a single-page portfolio built as a single `index.html` file with inline CSS and JS — no frameworks or build tools. It uses a "Mission Control" dark theme with accent color `#0096FF` (electric blue). Fonts (JetBrains Mono + Inter) are self-hosted from `assets/fonts/`.

Two view modes toggled by a view-toggle button (persisted in localStorage):
- **Section view** — 5 content sections: Experience, Projects, Beyond Engineering, Skills, Education
- **Chrono view** (default for first-time visitors, Experience filter active) — timeline with 6 filter buttons (All, Experience, Project, Research, Supply Chain Cases, Coursework) and semester sub-labels (Fall/Winter/Summer per year)

The **Experience** section uses 3 lane labels: Industry (2 entries), Research (1 Digital Manufacturing Lab entry), Campus (1 GSI entry). The **Projects** section uses 2 lane labels: Graduate Research, Engineering Projects. The **Beyond Engineering** section has 3 personal interest cards.

### Key files
- `index.html` — the entire site (all HTML, CSS, and JS inline)
- `404.html` — custom 404 page with dark/light theme support
- `robots.txt` + `sitemap.xml` — SEO basics
- `tests/smoke.spec.ts` — 14 Playwright smoke tests
- `ROADMAP.md` — categorized backlog with semester milestones
- `assets/headshot.jpg` — headshot photo (placeholder, to be provided)
- `assets/scott-cann-resume.pdf` — resume PDF (placeholder, to be provided)
- `ref/` — reference resumes (not deployed)

### CI checks (branch protection)
Four required status checks run on every PR:
- **HTML Validation** — validates `index.html` markup
- **Lighthouse CI** — performance/accessibility audit
- **Link Check** — verifies all links resolve
- **Playwright** — smoke tests for interactive JS features (`npx playwright test`)

Auto-merge is enabled. When creating PRs, always enable auto-merge with `gh pr merge --auto --squash` so they merge automatically once checks pass.

## Versioning & Releases

Version scheme: `year.ISOweek.ISOday` (e.g. `v2026.9.5`), with a `.2` patch suffix for same-day releases. GitHub Releases are tagged on `main` after each PR merges.

## Edition Gate

Content marked with `data-edition="fall"` is hidden on the live site but visible when `?edition=fall` is appended to the URL. The `hideEmptyChronoGroups()` function auto-hides semester and year labels in chrono view when all their cards are invisible after filtering.

## Deployment

Pushing to `main` triggers automatic deployment to GitHub Pages at https://scottcan-glitch.github.io/ScottCannSite/.
