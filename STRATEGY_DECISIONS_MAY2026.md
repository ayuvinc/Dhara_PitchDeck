# AyuVinc Strategic Decisions — May 2026

**Status:** Foundation for Pitch Deck & Business Plan Updates  
**Source:** Founder Strategy Session with Claude (claude.ai) — 14 May 2026  
**Approval:** AK (Founder & CEO)  
**Use:** Internal — Decision tracking for investor documents and operational execution  
**Canonical Until:** Next strategy review or superseded by explicit founder revision

---

## 1. THE PRECISE POSITIONING

### What AyuVinc Is NOT
- Not an EMR company
- Not a telemedicine platform
- Not an ABDM compliance play

### What AyuVinc IS
**AyuVinc is a patient-owned healthcare OS for India's 600,000 independent clinics.**

### The Architectural Inversion (The Unforkable Moat)

Every competitor (HealthPlix, EkaCare, Practo) built:
- Doctor-owned data models
- Clinic-owned data models

AyuVinc built:
- **Patient-owned from day one**
- Patient carries their record
- Clinic is the distribution layer, not the data owner

**This is not a feature. It is ground-up architecture that cannot be retrofitted.**

### The Retrofit Moat — Use This Language Exactly

> "Competitors cannot retrofit consent-native, patient-owned architecture onto a live system with paying customers who believe they own the data. To do so they must re-identify every patient record, rebuild access controls, create revocation infrastructure, and tell existing customers they've been demoted. That is not a feature sprint. It is a company rebuild. We built this as the foundation. They cannot catch up without destroying what they have."

---

## 2. REVENUE MODEL — PHASE 1 (SEED PERIOD)

### The Four Revenue Streams

| Stream | Amount | Unit | Economics |
|--------|--------|------|-----------|
| EMR | ₹199 | Per clinic/month | Acquisition tool, not revenue engine |
| Vaani AI Scribe | ₹187.5 | Per hour (session billing) | GP and Psych tiers; psychiatrist at 6 sessions/day > 10 GPs on EMR subscription |
| Pharmacy Routing | ₹31 | Per prescription fill | Collect-first via Razorpay; 7-day pharmacy settlement |
| Pathology Routing | ₹71 | Per referral | Collect-first structure; same settlement model |

### Why ₹199/Month is Strategically Correct

Practo charged ₹999/month and proved why that's wrong.
- ₹199 is below psychological friction threshold
- Revenue is in transactions, not subscription
- A single psychiatrist using Vaani AI generates more monthly revenue than 10 GPs on EMR subscription

### Working Capital Advantage

**AyuVinc holds positive float always.**
- Collect-first via Razorpay before settlement
- Zero equity cost working capital
- This is a structural advantage competitors with different models cannot match

### NMC Compliance Moat on Routing

- 100% of transaction fee goes to AyuVinc platform
- Zero goes to the clinician
- This is the architecture, not a compromise
- Competitors with existing clinician-incentive structures cannot unwind without triggering churn
- AyuVinc has zero such liability

---

## 3. PATIENT IDENTITY — CRITICAL ARCHITECTURAL DECISION

### AyuVinc Does NOT Use ABHA as Primary Patient Identity

This is a confirmed strategic decision. Full rationale below.

### Why ABHA Is Not the Foundation

| Factor | Reality |
|--------|---------|
| ABHA IDs claimed | 88 crore (government-inflated) |
| Actual private clinic ABDM adoption | 17,000 out of 600,000 (2.8%) |
| ABDM milestone certification achieved | Only 4 companies |
| ABHA onboarding cost per integrator | ₹5-7 lakh + months of integration |
| M1 integrator success rate | 112 of 2,073 attempted (5.4%) |
| ABDM Scan & Pay lifetime transactions | 41,500 nationwide (zero commercial traction) |

### AyuVinc's Identity Architecture

**UUID-first approach:**
1. AyuVinc generates patient UUID on first prescription
2. ABHA fetched and linked later via separate consent flow
3. ABHA is optional, not required for system to work

### Why This Is Superior

