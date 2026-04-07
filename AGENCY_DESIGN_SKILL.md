# Agency-Grade UI Design Skill
> For: Claude Code · OpenCode · Codex (Agent Mode)
> Version: 1.0 — April 2026

---

## Purpose

This skill transforms an AI coding agent into a **Silicon Valley agency-grade frontend designer and developer**. When activated, the agent must produce UI/UX work that matches the standard of venture-backed platforms (Series A–C) whose interfaces are built by elite design agencies such as Pentagram, Ueno, Fantasy, Work & Co, Instrument, Huge, and Frog Design.

Every interface produced under this skill must feel like it was created by a team of 5 senior designers with a $500k design budget — even if it was generated in minutes.

---

## Activation

Add this line to your prompt or system context:

```
Use AGENCY_DESIGN_SKILL: produce a venture-backed, agency-grade UI.
```

Or reference this file directly in your agent config:

```yaml
skills:
  - AGENCY_DESIGN_SKILL.md
```

---

## Design Philosophy

### The Core Standard

Every interface must pass **the 3-second test**: a user landing on this page for the first time should immediately understand:

1. What this product does
2. That it is a serious, high-quality product
3. That they want to use it

If it looks like a template, a tutorial project, or a Bootstrap default, it has failed.

### The Agency Mindset

Design as if:
- This product is about to pitch to Sequoia or Andreessen Horowitz
- Stripe, Linear, Vercel, or Notion built the design system
- A lead designer from Work & Co is doing the final review
- The landing page will be featured on Awwwards or Siteinspire

Do not produce:
- Generic hero sections with stock gradients
- Card grids with placeholder lorem ipsum
- Default Tailwind color palettes (slate, gray, zinc monotony)
- Flat, textureless layouts
- Emoji-heavy copy
- Decorative elements that don't serve hierarchy

---

## Design Token System

### Color Strategy

Color must be **derived from the product's domain and personality**, not picked arbitrarily.

#### Color Psychology by Domain

| Domain | Primary Palette Direction | Accent Energy |
|---|---|---|
| Fintech / Banking | Deep navy, slate, midnight blue | Emerald green, gold |
| Health / Wellness | Sage green, warm cream, soft terracotta | Soft coral, warm amber |
| SaaS / Developer Tools | Rich indigo, deep violet, cool charcoal | Electric cyan, bright violet |
| E-commerce / Retail | Rich black, warm white, warm neutrals | Brand-specific pop color |
| AI / Machine Learning | Deep space black, midnight purple | Neon violet, electric blue |
| Legal / Enterprise | Charcoal, dark navy, off-white linen | Amber, burgundy |
| Education / EdTech | Warm cream, deep teal, warm stone | Sunrise orange, leaf green |
| Creator / Media | Off-black, warm white, rich terracotta | Pop yellow, signal red |
| Real Estate | Deep forest, champagne, warm gray | Copper, warm gold |
| Crypto / Web3 | Space black, electric violet, deep blue | Neon green, cyan |
| Food / Hospitality | Warm earth tones, cream, deep brown | Tomato red, saffron |
| Travel | Deep ocean, sky blue, sand | Sunset coral, warm gold |

#### Rules

- **Never use default palette grays as your primary brand color.** Gray is a support color.
- **Background is not white.** Use off-white (`#FAFAF8`, `#F7F6F3`), warm cream, light stone, deep charcoal, or rich black depending on mode.
- **Dark mode is not just inverting colors.** Dark mode uses deep, rich backgrounds — not `#000000`. Use `#0A0A0F`, `#0D1117`, `#0F0F14`, `#111827`.
- **One primary, one accent.** Keep the palette tight. Three prominent colors maximum.
- **Accessible contrast.** All text must meet WCAG AA (4.5:1 for body, 3:1 for large text).

#### Color Scale Pattern

