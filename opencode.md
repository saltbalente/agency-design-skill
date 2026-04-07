# OpenCode — Agency Design Instructions

  Activate this for all UI/frontend work in this project.

  ## Mission

  Produce interfaces that match the quality standard of venture-backed platforms designed by Silicon Valley's top agencies. Every screen should feel like it belongs on Awwwards.

  ## The 3-Second Rule

  Any interface you generate must pass this test: a user landing on it for the first time, in 3 seconds, must understand what the product does, believe it is a serious product, and want to use it.

  If it looks like a template — it has failed.

  ## Mandatory Skill Reference

  Follow `AGENCY_DESIGN_SKILL.md` for the full specification including:
  - Color Psychology by Domain (12 industry categories)
  - Complete Design Token System (colors, typography, spacing, shadows, radius, animation)
  - Component Standards (buttons, cards, inputs — all 5 states each)
  - Layout Patterns (bento grid, section rhythm, page containers)
  - Motion System (easing curves, entrance animations, micro-interactions)
  - Performance Standards (LCP < 2.5s, JS < 200kb gzipped)
  - Anti-Patterns (15 explicitly forbidden shortcuts)
  - 12-point Quality Gate checklist

  ## Execution Protocol

  1. **Domain Analysis** — identify the product domain and choose the palette from the Color Psychology table
  2. **Design Tokens** — generate all CSS custom properties first (colors, type, spacing, shadows, radius, animation)
  3. **Component Architecture** — plan the component tree before writing any JSX
  4. **Implementation** — follow the 12-step order in AGENCY_DESIGN_SKILL.md
  5. **Quality Gate** — run the self-review checklist before declaring done

  ## Non-negotiable Standards

  - Color derived from domain, never generic grays as brand color
  - Real display font loaded with `font-display: swap`
  - Off-white or themed surface backgrounds (never pure white or black)
  - All animations via `transform`/`opacity` only
  - Skeleton/spinner for every async operation
  - Mobile-first, tested at 375px
  - WCAG AA contrast throughout
  - Sticky nav with backdrop blur
  - Verb-led CTA copy (`Start building`, not `Get started`)
  