- ✅ Zero onboarding cost for patient identity
- ✅ Works on day one without government dependency
- ✅ Scales without ABDM certification delays
- ✅ When ABHA matures, bridge retroactively on demand — no rebuild required
- ✅ Competitors who built on ABHA rails: ₹5-7 lakh + months. AyuVinc built in weeks.

### How to Position ABHA in Pitch Documents

> "ABDM is the rail we're built to run on when it matures. We don't wait for it — we generate our own patient identity and bridge to ABHA on consent when the patient has one. ABHA compliance is table stakes within 24 months. Our moat is not ABHA — it is three years of structured patient encounter data that no one can replicate by certifying tomorrow."

---

## 4. PATIENT ACTIVATION MECHANISM

This mechanism makes the patient-owned model operationally viable.

### The Flow

**Step 1:** Doctor writes prescription digitally on Dhara/Vaani  
**Step 2:** Platform generates SMS with URL to patient's phone number  
**Step 3:** URL opens mobile web page — prescription readable WITHOUT app download (zero friction)  
**Step 4:** App download prompted but optional for first access  
**Step 5:** On download, patient gets UUID, record begins building  
**Step 6:** On subsequent visits, record available to any Dhara-enabled doctor with patient consent  

### Why This Works

- No doctor behavior change required beyond writing prescription digitally
- Patient always gets their prescription — guaranteed delivery, no failure
- App download is a pull (patient wants their record, lab results, refills) not a push
- Activation happens gradually over multiple visits, not forced at visit one

### Non-Dhara Doctor Flow

Patient initiates record share FROM their own app:
1. Patient enters non-Dhara doctor's phone number
2. Non-Dhara doctor receives URL
3. Doctor opens link — clean, read-only FHIR R4 record
4. ICD-10 codes and narrative summary visible
5. No login, no registration, no app download required on doctor's end
6. **Bottom of page CTA:** "Become a Saarthi — join Dhara."

---

## 5. THE SAARTHI NETWORK — NEW STRATEGIC PILLAR

**Status:** Created in this session. Not in any existing document. **Must be added to Business Plan GTM section.**

### Definition

**Saarthi** (सारथी) = guide, companion, navigator

In AyuVinc context: **A clinician who has seen the Dhara patient record, understood the patient-owned model, and chosen to join — not because a rep sold them, but because a patient showed them.**

A Saarthi is not a user. Not a subscriber. A clinician who made a **decision**.

### Why Saarthi Is Strategically Important

#### 1. Zero-CAC Acquisition Channel

- Every active Dhara patient who visits a non-Dhara doctor = unsolicited product demo
- At 500 active clinics × 50 patients each × 2 non-Dhara doctor visits/year = 50,000 demos/year at zero cost
- Patient-delivered proof points have higher conversion than rep pitch

#### 2. Identity, Not Adoption

- "On Dhara" = customer
- "Dhara Saarthi" = advocate
- Changes IMA WhatsApp group dynamics
- Saarthis recruit Saarthis — network effect

#### 3. GTM Reframe

- KOLs are founding Saarthis
- PGI Chandigarh clinicians who join first = Saarthi Tier 1
- City launch begins with identifying 2-3 founding Saarthis before reps arrive
- Rep job shifts: not "sell" → "find next Saarthi"

#### 4. Series A Narrative

- "5,000 clinics" = a number
- "5,000 Saarthis across 8 cities" = a movement
- These are different investor conversations

### Conservative Saarthi Pipeline Math

**Assumption:** 20% of active patients share record with 1 non-Dhara doctor/year

| Milestone | Active Clinics | Active Patients | Demos/Year | @5% Conv | /Month |
|-----------|---|---|---|---|---|
| M12 | 300 | 30 avg | 1,800 | 90 | 7.5 |
| M24 | 1,000 | 50 avg | 10,000 | 500 | 42 |
| M36 | 3,500 | 60 avg | 42,000 | 2,100 | 175 |

**By M36:** 175 net new Saarthis per month from zero-CAC channel alone.

### What to Add to Documents

