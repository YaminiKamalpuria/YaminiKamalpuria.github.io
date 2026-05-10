# yaminikamalpuria.me — Portfolio Website

Personal portfolio website for Yamini Kamalpuria, Full Stack Developer (MERN). Built as a single-file HTML/CSS/JS site and deployed via GitHub Pages with a custom domain.

🔗 **[Live Site](https://yaminikamalpuria.me)** · **[GitHub Repo](https://github.com/YaminiKamalpuria/YaminiKamalpuria.github.io)**

---

## Overview

A high-design, dark-themed developer portfolio with a lime accent (`#C8FF00`), featuring smooth scroll reveal animations, a hero section with a live status badge, a scrolling ticker, and fully responsive layouts — all in a single `index.html` file, zero dependencies, no build step.

---

## Sections

| Section | Description |
|---|---|
| **Hero** | Full-viewport split: name + status badge on the left, headshot on the right, with a grid background |
| **Ticker** | Auto-scrolling marquee of skills and status |
| **About** | Bio paragraph + key–value info panel (role, stack, status) |
| **Skills** | 3×2 CSS grid — Languages, Frontend, Backend, Database & DevOps, AI & Cloud, Concepts |
| **Projects** | 2×2 card grid — Canova CRM, Inventory Management, Book Catalog API, Pocket Notes + Rock Paper Scissors |
| **Experience** | RRCAT internship — role, responsibilities, tech context |
| **Education** | 3-column panel — B.Tech + M.Tech (DAVV), Class XII, Class X |
| **Certifications** | AWS AI Practitioner certificate with verify link and topics covered |
| **Achievements** | 2×2 card grid — top recognitions |
| **Contact** | Split: left CTA + email button, right social/contact links |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 (single `index.html`) |
| Styling | CSS3 (inline, custom properties / CSS variables) |
| Interactivity | Vanilla JavaScript (scroll nav, IntersectionObserver reveal) |
| Fonts | Space Grotesk · Bebas Neue · IBM Plex Mono (Google Fonts) |
| Hosting | GitHub Pages |
| Domain | Custom domain via CNAME (`yaminikamalpuria.me`) |

---

## Design System

```css
--lime:    #C8FF00   /* primary accent */
--black:   #0D0D0D   /* hero/dark section background */
--white:   #FFFFFF
--gray:    #888888   /* body text */
--border:  #E0E0E0
```

**Typography:**
- `Bebas Neue` — display headings (hero name, section titles)
- `Space Grotesk` — body, cards, UI text
- `IBM Plex Mono` — labels, badges, status tags, monospace details

---

## Key Implementation Details

- **Single-file architecture** — all CSS, JS, and markup in one `index.html`; no framework, no bundler, no npm
- **CSS Grid layouts** — skills (3-col), projects (2-col), education (3-col), contact (2-col) — all collapse to 1-col below 960px via a single media query
- **Scroll-triggered reveal** — `IntersectionObserver` adds `.visible` to `.reveal` elements as they enter the viewport; CSS handles the `opacity` + `translateY` transition
- **Scrolled navbar** — `window.scroll` listener toggles `.scrolled` on `#navbar`, applying a blur-backed dark background
- **Animated ticker** — CSS `@keyframes ticker` on `translateX(-50%)`, using a doubled content string so the loop appears seamless
- **Hero grid lines** — pure CSS `::before` pseudo-element with `background-image: linear-gradient` creating a subtle grid overlay on the dark hero section
- **Status dot** — lime pulsing dot via `@keyframes blink` on `opacity`
- **Photo treatment** — `grayscale(15%) contrast(1.05)` filter with a `linear-gradient` overlay fading to black at the bottom

---

## Local Development

No build step required. Open directly in a browser:

```bash
# Clone the repo
git clone https://github.com/YaminiKamalpuria/YaminiKamalpuria.github.io.git
cd YaminiKamalpuria.github.io

# Open in browser
open index.html
# or serve locally
npx serve .
```

---

## Deployment

The site is deployed on GitHub Pages from the root of the `main` branch. The custom domain is configured via the `CNAME` file:

```
yaminikamalpuria.me
```
