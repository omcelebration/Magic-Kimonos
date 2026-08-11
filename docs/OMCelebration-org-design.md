# Magic Kimonos — OMCelebration Paperclip Org Design & Operating System

**Version:** 1.0  
**Date:** 2026-08-11  
**Company:** OMCelebration (Magic Collective)  
**Paperclip Company ID:** `69d8c1ea-30ad-4375-9f17-fdcbac23d95e`  
**Store:** u5bsgd-02.myshopify.com  
**Status:** Draft — Awaiting Founder Approval

---

## 1. Mission & Operating Context

OMCelebration is the umbrella company for **Magic Collective** — three brands unified by wearable art, movement, and community:

- **Magic Kimonos** — Genderless wearable art for movement, travel, music, festivals, city, beach.
- **Magic Glasses** — Eyewear line (~400 units in stock).
- **Path of Light** — Complementary brand within the ecosystem.

**Emotional Promise:** The customer does not only buy a garment. They enter a world of art, freedom, connection, and community.

**Voice:** Calm, elegant, human, confident, and poetic without exaggeration.

**Visual Direction:** Generous spacing, large images, editorial typography, natural palette (ivory, sand, black, warm beige, charcoal). Strong color lives in the kimonos and photography.

### Hard Rules (Non-Negotiable)
- **Never** edit the live Shopify theme directly.
- **Never** publish without explicit founder approval.
- **Never** touch OpenAI API billing.
- **Never** modify the owner's ideas or brand voice.
- **Never** use fake countdown timers or permanent-discount visual strategies.
- **Never** publish sustainability claims without evidence.
- **Never** label a product "silk" unless it contains silk.

---

## 2. The Eisenhower Matrix: Org Structure

The entire Paperclip org is structured around the **Eisenhower Matrix**. Every agent, task, and decision is routed through one of four quadrants. This is the single source of truth for priority, ownership, and workflow.

```
                  URGENT
                     │
         ┌───────────┼───────────┐
         │           │           │
         │   Q1      │   Q2      │
         │   DO      │   DECIDE  │
         │           │           │
NON-     ├───────────┼───────────┤
URGENT   │           │           │
         │   Q3      │   Q4      │
         │ DELEGATE  │  DELETE   │
         │           │           │
         └───────────┼───────────┘
                     │
                  NOT URGENT
```

### Q1 — DO (Urgent & Important)
**Execute immediately. No waiting. CEO or assigned lead takes action.**

| Domain | Owner | Examples |
|--------|-------|----------|
| Store outages / payment failures | Shopify Ops Lead | Fixing broken checkout, responding to critical alerts |
| Time-sensitive inventory updates | Shopify Ops Lead | Marking items sold out, updating stock counts |
| Customer service escalations | Shopify Ops Lead | Refunds, shipping disasters, complaints |
| Live marketing activations | Marketing Lead | Posting scheduled content, engaging real-time |
| Content deadlines | Content Lead | Publishing approved blog posts, updating journal |

**Rule:** Q1 items are reported to the CEO in the daily digest, not escalated for permission — they are actioned and logged.

### Q2 — DECIDE (Not Urgent & Important)
**CEO owns these. Strategic decisions that shape the business.**

| Domain | Owner | Examples |
|--------|-------|----------|
| Brand positioning & messaging | CEO | Finalizing hero copy, artist collaboration angles |
| Product pricing & SKU strategy | CEO | Confirming Base/Friends/Silk/Exclusive tiers |
| Marketing budget allocation | CEO | Monthly spend, channel mix, ambassador program |
| Tech stack & platform choices | CEO | Theme architecture, app approvals, GitHub strategy |
| Partner & wholesale relationships | CEO | Wholesale terms, artist contracts, ambassador program |
| Cross-brand strategy | CEO | Magic Collective cross-promotion priorities |

**Rule:** Q2 items require CEO decision. Agents prepare briefs with options and a recommendation. CEO responds within 24 hours or escalates to board review.

### Q3 — DELEGATE (Urgent & Not Important)
**Assign to specialist agents. CEO sets the standard, agent executes.**

