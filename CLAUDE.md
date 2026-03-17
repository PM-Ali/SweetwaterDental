# CLAUDE.md — Modern Minimalist Website Design System
> Best practices compiled from Awwwards, Figma, Apple, Stripe, Linear, Notion, and leading design publications (2025–2026).
> Use this file to guide Claude Code when building, reviewing, or refactoring any website UI.

---

## 1. CORE PHILOSOPHY

Minimalism is not about emptiness — it is about **intentionality**. Every element must earn its place.

> "Simplicity is the ultimate sophistication." — The guiding principle of Apple, Stripe, and Linear.

### The 4 Laws of Modern Minimalism
1. **Remove everything that doesn't serve the user.** No decorative elements without purpose.
2. **Whitespace is a design element.** It creates focus, not absence.
3. **Typography does the heavy lifting.** When in doubt, let type speak.
4. **One primary action per screen.** Never compete with yourself.

---

## 2. REFERENCE WEBSITES (Best-in-Class)

These are the gold standard. Study their patterns before building anything.

| Site | Why It Stands Out |
|---|---|
| `stripe.com` | Editorial layout, gradient accents, perfect microcopy, ultra-clear hierarchy |
| `linear.app` | Monochrome palette + sharp accent, crisp iconography, tactile hover states |
| `apple.com` | Oversized photography, sparse copy, bold-yet-quiet typography, fluid spacing |
| `notion.so` | Clean content grid, strong type hierarchy, frictionless nav |
| `tend.com` | Lifestyle minimalism, warm tone, conversion-first hero |
| `grandstreetdental.com` | Art-gallery aesthetic, generous whitespace, abstract shapes |
| `everlane.com` | Product-first photography, neutral tones, honest grid |
| `braun.com` | Dieter Rams "less but better" applied to digital, strict grid, monochromatic |

---

## 3. LAYOUT & SPACING

### Grid System
- Use a **12-column fluid grid** with consistent gutters.
- Max content width: `1280px` for desktop, `768px` for tablet.
- Never let body text exceed `72ch` (characters) in width — preserves readability.
- Prefer **asymmetric layouts** over rigid symmetry for modern feel (intentional imbalance creates movement).

### Spacing Scale (use a consistent 8pt base)
```
4px   — micro gaps (icon spacing, tag padding)
8px   — small (internal component padding)
16px  — base unit
24px  — section element spacing
32px  — between components
48px  — between major sections (mobile)
64px  — between major sections (desktop)
96px  — hero/section breathing room
128px — large section separators
```

### Whitespace Rules
- Sections need **generous vertical padding** — minimum `80px` top/bottom on desktop.
- Use `1em` between paragraphs; never less than `0.5em`.
- Headings: use **1.5× more whitespace above** a heading than below it.
- Left/right page margin: minimum `24px` mobile, `48px` tablet, `80–120px` desktop.

---

## 4. TYPOGRAPHY

Typography is the #1 design element in modern minimalism. It carries personality, hierarchy, and brand voice.

### Font Stack Recommendations
```css
/* Option 1 — Clean Sans (Stripe/Linear style) */
font-family: 'Inter', 'SF Pro Display', system-ui, -apple-system, sans-serif;

/* Option 2 — Editorial Serif + Sans Pairing */
--font-heading: 'Playfair Display', 'Georgia', serif;
--font-body: 'Inter', system-ui, sans-serif;

/* Option 3 — Minimal Swiss Style */
font-family: 'Helvetica Neue', 'Arial', sans-serif;
```

### Type Scale (Modular, 1.25 ratio)
```css
--text-xs:   0.75rem;   /* 12px — labels, captions */
--text-sm:   0.875rem;  /* 14px — secondary body */
--text-base: 1rem;      /* 16px — body text */
--text-lg:   1.125rem;  /* 18px — lead paragraph */
--text-xl:   1.25rem;   /* 20px — subheadings */
--text-2xl:  1.5rem;    /* 24px — card headings */
--text-3xl:  1.875rem;  /* 30px — section headings */
--text-4xl:  2.25rem;   /* 36px — page headings */
--text-5xl:  3rem;      /* 48px — hero headings */
--text-6xl:  3.75rem;   /* 60px — oversized hero (desktop) */
--text-7xl:  4.5rem;    /* 72px — editorial statement */
```

