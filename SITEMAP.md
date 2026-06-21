# Ovasys — Site Map & Copy Document

> **How to use this file:**
> Edit any copy, section status, or structure here. Then tell Claude to "rebuild from SITEMAP.md" and it will update the HTML to match. Sections marked `[ PLANNED ]` have copy ready but are not yet built. Sections marked `[ BUILT ]` are live in the HTML.

---

## SITE OVERVIEW

```
ovasys.co
├── index.html          ← Home / Landing Page
│   ├── /nav            → links to: services.html (planned), mailto:hello@ovasys.co
│   ├── /hero
│   ├── /hero-image
│   ├── /blog
│   ├── /quick-preview  → links to: takesbyovasys.substack.com
│   ├── /what-we-do     [ PLANNED ]
│   ├── /packages       [ PLANNED ]
│   ├── /who-its-for    [ PLANNED ]
│   ├── /process        [ PLANNED ]
│   ├── /final-cta      [ PLANNED ]
│   └── /footer         → links to: mailto:hello@ovasys.co, takesbyovasys.substack.com
│
└── services.html       ← What We Offer / Services Page
    ├── /nav            → links to: index.html, mailto:workwith@ovasys.co
    ├── /svc-hero
    ├── /positioning
    ├── /case-study     → internal anchor: #case-study
    ├── /pricing        → links to: mailto:workwith@ovasys.co
    ├── /testimonial    → links to: mailto:workwith@ovasys.co
    ├── /close          → links to: index.html, mailto:workwith@ovasys.co
    └── /footer         → links to: mailto:workwith@ovasys.co, takesbyovasys.substack.com
```

**Contact emails:**
- Home page (index.html): `hello@ovasys.co`
- Services page (services.html): `workwith@ovasys.co`

**External links:**
- Newsletter / Blog: `https://takesbyovasys.substack.com`

---

---

# PAGE 1 — index.html (Home)

**`<title>`:** Ovasys — Digital Foundation for Serious Founders
**`<meta description>`:** We work with experienced founders to design high-converting landing pages, build core infrastructure, and deploy AI workflows that grow your business.

---

## [ BUILT ] NAV

| Element          | Content                        |
|------------------|--------------------------------|
| Logo             | `Images/Logo/SVGs/L_White.svg` |
| Contact label    | Contact                        |
| Contact email    | @ hello@ovasys.co              |
| Email href       | mailto:hello@ovasys.co         |

---

## [ BUILT ] HERO — `#hero`

**Headline:**
```
Launch fast.
Look credible.
Scale with AI.
```
- "Launch fast." — accent color (purple `#BAA3FD`)
- "Look credible." — white
- "Scale with AI." — ghost/muted

**Subheadline:**
```
We work with experienced founders to design high-converting landing pages,
build core infrastructure, and deploy AI workflows that grow your business.
```

**CTA Button:**
- Style: dark pill button
- Label: `Contact:`
- Email: `hello@ovasys.co`
- href: `mailto:hello@ovasys.co`

---

## [ BUILT ] HERO IMAGE — `#hero-image`

Three project mockup images displayed side by side:

| Position | File                              | Alt text        |
|----------|-----------------------------------|-----------------|
| Left     | `Images/HeroImages/HRI_Mavlon.png`  | Mavlon project  |
| Center   | `Images/HeroImages/HRI_Truck.png`   | Truck project   |
| Right    | `Images/HeroImages/HRI_Revwit.png`  | Revwit project  |

---

## [ BUILT ] BLOG CAROUSEL — `#blog`

**Section Header:**

| Element       | Content                                                                                                                                       |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Title         | Follow Our Blog                                                                                                                               |
| Description   | When are we not building solutions for you, we are creating content to help founders, designers, PMs, and developers save time, cut costs, and build better with AI. |
| CTA button    | View in Substack                                                                                                                              |
| CTA href      | https://takesbyovasys.substack.com                                                                                                            |
| CTA icon      | `Images/Icons/Icon_Subtext.png`                                                                                                               |

**Carousel images** (auto-scroll, looping):

| File                                      | Alt              |
|-------------------------------------------|------------------|
| `Images/BlogCarousel/tbo_carousel_01.png` | TBO Episode 1    |
| `Images/BlogCarousel/tbo_carousel_02.png` | TBO Episode 2    |
| `Images/BlogCarousel/tbo_carousel_03.png` | TBO Episode 3    |
| `Images/BlogCarousel/tbo_carousel_04.png` | TBO Episode 4    |
| `Images/BlogCarousel/tbo_carousel_05.png` | TBO Episode 5    |
| `Images/BlogCarousel/tbo_carousel_06.png` | TBO Episode 6    |
| `Images/BlogCarousel/tbo_carousel_07.png` | TBO Episode 7    |