| Domain | Owner | Examples |
|--------|-------|----------|
| Routine theme updates | Shopify Ops Lead | Duplicating dev theme, applying approved sections |
| Image optimization | Content Lead | Compressing assets, generating alt text |
| Social media scheduling | Marketing Lead | Queueing posts, drafting captions |
| Data entry / metadata | Shopify Ops Lead | Product tags, collection descriptions |
| Monitoring & alerts | Shopify Ops Lead | Daily sales reports, stock level checks |

**Rule:** Q3 items are delegated with clear success criteria. CEO audits output, not process. If quality drops, the task escalates to Q2 for re-evaluation of the agent or brief.

### Q4 — DELETE (Not Urgent & Not Important)
**Eliminate. These tasks do not serve the brand.**

| Domain | Action |
|--------|--------|
| Fake countdown timers | Delete — violates brand trust |
| Permanent-discount visual banners | Delete — degrades perceived value |
| Unverified sustainability claims | Delete — legal and brand risk |
| Overcrowded homepage sections | Delete — violates "fewer but stronger" rule |
| Unapproved theme experiments | Delete — wastes dev resources |
| Redundant metrics dashboards | Delete — no one reads them |

**Rule:** Q4 items are formally logged in the weekly board review as "eliminated" so the team sees what was stopped, not just what was started.

---

## 3. Paperclip Agent Roles & Responsibilities

### 3.1 CEO Agent (`hermes_local`)
**Reports to:** Founder / Magic Kimonos owner  
**Role:** Strategic brain of the operation. Owns Q2 decisions, orchestrates Q1/Q3/Q4, audits all agents, and is the sole interface with the founder for strategic matters.

**Core Responsibilities:**
- Finalize all brand, product, and marketing decisions
- Assign tasks to specialist agents across quadrants
- Review and approve all outputs before they touch the live store
- Maintain the OMCelebration org design and update it as the team evolves
- Escalate founder-level decisions only when irreversible or outside defined authority
- Weekly board review facilitation and investor reporting

**Tools:** Hermes Agent (this system), Paperclip orchestrator, daily digest generator, board review facilitator.

---

### 3.2 Shopify Ops Lead (`hermes_local`)
**Reports to:** CEO  
**Role:** Technical guardian of the Shopify store. Owns all Q1 operational emergencies and Q3 delegated theme/shop tasks.

**Core Responsibilities:**
- Duplicate and work on the **dev theme only** (never live theme)
- Apply approved sections, product updates, and collection changes to dev
- Run daily stock checks and flag discrepancies to CEO
- Manage Shopify Admin under a **collaborator account** (not owner-level unless explicitly approved)
- Monitor checkout flow, payment gateways, and shipping settings
- Prepare deployment packages for founder approval

**Decision Rights:**
- Can fix broken metafields, adjust collection sorting, update product availability in dev
- Cannot publish to live, change theme settings on live, or modify pricing without CEO approval

**Escalation:** Any live-store issue → immediate Q1 → CEO notification within 15 minutes.

---

### 3.3 Content Lead (`hermes_local`)
**Reports to:** CEO (via Shopify Ops Lead for technical assets, directly for creative direction)  
**Role:** Voice and visual guardian of Magic Kimonos. Owns all content that touches the customer.

**Core Responsibilities:**
- Draft homepage hero copy, product descriptions, artist stories, and about-page narrative
- Maintain brand voice: calm, elegant, human, confident, poetic
- Optimize images for web (compression, alt text, lazy-load attributes)
- Write journal posts and newsletter drafts
- Review all public-facing content before it leaves the org

**Decision Rights:**
- Can reword and polish approved content briefs
- Cannot change core brand messaging, pricing mentions, or product claims without CEO sign-off

**Escalation:** Any content touching sustainability, material claims, or pricing → Q2 → CEO approval required.

---

### 3.4 Marketing Lead (`hermes_local`)
**Reports to:** CEO  
**Role:** Growth engine. Owns all marketing activations, channel strategy, and customer acquisition.

**Core Responsibilities:**
- Draft social media captions and campaign concepts
- Schedule and queue organic content (Instagram, TikTok, Pinterest as approved)
- Prepare paid campaign briefs for CEO approval
- Monitor campaign performance and produce weekly channel reports
- Ambassador program coordination (draft outreach, track referrals)

**Decision Rights:**
- Can schedule approved content and adjust captions within brand voice
- Cannot launch paid campaigns, commit budget, or change targeting without CEO approval

