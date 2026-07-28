# SDR KPIs & Compensation Strategy

**Prepared for:** Chase Anderson, SDR Team Lead
**Date:** 28 July 2026
**Data:** Bookings SDR View (1,668 SDR-owned leads, May–July 2026), full booking history,
Aircall call history (4,100 calls, 14 May – 28 July), Strategic Briefing v1.0, SDR Team Lead
Onboarding v1.0, and the live commission logic in `index.html`.

All figures below were computed by replaying the dashboard's own definitions
(`isQualifiedLead`, `isMeetingBookedStrict`, `isInstantClose`, `dealValueUSD`, Dubai day-keys)
against the raw CSVs. The replication reconciles to the July paycheque: MJ's $946 =
$1,000 meeting bracket × 0.85 quality multiplier + $96 New Sales; Gospel's $865 = $800
meeting bracket + $65 New Sales.

---

## Part 0 — The five numbers that drive everything else

| Metric | Value | Source |
|---|---|---|
| Revenue per **held** B2B meeting | **$540** | May+June cohorts, matured |
| Held meeting → closed deal | **41%** | 61 deals from 148 held meetings |
| SDR-sourced AOV | **$1,310** | vs company-wide $1,466 (SDRs work the sub-$1k tier) |
| Revenue per B2B lead | **$143** (June) | vs **$9** per B2C lead |
| 87% of revenue closes within **21 days** | confirms briefing's 86% | close-lag curve |

**A held, qualified B2B meeting is worth ~$540 of booked revenue.** That is the unit the
entire compensation plan should be priced against. Everything below flows from it.

---

## Part 1 — What should my KPIs be?

### The leading KPI: **Held Meeting Rate** — held qualified B2B meetings ÷ B2B leads assigned

| | June 2026 | July 2026 | Target |
|---|---|---|---|
| Team | 28.7% (129/449) | 21.6% (122/564) | **30%**, stretch 35% |
| MJ | 27.6% | 20.2% | |
| Gospel | 29.9% | 18.1% | |
| Mark | — | 32.7% | |
| Levi | — | 19.3% | |

*(July is a partly-immature cohort — 22 B2B meetings were still "Scheduled" at export. Adjusted
for those resolving at the historical 80% rate, July lands near 25%. The decline is real but
smaller than it first reads.)*

**Why this one:**

1. **It is the only number that is entirely yours and directly multiplies into revenue.**
   Held meetings × $540 = the revenue your team creates. Nothing else on the dashboard has
   that clean a line to money.
2. **It is a rate, not a volume.** Lead flow is set by marketing (~1,700/month), not by you.
   Measuring volume rewards you for a good month of ad spend and punishes you for a bad one.
3. **"Held" instead of "booked" closes the single biggest loophole in the current system.**
   This is the most important finding in the whole analysis:

   > Leads first touched **more than 4 hours** after arrival still get booked into meetings at
   > **23.3%** — barely below the 30.7% rate of leads touched within the hour. But they convert
   > to deals at **5.8% vs 13.1%**, and produce **$61 per lead vs $171**.
   >
   > **Booking a meeting is not the same as creating value, and the current plan cannot tell
   > the difference.** Held meetings can.

**Why not the alternatives:**

- **Meetings booked** (what the onboarding doc lists and what commission currently pays on) —
  disproven above. It is the metric most vulnerable to well-intentioned gaming.
- **% of leads qualified** — it is a *marking decision*, not an outcome. It is the single most
  manipulable field in Airtable, and the AE-disqualified rate (7–9% of qualified handoffs)
  shows it is already being stretched. Never make a self-reported field your headline number.
