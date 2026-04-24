# MTO Enterprise Pitch — Presentation Plan

## Goal
Create a customer-facing Astro slide deck that positions Stakater Multi-Tenant Operator (MTO) as the **Enterprise Kubernetes Platform Layer** — the missing piece that turns raw Kubernetes clusters into a governed, scalable, multi-tenant platform.

## Audience
- Platform engineering leads, CTOs, infrastructure architects
- Organizations running AKS, OpenShift, or vanilla Kubernetes at scale
- Teams currently managing cluster sprawl or attempting DIY multi-tenancy

## Narrative Arc
Move the customer from:
> "We have Kubernetes clusters running"

To:
> "We need an enterprise platform — and that platform is MTO"

The story has five beats:
1. **Pain** → "We are struggling with cluster sprawl and governance"
2. **Reframe** → "We misunderstood the problem — clusters aren't the answer, platforms are"
3. **Solution** → "This is what we need — MTO"
4. **Confidence** → "This works, it's proven, it's safe to adopt"
5. **Action** → "Let's start"

## Architecture
Single-file Astro slide deck (`src/pages/index.astro`) matching the SCO presentation's design system:
- Same CSS custom properties and typography
- Same section-light / dark alternating pattern
- Same `.highlight` accent class
- Same keyboard navigation
- Brand color: `#EA7845` (Stakater orange) for customer deck
- Speaker notes in `SPEAKER-NOTES.md`

## Slide Structure

### Slide 0 — Title
"Stakater MTO — From Kubernetes Clusters to Enterprise Platform"

### Slide 1 — The Multi-Cluster Trap
Opening hook. Most teams start with cluster-per-team for isolation. That decision makes sense on day one. By month six, it's a management disaster.

### Slide 2 — Where This Always Leads
Make the pain concrete. Cluster sprawl metrics. Platform team burnout. Security drift. Cost explosion. "This is not a future risk — this is what always happens."

### Slide 3 — The Real Problem
Reframe: this isn't a Kubernetes problem. It's a platform problem. Kubernetes provides primitives. Enterprises need a platform. "Namespace is not multi-tenancy."

### Slide 4 — The Platform Model
Introduce the right model before introducing MTO. Few clusters. Many secure tenants. Central governance. Self-service with guardrails. Let the solution feel inevitable.

### Slide 5 — Introducing MTO
MTO is the enterprise platform layer. Not another tool — the missing control plane. "The platform you end up building anyway — out of the box."

### Slide 6 — The 6 Pillars
Tenancy, Templates, Hibernation, FinOps, Extensions, Compliance. Each shown as Problem → How MTO Solves It. Compliance is the strategic differentiator — highlight strongest.

### Slide 7 — Before vs After
Visual transformation. Before: cluster sprawl, manual ops, no visibility, weak governance. After: controlled tenants, automated lifecycle, full visibility, built-in governance.

### Slide 8 — Build vs Buy
Kill the "we'll build it ourselves" objection. Quantify the real engineering cost. Frame MTO as cost control, not cost addition.

### Slide 9 — Business Value
Translate platform outcomes to executive language. Faster delivery. Reduced overhead. Built-in compliance. Predictable cost model.

### Slide 10 — Adoption Path
Remove fear of adoption. Pilot → Expand → Scale. Weeks, not months. No big-bang migration required.

### Slide 11 — Why Stakater
Red Hat Premier Partner. Kubernetes specialists. MTO is Red Hat Certified. Product + consulting combination.

### Slide 12 — Closing CTA
"The decision" framing. Continue scaling clusters and complexity — or move to a platform model with MTO.

## Technical Notes
- Pure HTML/CSS diagrams — no external dependencies
- Same Inter font, Stakater orange accent, dark text on light backgrounds
- Architecture/pillars sections use card grid layouts
- Before/after uses two-column comparison table styling
