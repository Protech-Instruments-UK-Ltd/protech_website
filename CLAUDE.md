# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ProTech Instruments UK Ltd website - a static single-page HTML website for an industrial instrumentation company based in Batley, UK. The site showcases products, company information, AI/Software Solutions, OT Cybersecurity services, and contact details.

## Development Commands

No build process required. This is a self-contained HTML file with embedded CSS and JavaScript.

- **Preview**: Open `index.html` directly in a browser, or serve locally with `npx serve` or `python -m http.server`
- **Edit**: Edit `index.html` directly - all CSS and JavaScript are embedded in the file

## Architecture

Single-page HTML website with:
- **Navigation**: Fixed navbar with scroll effects, mobile hamburger menu - includes links to: About Us, Our Products, AI Solutions, Cybersecurity, Why Us, Contact Us
- **Hero**: Full-height section with animated background elements and premium glow effects
- **About**: Mission/Vision cards
- **Products**: Tabbed interface (3 tabs: Liquid & Gas Analyzers, Process Measurements & Control, Gauges & Switches)
- **AI / Software Solutions**: Separate service section with 4 feature cards and GIF image area
- **OT Cybersecurity Solutions**: Separate service section with gold accent theme and GIF image area
- **Why Us**: 4-column grid of value propositions
- **Contact**: Contact details + working form (client-side only, shows success message)
- **Footer**: Links, business hours, copyright

Key technical details:
- Premium background with animated particles, glows, and grid patterns
- CSS custom properties for theming (navy/teal/gold color palette)
- Rajdhani (headings), Nunito Sans (body), Share Tech Mono (accents) fonts
- IntersectionObserver for scroll-reveal animations
- No external dependencies - vanilla HTML/CSS/JS only
- Product categories are hardcoded in the HTML

## Common Tasks

- **Add new product**: Add a new `.prod-card` div inside the appropriate `.prod-panel`
- **Add new service**: Copy the `.service-section` structure (lines ~420-500), add new id, update theme colors
- **Replace GIF images**: Find `<img>` tags in service sections and replace the `src` with actual GIF URLs
- **Update contact form**: The form is client-side only - `handleForm()` shows success message without sending data. Wire to a backend service if needed.
- **Add section**: Copy an existing section structure and modify content
- **Responsive changes**: Media queries in `<style>` at lines ~175-195