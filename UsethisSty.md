# Ovasys Brand Style Guide
## Use this to match the Ovasys website aesthetic exactly

---

## Brand Identity

**Ovasys** is a digital agency for founders. The design language is minimal, technical, and infrastructure-feel — think Linear, Vercel, early Stripe. Dark background, tight type, surgical use of a single purple accent. No gradients on backgrounds, no rounded bubbly shapes, no bright colours. Everything feels like a tool built for serious people.

---

## Google Fonts to Load

Add these in the `<head>` before any CSS:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Glegoo:wght@400;700&family=Unbounded:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Geist+Mono:wght@400;500&display=swap" rel="stylesheet">
```

---

## CSS Variables (Design Tokens)

Paste this `:root` block at the top of your CSS:

```css
:root {
  /* Backgrounds */
  --color-bg:           #191919;
  --color-surface:      #1d1d1d;
  --color-surface-2:    #1f1f1f;
  --color-surface-3:    #242424;

  /* Borders */
  --color-border:       rgba(255, 255, 255, 0.13);
  --color-border-s:     rgba(255, 255, 255, 0.05);
  --color-border-xs:    rgba(255, 255, 255, 0.04);

  /* Text */
  --color-white:        #ffffff;
  --color-text:         rgba(255, 255, 255, 0.70);
  --color-text-muted:   rgba(255, 255, 255, 0.55);
  --color-text-faint:   rgba(255, 255, 255, 0.30);
  --color-text-ghost:   rgba(255, 255, 255, 0.20);
  --color-text-light:   #dadada;

  /* Accent — purple */
  --color-accent:       #BAA3FD;
  --color-accent-dim:   rgba(186, 163, 253, 0.12);
  --color-accent-hover: rgba(186, 163, 253, 0.80);

  /* Semantic aliases */
  --bg:         var(--color-bg);
  --surface:    var(--color-surface-2);
  --border:     var(--color-border);
  --border-s:   var(--color-border-s);
  --muted:      var(--color-text-muted);
  --text:       var(--color-text);
  --dadada:     var(--color-text-light);
  --white:      var(--color-white);
  --accent:     var(--color-accent);
  --accent-dim: var(--color-accent-dim);

  /* Fonts */
  --font-display: 'Glegoo', serif;
  --font-body:    'Unbounded', sans-serif;
  --font-mono:    'Geist Mono', 'Courier New', monospace;

  /* Type scale */
  --text-2xs:  10px;
  --text-xs:   11px;
  --text-sm:   13px;
  --text-base: 14px;
  --text-md:   15px;
  --text-lg:   16px;
  --text-xl:   18px;
  --text-2xl:  20px;
  --text-3xl:  24px;
  --text-4xl:  32px;
  --text-5xl:  40px;
  --text-6xl:  clamp(40px, 5vw, 60px);
  --text-7xl:  clamp(48px, 6vw, 72px);
  --text-8xl:  clamp(48px, 7vw, 90px);

  /* Layout */
  --max:  1280px;
  --pad:  clamp(24px, 6.25vw, 80px);
  --row:  clamp(80px, 10vw, 140px);

  /* Radius */
  --r-xs:   6px;
  --r-sm:   8px;
  --r:      16px;
  --r-lg:   24px;
  --r-xl:   32px;
  --r-pill: 999px;

  /* Shadows */
  --shadow-sm:  0 0 3.4px rgba(0, 0, 0, 0.25);
  --shadow-md:  0 0 5.6px rgba(0, 0, 0, 0.25), 0 2px 8px rgba(0, 0, 0, 0.15);
  --shadow-lg:  0 0 12px rgba(0, 0, 0, 0.3), 0 4px 24px rgba(0, 0, 0, 0.2);
  --shadow-inset-light:
    inset 1.4px 1.4px 0 rgba(255, 255, 255, 0.08),
    inset -1.4px -1.4px 0 rgba(255, 255, 255, 0.03);

  /* Easing */
  --ease-spring:   cubic-bezier(0.16, 1, 0.3, 1);
  --ease-out:      cubic-bezier(0.0, 0.0, 0.2, 1);
  --duration-fast: 150ms;
  --duration-base: 200ms;
  --duration-slow: 400ms;
}
```

---

## Base Reset & Body

```css
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
  font-size: var(--text-lg);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}

