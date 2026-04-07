# Agency Design — Quick Reference Cheat Sheet
> Consulta rápida · Hex codes reales · Valores listos para copiar

---

## Color Palettes by Domain

### SaaS / Developer Tools
```
Background:  #0D0D12   Surface:  #13131A   Border:  #1E1E2E
Brand:       #6366F1   Hover:    #4F46E5   Accent:  #22D3EE
Text:        #F0F0FF   Muted:    #8B8BA8
```

### AI / Machine Learning
```
Background:  #08080F   Surface:  #0F0F1A   Border:  #1A1A2E
Brand:       #7C3AED   Hover:    #6D28D9   Accent:  #06B6D4
Text:        #F5F3FF   Muted:    #9490B8
```

### Fintech / Banking
```
Background:  #F7F8FA   Surface:  #FFFFFF   Border:  #E4E7EC
Brand:       #1A2B5E   Hover:    #0F1D45   Accent:  #10B981
Text:        #111827   Muted:    #6B7280
Dark bg:     #0A1628   Dark surface: #0F1E38
```

### Health / Wellness
```
Background:  #F9F8F4   Surface:  #FFFFFF   Border:  #E8E4DC
Brand:       #3D6B4F   Hover:    #2D5040   Accent:  #E8845A
Text:        #1C2017   Muted:    #6B7060
Dark bg:     #0F1A12   Dark surface: #162019
```

### E-commerce / Retail
```
Background:  #FAFAF8   Surface:  #FFFFFF   Border:  #EBEBEB
Brand:       #111111   Hover:    #333333   Accent:  #E63946
Text:        #111111   Muted:    #737373
Dark bg:     #0A0A0A   Dark surface: #141414
```

### Real Estate
```
Background:  #F5F2EE   Surface:  #FFFFFF   Border:  #DDD8D0
Brand:       #1C3A2B   Hover:    #142A1F   Accent:  #C5942A
Text:        #1C1C18   Muted:    #78726A
Dark bg:     #0D1A11   Dark surface: #152219
```

### Crypto / Web3
```
Background:  #06060A   Surface:  #0D0D14   Border:  #1A1A28
Brand:       #8B5CF6   Hover:    #7C3AED   Accent:  #00F5A0
Text:        #F8F7FF   Muted:    #9D9AB8
```

### Education / EdTech
```
Background:  #FDFCF7   Surface:  #FFFFFF   Border:  #E9E4D8
Brand:       #0F5F73   Hover:    #0A4559   Accent:  #F4874B
Text:        #1A1A16   Muted:    #6B6960
```

### Creator / Media
```
Background:  #F8F5F0   Surface:  #FFFFFF   Border:  #E8E2D8
Brand:       #1A1A1A   Hover:    #333333   Accent:  #D4621A
Text:        #1A1A1A   Muted:    #6B6560
Dark bg:     #0A0A08   Dark surface: #141410
```

### Legal / Enterprise
```
Background:  #F6F5F2   Surface:  #FFFFFF   Border:  #E2DFD9
Brand:       #1C2B3A   Hover:    #111E28   Accent:  #B45309
Text:        #1C1C1A   Muted:    #6B6860
Dark bg:     #0D1319   Dark surface: #131C25
```

### Food / Hospitality
```
Background:  #FBF8F3   Surface:  #FFFFFF   Border:  #EDE7DC
Brand:       #8B2500   Hover:    #6B1A00   Accent:  #D4A017
Text:        #1C1510   Muted:    #6B6058
Dark bg:     #160A00   Dark surface: #1F1000
```

### Travel
```
Background:  #F4F8FC   Surface:  #FFFFFF   Border:  #D6E4F0
Brand:       #0A4C6E   Hover:    #063852   Accent:  #F4845F
Text:        #0D1B2A   Muted:    #5A7A8A
Dark bg:     #040F1A   Dark surface: #071828
```

---

## Semantic Colors (universal)

```
Success green:  #10B981   bg: #ECFDF5   border: #A7F3D0
Warning amber:  #F59E0B   bg: #FFFBEB   border: #FDE68A
Error red:      #EF4444   bg: #FEF2F2   border: #FECACA
Info blue:      #3B82F6   bg: #EFF6FF   border: #BFDBFE
```

---

## Typography — Ready to Use

