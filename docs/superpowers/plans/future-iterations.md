# MTO Superpowers — Future Iteration Plans

This directory tracks planned improvements to the MTO pillar slides and supporting materials.

---

## Planned: AKS vs OpenShift Variant Slides

**Goal:** Create a thin slide swap layer for different audiences without duplicating the full deck.

**Slides to swap:**
- Slide 5 (Introducing MTO) — adjust positioning language per platform
- Slide 3 (The Real Problem) — optionally call out OpenShift Projects vs MTO Tenants

**Approach:** Add a CSS class (`body.aks`, `body.openshift`) toggled by a query param `?audience=aks` or `?audience=openshift`. Swap slide copy via JS on load.

---

## Planned: Compliance Deep-Dive Slide

**Goal:** Expand Pillar 6 (Compliance) into its own dedicated slide for regulated-industry audiences (finance, public sector, healthcare).

**Content to add:**
- Specific regulation callouts: ISO 27001, DORA, SOC 2, NIS2
- Kyverno policy examples (what "Policy-as-Code" looks like in practice)
- Audit evidence generation flow: policy → enforcement → audit trail

---

## Planned: Architecture Diagram Slide

**Goal:** Add a technical architecture diagram (similar to SCO's toggle slide) showing:

- Executive view: Kubernetes cluster → MTO layer → tenants (simple layered boxes)
- Technical view: Kubernetes API → Tenant Operator → Template Operator → Kyverno → ArgoCD integration

**Toggle mechanism:** Same as SCO — click diagram or press `t` to toggle exec/technical.

---

## Planned: FinOps Deep-Dive Slide

**Goal:** Dedicated slide for FinOps-focused conversations (when finance is in the room).

**Content:**
- Cost flow: workload runs → resource consumption metered → per-tenant cost record generated
- Showback vs chargeback distinction
- Integration with external billing/ERP (MTO generates the data, not the invoice)
- Hibernation savings calculator concept (non-prod hours × avg cost)

---

## Planned: Demo Notes

**Goal:** Create a `DEMO-NOTES.md` equivalent to the SCO version — step-by-step walkthrough of a live MTO demo following the presentation.

**Sections:**
1. Show tenant creation (kubectl apply → tenant provisioned with full isolation)
2. Show template inheritance (namespace created with golden template applied)
3. Show hibernation schedule (cron-based sleep/wake)
4. Show FinOps dashboard (per-tenant cost breakdown)
5. Show Kyverno policy enforcement (violating deploy rejected with clear message)
