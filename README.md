# Agency-Grade UI Design Skill
  > For Claude Code · OpenCode · Codex · GitHub Copilot · Any AI Agent

  A professional AI skill that transforms any coding agent into a **Silicon Valley agency-grade frontend designer**. Activate it and get UI that matches the standard of venture-backed platforms built by elite agencies — Ueno, Work & Co, Fantasy, Instrument, Frog Design.

  ---

  ## Quick Start

  ### Claude Code
  Copy `CLAUDE.md` to the root of your project. Claude Code reads it automatically on every session.

  ```bash
  curl -o CLAUDE.md https://raw.githubusercontent.com/saltbalente/agency-design-skill/main/CLAUDE.md
  ```

  ### GitHub Copilot / Codex
  Copy `.github/copilot-instructions.md` into your repo:

  ```bash
  mkdir -p .github
  curl -o .github/copilot-instructions.md https://raw.githubusercontent.com/saltbalente/agency-design-skill/main/.github/copilot-instructions.md
  ```

  ### OpenCode
  Copy `opencode.md` to your project root:

  ```bash
  curl -o opencode.md https://raw.githubusercontent.com/saltbalente/agency-design-skill/main/opencode.md
  ```

  ### Manual / Any Agent
  Paste this line at the top of any prompt:

  ```
  Use AGENCY_DESIGN_SKILL: produce a venture-backed, agency-grade UI.
  ```

  Or attach `AGENCY_DESIGN_SKILL.md` directly to the agent context.

  ---

  ## What It Does

  | Feature | Detail |
  |---|---|
  | Color system | Domain-derived palettes (12 industry categories), never generic grays |
  | Typography | Variable font pairings, fluid `clamp()` scale, display + body separation |
  | Motion | Agency-standard easing curves, scroll reveals, micro-interactions |
  | Components | Buttons, cards, inputs with all 5 states (default, hover, active, focus, disabled) |
  | Layout | Bento grids, section rhythm, 1280px containers, 4px spacing grid |
  | Performance | LCP < 2.5s, JS < 200kb gzipped, lazy images, `font-display: swap` |
  | Dark mode | First-class dark mode with rich deep backgrounds, not just color inversion |
  | Accessibility | WCAG AA contrast, keyboard nav, aria-labels, 44px touch targets |
  | Anti-patterns | 15 explicitly forbidden shortcuts that make UIs look like templates |
  | Quality gate | 12-point self-review checklist before declaring done |

  ---

  ## Reference Quality Benchmarks

  The skill instructs the agent to design at the level of: **Linear, Vercel, Stripe, Notion, Figma, Loom, Raycast, Arc, Resend, Framer**.

  ---

  ## File Index

  | File | Purpose |
  |---|---|
  | `AGENCY_DESIGN_SKILL.md` | Full skill specification (main document) |
  | `CLAUDE.md` | Claude Code auto-read file (references the skill) |
  | `.github/copilot-instructions.md` | GitHub Copilot / Codex custom instructions |
  | `opencode.md` | OpenCode agent instructions |
  | `README.md` | This file |

  ---

  ## License

  MIT — use freely in any project, commercial or personal.
  