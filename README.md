# MTO Enterprise Pitch — Stakater Multi-Tenant Operator

Astro-based slide deck for pitching MTO as the Enterprise Kubernetes Platform Layer.

## Design System

Matches the SCO Hyperscaler Engine presentation:
- Font: Inter (Google Fonts)
- Brand color: `#EA7845` (Stakater orange)
- Light/dark alternating slide backgrounds
- `.highlight` class for accent text
- Pure HTML/CSS diagrams — no external dependencies

## Running

```bash
npm install
npm run dev
```

Open `http://localhost:4321` in your browser.

## Navigation

| Key | Action |
|-----|--------|
| `→` / `↓` / `Space` | Next slide |
| `←` / `↑` | Previous slide |
| `Home` | First slide |
| `End` | Last slide |
| Click nav dots | Jump to slide |
| Swipe left/right | Next/prev (touch) |

## Slide Structure

| # | Slide | Purpose |
|---|-------|---------|
| 0 | Title | Opening, credentials |
| 1 | The Multi-Cluster Trap | Hook — mirror the pain |
| 2 | Where This Always Leads | Quantify the problem |
| 3 | The Real Problem | Reframe: platform problem, not cluster problem |
| 4 | The Platform Model | The right model (before naming MTO) |
| 5 | Introducing MTO | Product introduction |
| 6 | The 6 Pillars | Capability overview |
| 7 | Before vs After | Visual transformation |
| 8 | Build vs Buy | Kill the DIY objection |
| 9 | Business Value | Executive framing |
| 10 | Adoption Path | Remove fear of starting |
| 11 | Why Stakater | Credibility + social proof |
| 12 | Closing CTA | The decision |

## Speaker Notes

See `SPEAKER-NOTES.md` for full speaker notes per slide.

## Variants

For AKS audiences: emphasize slide 3 ("platform problem, not cluster problem") and slide 5 (MTO adds the platform on top of what AKS gives you).

For OpenShift audiences: on slide 5, position as "OpenShift provides the foundation — MTO completes the platform."

## Files

```
mto-enterprise-pitch/
├── src/pages/index.astro     # Full slide deck
├── public/stakater-logo.png  # Stakater logo
├── SPEAKER-NOTES.md          # Speaker notes per slide
├── docs/
│   ├── plans/                # Presentation plan documents
│   └── superpowers/
│       └── specs/pillars.md  # 6 pillars full spec
├── package.json
└── astro.config.mjs
```