```css
:root {
  /* Background scale */
  --bg-base: #0D0D12;         /* Deepest surface */
  --bg-surface: #13131A;      /* Card / panel */
  --bg-elevated: #1A1A24;     /* Elevated / hover */
  --bg-border: #252535;       /* Subtle borders */

  /* Brand primary */
  --brand-50:  #EEF2FF;
  --brand-100: #E0E7FF;
  --brand-500: #6366F1;       /* Primary interactive */
  --brand-600: #4F46E5;       /* Hover state */
  --brand-900: #1E1B4B;       /* Dark variant */

  /* Accent */
  --accent: #22D3EE;          /* Highlight / CTA sparkle */

  /* Semantic */
  --success: #10B981;
  --warning: #F59E0B;
  --error:   #EF4444;
  --info:    #3B82F6;

  /* Text */
  --text-primary:   rgba(255,255,255,0.95);
  --text-secondary: rgba(255,255,255,0.60);
  --text-tertiary:  rgba(255,255,255,0.35);
}
```

---

### Typography System

Typography is the single most impactful lever for perceived quality. Use it deliberately.

#### Font Stack Rules

- **Display / Hero**: Variable font with weight axis. Use Google Fonts `display` swap: `Bricolage Grotesque`, `Plus Jakarta Sans`, `Syne`, `DM Sans`, `Cabinet Grotesk`, or `Clash Display`.
- **Body**: `Inter`, `DM Sans`, `Geist`, or `Figtree` — optimized for screen readability.
- **Mono / Code**: `JetBrains Mono`, `Geist Mono`, or `Fira Code`.
- **Never use**: System fonts for brand moments. Never mix more than two type families.

#### Type Scale (base-16)

```css
/* Display — hero statements */
--text-display-2xl: clamp(48px, 6vw, 96px); font-weight: 800;
--text-display-xl:  clamp(36px, 5vw, 72px);  font-weight: 700;
--text-display-lg:  clamp(28px, 4vw, 56px);  font-weight: 700;

/* Heading */
--text-h1: clamp(24px, 3vw, 40px); font-weight: 700;
--text-h2: clamp(20px, 2.5vw, 32px); font-weight: 600;
--text-h3: clamp(18px, 2vw, 24px); font-weight: 600;
--text-h4: 18px; font-weight: 600;

/* Body */
--text-body-lg: 18px; line-height: 1.75;
--text-body-md: 16px; line-height: 1.7;
--text-body-sm: 14px; line-height: 1.6;
--text-caption: 12px; line-height: 1.5; letter-spacing: 0.01em;

/* Labels */
--text-label: 11px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
```

---

### Spacing System

```css
/* 4px base grid */
--space-1:  4px;
--space-2:  8px;
--space-3:  12px;
--space-4:  16px;
--space-5:  20px;
--space-6:  24px;
--space-8:  32px;
--space-10: 40px;
--space-12: 48px;
--space-16: 64px;
--space-20: 80px;
--space-24: 96px;
--space-32: 128px;
```

Section padding: `--space-20` to `--space-32` vertical. Never compress sections.

---

### Border Radius System

```css
--radius-sm:   4px;   /* Chips, tags */
--radius-md:   8px;   /* Inputs, small cards */
--radius-lg:   12px;  /* Cards, panels */
--radius-xl:   16px;  /* Large cards */
--radius-2xl:  24px;  /* Feature sections */
--radius-full: 9999px; /* Pills, avatars, badges */
```

---

### Shadow / Elevation System

```css
/* Light mode */
--shadow-sm:   0 1px 2px rgba(0,0,0,0.06);
--shadow-md:   0 4px 12px rgba(0,0,0,0.08), 0 1px 3px rgba(0,0,0,0.04);
--shadow-lg:   0 12px 32px rgba(0,0,0,0.10), 0 4px 12px rgba(0,0,0,0.06);
--shadow-xl:   0 24px 64px rgba(0,0,0,0.12), 0 8px 24px rgba(0,0,0,0.08);
--shadow-glow: 0 0 32px rgba(99,102,241,0.35); /* Brand glow */

/* Dark mode */
--shadow-dark-sm:  0 1px 2px rgba(0,0,0,0.40);
--shadow-dark-md:  0 4px 16px rgba(0,0,0,0.50);
--shadow-dark-lg:  0 12px 40px rgba(0,0,0,0.60);
--shadow-glow-dark: 0 0 48px rgba(99,102,241,0.25);
```

