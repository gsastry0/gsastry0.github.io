# CLAUDE.md - AI Assistant Guide

This file provides guidance for AI assistants working with this repository.

## Repository Overview

This is a personal website for Girish Sastry, hosted on GitHub Pages at `gsastry0.github.io`. It's a minimalist, single-page static site focused on AI governance and research.

## Project Structure

```
gsastry0.github.io/
├── index.html              # Main (and only) HTML page
├── fonts/
│   └── ibm-plex-sans-latin.woff2  # Custom font (IBM Plex Sans)
├── 6351ceb74b95d8ae.gif    # Animated hero image (radio telescope)
└── CLAUDE.md               # This file
```

## Technology Stack

- **Pure HTML/CSS**: No build tools, frameworks, or JavaScript
- **GitHub Pages**: Static site hosting (deployed from main branch)
- **Self-hosted assets**: Fonts and images are local (no external CDN)

## Design Conventions

### Styling
- Dark theme with CSS custom properties (variables in `:root`)
- Color palette:
  - `--bg: #0b0b0b` (background)
  - `--panel: #050505` (panel background)
  - `--text: #e7e7e7` (primary text)
  - `--muted: #b9b9b9` (secondary text)
  - `--hair: #262626` (borders)
- Typography: IBM Plex Sans with system font fallbacks
- Responsive layout with CSS Grid (breakpoint at 860px)
- Respects `prefers-reduced-motion` for accessibility

### Security Headers
The site includes strict security measures via meta tags:
- Content-Security-Policy (self-only sources)
- No referrer policy
- FLoC opt-out

## Development Workflow

### Local Development
Since this is a static site with no build process:
1. Edit files directly
2. Preview in browser (open `index.html` locally or use a local server)

### Deployment
- Push to main branch triggers automatic GitHub Pages deployment
- No CI/CD configuration needed

## Key Guidelines for Changes

### Do
- Maintain the minimalist, clean aesthetic
- Keep the site lightweight (no frameworks or unnecessary dependencies)
- Preserve existing security headers when adding new features
- Ensure responsive design works on mobile devices
- Test with `prefers-reduced-motion` enabled

### Don't
- Add external dependencies or CDNs (violates CSP)
- Include tracking scripts or analytics
- Add JavaScript unless absolutely necessary
- Break the single-page structure without discussion

## Content Updates

The main content areas that may need updates:
- **Bio text**: Lines 179-189 in `index.html`
- **Social links**: Lines 191-195 in `index.html`
- **Last updated date**: Line 210 in `index.html`

## Testing Changes

Before committing:
1. Validate HTML (can use W3C validator)
2. Test responsive layout at various widths
3. Verify all links work
4. Check image loading and animation

## File Naming

- Use lowercase with hyphens for new files
- The GIF uses a hash-based name for cache-busting