---

## [ BUILT ] QUICK PREVIEW BLOG — `#quick-preview`

**Eyebrow label:** `--- Quick Preview`

**Blog Posts** (each links to `https://takesbyovasys.substack.com`):

### Post 1
- Episode: `EP 18:`
- Title: `Claude Code to Figma and why it matters`
- Excerpt: To further highlight the consistent misinterpretation of possibilities and reality, I want to zoom in on a recent feature: Cloud Code to Figma by Anthropic.
- Views: 49 Views
- Published: Sep 26

### Post 2
- Episode: `EP 16:`
- Title: `AI Adoption and the Actual Reality`
- Excerpt: All these matter because there's a truckload of information out there about AI and without context of who is writing it and what the agenda is, the conclusions drawn can easily be "Panic or Doom" which isn't always helpful.
- Views: 61 Views
- Published: Feb 25

### Post 3
- Episode: `EP 07:`
- Title: `Faster Doesn't Always Mean Better. But it can`
- Excerpt: AI dictation lets you create briefs faster without losing your authentic voice and content context. Dictation saves at least 2+ hours daily. AI transcription can keep your tone intact. Voice notes can become structured briefs in minutes.
- Views: 49 Views
- Published: Sep 26

### Post 4
- Episode: `EP 01:`
- Title: `All Founders are Designers. Fight Me.`
- Excerpt: ... too many teams don't realize it. They think "design" starts when it's time to hire someone to polish an MVP. That's like calling an architect only after you've poured the foundation. Now add AI into the mix.
- Views: 24 Views
- Published: Sep 26

**Read More CTA:**
- Style: dark pill button
- Text: Read more →
- Icon: `Images/Icons/Icon_Subtext.png`
- href: `https://takesbyovasys.substack.com`

---

## [ BUILT ] WHAT WE OFFER — `#what-we-offer`

**Section eyebrow:** `--- What We Offer`
**Section headline:** We build tools that **accelerate your business operations.**
- "We build tools that" — white
- "accelerate your business operations." — accent (purple)

**Three service cards:**

| Card | Description | Features |
|------|-------------|----------|
| Standard | Save time & remove blockers on internal knowledge sharing. | Learning Management system · Built for how you train employees · E-commerce automation support |
| Promote | Cut down content review time, promote business more. | Content review tool · Built for how you drive engagement · Marketing automation support |
| Custom | Suitable for creating a solution for customers to improve retention. | Audit highest cost operational gap · Build custom business tool · For Internal or Client Facing tool |

**Mockup row:** Uses `HRI_Mavlon.png`, `HRI_Truck.png`, `HRI_Revwit.png`

**Case study teaser banner:**
- Eyebrow: `→ Case Study · Kelliworks Financial Services`
- Headline: We cut a firm's weekly operational load from 10 hours to 1 — with 4 custom AI systems in one month.
- CTA: `Read proposal →` → `services.html`

---

## [ PLANNED ] PACKAGES — `#packages`

**Section eyebrow:** How We Work
**Section title:** Pick your starting point.

### Package 01 — Scale
- Tagline: AI Systems
- For: Businesses optimising operations
- Includes:
  - Standard: Tool for Onboarding & Marketing 
  - Custom: Tool Built for business operations
- CTA: "Discuss AI Systems" → `mailto:workwith@ovasys.co`

### Package 02 — Launch
- Tagline: Foundation
- For: Founders who need to go live properly
- Includes:
  - Landing page design
  - Domain setup
  - Email infrastructure
- CTA: "Start with Launch" → `mailto:workwith@ovasys.co`

### Package 03 — Promote
- Tagline: Growth
- For: Founders ready to push distribution
- Includes:
  - Promotional Storyboard design
  - Motion graphics & promotional videos
- CTA: "Start with Promote" → `mailto:workwith@ovasys.co`


---

## [ PLANNED ] WHO THIS IS FOR — `#who-its-for`

**Section eyebrow:** Who We Work With
**Section title:** The foundation most founders need.

**We work best with:**
- Second-time founders
- Industry operators launching new ventures
- Teams that already know their market

**We're not a fit for:**
- Idea-stage founders without validation
- Long exploratory engagements

**Microcopy:** "We've seen what slows founders down. We remove it."

---

## [ BUILT ] WHY CHOOSE US — `#why-choose-us`

**Section eyebrow:** `--- Why Choose Us`
**Headline (left):** 5+ Years helping businesses launch & promote product.
**Body (right):** Our experience building software products, websites, and business campaigns led us to focus on crafting custom software solutions that now help them keep and serve those leads better.