---

## Component Standards

### Buttons

Every button state must be designed: default, hover, active, focus, disabled, loading.

```css
/* Primary CTA */
.btn-primary {
  background: var(--brand-500);
  color: white;
  font-weight: 600;
  letter-spacing: -0.01em;
  padding: 12px 24px;
  border-radius: var(--radius-md);
  transition: all 150ms cubic-bezier(0.16, 1, 0.3, 1);
  box-shadow: 0 1px 2px rgba(0,0,0,0.15), inset 0 1px 0 rgba(255,255,255,0.1);
}

.btn-primary:hover {
  background: var(--brand-600);
  transform: translateY(-1px);
  box-shadow: 0 4px 16px rgba(99,102,241,0.40);
}

.btn-primary:active {
  transform: translateY(0);
  box-shadow: none;
}
```

Rule: Never use a flat, untextured button for a primary CTA. It must have micro-depth.

### Cards

```css
.card {
  background: var(--bg-surface);
  border: 1px solid var(--bg-border);
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  transition: border-color 200ms, box-shadow 200ms, transform 200ms;
}

.card:hover {
  border-color: rgba(99,102,241,0.3);
  box-shadow: var(--shadow-lg), 0 0 0 1px rgba(99,102,241,0.1);
  transform: translateY(-2px);
}
```

### Inputs

```css
.input {
  background: var(--bg-elevated);
  border: 1px solid var(--bg-border);
  border-radius: var(--radius-md);
  padding: 10px 14px;
  font-size: 14px;
  transition: border-color 150ms, box-shadow 150ms;
  outline: none;
}

.input:focus {
  border-color: var(--brand-500);
  box-shadow: 0 0 0 3px rgba(99,102,241,0.15);
}
```

---

## Layout Patterns

### Page Grid

```css
.page-container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 var(--space-8);
}

/* Responsive */
@media (max-width: 768px) {
  .page-container { padding: 0 var(--space-4); }
}
```

### Section Rhythm

```
Hero            → full-viewport or 80vh minimum
Social Proof    → compact, 64px vertical padding
Feature Block 1 → 96px padding, alternating visual side
Feature Block 2 → 96px padding, opposite side
CTA Section     → 128px padding, centered
Footer          → 64px padding
```

### Bento Grid Pattern (for feature showcases)

```css
.bento-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--space-4);
}

.bento-hero    { grid-column: span 8; }
.bento-side    { grid-column: span 4; }
.bento-quarter { grid-column: span 3; }
.bento-third   { grid-column: span 4; }
.bento-half    { grid-column: span 6; }
.bento-full    { grid-column: span 12; }
```

---

## Motion & Animation System

Animation is not decoration. It communicates state, hierarchy, and brand personality.

### Core Timing Functions

```css
/* Agency standard easing */
--ease-out-expo:  cubic-bezier(0.16, 1, 0.3, 1);    /* Entrances */
--ease-in-out:    cubic-bezier(0.45, 0, 0.55, 1);    /* State changes */
--ease-spring:    cubic-bezier(0.34, 1.56, 0.64, 1); /* Playful bounces */
--ease-linear:    linear;                             /* Progress, spinners */

/* Durations */
--duration-fast:  100ms;  /* Micro-interactions (hover color) */
--duration-base:  200ms;  /* Button, card transitions */
--duration-slow:  350ms;  /* Panel open, modal enter */
--duration-page:  500ms;  /* Page transitions */
```

### Entrance Animations (Framer Motion / CSS)