### Typography Rules
- **Limit to 2 font families max** — one heading, one body.
- Use **variable fonts** when possible (reduces file size, enables responsive weight).
- Line height: `1.2–1.35` for headings; `1.5–1.65` for body text.
- Letter spacing: tight on large headings (`-0.02em`), normal on body (`0`), slightly wide on uppercase labels (`0.08em`).
- Body text minimum: `16px` — never smaller for readability.
- Bold headings with **light body weight** create high-impact contrast.
- Kinetic/animated typography on scroll is a standout 2025/2026 trend — use sparingly.

---

## 5. COLOR SYSTEM

### Palette Architecture
```css
/* Neutral Base (core of minimalism) */
--color-white:       #FFFFFF;
--color-gray-50:     #F9FAFB;
--color-gray-100:    #F3F4F6;
--color-gray-200:    #E5E7EB;
--color-gray-400:    #9CA3AF;
--color-gray-600:    #4B5563;
--color-gray-900:    #111827;
--color-black:       #0A0A0A;

/* One Accent Color (CTAs, links, highlights) */
--color-accent:      #your-brand-color;  /* e.g. #635BFF for Stripe-like */

/* Semantic */
--color-success:     #10B981;
--color-error:       #EF4444;
```

### Color Rules
- **Maximum 3 colors**: background, text, accent. Add a 4th only if necessary.
- Accent color is reserved for **CTAs and interactive elements only** — don't dilute it.
- Maintain **4.5:1 contrast ratio** minimum (WCAG AA) for all text.
- Dark mode: design both light and dark variations from the start.
- Avoid pure black (`#000000`) — use near-black (`#0A0A0A` or `#111827`) for warmth.
- Background: pure white feels harsh — use `#FAFAFA` or `#F9FAFB` for softness.

---

## 6. VISUAL ELEMENTS

### Imagery
- Use **high-quality, purposeful photography** — no stock clichés.
- Full-bleed hero images with subtle overlay when text is placed on top.
- Product images: always on neutral/white backgrounds with generous padding.
- Before/after comparisons work well in service businesses (dental, fitness, etc.).
- Photography should support the brand voice — not just fill space.

### Iconography
- Use a **single consistent icon library** (Lucide, Heroicons, or Phosphor).
- Icon size: `16px` inline, `20–24px` standalone, `32–40px` feature icons.
- Prefer **outline icons** for minimal aesthetics; filled icons for active states.
- Never mix icon styles within the same product.

### Shapes & Decorative Elements
- **Organic shapes** (blobs, flowing curves) soften technical products.
- Subtle **gradients** add depth without clutter — use in hero sections only.
- Avoid borders where whitespace can separate elements instead.
- Neumorphism (soft shadows, raised elements): use sparingly for interactive components only.

---

## 7. COMPONENTS

### Navigation
- **Sticky header**: transparent on scroll-top, solid on scroll-down.
- Max 5–6 nav items. More than 6 = restructure your IA.
- CTA button in the header must **contrast visually** from nav links.
- Mobile: hamburger → full-screen overlay or slide-in panel (not a dropdown).
- Hide the header on scroll-down, reveal on scroll-up (Headroom.js pattern).

### Hero Section
- Single headline + single subheadline + single CTA.
- Headline should answer: *"What is this and why do I care?"* in under 10 words.
- CTA button: clear, verb-first label ("Get Started", "Book a Call", not "Learn More").
- Hero height: `100vh` or `80vh` — never shorter than `600px`.
- One product image or video — never a carousel in the hero.

### Buttons
```css
/* Primary CTA */
.btn-primary {
  background: var(--color-accent);
  color: white;
  padding: 12px 24px;
  border-radius: 6px;        /* subtle — not pill, not sharp */
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.15s ease;
}
.btn-primary:hover {
  opacity: 0.9;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

/* Secondary / Ghost */
.btn-secondary {
  background: transparent;
  border: 1px solid var(--color-gray-200);
  color: var(--color-gray-900);
}
```