- **Revenue sourced** — the right goal, but the wrong dial. 87% of it lands within 21 days, so
  you learn three weeks late, and it is co-owned with seven AEs (five of whom are under six
  months' tenure). You cannot run a Monday standup on it.
- **Dials / activity** — actively misleading here. June B2B leads that took **1 dial** booked
  meetings at 54% and produced $251/lead; leads that took **7+ dials** booked at 7% and produced
  $20/lead. More dialling is a symptom of a dead list, not a sign of effort. Gospel made 842
  July dials at a 6.8% connect rate; Levi made 349 at 51.9%. Dial counts would rank them
  exactly backwards.

---

### Supporting metric 1 (upstream): **Speed-to-Lead Compliance — % of B2B leads first touched within 1 hour**

May+June cohorts, matured, B2B only, first outbound Aircall call matched to lead by phone:

| First touch | Share of leads | Held rate | Lead → deal | **Revenue per lead** |
|---|---|---|---|---|
| Within 1 hour | 74% | 30.7% | 13.1% | **$171** |
| 1–4 hours | 9% | 23.4% | 12.8% | **$203** |
| Over 4 hours / never called | 17% | 23.3% | **5.8%** | **$61** |

Current compliance (within 20 min, July): MJ 72%, Gospel 74%, Mark 66%, Levi 66%.
Tail (>4h or never): 13–21% per SDR. Levi never called 16% of his assigned leads at all.

**Target: 90% within 1 hour; tail below 8%.**

**The counter-intuitive part — do not build a five-minute culture.** Sub-5-minute dialling
performs *worse* than a 5–60 minute response, and it holds for each SDR individually, so it is
not a mix artefact:

| | 0–5 min | 5–60 min |
|---|---|---|
| MJ | $130/lead (n=54) | **$264/lead** (n=123) |
| Gospel | $92/lead (n=153) | **$226/lead** (n=51) |

The most plausible read: an instant dial is a dial made *before reading the enquiry*. The brief,
the city, the shoot date and the budget tier are all in the record. Ninety seconds of reading
appears to be worth more than four minutes of speed. **The rule to coach is "nothing sits past
the hour," not "call in five minutes."** This is worth validating with call recordings before
it becomes policy.

This closes the loop back to the briefing's headline: *"Not responsive" accounts for 29% of all
leads, the largest leak in the funnel by far.* This metric is that leak, measured from your side.

---

### Supporting metric 2 (downstream): **Held Meeting → Deal Rate**

| | Value |
|---|---|
| May+June (matured) | **41.2%** (61 deals / 148 held meetings) |
| MJ, June | 45% |
| Gospel, June | 30% |
| AE-disqualified rate (early tripwire) | MJ 7.1%, Gospel 9.3%, Levi 7.7%, Mark 0% |

**Why you need it:** the leading KPI can be pushed up by lowering the bar on what counts as a
meeting. This is the metric that catches that, and it is the one your AEs feel. If held meeting
rate rises while this falls, you are manufacturing volume and spending AE hours — the genuinely
scarce resource, given five of seven AEs are still ramping.

Use **AE-Disqualified %** as the fast-twitch version: it surfaces within days rather than
waiting 21 for the close. Alarm threshold 10%; Gospel is already at 9.3%.

---

### What to drop

Your onboarding doc lists six KPIs: hiring milestones, team meetings booked, % leads qualified,
speed-to-lead, lead coverage, handoff quality. Three of those are load-bearing (speed, coverage,
handoff quality) and are captured above. **Meetings booked** and **% qualified** should come off
the scoreboard as headline numbers for the reasons above — keep them visible as diagnostics, not
as things anyone is judged or paid on. **Hiring milestones** are a project plan, not a KPI; track
them on the gate review, not the weekly.

---

## Part 2 — Compensation

### 2.1 What is wrong with the current plan

Total pay = Base + discretionary Bonus + Qualified Leads Incentive + Meeting Set Incentive +
New Sales Incentive, with a Meeting Quality Multiplier scaling the first two incentives.

**Problem 1 — The Qualified Leads Incentive is dead.** Its floor is a 40% qualification rate.
MJ and Gospel run 28–35%. In six SDR-months it paid out twice, both in low-volume months
(Gospel's 2-week May, Mark's first July). A component that never fires teaches nothing, but it
does quietly reward marking leads qualified — the exact behaviour the AE-DQ rate polices.

**Problem 2 — The Meeting Incentive is already maxed out, so it has stopped being an incentive.**
MJ booked at 41.3% in June; the top bracket starts at 40% and pays $1,000. His marginal reward
for the 94th meeting was **$0**. Ninety-one percent of his variable pay came from a bracket he
had already saturated. The plan's main lever currently has no headroom at all.

**Problem 3 — The brackets are cliffs.** Gospel's June rate was 40.2%. At 39.9% she earns $800;
at 40.0%, $1,000. One meeting was worth $200. Cliffs invite month-end marking games and feel
arbitrary in a 1:1.

**Problem 4 — It pays on booked, not held.** Quantified in Part 1: booking is nearly
speed-independent, value is not.

**Problem 5 — The revenue link is a rounding error.** New Sales pays 0.25% — $96 for MJ, $65 for
Gospel. It is the *only* component tied to money and it is 4–9% of variable pay. Right now an SDR
has no financial reason to prefer a $3,000 multi-city shoot over a $600 headshot session.

**Problem 6 — The rate denominators are asymmetric.** Qualified and meetings are counted from
B2B **+ B2C** leads but divided by **B2B leads only**. This inflates every rate by 4–15 points and
pays the same for work worth $78/lead and work worth $9/lead:

| | Meeting rate as paid | Meeting rate, B2B only | Bracket swing |
|---|---|---|---|
| MJ, June | 41.3% → $1,000 | 33.8% → $600 | **$400/month** |
| Gospel, June | 40.2% → $1,000 | 33.0% → $600 | **$400/month** |
| Mark, July | 56.4% | 41.6% | |

**Problem 7 — The quality multiplier is uncomputable by the person it applies to.** It runs on a
30-day window ending *one week ago*, which never matches the payout month. The logic is sound —
punish habitual no-shows, not one bad week — but an SDR cannot reconstruct their own number.
Compensation nobody can calculate does not change behaviour; it just generates disputes.

**The combined effect, in one line:** in July, Mark earned the top meeting bracket on $486 of
closed revenue while MJ earned a lower bracket on $8,156 — sixteen times the revenue.

---

### 2.2 The business constraints this has to respect

1. **Lead flow is fixed and not yours.** ~1,700/month, set by marketing. Pay for conversion of
   what arrives, never for volume that arrives.
2. **AE time is the real bottleneck, not leads.** Seven AEs, five under six months. A junk
   meeting consumes the scarce resource. The plan must price *quality*, not just throughput.
3. **The plan must get cheaper per dollar as it works.** Model below: comp falls from 15.0% of
   sourced revenue at a 20% held rate to 9.9% at 40%. Good plans self-fund.
4. **The SDR tier is deliberately the low-value tier** ($1,310 AOV vs $1,466 company-wide).
   Do not set revenue targets that push SDRs to cherry-pick and abandon the sub-$1k flow —
   working that tier *is* the mandate.
5. **B2C is a free pool but not a valuable one.** $9/lead vs $78. Worth working, worth paying for
   — at roughly 40% of the B2B rate, not parity.

### 2.3 The target number

July's paycheque, as earned (adding back MJ's $700 advance, which was a repayment, not lower
earnings): **$7,811**. Your +10% target is **≈ $8,600/month** for the four-person team.

