# PAYOFF — Independent Growth Studio

PAYOFF is a responsive, single-page marketing-agency website built with semantic HTML, CSS, and vanilla JavaScript. It presents an editorial growth-studio proposition, connected services, a customer-journey framework, an experimentation loop, and conversion paths.

The repository contains the complete standalone website. It is frontend-only: there is no backend, database, authentication system, API, form submission service, or analytics integration.

## Overview

The page is organized as an editorial conversion experience for an agency that focuses on the handoffs between attention, acquisition, conversion, retention, and expansion. Its sections explain the business problem, growth strategy, services, methodology, client fit, operating rhythm, and final contact action.

Several proof and company-specific fields are intentionally visible placeholders. Metrics, case studies, testimonials, team information, and booking details must be replaced with approved real material before the site is presented as a live agency website.

## Implemented Features

- Sticky desktop and mobile navigation with section links
- Full-screen mobile menu with keyboard and Escape-key support
- Responsive editorial layout for desktop, tablet, and mobile
- Native HTML disclosure controls for service capabilities and FAQ answers
- Scroll-based compact header state
- Optional IntersectionObserver section reveals
- Reduced-motion support
- Skip-to-content and visible keyboard-focus styles
- Semantic page structure and descriptive image alternatives
- Dynamic footer year
- Locally packaged optimized WebP photography
- Manus deployment route declaration for `/`
- Brand favicon and SVG brand mark

## Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Markup | HTML5 | Page structure and native disclosures |
| Styling | CSS | Editorial layout, responsive breakpoints, colors, typography, and motion |
| Behavior | Vanilla JavaScript | Mobile navigation, header state, footer year, and reveal effects |
| Fonts | Google Fonts | Manrope, Instrument Serif, and DM Mono |
| Images | Local WebP assets | Photography for page sections |
| Hosting target | Static HTTP server or Manus | Serves the standalone frontend without a build step |

No JavaScript dependencies, package manager manifest, build system, or backend framework is used.

## Project Structure

```text
PayOff/
├── index.html                 # Main and only application page
├── styles.css                 # Complete visual system and responsive rules
├── script.js                  # Navigation and progressive-enhancement behavior
├── manus-routes.json          # Root route declaration
├── app.config.ts              # Manus application metadata
├── assets/
│   ├── payoff-mark.svg        # Brand mark and favicon
│   ├── image-sources.md       # Pexels source and credit information
│   └── images/                # Six optimized local WebP photographs
└── docs/
    ├── plan.md                # Implemented design and content plan
    ├── TODO.md                # Delivery checklist and launch placeholders
    └── elementor-novamira.md  # Detailed section rebuild reference
```

## Prerequisites

- A modern browser
- Python 3, for the documented local static-server command
- Network access while loading Google Fonts

The HTML, CSS, and JavaScript also work without a build tool or dependency installation. A static server is recommended for consistent local URL and asset behavior.

## Installation

The repository has no package installation step.

From the repository root:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

The entry point is `index.html`.

## Running the Website

Serve the repository with any static web server, not only Python's module server. The server must expose the repository root so relative URLs such as `styles.css`, `script.js`, and `assets/images/...` resolve correctly.

For example:

```bash
cd /path/to/PayOff
python3 -m http.server 8000
```

No application startup process or external service is required.

## Application Behavior

The page provides anchor navigation to the services, work, approach, about, insights, and contact sections.

At widths below 760 pixels:

- The navigation becomes a full-screen menu
- Opening the menu prevents page scrolling
- Selecting a link closes the menu
- Escape closes the menu and returns focus to the toggle
- Resizing above 760 pixels closes the menu

At wider widths:

- The header begins in a spacious state
- Scrolling beyond 16 pixels applies a compact contained header style

The service and FAQ rows use native `<details>` elements. JavaScript adds no replacement disclosure framework.

Reveal animations run only when the browser supports `IntersectionObserver` and the visitor has not enabled reduced motion. The page remains fully visible without JavaScript.

## Configuration

### Manus route configuration

`manus-routes.json` declares the root route:

```json
{"routes":[{"path":"/","title":"PAYOFF — Independent Growth Studio"}]}
```

### Manus application metadata

`app.config.ts` contains a Manus logo URL:

```typescript
export default {
  logoUrl: "https://files.manuscdn.com/user_upload_by_module/session_file/310519663896080175/odmSXLWEwxiRzDbM.svg"
};
```

This file is Manus-specific metadata and is not required to run the standalone website.

### External font configuration

`index.html` loads Manrope, Instrument Serif, and DM Mono from Google Fonts. CSS font fallbacks remain available if the font service cannot be reached.

There are no environment-variable files or `.env.example` in the repository.

## Public-Launch Placeholders

The repository is implemented as a complete website template, but the following content is not backed by verified project data:

- Revenue, campaign, conversion, pipeline, ROAS, acquisition, and cost metrics
- Featured and selected client work
- Client testimonials and names
- Team portrait and lead profile
- Company year and location
- Final scheduling or contact destination
- Social, privacy, and terms links

The source explicitly identifies these fields as placeholders. It does not contain a real scheduling URL or backend contact endpoint.

## Accessibility

The implementation includes:

- A skip link
- Semantic landmarks and headings
- Descriptive alternative text for photographs
- Native keyboard-operable disclosures
- Visible `:focus-visible` styling
- A full-screen mobile navigation state
- `aria-expanded`, `aria-controls`, and `aria-label` updates
- Reduced-motion rules

## Image Credits

Six Pexels photographs are stored under `assets/images/` and listed in `assets/image-sources.md`. The in-page captions and alternative text identify them as illustrative stock imagery rather than PAYOFF staff or verified client work.

## Documentation

- `docs/plan.md` — design system and implementation direction
- `docs/TODO.md` — implementation status and remaining public-launch replacements
- `docs/elementor-novamira.md` — detailed rebuild reference for implementation in Elementor
- `assets/image-sources.md` — photograph sources and placement notes

## Testing

No automated test suite or test configuration is included. Validation should cover browser rendering, responsive navigation, link targets, keyboard focus, disclosures, reduced-motion behavior, and image loading.

## Known Limitations

- This is a frontend-only, static website.
- The displayed proof, case studies, testimonial, and team profile are not verified agency data.
- The contact and booking controls point to placeholder destinations and do not submit or schedule anything.
- No analytics, cookies, CMS, API, database, or form backend is implemented.
- Google Fonts require a network connection unless the fonts are otherwise available or self-hosted.

## License

No license file or license declaration is present in the repository.