### Cards
- Subtle border (`1px solid #E5E7EB`) or very light shadow (`0 1px 3px rgba(0,0,0,0.08)`).
- Internal padding: `24–32px`.
- Border radius: `8–16px` (rounder = friendlier; sharper = more technical).
- On hover: lift effect (`translateY(-2px)` + shadow increase).
- Never use cards when a simple list or prose would serve the user better.

### Forms
- One field per row — never two columns on mobile.
- Labels above inputs, always visible (never placeholder-only).
- Input height: `44px` minimum (touch-friendly).
- Inline validation — show errors on blur, not on submit.
- Submit button: full-width on mobile.

---

## 8. MOTION & MICRO-INTERACTIONS

Motion is the difference between a good site and a memorable one — but restraint is key.

### Principles
- **Purpose over decoration**: every animation must have a reason.
- **Speed**: UI transitions `150–250ms`; page entrances `300–500ms`. Never slower.
- **Easing**: use `ease-out` for entrances, `ease-in` for exits, `ease-in-out` for loops.
- Always respect `prefers-reduced-motion` — provide a no-motion fallback.

### High-Impact, Low-Effort Micro-Interactions
```css
/* Smooth page scrolling */
html { scroll-behavior: smooth; }

/* Fade-up on scroll (use Intersection Observer) */
.animate-on-scroll {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.5s ease, transform 0.5s ease;
}
.animate-on-scroll.visible {
  opacity: 1;
  transform: translateY(0);
}

/* Button hover lift */
.btn:hover {
  transform: translateY(-1px);
  transition: transform 0.15s ease;
}

/* Link underline grow */
a {
  text-decoration: none;
  background-image: linear-gradient(currentColor, currentColor);
  background-size: 0% 1px;
  background-position: 0 100%;
  transition: background-size 0.2s ease;
}
a:hover { background-size: 100% 1px; }
```

### Scroll-Triggered Effects (2025 Standard)
- Use **Intersection Observer API** — never scroll event listeners.
- Stagger entrance animations: `200ms` delay between sibling elements.
- Parallax: subtle (`0.2–0.3` speed ratio) or skip entirely — performance risk.
- Kinetic typography (text that animates on scroll) — powerful for hero sections.

---

## 9. PERFORMANCE (The Silent Killer of Beautiful Sites)

A slow minimalist site defeats its own purpose.

### Targets
- **LCP** (Largest Contentful Paint): < 2.5s
- **FID** (First Input Delay): < 100ms
- **CLS** (Cumulative Layout Shift): < 0.1
- **Page weight**: < 1MB total (HTML + CSS + JS + images)

### Non-Negotiables
- Images: use `WebP` or `AVIF` format. Always specify `width` and `height` attributes.
- Lazy-load all images below the fold: `loading="lazy"`.
- Self-host fonts or use `font-display: swap`.
- Inline critical CSS; defer non-critical CSS.
- Minify and bundle all JS. No unused libraries.
- Use a CDN for static assets.

---

## 10. RESPONSIVE & MOBILE-FIRST

- **Build mobile-first**, then scale up — not the reverse.
- 56.74% of global web traffic is mobile. Design for thumbs first.
- Touch targets: minimum `44×44px` (Apple HIG standard).
- Font sizes never below `16px` on mobile (prevents iOS zoom on input focus).
- Navigation must be usable with one thumb on a 375px screen.
- Test on real devices — emulators lie about font rendering.

### Breakpoints
```css
/* Mobile first */
/* Base: 0–639px */
@media (min-width: 640px)  { /* sm: tablet portrait */ }
@media (min-width: 768px)  { /* md: tablet landscape */ }
@media (min-width: 1024px) { /* lg: small desktop */ }
@media (min-width: 1280px) { /* xl: desktop */ }
@media (min-width: 1536px) { /* 2xl: large desktop */ }
```

---

## 11. ACCESSIBILITY (Non-Negotiable)