---

### 2.4 Three structures

All three keep base salaries unchanged, drop the Qualified Leads Incentive entirely, pay on
**held** meetings with **B2B-only** denominators, and replace the multiplier with a legible gate.

**Quality gate (all options)** — replaces the Meeting Quality Multiplier. Same intent, computed
on the payout month itself so the SDR can check it:

| Trailing 60-day B2B no-show + rejection rate | Gate |
|---|---|
| Under 20% | ×1.00 |
| 20–30% | ×0.75 |
| Over 30% | ×0.50 |

Sixty days rather than thirty, ending at month-end rather than a week short, so it reacts to
patterns and can be reproduced by hand.

---

#### **Option 1 — "Held & Sold"** *(recommended)*

- **$15** per held qualified **B2B** meeting
- **$6** per held **B2C** meeting
- **1.0%** of closed revenue from own-created leads (4× the current rate)
- × quality gate on the meeting component only

Linear, no cliffs, no cap, no denominators. An SDR can compute it on a napkin: *"fifteen dollars
for every meeting that actually happens, plus one percent of everything I close."*

$15 per held meeting = **2.8% of the $540 that meeting generates**.

#### **Option 2 — "Held-Rate Tiers"**

Keeps the familiar bracket format but on **held rate, B2B both sides**, with the top end extended
so headroom exists: <15% → $0 · 15–20% → $250 · 20–25% → $400 · 25–30% → $600 · 30–35% → $850 ·
35–40% → $1,150 · **40%+ → $1,500**. Plus **0.75%** of closed revenue, × the gate.

More predictable cost, easier to sell as "the same plan, fixed." But it keeps the cliffs, and it
still rewards a small denominator — it pays Mark $854 on $486 of July revenue, where Option 1
pays $530.

#### **Option 3 — "Revenue-Led"**

