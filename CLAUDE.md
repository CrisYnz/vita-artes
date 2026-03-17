# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page website for **Fundación Vita Artes**, an educational nonprofit in Chile. The entire site lives in one file: `index.html`.

## Running

No build step. Open `index.html` directly in a browser, or serve it with any static file server:

```bash
# Python
python -m http.server 8000

# Node (npx)
npx serve .
```

## Architecture

The site is a self-contained `index.html` with:

- **Tailwind CSS** (CDN) — all styling via utility classes, no separate CSS file
- **AOS** (Animate On Scroll, CDN) — scroll-triggered fade-in animations
- **Vanilla JS** (inline `<script>` at end of `<body>`) — handles mobile menu toggle, accordion component, and page load animation

### Page Sections (in order)

1. Header/Nav — sticky, with mobile hamburger menu
2. Hero — main CTA
3. About Us — mission and vision
4. Services — two subsections:
   - *Colegio Virtual Gratuito* (free online school for adults)
   - *Asesorías en Gestión Educacional* (consulting, shown via accordion)
5. Support Us — donation appeal
6. Contact — form (name, email, school, RBD, phone, message)
7. Footer

### Color Scheme

- Primary: Teal
- Accent: Orange
- Backgrounds: Gray shades

### Images

External images are loaded from Unsplash URLs embedded in the HTML.
