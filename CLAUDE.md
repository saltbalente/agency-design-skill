# Claude Code — Agency Design Instructions

  You are working in a project that requires **agency-grade, venture-backed UI quality**.

  ## Mandatory Skill

  Read and follow `AGENCY_DESIGN_SKILL.md` at the root of this repository for all frontend and design work. It is the single source of truth for every design decision.

  ## Activation

  When producing any UI, interface, component, or frontend code, activate the skill with:

  > Use AGENCY_DESIGN_SKILL: produce a venture-backed, agency-grade UI.

  ## Non-negotiable Rules

  1. **Color**: Always derive the palette from the product domain. Never use default Tailwind grays as brand color.
  2. **Typography**: Always load a real display font (Bricolage Grotesque, Syne, Plus Jakarta Sans, etc.) via Google Fonts with `font-display: swap`.
  3. **Backgrounds**: Never use pure white (`#ffffff`) or pure black (`#000000`) as page backgrounds.
  4. **Animations**: Only animate `transform` and `opacity`. Never animate layout properties.
  5. **Buttons**: Every primary CTA must have micro-depth (`box-shadow` + `translateY` on hover).
  6. **States**: Every interactive element needs hover, focus, active, and disabled states.
  7. **Loading**: Every async operation needs a skeleton or spinner state.
  8. **Mobile**: Design mobile-first. Test at 375px minimum.
  9. **Accessibility**: WCAG AA contrast on all text. `aria-label` on all icon-only buttons.
  10. **Self-review**: Run the 12-point Quality Gate checklist from `AGENCY_DESIGN_SKILL.md` before declaring done.

  ## Forbidden Patterns

  - `bg-white` / `bg-gray-50` as primary page background
  - Generic blue-to-purple gradient (`from-blue-500 to-purple-600`)
  - `transition: all` — always specify properties
  - Emoji in headlines or CTAs
  - Unstyled 404, error, or empty states
  - `font-sans` without a real font family specified
  - Any animation on `width`, `height`, `top`, `left` (causes reflow)

  ## Implementation Order

  1. Design tokens (CSS custom properties)
  2. Global layout + typography reset
  3. Navigation (sticky, backdrop blur)
  4. Hero section
  5. Core content sections
  6. Supporting sections
  7. CTA + Footer
  8. Responsive adjustments
  9. Animation pass
  10. Dark mode
  11. Performance audit
  12. Quality Gate self-review
  