**Escalation:** Any paid activation → Q2 → CEO approval. Budget overruns → immediate escalation.

---

### 3.5 Codex Coding Specialist
**Reports to:** CEO (via Shopify Ops Lead for technical tasks)  
**Role:** Hands-on coding specialist for Liquid, CSS, JavaScript, and theme architecture. Executes Q3 delegated development work only.

**Core Responsibilities:**
- Build and modify Liquid sections, snippets, and templates on the **dev theme**
- Implement homepage architecture per CEO brief (hero, featured collection, artists, movement, lifestyle, newsletter)
- Optimize theme performance (image loading, font subsetting, CSS cleanup)
- Maintain GitHub repo for theme code backup and version control
- Fix bugs reported by Shopify Ops Lead

**Decision Rights:**
- Can write and test code on the dev theme
- Cannot publish to live, merge to protected branches without approval, or change checkout logic

**Workflow:**
1. CEO or Shopify Ops Lead assigns a ticket via Paperclip with a clear brief
2. Codex works in the duplicated dev theme branch
3. Output is reviewed by Shopify Ops Lead for technical correctness
4. CEO reviews for brand alignment
5. Founder approves before any merge to main or live publish

**Governance:** Codex does not hold Shopify Admin access directly. All work is mediated through Paperclip agents.

---

## 4. Reporting Lines

```
Founder (Magic Kimonos)
    │
    ▼
CEO Agent (OMCelebration)
    │
    ├──► Shopify Ops Lead
    │       └──► Codex (coding specialist, task-based)
    │
    ├──► Content Lead
    │
    └──► Marketing Lead
```

**Flat by design.** No agent manages another agent except the CEO. This keeps communication fast and accountability clear.

**Paperclip Visibility:** All agent outputs, decisions, and escalations are logged in the Paperclip company workspace. The CEO can audit any agent's recent work at any time.

---

## 5. Decision Rights Matrix

| Decision Type | Authority | Must Inform CEO | Must Approve Founder |
|---------------|-----------|-----------------|----------------------|
| Fix broken dev theme section | Shopify Ops Lead | Weekly | No |
| Adjust product tags in dev | Shopify Ops Lead | Daily digest | No |
| Change product pricing | CEO | Yes | Yes |
| Publish to live theme | CEO | Yes | Yes |
| Launch paid marketing campaign | Marketing Lead → CEO | Yes | Yes |
| Draft new brand copy | Content Lead | Weekly | No |
| Change core brand messaging | CEO | Yes | Yes |
| Ambassador program terms | CEO | Yes | Yes |
| Theme architecture changes | CEO + Codex | Yes | No |
| Add/remove Paperclip agents | CEO | Yes | No |
| GitHub branch strategy | CEO | Yes | No |
| Inventory count updates | Shopify Ops Lead | Weekly | No |
| Sustainability claims | CEO | Yes | Yes |

---

## 6. Escalation Paths

### Standard Path (Non-Emergency)
```
Agent detects need for decision
    → Agent documents options + recommendation
    → Routes to CEO via Paperclip Q2 queue
    → CEO decides within 24 hours
    → CEO communicates decision back to agent
    → Agent executes
```

### Emergency Path (Q1 — Store Down, Payment Failure, etc.)
```
Agent detects emergency
    → Agent executes immediate fix within authority
    → Agent notifies CEO within 15 minutes via urgent alert
    → CEO reviews and confirms/adjusts action
    → Incident logged in daily digest
```

### Founder Escalation Path (Irreversible or High-Stakes)
```
CEO determines decision is irreversible or high-stakes
    → CEO prepares one-page brief: context, options, recommendation, risk
    → Routes to Founder via preferred channel (WhatsApp/Email/IG DM as authorized)
    → Founder responds
    → CEO executes and confirms
```

**Never** publish, charge, or commit the brand publicly without founder approval on high-stakes decisions.

---

## 7. 24/7 Workflow

Magic Kimonos operates with a **follow-the-sun + async-first** model. The org is designed to make progress while the founder sleeps, without requiring real-time presence.

### Daily Cycle

| Time Window | Activity | Owner |
|-------------|----------|-------|
| 06:00 — 07:00 | Founder wake-up digest | CEO → Founder |
| 07:00 — 22:00 | Active work window | All agents |
| 22:00 — 06:00 | Low-activity / monitoring | Shopify Ops Lead (alerts only) |
| Any time | Urgent Q1 escalation | Shopify Ops Lead / Marketing Lead → CEO |