### Google Fonts import (paste in `<head>`)
```html
<!-- Display + Body combo -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,300..800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

### Font pairings
| Display | Body | Personality |
|---|---|---|
| Bricolage Grotesque | Inter | Modern SaaS, editorial |
| Plus Jakarta Sans | DM Sans | Friendly, startup |
| Syne | Inter | Bold, creative |
| Cabinet Grotesk | Geist | Developer tool |
| DM Serif Display | DM Sans | Premium, editorial |
| Clash Display | Inter | Web3, crypto |

### Type scale (copy-paste CSS)
```css
:root {
  --font-display: 'Bricolage Grotesque', sans-serif;
  --font-body:    'Inter', sans-serif;
  --font-mono:    'JetBrains Mono', monospace;

  --text-2xl: clamp(48px, 6vw,  88px);
  --text-xl:  clamp(36px, 5vw,  64px);
  --text-lg:  clamp(28px, 4vw,  48px);
  --text-h1:  clamp(24px, 3vw,  40px);
  --text-h2:  clamp(20px, 2.5vw,32px);
  --text-h3:  clamp(18px, 2vw,  24px);
  --text-h4:  18px;
  --text-body:16px;
  --text-sm:  14px;
  --text-xs:  12px;
  --text-label: 11px;

  --leading-tight:  1.2;
  --leading-snug:   1.4;
  --leading-normal: 1.6;
  --leading-loose:  1.75;

  --tracking-tight:  -0.03em;
  --tracking-normal: -0.01em;
  --tracking-wide:   0.04em;
  --tracking-wider:  0.08em;
}
```

---

## Spacing Scale

```css
:root {
  --s-1:  4px;   --s-2:  8px;   --s-3:  12px;  --s-4:  16px;
  --s-5:  20px;  --s-6:  24px;  --s-8:  32px;  --s-10: 40px;
  --s-12: 48px;  --s-16: 64px;  --s-20: 80px;  --s-24: 96px;
  --s-32: 128px; --s-40: 160px; --s-48: 192px;

  /* Section vertical padding */
  --section-sm: 64px;
  --section-md: 96px;
  --section-lg: 128px;

  /* Page container */
  --container: 1280px;
  --container-tight: 960px;
  --container-prose: 720px;
  --gutter: 32px;
  --gutter-sm: 16px;
}
```

---

## Border Radius

```css
:root {
  --r-xs:   2px;
  --r-sm:   4px;
  --r-md:   8px;
  --r-lg:   12px;
  --r-xl:   16px;
  --r-2xl:  24px;
  --r-3xl:  32px;
  --r-full: 9999px;
}
```

---

## Shadow Scale

```css
:root {
  /* Light mode */
  --shadow-xs: 0 1px 2px rgba(0,0,0,0.05);
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.07), 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08), 0 2px 4px rgba(0,0,0,0.04);
  --shadow-lg: 0 12px 32px rgba(0,0,0,0.10), 0 4px 8px rgba(0,0,0,0.05);
  --shadow-xl: 0 24px 64px rgba(0,0,0,0.12), 0 8px 16px rgba(0,0,0,0.06);

  /* Dark mode (replace rgba with your brand color for glow) */
  --shadow-dark-sm: 0 1px 3px rgba(0,0,0,0.40);
  --shadow-dark-md: 0 4px 16px rgba(0,0,0,0.50), 0 2px 4px rgba(0,0,0,0.30);
  --shadow-dark-lg: 0 12px 40px rgba(0,0,0,0.60), 0 4px 8px rgba(0,0,0,0.40);

  /* Brand glow (substitute your brand color) */
  --shadow-glow-indigo:  0 0 32px rgba(99,102,241,0.30);
  --shadow-glow-violet:  0 0 32px rgba(124,58,237,0.30);
  --shadow-glow-cyan:    0 0 32px rgba(6,182,212,0.30);
  --shadow-glow-emerald: 0 0 32px rgba(16,185,129,0.30);
}
```

---

## Animation — Easing Curves

```css
:root {
  --ease-out:      cubic-bezier(0.16, 1, 0.3, 1);     /* Entrances — fast in, slow out */
  --ease-in:       cubic-bezier(0.7, 0, 0.84, 0);     /* Exits */
  --ease-in-out:   cubic-bezier(0.45, 0, 0.55, 1);    /* State changes */
  --ease-spring:   cubic-bezier(0.34, 1.56, 0.64, 1); /* Bouncy / playful */
  --ease-smooth:   cubic-bezier(0.25, 0.46, 0.45, 0.94);

  --dur-fast:   100ms;
  --dur-base:   200ms;
  --dur-slow:   350ms;
  --dur-slower: 500ms;
}
```

### Framer Motion variants (copy-paste)
```typescript
export const fadeUp = {
  hidden:  { opacity: 0, y: 20 },
  visible: { opacity: 1, y: 0, transition: { duration: 0.5, ease: [0.16,1,0.3,1] } },
};
export const fadeIn = {
  hidden:  { opacity: 0 },
  visible: { opacity: 1, transition: { duration: 0.4, ease: [0.16,1,0.3,1] } },
};
export const scaleIn = {
  hidden:  { opacity: 0, scale: 0.94 },
  visible: { opacity: 1, scale: 1, transition: { duration: 0.35, ease: [0.16,1,0.3,1] } },
};
export const stagger = {
  visible: { transition: { staggerChildren: 0.08, delayChildren: 0.05 } },
};
export const slideRight = {
  hidden:  { opacity: 0, x: -16 },
  visible: { opacity: 1, x: 0, transition: { duration: 0.4, ease: [0.16,1,0.3,1] } },
};
```

---

## Component Snippets

### Primary Button (CSS)
```css
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 11px 22px;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: -0.01em;
  border-radius: var(--r-md);
  border: none;
  cursor: pointer;
  transition: transform 150ms var(--ease-out),
              box-shadow 150ms var(--ease-out),
              background 150ms;
}
.btn-primary {
  background: var(--brand);
  color: #fff;
  box-shadow: 0 1px 2px rgba(0,0,0,0.18),
              inset 0 1px 0 rgba(255,255,255,0.12);
}
.btn-primary:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 16px var(--brand-glow),
              0 1px 2px rgba(0,0,0,0.15);
}
.btn-primary:active { transform: translateY(0); box-shadow: none; }
.btn-primary:disabled { opacity: 0.45; cursor: not-allowed; transform: none; }
```

### Card (CSS)
```css
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--r-lg);
  padding: var(--s-6);
  transition: border-color 200ms, box-shadow 200ms, transform 200ms var(--ease-out);
}
.card:hover {
  border-color: color-mix(in srgb, var(--brand) 30%, transparent);
  box-shadow: var(--shadow-lg),
              0 0 0 1px color-mix(in srgb, var(--brand) 10%, transparent);
  transform: translateY(-3px);
}
```

### Input (CSS)
```css
.input {
  width: 100%;
  padding: 10px 14px;
  font-size: 14px;
  background: var(--bg-elevated);
  border: 1px solid var(--border);
  border-radius: var(--r-md);
  color: var(--text-primary);
  outline: none;
  transition: border-color 150ms, box-shadow 150ms;
}
.input:focus {
  border-color: var(--brand);
  box-shadow: 0 0 0 3px color-mix(in srgb, var(--brand) 18%, transparent);
}
.input::placeholder { color: var(--text-tertiary); }
```

### Sticky Nav (CSS)
```css
.nav {
  position: sticky;
  top: 0;
  z-index: 50;
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  background: color-mix(in srgb, var(--bg-base) 80%, transparent);
  border-bottom: 1px solid var(--border);
  transition: background 200ms;
}
```

### Skeleton shimmer (CSS)
```css
@keyframes shimmer {
  0%   { background-position: -200% 0; }
  100% { background-position:  200% 0; }
}
.skeleton {
  background: linear-gradient(
    90deg,
    var(--bg-elevated) 25%,
    color-mix(in srgb, var(--bg-elevated) 70%, var(--bg-surface)) 50%,
    var(--bg-elevated) 75%
  );
  background-size: 200% 100%;
  animation: shimmer 1.4s ease-in-out infinite;
  border-radius: var(--r-sm);
}
```

---

## Dark Mode Toggle (React)

```typescript
import { useState, useEffect } from 'react';