a { color: inherit; text-decoration: none; }
img, video { display: block; max-width: 100%; }
```

---

## Typography Patterns

### Headlines
Use **'Glegoo' serif** (`--font-display`) for all big headings. Tight letter-spacing, heavy weight.

```css
/* Hero / page title */
.hero-headline {
  font-family: var(--font-display);
  font-size: clamp(48px, 6vw, 72px);
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.06em;
  color: var(--white);
}

/* Section title */
.section-title {
  font-family: var(--font-display);
  font-size: clamp(40px, 5vw, 60px);
  font-weight: 700;
  line-height: 1.0;
  letter-spacing: -0.05em;
  color: var(--white);
}

/* Card / block headline */
.card-headline {
  font-family: var(--font-display);
  font-size: 32px;
  font-weight: 700;
  line-height: 1.0;
  letter-spacing: -0.04em;
  color: var(--white);
}
```

### Body Copy
Use **'Unbounded' sans-serif** (`--font-body`) at light weight (300) for body text. Wide tracking feels intentional.

```css
.body-copy {
  font-family: var(--font-body);
  font-size: clamp(13px, 1.35vw, 16px);
  font-weight: 300;
  line-height: 1.6;
  color: var(--dadada);
  letter-spacing: 0.02em;
}
```

### Mono / Eyebrow Labels
Use **'Geist Mono'** for small section labels and technical-feeling annotations.

```css
.eyebrow-mono {
  font-family: var(--font-mono);
  font-size: 16px;
  font-weight: 500;
  color: var(--accent);
  letter-spacing: -0.04em;
}
/* Prepend with: "--- " */
```

### Uppercase Label Tags

```css
.label {
  font-family: var(--font-body);
  font-size: 10px;
  font-weight: 400;
  letter-spacing: 0.10em;
  text-transform: uppercase;
  color: var(--accent);
}
```

---

## The Eyebrow Pattern

Before every section title, add a small "--- SECTION NAME" eyebrow line. This is a signature pattern.

**HTML:**
```html
<div class="eyebrow">
  <span class="label">What's Inside</span>
</div>
<h2 class="section-title">Your headline here</h2>
```

**CSS:**
```css
.eyebrow {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 16px;
}

.eyebrow::before {
  content: '---';
  font-family: var(--font-body);
  font-size: var(--text-sm);
  font-weight: 300;
  color: var(--accent);
  letter-spacing: 0.05em;
}

.eyebrow .label { color: var(--accent); }
```

---

## Layout

```css
/* Centered container — max 1280px, responsive horizontal padding */
.container {
  width: 100%;
  max-width: var(--max);
  margin: 0 auto;
  padding: 0 var(--pad);
}