### Daily Digest Format (sent to Founder each morning)
```
📋 OMCelebration Daily Digest — [Date]

✅ Completed Yesterday (3-5 bullets)
🔄 In Progress (current Q2/Q3 work)
⚠️ Needs Decision (Q2 items awaiting founder/CEO)
🚨 Urgent (Q1 items — resolved or ongoing)
📊 Metrics Snapshot (sales, visits, conversion, top products)
🗑️ Stopped (Q4 items eliminated)
```

### Async Operating Principles
- **No real-time meetings required.** All coordination happens via Paperclip threads.
- **All outputs are documented.** Agents do not speak for each other; they write.
- **CEO is the synthesizer.** The CEO reads all agent outputs and produces the digest for the founder.
- **Founder approval is asynchronous.** The founder reviews and approves on their schedule. Agents continue Q3 work that does not require approval.

---

## 8. Weekly Board-Style Review Cadence

Every **Monday at 10:00 AM** (founder's timezone), the CEO facilitates a structured board review. Format is designed to feel like a real board meeting — concise, decision-oriented, and forward-looking.

### 8.1 Review Agenda (60 minutes)

| Time | Section | Owner | Output |
|------|---------|-------|--------|
| 00:00 — 05:00 | Opening & Metrics | CEO | One-slide dashboard |
| 05:00 — 15:00 | Q4 Review (Stopped Work) | CEO | List of eliminated tasks + rationale |
| 15:00 — 30:00 | Q1/Q3 Review (Done & Delegated) | All leads | Progress updates, blockers |
| 30:00 — 45:00 | Q2 Review (Decisions Needed) | CEO | Decision queue, options, recommendations |
| 45:00 — 55:00 | Forward Look | CEO | Next week's priorities by quadrant |
| 55:00 — 60:00 | Founder Input | Founder | Strategic guidance, approvals |

### 8.2 Board Dashboard (Standard Template)
```
Magic Kimonos — Weekly Board Review
Week of: [Date]

METRICS
- Revenue: €X (vs €Y target)
- Orders: X (vs Y target)
- Conversion: X% (vs Y%)
- Top product: [SKU]
- Underperformer: [SKU]

Q4 STOPPED THIS WEEK
- [Item] — [Rationale]

Q1/Q3 PROGRESS
- [Agent]: [Completed] / [Blocked by]

Q2 DECISIONS REQUIRED
1. [Decision] — Options: [A/B/C] — CEO recommends: [X] — Deadline: [Date]

NEXT WEEK'S PRIORITIES
- Q1: [3 items]
- Q2: [2 decisions]
- Q3: [3 delegations]
```

### 8.3 Board Review Rules
- **No surprises.** All Q2 decisions are pre-circulated 24 hours before the meeting.
- **Decisions are recorded.** Every Q2 outcome is logged with owner and deadline.
- **No meeting without metrics.** If the dashboard isn't ready, the meeting is rescheduled.
- **Founder time is sacred.** The meeting ends on time. Strategic discussions that need more time are scheduled separately.

---

## 9. Investor Reporting Format

Magic Kimonos reports to Magic Collective stakeholders (including investors, if applicable) using a consistent, investor-grade format. The CEO owns this output.

### 9.1 Monthly Investor Update

```
MAGIC KIMONOS — Monthly Investor Update
Period: [Month Year]
Prepared by: OMCelebration CEO

EXECUTIVE SUMMARY (3 bullets)
- Top-line revenue and growth vs. prior month
- Key milestone achieved
- Biggest risk or opportunity

FINANCIALS
- Revenue: €X (target: €Y, variance: Z%)
- Gross Margin: X%
- Marketing Spend: €X (X% of revenue)
- Cash Runway: X months (if applicable)

OPERATIONAL HIGHLIGHTS
- Store performance: visitors, conversion, AOV
- Product: new SKUs launched, inventory status, best-sellers
- Marketing: channel performance, new campaigns, ambassador program status
- Tech: theme updates, app integrations, site speed

MAGIC COLLECTIVE SYNERGY
- Cross-promotion with Magic Glasses / Path of Light
- Shared brand initiatives
- Wholesale or partnership progress

RISKS & MITIGATIONS
- Risk: [Description]
- Mitigation: [Action]

LOOKING AHEAD
- Next month's priorities
- Key dates: sales events, product launches, content drops
- Capital needs (if any)
```

### 9.2 Quarterly Board Deck
- Extends the monthly format with 3-month trend charts
- Includes Magic Glasses and Path of Light roll-up for collective view
- Ends with strategic asks or decisions required from investors

---

## 10. Paperclip Company Configuration

### Current Agents
| Agent Name | Role | Provider | Status |
|------------|------|----------|--------|
| CEO | OMCelebration Chief Executive | hermes_local | Active |
| Shopify Ops Lead | Store operations & theme | hermes_local | Active |
| Content Lead | Brand voice & content | hermes_local | Active |
| Marketing Lead | Growth & campaigns | hermes_local | Active |
| Codex | Coding specialist | Codex CLI (ChatGPT auth) | On-demand |

### Agent Onboarding Protocol
1. Define role, quadrant, and decision rights in this document
2. Add agent to Paperclip company `69d8c1ea-30ad-4375-9f17-fdcbac23d95e`
3. Assign reporting line to CEO
4. Set alert thresholds and escalation rules
5. Run a 1-week shadow mode where outputs are reviewed before execution
6. Graduate to autonomous Q3 execution after 5 successful shadow outputs

---

## 11. GitHub & Deployment Strategy

### Branch Strategy
```
main (protected)
  └── development (integration branch)
        ├── feature/hero-redesign
        ├── feature/product-page-v2
        └── feature/collection-grid
```

### Rules
- **Codex** works on feature branches off `development`
- **Shopify Ops Lead** merges feature branches into `development` after QA
- **CEO** approves merges from `development` to `main`
- **Founder** approves deployment from `main` to live theme
- **Never** push directly to `main` or live

### Deployment Flow
1. Codex builds on feature branch
2. Shopify Ops Lead tests on dev theme
3. CEO reviews for brand alignment
4. Founder approves
5. Shopify Ops Lead deploys to live theme
6. Post-deploy check: visual + functional QA
7. Close ticket and log in weekly board review

---

## 12. CEO Agent Audit Protocol

The CEO audits every agent continuously, not in annual reviews. This is built into the daily and weekly rhythms.

### Daily Audit (5 minutes)
- Review each agent's daily digest entries
- Flag any output that deviates from brand voice, technical standards, or decision rights
- Send correction note or kudos via Paperclip

### Weekly Audit (Monday board review)
- Review each agent's Q1/Q3 outputs from the prior week
- Score each agent on: quality, speed, adherence to brief, escalation appropriateness
- Adjust quadrant assignments or decision rights if an agent is consistently over or underperforming

### Monthly Audit
- Deep-dive into one agent's work product
- Compare outputs against brand standards and business goals
- Update role definitions or retrain agents as needed

### Audit Triggers (immediate review)
- Founder complaint or question about an agent's output
- Two consecutive Q3 tasks requiring rework
- Any Q4 item that escaped the "delete" filter
- Agent escalates outside its defined authority

---

## 13. Open Questions & Approval Gates

This document is a draft. The following items require founder response before the org can go live:

1. **Store access:** Shall we operate under a collaborator account only?
2. **Communication channels:** Which channels may agents use to reach you? (Email, WhatsApp, IG DM, all?)
3. **Brand assets:** Do you authorize the desktop kimono image as the primary brand visual?
4. **Pricing verification:** Are the master brief price points still current?
5. **Inventory counts:** What are the actual incoming inventory numbers?
6. **Marketing budget:** What is the approved monthly marketing budget?
7. **Ambassador program:** Do you approve the 10-buyer / €44 unit economics model?
8. **24/7 preferences:** Daily digest, weekly summary, or urgent alerts only? Do-not-disturb hours?
9. **Approval threshold:** All marketing/content changes, or only irreversible ones?

> **Reference:** See `docs/OMCelebration-questions.md` for the full question list.

---

## 14. Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-08-11 | OMCelebration CEO | Initial draft |

---

*This document is the single source of truth for the OMCelebration Paperclip operating system. Any changes to roles, decision rights, or workflow must be logged here and communicated to all agents.*