**Client chips:** Insite · Dabo · DriveMe · SMB Hive · Justinvate · Mavlon Tours · IgnitaTunes · High N Dry · Renaissance · Nashville · All Clear Glass · Role Vendor · Lasheveal

---

## [ PLANNED ] PROCESS — `#process`

**Section eyebrow:** How It Works
**Section title:** We don't do endless revisions. We ship.

**Steps:**
1. Reach out
2. We assess fit
3. We build + deploy
4. You launch

---

## [ PLANNED ] FINAL CTA — `#final-cta`

**Headline:** Ready to launch properly?
**Body:** Send a short note about your business and what you're building.
**Primary CTA:** "Start a project" → `mailto:workwith@ovasys.co`
**Secondary CTA:** "Or read our thinking first" → `https://takesbyovasys.substack.com`

---

## [ BUILT ] FOOTER — `<footer>`

| Element            | Content                                |
|--------------------|----------------------------------------|
| Headline           | Get in touch now...                    |
| Logomark           | `Images/logoIcon_Footer.svg`           |
| Email icon href    | mailto:hello@ovasys.co                 |
| Substack icon href | https://takesbyovasys.substack.com     |
| Email display      | hello@ovasys.co                        |
| CTA button         | Let's talk → mailto:hello@ovasys.co   |
| Copyright          | © 2026 — Copyright                     |

---

---

# PAGE 2 — services.html (What We Offer)

**`<title>`:** What We Offer — Ovasys
**`<meta description>`:** Ovasys builds AI automations, systems, and tools that remove friction from your day-to-day operations. See how we work and what it costs.

---

## [ BUILT ] NAV

| Element          | Content                         |
|------------------|---------------------------------|
| Logo             | `Images/Logo/SVGs/L_White.svg`  |
| Logo href        | index.html                      |
| Contact label    | Contact                         |
| Contact email    | @ workwith@ovasys.co            |
| Email href       | mailto:workwith@ovasys.co       |

---

## [ BUILT ] HERO — `#svc-hero`

**Eyebrow label:** What We Offer

**Headline:**
```
Optimise business
operations with
custom AI tools.
```
- "Optimise business" — white
- "operations" — accent color (purple `#BAA3FD`)
- "with" — white
- "custom AI tools." — ghost/muted

**Subheadline:**
```
We work with established businesses and founders who are generating revenue
— but losing time to manual processes, disconnected workflows, and operations
that still depend on the wrong people doing the wrong things.
```

**CTAs:**
- Primary: dark pill — "Start a project: workwith@ovasys.co" → `mailto:workwith@ovasys.co`
- Secondary: text link — "or see how we work →" → `#case-study`

---

## [ BUILT ] POSITIONING — `#positioning`

**Eyebrow:** What We Do
**Headline:**
```
An implementation partner.
Not an agency.
```
- "Not an agency." in muted color

**Subheadline:**
```
We don't audit and disappear. We build automations, systems, and tools that
remove friction from your day-to-day and give you back the hours your business
is quietly bleeding.
```

**We're NOT:**
- A branding agency
- A generic digital marketing firm
- Consultants who audit and write reports
- A team that disappears after handoff

**We ARE:**
- An implementation partner — the team you call when your business works and you need the infrastructure to prove it
- Builders of automations, systems, and custom AI tools
- Operators who ship — not strategists who theorise
- One engagement. Measurable reduction in weekly operational load.

---

## [ BUILT ] CASE STUDY — `#case-study`

**Eyebrow:** How We Do It
**Headline:**
```
Real work.
Real outcomes.
```

**Client block:**
- Tag: Case Study
- Client name: Kelliworks Financial Services
- Description: A Florida-based financial services firm generating consistent revenue — but bleeding hours every week to manual onboarding, fragmented intake processes, and a marketing workflow with no single owner. The CEO was personally involved in tasks that had no business requiring their attention.

**The Problems:**

| # | Problem |
|---|---------|
| 1 | **New hires took weeks to onboard.** Every one required 1–2 hours of the CEO's time, repeatedly. |
| 2 | **Client intake was a manual time sink.** Contracts, CRM updates, and calendar booking took an hour of staff time per client — every time. |
| 3 | **Marketing approvals were scattered across three platforms** with no clear owner and no unified workflow. |
| 4 | **Potential clients needed a full sales engagement** before receiving any financial insight — delaying the relationship from the start. |

**What We Built:**

| What we built | Problem solved | Result attained |
|---------------|----------------|-----------------|
| Training LMS | Self-directed onboarding | Zero recurring CEO time |
| Sales Automation | Full client intake — contracts, CRM, calendar | Instant, zero-touch for all staff |
| Content Approval Tool | All reviews in one interface | Live feedback. No coordination overhead. |
| Bank Statement Analyser | Immediate financial insight for prospects | Delivered at first client contact |