export function useTheme() {
  const [theme, setTheme] = useState<'light' | 'dark'>(() => {
    if (typeof window === 'undefined') return 'dark';
    return (localStorage.getItem('theme') as 'light' | 'dark')
      ?? (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
  });

  useEffect(() => {
    const root = document.documentElement;
    root.setAttribute('data-theme', theme);
    localStorage.setItem('theme', theme);
  }, [theme]);

  return { theme, toggle: () => setTheme(t => t === 'dark' ? 'light' : 'dark') };
}
```

```css
:root               { --bg-base: #FAFAF8; --text-primary: #111111; --surface: #FFFFFF; --border: #E5E5E5; }
[data-theme="dark"] { --bg-base: #0D0D12; --text-primary: #F0F0FA; --surface: #13131A; --border: #1E1E2E; }
```

---

## Tailwind CSS v4 — Custom Properties Integration

```css
/* globals.css */
@import "tailwindcss";

@theme {
  --color-brand:   #6366F1;
  --color-accent:  #22D3EE;
  --color-surface: #13131A;
  --color-border:  #1E1E2E;

  --font-display: 'Bricolage Grotesque', sans-serif;
  --font-body:    'Inter', sans-serif;

  --radius-card: 12px;
  --radius-btn:  8px;

  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
}
```

---

## Quality Gate Checklist

Before shipping any UI, verify:

- [ ] Background is off-white or themed — not `#fff` / `#000`
- [ ] Brand color derived from domain, not generic gray/blue
- [ ] Display font loaded with `font-display: swap`
- [ ] All heading sizes use `clamp()`
- [ ] Primary button has `box-shadow` + `translateY(-1px)` on hover
- [ ] All cards have hover lift (`translateY` + border glow)
- [ ] All inputs have `:focus` ring using brand color
- [ ] Nav is sticky with `backdrop-filter: blur`
- [ ] Animations use `transform` / `opacity` only
- [ ] Every async view has a skeleton/spinner
- [ ] Mobile layout works at 375px
- [ ] WCAG AA contrast on all text
- [ ] Icon-only buttons have `aria-label`
- [ ] Empty states are designed (not just blank)
- [ ] Error states are designed (not just red text)