/* Section rhythm — use padding-top/bottom: var(--row) */
.section {
  padding: var(--row) 0;
  border-top: 1px solid var(--color-border-s);
}
```

---

## Buttons

### Primary — White Fill (high emphasis CTA)
```css
.btn-primary {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  background: var(--color-white);
  color: var(--color-bg);
  padding: 14px 28px;
  border-radius: var(--r);
  font-family: var(--font-body);
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  border: none;
  cursor: pointer;
  transition: opacity 200ms, transform 150ms;
  white-space: nowrap;
}
.btn-primary:hover { opacity: 0.88; transform: translateY(-1px); }
```

**Use for:** main purchase/sign-up CTA.

### Ghost — Dark Pill (secondary action)
```css
.btn-ghost {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  background: linear-gradient(180deg, #353537 0%, #1f1e1e 100%);
  color: var(--white);
  padding: 10px 18px 10px 10px;
  border-radius: 10px;
  font-family: var(--font-body);
  font-size: 14px;
  font-weight: 400;
  text-decoration: none;
  border: none;
  cursor: pointer;
  box-shadow:
    0 0 5.6px rgba(0,0,0,0.25),
    inset 1.4px 1.4px 0 rgba(255,255,255,0.08),
    inset -1.4px -1.4px 0 rgba(255,255,255,0.03);
  transition: opacity 200ms, transform 150ms;
}
.btn-ghost:hover { opacity: 0.85; transform: translateY(-1px); }
```

### Text Link — Accent with arrow
```css
.btn-text {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: var(--accent);
  font-family: var(--font-body);
  font-size: 13px;
  font-weight: 400;
  text-decoration: none;
  transition: gap 200ms, opacity 200ms;
}
.btn-text:hover { gap: 12px; opacity: 0.8; }
```

---

## Cards

### Bordered Card — standard content card
```css
.card-bordered {
  background: transparent;
  border: 1px solid var(--color-border);
  border-radius: var(--r);
  padding: 32px 28px;
}
```

### Subtle Dark Card — lower contrast
```css
.card-subtle {
  background: var(--color-surface); /* #1d1d1d */
  border: 1.1px solid var(--color-border-xs);
  border-radius: 14px;
  overflow: hidden;
}
```

### Card with Hover Accent Bar (bottom purple line on hover)
```css
.card-accent-bar {
  position: relative;
  overflow: hidden;
  border: 1px solid var(--color-border);
  border-radius: var(--r);
}
.card-accent-bar::after {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 2px;
  background: var(--color-accent);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 400ms cubic-bezier(0.16, 1, 0.3, 1);
}
.card-accent-bar:hover::after { transform: scaleX(1); }
```

### Card Header Bar (dark top strip, like a browser chrome)
```css
.card-header-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  background: var(--color-bg);
  border-bottom: 1.1px solid var(--color-border-xs);
  padding: 10px 14px;
  height: 42px;
}
```

---

## Badges & Tags

```css
/* Pill badge — outlined */
.badge {
  display: inline-flex;
  align-items: center;
  height: 24px;
  padding: 0 10px;
  border-radius: 999px;
  font-family: var(--font-body);
  font-size: 10px;
  font-weight: 400;
  letter-spacing: 0.10em;
  text-transform: uppercase;
  border: 1px solid var(--color-border);
  color: var(--color-text-muted);
}

/* Accent tint badge */
.badge-accent {
  background: var(--color-accent-dim);
  border-color: transparent;
  color: var(--color-accent);
}
```

---

## Blockquote / Pullquote

The accent left-border quote is used throughout the site for testimonials and callout lines.

```css
.blockquote {
  font-family: var(--font-body);
  font-size: 13px;
  font-weight: 300;
  color: var(--color-text-muted);
  letter-spacing: 0.03em;
  padding-left: 16px;
  border-left: 2px solid var(--color-accent);
  line-height: 1.6;
}
```

---

## Feature / Benefit List Items

Accent dot bullet, light text:

```css
.feature-list { list-style: none; }

.feature-list li {
  font-family: var(--font-body);
  font-size: 13px;
  font-weight: 300;
  color: var(--text);
  padding: 10px 0;
  border-bottom: 1px solid var(--color-border);
  display: flex;
  align-items: center;
  gap: 10px;
  line-height: 1.4;
}

.feature-list li::before {
  content: '';
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: var(--color-accent);
  flex-shrink: 0;
}
```

---

## Dividers

```css
.divider   { width: 100%; height: 1px; background: var(--color-border); }
.divider-s { width: 100%; height: 1px; background: var(--color-border-s); }
```

---

## Scroll Fade-In Animation

Add `.fi` to any element. JavaScript below triggers `.on` when element enters viewport.

```css
.fi {
  opacity: 0;
  transform: translateY(24px);
  transition:
    opacity 750ms cubic-bezier(0.16, 1, 0.3, 1),
    transform 750ms cubic-bezier(0.16, 1, 0.3, 1);
}
.fi.on { opacity: 1; transform: none; }

/* Stagger children — add .fi-group to parent */
.fi-group > *:nth-child(1) { transition-delay: 0ms; }
.fi-group > *:nth-child(2) { transition-delay: 80ms; }
.fi-group > *:nth-child(3) { transition-delay: 160ms; }
.fi-group > *:nth-child(4) { transition-delay: 240ms; }
.fi-group > *:nth-child(5) { transition-delay: 320ms; }
.fi-group > *:nth-child(6) { transition-delay: 400ms; }
```

```js
// Paste before </body>
const obs = new IntersectionObserver(
  entries => entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('on'); obs.unobserve(e.target); } }),
  { threshold: 0.12 }
);
document.querySelectorAll('.fi').forEach(el => obs.observe(el));
```

---

## Hover Utilities

```css
.hover-lift {
  transition: opacity 200ms, transform 150ms;
}
.hover-lift:hover { opacity: 0.85; transform: translateY(-1px); }