**$6** per held B2B meeting + **2.5%** of closed revenue. Maximum business alignment. Rejected as
primary: it makes an SDR's pay hostage to AE close rates (which range 10%–18% by AE) and to the
21-day close lag, and it under-rewards the volume grind that *is* the job. At plan it delivers
only +3%, missing your target.

---

### 2.5 What each pays

| | June actual | July actual | **August at plan** |
|---|---|---|---|
| **Current plan** | $4,511 | $6,818 | $8,682 |
| **Option 1 (recommended)** | $5,410 | $7,020 | **$8,790  (+12.5%)** |
| Option 2 | $4,383 | $6,871 | $8,544  (+9.4%) |
| Option 3 | $5,084 | $6,252 | $8,042  (+3.0%) |

*"August at plan" = 4 SDRs, 175/175/150/150 B2B leads, held rate 30%/30%/28%/28%, no-show 15–18%,
revenue $130/$90 per B2B lead → $72,500 sourced revenue. Total comp = 12.1% of sourced revenue.*

Per person under Option 1 at plan: MJ $2,244 · Gospel $2,544 · Mark $1,901 · Levi $2,101.

**The 10% raise is available but it is not automatic.** At July's actual performance Option 1
pays $7,020 — *below* today. It pays 10%+ only when the team gets back to June's conversion at
July's volume. That is the correct design: the raise is funded by the performance that pays for it.

### 2.6 Cost control

| Scenario | Sourced revenue | Total comp | **Comp as % of revenue** |
|---|---|---|---|
| Held rate 20% | $51,552 | $7,710 | 15.0% |
| Held rate 25% | $64,440 | $8,326 | 12.9% |
| Held rate 29% (June) | $74,750 | $8,819 | 11.8% |
| Held rate 35% | $90,216 | $9,559 | 10.6% |
| Held rate 40% | $103,103 | $10,175 | **9.9%** |
| Lead flow +60% | $119,600 | $10,964 | 9.2% |

The ratio improves monotonically as the team performs. There is no scenario in this range where
the plan runs away from you.

---

### 2.7 Implementation notes

1. **Grandfather July.** Pay July on the old plan. Announce the new one for August with the
   brackets published in advance.
2. **Ramp guarantee for new hires.** Month 1 at 100% of target variable, month 2 at 50%, month 3
   at zero. Mark and Levi's $450 guarantees expire before they have a mature cohort; two more
   Coordinators are coming to reach the team of six. Make the ramp a written policy rather than a
   monthly discretionary call.
3. **Keep the one-month lag** — it is correct, and the close-lag curve proves it: only 63.7% of
   revenue has closed by day 7, 86.8% by day 21. Running commission 3–4 weeks into the following
   month captures ~89%.
4. **Consider a small team gate** ($150/person when team held rate ≥28% *and* speed compliance
   ≥85%). You run two time zones with overnight round-robin routing; nothing currently pays anyone
   to cover a teammate's leads.
5. **Fix the denominator bug regardless of which option you pick.** Counting B2C in the numerator
   and B2B in the denominator is worth ~$400/SDR/month of unearned incentive today.

---

## Part 3 — Open questions

These would sharpen the calibration; none of them block adopting the KPI framework.

1. **Gross margin per shoot.** Everything above is priced against *revenue*. With the
   four-component cost model (operator, equipment, on-site time, editing), a 35% vs 55% margin
   changes what the team can afford by roughly a third. This is the single biggest unknown.
2. **Is AE capacity actually free?** Stephan, Khalil and Savio each absorbed 56–69 qualified
   handoffs over June–July. If the AEs are already saturated, more meetings has *negative*
   marginal value and the plan should weight revenue higher than Option 1 does.
3. **Why did July soften?** Held rate fell for both tenured SDRs while region mix shifted from
   95% NA to 62% NA / 30% EUR. The briefing has rest-of-world converting at 11% vs North America's
   16%. If this is mix, targets should be set per desk. If it is coaching, it is fixable.
4. **Contract structure.** Are the SDRs contractors on fixed monthly base? Any local minimums, and
   is everything USD? Affects how aggressive the variable share can be.
5. **Was MJ's $700 advance a one-off,** or should the plan carry a formal draw mechanism?
6. **Your own incentive beyond month 3** — the onboarding doc defers it. It should be built on the
   same leading KPI, or you and the team will be optimising different things.
