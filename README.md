# Growth Friction Index™ (GFI)

Business diagnostic assessment platform by **Anera** — helps business owners identify the biggest friction points limiting their growth, delivered as a shareable, MBTI-style diagnostic experience.

> ⚠️ **This repository is documentation-only.** It tracks project scope, decisions, and changelog. Source code is not published here.

---

## Overview

Growth Friction Index™ (GFI) is a proprietary diagnostic framework developed by Anera to:

- Generate qualified leads for Anera's growth/conversion services
- Educate business owners about hidden growth bottlenecks
- Position Anera as a growth and conversion expert
- Drive consultation and audit bookings
- Create a shareable business "archetype" result, similar to MBTI, DISC, or HubSpot Website Grader

## How It Works

Users complete a 25-question assessment across 5 growth dimensions:

| Dimension | Question |
|---|---|
| Visibility | Can customers find your business? |
| Trust | Do customers trust your business? |
| Conversion | Can interested prospects easily become customers? |
| Follow-Up | Does the business consistently nurture opportunities? |
| System | Can the business measure and improve performance? |

Each dimension is scored 0–20 (5 questions × 0–4 scale), combining into a total **GFI Score (0–100)**. The lowest-scoring dimension determines the user's **Growth Archetype** (e.g. "The Invisible Business", "The Busy But Bleeding Business"), each with a tailored headline, blind spot, and recommended next step.

Users also get a **Revenue Opportunity Estimate** based on monthly leads, estimated leakage rate, and average transaction value — designed to create curiosity and drive consultation bookings.

## User Flow

```
Landing Page → Introduction → Assessment → Lead Capture →
Score Calculation → Archetype Calculation → Results Dashboard →
PDF Generation → Email Delivery → Consultation CTA
```

## Tech Stack

- **Backend:** PHP (no MySQL — file-based JSON/CSV storage)
- **Frontend:** HTML, CSS (Urbanist font), vanilla JavaScript
- **Hosting:** Shared hosting (Hostinger), no server framework required
- **Email/CRM:** kirim.email integration for lead automation
- **PDF Generation:** Client-side HTML → PDF report generation

## Environments

| Environment | URL | Status |
|---|---|---|
| Production | `gfilab.id` | Active |
| Staging | `staging.gfilab.id` | Active |


## Project Status

Actively in development. See [CHANGELOG.md](./CHANGELOG.md) for recent updates.

### Roadmap

- **Phase 2:** AI-generated insights
- **Phase 3:** Industry benchmarking (clinics, agencies, SMEs)
- **Phase 4:** Multi-language support
- **Phase 5:** Standalone SaaS product

## Design Direction

Premium, modern, consultant-like — intentionally avoiding generic quiz/survey aesthetics or cheap marketing-funnel styling. The goal is for the experience to feel like a professional business diagnostic platform, not a typical lead magnet.

---

**© Anera** — Growth Friction Index™ is a proprietary framework and trademark of Anera. Not for redistribution.