.hover-fade {
  transition: opacity 200ms;
}
.hover-fade:hover { opacity: 0.75; }
```

---

## Colour Usage Rules

| Use case | Value |
|---|---|
| Page background | `#191919` |
| Card / surface background | `#1d1d1d` |
| Card hover state | `rgba(255,255,255,0.03)` |
| Primary headline | `#ffffff` |
| Body / paragraph text | `rgba(255,255,255,0.70)` |
| Muted / secondary text | `rgba(255,255,255,0.55)` |
| Faint / placeholder text | `rgba(255,255,255,0.30)` |
| Accent (purple) | `#BAA3FD` |
| Accent tint fill | `rgba(186, 163, 253, 0.12)` |
| Standard border | `rgba(255,255,255,0.13)` |
| Subtle border | `rgba(255,255,255,0.05)` |

**Accent `#BAA3FD` is used on:**
- Eyebrow label text and `---` dashes
- Accent left-border on blockquotes
- Feature list bullet dots
- `.btn-text` colour
- Badge tint background/text
- Hover states on bordered cards

---

## Typography Rules

| Element | Font | Weight | Notes |
|---|---|---|---|
| Hero headline | Glegoo | 700 | letter-spacing: -0.06em |
| Section title | Glegoo | 700 | letter-spacing: -0.05em |
| Card headline | Glegoo | 700 | letter-spacing: -0.04em |
| Subheading | Unbounded | 600 | letter-spacing: -0.03em |
| Body paragraph | Unbounded | 300 | letter-spacing: 0.02em |
| Labels / meta | Unbounded | 300–400 | letter-spacing: 0.01em |
| Eyebrow tag | Unbounded | 400 | UPPERCASE, tracking: 0.10em |
| Mono label | Geist Mono | 500 | letter-spacing: -0.04em |

---

## Design Principles (follow these)

1. **Dark, not flashy.** The background is near-black `#191919`. No colourful backgrounds, no light mode.
2. **One accent colour only.** `#BAA3FD` purple. Never add secondary accent colours.
3. **Glegoo for display, Unbounded for everything else.** Mixing them is intentional — the serif headlines contrast against the tight geometric sans.
4. **Tight letter-spacing on headlines.** `-0.04em` to `-0.06em`. Headlines should feel compressed and confident.
5. **Light weight body copy.** `font-weight: 300` on most paragraph text. Feels precise, not heavy.
6. **Borders not backgrounds.** Cards prefer a subtle `1px solid rgba(255,255,255,0.13)` border over a solid background fill.
7. **Minimal hover states.** `opacity: 0.85` + `translateY(-1px)` is the standard hover. Don't add colour flashes or scale effects.
8. **No decorative elements.** No gradients on sections, no blobs, no icons unless they serve a function.
9. **The `---` dash pattern.** Every section eyebrow uses three hyphens (`---`) followed by the label. Keep this consistent.
10. **Spacing is generous.** Section padding uses `clamp(80px, 10vw, 140px)`. Let content breathe.

---

## Minimal Boilerplate

Use this as your HTML starting point:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Glegoo:wght@400;700&family=Unbounded:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Geist+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    /* Paste :root tokens and base reset here */
  </style>
</head>
<body>

  <!-- Your page content -->

  <script>
    // Scroll fade-in
    const obs = new IntersectionObserver(
      entries => entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('on'); obs.unobserve(e.target); } }),
      { threshold: 0.12 }
    );
    document.querySelectorAll('.fi').forEach(el => obs.observe(el));
  </script>
</body>
</html>
```

---

## Common Section Pattern

Every content section follows this pattern:

```html
<section style="padding: var(--row) 0; border-top: 1px solid var(--color-border-s);">
  <div class="container">

    <!-- Eyebrow -->
    <div class="eyebrow" style="margin-bottom: 16px;">
      <span class="label">Section Name</span>
    </div>

    <!-- Title -->
    <h2 class="section-title" style="margin-bottom: 48px;">
      Your headline
    </h2>

    <!-- Content -->

  </div>
