# GitHub Copilot — Agency Design Instructions

  This project requires **agency-grade, venture-backed UI quality** for all frontend work.

  ## Core Directive

  Every interface you generate must pass the 3-second test: a first-time visitor immediately understands what the product does, that it is serious and high-quality, and that they want to use it. Generic templates, Bootstrap defaults, and lorem ipsum placeholders are not acceptable.

  ## Design Standard

  Design as if:
  - This product pitches to Sequoia Capital next week
  - Stripe, Linear, or Vercel built the design system
  - A lead designer from Work & Co or Ueno reviews every screen

  ## Required Practices

  ### Color
  - Derive the palette from the product domain (fintech → navy/emerald, SaaS → indigo/violet, AI → space-black/cyan, etc.)
  - Never use `#ffffff` or `#000000` as surface colors
  - Dark mode backgrounds: `#0D0D12`, `#0D1117`, `#0F0F14`, or similar deep rich tones
  - Always include a brand color scale (50–900) and one accent color

  ### Typography
  - Load a variable display font via Google Fonts (`Bricolage Grotesque`, `Plus Jakarta Sans`, `Syne`, `DM Sans`)
  - Always use `font-display: swap`
  - Use fluid `clamp()` sizing for all display and heading text
  - Never use system font stacks for brand moments

  ### Components — All States Required
  Every interactive component must implement: default · hover · active · focus · disabled · loading

  ### Animation Rules
  - Only animate `transform` and `opacity` (never layout properties — no width, height, top, left)
  - Use cubic-bezier easing: `cubic-bezier(0.16, 1, 0.3, 1)` for entrances
  - Stagger list items with 80ms delay between children
  - Add `whileInView` or `IntersectionObserver` reveals for below-fold sections

  ### Performance
  - Lazy-load all images below the fold
  - Code-split by route
  - Target: FCP < 1.2s, LCP < 2.5s, JS bundle < 200kb gzipped

  ### Accessibility
  - WCAG AA contrast on all text
  - `aria-label` on all icon-only buttons
  - Keyboard navigable interactive elements
  - Minimum 44px touch targets on mobile

  ## Forbidden Patterns

  | Never do | Do instead |
  |---|---|
  | `bg-white` as page background | Use off-white: `#FAFAF8`, `#F7F6F3` |
  | `from-blue-500 to-purple-600` gradient | Derive gradients from brand color |
  | Emoji in CTAs or headlines | Use text or icons from Lucide/Phosphor |
  | `transition: all` | Specify: `transition: transform 200ms, opacity 200ms` |
  | Unstyled 404/error pages | Design them with brand expression |
  | Fixed `px` font sizes | Use `clamp(min, preferred, max)` |
  | Flat untextured primary buttons | Add `box-shadow` + hover `translateY(-1px)` |

  ## Reference Implementations

  Study and match the quality of: **Linear · Vercel · Stripe · Notion · Raycast · Arc Browser · Framer**
  