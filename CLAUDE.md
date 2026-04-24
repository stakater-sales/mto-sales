# MTO Enterprise Pitch — Project Rules

## Working Style

- Prefer surgical changes with limited side-effects. Touch only what the task requires; leave unrelated code, layouts, and copy alone. No opportunistic refactors or cleanups bundled in.

## Slide Design

### Accent Rule
Only accent (`.highlight`) the **core concept** each slide is introducing — the one thing the audience should remember from that slide.

- Accent the key noun or phrase, not filler words
- Do not use `<strong>` for emphasis in slides — use `.highlight` or nothing
- One accent per slide title is the default; two is acceptable if both are core concepts
- Body text and subtitles should generally remain unaccented unless the concept is the slide's primary takeaway

### Presentation Style
- Minimal text per slide — short phrases, not sentences
- Use visual structure (cards, pills, flow diagrams) over bullet lists
- Alternate between `section-light` and default white backgrounds
- Content should breathe — don't pack slides tight; favor whitespace and spacing
- Keep layouts balanced — if two columns, ensure equal visual weight
- Avoid abbreviations unless already introduced — write out "Multi-Tenant Operator" before shortening to MTO

### Visual Language
- Brand color: `--primary` (#EA7845 Stakater orange) for customer deck
- Three-tier visual hierarchy: neutral (white/light border) → accented (primary border, tinted bg) → strong (gradient bg)
- The closing CTA slide uses a dark gradient background — matches SCO pattern
- Cards with `accented` class use `--primary-light` background + `--primary` border
- `.quote-block` uses left orange border for customer quotes and key statements

## Speaker Notes Style

### Voice
- Conversational and direct — written as spoken words, not essay prose
- Confident but not salesy — state facts, don't oversell
- Short declarative sentences — no filler, no hedging
- Use `>` blockquotes for what to actually say; plain text for stage directions

### Structure per slide
- Open with the key framing line
- Walk through the content naturally (don't narrate the slide verbatim)
- Land with a punchy relationship or takeaway
- Stage directions are brief and practical ("Pause. Let that land.", "Keep it short.", "Don't fake it.")

### Terminology
- Use "MTO" after first introduction; spell out "Multi-Tenant Operator" on first mention
- "Platform layer" not "product" when positioning MTO's role
- "Tenant" not "namespace" — this distinction is a core part of the pitch
- Don't spoil later slides — each note should set up without revealing what comes next

## Slide Variants

### For AKS Audiences
Slide 5 positioning: "AKS gives you Kubernetes. MTO gives you the platform on top."
Emphasize: Standardization, governance, self-service, cost visibility.
Tone: "We help you build what you don't have yet."

### For OpenShift Audiences
Slide 5 positioning: "OpenShift provides the foundation. MTO completes the platform."
Emphasize: Tenant abstraction beyond projects, FinOps gap, compliance automation, multi-team scale.
Tone: "We extend what you already invested in."

## File Structure

```
mto-enterprise-pitch/
├── src/pages/index.astro          # Single-file slide deck — edit here
├── public/stakater-logo.png       # Logo — fixed top-left on all slides
├── CLAUDE.md                      # This file
├── SPEAKER-NOTES.md               # Speaker notes per slide (customer deck)
├── README.md                      # Setup and navigation guide
├── docs/
│   ├── plans/
│   │   └── 2026-04-24-mto-presentation-plan.md   # Narrative & slide plan
│   └── superpowers/
│       ├── plans/                 # Future iteration plans go here
│       └── specs/
│           └── pillars.md         # Full 6-pillar spec (Problem→Why→Solution→Outcome)
├── package.json
└── astro.config.mjs
```