</section>
```

---

---

## Light Mode — Blog / Ebook Pages

The blog and any ebook/content pages use **light mode** while keeping the exact same typographic DNA — same fonts, same `---` eyebrow pattern, same purple accent, same tight tracking. Only the colour palette inverts.

The reference feel is: clean editorial, like a well-designed publication. Think Linear docs light mode or Stripe's editorial pages.

### Light Mode Color Tokens

Add these overrides to your page (either in a `.light` wrapper class or directly on `body` for a fully light page):

```css
body.light-mode,
.light-mode {
  /* Backgrounds */
  --color-bg:           #F7F7F5;   /* warm off-white, not pure white */
  --color-surface:      #FFFFFF;
  --color-surface-2:    #F0F0EE;
  --color-surface-3:    #E8E8E5;

  /* Borders */
  --color-border:       rgba(0, 0, 0, 0.10);
  --color-border-s:     rgba(0, 0, 0, 0.06);
  --color-border-xs:    rgba(0, 0, 0, 0.04);

  /* Text */
  --color-white:        #111111;   /* inverted — use for headings */
  --color-text:         rgba(0, 0, 0, 0.72);
  --color-text-muted:   rgba(0, 0, 0, 0.50);
  --color-text-faint:   rgba(0, 0, 0, 0.30);
  --color-text-ghost:   rgba(0, 0, 0, 0.15);
  --color-text-light:   #333333;

  /* Accent — keep the same purple, slightly deeper */
  --color-accent:       #7C5CFC;
  --color-accent-dim:   rgba(124, 92, 252, 0.10);
  --color-accent-hover: rgba(124, 92, 252, 0.80);

  /* Semantic aliases */
  --bg:         var(--color-bg);
  --surface:    var(--color-surface);
  --border:     var(--color-border);
  --border-s:   var(--color-border-s);
  --muted:      var(--color-text-muted);
  --text:       var(--color-text);
  --dadada:     var(--color-text-light);
  --white:      var(--color-white);
  --accent:     var(--color-accent);
  --accent-dim: var(--color-accent-dim);
}
```

> **Why `#7C5CFC` instead of `#BAA3FD`?** The light background makes the original pastel purple too faint to read. This deeper value keeps the same hue but has enough contrast on white.

### Light Mode Body

```css
body.light-mode {
  background: var(--bg);       /* #F7F7F5 */
  color: var(--text);          /* rgba(0,0,0,0.72) */
  font-family: var(--font-body);
  font-size: var(--text-lg);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}
```

### Light Mode Nav / Header

```css
nav.light {
  background: rgba(247, 247, 245, 0.92);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(0, 0, 0, 0.06);
}
```

### Light Mode Buttons

**Primary CTA — dark fill (inverted from dark mode):**
```css
.light-mode .btn-primary {
  background: #111111;
  color: #ffffff;
}
.light-mode .btn-primary:hover { opacity: 0.85; transform: translateY(-1px); }
```

**Ghost — light pill:**
```css
.light-mode .btn-ghost {
  background: linear-gradient(180deg, #ffffff 0%, #f0f0ee 100%);
  color: #111111;
  box-shadow:
    0 0 5.6px rgba(0,0,0,0.08),
    inset 1.4px 1.4px 0 rgba(255,255,255,0.90),
    inset -1.4px -1.4px 0 rgba(0,0,0,0.04);
}
```

**Accent text link — unchanged, accent colour is still purple:**
```css
.light-mode .btn-text {
  color: var(--accent); /* #7C5CFC */
}
```

### Light Mode Cards

```css
/* Standard card — white fill with soft border */
.light-mode .card-bordered {
  background: #ffffff;
  border: 1px solid rgba(0, 0, 0, 0.10);
  border-radius: var(--r);
  padding: 32px 28px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.06);
}

/* Subtle card — slightly off-white */
.light-mode .card-subtle {
  background: #F0F0EE;
  border: 1.1px solid rgba(0,0,0,0.06);
  border-radius: 14px;
}

/* Hover state */
.light-mode .card-hover:hover {
  background: rgba(0, 0, 0, 0.02);
}

/* Accent bar — same purple underline on hover */
.light-mode .card-accent-bar::after {
  background: var(--accent);
}
```

