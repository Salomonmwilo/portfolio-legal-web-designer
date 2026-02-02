# WordPress Architecture & Theme Strategy

## Overview

This document describes the WordPress architecture chosen for the
**Legal Web Designer Portfolio**, with a focus on maintainability,
legal compliance, and UX clarity.

The project is developed locally using **Local by Flywheel**.

---

## WordPress Setup

### Local Environment

- Tool: Local by Flywheel
- Purpose: Safe local development and testing
- Deployment: Local only (no production deployment at this stage)

---

## Theme Strategy

### Parent Theme

A purchased premium WordPress theme is used as the visual and structural base
of the portfolio.

The parent theme provides:

- Responsive layout
- Modern UI components
- Compatibility with Gutenberg / page builders

Note :The parent theme is **never modified directly**.

---

### Child Theme (Compliance-Oriented)

A custom child theme is created to:

- Safely override styles and templates
- Preserve changes during theme updates
- Maintain a clear separation between vendor code and custom logic

#### Child Theme Files

- `style.css`
  - Contains the child theme declaration
  - Used for custom styling and overrides
- `functions.php`
  - Enqueues parent theme styles
  - Reserved for future compliance-related hooks or filters

---

## Rationale (Legal & UX Perspective)

Using a child theme supports:

- **Traceability** of custom changes
- **Auditability** of design and UX decisions
- **Risk reduction** when updating third-party themes
- **Clean documentation** for future clients or collaborators

This approach aligns with a legal mindset where:

- Core systems remain untouched
- Changes are controlled, documented, and reversible

---

## Next Steps

- Configure essential plugins (RGPD, accessibility, SEO)
- Create the core pages structure (Home, Services, Projects, Legal pages)
- Continue documenting legal and UX decisions in the `/docs` folder
