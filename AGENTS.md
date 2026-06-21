# AGENTS.md — Ovasys Landing Page (AI_Build/Ovasys)

**See `../../Kelli Lewis/training-site/AGENTS.md` for the reference workflow.** This is a static landing page, so the test surface is lighter but the rules still apply.

---

## Project in one paragraph

Static HTML + CSS landing page for Ovasys (Ola's design company). `index.html` + `styles.css` + `Images/`. Written copy lives in `ovasys-landing-page.md`. The site is the **conversion machine** for Ovasys — a broken CTA or a dead link means lost revenue, not just an annoyance.

---

## Stack

- **Frontend:** Plain HTML + CSS. No JS framework, no build step.
- **Copy:** `ovasys-landing-page.md` is the source of truth for wording
- **Host:** [intended] Vercel or similar static host
- **Repo:** Git initialized (`.git/` present)

---

## The relevant "tests" for a static landing

Not everything needs Playwright. Landing pages need:

### 1. Link integrity
Every `<a href>` must resolve (internal) or 200 (external). Tool: `markdown-link-check` on the copy file + a Playwright crawl on the rendered HTML.

### 2. Copy parity with source-of-truth
The text on the page must match `ovasys-landing-page.md`. If copy changes, update the markdown first, then the HTML — never the reverse. A simple script can assert key phrases appear in both.

### 3. CTA wiring
Each CTA must trigger its intended action (mailto:, calendly link, contact form). One Playwright test per CTA.

### 4. Mobile & viewport
At least three viewport tests: 375px (mobile), 768px (tablet), 1440px (desktop). No horizontal scroll, no clipped CTAs.

### 5. Accessibility smoke
axe-core via `@axe-core/playwright`. Run once, fix the criticals, keep it passing.

### 6. Performance floor
Lighthouse CI or a simple `lhci autorun` — the page must hit Performance > 85, Accessibility > 90, Best Practices > 90. Regressions fail the build.

---

## Required files (to add)

```
AI_Build/Ovasys/
├── index.html
├── styles.css
├── Images/
├── ovasys-landing-page.md       (source of truth for copy)
├── copy-checklist.md            (must-have claims / disclaimers / positioning)
├── tests/
│   ├── smoke.spec.ts            (page loads, CTAs wired)
│   ├── links.spec.ts            (no dead links)
│   └── a11y.spec.ts             (axe-core)
├── playwright.config.ts
├── PRD.md                        (add one — inherits from Ovasys Strategic Review)
├── PLAN.md
├── REMEDIATION.md
└── AGENTS.md                     (this file)
```

---

## Commands

```bash
npm init -y
npm i -D @playwright/test @axe-core/playwright markdown-link-check
npx playwright install chromium

# Serve locally
npx http-server . -p 5500

# Run tests
npx playwright test

# Link-check the copy doc
npx markdown-link-check ovasys-landing-page.md
```

---

## The loop

1. Copy change? → edit `ovasys-landing-page.md` → run copy-checklist check → update HTML → run Playwright
2. Visual change? → `PLAN.md` → failing visual-regression test (if you add one) → CSS change → Playwright + screenshot review
3. New section? → update PRD → PLAN → tests → HTML

---

## Things to never do

- **Never** change body copy directly in `index.html` without updating `ovasys-landing-page.md` first
- **Never** ship with broken external links (LinkedIn, Calendly, email) — the landing page is the first impression
- Don't add JS frameworks to this page without a real reason — the static-HTML constraint is a feature
- Don't let the Lighthouse perf score slip below 85 — page weight matters on first-load

---

## What "done" looks like

- [ ] `PLAN.md` present for this change
- [ ] Copy matches `ovasys-landing-page.md`
- [ ] Playwright smoke + links + a11y all green
- [ ] Lighthouse scores within thresholds
- [ ] CTAs manually tested in a deployed preview

---

## Reference

Full workflow: `../../Kelli Lewis/training-site/AGENTS.md`
Project-wide playbook: `../../Ovasys/Agentic TDD Playbook.md`
Business context: `../../Ovasys/Ovasys Strategic Review — April 2026.md`
