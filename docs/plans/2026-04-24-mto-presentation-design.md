# MTO Enterprise Pitch — Presentation Design

## Context

- Audience: Platform leads, CTOs, infrastructure architects (first or second meeting)
- Their situation: Running Kubernetes at scale, dealing with cluster sprawl or early signs of it, aware of multi-tenancy challenges
- Goal: Move them from "we have Kubernetes" to "we need an enterprise platform — and that platform is MTO"

## Narrative Architecture

The presentation follows a five-beat psychological flow — not a feature list:

```
Pain → Reframe → Solution → Confidence → Action
```

Each beat must complete before the next begins. Skipping the reframe (jumping straight from pain to product) is the most common pitch mistake — it leaves the customer thinking "but we could just build this ourselves."

## Slide-by-Slide Design Notes

### Slide 0 — Title
Clean, minimal. Eyebrow sets context ("Stakater Multi-Tenant Operator"). Headline states the transformation, not the product name. Pills establish instant credibility: Red Hat Certified, OpenShift Native, AKS Compatible, any distro.

Don't open with the product. Open with the promise.

### Slide 1 — The Multi-Cluster Trap
The hook. Mirror the customer's actual decision back at them — sympathetically. "Let's give each team their own cluster" is a reasonable decision that most teams make. Don't mock it. Validate it first, then show what happens.

Visual: cluster-chaos grid that grows redder as it scales. Three consequence cards on the right. The emotional landing: this isn't their fault — it's the predictable outcome of the wrong model.

### Slide 2 — Where This Always Leads
Quantify the pain with stats. Three callout numbers (6×, 40%, 0). Not sourced from research papers — industry pattern numbers that resonate as true. The audience will nod, not challenge them.

The one-liner at the bottom is the bridge to the next section:
> "Clusters don't scale. Platforms do."

This is the pivot point. Don't rush past it.

### Slide 3 — The Real Problem
The reframe. Most pitches skip this slide. Don't.

The customer needs to hear that they've been solving the wrong problem — not because they're wrong, but because the right framing changes what the solution looks like. Three industry truths, stated plainly:
1. Namespace ≠ multi-tenancy
2. Kubernetes gives primitives, not a platform
3. Self-service without guardrails is a compliance risk

End with: "This is not a Kubernetes problem. It's a platform problem."

### Slide 4 — The Platform Model
Introduce the model before introducing MTO. Let the solution feel inevitable before you name it.

Visual: cluster chaos (left) → arrow → tenant model diagram (right). The tenant model diagram shows a single cluster with multiple isolated tenant tags inside — the visual contrast does the selling.

Four outcomes on the right confirm what the model delivers. End with the pairing of the earlier one-liner:
> "Clusters give isolation. Platforms give control."

### Slide 5 — Introducing MTO
Now name the product. Two-column: Kubernetes provides (left, muted gray) vs MTO provides (right, with orange accent border). The contrast is the point.

The quote block at the bottom is the positioning statement:
> "Every enterprise eventually builds this layer. MTO gives it to you out of the box."

Don't over-explain here. The product intro should be brief and confident. The pillars slide does the depth.

### Slide 6 — The 6 Pillars
Three-column grid of pillar cards. Five neutral cards + one featured card (Compliance) with an "DIFFERENTIATOR" badge.

Key design decision: frame each pillar by what it *eliminates*, not what it *adds*. Buyers respond to pain removal more than feature addition.

Compliance is featured because it's the pillar that elevates MTO from "multi-tenancy tool" to "enterprise platform." Every other pillar has competitors. The combination of continuous policy enforcement + audit-ready output is what closes regulated-industry deals.

### Slide 7 — Before vs After
Six-row comparison table. Before (red header) vs After (orange header). This is the emotional decision slide — the audience should look at the Before column and see themselves.

Design: clean table, no decorative elements. The content contrast is the visual. Keep rows short — each one should land in under 3 seconds of reading.

### Slide 8 — Build vs Buy
The objection killer. Address it directly, not defensively.

The build-vs-buy table quantifies what DIY actually requires: 6+ months across 6 capability areas, then ownership forever. The right column is always "Day one" or "Plug-and-play."

The closing line is the one to land clearly:
> "You're not avoiding the work. You're choosing to own it forever."

### Slide 9 — Business Value
Translate the platform story into language for each stakeholder in the room. Four outcome rows (left) + three audience-specific cards (right). Each card is labeled by audience type — engineering leadership, finance, security.

This slide works best when you know who's in the room and can emphasize the relevant card.

### Slide 10 — Adoption Path
Four steps. Remove fear of starting. The key message is that there is no big-bang migration — you install MTO alongside existing workloads on a single cluster and expand from there.

Concrete timelines per step matter. "Weeks, not months" needs to be specific enough to be credible: 1-2 weeks for pilot, 4-6 weeks to expand, 8-12 weeks to standardize.

### Slide 11 — Why Stakater
Four credential badges (Red Hat Premier Partner, Certified Operator, multi-tenancy specialists, product + consulting). Followed by four customer quotes — short, outcome-focused, no attribution needed.

Don't oversell here. The credibility is in the specificity of the quotes, not the length of the company history.

### Slide 12 — Closing CTA
Dark gradient background — same CTA pattern as SCO deck. Headline states the inevitability plainly. Two-option comparison (Option A: build yourself vs Option B: MTO) laid out as equal-width cards — but Option B has the orange border accent.

Three CTA pills at the bottom: Workshop/Assessment, Pilot Deployment, Platform Maturity Roadmap. The first conversation to aim for is always the Assessment or Pilot — low commitment, high signal.

## Technical Design

### CSS Architecture
- Custom properties for all brand colors (easily swappable for white-label or partner versions)
- No external CSS frameworks — fully self-contained
- `display: none` / `display: flex` toggle for active slide (not opacity — avoids bleed-through on screenshot)
- Font loaded from Google Fonts (Inter) — for offline use, download and self-host

### Navigation
- Arrow keys (← → ↑ ↓), Space, Home, End
- Swipe left/right for touch devices
- Clickable nav dots at bottom
- Slide counter (current / total) fixed bottom-right

### Diagrams
- All diagrams are pure HTML/CSS — no SVG, no canvas, no external libraries
- Cluster chaos grid: CSS flexbox with `.cluster-box` and `.cluster-box.stressed` variants
- Tenant model: `.tenant-cluster` with `.tenant-row` inside
- Before/After: native `<table>` with custom thead/td styling
- Adoption steps: flex row with `::after` arrow pseudo-elements

### Self-Contained Build
The `src/pages/index.astro` file compiles to a single HTML file with no runtime dependencies. For offline/standalone use, run `npm run build` and open `dist/index.html` — or use the pre-built `mto-presentation-standalone.html` (logo embedded as base64).
