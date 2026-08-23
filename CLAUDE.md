# Opryn Landing Page — Build Instructions for Claude Code

## What this repo is
A standalone marketing landing page for **Opryn** (Opryn OS) — a WhatsApp-native
business operations platform for traditional, non-technical SMEs in emerging
markets (retail, pharmacy, F&B, wholesale distribution). This repo is
independent of the Opryn OS application codebase. Do not assume backend access.

## Before you write any code
Look at these files first, in this order:
1. `/design/reference.png` (or `.jpg`) — a screenshot of a website design pulled
   from Godly that captures the visual direction (layout, spacing, imagery style,
   general "feel"). Study its structure: hero layout, section rhythm, use of
   whitespace, image treatment, button/card styling. Do not clone it verbatim —
   it's a reference for *quality and structure*, not a template to trace.
2. `/design/logo.svg` (or whatever format is provided) — the actual Opryn logo
   file. Use this exact asset; do not recreate or approximate the logo from
   description.
3. This file, for brand tokens, copy direction, and content.

If either design file is missing when you start, stop and ask rather than
guessing or generating a placeholder logo/screenshot.

## Brand tokens (from Opryn OS 2.0 Premium Brand Identity System)

```
--navy: #0D1B2A;         /* wordmark on light backgrounds, primary/enterprise trust */
--primary-blue: #1B6CA8; /* O-ring, accent elements, interactive components */
--accent-blue: #4f9cf9;  /* gradient midpoint */
--light-blue: #7ab8fb;   /* gradient start, highlights, growth/motion */
--cream: #f0ece4;        /* wordmark + primary text on dark backgrounds */
--dark-bg: #0a0a0a;
```

- **Wordmark font:** Outfit (sans-serif), weight 500, letter-spacing -0.8px.
- **Display/headline font:** Cormorant Garamond (serif), weight 300 — used for
  large section titles, gives the "premium" register.
- **Mono/label font:** DM Mono — used sparingly, for small uppercase tags/labels
  (e.g. eyebrow text above a headline), letter-spacing 0.15–0.2em, uppercase.
- **Body font:** Outfit, weight 300–400.
- Gradient rule: any gradient use is diagonal 45°, light-blue → primary-blue.
  Never use a flat single color where the brand system specifies a gradient
  (e.g. the arrow/growth elements).
- Navy for wordmark/text on light backgrounds; cream on dark backgrounds.
  Maintain at least 2:1 contrast.

## Logo usage rules
- Minimum size: 64×64px (icon mark alone) or 240px width (full lockup).
- Clear space: at least 8px on all sides, scaling up with logo size — nothing
  else may intrude on that space.
- Use the horizontal lockup (icon + wordmark) in the site header/nav, left-aligned.
- Use the icon mark alone for favicon and any small/square placement.
- Never recolor, distort, rotate, skew, or add shadows/glows/outlines to the logo.
- Never separate the O-ring icon from the wordmark in the header — that's the
  primary lockup and should stay intact.

## Positioning & tone (this is the hardest part to get right — read this twice)
Opryn's mission: run your operations with the clarity of a Fortune 500 company,
with data entry as simple as sending a WhatsApp message. The copy needs to hold
**two registers at once**:
1. **Aspirational / luxury-adjacent** — elevated, confident, not startup-generic.
   This is where Cormorant Garamond headlines and generous whitespace do the work.
2. **Practical / pain-point literate** — this is for a shop owner in Lagos or
   Accra who is tired of manual stock counts and end-of-day reconciliation, not
   a Silicon Valley buyer. Don't drift into jargon ("leverage," "synergy,"
   "unlock your data") — speak to a real operational pain plainly, then let the
   visual design carry the premium feel.

Do not write generic SaaS copy ("Streamline your business with our
all-in-one platform"). Every headline/subhead should be traceable to a real
Opryn capability: inventory + COGS tracking, WhatsApp-native (zero dashboard,
zero app to download), demand forecasting, purchase orders, sales approval
thresholds, discovery via a WhatsApp chatbot.

Zero-dashboard / WhatsApp-native is the core differentiator — make this a
headline idea, not a footnote. The pitch is "no new app, no dashboard to learn
— it works inside the app your staff already have open all day."

## Tech stack (recommendation — confirm before deviating)
Static site, no backend needed for a landing page:
- Plain HTML/CSS/vanilla JS, **or** Next.js with static export if you expect to
  add a blog/CMS later.
- Deploy target: Vercel or Netlify (either works with a static export).
- No database, no auth, no API routes — this page only needs a contact/waitlist
  form, which can post to a simple form service (e.g. Formspree) or a WhatsApp
  click-to-chat link rather than custom backend code.
- Mobile-first: a large share of visitors will be on mobile in the target markets.

## What "done" looks like for a first pass
- Hero section: headline (Cormorant Garamond), subhead, primary CTA
  ("Get Started" / WhatsApp click-to-chat link), logo lockup in nav.
- 3–4 sections translating real capabilities (inventory/COGS, forecasting,
  WhatsApp-native, purchase orders) into plain-language benefit statements.
- Visual proof section (mockup/screenshot placeholder acceptable if no real
  product screenshots exist yet — flag this rather than inventing fake UI).
- Footer with logo icon mark + basic contact/social placeholders.
- Responsive at mobile, tablet, desktop breakpoints.

## What NOT to do
- Don't invent stats, customer counts, testimonials, or logos of companies
  "using" Opryn — there are none yet. Flag anywhere a real placeholder is needed.
- Don't build backend features, auth, or payment flows in this repo.
- Don't deviate from the brand color/font tokens above without flagging it first.
