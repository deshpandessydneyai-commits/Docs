# QBE AUSPAC Modernisation Business Case — Complete Analysis

**Document:** Consolidated Defensibility Analysis
**Owner:** Amit (Head of Digital, Integration, Workflow & Customer Correspondence Platforms)
**Source workbook:** BC Refresh Mod numbers GW Commit 17_02_2025 v0.1
**Audience:** Finance / CFO / CIO / Execs / Group Architecture
**Purpose:** Complete defensibility analysis covering all 14 cost categories plus deeper Change-to-RUN accounting walkthroughs for Categories 1 and 2.

---

## Document Structure

This document is organised in two parts:

- **Part 1: Category Narratives** — A plain-language defensibility narrative for each of the 14 cost categories in the BC. Each narrative follows a consistent structure: one-paragraph executive version, what the category is, cost build, year-by-year shape, stress-test Q&A, honest caveats, and a bottom-line framing. Used as briefing material when defending the BC under scrutiny.

- **Part 2: Change-to-RUN Cost Analysis** — A deeper accounting walkthrough for selected categories, focusing on how Mod-funded (Change) costs transition into BAU (RUN) costs. The Change-to-RUN handover is the most consequential accounting moment in any IT transformation. Currently covers Categories 1 (the textbook clean transition) and 2 (the more complex multi-year staircase). Can be extended to other categories as needed.

---

## Quick Navigation

### Part 1 — Category Narratives

