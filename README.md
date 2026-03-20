# ScottCannSite

Personal portfolio site for Scott Cann — [scottcan-glitch.github.io/ScottCannSite](https://scottcan-glitch.github.io/ScottCannSite/)

## Current Features

### General
- Zero-dependency single-page portfolio (`index.html`, inline CSS/JS, no build tools)
- "Mission Control" dark theme with electric blue accent (`#0096FF`), `#0a0a12` background
- Self-hosted JetBrains Mono + Inter fonts (`assets/fonts/`)
- Dark mode default; light/dark toggle persisted in `localStorage`
- Frosted-glass fixed nav with smooth-scroll anchors
- Side-index navigation (right rail, desktop)
- Back-to-top button with "T" keyboard shortcut
- Scroll-triggered fade-in animations (IntersectionObserver)
- `content-visibility: auto` optimization
- Edition-gated preview content (`?edition=fall`)
- Custom 404 page with matching dark/light theme
- `robots.txt` + `sitemap.xml`
- Open Graph meta tags
- Responsive: mobile-first, tablet (768px+), desktop (1200px+)
- Accessibility: skip-to-content link, `focus-visible` outlines, `prefers-reduced-motion`, semantic HTML
- Print stylesheet with light-theme override
- Auto-deploy via GitHub Pages on push to `main`

### Sections
- **About** — brief intro
- **Experience** — 3 lane labels: Industry (2 entries), Research (1 entry), Campus (1 entry)
- **Projects** — 2 lane labels: Graduate Research, Engineering Projects (see below)
- **Beyond Engineering** — responsive 3-column card grid (Distance Running, Wrestling, Ultimate Frisbee & Pickleball)
- **Skills** — Languages & Tools, Software & Environments
- **Education** — degree entries

### Projects

**Graduate Research**
| Project | Media on hover | Links to |
|---|---|---|
| Traction Control using Nonlinear MPC *(featured)* | Image | PDF report |
| Self-Balancing Robot | Image | PDF report |
| Aerial Leveling of RC Car | — | — |
| Bond Graph Modeling | Image | PDF report |

**Engineering Projects**
| Project | Media on hover | Links to |
|---|---|---|
| SEPIC Converter | Image | PDF report |
| 5DOF Robot Arm | Video | PDF report |
| Coherix Computer Vision | — | — |
| FDM 3D Printer (Voron 2.4) | 3-image grid | — |
| Speed Controller & Sensor Fusion Firmware | Image | GitHub repo |

### Project Card UX
- Hover-to-reveal image/video overlay with smooth height transition
- Title pill oval on all project cards (linked and non-linked)
- `↗` arrow appears on card hover
- Hovering the image/video also highlights the card title (CSS `:has()`)
- Glow + lift + accent border reveal on hover

### Contact & Resume
- **Contact Me** → `mailto:scottcan@umich.edu?subject=Hello%20Scott`
- **Resume** → opens `assets/scott-cann-resume.pdf` in a new tab

## Tech Stack

HTML · CSS · JavaScript · GitHub Pages

## Local Development

No build step required.

```bash
npx serve .              # local server at http://localhost:3000
npx playwright test      # run smoke tests
```