- **Color contrast**: 4.5:1 for body text; 3:1 for large text (18px+).
- All images must have descriptive `alt` text.
- Focus states must be visible — never `outline: none` without a custom replacement.
- Form fields require `<label>` elements — never placeholder-as-label.
- Keyboard navigation must work for all interactive elements.
- Use semantic HTML: `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.
- `aria-label` on icon-only buttons.
- Test with screen reader (VoiceOver or NVDA).

---

## 12. DARK MODE

```css
:root {
  --bg-primary:   #FFFFFF;
  --bg-secondary: #F9FAFB;
  --text-primary: #111827;
  --text-muted:   #6B7280;
  --border:       #E5E7EB;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary:   #0A0A0A;
    --bg-secondary: #111111;
    --text-primary: #F9FAFB;
    --text-muted:   #9CA3AF;
    --border:       #1F2937;
  }
}
```

- Design both themes from day one — retrofitting dark mode is painful.
- Dark mode ≠ inverting colors. Re-evaluate every element independently.
- Accent color may need a lighter shade in dark mode for contrast.

---

## 13. COPY & CONTENT PRINCIPLES

Design without good copy fails. These rules apply to all text content:

- **Hero headline**: 6–10 words max. Benefit-first, not feature-first.
- **Subheadline**: 1–2 sentences. Expand on the headline's promise.
- **Body copy**: short paragraphs (3–4 lines max). Break up walls of text.
- **CTAs**: verb-first, specific ("Start Free Trial" > "Get Started" > "Learn More").
- **Microcopy**: error messages, form hints, and tooltips should be human and helpful.
- Remove adverbs and filler words. Every word pays rent.

---

## 14. DESIGN TOKENS (CSS Custom Properties)

Define these at the root of every project for consistency:

```css
:root {
  /* Spacing */
  --space-1: 4px;   --space-2: 8px;   --space-3: 12px;
  --space-4: 16px;  --space-5: 20px;  --space-6: 24px;
  --space-8: 32px;  --space-10: 40px; --space-12: 48px;
  --space-16: 64px; --space-20: 80px; --space-24: 96px;

  /* Border Radius */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
  --shadow-md: 0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.06);
  --shadow-lg: 0 10px 15px rgba(0,0,0,0.08), 0 4px 6px rgba(0,0,0,0.05);
  --shadow-xl: 0 20px 25px rgba(0,0,0,0.10), 0 10px 10px rgba(0,0,0,0.04);

  /* Transitions */
  --transition-fast:   150ms ease;
  --transition-base:   200ms ease;
  --transition-slow:   300ms ease;

  /* Z-Index Scale */
  --z-below:   -1;
  --z-base:     0;
  --z-raised:   10;
  --z-dropdown: 100;
  --z-sticky:   200;
  --z-modal:    300;
  --z-toast:    400;
}
```

---

## 15. COMMON MISTAKES TO AVOID

| ❌ Don't | ✅ Do Instead |
|---|---|
| Use 4+ fonts | Stick to 2 max |
| Carousel in the hero | Single static image or video |
| Full-width text columns | Max `72ch` line length |
| Placeholder-only form labels | Always use visible `<label>` |
| `outline: none` on focus | Custom visible focus styles |
| Overuse of shadows | Whitespace to separate elements |
| Animations > 500ms | Keep transitions under 300ms |
| Dark mode as afterthought | Build both from the start |
| 5+ nav items on mobile | Hamburger menu with max 6 items |
| Stock photography | Real, brand-aligned photography |
| Multiple primary CTAs | One primary CTA per section |
| Pure black text (#000) | Near-black (#111827) for warmth |

---

## 16. QUICK DECISION FRAMEWORK

When building any new component or section, ask:

1. **Does it serve the user's goal right now?** → If no, remove it.
2. **Is there whitespace around it?** → If not, add more.
3. **Can the message be communicated with fewer words?** → Rewrite it.
4. **Does it work on a 375px screen with one thumb?** → Test it.
5. **Does it pass 4.5:1 contrast?** → Check it.
6. **What happens without the animation?** → If it still works, simplify it.

---

*Last updated: March 2026. Sources: Awwwards, Figma, DigitalSilk, TodayMade, Stripe Design, Apple HIG, Linear, Elementor Blog.*