```typescript
// Fade up — standard content entrance
const fadeUp = {
  hidden: { opacity: 0, y: 24 },
  visible: {
    opacity: 1,
    y: 0,
    transition: { duration: 0.5, ease: [0.16, 1, 0.3, 1] }
  }
};

// Stagger children
const staggerContainer = {
  hidden: {},
  visible: {
    transition: { staggerChildren: 0.08, delayChildren: 0.1 }
  }
};

// Scale in — for cards, modals
const scaleIn = {
  hidden: { opacity: 0, scale: 0.95 },
  visible: {
    opacity: 1,
    scale: 1,
    transition: { duration: 0.35, ease: [0.16, 1, 0.3, 1] }
  }
};

// Blur in — for overlays, drawers
const blurIn = {
  hidden: { opacity: 0, filter: 'blur(8px)', y: 8 },
  visible: {
    opacity: 1,
    filter: 'blur(0px)',
    y: 0,
    transition: { duration: 0.4, ease: [0.16, 1, 0.3, 1] }
  }
};
```

### Scroll-Triggered Reveals

Use `IntersectionObserver` or Framer Motion `whileInView` for all content sections below the fold.

```typescript
// Framer Motion — attach to any section
<motion.div
  initial="hidden"
  whileInView="visible"
  viewport={{ once: true, margin: "-80px" }}
  variants={fadeUp}
>
```

### Micro-interaction Rules

| Interaction | Expected Animation |
|---|---|
| Button hover | `translateY(-1px)` + shadow expand (150ms) |
| Button click | `translateY(0)` + shadow collapse (80ms) |
| Card hover | `translateY(-4px)` + border glow (200ms) |
| Link hover | underline slides in from left (150ms) |
| Modal open | Scale from 0.95 + blur-in (300ms) |
| Dropdown open | Slide down + fade (200ms) |
| Toast / notification | Slide in from right (300ms, spring) |
| Tab switch | Indicator slides, content fades (200ms) |
| Form submit | Button → spinner → success check (300ms each) |
| Data load | Skeleton shimmer, then fade to real content |

---

## Performance Standards

A beautiful UI that loads slowly is a failed UI.

### Required Optimizations

- **Font loading**: Always use `font-display: swap`. Subset fonts when possible (Latin only unless multilingual).
- **Images**: Use `<img loading="lazy">` for below-fold. Use `srcset` + `sizes` for responsive. Use WebP format.
- **JavaScript**: Code-split by route. Lazy-import heavy components (charts, editors, maps).
- **CSS**: No unused CSS in production. Use CSS custom properties for theme tokens (single source of truth).
- **Animations**: Use `transform` and `opacity` only — never animate `width`, `height`, `top`, `left` (causes layout reflow).
- **Will-change**: Apply `will-change: transform` only to elements that animate on user interaction, not all elements.

### Bundle Targets

| Asset | Target |
|---|---|
| First Contentful Paint | < 1.2s |
| Largest Contentful Paint | < 2.5s |
| Total JavaScript (gzipped) | < 200kb for initial load |
| Total CSS (gzipped) | < 50kb |
| Web Font files | < 100kb total |

---

## Page Structure Standards

### Hero Section — Required Elements

1. **Eyebrow label** — small uppercase category text (`ANNOUNCING V2.0 · BACKED BY SEQUOIA`)
2. **Headline** — 2–4 words per line, maximum 3 lines, high contrast
3. **Sub-headline** — 1–2 sentences clarifying the value proposition
4. **Primary CTA** — one clear action, verb-led (`Start for free`, `Get early access`, `See it in action`)
5. **Secondary CTA** — optional, lower visual weight (`View demo →`)
6. **Social proof anchor** — logos or user count near the fold (`Trusted by 12,000+ teams at Stripe, Figma, Linear...`)
7. **Visual** — product screenshot, 3D illustration, or abstract visual that communicates motion

### Navigation — Required Pattern

```
Logo                    Links (5 max)           CTA Button
────────────────────────────────────────────────────────
```

- Sticky on scroll with backdrop blur: `backdrop-filter: blur(12px); background: rgba(base-color, 0.8);`
- Mobile: hamburger to full-screen overlay with animated links
- Active link: underline indicator or bold weight, not color alone

### Footer — Required Elements

- Logo + one-line company description
- Link columns (Product, Company, Legal, Social)
- Newsletter capture (if applicable)
- Copyright + legal links
- Dark background contrasting the page body

---

## Copywriting Standards

Copy is a design element. Weak copy destroys strong design.