Create **"Saarthi Network"** section under GTM in Business Plan:

- Definition of a Saarthi
- How patient-initiated record sharing creates Saarthi pipeline
- Founding Saarthis by city by M24 (conservative estimate)
- Saarthi as the identity of the KOL programme
- The Saarthi CTA on every patient-shared record URL
- Pipeline math (shown above)

---

## 6. COMPETITIVE ASSESSMENT — CONFIRMED POSITIONS

### HealthPlix

**Status:** Vacating the independent clinic market

| Metric | Value | Context |
|--------|-------|---------|
| Raised | $43M | |
| FY25 Revenue | ₹38.4 Cr | 10.7 cents per dollar raised |
| Profitability | Loss-making | Still burning |
| ABHA Links | 25.34 lakh | Most embedded commercial EMR |
| Pricing | ₹4,200/month | Excludes Tier 2-3 independent clinics |
| AI Scribe | None | Despite 12 years and $43M |
| GTM Shift | Pivoting to enterprise | **Vacating AyuVinc's market** |
| CAC | ~₹25,000/clinic | Via DSA fleet |

**AyuVinc CAC comparison:** ₹4,500/clinic via engagement (5.5x lower)

### EkaCare

**Status:** A development centre for US parent, not commercial India competitor

| Metric | Value | Context |
|--------|-------|---------|
| Raised | $19.5M | |
| FY24 India Revenue | ₹29.5 Cr | |
| From US Parent | ₹28.12 Cr (95%) | Essentially a cost centre |
| Independent India Revenue | Under ₹1.5 Cr | Negligible |
| ASR Tech | OpenAI Whisper V3 Large | English-dominant, not built for Indian languages |
| NVIDIA Collab | Feb 2026 announcement | Not yet deployed |

### TatvaCare

**Status:** Different lane (clinic SaaS vs patient-owned OS), not direct competitor

| Metric | Value | Context |
|--------|-------|---------|
| Status | Bootstrapped | |
| FY25 Revenue | ₹13.2 Cr | |
| Employees | 286 | |
| Products | TatvaPractice (EMR) + MyTatva (DTx) | |
| Pricing | ₹1,250-5,999/month | |
| AI Scribe | No | |
| Transaction Layer | No | |
| Patient-Owned Arch | No | |

**Proof point:** India clinic market hits thin margins without transaction layer.

### The Real Threat (Not Mentioned in Current Docs)

A well-capitalised new entrant — Tata 1MG, Reliance Health, or funded startup — reads AyuVinc thesis and enters with 10x capital + existing pharmacy/lab networks.

**How we stay ahead — 18-24 month window:**

1. **Psychiatric consultation data corpus** — 3 years of unstructured data, uncopyable
2. **Saarthi network trust** — IMA relationships and peer validation, not replicable by capital
3. **Patient UUID base** — historical records; cannot be replicated by signing same clinics tomorrow
4. **NMC-compliant routing architecture** — competitors cannot retrofit without destroying clinician relationships

---

## 7. PATIENT ACTIVATION FUNNEL — CRITICAL GAP IN CURRENT DOCUMENTS

### The Problem

- Business Plan models clinic ramp as primary risk ✓
- **Patient activation rate is NOT explicitly modelled** ✗
- Pharmacy capture rate ramp (0%→65%) is doing proxy work for patient activation
- **This is a critical gap** — if only 10% of clinic patients activate (vs 50% assumption), all clinic ramp gains are negated

### What Needs to Be Added

Add **"Patient Activation Funnel"** section to Business Plan:

### Proposed Model

| Stage | Assumption | Month 6 | Month 12 | Month 24 | Month 36 |
|-------|-----------|--------|---------|---------|---------|
| Prescriptions written | 100% | 100% | 100% | 100% | 100% |
| SMS received | 95% | 95% | 95% | 95% | 95% |
| Link opened (web-first) | 85% | 85% | 85% | 85% | 85% |
| App downloaded | 35% | 40% | 50% | 60% | 65% |
| UUID generated + active | 30% | 35% | 45% | 55% | 60% |
| Consent to future doc sharing | 25% | 30% | 40% | 50% | 55% |