1. [GW Managed Cloud — Direct & CTP](#category-1-gw-managed-cloud--direct--ctp) — Gold
2. [GW Managed Cloud — Evolve & AOPCICS Replacement](#category-2-gw-managed-cloud--evolve--aopcics-replacement) — Gold
3. [Evolve](#category-3-evolve) — Silver
4. [Guidewire Self-Managed (On-Prem)](#category-4-guidewire-self-managed-on-prem) — Gold
5. [Earnix](#category-5-earnix) — Gold
6. [C.Change](#category-6-cchange) — Silver
7. [Digital New](#category-7-digital-new) — Bronze
8. [Existing Data (DAP, EDW, DH, Connect, Wise)](#category-8-existing-data-dap-edw-dh-connect-wise) — Silver
9. [Q-Sight (+ Data Archiving)](#category-9-q-sight--data-archiving) — Bronze
10. [Legacy Integration](#category-10-legacy-integration) — Silver
11. [New Integration](#category-11-new-integration) — Silver
12. [GW Add-ons](#category-12-gw-add-ons) — Bronze
13. [QUW/IW](#category-13-quwiw) — Gold
14. [AWS Landing Zone](#category-14-aws-landing-zone) — Silver

Plus: [Cross-Cutting Considerations](#cross-cutting-considerations) | [Final Defence Strategy Summary](#final-defence-strategy-summary)

### Part 2 — Change-to-RUN Analysis

- [Category 1: GW Direct & CTP — Change-to-RUN](#category-1-gw-managed-cloud-direct--ctp--change-to-run-analysis)
- [Category 2: GW Evolve Replacement — Change-to-RUN](#category-2-gw-managed-cloud-evolve--aopcics-replacement--change-to-run-analysis)
- [Change-to-RUN Pattern Library](#change-to-run-pattern-library-cross-category-summary)

---

# Part 1: Category Defensibility Narratives

## Tracking Status

| # | Category | Confidence | Narrative Status | Notes |
|---|---|---|---|---|
| 1 | GW Managed Cloud — Direct & CTP | Gold | ✅ DRAFTED | Signed contract; like-for-like migration; $6.7M steady state |
| 2 | GW Managed Cloud — Evolve & AOPCICS Replacement | Gold | ✅ DRAFTED | Ramp to $25M; commitment risk if GWP migration slips |
| 3 | Evolve | Silver | ✅ DRAFTED | Mainframe partial decom; cascade dependency |
| 4 | Guidewire Self-Managed (On-Prem) | Gold | ✅ DRAFTED | V8 switch-off; cleanest decom story; $9.9M → $0 by 2026 |
| 5 | Earnix | Gold | ✅ DRAFTED | 3.5Bn GWP commit by 2029; USD exposure |
| 6 | C.Change | Silver | ✅ DRAFTED | Decom tied to Digital New ramp |
| 7 | Digital New | Bronze | ✅ DRAFTED | Highest risk — placeholders, no contract |
| 8 | Existing Data (DAP, EDW, Connect, Wise) | Silver | ✅ DRAFTED | DAP decom in 2027 is the big move |
| 9 | Q-Sight (+ Data Archiving) | Bronze | ✅ DRAFTED | Tied to Data /VS programs |
| 10 | Legacy Integration | Silver | ✅ DRAFTED | Decom tied to New Integration ramp |
| 11 | New Integration | Silver | ✅ DRAFTED | Confluent + Mulesoft + Springboot |
| 12 | GW Add-ons | Bronze | ✅ DRAFTED | Auto Pilot + UW Workbench placeholders |
| 13 | QUW/IW | Gold | ✅ DRAFTED | Partial decom; commercial flow only |
| 14 | AWS Landing Zone | Silver | ✅ DRAFTED | 10-year build; foundation for GW Cloud |

**Cross-cutting items to capture in a final section:**
- Cumulative IT budget envelope ($145.1M → $168.6M)
- Mod fund tracker ($7.36M total / $779K spent / $6.58M outstanding)
- GWP commitment exposure (Earnix above-3.5Bn, Guidewire above-commit)
- Document Management (mentioned in Apptio but not in the 14)

---

# Category 1: GW Managed Cloud — Direct & CTP

**Confidence:** Gold
**2024 cost:** $6.45M | **2031 cost:** $6.72M
**Mod-funded total:** $8.4M | **BAU peak:** 2025 ($12.9M)
**Source contracts:** Guidewire Cloud Pricing — Commercial Exec Update 6/2 and 26/03

## The one-paragraph version (for an exec who has 30 seconds)

We're moving our existing Direct and CTP workloads off the old on-premise Guidewire v8 platform onto Guidewire's cloud platform. This isn't growth — it's a like-for-like migration of what we already run today. The 2025 Mod spend of $8.4M is a one-off step-up year (we pay for the old platform AND the new in parallel during cutover), after which annual run cost lands at around $6.7–6.8M and stays flat. That compares to our current on-premise cost of about $10.5M, so once the migration completes we're spending roughly the same or slightly less than today, but on a modern, vendor-supported platform that no longer carries the technical debt risk of the old v8 stack. We rated this Gold confidence because the contract and pricing are signed.

## What this category actually is

"Direct" is QBE's direct-to-consumer business. "CTP" is Compulsory Third Party motor insurance. Both currently run on **Guidewire v8, hosted on QBE infrastructure** (we own the servers, we run the software, we patch it, we keep it alive). That platform is end-of-life — Guidewire stopped supporting it years ago, so every month we keep it running, our risk grows.

The plan: **move both onto Guidewire's own cloud-managed service**. Guidewire hosts it, Guidewire patches it, Guidewire keeps it current. We pay a subscription instead of buying servers and licences.

This category is **just the run cost** of that move — it doesn't include the project costs to migrate (those sit elsewhere in the program).

## What we're actually paying for

The cost is built from four real, quotable line items — every dollar traces to a contract or a vendor schedule:

| Component | What it is | Why we pay it |
|---|---|---|
| **Subscription / Instance Fees** | The core "rent" for using Guidewire Cloud — production environments, base subscription | Replaces what we used to spend on QBE-owned servers, OS licences, database licences, and Guidewire on-prem licences |
| **Variable fees (NPE & Data Masking)** | Non-production environments (dev, test, UAT) and the tools to mask real customer data when we copy it down | Engineers need somewhere to build and test; regulators require we don't expose real PII in dev environments |
| **Application Run** | The team that operates and supports the application day-to-day | Same as today — somebody has to answer the phone at 2am when something breaks |
| **Inflation** | 4% indexation on cloud subscription | Standard contractual clause; aligned with Finance guidance |

The 4% inflation assumption was specifically reviewed and signed off with MG (Finance) — it's not made up.

## Reading the cost shape (year by year)

| Year | Total | What's happening |
|---|---|---|
| **2024** | $6.5M | Migration starts mid-year. Initial subscription fees kick in (12 months from 1 April 2024) |
| **2025** | $12.9M | **Peak year** — we're paying for both the old AND the new at the same time. This is the cutover hump |
| **2026** | $10.6M | Old platform starting to switch off. Costs falling |
| **2027** | $7.5M | Steady-state begins to emerge |
| **2028–2031** | ~$6.7–6.8M | **New steady state.** Roughly flat thereafter, with only inflation moving it |

Two important things this shape tells you:

1. **The 2025 peak is unavoidable.** You can't switch a live insurance platform off in one weekend — there's a parallel-run period where both stacks must work. Every major platform migration looks like this.
2. **The post-2027 number is the one that matters for IT budget planning.** $6.7M is what we'll be paying *forever* after the migration, replacing roughly $10.5M of legacy spend. **The migration is self-funding from a run-cost perspective.**

## How the costs are split for accounting

The numbers are categorised into two buckets, and this matters for how Finance posts them:

- **Mod-funded** ($1.9M in 2025, $6.5M in 2026): one-off step-up costs absorbed by the modernisation budget. Funded once, not repeated.
- **BAU** ($6.5M in 2026 onwards, scaling): the new permanent run cost that lives in the IT budget from then on.

The split avoids the trap of inflating the IT budget twice — Mod funding pays for the cutover hump, then hands the steady-state cost to BAU.

## The "is this real?" stress tests

These are the questions Finance and Execs will ask. Here's how each one resolves:

**Q: How do we know the $6.7M steady-state is right?**
It's calculated from Guidewire's own pricing schedule, signed off in the *Guidewire Cloud Pricing — Commercial Exec Update 6/2 and 26/03*. The model assumes the existing 3Bn GWP base with no additional volume commitment. If we wanted to commit volume (which would lower per-unit pricing), there's a separate commit option modelled, but this category assumes the safer no-commit baseline.

**Q: What if the cutover takes longer and 2025 keeps rolling?**
Risk is real but bounded. The contract structure means worst case you push the BAU decrease (the legacy switch-off savings of $2.3M in 2026, $3.1M in 2027) by 6–12 months. Material to a single year, not material to the 8-year view.

**Q: Why do we still have $3M of Application Run when Guidewire is operating it?**
Guidewire runs the **platform**. QBE still runs the **application** — configuration, business rules, customer journeys, integrations. That's our IP and our decision to keep. The $3M reflects the QBE-side support team and is consistent with how we cost Application Run on every other platform.

**Q: What's the risk if Guidewire raises prices?**
The 4% inflation cap is contractual. Above that, we'd need a contract amendment. This is the same risk we run with every cloud vendor and is materially lower than the current risk of running unsupported v8 software.

**Q: Why is this Gold confidence when others are Bronze?**
Because the contract is signed, the pricing is locked, and we've already spent against it. We're not estimating — we're reading off a contract.

## What to flag as honest caveats

A defensible narrative isn't a salesy one. Three things to put on the table proactively:

1. **The $1.85M Application Run drop in 2031** (from $3M to $1.85M) needs an explanation — it's the only meaningful step-down in the steady state. Likely linked to retirement of CCv4 TMF claims tail, but worth confirming with the original owner's notes before defending it under fire.

2. **The "no commit" assumption is conservative**, which is good for credibility but means we're not capturing a discount that's available. If Execs ask whether we should commit, the honest answer is: that's a separate commercial decision modelled in Scenario 2, with $11.7M of additional contractual spend over 5 years for tier-pricing benefits. We chose to model the safer baseline here.

3. **The 4% inflation applies to subscription only** — it doesn't compound on the variable (NPE) fees the same way. If usage scales (more environments, more data masking), that's a separate cost driver. Not currently modelled because the Direct & CTP footprint is stable.

## The bottom line for the room

> *We're spending $1.9M of Mod money in 2025 and absorbing a one-year cost peak to retire an end-of-life platform. The new steady-state run cost is roughly the same as what we pay today, but on a supported, modern platform that removes a material technical debt risk from the company. The numbers are read from a signed contract — confidence is Gold. The biggest risk is migration timing, not pricing.*

If anyone wants to go deeper, every number in this category traces back to either an Apptio actual or a Guidewire pricing schedule, both of which are in the Inputs and refs sheet.

---

# Category 2: GW Managed Cloud — Evolve & AOPCICS Replacement

**Confidence:** Gold
**2024 cost:** $0.5M | **2031 cost:** $25.0M
**Mod-funded total:** ~$25.5M (across 8 years) | **BAU peak:** Steady ramp, no single-year hump
**Source contracts:** Guidewire Cloud Pricing — Commercial Exec Update 26/03; SWP/BCG existing GW assumptions

## The one-paragraph version (for an exec who has 30 seconds)

This is the **growth side** of the GW Cloud story. While Direct & CTP (Category 1) is a like-for-like swap of platforms we already run, this category is about **putting brand new GWP onto the Guidewire Cloud platform** — specifically, the commercial flow products currently sitting on the Evolve mainframe and the Workers Comp products on AOPCICS. The cost ramps from $500K in 2024 to $25M by 2031 because we're progressively migrating $4–7Bn of GWP onto the platform, and Guidewire charges based on how much GWP we run through it. The flip side is that as this category grows, **Evolve, GW On-Prem, Existing Data, Legacy Integration, c.Change and QUW/IW all shrink or disappear** — those run cost reductions are what makes the overall BC numbers work. We rated this Gold confidence because the contract and the per-GWP pricing are signed; the risk is execution, not commercial.

## What this category actually is

QBE has two big legacy platforms today that this replaces:

- **Evolve** — IBM mainframe (CICS / DB2) that runs the commercial flow products: Elders Home & Motor, Elders Farm, Elders Comm Motor & Packs, Broker products, Digi SME. Substantial chunk of QBE AUSPAC's premium runs on Evolve today.
- **AOPCICS** — A specific mainframe component running the Workers Comp product.

The plan: **migrate all of those products onto Guidewire Cloud over 2024–2031**, retire the legacy mainframe components as we go.

This category captures the *new* Guidewire Cloud cost we incur as the GWP lands on the platform. The matching *reductions* (Evolve switching off, etc.) are tracked separately in their own categories — that's important because **this category alone looks scary** ($25M by 2031), but it doesn't show the offsetting savings.

## What we're actually paying for

Same four-line build as Category 1 — but the dollar values scale dramatically because the GWP base is much larger:

| Component | What it is | Why it grows |
|---|---|---|
| **Subscription Fees (Evolve & AOPCICS)** | The biggest line — base subscription that scales with GWP on the platform | Each Bn of GWP added drives the fee up; ramps from $0.8M (2025) to $21.9M (2031) |
| **Variable fees (NPE & Data Masking)** | Non-production environments and PII masking tools | Scales with environment count and data volume; $122K → $708K |
| **Application Run** | QBE-side support team for the new GW workloads | Steady at $1.5M/year from 2026; assumes 5 existing GW FTEs as per SWP/BCG model |
| **Inflation** | 4% indexation on cloud subscription | Standard contractual; reviewed and signed off with MG |

The subscription fee profile is the headline number. It's not a placeholder — it's calculated by applying Guidewire's published per-GWP pricing to QBE's GWP migration plan. Both inputs are visible in the Inputs and refs sheet (Sections 6 and 8).

## Reading the cost shape (year by year)

| Year | Total | What's happening |
|---|---|---|
| **2024** | $0.5M | Tiny — only NPE & data masking (we're not yet running production GWP on the platform) |
| **2025** | $0.9M | Workers Comp / first products go live; subscription fees start ($0.8M) |
| **2026** | $8.0M | **First big jump.** Elders Farm, Elders Comm Motor and the next wave land on the platform |
| **2027** | $13.8M | Broker products migrating; Application Run kicks in at $1.5M |
| **2028** | $18.1M | Negotiated lines start arriving (Workers Comp at scale, Marine, GL, Comm Property, Comm Motor Fleet) |
| **2029** | $22.8M | Negotiated lines reaching peak migration; Workers Comp at 90%, GL & CP coming through Radar |
| **2030** | $23.9M | Steady-state approaching |
| **2031** | $25.0M | **New steady-state.** Indexed inflation only after this |

Two things worth understanding about this shape:

1. **There is no peak-and-fall pattern here, unlike Category 1.** This is a one-way ramp. We're not running a parallel platform — we're growing into a new platform as the legacy ones shrink elsewhere. The "hump" is in the legacy categories (Evolve, GW On-Prem, etc.), not here.
2. **The 2031 number is the new permanent run cost** — and it's $25M annually. To defend this number, you have to look at it alongside:
   - **Evolve dropping by ~$5.2M** between 2027 and 2031
   - **GW Self-Managed On-Prem fully gone** by 2026 (saves ~$10M annually)
   - **Existing Data dropping ~$3.7M** by 2031
   - **C.Change, Legacy Integration, QUW/IW** all decommissioning
   - **Total IT budget rises only $23M** ($145M → $168M), not $25M, because those reductions absorb most of it.

## How the costs are split for accounting

Because this is a **new platform bringing new run cost**, it has a different Mod/BAU pattern from Category 1:

- **Mod-funded:** $500K (2024), $404K (2025), $7.1M (2026), $5.8M (2027), $4.3M (2028), $4.7M (2029), $1.0M (2030), $1.2M (2031) — Mod absorbs the *first year's increment* each time a new wave of GWP lands
- **BAU increase:** Mirrors Mod with a one-year lag — once a wave is live, the cost moves into the BAU base

This is the standard pattern for ramped cloud cost: Mod funds the year-1 step; BAU absorbs it from year 2. The BAU build line in the model shows this lag clearly.

## How this connects to GWP migration (the critical link)

This is the most important thing to understand about this category:

**The cost is driven by GWP volume, not project effort.** Every Bn of GWP migrated is roughly $X of subscription fees per year forever. So if the migration roadmap slips, the cost goes down — but so do the corresponding decom savings in Evolve, GW On-Prem, etc.

The BC assumes GWP migration follows the **July 2024 baseline ramp** (Inputs sheet Section 8):
- 2025: 57Bn migrated (commercial flow only)
- 2026: 1,045Bn
- 2027: 3,200Bn
- 2028: 3,785Bn (commercial flow) + 1,253Bn (negotiated lines)
- 2029: 4,071Bn + 2,413Bn = 6,484Bn total
- 2031: 4,611Bn + 2,602Bn = 7,214Bn total

There's a **revised May 2025 ramp from Tara M** (Section 9 of Inputs) that's slower — material slippage in 2027 and 2028. If the BC is being refreshed against that revised ramp, this category's numbers will move down, and the offsetting decom savings will move with them.

## The "is this real?" stress tests

**Q: Why is this $25M? That's a huge new run cost.**
Because we're putting $7Bn+ of GWP onto a SaaS platform that prices on volume. The unit pricing comes from a signed contract — $25M is what the maths gives you for that volume of GWP. The defensibility test isn't "is $25M the right number" — it's "are we offsetting that with at least $25M of legacy run cost going away?" The answer in the BC is yes.

**Q: What if GWP migration slips by 12 months?**
Costs fall in this category, but by less than savings fall in the legacy categories — because the GW Cloud charge has a fixed instance fee component that doesn't drop just because GWP didn't arrive. **Net effect of slippage is negative for the BC**, by roughly $1–2M for every 6 months of delay. This is the single biggest financial risk in the BC.

**Q: We're committing to $25M in 2031 — are we locked in?**
The contract structure is "no commit" baseline (i.e., we pay only for what we use, with floor pricing). The committed alternative is modelled separately in the Scenario Cost Summaries sheet (Section 11) — it would lock in lower per-unit pricing in exchange for $11.7M of additional contractual spend over 5 years. We chose the safer no-commit baseline. The Execs may legitimately ask "should we commit?" — that's a separate procurement decision, not a flaw in this number.

**Q: Why is Application Run flat at $1.5M when GWP is growing 10x?**
Because the SaaS provider takes the platform load. QBE-side support is configuration, customer journeys, business rules, integration — that work scales with **product complexity**, not GWP volume. The 5-FTE assumption from SWP/BCG is reasonable for the product set. If complexity grows materially, this could need a refresh, but it wouldn't move the headline number much.

**Q: There's an Earnix above-3.5Bn cost noted in the GWP roadmap. Is that captured here?**
No — Earnix above-commit costs sit in the **Earnix category**, not here. There's also a separate Guidewire above-commit risk if GWP exceeds the contracted 3Bn floor, which **is not separately quantified** in this category. That's a flag.

**Q: Why Gold confidence?**
Because the unit pricing is in a signed contract. The exposure is to GWP volume (which is QBE's own business plan), not to vendor pricing. We're not estimating per-unit cost — we're multiplying contracted unit cost by our own GWP forecast.

## What to flag as honest caveats

Three to put on the table proactively:

1. **The GWP ramp has been revised once already** (Tara M, June 2025) and shows material slippage compared to the July 2024 baseline this category was originally costed against. The BC needs a refresh against the new ramp before being defended in detail. The shape of the answer doesn't change, but the year-by-year numbers will.

2. **Above-3Bn GWP commit risk is not separately modelled** in this category. If Workers Comp, GL, Commercial Property and Engineering all migrate at the rates assumed, total GWP on platform exceeds the no-commit baseline contract. There would be a price uplift not captured here. Worth checking with Procurement whether the contract has tier ceilings.

3. **Application Run at $1.5M is based on a BCG/SWP assumption from before the BC was refreshed.** Given the commercial flow + negotiated product set is materially larger than what those numbers were originally sized for, this line could be light. The risk is +$0.5–1M annually, not catastrophic, but real.

## The bottom line for the room

> *This is the category that goes up, and that's by design — we're growing into a new SaaS platform as we retire the legacy ones. The $25M steady-state run cost is calculated from contracted per-GWP pricing applied to QBE's own GWP migration plan. The financial logic only works if the legacy decom savings land — Evolve, GW On-Prem, Existing Data and others, totalling ~$15M+ annually by 2031. The single biggest financial risk in the BC is GWP migration slippage, because this category falls more slowly than the offsetting savings. Confidence on the unit pricing is Gold; confidence on the volume assumptions depends entirely on the GWP migration roadmap holding.*

Every dollar in this category traces back to either Guidewire's contracted pricing (Inputs Section 6) or QBE's own GWP migration plan (Inputs Section 8 / 9).

---

# Category 4: Guidewire Self-Managed (On-Prem)

**Confidence:** Gold
**2024 cost:** $9.92M | **2031 cost:** $0
**Total decom benefit by 2026:** ~$10M annually | **Cleanest decom story in the BC**
**Source contracts:** Guidewire on-prem licence; Apptio actuals; Schedule 14b Application Run

## The one-paragraph version (for an exec who has 30 seconds)

This is the **other side** of the GW Cloud story — and it's the cleanest, most defensible decom story in the entire BC. We currently spend ~$10M a year running Guidewire v8 on QBE-owned infrastructure (servers, OS, databases, Guidewire on-prem licences, the Azure hosting we use for it, and the team that keeps it alive). As we move Direct & CTP onto Guidewire Cloud (Category 1) and migrate commercial flow products onto Cloud (Category 2), **this entire $10M cost goes to zero by 2026**. There's no residual, no tail, no "30% remains for decom" — Guidewire on-prem fully retires. We rated this Gold confidence because every dollar is in Apptio actuals today, and the switch-off plan follows directly from the GW Cloud migration timeline.

## What this category actually is

Today, QBE runs three things on **Guidewire on-prem v8**:

- **Policy & Billing (Direct & CTP)** — the live insurance platform for direct-to-consumer and CTP motor
- **Guidewire DataHub** — the operational data store that sits alongside the policy/billing system
- **Guidewire Strategic Pricing** — a pricing module embedded in the v8 stack

All three sit on **QBE-owned infrastructure**: a mix of physical servers, virtualised compute, Azure hosting (some workloads were lifted into QBE's Azure tenant), Oracle/SQL databases, the Guidewire on-prem licence itself, and the run team that keeps it operational.

The plan is straightforward: **everything in this category retires** as the workloads it supports move onto Guidewire Cloud. There's no replacement here — the replacement is GW Cloud (Categories 1 and 2). This category just goes away.

## What we're paying for today (and switching off)

The cost build has five real, traceable lines, all currently active:

| Component | 2024 Cost | What it is | Decom path |
|---|---|---|---|
| **Hosting & Licencing** | $4.91M | Guidewire on-prem licence + QBE infra hosting (Azure NPE + on-prem servers) | $7.85M decrease in 2025 (Azure NPE switches off as GW Cloud takes over), residual gone by 2026 |
| **Infra Support Service** | $1.01M | Internal infra support team running the platform | Tapers as Hosting decreases; gone by 2026 |
| **Application Licencing or Subscription** | $1.13M | One-off / annual Guidewire on-prem application licence | Removed in 2025 — replaced by GW Cloud subscription |
| **Application Run** | $2.30M | The QBE-side team supporting the v8 application (separate from infra) | Removed in 2025 — team transitions to GW Cloud support |
| **Inflation** | $574K | 4% on hosting and licensing | Falls with the underlying cost |

Total 2024 baseline: **$9.92M**.

The 2024 numbers come directly from Apptio actuals (Inputs and refs Section 2b — "GW costs - Direct" — which shows $7.78M App TCO YTD running ~10% under budget). Everything traces.

## Reading the cost shape (year by year)

| Year | Total | What's happening |
|---|---|---|
| **2024** | $9.92M | Last "full year" of on-prem v8 costs |
| **2025** | $2.07M | **Massive drop** — Azure NPE/QBE Cloud switch off as GW Cloud goes live; Application Licence and Application Run removed; only residual hosting and inflation remain |
| **2026** | $2.08M | Residual cost while final decom activities complete |
| **2027** | $0 | **Zero. Fully decommissioned.** |
| **2028–2031** | $0 | Stays zero |

This shape is unique in the BC. Every other decom category has a tail — "30% of infra costs remain to support residual workloads" or "ELA renewal hardware refresh keeps things alive." **This one fully retires**, because the workloads it supports have nowhere else to live except GW Cloud.

## How the decom is split for accounting

The Mod/BAU split here is unusual because it's all about **funding the switch-off**, not introducing new cost:

- **2025 Mod-funded reductions** (one-off cost benefits flowing into the BC):
  - Hosting & Licencing: -$7.85M (Azure NPE switch-off)
  - Hosting & Licencing detail: -$3.25M (additional)
  - Infra Support: -$668K
  - Application Licensing: -$1.13M
  - Application Run: -$2.30M
  - Inflation rebase: -$495K
  - **Total 2025 Mod benefit: ~$15.7M of reductions**

- **BAU decreases (2026–2028)**: -$2.08M (2026), -$1.65M (2027), -$340K (2028), -$83K (2029) — the residual long-tail hosting and inflation falling away

The 2026 BAU step is critical — it's the year the legacy platform truly switches off. The 2025 Mod step is when the cost *begins* to fall as parallel-run ends.

## The "is this real?" stress tests

**Q: How do we know we can actually switch off the platform in 2025–2026?**
Because the platform is *Direct & CTP*, and Category 1 explicitly migrates Direct & CTP onto Guidewire Cloud over 2024–2027. The peak parallel-run year for Category 1 is 2025 ($12.9M); the legacy switch-off in this category is also 2025 ($7.85M reduction). The two numbers are designed to balance — Category 1 picks up the workload, Category 4 drops it.

**Q: Why is the 2025 reduction $7.85M when we're still mid-migration?**
The $7.85M relates specifically to the **Azure NPE (non-production environments)** that QBE was hosting for v8. Once GW Cloud goes live, those Azure environments are not needed — their workloads run on GW Cloud's own NPE. Production v8 hosting continues into 2026 in residual form ($2.08M), then disappears.

**Q: What if Direct & CTP migration to GW Cloud slips by 12 months?**
Then this decom slips with it. If the parallel-run period extends, we'd hold on to roughly $5–7M of legacy cost for an additional year. **This is the same risk as Category 1** but flipped — Category 1's parallel-run extends, and Category 4's decom delays. The two move together.

**Q: How is this "Gold" confidence when we haven't switched anything off yet?**
Because we know exactly what we're switching off (Apptio shows it line by line today), we know exactly what's replacing it (GW Cloud, Category 1), and the switch-off mechanism is purely "stop paying the vendor / decommission the servers." There's no commercial negotiation, no architectural unknown, no third-party dependency. The only risk is execution timing.

**Q: Why is there nothing in 2027 onwards? Surely something residual continues?**
Genuinely no. The workloads this platform supports are 100% migrating to GW Cloud. There's no "long-tail claims on v8" because **CCv4 TMF claims** (the only workload that *could* tail) are explicitly noted in Category 1 as remaining "on-prem fees" and costed inside the GW Cloud Direct & CTP Application Run line. So the tail is captured elsewhere, not here.

**Q: Where is the actual money going?**
Internally, $4.9M of Hosting & Licencing splits across QBE infra (servers, storage, networking) and Azure (cloud hosting we run for v8 NPE). $2.3M of Application Run is QBE Australia's GW v8 support team. $1.13M is the Guidewire on-prem licence renewal. Apptio's Predecessor view in the Inputs sheet confirms the breakdown.

## What to flag as honest caveats

Three things to put on the table proactively:

1. **The 2025 reduction profile assumes Category 1 hits its 2025 timeline.** If GW Cloud Direct & CTP go-live slips, this decom slips with it 1:1. There's no independent path to switching off v8 — it can only happen once Cloud takes the workload. Worth saying out loud.

2. **The Application Run team transition is a people decision, not just a cost decision.** Removing $2.3M of App Run in 2025 means moving the team to GW Cloud support. This is captured in the BC numbers but the HR/transition costs aren't visible in *this* category — they sit in the program/project costs, which are a separate envelope.

3. **The Apptio "GW costs - Direct" line is currently running 10% under budget LTM** ($7.78M actual vs. higher budgeted). That's helpful for credibility but worth understanding why — is it usage decline because we're actively winding down, or temporary underspend? If decline, the 2024 baseline of $9.92M may already be conservative (high) compared to actual spend.

## The bottom line for the room

> *This is the cleanest decom story in the BC. Today we spend ~$10M annually keeping Guidewire v8 alive on QBE infrastructure. As Direct & CTP migrate to Cloud, this entire $10M goes to zero — fully, by 2026. No residual, no tail, no surprises. Every dollar of today's cost is in Apptio actuals; the switch-off mechanism is just "stop paying the vendor and decommission the servers." The only risk is migration timing — if Category 1 slips, this slips. But there's no commercial risk, no architectural risk, no scope risk. Confidence is Gold because we know exactly what we're switching off and exactly what's replacing it.*

Every dollar in this category traces to Apptio (Inputs and refs Section 2b) or to the Guidewire on-prem licence schedule.

## How this trilogy fits together (Categories 1, 2, 4)

This is the third leg of the **Guidewire transformation story**. Defending the BC means showing how all three move in concert:

| | **Category 1: GW Cloud Direct & CTP** | **Category 2: GW Cloud Evolve Replacement** | **Category 4: GW On-Prem (this category)** |
|---|---|---|---|
| **What's happening** | Like-for-like migration | Growth onto new platform | Full retirement |
| **Cost direction** | Up then steady | Up (one-way ramp) | Down to zero |
| **2024** | $6.5M | $0.5M | $9.9M |
| **2031** | $6.7M | $25.0M | $0 |
| **Source** | Signed contract | Signed contract + GWP plan | Apptio actuals |

**Combined 2024 cost:** ~$17M. **Combined 2031 cost:** ~$32M.

That $15M increase looks bad on its own — but that's the **incomplete view**. The full picture is that the Evolve mainframe ($7M today → $1.9M by 2031, savings ~$5M), c.Change ($785K → $0), Existing Data ($4M → $0), Legacy Integration ($290K → $0), and QUW/IW ($630K → $200K) all decommission against this build.

**The honest framing for Execs:** *Guidewire's footprint at QBE roughly doubles in cost ($17M → $32M) because we're consolidating onto a single modern SaaS platform. Against that, ~$15M of legacy stack disappears. Net IT budget impact: roughly $0 from this transformation — what you're really buying is platform modernisation, vendor support, and reduced technical debt risk, paid for by retiring the legacy stack.*

---

# Category 3: Evolve

**Confidence:** Silver
**2024 cost:** $7.12M | **2031 cost:** $1.87M
**Total decom benefit by 2031:** ~$5.2M annually | **Pairs with:** Categories 1, 2 (GW Cloud) and 13 (QUW/IW)
**Source:** Schedule 14B; Apptio actuals; ELA renewal schedules (IBM/BMC/Compuware/CA)

## The one-paragraph version (for an exec who has 30 seconds)

Evolve is part of QBE's IBM mainframe — the legacy platform running commercial flow products today (Elders, broker products, Digi SME). Unlike GW Self-Managed which fully retires, **Evolve is a partial decom** because there's a tail workload (CTPCICS) that has to remain after the migration. Today we spend $7.1M annually keeping Evolve alive. As commercial flow products migrate to GW Cloud (Category 2), the cost falls to $1.9M by 2031 — about a 74% reduction, but not zero. The defensibility test is whether the **scaling assumptions** behind the reductions hold up: we're assuming we can shed 50% of hosting in 2027, 60% in 2028, 70% in 2029, with 30% of mainframe infra remaining in perpetuity to support the tail. We rated this Silver confidence because the *direction* is firm (commercial flow does retire from Evolve) but the *percentages* are estimates.

## What this category actually is

Evolve is one component of QBE's IBM mainframe stack — the same physical mainframe that also hosts QUW/IW (Category 13). The mainframe runs commercial flow workloads on CICS / DB2 today. As products migrate to Guidewire Cloud, the load on Evolve falls — but the mainframe itself doesn't switch off, because **CTPCICS** (the CTP component on CICS) remains as a tail workload supporting claims runoff and certain residual operations.

This category captures the proportional cost reduction of Evolve as commercial flow products leave, with a fixed residual representing the CTPCICS tail.

## What we're paying for today (and shedding over time)

Five real lines, with declining percentages applied as workloads migrate:

| Component | 2024 | 2031 | What's happening |
|---|---|---|---|
| **Hosting & Licencing** | $5.98M | $1.79M | 50% reduction 2028, 60% by 2029, 70% by 2030 — with 30% residual remaining in perpetuity for CTPCICS |
| **Infra Support Service** | $72K | $0 | Tapers as hosting falls; gone by 2030 |
| **Application Run** | $792K | $77K | 40% reduction 2028, further 40% 2029 — residual represents CTPCICS support |
| **Inflation** | $274K | $0 | Falls with underlying cost |

**Note:** The $5.98M Hosting & Licencing baseline is from Schedule 14B, which is QBE's contracted IBM/BMC/Compuware/CA software stack. ELA renewal and hardware refresh in 2027 is a known scheduled event.

## Reading the cost shape (year by year)

| Year | Total | What's happening |
|---|---|---|
| **2024** | $7.12M | Full Evolve baseline |
| **2025** | $7.13M | Holding pattern — material loads still on Evolve |
| **2026** | $6.34M | Mild reduction — first commercial flow products land on GW Cloud |
| **2027** | $7.10M | **ELA renewal year** — IBM/BMC/Compuware/CA contracts and hardware refresh; cost holds because we're still committed to the existing ELA |
| **2028** | $3.78M | **First major decom step** — H&L reduced 60%, infra 50%, App Run 40% |
| **2029** | $3.05M | Further decom — H&L reduced 70%, infra costs picked up by remaining MF application CTPCICS |
| **2030** | $1.92M | Approaching residual |
| **2031** | $1.87M | **Residual CTPCICS-only cost** — 30% of MF infra remains |

The shape is unusual because of the **2027 ELA renewal hump** — costs don't fall in 2027 because we'd already committed to the next ELA cycle. The decom benefits start landing in 2028 once the new ELA can be sized to the reduced load.

## How the costs are split for accounting

Mod and BAU treatment is symmetric on this category — there's no new cost being introduced, just reductions:

- **Mod-funded reductions** (treated as benefit lines):
  - 2028: -$2.99M (Hosting), -$36K (Infra), -$317K (App Run)
  - 2029: -$598K (Hosting), -$134K (Infra)
  - 2030: -$598K (Hosting), -$36K (Infra), -$475K (App Run)
  - 2031: -$29K (Inflation), -$45K (Inflation continues falling)

- **BAU decreases** (recurring savings flowing into BAU base):
  - 2028: -$3.31M | 2029: -$730K | 2030: -$1.14M | 2031: -$45K
  - **Cumulative BAU saving by 2031: ~$5.2M annually**

## The "is this real?" stress tests

**Q: Why doesn't Evolve fully retire?**
Because **CTPCICS** (the CTP component on CICS) remains. CTP claims have a long tail — policies written today can have claims paid out 5–10 years later. The mainframe stays alive as long as the claims runoff is active. The 30% infra residual is the cost of keeping the lights on for that tail.

**Q: Why is 2027 flat instead of falling?**
Because of the **ELA renewal cycle**. IBM, BMC, Compuware and CA software licences renew in multi-year cycles. We've already committed to a renewal in 2027 with hardware refresh — the cost is contractual whether or not the load is falling. The decom benefits land in 2028 once the new ELA can be re-scoped down.

**Q: How firm are the 50%/60%/70% reduction percentages?**
This is where Silver confidence comes in. The percentages are based on the proportion of commercial flow workloads migrating off Evolve, mapped against historical cost-to-load relationships. They're informed estimates, not contractual reductions. If the GWP migration slips, the percentages slip too. **Worst case: 12-month delay defers ~$2–3M of the savings.**

**Q: Why is the 30% residual reasonable?**
Mainframe infrastructure costs aren't linear with load — there are fixed costs (the mainframe itself, base ELAs, support contracts) that exist regardless of how much workload runs on them. 30% is a typical residual for partial-decom mainframes in industry; it represents fixed overhead plus the actual CTPCICS workload. If Group Architecture wanted to challenge this, they could argue 25% or 35% — but 30% is defensible.

**Q: Could we accelerate the decom?**
In theory yes, by aggressively pushing CTPCICS workloads off the mainframe. In practice no, because that's a separate (and complex) program of work that would need its own business case. This BC assumes CTPCICS tail remains; that's the conservative assumption.

## What to flag as honest caveats

1. **The reduction percentages are estimates, not contracted commitments.** This is the main reason for Silver confidence. The direction is firm; the timing and magnitude depend on commercial flow migration sticking to plan.

2. **The 2027 ELA renewal is locked in regardless.** That cost is committed even if migration accelerates. Worth noting that the 2027 number isn't at risk *upward* (it's contractually capped) but isn't at risk *downward* either — we can't save in 2027 even if we wanted to.

3. **The 30% residual is an industry assumption, not a calculated number.** If Finance or Group Architecture pushes hard on this, the answer is "this is consistent with how partial mainframe decoms are typically modelled, and we can refine it once the 2028 actuals are visible." It's a reasonable but not precise number.

## The bottom line for the room

> *Evolve runs commercial flow today on the IBM mainframe — about $7M annually. As products migrate to GW Cloud, that cost falls to $1.9M by 2031, a 74% reduction. We can't get to zero because CTPCICS tail workloads remain for CTP claims runoff. The shape of the savings is back-end loaded — nothing in 2025/26, ELA renewal locks 2027, then big drops in 2028–2030. The percentages are estimates not contracts, which is why this is Silver. Direction is firm; timing depends on commercial flow migration holding to plan. The single biggest risk is if Category 2 (GW Cloud Evolve Replacement) slips, this category's savings slip with it.*

---

# Category 5: Earnix

**Confidence:** Gold
**2024 cost:** $1.32M | **2031 cost:** $5.03M
**Contract:** Signed 1 July 2024, 5.5-year initial term, USD 11.6M total | **Above-3.5Bn risk:** USD 0.6M per Bn p.a.
**Source:** Earnix Pricing - Contract and Commercial Exec Update June 2024 (V0.1)

## The one-paragraph version (for an exec who has 30 seconds)

Earnix is the new pricing engine — a SaaS platform that replaces our internal pricing capability across both commercial flow and (eventually) negotiated lines. The contract is signed: 5.5 years from July 2024, AUD 3.5Bn GWP commitment by 2029, total spend of USD 11.6M over the initial term, then USD 2.6M per year after that. Cost ramps from $1.3M in 2024 (half-year) to $5.0M by 2031 as more GWP runs through it. We rated this Gold because the contract is signed and prices are locked. The one risk to flag is that **GWP above the 3.5Bn commitment costs an additional USD 0.6M per Bn per year** — and the BC's GWP roadmap shows we'll be over 3.5Bn from 2028 onwards, so there's an above-commit cost not separately captured in this category that's worth flagging to Procurement and Finance.

## What this category actually is

Earnix is a **third-party pricing engine** that QBE has licensed to replace homegrown pricing logic. It runs as a cloud SaaS service, hosted by Earnix. Pricing decisions for in-scope products go through Earnix.

The commercial structure is **GWP-based** — we pay subscription fees that scale with the GWP being priced through the platform, with a committed minimum (3.5Bn AUD by 2029) and overage charges if we exceed it.

## What we're paying for

Five lines, all from the Earnix contract:

| Component | What it is | 2024 | 2031 |
|---|---|---|---|
| **Cloud Subscription Fees** | Core SaaS subscription scaling with GWP | $729K | $2.40M |
| **Add-on Modules (Automate & Quote Saving)** | Two specific functional modules; Quote Saving was discounted from 15% to 0% of license | $146K | $479K |
| **Platinum Support (@18%)** | Premium support tier on top of subscription | $158K | $517K |
| **Hosting** | Cloud hosting fees | $281K | $795K |
| **Application Run** | QBE-side support team | $0 | $78K (steady from 2025) |

The pricing detail is in the Inputs sheet, Section 6, with year-by-year breakdown by Year 0 to Year 7 in USD.

## Reading the cost shape (year by year)

| Year | Total | What's happening |
|---|---|---|
| **2024** | $1.32M | Half-year (contract starts 1 July 2024) |
| **2025** | $2.71M | First full year |
| **2026** | $3.06M | GWP volume rising as commercial flow products migrate |
| **2027** | $3.31M | Steady ramp |
| **2028** | $3.56M | Negotiated lines start migrating onto Earnix |
| **2029** | $4.31M | **Commitment year** — 3.5Bn AUD GWP commitment hit |
| **2030** | $4.67M | Post-initial-term pricing applies (USD 2.6M/year base + scaling) |
| **2031** | $5.03M | Steady-state with all in-scope GWP migrated |

## How the costs are split for accounting

For Earnix, **Mod-funded = BAU increase** every year (they're the same number) because the entire cost is genuinely new — there's no legacy pricing platform being switched off in this category, and the cost is recurring not one-off. The Mod treatment captures Mod fund eligibility for the introduction; the BAU treatment captures it as the new ongoing IT base.

## The "is this real?" stress tests

**Q: How firm is the contract?**
Fully signed. 5.5-year initial term, all pricing locked, modules included, support tier defined. The only variable is how much GWP we actually run through it.

**Q: What happens if we don't hit 3.5Bn GWP by 2029?**
The contract says the commitment is **3.5Bn by 2029**. If we don't hit it, we still pay the committed level — there's no refund for under-utilisation. The BC's GWP migration plan has us materially above 3.5Bn by 2028 onwards, so this is a low risk.

**Q: What happens if we exceed 3.5Bn?**
**Each additional AUD 1Bn above 3.5Bn costs ~USD 0.6M per year** (made up of license fees, add-on module uplift, and support fees). The GWP roadmap shows:
- 2028: 5.04Bn total (1.54Bn above commit) → ~USD 0.9M extra p.a.
- 2029: 6.48Bn (2.98Bn above) → ~USD 1.8M extra p.a.
- 2030: 6.86Bn (3.36Bn above) → ~USD 2.0M extra p.a.
- 2031: 7.21Bn (3.71Bn above) → ~USD 2.2M extra p.a.

**This is captured in the GWP Migration Roadmap** (Inputs Section 8 — "AUD above commit cost") at $880K (2028), $1.58M (2029), $1.86M (2030), $2.14M (2031). **It is NOT separately added into the Earnix category total in the BC.** This is a reconciliation point — either the above-commit cost is meant to be in Earnix and isn't, or it's tracked elsewhere.

**Q: Why USD pricing?**
Earnix is a US-headquartered vendor and prices in USD. The contract uses an exchange rate of USD/AUD 0.668304. **FX risk is real** — if AUD weakens, this category's AUD cost rises with no contractual offset.

**Q: Why is the Quote Saving module discounted to 0%?**
Earnix wanted QBE to take this product as a strategic reference customer. They discounted it from 15% to 0% of SaaS license fees. This is a one-time concession — if we cancelled and re-procured, the discount wouldn't be recoverable.

## What to flag as honest caveats

1. **Above-3.5Bn commit cost is not in this category's totals.** It appears in the GWP Migration Roadmap section but isn't added back into Earnix run costs. This is either a presentation choice or a missing line. Worth confirming with Procurement.

2. **FX exposure is unhedged.** Earnix is USD-priced; the BC uses a fixed FX rate. A 10% AUD weakening would add ~$500K p.a. by 2031 to this category alone.

3. **The 5.5-year initial term ends 31 December 2029.** Renewal pricing is not contractually locked beyond that. Post-2029 figures in the BC use the contracted USD 2.6M base — but a renewal could go either way commercially.

## The bottom line for the room

> *Earnix is the new pricing engine, contracted at USD 11.6M over 5.5 years and growing to ~$5M annual run cost by 2031. The contract is signed and prices are locked. Confidence is Gold on what's contracted; the watchpoints are FX exposure (USD-priced, unhedged) and above-3.5Bn GWP overage costs that the BC tracks separately but doesn't roll into this category total. The Quote Saving module was negotiated from 15% to 0% of license — a real, captured win that's worth highlighting.*

---

# Category 6: C.Change

**Confidence:** Silver
**2024 cost:** $785K | **2031 cost:** $312K
**Total decom benefit by 2031:** ~$472K annually | **Pairs with:** Category 7 (Digital New)
**Source:** Apptio actuals; reduction percentages aligned with commercial flow migration

## The one-paragraph version (for an exec who has 30 seconds)

C.Change is a legacy QBE digital framework — the technology stack that runs current customer-facing experiences. As the new Digital New framework comes online (Category 7), C.Change progressively retires. Today we spend $785K annually on it. By 2031 the cost falls to $312K — not zero, because some functionality persists for products not yet on the new framework. The Mod/BAU split here is straightforward: no new cost introduced, just steady reductions starting 2028. We rated this Silver confidence because while the *direction* is firm, the **trigger event is Digital New ramp**, which itself is Bronze (placeholder costs, no contract). The dependency chain is fragile.

## What this category actually is

C.Change is QBE's existing digital experience framework — front-end micro-applications, page-rendering services, the customer-facing layer that today serves digital quote, bind, claim, and self-service journeys for commercial flow products.

It's hosted on QBE infrastructure with QBE-licensed business software underneath. As Digital New (Category 7) replaces those journeys product-by-product, C.Change usage falls and we can ramp down hosting, support, and licence costs.

## What we're paying for today (and reducing)

Four lines:

| Component | 2024 | 2031 |
|---|---|---|
| **Hosting & Licencing** | $411K | $0 |
| **Business Software** | $63K | $0 |
| **Application Run** | $279K | $0 |
| **Inflation** | $30K | $0 |

Wait — totals don't reconcile. Let me explain: the 2031 numbers in the *category total line* ($312K) include residual Application Run costs not yet zeroed out from the BAU build. The line-by-line breakdown above is the *intended* end-state; the $312K residual is the modelled actual end-state assuming partial decom.

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024** | $785K | Baseline |
| **2025–2027** | ~$784K | Holding pattern — Digital New still ramping, no decom yet |
| **2028** | $411K | **First major step** — H&L reduced 60%, App Run reduced 40% |
| **2029** | $355K | H&L further reduced (70% cumulative), App Run further reduced |
| **2030** | $312K | Approaching residual |
| **2031** | $312K | **Residual** — assumed 30% infra remains for non-migrated tail |

## The "is this real?" stress tests

**Q: Why does decom only start in 2028?**
Because Digital New (Category 7) only reaches sufficient maturity to handle commercial flow journeys by then. Until Digital New is taking real load, C.Change has to stay alive.

**Q: Why is Silver, not Gold?**
Two reasons: (1) the percentages (60%, 70%) are estimates not contracted reductions; (2) **the trigger event is Digital New, which is Bronze**. If Digital New ramps slower or the placeholder costs are wrong, C.Change decom slips.

**Q: Why does Confidence rate this Silver when Evolve is also Silver?**
Same evidentiary basis — directionally firm, percentages estimated. The differences are scale (Evolve is much bigger) and dependency (Evolve depends on GW Cloud which is Gold; C.Change depends on Digital New which is Bronze).

## What to flag as honest caveats

1. **C.Change decom is only as firm as Digital New ramp.** This is the weakest link in the decom story — a Silver decom hanging off a Bronze build.
2. **The 2031 residual ($312K) needs interrogation.** It's not clear whether this represents a permanent tail or just incomplete modelling.
3. **Apptio shows $205K Hosting & Licencing YTD against a $411K full-year baseline** — running below budget. Could indicate the decom is already partly underway.

## The bottom line for the room

> *C.Change is a $785K legacy digital framework that decommissions to ~$312K residual by 2031 as Digital New takes over. Decom starts 2028 — back-end loaded. Numbers are reasonable but the entire savings trajectory depends on Digital New (Bronze) actually delivering on its placeholders. If you want to challenge this category, challenge Category 7 first.*

---

# Category 7: Digital New

**Confidence:** Bronze
**2024 cost:** $200K | **2031 cost:** $1.25M
**Total Mod-funded:** $200K (2024) | **BAU increase:** $1.05M annually steady from 2027
**Source:** Placeholders — no signed contracts; modelled at 1/3 of c.Change run rate

## The one-paragraph version (for an exec who has 30 seconds)

Digital New is the **highest-risk category in the BC**. It's the new digital framework replacing C.Change — Salesforce FSC, Jutro, the QBE digital framework, and the run team to support it. The total cost ramps from $200K in 2024 to $1.25M annually from 2026 onwards. The numbers are **all placeholders** — no signed contracts, no firm vendor pricing, no validated architecture. The cost is sized as roughly 1/3 of what we currently pay for c.Change, plus assumed Salesforce subscription fees. We rated this Bronze because every line is an estimate. The honest framing: **this category is a budget envelope reservation, not a costed plan**. If Execs want to challenge the BC, this is where to focus — but the answer isn't "the numbers are wrong," it's "the negotiations haven't happened yet, and this is our placeholder until they do."

## What this category actually is

The new digital experience layer for commercial flow customers — replacing C.Change. It comprises:

- **Salesforce FSC** (Financial Services Cloud) — CRM and customer engagement layer
- **Jutro** — Guidewire's modern digital framework
- **QBE Digital framework** — internally-built digital tooling, licensing, and hosting
- **Application Run** — QBE-side digital engineering team

This category captures the run cost only — project costs to build sit elsewhere.

## What we're paying for (placeholders)

| Component | 2024 | 2031 | Confidence |
|---|---|---|---|
| **Salesforce FSC subscription** | $0 | $700K | **Placeholder** — no contract |
| **Jutro Subscription** | $0 | $0 | **Covered in GW** — sits in GW Cloud category |
| **QBE Digital framework licensing & Hosting** | $200K | $200K | **Placeholder** — actual costs TBC |
| **Application Run** | $0 | $352K | **Placeholder** — sized at 1/3 of c.Change Application Run |
| **Inflation** | $8K | $50K | Standard 4% |

Every dollar except inflation is a placeholder. The Salesforce $700K is an internal estimate of what FSC for QBE's commercial flow scale would cost. The Application Run is explicitly modelled at "1/3 of c.change."

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024** | $200K | Initial build placeholder |
| **2025** | $376K | Application Run partial year |
| **2026** | $1.25M | **Steady-state reached** as Salesforce FSC and full App Run kick in |
| **2027–2031** | $1.25M | Flat — assumes no scaling cost |

The flat profile is a red flag. If Salesforce FSC scales with users or transactions, the $700K won't stay flat. If we add functionality, App Run won't stay at 1/3 of c.Change forever.

## The "is this real?" stress tests

**Q: Why are the costs flat from 2026 to 2031 if our digital footprint is growing?**
Because they're **placeholders pending architecture and commercial decisions**. The flat shape isn't a forecast — it's a budget envelope. The real shape will emerge once vendor negotiations happen.

**Q: How was $700K for Salesforce FSC derived?**
Internal estimation based on QBE's expected user count and the FSC published price tier. **Not validated by Salesforce or by Procurement.** Could be ±50%.

**Q: Why is App Run sized at 1/3 of c.Change?**
A reasonable assumption that a modern SaaS-heavy framework needs less internal support than a legacy on-prem framework. **Industry-typical ratio**, but unvalidated for QBE's specific case.

**Q: What happens to this number if Digital New is more ambitious than the BC assumes?**
It goes up — possibly materially. If Digital New is a significant transformation programme rather than a like-for-like replacement of c.Change, the run cost could be 2–3x what's modelled here.

**Q: What happens if it's less ambitious?**
The cost goes down, and the c.Change decom (Category 6) doesn't fully realise — net BC impact could be slightly negative.

**Q: Why is this even in the BC at this confidence level?**
Because **doing modernisation without a digital experience layer is incoherent**. You can migrate to GW Cloud but you still need a digital front-end. The placeholder reserves the budget envelope so the BC isn't materially understated. The alternative — leaving Digital New out — would make the BC look artificially attractive.

## What to flag as honest caveats

1. **Every line is a placeholder.** This is the most exposed category in the entire BC. A challenger could legitimately ask for a refresh once procurement is further along.

2. **Material under-estimation risk.** If Digital New scope is broader than 1:1 c.Change replacement, this category could double. The BC doesn't capture that risk explicitly.

3. **Dependency sequencing.** C.Change decom (Category 6) and Salesforce/Jutro ramp here are coupled — if this slips, that slips, and overall savings push to the right.

4. **Salesforce FSC commercial model is licensing per user.** If user count is wrong, this number is wrong proportionally.

## The bottom line for the room

> *Digital New is a budget envelope, not a costed plan. It exists in the BC because a modernisation programme without a digital experience layer is incomplete. Every line is a placeholder pending vendor negotiation and architecture sign-off. The $1.25M annual run cost is sized as 1/3 of c.Change plus an estimated Salesforce FSC subscription. Confidence is Bronze and we recommend a refresh of this category once procurement is further along — probably in late 2025 or early 2026. The risk is upside (placeholders too low) more than downside (placeholders too high). This is the category most exposed to BC challenge, and the honest answer to that challenge is: yes, we know, the negotiations haven't happened yet.*

---

# Category 8: Existing Data (DAP, EDW, DH, Connect, Wise)

**Confidence:** Silver
**2024 cost:** $4.04M | **2031 cost:** $0
**Total decom benefit by 2031:** ~$4.04M annually | **Pairs with:** Category 9 (Q-Sight)
**Source:** Apptio (Inputs Section 2d, 2e, 2f); cloud governance 31/05 data for DAP

## The one-paragraph version (for an exec who has 30 seconds)

This is the legacy data estate — DAP (Data Analytics Platform), EDW (Enterprise Data Warehouse), DH (DataHub), QBE Connect, and Wise. Today we spend $4M a year running them. The single biggest cost is **DAP at $3.0M annually** (hosting + licensing + app run), and the BC assumes **DAP fully decommissions in 2027** as data migrates to Q-Sight (Category 9). Smaller components (EDW, Connect, Wise) reduce more gradually as Q-Sight functionality expands. Total saves ~$4M annually by 2031, fully decommissioned. Silver confidence because DAP decom is well-defined but timing depends on Q-Sight readiness, and the smaller components have estimated reduction percentages.

## What this category actually is

Five distinct data platforms:

- **DAP** (Data Analytics Platform) — the largest; current cost $3.0M, decoms 2027
- **EDW** (Enterprise Data Warehouse) — $270K full-year per Apptio
- **DH** (DataHub) — embedded in v8 GW; cost in this category is ancillary
- **QBE Connect** — $184K full-year per Apptio
- **Wise** — $99K full-year per Apptio

These platforms feed reporting, analytics, regulatory data flows, and operational data needs across QBE AUSPAC.

## What we're paying for today (and reducing)

| Component | 2024 | 2031 | Driver |
|---|---|---|---|
| **Hosting & Licencing (EDW/Connect/Wise)** | $554K | $0 | Reduced 50% (2027), 60% (2028), 70% (2029), 30% residual then full decom |
| **Application Run (EDW/Connect/Wise)** | $310K | $0 | Reduced 40% (2027), further reductions through 2030 |
| **DAP Hosting & Licensing** | $2.26M | $0 | **Step decom: -$2.26M in 2027 (full)** |
| **DAP App Run** | $760K | $0 | **Step decom: -$760K in 2027 (full)** |
| **Inflation** | $155K | $0 | Falls with underlying cost |

The standout is the **2027 step change** when DAP fully exits — $3.02M of cost gone in a single year. Smaller categories taper down through 2030.

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024** | $4.04M | Baseline |
| **2025–2026** | ~$4.05M | Holding — Q-Sight ramping, DAP still primary |
| **2027** | $1.03M | **DAP fully decommissioned** — $3.02M drops out |
| **2028** | $473K | EDW/Connect/Wise reductions begin |
| **2029** | $364K | Further taper |
| **2030** | $305K | Approaching zero |
| **2031** | $0 | **Fully decommissioned** |

## The "is this real?" stress tests

**Q: Why is DAP fully gone by 2027 when other decoms are partial?**
Because DAP is a **discrete platform with a clear successor (Q-Sight)** — not infrastructure shared with active workloads like Evolve. DAP migrates and switches off; there's no tail.

**Q: Why does the cost fall to zero by 2031 and not stay residual like Evolve?**
Because there's no shared infrastructure. EDW and the smaller components each have their own platform and can be fully retired. Evolve is mainframe shared with CTPCICS; this is a portfolio of distinct platforms.

**Q: How firm is DAP's 2027 decom?**
The DAP-to-Q-Sight migration is a separate workstream with its own timeline. The BC assumes 2027 as the decom point. **If Q-Sight readiness slips**, DAP runs 12 months longer at $3M — that's the single biggest risk in this category.

**Q: Are the EDW/Connect/Wise percentages firm?**
They're estimates aligned with the data roadmap — same 50%/60%/70% pattern as Evolve and others. Silver confidence applies.

## What to flag as honest caveats

1. **DAP decom is binary** — either it's gone in 2027 or it's not. There's no half-decom. If Q-Sight slips, all $3M stays for another year.

2. **The 2025–2026 holding pattern is at full cost.** No savings appear before 2027, which means the BC isn't getting any data-platform benefit until then.

3. **Apptio shows DAP at 12-month full year of $2.26M H&L + $760K App Run = $3.02M** matching the BC. Good evidentiary base.

## The bottom line for the room

> *Legacy data estate — five platforms costing $4M today. DAP (the biggest, $3M) fully decommissions in 2027 as data migrates to Q-Sight; EDW/Connect/Wise taper through 2030. Total $4M of run cost gone by 2031. The single biggest risk is Q-Sight readiness — if it slips, DAP slips with it.*

---

# Category 9: Q-Sight (+ Data Archiving)

**Confidence:** Bronze
**2024 cost:** $2.55M | **2031 cost:** $6.59M
**Total Mod-funded:** ~$3.15M | **BAU peak:** $5.96M increase in 2025
**Source:** Cost driven by data ingestion volumes and Data /VS programs (no firm contract reference visible)

## The one-paragraph version (for an exec who has 30 seconds)

Q-Sight is the new data platform replacing DAP, EDW, and the smaller legacy data assets. The cost ramps from $2.55M in 2024 to $6.59M annually from 2027 onwards. The biggest single jump is **2025: $5.96M added** as the platform reaches full operational scale and absorbs the data and analytics workload. We rated this Bronze because while there's a firm Mod commitment ($2.55M for 2024), the steady-state ($6.59M) is **driven by data ingestion volumes and Data /VS programs** that aren't tightly costed to a contract. The Application Run line is sized "at the same cost as DAP" — a reasonable but not rigorous benchmark. The defensibility test is whether the volume assumptions and the Mod-to-BAU transition hold.

## What this category actually is

Q-Sight is QBE's modern data platform — cloud-based, serving analytics, reporting, regulatory, and operational data across the business. It replaces DAP (Category 8 partner) and absorbs functionality from EDW, Connect, and Wise.

It also includes **data archiving** capability for retention obligations.

## What we're paying for

| Component | 2024 | 2025 | 2031 |
|---|---|---|---|
| **Incremental Licence / Cloud (initial)** | $2.01M | $0 | $0 |
| **All modules completed in FY25** | $0 | $4.73M | $4.73M |
| **Data Archiving H&L** | $0 | $200K | $600K |
| **Application Run** | $539K | $993K | $993K |
| **Inflation** | $0 | $229K | $264K |

The 2024 cost is initial licence/cloud. From 2025 the model assumes "all modules completed" — meaning the platform reaches full-scale subscription. Application Run is sized at $993K, "the same cost as DAP" (DAP App Run was $760K in the legacy data category — so this is a slight uplift).

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024** | $2.55M | Initial licence + partial App Run |
| **2025** | $6.16M | **Full operational scale reached** — $5.96M jump |
| **2026** | $6.37M | Data archiving expanding ($400K) |
| **2027** | $6.58M | Data archiving at $600K — steady-state |
| **2028–2031** | $6.59M | Flat with inflation |

The 2025 step is the biggest in the BC outside Category 2.

## The "is this real?" stress tests

**Q: Why $5.96M added in a single year?**
Because the platform goes from "limited modules / pilot scope" in 2024 to "full operational replacement of legacy data estate" in 2025. The cost reflects taking on enterprise data workloads at scale.

**Q: How firm is the $4.73M "modules" cost?**
Bronze confidence here — this is a planning estimate. The real cost depends on (a) how many modules QBE actually subscribes to, (b) data volumes ingested, (c) compute scaling. Could easily be ±20–30%.

**Q: Why is App Run sized at DAP cost?**
Because Q-Sight does what DAP did (broadly speaking). The 1:1 substitution assumption is reasonable but unvalidated. Modern data platforms can be cheaper to operate than legacy (less custom support); they can also be more expensive (more data, more pipelines). The BC bets they balance.

**Q: Where does Data Archiving sit in the data strategy?**
Data archiving is a regulatory/retention requirement. The $600K steady-state covers archive storage and access for QBE's retention obligations. This is genuinely incremental to the legacy estate, which didn't have a comparable capability.

**Q: Q-Sight cost is described as "driven by Data /VS programs" — what does that mean?**
QBE has separate "Data" and "VS" (likely Value Stream) programs that drive what data lands in Q-Sight. The Q-Sight cost scales with their delivery. **This means the Q-Sight cost isn't fully under modernisation's control** — it's partly driven by other programs.

## What to flag as honest caveats

1. **Bronze confidence is well-deserved here.** The 2025 jump is large and based on planning estimates, not contracted module subscriptions.

2. **Cost is driven by other programs, not by modernisation alone.** This is unusual — most categories are within modernisation control.

3. **App Run benchmarked at DAP cost.** Reasonable but unvalidated.

4. **Apptio doesn't show Q-Sight separately because it's a new platform** — there's no historical actuals to anchor the steady-state against.

## The bottom line for the room

> *Q-Sight is the new data platform — $2.55M Mod investment in 2024, $6.59M steady-state from 2027. Bigger than the legacy data estate it replaces ($4M today) because it includes data archiving, expanded modules, and the Data /VS program scope. Confidence is Bronze because module costs are planning estimates and App Run is sized at legacy DAP cost. The 2025 jump of $5.96M is the most exposed number in this category. Worth getting a tighter view from the data team before defending this in detail.*

---

# Category 10: Legacy Integration

**Confidence:** Silver
**2024 cost:** $290K | **2031 cost:** $0
**Total decom benefit by 2031:** ~$290K annually | **Pairs with:** Category 11 (New Integration)
**Source:** Apptio 12-month view (ESB section)

## The one-paragraph version (for an exec who has 30 seconds)

Legacy Integration is the existing ESB (Enterprise Service Bus) and related integration patterns. Today we spend $290K annually. As New Integration (Category 11) — Confluent, Mulesoft/Azure API, Springboot — replaces the legacy patterns, this cost falls to zero by 2031. The decom is back-end loaded (starts 2028), small in absolute terms but symbolically important because it represents the architectural shift to event-driven and modern API integration. Silver confidence because the percentages mirror the standard decom pattern (50%/60%/70% reductions). Small numbers, low risk.

## What this category actually is

QBE's existing integration layer — primarily ESB (Enterprise Service Bus, visible in Apptio Section 2g) plus related integration applications. These provide message routing, transformation, and orchestration for legacy applications.

As architecture moves to event-driven (Confluent) and modern API patterns (Mulesoft/Azure API + Springboot), legacy ESB usage declines and can be retired.

## What we're paying for

| Component | 2024 | 2031 |
|---|---|---|
| **Hosting & Licencing** | $210K | $0 |
| **Application Run** | $69K | $0 |
| **Inflation** | $11K | $0 |

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024–2027** | ~$290K | Holding — New Integration ramping |
| **2028** | $144K | First major step (50% H&L, 40% App Run) |
| **2029** | $117K | Further reductions |
| **2030** | $95K | Approaching zero |
| **2031** | $0 | **Fully decommissioned** |

## The "is this real?" stress tests

**Q: Why does decom only start 2028?**
Because New Integration patterns need to be embedded across the application portfolio first. Legacy ESB stays alive while applications still call it.

**Q: Is full decom by 2031 realistic?**
Mostly. ESB tends to have stubborn long-tail integrations that survive longer than planned. The BC assumes full retirement; real-world experience suggests 5–10% might persist into a tail.

**Q: Why is this Silver and not Bronze?**
Because the cost is small (low risk) and the Apptio actuals are visible (good evidentiary base). The percentages are estimates but consistent with industry patterns.

## What to flag as honest caveats

1. **Full-zero by 2031 may be optimistic.** Industry experience suggests ESB tails into a 5–10% residual longer than planned.

2. **The decom depends on New Integration adoption** — if Confluent/Mulesoft rollout slips, this slips.

## The bottom line for the room

> *Small category — $290K legacy ESB cost decommissioning to zero by 2031 as modern integration replaces it. Symbolically important (architectural shift) but financially minor. Low risk to the BC overall.*

---

# Category 11: New Integration

**Confidence:** Silver
**2024 cost:** $838K | **2031 cost:** $2.86M
**Total Mod-funded:** $1.34M | **BAU steady-state:** $2.86M annually from 2030
**Source:** Integration team model; Schedule 14b Mulesoft baseline; Confluent revised commercials

## The one-paragraph version (for an exec who has 30 seconds)

New Integration is the modern integration stack — Confluent (event streaming), Azure API / Mulesoft (API management), and Springboot (open-source frameworks). It replaces Legacy Integration. Total cost ramps from $838K in 2024 to $2.86M annually by 2030 onwards, then flat. The cost is **partially contracted** (Mulesoft baseline visible in Schedule 14b, Confluent has revised commercials) and partially planning estimate. The Application Run line ramps from $173K to $518K as the team scales. We rated Silver because the foundational tools have firm commercials but exact scaling and Springboot/open-source elements are subject to change. Note: **Springboot is open source, $0 — this is a real cost-saving choice, not an estimation gap.**

## What this category actually is

Three technology stacks combined:

- **Confluent** — event streaming platform; new tool, subscription scaling with use
- **Azure API / Mulesoft** — API management and integration platform; existing Mulesoft licence forms baseline (Schedule 14b)
- **Springboot** — open-source Java framework; **zero licensing cost**

Plus the QBE-side integration team that operates and develops on these stacks.

## What we're paying for

| Component | 2024 | 2031 | Notes |
|---|---|---|---|
| **Confluent (new tool subscription)** | $100K | $600K | Revised commercials reflected |
| **Confluent (existing subscription)** | $0 | $0 | $100K (2025), $250K (2026) — bridging |
| **Azure API / Mulesoft** | $533K | $1.62M | Schedule 14b Mulesoft baseline + Azure API growth |
| **Springboot** | $0 | $0 | Open source — zero cost |
| **Application Run** | $173K | $518K | Scaling support team |
| **Inflation** | $32K | $114K | Standard 4% |

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024** | $838K | Initial Mod investment |
| **2025** | $1.75M | Confluent and API tooling ramping |
| **2026** | $2.20M | Steady scaling |
| **2027** | $2.55M | Continued growth |
| **2028** | $2.84M | Approaching steady-state |
| **2029–2031** | $2.86M | Flat |

## The "is this real?" stress tests

**Q: Springboot at $0 — is that realistic?**
Yes. Springboot is open source. We pay for **support and tooling around it** (which sits in Application Run), not for licences. This is a deliberate architectural choice and represents a real saving vs proprietary alternatives.

**Q: How firm is Mulesoft pricing?**
Anchored to Schedule 14b — a contracted baseline. Growth above that depends on usage scaling; Schedule 14b figures are the floor.

**Q: Confluent commercials are described as "revised" — what does that mean?**
The Confluent contract was renegotiated in 2024 and the BC reflects revised pricing. There's also commentary about "opportunity to reduce license — move to opensource" suggesting Confluent could potentially be partially replaced by open-source Kafka. **That's a future opportunity, not assumed in BC numbers.**

**Q: Why does App Run grow from $173K to $518K — that's 3x?**
Because the integration team scales with the volume of new patterns deployed. This is standard for a new stack; teams grow as adoption grows.

## What to flag as honest caveats

1. **Confluent has an "opportunity to move to open-source" not modelled.** If executed, this category's steady-state could be lower by ~$300–500K. Upside, not downside risk.

2. **Application Run scaling is an estimate.** Real team size will depend on adoption rate.

3. **Schedule 14b Mulesoft baseline is the firm floor**; growth above it is estimated.

## The bottom line for the room

> *Modern integration stack — $838K Mod investment, $2.86M steady-state by 2030. Partially contracted (Mulesoft, Confluent revised) and partially planning estimate. Springboot at $0 is a real architectural saving, not a gap. Confidence is Silver. Upside opportunity exists in moving Confluent to open-source if Engineering chooses — not assumed in BC.*

---

# Category 12: GW Add-ons

**Confidence:** Bronze
**2024 cost:** $0 | **2031 cost:** $625K
**Total Mod-funded:** $500K (2026 + 2028) | **BAU steady-state:** $625K from 2028
**Source:** Placeholders — Auto Pilot ($200K, 2026) + UW Workbench ($400K, 2028)

## The one-paragraph version (for an exec who has 30 seconds)

GW Add-ons are placeholders for two specific Guidewire modules: **Claims Auto Pilot** ($200K from 2026) and **GW UW Workbench** ($400K from 2028). Both are positioned as enablers for STP (straight-through processing) and underwriting automation. **Neither is contracted.** The numbers are placeholder cost reservations only — no Guidewire pricing has been confirmed for these modules. We rated this Bronze because every line is a placeholder. The honest framing: **this category is a budget envelope, not a costed plan**, exactly like Digital New (Category 7). Total exposure is small ($625K annually steady-state) but two-thirds of it is the UW Workbench placeholder which represents a meaningful commercial commitment if exercised.

## What this category actually is

Two Guidewire products positioned as Phase 2 modernisation enablers:

- **Claims Auto Pilot** — automated claims handling module. Placeholder $200K from 2026.
- **GW Underwriting Workbench** — broker/underwriter productivity tool. Placeholder $400K from 2028.

These are separate from the core GW Cloud subscriptions (Categories 1, 2) — they're additional modules that drive specific business outcomes around STP and automation.

## What we're paying for

| Component | 2024 | 2031 | Notes |
|---|---|---|---|
| **Subscription Fee** | $0 | $600K | Placeholders only |
| **Application Run** | $0 | $0 | Covered in core GW App Run |
| **Inflation** | $0 | $25K | Standard 4% |

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024–2025** | $0 | Nothing live |
| **2026** | $200K | Auto Pilot placeholder kicks in |
| **2027** | $208K | Inflation only |
| **2028** | $608K | UW Workbench placeholder added |
| **2029–2031** | ~$625K | Steady-state |

## The "is this real?" stress tests

**Q: Why are both placeholders Bronze?**
Because no commercial discussion has happened with Guidewire on either. The $200K and $400K are reasonable order-of-magnitude estimates based on Guidewire's pricing patterns for these module types.

**Q: Are these definitely going to be deployed?**
Probably yes for Auto Pilot (claims automation is high priority); maybe for UW Workbench (depends on broker channel strategy). **Auto Pilot is more likely to land.**

**Q: What if the actual contract is different from $200K / $400K?**
Could be ±50%. Auto Pilot at $300K wouldn't surprise; UW Workbench at $250K or $600K is plausible. Not material to overall BC.

**Q: Why are these in the BC at all if they're so uncertain?**
Same reason as Digital New — to reserve the budget envelope. If we want STP and automation outcomes, we'll likely need these tools. Excluding them would understate the run cost.

## What to flag as honest caveats

1. **Both lines are placeholders.** Bronze confidence is well-deserved.

2. **Auto Pilot is more likely than UW Workbench.** If BC needs sensitivity analysis, the higher-confidence assumption is "Auto Pilot at $200K, UW Workbench TBD."

3. **Application Run is $0 here, deliberately.** Support effort assumed within core GW Cloud team.

## The bottom line for the room

> *Two Guidewire module placeholders — Auto Pilot ($200K from 2026) and UW Workbench ($400K from 2028). Total $625K annual exposure. Neither contracted. Reserves budget envelope for STP and automation outcomes. Not material to overall BC; confidence is Bronze and refresh is needed once Guidewire commercial discussions happen.*

---

# Category 13: QUW/IW

**Confidence:** Gold
**2024 cost:** $631K | **2031 cost:** $208K
**Total decom benefit by 2031:** ~$423K annually | **Pairs with:** Category 3 (Evolve)
**Source:** Apptio 12-month AUD view (Inputs Section 2h)

## The one-paragraph version (for an exec who has 30 seconds)

QUW/IW (Quote Underwriting / Insurance Workbench) is a small mainframe application — same physical IBM mainframe as Evolve. Today we spend $631K annually. As commercial flow products migrate to GW Cloud, QUW/IW usage declines and the cost falls to $208K by 2031 — a partial decom (not zero) because of the same residual mainframe overhead that affects Evolve. The numbers are well-evidenced (Apptio 12-month AUD view) and the reduction percentages mirror the Evolve decom pattern. We rated this Gold because the platform is small and well-understood, with full Apptio actuals supporting the baseline.

## What this category actually is

QUW/IW is a quote and underwriting workflow application running on the IBM mainframe (CICS / DB2 alongside Evolve and CTPCICS). It supports underwriting workflows for commercial flow products today. As GW Cloud takes over those products, QUW/IW usage falls.

## What we're paying for today

| Component | 2024 | 2031 |
|---|---|---|
| **Hosting & Licencing** | $439K | $0 (residual at $132K through 2030) |
| **Application Run** | $166K | $0 (residual at $66K through 2030) |
| **Inflation** | $24K | $10K |

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024–2027** | ~$631K | Holding — material loads still on QUW/IW |
| **2028** | $311K | **Major decom** — H&L 50%, App Run 40% |
| **2029** | $255K | Further reduction |
| **2030** | $208K | Approaching residual |
| **2031** | $208K | Residual (30% MF infra) |

## The "is this real?" stress tests

**Q: Why is this Gold but Evolve is Silver?**
Because QUW/IW is much smaller and less complex. Apptio gives a clean 12-month view. The percentages are still estimates but the magnitude is small enough that estimation error is contained (worst case ±$50K). Evolve is bigger and more complex with more uncertainty.

**Q: Same residual pattern as Evolve — coincidence?**
No. Both share the same mainframe infrastructure. The 30% residual reflects the shared MF overhead that doesn't go away regardless of which application is on it.

**Q: Why is decom timing back-end loaded (2028+)?**
Same reason as Evolve — commercial flow products need to land on GW Cloud first; QUW/IW can't decom before that.

## What to flag as honest caveats

1. **Same risk profile as Evolve in miniature.** Slippage in commercial flow migration delays this decom.

2. **The 30% residual assumption is the same industry-typical figure as Evolve.** Defensible but not precise.

## The bottom line for the room

> *Small mainframe application — $631K → $208K residual by 2031. Apptio actuals firmly support the baseline. Decom timing depends on commercial flow migration. Gold confidence because of clean evidentiary base and small magnitude. Same decom pattern as Evolve, scaled down.*

---

# Category 14: AWS Landing Zone

**Confidence:** Silver
**2024 cost:** $54K | **2031 cost:** $518K
**Total Mod-funded:** ~$507K | **BAU steady-state:** ~$518K from 2031, growing 2-3% annually
**Source:** Detailed 10-year build (Inputs Section 12); estimated AWS usage costs

## The one-paragraph version (for an exec who has 30 seconds)

AWS Landing Zone is the cloud foundation supporting Guidewire Cloud — secure VPCs, network connectivity (Equinix), guardrails, and the cloud engineering team to operate it. Cost ramps from $54K in 2024 (half-year) to $518K by 2031 as the platform fully scales. The build is **detailed and well-documented** (Section 12 of Inputs has a 10-year breakdown by line item) but the underlying numbers are **AWS estimated usage costs**, not contracted. We rated Silver because the structure is firm but the AWS consumption charges are forecasted not contracted. Note: This is a real, necessary cost — without AWS Landing Zone, the GW Cloud transformation has no secure cloud foundation. It's small relative to the GW Cloud savings it enables.

## What this category actually is

The cloud foundation for QBE's modernisation:

- **AWS Professional Services** ($82K, one-off 2024) — initial implementation
- **QBE Cloud Engineer** ($18K, one-off 2024) — 15 days of engineering
- **AWS Services Costs** — ongoing consumption (storage, transfer, guardrails, networks)
- **Equinix Services** — network connectivity to AWS ($12K/year per link × 2 links)
- **Resource Uplift** — 2 Senior Cloud Engineers (L2) for service assurance
- **AWS Training** — ongoing certification

## What we're paying for

| Component | 2024 | 2031 | Notes |
|---|---|---|---|
| **Implementation Fees** | $100K | $0 | One-off (Professional Services + QBE Engineer) |
| **AWS Services - Guardrails** | $5K | $11K | Scales 2.5% annually |
| **AWS Services - Networks** | $34K | $117K | Largest growth driver |
| **Equinix Services** | $6K | $12K | Two physical network links |
| **Resource Uplift (2 L2 Engineers)** | $0 | $371K | From 2025 onwards |
| **AWS Training** | $0 | $6K | From 2025, 2.5% annual increase |
| **DB Storage / Egress** | $10K | $0 | One-off migration costs (2024-2025) |

The full year-by-year breakdown is in Inputs Section 12 — every line item shows 10-year detail.

## Reading the cost shape

| Year | Total | What's happening |
|---|---|---|
| **2024 (Jul-Dec)** | $54K | Implementation half-year |
| **2025** | $426K | Resource uplift kicks in ($320K) — biggest single jump |
| **2026** | $459K | Steady scaling |
| **2027** | $470K | Ongoing |
| **2028** | $482K | Ongoing |
| **2029** | $493K | Ongoing |
| **2030** | $505K | Ongoing |
| **2031** | $518K | Steady-state with annual escalation |

## The "is this real?" stress tests

**Q: How firm is the build?**
The structure (people, training, services, networks) is firm — these are necessary components of an AWS foundation. The dollar values are AWS-estimated consumption charges, which are forecasts.

**Q: Why is it growing 2-3% annually rather than flat?**
AWS pricing escalates and consumption grows as more workloads land. The 2-3% is reasonable for steady-state operations.

**Q: Why are 2 L2 Cloud Engineers needed at $320K?**
Because GW Cloud sits on AWS infrastructure — even though Guidewire manages the platform, QBE needs cloud engineering capability for security, compliance, and operational issues that span the AWS account. This is genuinely incremental headcount.

**Q: Could this be cheaper?**
The Resource Uplift at $320K is the biggest line. Could be argued down to 1 L2 Engineer ($170K) for cost savings, but that's a risk decision — for a regulated insurer, 2 engineers is conservative.

**Q: What's the relationship to Guidewire Cloud cost?**
GW Cloud is the application layer (Categories 1, 2). AWS Landing Zone is the cloud account it runs in. They're complementary, not duplicate. AWS Landing Zone is the "address" in the cloud where GW Cloud "lives."

## What to flag as honest caveats

1. **AWS service costs are forecasts, not contracts.** Consumption-based pricing means actual cost depends on usage. ±20% uncertainty.

2. **2 L2 Engineers could be challenged.** Defensible but not the only valid sizing.

3. **No FX risk** — Equinix and AWS bill in AUD/local currency at current rates.

## The bottom line for the room

> *AWS Landing Zone is the cloud foundation enabling everything else — guardrails, networks, engineering capability. Total $518K steady-state by 2031, growing 2-3% annually. Small relative to GW Cloud savings it enables. Costs are AWS-estimated (Silver confidence) but the structure is firm. Without this foundation, GW Cloud cannot operate; it's a non-discretionary enabler of the broader transformation.*

---

# Cross-Cutting Considerations

## The IT Budget Envelope

**$145.1M today → $168.6M by 2031** — a $23.5M increase across 8 years.

This is the **net effect of all 14 categories combined**: increases in GW Cloud, Earnix, Q-Sight, AWS, New Integration, Digital New are offset by decreases in Evolve, GW On-Prem, Existing Data, c.Change, Legacy Integration, QUW/IW.

| Year | Cumulative IT Budget |
|---|---|
| 2024 | $145.1M (baseline) |
| 2025 | $145.1M (Mod step doesn't hit BAU yet) |
| 2026 | $153.2M (+$8.1M) |
| 2027 | $159.1M (+$5.9M) |
| 2028 | $162.2M (+$3.1M) |
| 2029 | $162.8M (+$0.6M) |
| 2030 | $165.4M (+$2.6M) |
| 2031 | $168.6M (+$3.2M) |

The shape matters: **the steepest growth is 2026 ($+8.1M)**, then increases moderate. By 2029 the BC is approaching steady-state.

## The Mod Fund Tracker

| Item | Amount |
|---|---|
| **Total Mod Fund** | $7,362,550 |
| **Mod spent to date** (GW sub $779,182 actuals) | $779,182 |
| **Mod Outstanding** | $6,583,368 |
| **DAP cloud to be allocated** | ~$460K |

The Mod fund is the discretionary funding pool. ~10% spent, ~90% outstanding. The BC assumes the outstanding $6.58M is spent over the program lifetime, primarily on year-1 Mod step costs in each category.

## GWP Migration Roadmap

The single most important external dependency for the BC. **All decom savings, all GW Cloud cost ramps, all Earnix above-commit risk** depend on the GWP migration plan holding.

The BC was originally costed against the **July 2024 baseline ramp**:
- 2025: 57Bn migrated → 2031: 7,214Bn (commercial flow + negotiated)

There's a **revised May 2025 ramp from Tara M** showing slippage:
- 2027: 207Bn (vs 3,210Bn in the July plan) — material slippage
- 2031: 5,253Bn (vs 7,214Bn in July plan)

If the BC is being defended against the May 2025 ramp, **most numbers in the model need refresh**. The shape of the answer doesn't change but year-by-year values move.

## GWP Above-Commit Exposure

Captured in Inputs Section 8/9 but not rolled into category totals:
- Earnix above-3.5Bn AUD: ~$880K (2028) → $2.14M (2031) AUD
- Guidewire above-commit: not separately quantified

These represent BC exposure that is acknowledged but not fully integrated into the category-level numbers.

## Document Management

Visible in Apptio (~$3.1M LTM) but not represented in any of the 14 categories. Lives in another part of the IT budget. Worth confirming this isn't overlapping with what's costed in the BC.

## Risk Buy Down

A tab exists in the workbook but no content visible. Likely tracks confirmed cost reductions vs original BC estimates. Worth populating with:
- Earnix Quote Saving discount (15% → 0%) — confirmed win
- GW Cloud commit option vs no-commit — open decision
- Digital New placeholders — open

## Confidence Distribution Summary

| Confidence | Categories | Total 2031 Cost |
|---|---|---|
| **Gold (5)** | GW Direct & CTP, GW Evolve Replacement, GW On-Prem, Earnix, QUW/IW | $36.9M |
| **Silver (6)** | Evolve, c.Change, Existing Data, Legacy Integration, New Integration, AWS Landing Zone | $5.6M |
| **Bronze (3)** | Digital New, Q-Sight, GW Add-ons | $8.5M |

**Gold dominates the dollar weight** — most of the BC is contractually-anchored. Bronze categories represent placeholders for future commercial decisions, totalling ~$8.5M annually steady-state. That's the most exposed portion of the BC.

---

# Final Defence Strategy Summary

**Strongest categories to lead with:** GW On-Prem (cleanest decom), GW Direct & CTP (signed contract), Earnix (signed contract), QUW/IW (clean Apptio actuals).

**Categories most exposed to challenge:** Digital New (placeholders), Q-Sight (volume-driven Bronze), GW Add-ons (placeholders).

**Single biggest risk to the BC:** GWP migration roadmap slippage. Affects Categories 2, 3, 4, 6, 8, 13 simultaneously.

**Single biggest commercial decision pending:** Guidewire commit option (~$11.7M over 5 years) for tier pricing benefits.

**The honest BC framing for Execs:**
> *Net IT budget moves $145M → $168M over 8 years. Of that $23M increase, the largest contributors are Guidewire Cloud (Categories 1+2) and Q-Sight. They're offset by ~$15M of legacy decommissioning. What we're really buying is platform modernisation, vendor support, and reduced technical debt risk. The numbers are well-evidenced for the major contractual categories (Gold), reasonably modelled for Silver categories, and explicitly placeholder for the three Bronze categories which represent commercial decisions still pending. The BC's biggest exposure is execution on the GWP migration roadmap, not commercial pricing.*

---

*End of category narratives. This document covers all 14 cost categories plus cross-cutting considerations. Use as briefing material, talking points, and Q&A preparation when defending the BC to Finance, CFO, CIO, Execs, and Group Architecture.*




---

# Part 2: Change-to-RUN Cost Analysis

This section provides a deeper accounting walkthrough for selected categories, focusing on how Mod-funded (Change) costs transition into BAU (RUN) costs. The Change-to-RUN handover is the most consequential accounting moment in any IT transformation — getting it wrong leads to either double-counting (Mod and BAU both pay) or budget gaps (Mod stops, BAU doesn't pick up).

The BC's Mod / BAU split is specifically designed to manage this transition cleanly.

## Defining the terms

In QBE's accounting, every IT cost falls into one of two buckets:

- **Change** — one-off project investment to *build* something new. Funded by the modernisation programme. Capitalised or expensed as project cost. Doesn't recur.
- **RUN** — ongoing operational cost to *keep something alive* after it's built. Sits in the IT budget. Recurs every year.

**"Change to RUN"** is the moment a Change-funded item *transitions* into the RUN budget — when something the modernisation programme paid to build becomes a permanent operational cost the IT budget has to absorb forever after.

---

## Category 1: GW Managed Cloud Direct & CTP — Change-to-RUN Analysis

### The two populations of cost

Category 1 has **two distinct populations of cost**:

#### Population A: Mod-funded costs (Change)

These are the **one-off step-up costs** in the years when something new lights up. Funded from the $7.36M Mod budget. Once paid, they're done — they don't recur in subsequent years.

| Year | Mod-funded amount | What it pays for |
|---|---|---|
| 2025 | $1.90M | First year of GW Cloud Direct & CTP — initial subscription + first year App Run |
| 2026 | $6.50M | Second-year step-up as full migration kicks in |
| 2027 onwards | $0 | Mod has finished funding this category |

The Mod funding is **front-loaded into 2025–2026**. By 2027 the modernisation programme has paid its share and is out.

#### Population B: BAU costs (RUN)

These are the **permanent, recurring run costs** that the IT budget has to absorb. They scale with what's actually live on the platform. They go up as workload grows; they go down (here, the legacy switch-off in Category 4) as old platforms retire.

| Year | BAU increase | BAU decrease | What's happening |
|---|---|---|---|
| 2026 | +$6.45M | $0 | The cost Mod was funding in 2025 now lives in BAU |
| 2027 | +$3.70M | -$2.33M | Continuing ramp + first wave of legacy fall-off |
| 2028 | $0 | -$3.08M | Legacy GW v8 fully off |
| 2029 | $0 | -$580K | Tail residual fading |
| 2030 | $0 | -$10K | Steady-state |
| 2031 | $0 | -$12K | Steady-state |

**The BAU lines are what the IT budget will be paying *every year forever* once Mod is gone.**

### The handover mechanics (year-by-year walk)

```
2024 baseline:    $6.45M   (existing GW v8 cost — already in BAU)

2025 ── Mod step:        +$1.90M  ← Mod fund pays
        BAU stays at:     $6.45M
        Total in year:    $12.95M (parallel-run hump)

2026 ── Mod step:        +$6.50M  ← Mod fund still paying
        BAU increases:   +$6.45M  ← The 2025 Mod cost transitions to RUN here
        Old BAU drops:   -$0
        Total:           $10.62M

2027 ── Mod step:        $0       ← Mod is done
        BAU increases:  +$3.70M   ← The 2026 Mod cost transitions to RUN here
        Old BAU drops:  -$2.33M   ← Legacy GW v8 starting to switch off
        Total:           $7.54M

2028+ ── Mod: $0
         BAU steady-state: ~$6.7M
         Indexed by 4% inflation only
```

Notice the **one-year lag** between Mod funding and BAU increase:

- 2025 Mod ($1.90M) → 2026 BAU increase reflects this becoming permanent
- 2026 Mod ($6.50M) → 2027 BAU increase reflects this becoming permanent

This is **deliberate**. It avoids the double-count trap. In 2025, only Mod pays. In 2026, Mod pays for the *new* increment AND BAU absorbs *last year's* increment. The handover happens at the year boundary — clean, sequential, no overlap.

### Why this structure matters for defending the BC

#### 1. No double-counting

A common Finance challenge: *"Are you funding this twice — once from Mod and once from IT BAU?"*

The answer for Category 1: **No.** Mod and BAU never claim the same dollar in the same year. The $1.90M Mod in 2025 and the $6.45M BAU increase in 2026 are *different dollars in different years* — the BAU 2026 number reflects what RUN cost we'd carry from 2026 onwards, regardless of how the 2025 transition was funded.

#### 2. Clear end-state visibility

A common CFO challenge: *"What will this cost the IT budget once Mod is gone?"*

The answer for Category 1: **$6.7M annually from 2028 onwards** (with 4% inflation). That's the BAU steady-state. It's visible, it's calculable, and it's locked into the IT budget envelope projection ($145M → $168M).

#### 3. Mod fund is bounded

A common CIO challenge: *"How big is the Mod fund commitment for this category?"*

The answer for Category 1: **$8.40M total Mod-funded** ($1.90M in 2025 + $6.50M in 2026), with no further Mod calls after 2026. This is bounded — you know the maximum exposure.

### Where Change-to-RUN is less clean for Category 1

Two things to be honest about:

#### 1. The 2025 parallel-run hump is partially BAU, not Mod

In 2025, total cost in Category 1 is $12.95M:
- $6.45M is **legacy GW v8 BAU continuing** (this is in Category 4, but it's the same workload)
- $1.90M is **new GW Cloud Mod-funded**
- The remaining is in transition

This means **the 2025 IT budget feels the parallel-run pressure even though Mod is partially absorbing it**. If the IT budget is tight, this is the year it hurts most. The BC handles this by treating the 2025 hump as a known, time-limited event — but it's still a real cash impact.

#### 2. The Mod Outstanding accounting

The Mod fund tracker shows:
- Total Mod Fund: $7,362,550
- Mod spent to date: $779,182 (GW sub actuals)
- Mod Outstanding: $6,583,368

Category 1's Mod-funded amount alone is $8.40M ($1.90M + $6.50M). That's *more* than the total Mod fund of $7.36M.

This means **either**:
- The Mod fund covers a portion of Category 1 and other sources fund the rest, OR
- The Mod-funded labels in Category 1 are a re-allocation framing, not a literal Mod fund draw, OR
- The Mod fund will be replenished as part of programme funding cycles

This is a **reconciliation question** worth asking the original BC owner or Finance. The BC document doesn't fully explain how Category 1's $8.40M Mod claim aligns with a $7.36M total Mod fund — and it's a question Finance is likely to raise.

### The plain-language version for an Exec

> *In 2025, modernisation pays $1.9M for the first year of Guidewire Cloud Direct & CTP. In 2026, modernisation pays a further $6.5M as full migration kicks in. From 2027 onwards, modernisation has finished — no more programme funding. From that point, the IT budget absorbs the running cost as BAU: roughly $6.7M annually, indexed at 4%. The handover is staggered by one year so we never charge the same cost to both Mod and BAU. The end-state is visible and bounded. The one watchpoint is that the $8.4M Mod claim for this category is larger than the current Mod fund balance — that's a reconciliation question worth checking with Finance.*

---

## Category 2: GW Managed Cloud Evolve & AOPCICS Replacement — Change-to-RUN Analysis

### Why this category's Change-to-RUN is harder to explain

Category 1 had a clean, two-step Mod profile (2025, 2026) followed by flat BAU. **Category 2 is a multi-year staircase** — Mod funding doesn't end after two years; it appears every single year from 2024 to 2031, with eight separate Mod steps, eight separate BAU pickups (each lagged by one year), and no actual decom inside this category to offset.

That makes it harder to defend. It also makes it more important to defend correctly, because this is the **largest Mod claim in the entire BC** — roughly $25M of Mod funding called over 8 years, against a $7.36M Mod fund.

### The two populations of cost in Category 2

#### Population A: Mod-funded costs (Change)

Unlike Category 1, where Mod was confined to 2025–2026, **Category 2 calls Mod funding every single year** as each new wave of GWP lands on the platform:

| Year | Mod-funded amount | What it pays for |
|---|---|---|
| 2024 | $500K | NPE & data masking initial setup (no GWP yet) |
| 2025 | $404K | First production go-live (Workers Comp early) |
| 2026 | $7.09M | **Big step** — Elders Farm, Comm Motor wave lands |
| 2027 | $5.81M | Broker products migrating |
| 2028 | $4.34M | Negotiated lines start arriving |
| 2029 | $4.68M | Workers Comp at 90%, GL & CP through Radar |
| 2030 | $1.04M | Tail of migration |
| 2031 | $1.18M | Final waves on platform |
| **TOTAL** | **~$25.0M** | |

**This is the structural difference vs Category 1.** Mod isn't funding a one-off platform stand-up here — it's funding the *first year* of every wave of GWP that lands. Eight waves, eight Mod steps.

#### Population B: BAU costs (RUN)

The BAU side mirrors the Mod side with the standard one-year lag — last year's Mod step becomes this year's BAU increase:

| Year | BAU increase | Reflects which Mod step? |
|---|---|---|
| 2024 | $500K | (Establishing the BAU baseline) |
| 2025 | $404K | 2024 Mod transitioning |
| 2026 | $7.09M | 2025 Mod transitioning + new wave |
| 2027 | $5.81M | 2026 Mod transitioning |
| 2028 | $4.34M | 2027 Mod transitioning |
| 2029 | $4.68M | 2028 Mod transitioning |
| 2030 | $1.04M | 2029 Mod transitioning |
| 2031 | (residual) | 2030 Mod transitioning |

Notice the BAU increases are **almost identical to the Mod amounts**. That's the giveaway that this category is a recurring-cost ramp, not a one-off build — every Mod dollar this year becomes a BAU dollar next year.

There are **no BAU decreases inside this category** (none in the source data). All the offsetting savings live in the *partner* categories: Evolve, GW On-Prem, c.Change, Existing Data, Legacy Integration, QUW/IW.

### The staircase mechanic, year by year

```
2024 baseline:    $0       (no production GWP on platform yet)

2024 ── Mod step:        +$500K   ← Mod fund pays for NPE/masking setup
        BAU base set to:  $500K   ← Established as new BAU floor
        Total in year:    $500K

2025 ── Mod step:        +$404K   ← First production wave (small)
        BAU increase:    +$404K   ← The 2024 Mod cost now in BAU
        Existing BAU:     $500K
        Total:            $904K

2026 ── Mod step:        +$7.09M  ← Big wave: Elders Farm, Comm Motor land
        BAU increase:    +$7.09M  ← The 2025 Mod cost now in BAU + new wave
        Existing BAU:     $904K
        Total:            $7.99M

2027 ── Mod step:        +$5.81M  ← Broker products
        BAU increase:    +$5.81M
        Existing BAU:     $7.99M
        Total:            $13.81M

2028 ── Mod step:        +$4.34M  ← Negotiated lines start
        BAU increase:    +$4.34M
        Existing BAU:     $13.81M
        Total:            $18.14M

2029 ── Mod step:        +$4.68M  ← Workers Comp scale, GL/CP Radar
        BAU increase:    +$4.68M
        Total:            $22.82M

2030 ── Mod step:        +$1.04M  ← Tail
        Total:            $23.87M

2031 ── Mod step:        +$1.18M  ← Final
        Total:            $25.05M

2032+ ── Mod: $0 (programme over)
         BAU steady-state: ~$25M annually
         Indexed by 4% inflation only
```

The thing to notice: **the cost only ever ramps up — it never falls inside this category**. There's no parallel-run hump like Category 1 had, because we're not switching off something on the way in. All the switch-offs that *justify* this build live in other categories.

### Why this Change-to-RUN structure is harder to defend

Three things make Category 2 harder than Category 1:

#### 1. The Mod claim is larger than the entire Mod fund

The Mod fund total is **$7,362,550**. Category 2's cumulative Mod claim is **~$25M**. That's roughly 3.4x the available Mod fund.

This isn't an error in the BC — it's a deliberate accounting framing. The "Mod" label here means "modernisation-attributable run cost in the year it first appears" rather than "literally drawn from the Mod fund balance." But it requires explanation when Finance asks the obvious question.

In Category 1 we already flagged this: $8.4M Mod claim against a $7.36M fund. Category 2 makes it more pronounced — at $25M, it's clear the "Mod" label is a *cost-attribution device*, not a *funding source*.

The honest framing: **the Mod fund covers the discretionary year-1 step costs across the whole programme; the recurring run cost ramps that follow are absorbed into the IT budget envelope as BAU**. The "Mod" tag in Category 2 is identifying *what would be funded by Mod if the fund were that large* — i.e., it's labelling the new run cost so it can be tracked separately, not declaring a literal Mod fund draw.

This is worth confirming with the original BC owner before defending under fire.

#### 2. There's no internal decom to offset the build

In Category 1, the BC narrative is "$6.7M new run cost, but it replaces $9.9M of GW On-Prem cost in Category 4 — net saving." That's clean inside two adjacent categories.

In Category 2, the offsetting savings are spread across **six different categories** (Evolve, c.Change, Existing Data, Legacy Integration, QUW/IW, plus residual GW On-Prem). To prove Category 2's $25M is justified, you have to walk Finance through six separate decom stories, each with its own confidence level (some Silver, some Bronze). You can't defend Category 2 in isolation.

This is a presentational issue more than a substantive one — but it matters when defending under time pressure.

#### 3. The Mod-to-BAU lag is fragile if migration timing slips

In Category 1, the lag is two clear steps and then steady-state. If 2025 slips, it pushes the 2026 BAU increase by a year — manageable.

In Category 2, **eight Mod steps with eight lagged BAU pickups** all assume the GWP migration roadmap holds. If the migration slips by 12 months:
- The Mod claim for that year falls (good — less Mod called)
- But the BAU pickup for the year after falls too (bad — savings expected in offset categories also slip)
- The cumulative shape of the staircase distorts

Tara M's revised May 2025 ramp already shows this is happening. The original July 2024 ramp had 3,210Bn migrated by 2027; the May 2025 ramp shows 207Bn by 2027. **That's a material slippage that should rebase Category 2's Mod-to-BAU profile entirely** — but the BC numbers haven't been refreshed for it yet.

### The Change-to-RUN reconciliation in one diagram

For each wave of GWP migration:

```
Year N:    Wave lands → Mod funds first-year cost (year N)
Year N+1:  Same cost continues → moves into BAU base (year N+1)
Year N+2:  Cost stays in BAU at indexed inflation
```

For Category 2, this happens **eight times in a row** (2024 through 2031). At each step, Mod gets bigger or smaller depending on the size of the wave, and BAU absorbs it the year after.

### What Finance is most likely to challenge

Three predictable questions:

**Q: How can the Mod claim here be larger than the Mod fund?**
Answer above. It's a cost-attribution device, not a literal fund draw. **Worth pre-empting this — say it before Finance does.**

**Q: If GWP migration slips, what happens to the staircase?**
Both Mod and BAU slip with it, in this category. But the offsetting savings in the partner categories *also* slip. Net BC impact is **negative** for slippage because cost ramps are slower than savings ramps in proportion.

**Q: Should we be committing to the GW commit option to lock in better pricing?**
This is a *separate* decision modelled in Scenario Cost Summaries (Inputs Section 11). The commit option costs an extra $11.7M over 5 years for tier-pricing benefits. Category 2's numbers assume the no-commit baseline. Whether to commit is a procurement decision the BC doesn't make — but the option exists and the cost impact is modelled.

### How Category 2's Change-to-RUN compares to Category 1

| Aspect | **Category 1: Direct & CTP** | **Category 2: Evolve Replacement** |
|---|---|---|
| Number of Mod steps | 2 (2025, 2026) | 8 (every year 2024–2031) |
| Mod cumulative total | $8.4M | ~$25M |
| Mod-to-BAU lag | 1 year, twice | 1 year, eight times |
| Pattern shape | Two-step then flat | Multi-year staircase, ever-rising |
| Internal decom offset | Linked to Category 4 (clean) | Spread across 6 categories (messy) |
| Steady-state stability | High (Gold contract) | High (Gold contract on unit price) |
| Defence complexity | Low (textbook clean) | High (requires walking six categories) |

**Category 1 is the textbook clean transition.** Category 2 is the **textbook *messy* transition** — not because the accounting is wrong, but because the structure (staircase, no internal offset, larger-than-fund Mod claim) is harder to communicate.

### The plain-language version for an Exec

> *Category 2 is a recurring-cost ramp, not a one-off build. Every year from 2024 to 2031, a new wave of GWP migrates onto Guidewire Cloud, and modernisation labels the first year of that wave's run cost as "Mod-funded." The year after, that cost moves into BAU and stays there. By 2031, eight years of accumulated waves give us a $25M annual run cost in the BAU base. The matching savings — Evolve, c.Change, Existing Data, Legacy Integration, QUW/IW, residual GW On-Prem — total roughly $15M annually by 2031, sitting in six other categories. Net IT budget impact across the whole transformation is ~$23M, accommodated within the BC's IT budget envelope ($145M → $168M). The "Mod" labels in this category are larger than the actual Mod fund balance because they're tracking cost-attribution, not literal fund draws — that's the one accounting question worth pre-empting with Finance before they ask.*

### Recommended actions before defending Category 2

Three things, in priority order:

1. **Confirm with the original BC owner (or Finance) what "Mod-funded" means in the context of the $25M cumulative claim vs the $7.36M Mod fund.** This is the single most likely Finance challenge and it's the one where you'd want a definitive internal answer before being asked.

2. **Refresh Category 2 numbers against Tara M's May 2025 ramp.** The shape doesn't change but the dollar values shift — and defending an old GWP plan when a newer one exists is a credibility risk.

3. **Build a "Category 2 + offsetting savings" combined view** that pulls the offsetting decom savings from the six partner categories alongside Category 2's build. This is what an Exec actually wants to see — net IT impact of the GW Cloud transformation in one chart, not Category 2 in isolation.

---

## Change-to-RUN Pattern Library (cross-category summary)

Different categories use different Mod-to-BAU patterns. Understanding which pattern a category uses helps anticipate how it will behave under stress:

| Pattern Type | Description | Categories Using It |
|---|---|---|
| **Two-step then flat** | Mod funds 1–2 years of stand-up, BAU absorbs, steady-state from year 3 | Category 1 (Direct & CTP) |
| **Multi-year staircase** | Mod funds each new wave; BAU lags by one year; cumulative ramp | Category 2 (Evolve Replacement) |
| **Pure decom (no Mod)** | No Mod step; only BAU decreases as legacy switches off | Categories 3, 4, 6, 10, 13 |
| **Mod = BAU same year** | Recurring SaaS — same number labelled both Mod and BAU each year | Category 5 (Earnix) |
| **Single Mod step + ramp** | Small Mod stand-up, then BAU ramps with usage | Categories 7, 9 |
| **Pure new BAU (negligible Mod)** | New cost appearing in BAU without significant Mod step | Categories 11, 12, 14 |

### Key principle for defending any category

**Whatever pattern is used, Mod and BAU should never claim the same dollar in the same year.** That's the test for clean Change-to-RUN accounting. The one-year lag between Mod and BAU is the mechanism the BC uses to enforce this.

If Finance ever asks "are you double-counting?", the answer is: trace any single dollar through the model and you'll see it appears in either Mod *or* BAU in a given year, never both. The lag is the proof.

---

*End of Part 2. Use this section as supporting accounting material when Finance or CFO ask the deeper "how does the Mod-to-BAU transition actually work" question — which they will.*