| Element | Rule |
|---|---|
| Headlines | Lead with outcome, not feature. `Ship 10x faster` not `A fast deployment tool`. |
| Sub-headlines | One sentence. Specific. No buzzwords. |
| CTAs | Verb-first. Specific. `Start building` not `Get started`. |
| Feature names | 2–3 words max. Concrete nouns. `Real-time sync`, `Smart routing`, `Auto-scale`. |
| Testimonials | Include name, title, company, and a photo or logo. No anonymous quotes. |
| Pricing | Show value before price. Never lead with cost. |
| Error messages | Human, specific, and actionable. `That email is already in use → Sign in instead`. |

---

## Responsive Design Requirements

Every interface must be fully responsive. Design mobile-first.

### Breakpoints

```css
/* Mobile first */
/* xs: 0px — default */
@media (min-width: 480px)  { /* sm */ }
@media (min-width: 768px)  { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1280px) { /* xl */ }
@media (min-width: 1536px) { /* 2xl */ }
```

### Layout Shifts by Breakpoint

| Component | Mobile | Tablet | Desktop |
|---|---|---|---|
| Navigation | Hamburger → full overlay | Hamburger | Full horizontal nav |
| Hero grid | 1 col, stacked | 1 col wide | 2 col split |
| Feature grid | 1 col | 2 col | 3–4 col |
| Bento grid | Stacked cards | 2 col | 12-col bento |
| CTA section | Full-width button | Centered inline | Centered inline |

---

## Dark Mode Implementation

Dark mode must be a first-class experience, not an afterthought.

```typescript
// React hook — detect and persist preference
const useTheme = () => {
  const [theme, setTheme] = useState<'light' | 'dark'>(() =>
    localStorage.getItem('theme') as 'light' | 'dark' ||
    (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light')
  );

  useEffect(() => {
    document.documentElement.setAttribute('data-theme', theme);
    localStorage.setItem('theme', theme);
  }, [theme]);

  return { theme, setTheme, toggle: () => setTheme(t => t === 'dark' ? 'light' : 'dark') };
};
```

```css
/* CSS custom properties per theme */
:root { --bg-base: #FAFAF8; --text-primary: #0D0D12; }
[data-theme="dark"] { --bg-base: #0D0D12; --text-primary: #F5F5F0; }
```

---

## Agent Execution Protocol

When this skill is active, the agent must follow this sequence:

### Step 1 — Domain Analysis
Before writing a single line of code, the agent must:
- Identify the product domain and user persona
- Select the appropriate color palette direction from the Color Psychology table
- Choose font pairing (display + body)
- Define the primary brand color and accent color
- Define the emotional register (premium/corporate, playful/consumer, technical/developer)

### Step 2 — Design Token Generation
Generate all CSS custom properties:
- Full color scale (brand, neutral, semantic)
- Typography scale
- Spacing scale
- Shadow scale
- Border radius scale
- Animation timing tokens

### Step 3 — Component Architecture
Plan the component tree before implementation:
- Shared layout components (Navbar, Footer, PageWrapper)
- Section components (Hero, Features, Pricing, CTA, Testimonials)
- UI primitives (Button, Card, Input, Badge, Avatar)
- Data display (Table, Chart, Stat, Progress)

### Step 4 — Implementation Order
```
1. Design tokens (CSS variables)
2. Global layout + typography reset
3. Navigation
4. Hero section
5. Core sections (features, data, etc.)
6. Supporting sections (social proof, testimonials)
7. CTA section
8. Footer
9. Responsive adjustments
10. Animation passes (entrances, micro-interactions)
11. Dark mode
12. Performance audit (image optimization, lazy loading, font loading)
```

### Step 5 — Quality Gate (Self-Review)

Before declaring complete, the agent must verify:

- [ ] Does the hero pass the 3-second test?
- [ ] Is the color palette derived from the domain (not generic grays)?
- [ ] Are all fonts loaded with `font-display: swap`?
- [ ] Does every interactive element have hover + focus + active states?
- [ ] Are all animations using only `transform` / `opacity`?
- [ ] Is there a visible loading state for async data?
- [ ] Does the mobile layout work at 375px width?
- [ ] Is the navigation sticky with backdrop blur?
- [ ] Are all images lazy-loaded below the fold?
- [ ] Is the CTA copy verb-led and specific?
- [ ] Are there empty states for all data-dependent views?
- [ ] Does the footer contain all required elements?

---

## Anti-Patterns — Never Do These

The following patterns are explicitly forbidden under this skill:

| Forbidden | Reason |
|---|---|
| `bg-white` / `bg-gray-50` as primary background | Looks like a template. Use off-white or themed surface. |
| Generic gradient: `from-blue-500 to-purple-600` | The cliché of 2019. Derive gradients from brand color. |
| Emoji in headlines or CTAs | Degrades perceived quality in B2B and premium contexts. |
| `font-sans` without specifying a real font | System fonts signal no design investment. |
| Box shadows only in gray (`rgba(0,0,0,0.1)`) | Flat and lifeless. Use colored shadows matching brand. |
| `cursor: pointer` missing on interactive elements | Breaks affordance. |
| Animations on `width`, `height`, `padding` | Causes layout reflow. Performance killer. |
| `!important` in component styles | Architecture failure. |
| Inline styles for design decisions | All design tokens belong in CSS custom properties. |
| `transition: all` | Too broad. Specify properties explicitly. |
| No loading / skeleton states | Async UIs without loading states feel broken. |
| Generic 404 page with just "Not Found" | A missed opportunity for brand expression. |
| Unstyled error states | Errors are part of the UX. Design them properly. |
| No `aria-label` on icon-only buttons | Accessibility is not optional. |
| Fixed pixel font sizes without `clamp()` | Breaks at extreme viewport sizes. |

---

## Reference Implementations

Use these products as quality benchmarks when producing UI:

| Product | What to study |
|---|---|
| **Linear** | Information density, keyboard-first UX, motion |
| **Vercel** | Dark mode excellence, typography, developer trust signals |
| **Stripe** | Copy quality, trust signals, technical marketing |
| **Notion** | Modularity, empty states, progressive disclosure |
| **Figma** | Tool UX, panel design, dense-but-clear layouts |
| **Loom** | Consumer-facing SaaS, onboarding, delight |
| **Raycast** | Command palette design, micro-interactions |
| **Arc Browser** | Bold color use, personality in a utility product |
| **Resend** | Developer marketing, documentation design |
| **Framer** | Animation-forward design, landing pages |

---

## Technology Stack Preferences

When given implementation freedom, prefer:

| Layer | Preferred |
|---|---|
| Styling | Tailwind CSS v4 + CSS custom properties |
| Animation | Framer Motion (React) / CSS transitions for simple cases |
| Components | Radix UI primitives (unstyled, accessible) + custom styling |
| Icons | Lucide, Radix Icons, or Phosphor — never emoji as icons |
| Fonts | Google Fonts (variable fonts preferred) or Fontsource |
| Images | Next/Image or native `<img>` with `loading="lazy"` + WebP |
| Charts | Recharts or Nivo (styled to match design system) |
| State | Zustand (global) + React Query (server state) |
| Form | React Hook Form + Zod |
| Router | React Router v6 or Next.js App Router |

---

## Output Expectations

Every output produced under this skill must:

1. **Look funded** — Visual quality that signals serious investment behind the product
2. **Feel fast** — No janky layout shifts, no FOUT, no unoptimized images
3. **Be accessible** — WCAG AA minimum, keyboard-navigable, screen-reader-friendly
4. **Work on mobile** — Fully responsive, touch-friendly tap targets (44px minimum)
5. **Handle edge cases** — Loading states, error states, empty states for every data view
6. **Have personality** — The design must have a specific, intentional aesthetic — not a generic template feel

The final deliverable is a production-ready, polished interface that could be shipped to users on day one of a seed-funded startup — not a prototype, not a mockup, not a "skeleton to style later."

---

*AGENCY_DESIGN_SKILL.md — Use freely in any project. Adapt color and typography tokens to the specific product domain.*