**Metrics:**

| Metric | Value | Description |
|--------|-------|-------------|
| Milestone | 4 Systems | Built and deployed in 1 month |
| Weekly Operational Load | 10hrs → 1hr | Reduced from 10 hours to 1 hour per week |

**Mid-page CTA:**
- Text: "Your business has the same gaps. We can close them."
- Button: dark pill — "Start a project: workwith@ovasys.co" → `mailto:workwith@ovasys.co`

---

## [ BUILT ] PRICING — `#pricing`

**Eyebrow:** The Offer
**Headline:** What you can get.

**Intro:**
- Pain headline: "Your time is the most expensive resource in your business."
- Pain body: Every hour spent on intake, onboarding, approvals, and repetitive coordination is an hour you're not spending on clients, strategy, or growth. We fix the operational gaps that are quietly costing you the most.

**Pricing Cards:**

### Standard — Most Popular
- Price: $800
- Sub: 1 engagement · 2 systems · full deployment
- Includes:
  - Employee Onboarding & Training LMS
  - Content Workflow Automation
  - 1 engagement. 2 systems. All for your firm.
- CTA: "Start with Standard →" → `mailto:workwith@ovasys.co?subject=Standard%20Package%20Enquiry`

### Custom Solution
- Price: $1,250
- Sub: Bespoke build · internal or client-facing
- Includes:
  - Identify your highest-cost operational gap
  - Build the tool that closes it
  - For internal operations or client-facing tools
- CTA: "Discuss Custom →" → `mailto:workwith@ovasys.co?subject=Custom%20Solution%20Enquiry`

**Footer note:** All engagements are scoped before any work begins. No surprises.

---

## [ BUILT ] TESTIMONIAL — `#testimonial`

| Element      | Content                                         |
|--------------|-------------------------------------------------|
| Tag          | Testimonial                                     |
| Quote        | "This is exactly the support I'm looking for. Great value add." |
| Attribution  | Founder, KelliWorks                             |
| Location     | Florida, USA                                    |
| CTA button   | "Start a project" → `mailto:workwith@ovasys.co` |
| Sub-note     | We typically respond within 24 hours.           |

---

## [ BUILT ] FINAL CTA — `#close`

**Headline:**
```
Let's fix your
operations.
```

**Body:** Send a short note about your business and what's slowing you down. We'll tell you if we're a fit.

**CTAs:**
- Primary: "Start a project" → `mailto:workwith@ovasys.co`
- Secondary: "← Back to home" → `index.html`

---

## [ BUILT ] FOOTER — `<footer>`

| Element            | Content                                    |
|--------------------|--------------------------------------------|
| Headline           | Get in touch now...                        |
| Logomark           | `Images/logoIcon_Footer.svg`               |
| Email icon href    | mailto:workwith@ovasys.co                  |
| Substack icon href | https://takesbyovasys.substack.com         |
| Email display      | workwith@ovasys.co                         |
| CTA button         | Let's talk → mailto:workwith@ovasys.co    |
| Copyright          | © 2026 — Copyright                         |

---

---

# MICROCOPY BANK

These are approved one-liners available to use anywhere on the site (headlines, labels, captions, hover states).

```
"Built for founders who move fast"
"We don't do endless revisions. We ship."
"Clarity over complexity"
"Small team. High leverage."
"Your stack, sorted."
"Speed is the strategy."
"Not an agency. A system."
"From blank to launched — properly."
"The foundation most founders skip."
"One team. Design, distribution, and AI."
"We handle the infrastructure. You focus on the business."
"We've seen what slows founders down. We remove it."
```

**Progression framing:**
```
Launch → Promote → Scale
Go live. Get seen. Grow smart.
Build the base. Push the signal. Scale the ops.
```

---

# DESIGN SYSTEM NOTES

> Do not change these unless explicitly requested — they define the site's visual identity.

| Token | Value |
|-------|-------|
| Background | `#191919` |
| Accent (purple) | `#BAA3FD` |
| White | `#ffffff` |
| Font: Display | Glegoo (serif) |
| Font: Body | Unbounded (sans) |
| Font: Mono | Geist Mono |
| Max width | 1280px |
| Default radius | 16px |

**CSS load order (all pages):** `design-system.css` → `styles.css` → (page-specific, e.g. `services.css`)

**References:** Linear.app, Vercel.com, early Stripe.com

---

# CHANGE LOG

> Record edits here so Claude can track what changed and why.

| Date | Page | Section | Change |
|------|------|---------|--------|
| 2026-06-19 | — | — | Initial SITEMAP.md created |