### Light Mode Card Header Bar

```css
.light-mode .card-header-bar {
  background: #F0F0EE;
  border-bottom: 1.1px solid rgba(0,0,0,0.06);
}
```

### Light Mode Blockquote

```css
.light-mode .blockquote {
  color: rgba(0, 0, 0, 0.55);
  border-left: 2px solid var(--accent);
}
```

### Light Mode Feature List

```css
.light-mode .feature-list li {
  color: rgba(0, 0, 0, 0.72);
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
}

.light-mode .feature-list li::before {
  background: var(--accent); /* purple dot */
}
```

### Light Mode Dividers

```css
.light-mode .divider   { background: rgba(0, 0, 0, 0.10); }
.light-mode .divider-s { background: rgba(0, 0, 0, 0.06); }
```

### Light Mode Badges

```css
.light-mode .badge {
  border-color: rgba(0, 0, 0, 0.12);
  color: rgba(0, 0, 0, 0.55);
}

.light-mode .badge-accent {
  background: var(--color-accent-dim);
  border-color: transparent;
  color: var(--accent);
}
```

### Light Mode Blog Post Cards

The blog card pattern — dark header bar with light body — inverts like this:

```css
/* Post card wrapper */
.light-mode .blog-post {
  background: #ffffff;
  border: 1.1px solid rgba(0,0,0,0.08);
  border-radius: 14px;
}

.light-mode .blog-post:hover {
  border-color: rgba(0,0,0,0.18);
}

/* Header bar */
.light-mode .blog-post-head {
  background: #F0F0EE;
  border-bottom: 1.1px solid rgba(0,0,0,0.06);
}

/* Meta text */
.light-mode .blog-post-meta { color: #888888; }
.light-mode .blog-post-ep   { color: #888888; }
.light-mode .blog-post-title-text { color: #111111; }

/* Excerpt */
.light-mode .blog-post-excerpt {
  color: #333333;
}
```

### Light Mode Section Pattern

```html
<section class="light-mode" style="padding: var(--row) 0; border-top: 1px solid rgba(0,0,0,0.06);">
  <div class="container">

    <div class="eyebrow" style="margin-bottom: 16px;">
      <span class="label">Section Name</span>
    </div>

    <h2 style="
      font-family: 'Glegoo', serif;
      font-size: clamp(40px, 5vw, 60px);
      font-weight: 700;
      color: #111111;
      letter-spacing: -0.05em;
      line-height: 1.0;
      margin-bottom: 48px;
    ">Your headline</h2>

    <!-- Content -->

  </div>
</section>
```

### Light Mode Colour Reference Table

| Use case | Value |
|---|---|
| Page background | `#F7F7F5` |
| Card / surface | `#FFFFFF` |
| Elevated surface | `#F0F0EE` |
| Primary headline | `#111111` |
| Body text | `rgba(0,0,0,0.72)` |
| Muted / secondary | `rgba(0,0,0,0.50)` |
| Faint / placeholder | `rgba(0,0,0,0.30)` |
| Accent (purple) | `#7C5CFC` |
| Accent tint fill | `rgba(124, 92, 252, 0.10)` |
| Standard border | `rgba(0,0,0,0.10)` |
| Subtle border | `rgba(0,0,0,0.06)` |

### What Stays the Same in Light Mode

These elements do **not** change — they are brand constants:

- All three fonts: **Glegoo, Unbounded, Geist Mono**
- The `---` eyebrow dash pattern
- Tight letter-spacing on all headlines (`-0.04em` to `-0.06em`)
- Light `font-weight: 300` on body copy
- Spacing scale and section rhythm (`--row`, `--pad`, `--max`)
- Radius values (`--r`, `--r-sm`, `--r-lg`, `--r-pill`)
- The accent-bar card hover animation (purple underline sweeps left to right)
- Scroll fade-in animation (`.fi` / `.fi.on`)
- Button shapes and padding
- The `.container` max-width and padding pattern

---

*This style guide is derived from the live Ovasys website codebase. Match these tokens and patterns exactly to stay on-brand.*
