# NeuByte CDN — Content Delivery Network
The **NeuByte CDN** repository provides a centralized, version‑controlled location for all static assets used across the NeuByte Technologies ecosystem.
It hosts images, icons, CSS, JavaScript, diagrams, and manifest files that support documentation sites, portfolio pages, architecture diagrams, and application UI components.

This repository ensures consistent branding, fast asset delivery, and a single source of truth for all shared static resources.

# Purpose
NeuByte CDN exists to:

- Serve **static assets** for Resume, Portfolio, Standards, Architecture, Help Product, and Fitness App documentation
- Provide **consistent branding** across all NeuByte sites
- Host architecture diagrams and UI specification images
- Centralize CSS and JS used by multiple repos
- Support Jekyll‑based documentation sites via GitHub Pages
- Provide a stable CDN endpoint (cdn.neubyte.com) for cross‑repo consumption

This repo is foundational to the NeuByte Design System.

# Current Assets (Live)
These assets are fully implemented and actively used across NeuByte repositories.

## 1. CSS (docs/assets/css/)
Includes:
- neubyte.css — Core NeuByte design system styles
- custom.css — Repo‑specific overrides
- style.scss — SCSS source for future expansion

Used by Resume, Portfolio, Standards, and Architecture sites.

## 2. Images (docs/assets/img/)
Includes:

- NeuByte logos
- Icons
- Architecture diagrams
- Sequence diagrams
- Activity diagrams
- Fitness App domain model

Favicon and touch icons

These assets support documentation, UI specifications, and portfolio visuals.

3. Icons (docs/assets/img/icons/)
Includes:

favicon.svg

apple-touch-icon.png

Additional SVG/PNG icons for cross‑site branding

4. JavaScript (docs/js/)
Reserved for:

Lightweight UI enhancements

Menu interactions

Documentation helpers

(Currently minimal, ready for expansion.)

5. JSON (docs/json/)
Reserved for:

Manifest files

Structured metadata

Future documentation tooling

6. Web Manifest (site.webmanifest)
Defines:

App icons

Display mode

Branding metadata

Progressive enhancement support

Used by mobile browsers and modern documentation sites.

7. GitHub Pages Configuration
.nojekyll — Ensures GitHub Pages serves raw assets

CNAME — Binds the CDN to cdn.neubyte.com

# Repository Structure
Code
neubyte-cdn/
└── docs/
    ├── assets/
    │   ├── css/
    │   │   ├── custom.css
    │   │   ├── neubyte.css
    │   │   └── style.scss
    │   └── img/
    │       └── icons/
    │           ├── favicon.svg
    │           ├── apple-touch-icon.png
    │           └── ...additional icons and diagrams
    ├── js/
    ├── json/
    ├── site.webmanifest
    ├── .nojekyll
    ├── CNAME
    └── README.md
This structure keeps assets organized, scalable, and easy to consume across all NeuByte sites.

# Proposed Expansion (Roadmap)
These enhancements are planned for future development.
Once implemented and used across NeuByte sites, they will be promoted to the Live section.

A. Versioned Asset Bundles
Planned additions:

/v1/, /v2/ asset folders

Versioned CSS and JS bundles

Versioned diagram sets

Purpose:

Allow safe updates without breaking older documentation

Support long‑term stability for portfolio and standards sites

B. Component‑Level CDN Assets
Planned additions:

Button styles

Card styles

Section headers

Alert components

Purpose:

Provide reusable UI components for documentation and portfolio sites

C. Documentation Assets API
Planned additions:

JSON metadata describing diagrams

Asset lookup endpoints (static JSON)

Cross‑repo asset mapping

Purpose:

Support automated documentation generation

Enable tooling to reference assets programmatically

D. Expanded JavaScript Utilities
Planned additions:

Menu toggles

Theme switching

Diagram zooming

Documentation navigation helpers

Purpose:

Improve UX across documentation sites

E. Automated Asset Validation
Planned additions:

Cypress tests for broken images

Link validation

Manifest validation

CSS linting

Purpose:

Ensure CDN assets never break downstream sites

# Testing Strategy
As part of the October TDD initiative, the CDN will be validated using:

Cypress asset tests

HTML link checks

Image existence checks

Manifest validation

CSS linting

This ensures reliability across all NeuByte documentation and portfolio sites.

# Deployment
The CDN is deployed automatically via GitHub Pages.

Any push to main triggers:

Asset publishing

CNAME binding

Immediate availability at cdn.neubyte.com

No manual steps required.

# Contact
For updates or new asset requests:
gordon.neuls@gmail.com