**Key insight:** Pharmacy capture ramp depends on activation rate. If activation slips, model must explicitly show pharmacy capture degradation.

### Copy to Include

> "Patients don't need to download the app to get their prescription. SMS delivers a web-first link; prescription is readable without app install. This removes the largest activation barrier. App download becomes optional, driven by patient pull (lab results, refill history, record sharing) rather than clinic push. Our conservative model assumes 60% app adoption and 55% UUID-active by M36. If patient activation lags clinic ramp, pharmacy capture ramp is the first impact metric, giving us early warning."

---

## 8. DOCUMENT ISSUES — MANDATORY FIXES BEFORE INVESTOR MEETINGS

### Issue 1: Two KPI Documents With Material Discrepancies

**Files:** `AyuVinc_KPI_Targets_36M.pdf` and `AyuVinc_KPI_Targets_36M.docx`

| KPI | PDF | DOCX | Delta | Impact |
|-----|-----|------|-------|--------|
| M21 cash floor | ₹250L | ₹313L | ₹63L (25% diff) | Series A timing |
| M22 net | +₹7L | +₹2.2L | ₹4.8L (69% diff) | Profitability claim |
| M12 EBITDA note | -₹27L | -₹11L | ₹16L (145% diff) | Burn rate |
| M36 cash | ₹1,715L | ₹1,115L | ₹600L (54% diff) | Exit value |

**Action Required:**
- ❌ Destroy one version completely
- ✅ Establish single canonical KPI document (DOCX supersedes PDF)
- ✅ Mark version date clearly: "Last updated: 14 May 2026"
- ✅ Add footnote: "Previous version (PDF) deprecated as of 14 May 2026. Use DOCX as canonical."

### Issue 2: Monte Carlo Failure Rate Inconsistency

**Locations:**
- Risk Dossier: 1.0% failure rate (post-working-capital correction)
- Business Plan: 17.6% probability cash negative
- Both appear in investor pack without reconciliation

**Context:** 17.6% is pre-WC-correction. Post-correction (UPI collect-first model) = 1.0%

**Action Required:**
- ✅ Add one reconciliation paragraph:

> "The model shows two failure rates depending on working capital assumptions. Initial model (pre-correction): 17.6% probability cash floor drops below ₹150L. Post-correction with UPI collect-first via Razorpay: 1.0% failure rate. The difference reflects positive float from transaction settlement. Current model uses UPI collect-first (1.0% figure). The 17.6% is documented as superseded in Risk Dossier Appendix A for completeness."

- ✅ Use **1.0% as the headline figure**
- ✅ Use **1.0%** in investor pitches
- ✅ Explain **17.6% as superseded** only if asked

### Issue 3: Contact Email — CRITICAL

**Current:** `aditya.irctc.1@gmail.com` in Risk Dossier footer

**Action Required:**
- ❌ Replace with `aditya@ayuvinc.com` in every document immediately
- ✅ Search all PDFs and DOCX for old email
- ✅ Regenerate PDFs from DOC originals if needed

---

### Issue 4: Series A Valuation Range Inconsistency

**Locations:**
- Business Plan: ₹350-450 Cr pre-money
- Risk Dossier: ₹250-350 Cr pre-money

**Context:** Risk Dossier body text is more recent and conservative.

**Action Required:**
- ✅ Use **₹250-350 Cr** as canonical Series A pre-money
- ✅ Update Business Plan to match
- ✅ Rationale footnote: "Conservative valuation assumes clinic ramp at 80% of plan. Upside case (₹350-450 Cr) available if ramp at 110% or pharma routing volume exceeds 100k fills/month by M30."

---

### Issue 5: T3 Tranche Leverage Risk

**Current Language:** T3 released when EBITDA positive (on board approval)

**Problem:** This gives investor leverage at exact moment AyuVinc needs capital

**Action Required:**

Add backstop clause language:

