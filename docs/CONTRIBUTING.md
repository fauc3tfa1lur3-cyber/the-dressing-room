# 🤝 Contributing to The Dressing Room

Thank you for contributing to **The Dressing Room**.

Whether you're a human developer or an AI coding assistant, this document defines the development standards for the project.

The goal is to build a beautiful, scalable, and maintainable luxury fashion application that consistently delivers an exceptional user experience.

---

# Project Philosophy

The Dressing Room is not simply a wardrobe app.

It is an AI-powered luxury personal image platform.

Every contribution should support the project's core pillars:

* Luxury
* Simplicity
* Elegance
* Performance
* Accessibility
* Personalization
* Scalability
* Representation

If a proposed change makes the application feel more complicated instead of more luxurious, reconsider the approach.

---

# Design Principles

Every screen should feel like entering a luxury dressing room.

Prioritize:

* clean layouts
* generous spacing
* thoughtful animations
* elegant typography
* premium color palettes
* smooth transitions

Avoid:

* clutter
* excessive buttons
* overwhelming menus
* unnecessary visual noise

Luxury comes from restraint.

---

# Development Workflow

Before beginning any feature:

1. Read the relevant documentation in the `/docs` folder.
2. Verify that the feature aligns with the Product Requirements Document (PRD).
3. Check whether reusable components already exist.
4. Build the smallest polished version before adding enhancements.
5. Test the feature before committing changes.

---

# Documentation First

Documentation is the source of truth.

If implementation and documentation conflict:

* do not guess
* do not invent new requirements

Instead:

* update the documentation with approval, or
* request clarification before proceeding

---

# Coding Standards

## Language

* JavaScript (ES6+)
* React (.jsx)

---

## Framework

* React
* Vite

---

## Styling

Use:

* Tailwind CSS

Do not use inline styling unless absolutely necessary.

All colors, spacing, and typography should come from the design system.

---

## Icons

Use:

* Lucide React

Do not introduce additional icon libraries without approval.

---

## Animation

Use:

* Framer Motion

Animations should be:

* smooth
* subtle
* purposeful

Avoid flashy or distracting effects.

---

# Component Guidelines

Components should be:

* reusable
* modular
* small
* composable

Avoid creating components that try to do too many things.

Prefer composition over duplication.

---

# Folder Organization

Follow the documented architecture.

Example:

```text
src/

components/

pages/

hooks/

services/

store/

utils/

assets/

styles/
```

Keep folders organized by responsibility.

---

# State Management

Official solution:

Zustand

Use React Context only for lightweight providers such as theme or authentication wrappers if needed.

---

# Backend

Official backend:

* Supabase
* PostgreSQL
* Storage
* Edge Functions

Never expose API keys in frontend code.

All AI requests should flow through secure backend functions.

---

# AI Development Standards

The AI should:

* explain recommendations
* remember user preferences
* remain consistent with its personality
* use wardrobe context before making suggestions

The AI should never:

* invent wardrobe items
* recommend unavailable clothing
* ignore laundry status
* contradict stored preferences

---

# Accessibility Standards

Every feature should support:

* keyboard navigation
* readable typography
* sufficient color contrast
* descriptive labels
* screen readers where appropriate

Accessibility is a core requirement, not an optional enhancement.

---

# Performance Standards

Optimize for:

* fast page loads
* responsive interactions
* lazy-loaded images
* efficient database queries
* minimal bundle size

Avoid unnecessary re-renders and duplicate API requests.

---

# Git Workflow

For now, development will primarily occur on the `main` branch while the MVP is being built.

As the project grows, adopt a feature-branch workflow:

* `main` → stable production-ready code
* `feature/<feature-name>` → new features
* `fix/<bug-name>` → bug fixes
* `docs/<document-name>` → documentation updates

---

# Commit Message Format

Use clear, descriptive commit messages.

Examples:

```text
docs: add User-Flows documentation

feat: create luxury dashboard layout

feat: implement outfit builder

fix: resolve image upload issue

style: update Black Luxury color palette

refactor: simplify theme provider
```

Avoid generic messages like:

```text
updates

changes

fixed stuff

work
```

---

# Pull Requests

Every pull request should:

* solve one clear problem
* include a meaningful description
* avoid unrelated changes
* keep code focused and easy to review

---

# Quality Checklist

Before merging code, verify:

* Documentation is still accurate.
* Components are reusable.
* No duplicate logic exists.
* Mobile layouts work correctly.
* Accessibility has been considered.
* Theme support has not been broken.
* Existing features continue to function.

---

# AI Assistant Guidelines

If you are an AI assistant contributing to this project:

* Read all relevant documentation before writing code.
* Do not introduce undocumented features.
* Explain architectural changes before making them.
* Prefer maintainability over cleverness.
* Build incrementally.
* Preserve the project's luxury aesthetic.
* Respect the established design system and coding standards.

When uncertain, ask for clarification rather than making assumptions.

---

# Long-Term Vision

The Dressing Room is intended to evolve into a complete luxury personal image ecosystem.

Every contribution should move the project toward that vision while keeping the codebase clean, organized, and scalable.

Build with the future in mind—but only implement what is needed today.