> "T3 (₹X Cr) releases within 90 days of EBITDA positive on majority board approval with objectively verifiable data. If EBITDA positive not achieved within 6 months of M22 target (by M28), T3 converts from EBITDA trigger to product milestone trigger (clinic count ≥1,200 or transaction volume ≥50k fills/month) at founder-investor mutual agreement, ensuring capital delivery remains independent of timing of profitability milestone."

---

### Issue 6: Patient Activation Gap (DETAILED IN SECTION 7 ABOVE)

Already addressed. See Section 7.

---

### Issue 7: Saarthi Network Missing (DETAILED IN SECTION 5 ABOVE)

Already addressed. See Section 5.

---

### Issue 8: Plan B on PGI Framing

**Current:** "PGI is load-bearing. If June doesn't convert, timeline doesn't hold."

**Problem:** Creates investor anxiety about single-point dependency

**Action Required:**

Reframe as:

> "We are raising concurrent with PGI because institutional anchors and investor conversations reinforce each other. We are NOT dependent on PGI converting to close the round — we are dependent on PGI converting to execute the Chandigarh cluster GTM in Year 1. Alternative institutional anchors identified: AIIMS Delhi AI CoE (discussion M3 2026), major private psychiatry institution in NCR (Fortis Delhi, Apollo Delhi — M4 2026), Tier 1 private hospital chain (Max Healthcare, Apollo Hospitals — M4-M5 2026). Round closes on investor conviction of market, not on PGI outcome."

---

## 9. SEED ASK — CORRECT FRAMING

### The Problem With Current Framing

**Current:** "₹9 Cr to reach 5,000 clinics"

- Investor will re-price the round up, or discount the vision
- Both outcomes are bad

### The Correct Framing

> "₹9 Cr gets us to EBITDA positive at 800 clinics by Month 22. From Month 22, the business funds its own expansion to 5,000 clinics from operating cash flow. The two planned EBITDA dips at M25-26 (metro expansion) are absorbed by Chandigarh and NCR transaction revenue — cash floor never drops below ₹500L post-T3. No additional equity required until Series A at M30-36, by which point we raise from 3,500+ clinics and consecutive EBITDA positive quarters."

### The Key Message

**The seed is not the 5,000-clinic bet. It is the proof that the 5,000-clinic bet is winnable.**

Use this in:
- Investor updates
- Board meetings
- Pitch narrative (Slide 6, Business Model)
- FAQ responses

---

## 10. VISION & DEFENSIBILITY STATEMENTS

Use these exact framings when asked in conversations.

### "What is AyuVinc building?"

> "India's 600,000 independent clinics have no memory. Every patient who changes doctor starts from zero. Every prescription is written on paper and lost. Every referral is a WhatsApp message. We are building the layer that connects India's independent clinic network around the patient — not the institution. The patient owns their record. Every Dhara-enabled doctor sees the complete clinical history from visit one. The transaction layer — pharmacy routing, pathology routing — runs on that record. The data that results is India's first longitudinal patient health dataset built on real clinical encounters, not government registrations. That dataset is the Series A asset. The OS is the seed story."

### "What makes you defensible?"

> "Three things. One: patient-owned architecture built from day one — competitors cannot retrofit this without destroying existing customer relationships. Two: three years of structured psychiatric consultation data from a PGI-anchored network — this cannot be replicated by signing the same clinics tomorrow. Three: the Saarthi Network — 5,000 clinicians who joined because a patient showed them the product, not because a rep sold them. Trust networks of that kind take years to build, not months."

---

## 11. OUT OF SCOPE FOR SEED (DO NOT ADD TO SEED DOCUMENTS)

The following are real strategic initiatives but are **Series A / Series B stories**. Do not let them dilute seed pitch:

- ❌ Cancer module
- ❌ Dialysis module
- ❌ Haath (hospital navigation marketplace)
- ❌ NOTTO national deployment (Setu is seed-stage only at PGI level)
- ❌ Proprietary clinical LLM (Series A hire, M37+)
- ❌ GPU infrastructure (M30+)
- ❌ National pharmacy chain API deals (Tata 1MG, PharmEasy — Y4-Y5)

**Exception:** Mention as exit optionality only if asked in due diligence.

---

## 12. THE ONE METRIC THAT DETERMINES EVERYTHING

From Monte Carlo: **clinic ramp speed accounts for 55.1% of all outcome variance.**

Everything in seed period is in service of one number: **net new clinics per month**

- Engagement programme spend
- KOL activation
- Saarthi network
- CME events
- Rep hiring schedule

All are ultimately accountable to this metric.

### Engagement Programme Budget (Clinic Ramp Accelerant)

| Period | Budget | Purpose |
|--------|--------|---------|
| Y1 (Seed) | ₹15L | Foundation KOL + Saarthi identification |
| Y2 | ₹72L | Clinic ramp at scale (300→1,000) |
| Y3 | ₹180L | Multi-city expansion (1,000→3,500) |

Every rupee should be evaluated against: **"How does this accelerate net new clinics per month?"**

### Board Meeting North Star

**Each board meeting, lead with:** Net new clinics added in the last 30 days vs target

**Format:**
- Target: __ clinics
- Actual: __ clinics
- % of target: __
- Runway impact: __ month change if trend continues
- Corrective actions: [if off track]

---

## 13. DOCUMENT HIERARCHY — CANONICAL ORDER

When documents conflict, resolve using this hierarchy:

1. ⭐ **This document** (most recent strategic decisions)
2. `AyuVinc_Investor_Risk_Narrative.docx` (most complete financial logic)
3. `AyuVinc_Investor_FAQ_Risks.docx` (most complete competitive logic)
4. `AyuVinc_Business_Plan_2026.docx` (primary investor document)
5. `AyuVinc_36M_Narrative.docx` (operational detail)
6. `AyuVinc_KPI_Targets_36M.docx` (canonical KPI — DOCX supersedes PDF)
7. `AyuVinc_Financial_Model.xlsx` (single source of truth for all numbers)

---

## 14. IMMEDIATE ACTION ITEMS

### Critical (Before Investor Meetings)

- [ ] **Fix Issue 3:** Replace `aditya.irctc.1@gmail.com` with `aditya@ayuvinc.com` in all PDFs
- [ ] **Fix Issue 1:** Destroy PDF KPI document; mark DOCX as canonical v14 May 2026
- [ ] **Fix Issue 4:** Align Series A valuation to ₹250-350 Cr across all documents
- [ ] **Add Section 7:** Patient activation funnel to Business Plan
- [ ] **Add Section 5:** Saarthi Network to GTM section of Business Plan
- [ ] **Fix Issue 8:** Update PGI framing in FAQ to include Plan B anchors
- [ ] **Fix Issue 2:** Add Monte Carlo reconciliation paragraph to Risk Dossier

### High Priority (Before Next Board Meeting)

- [ ] **Fix Issue 5:** Add T3 backstop clause to term sheet language
- [ ] **Update Slide 6:** Use correct seed framing ("proof the 5,000-clinic bet is winnable")
- [ ] **Add Vision Slides:** Use exact statements from Section 10
- [ ] **Competitive Slides:** Update with Issue 6 real threat assessment

### Ongoing

- [ ] North Star metric: Track net new clinics/month in real time
- [ ] Board meetings: Lead with clinic ramp vs target (Section 12)
- [ ] Engagement spend: Evaluate all cost against clinic ramp acceleration
- [ ] Saarthi tracking: Document founding Saarthis by city as they convert

---

## Document Metadata

| Field | Value |
|-------|-------|
| Created | 14 May 2026 |
| Strategy Session | AK × Claude (claude.ai) |
| Approved By | AK (Founder & CEO) |
| Distribution | Internal — Pitch development only |
| Status | Active — Foundation for all pitch updates |
| Review Cycle | Next update: June 2026 board meeting or explicit founder revision |
| Questions | Refer to original session transcript or contact AK directly |

---

*This document is the source of truth for all strategic decisions made in May 2026. Use this as the brief before editing any investor document. Conflicts between this document and other investor materials should be resolved in favor of this document.*
