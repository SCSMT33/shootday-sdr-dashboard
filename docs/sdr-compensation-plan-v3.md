# SDR KPIs & Compensation — Proposal

**For:** Chase Anderson, SDR Team Lead · **Date:** 28 July 2026 · **Supersedes:** v1, v2

**Data:** 1,668 SDR-owned leads (May–July 2026), 4,100 Aircall records, full booking history,
the Strategic Briefing, the Team Lead Onboarding doc, and the live commission code.
Every figure was produced by replaying the dashboard's own definitions against the raw CSVs;
the replication reconciles exactly to the July paycheque, so these are real numbers.

**Three one-page summaries are at the back:** A (SDR plan, internal, with the math),
B (SDR plan, team-facing, ready to send), C (your plan, ready to take to Serge).

---

## Part 0 — The numbers everything rests on

| | Value | Basis |
|---|---|---|
| Revenue per **held** B2B meeting | **$547** | May+June matured |
| Held meeting → closed deal | **42.5%** | 54 deals from 127 held meetings |
| Revenue per qualified **no-meeting** handoff | **$278** | exactly half a held meeting |
| SDR-sourced AOV | **$1,287** | vs $1,466 company-wide (SDRs work the sub-$1k tier) |
| Revenue per B2B lead / per B2C lead | **$143 / $9** | June, matured |
| Cost per held meeting (June actual) | **$29.87** | against $547 of revenue |
| 87% of revenue closes within 21 days | matches briefing's 86% | close-lag curve |

**A held B2B meeting is worth $547 and costs $30 to produce.** That 18:1 ratio is why there is
room to pay more, and it is the number to defend as the team scales.

**Cost-per-lead, clarified** — you asked whether June's $4,511 covered four people. It did not.
June was **MJ and Gospel only**; Mark and Levi started in July.

| | SDRs | Comp | Leads | Cost/lead | Cost/qualified | Cost/held mtg | Comp ÷ revenue |
|---|---|---|---|---|---|---|---|
| June | 2 | $4,511 | 652 | $6.92 | $29.68 | $29.87 | **5.7%** |
| July | 4 | $6,818 | 915 | $7.45 | $35.88 | $51.26 | 26.9% |

Revenue here includes instant closes, per your decision. That alone moves June from 7.0% to
**5.7%** — real headroom that did not exist in v2.

---

## Part 1 — Your KPIs

### Primary: Team B2B Lead → Deal Rate

| Month | B2B leads | Closed | Lead→deal |
|---|---|---|---|
| May | 66 | 13 | 19.7% |
| **June** | 449 | 48 | **10.7%** |
| July | 564 | 16 | 2.8% *(immature)* |
| Company benchmark | | | 14.2% |

Your call, and it is the right one. It is the whole machine in one number and no marking decision
can move it. Read it matured — prior month, run 3–4 weeks later, same timing as commission.

### Supporting 1: Team Non-Response Rate — you were right about this

You flagged it and the data backs you hard. It is the briefing's single biggest leak (29% of all
company leads) and it tracks almost perfectly inverse to output:

| Month | SDR | B2B leads | **Non-response** | Held rate | Rev/B2B lead |
|---|---|---|---|---|---|
| June | MJ | 225 | 32.9% | 27.6% | $176 |
| June | Gospel | 224 | 36.6% | 29.9% | $147 |
| June | **Team** | 449 | **34.7%** | 28.7% | $161 |
| July | Mark | 101 | **26.7%** ← best | **32.7%** ← best | $7 |
| July | MJ | 178 | 38.2% | 20.2% | $49 |
| July | Levi | 119 | 45.4% | 19.3% | $27 |
| July | Gospel | 166 | **55.4%** ← worst | **18.1%** ← worst | $58 |
| July | **Team** | 564 | **42.7%** | 21.6% | $39 |

Lowest non-response = highest held rate, every time, in both directions. Team NR went 34.7% →
42.7% between June and July, and held rate fell with it. Company baseline is 29%; **the team is
5–14 points worse than the company average on the metric the briefing calls the biggest leak in
the funnel.** That is your headroom, and it is why it sits in your comp plan (Part 4).

One caveat to keep in mind: non-response and held-meeting rate are partly mirrors of each other —
a lead is either engaged or it isn't. NR is the better *coaching* number because it names the
failure directly; held rate is the better *scoreboard* number because it counts the win.

### Supporting 2: Team Held Meeting Rate

June 28.7%, July 21.6%. The leading half of your primary KPI: *lead→deal = held meeting rate ×
held-to-deal rate*. When lead→deal moves, this tells you whether the cause was your team's
throughput or the AEs' closing.

### Diagnostics — track, don't get paid on

**Speed-to-lead.** You were right to keep it off your scorecard; it is too noisy month to month.
But the evidence is strong and it drives non-response: leads touched within 1 hour produce
**$171/lead**; leads touched after 4 hours produce **$61** and close at 5.8% instead of 13.1%.
Critically, those slow leads *still get booked into meetings at 23.3%* — which is exactly why the
old plan, which paid on booked meetings, could not tell good work from bad.

Coach **"nothing sits past the hour,"** not "call in five minutes" — sub-5-minute dialling
underperforms a 5–60 minute response for both tenured SDRs individually (MJ $130 vs $264/lead;
Gospel $92 vs $226). The likely cause is dialling before reading the enquiry.

**Never use dial counts.** June leads needing 1 dial produced $251/lead; leads needing 7+ produced
$20. In July Gospel made 842 dials at a 6.8% connect rate, Levi 349 at 51.9%. Activity metrics
rank them backwards.

---

## Part 2 — What is wrong with the current plan

| Problem | Evidence | Fix in v3 |
|---|---|---|
| **Qualified Leads Incentive is dead** | 40% floor vs 28–35% actual. Fired twice in six SDR-months | Removed |
| **Meeting Incentive is maxed out** | MJ booked 41.3% in June; top bracket starts at 40%. His marginal reward for meeting #94 was **$0** — and 91% of his variable came from that saturated bracket | Uncapped top tier |
| **Pays on booked, not held** | >4h leads book at 23.3% but close at 5.8% vs 13.1%. Booking is nearly speed-independent; value is not | Held meetings only |
| **$200 cliffs** | Gospel's June rate was 40.2%. At 39.9% he earns $800; at 40.0%, $1,000 | 1.5-pt bands, max $55 step |
| **B2C inflates the rate** | Numerator counts B2B+B2C, denominator B2B only — inflates rates 4–15 points, worth ~$400/SDR/month | B2C on its own line |
| **Small books win** | July: Mark earned the top bracket on **$486** of revenue; MJ earned a lower one on $8,156 | Volume factor |
| **Revenue link is noise** | 0.25% paid MJ $96 — 9% of variable. No reason to prefer a $3,000 shoot over a $600 one | 0.5% |
| **Multiplier is uncomputable** | 30-day window ending *a week ago*, never matching the payout month | Removed entirely |

**Why the no-show multiplier is gone.** Paying on *held* meetings already prices a no-show at the
full value of the meeting. A second penalty on top double-counts the same event — and, as you
said, no-show recovery now sits with the SDR anyway.

---

## Part 3 — The SDR plan

### 3.1 Credits

```
Credits    = held B2B meetings + 0.5 × qualified B2B leads with no meeting
Credit Rate = Credits ÷ B2B leads assigned
```

**Both sides B2B only.** No new Airtable state, no new marking convention — the no-meeting
component uses the qualified definition you already have: *Hot, Warm, Closed, Lost, Qualified_SDR,
or any refund status, with no Meeting Status set.*

**Why 0.5:** those handoffs are worth **$278/lead against $547** for a held meeting — 51%. The
data set the weight, not a negotiation. Re-check it in 90 days once volume builds.

**No cap**, per your call. The gaming risk is real but self-limiting: when an AE bounces a lead it
becomes `Disqualified AE`, which is **not** in your qualified set, so the SDR loses the credit
automatically. Verified in the data — no AE-disqualified lead counts as qualified anywhere.
Watch one number monthly: if anyone's no-meeting credits exceed ~30% of their total credits,
look at their marking. Today the highest is MJ at 8%.

### 3.2 The tier table

| Credit rate | Tier | | Credit rate | Tier |
|---|---|---|---|---|
| under 18% | $0 | | 30 – 31.5% | **$655** |
| 18 – 19.5% | $250 | | 31.5 – 33% | $705 |
| 19.5 – 21% | $300 | | 33 – 34.5% | $760 |
| 21 – 22.5% | $350 | | 34.5 – 36% | $810 |
| 22.5 – 24% | $400 | | 36 – 37.5% | $860 |
| 24 – 25.5% | $455 | | 37.5 – 39% | $910 |
| 25.5 – 27% | $505 | | **39%+** | **$960 + $55 per credit above 39%** |
| 27 – 28.5% | $555 | | | |
| 28.5 – 30% | $605 | | | |

**Why the floor is 18%, not 20%.** In the old plan 20% was arbitrary. Here it is derived: at $547
per held meeting and a 7% cost target, an SDR on a $1,200 base needs ~31 held meetings to cover
their own base. On a 175-lead book that is **17.9%**. Below the floor the SDR is not yet paying
for themselves.

**Why it never caps.** Above 39% the tier becomes $55 per additional credit, uncapped — the direct
fix for the flaw that made the old plan pointless at the margin.

### 3.3 The other three components

**Volume factor: `min(1.0, B2B leads ÷ 160)`**, applied to the tier only.

You asked me to choose between the plan's 275/Coordinator and the reality of ~175. **I chose 160**
— just below the delivered range so a normally-loaded SDR is unaffected (June 225/224 → 1.00; July
MJ 178, Gospel 166 → 1.00), while a materially under-loaded one is pro-rated (Mark's 101 → 0.63).
Using 275 would zero out everyone's tier for a routing decision they don't control; using 175
would penalise a normal month. Revisit when routing actually moves toward capacity.

**B2C kicker: $12 per held B2C meeting.** Its own line, never touching the rate. This answers your
question directly: B2C is worth **$9/lead against B2B's $78**, so paying it inside the same rate
meant paying full price for an eighth of the value. On its own line it stays worth chasing — free
leads, no media cost — without ever distorting the main number.

**Revenue share: 0.5% of closed revenue** on own-created leads. Your instinct was right at 1%: MJ's
June revenue would have paid $384, roughly 40% of his variable, arriving weeks late from a deal an
AE closed — exactly the "I've banked enough, I can ease off" money. At 0.5% it pays $222: enough
that a $3,000 multi-city shoot feels different from a $600 headshot, not enough to coast on.
The tier motivates; the revenue share steers.

**AE-disqualified gate**, on the tier only: under 10% → ×1.00 · 10–15% → ×0.90 · over 15% → ×0.75.
Computed on the payout month and reproducible by hand. Current rates: MJ 5.6–8.3%, Gospel
7.2–10.4%, Mark 0%, Levi 7.1%.

### 3.4 What it pays

**June 2026 — the reference month:**

| SDR | B2B | Held | No-mtg | Credits | Rate | Tier | B2C | Rev | **Variable** | Was | **Δ** | Total |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| MJ | 225 | 62 | 11 | 67.5 | 30.0% | $655 | $132 | $222 | **$1,009** | $946 | **+7%** | $2,209 |
| Gospel | 224 | 67 | 6 | 70.0 | 31.2% | $655 | $132 | $171 | **$958** | $865 | **+11%** | $2,458 |
| **Team** | 449 | 129 | | | | | | | **$1,967** | $1,811 | **+9%** | **$4,667** |

Comp ÷ revenue **5.9%** · cost/lead **$7.16** · cost/qualified **$35.36** · cost/held **$36.18**.

**July 2026 — for reference only, not a benchmark.** MJ $371, Gospel $321, Mark $546, Levi $287.
That is well below the old plan, and it should be: July's variable was largely a $1,000 bracket
paid on *booked* meetings that didn't convert. July's revenue component is also understated — the
cohort averages 12 days old, and only ~68% of its revenue has landed. Note the volume factor
working as intended: Mark's 33.2% rate on a 101-lead book earns $480 rather than $760, and he now
ranks behind MJ instead of topping the team on $486 of revenue.

### 3.5 Cost across performance levels

Four SDRs, 175 B2B leads each, $600 revenue per held meeting:

| | Credit rate | Team revenue | Variable/SDR | **as % of base** | Total comp | **Comp ÷ rev** |
|---|---|---|---|---|---|---|
| Poor (July-like) | 22.9% | $86,400 | $628 | 49% | $7,612 | 8.8% |
| Below target | 26.9% | $103,200 | $754 | 59% | $8,116 | 7.9% |
| **June level** | **32.6%** | **$127,200** | **$984** | **77%** | **$9,036** | **7.1%** |
| Strong | 36.6% | $144,000 | $1,160 | 91% | $9,740 | 6.8% |
| **Very strong** | **40.0%** | **$158,400** | **$1,374** | **108%** | **$10,596** | **6.7%** |
| Exceptional | 43.4% | $172,800 | $1,722 | 135% | $11,988 | 6.9% |

**Your "double their pay if they kill it" is built in.** Variable passes 100% of base at a 40%
credit rate — total pay doubles. That is 9 points above June, genuinely exceptional, and reachable.

**And 7% holds.** The ratio *improves* as they perform, bottoming at 6.7%. It only breaches 8% in
a poor month, which is the plan telling you the truth rather than hiding it.

### 3.6 On the 7% target

You agreed it is a revenue target, not a comp lever, and the arithmetic confirms it. Fixed base for
four SDRs is **$5,100/month** — spent before anyone books anything. For total comp to sit at 7%
while paying a competitive variable, the team needs roughly **$130,000/month** of sourced revenue.
June ran at $39,299 per SDR; four at that level produce $157,000. **Hitting 7% and ramping Mark and
Levi to June productivity are the same objective.**

---

## Part 4 — Your plan

**The pitch to Serge is cost-neutral at status quo.** You are paid $3,500 base plus a $1,000
guarantee that expires after August. Proposal: **fold it into a flat $4,500 base** — the company
pays exactly what it pays today — **and add variable that pays nothing unless the business
improves.** Serge only pays more when he gets more.

**Base $4,500. Variable $0 at status quo, up to ~$3,000 (66%) at exceptional.**

**1 — Team B2B lead→deal rate** *(matured, prior month)*

| Rate | Payout | |
|---|---|---|
| under 11% | $0 | ← June was 10.7% |
| 11 – 12.5% | $300 | |
| 12.5 – 14% | $600 | |
| 14 – 15.5% | $950 | ← company benchmark 14.2% |
| 15.5 – 17% | $1,250 | |
| 17%+ | $1,500 | |

**2 — Team non-response rate** *(B2B)*

| Rate | Payout | |
|---|---|---|
| 34%+ | $0 | ← June 34.7%, July 42.7% |
| 31 – 34% | $200 | |
| 28 – 31% | $400 | ← company baseline 29% |
| 25 – 28% | $600 | |
| under 25% | $800 | |

**3 — Revenue override: 1.0% of team revenue above ($40,000 × active Coordinators)**

The threshold scales with headcount deliberately — it pays for *productivity per head*, never for
hiring. $40,000 is just above June's $39,299 per SDR, so adding a body earns you nothing until
they produce.

| Scenario | Lead→deal | Non-resp | SDRs | Team revenue | Variable | **Total** | % of base |
|---|---|---|---|---|---|---|---|
| **Status quo (June × 4)** | 10.7% | 34.7% | 4 | $157,196 | **$0** | **$4,500** | 0% |
| Modest gain | 12.0% | 32.0% | 4 | $175,000 | $650 | $5,150 | 14% |
| Good | 13.5% | 30.0% | 4 | $200,000 | $1,400 | $5,900 | 31% |
| Very strong | 15.0% | 27.0% | 4 | $225,000 | $2,200 | $6,700 | 49% |
| **Exceptional** | 16.5% | 24.0% | 4 | $250,000 | **$2,950** | **$7,450** | **66%** |
| Outstanding (6 SDRs) | 17.5% | 23.0% | 6 | $360,000 | $3,500 | $8,000 | 78% |

**No hiring milestones** — per your call, building the team is the role, not a bonus.

**Alignment:** they are paid for *producing* meetings, you for what those meetings *become*.
Neither of you can win by pushing volume that doesn't close.

---

## Part 5 — Rollout and two things to check

### The timeline is safe

| Paid | Covers | Plan |
|---|---|---|
| **August** | July performance | **Old plan** — already worked, unchanged |
| **September** | **August performance** | **New plan** |

Nothing is retroactive. The one hard deadline: **the team needs the new rules before 1 August**,
or they spend August optimising for a plan that no longer exists. Appendix B is written to send.

### The duplicate/wrong-info filter — working, but currently catching nothing

You asked me to confirm bad leads are excluded from the math. **The code is correct**:
`isLeadExcluded()` (`index.html:3270`) drops any lead whose Disqualified reason is *Duplicate
record* or *Wrong info*, and `commissionMetricsForSDR` filters those rows out **before any count**
— so they never appear in leads, qualified, meetings or revenue. Both sides of every ratio.

**But it currently matches zero leads.** Across all 1,668 SDR leads in May–July, not one carries
either reason. The reasons actually in use are: Not responsive (397), Just browsing (158), Price
sensitive (130), Found other alternative (78), Session canceled (67), Stopped responding (27),
We don't provide the service (27).

So either the team isn't using those options, or Airtable spells them differently. **Worth checking
the Airtable option list** — the guard is real but it is guarding nothing today.

### Also confirmed

Your qualified definition is already the live one everywhere that pays: `STRICT_QUALIFIED_STATUSES`
(`index.html:3260`) drives `isQualifiedLead`, which the Summary Cards, charts, Mandate Scoreboard,
Capacity & Cost and the Commission Calculator all call. A second, broader list exists at line 3136
but is used **only** by Data Hygiene, which is flagged in-code as under construction and
deliberately frozen. It touches no payout. Last month's rates are already on the current
definition, so nothing needs restating.

### Open

**July's softness is still unexplained** — held rate fell for both tenured SDRs while region mix
moved from 95% North America to 62% NA / 30% Europe, and the briefing has rest-of-world converting
at 11% against NA's 16%. Your read is holidays and summer slowdown, and July is not used as a
benchmark anywhere in this plan. But if the cause is regional mix rather than seasonality, the
tier thresholds should eventually differ by desk. Revisit at the quarterly re-benchmark (end of
October), by which time August and September will have settled it.

---
---

# Appendix A — SDR Plan, Internal

**Effective:** August performance, paid September. Grandfathered: July paid on the old plan.

### The formula

```
Credits      = held B2B meetings + 0.5 × qualified B2B leads with no meeting
Credit Rate  = Credits ÷ B2B leads assigned
Volume Factor = min(1.0, B2B leads ÷ 160)

VARIABLE = Tier(Credit Rate) × Volume Factor × AE-DQ Gate
         + $12 × held B2C meetings
         + 0.5% × closed revenue on own leads

TOTAL PAY = Base + Variable
```

| Credit rate | Tier | Credit rate | Tier |
|---|---|---|---|
| under 18% | $0 | 30 – 31.5% | $655 |
| 18 – 19.5% | $250 | 31.5 – 33% | $705 |
| 19.5 – 21% | $300 | 33 – 34.5% | $760 |
| 21 – 22.5% | $350 | 34.5 – 36% | $810 |
| 22.5 – 24% | $400 | 36 – 37.5% | $860 |
| 24 – 25.5% | $455 | 37.5 – 39% | $910 |
| 25.5 – 27% | $505 | **39%+** | **$960 + $55/credit above 39%** |
| 27 – 28.5% | $555 | | |
| 28.5 – 30% | $605 | | |

AE-DQ gate: under 10% → ×1.00 · 10–15% → ×0.90 · over 15% → ×0.75.

### Why each number

| Parameter | Value | Derivation |
|---|---|---|
| No-meeting weight | **0.5** | $278/lead vs $547 for a held meeting = 51% |
| Tier floor | **18%** | $1,200 base ÷ 7% ÷ $547 per meeting ≈ 31 meetings on a 175-lead book |
| Volume reference | **160** | Just below delivered range (June 224–225, July 166–178); pro-rates only under-loaded books |
| B2C rate | **$12** | B2C is $9/lead vs B2B $78 — pays for the meeting, never distorts the rate |
| Revenue share | **0.5%** | 1% would be ~40% of variable, arriving late from an AE's close |
| Top tier | **$960 + $55** | Variable passes 100% of base at a 40% credit rate → pay doubles |

### Calibration against actuals (June, the reference month)

| SDR | B2B | Held | No-mtg | Rate | Tier | B2C | Rev | Variable | Was | Δ |
|---|---|---|---|---|---|---|---|---|---|---|
| MJ | 225 | 62 | 11 | 30.0% | $655 | $132 | $222 | $1,009 | $946 | **+7%** |
| Gospel | 224 | 67 | 6 | 31.2% | $655 | $132 | $171 | $958 | $865 | **+11%** |

Team comp ÷ revenue **5.9%**. Cost per held meeting **$36.18** against $547 of revenue generated.

**Cost control** (4 SDRs, 175 leads each) — comp ÷ revenue: poor month 8.8% · June level 7.1% ·
very strong **6.7%** · exceptional 6.9%. Variable passes **108% of base** at a 40% credit rate, so
pay doubles at genuinely exceptional performance. The ratio improves as they perform and only
breaches 8% in a bad month.

**Watch monthly:** (1) no-meeting credits as a share of total credits — investigate above ~30%,
today's max is 8%; (2) AE-disqualified rate — Gospel at 10.4% and drifting; (3) whether the volume
factor is biting anyone who should be at 1.0 — reset the 160 reference if routing changes.

---
---

# Appendix B — SDR Compensation, effective August

**Your pay = Base + Variable.** Your base does not change. Everything below is the variable.

### What you earn on

Your work is measured on **credits**, from the B2B leads assigned to you:

- **1 credit** for every meeting that actually happens (Meeting Status = *Meeting Done*)
- **½ credit** for a lead you qualify and hand to an AE where no meeting is needed — the ones
  where the client says *"just email me"* and it still goes somewhere

**Your Credit Rate = your credits ÷ your B2B leads.** That rate sets your tier:

| Credit rate | You earn | Credit rate | You earn |
|---|---|---|---|
| under 18% | $0 | 30 – 31.5% | $655 |
| 18 – 19.5% | $250 | 31.5 – 33% | $705 |
| 19.5 – 21% | $300 | 33 – 34.5% | $760 |
| 21 – 22.5% | $350 | 34.5 – 36% | $810 |
| 22.5 – 24% | $400 | 36 – 37.5% | $860 |
| 24 – 25.5% | $455 | 37.5 – 39% | $910 |
| 25.5 – 27% | $505 | **39% and above** | **$960, plus $55 for every extra credit** |
| 27 – 28.5% | $555 | | |
| 28.5 – 30% | $605 | | |

**There is no cap.** Past 39% every additional credit pays $55. If you have an outstanding month,
your variable can exceed your base — your pay doubles.

### Plus two more things

- **$12 for every B2C meeting held.** Separate from everything above. B2C leads are free to the
  company, so every one you convert is upside.
- **0.5% of the revenue** from deals that close on your leads. A $3,000 shoot pays more than a
  $600 one.

### Two things that reduce it

- **If you handle fewer than 160 B2B leads in a month**, your tier is pro-rated to the leads you
  actually worked (e.g. 120 leads → 75% of the tier). A high rate on a small book isn't the same
  achievement as a high rate on a full one.
- **If more than 10% of what you hand over gets bounced back** by an AE as wrongly qualified, your
  tier is reduced (10–15% → 90%, over 15% → 75%). Everyone is comfortably clear of this today.

### What counts

| | |
|---|---|
| **Qualified** | Sales status = Hot, Warm, Closed, Lost, Qualified_SDR, or any refund status |
| **Meeting held** | Meeting Status = *Meeting Done*. A no-show or rejection is not a held meeting |
| **Not counted** | Leads marked Duplicate record or Wrong info — removed from both your credits and your lead count, so they never hurt your rate |
| **Which month** | Leads are counted by the month they were **created** |
| **When you're paid** | Your variable is calculated from **last month's** leads and paid with this month's salary. A deal booked at month end needs time to close — the one-month lag makes sure it counts |

### The short version

**Book meetings that actually happen, on the leads you're given.** Not meetings booked — meetings
held. Everything else follows from that.

---
---

# Appendix C — Team Lead Compensation Proposal

**Chase Anderson, SDR Team Lead** · Proposal for August onward

### The ask

Current: **$3,500 base + $1,000 guarantee**, guarantee expiring after August (month 3).

Proposed: **$4,500 flat base + performance variable that pays $0 unless the business improves.**

**This is cost-neutral today.** The company pays $4,500 now and would pay $4,500 under this plan at
current performance. Every additional dollar is funded by measurable gains.

### The variable — three components

| **1 · Team B2B lead→deal rate** *(matured, prior month)* | Payout | | **2 · Team non-response rate** *(B2B)* | Payout |
|---|---|---|---|---|
| under 11% — *June was 10.7%* | **$0** | | 34%+ — *June was 34.7%* | **$0** |
| 11 – 12.5% | $300 | | 31 – 34% | $200 |
| 12.5 – 14% | $600 | | 28 – 31% — *company baseline 29%* | $400 |
| 14 – 15.5% — *company benchmark 14.2%* | $950 | | 25 – 28% | $600 |
| 15.5 – 17% | $1,250 | | under 25% | $800 |
| 17%+ | $1,500 | | | |

**3 · Revenue override — 1.0% of team-sourced revenue above ($40,000 × active Coordinators).**
The threshold scales with headcount, so this pays for productivity per head and never for hiring.
$40,000 sits just above June's actual $39,299 per SDR.

### What it costs the company

| Scenario | Lead→deal | Non-resp | Team revenue | Variable | **Total** | % of base |
|---|---|---|---|---|---|---|
| **Status quo** | 10.7% | 34.7% | $157,196 | **$0** | **$4,500** | 0% |
| Modest gain | 12.0% | 32.0% | $175,000 | $650 | $5,150 | 14% |
| Good | 13.5% | 30.0% | $200,000 | $1,400 | $5,900 | 31% |
| Very strong | 15.0% | 27.0% | $225,000 | $2,200 | $6,700 | 49% |
| **Exceptional** | 16.5% | 24.0% | $250,000 | $2,950 | $7,450 | 66% |
| Outstanding (6 SDRs) | 17.5% | 23.0% | $360,000 | $3,500 | $8,000 | 78% |

At the exceptional case the company pays **$2,950 more per month** and receives roughly **$93,000
more monthly revenue** than the status quo — a **31:1 return** on the incremental compensation.

### Why these two metrics

**Lead→deal** is the whole funnel in one number, it is the business outcome, and no marking
decision can move it.

**Non-response** is the largest leak in the company's funnel per the Strategic Briefing (29% of all
leads). The SDR team runs at 34.7–42.7% — 5 to 14 points *worse* than the company average. In the
data it tracks inverse to output without exception: in July the SDR with the lowest non-response
rate also had the highest held-meeting rate, and the SDR with the highest had the lowest.

Both are team-level and neither can be moved by working harder personally — only by building a team
that converts better. That is the job.

**Alignment:** the Coordinators are paid for *producing* qualified meetings; the Team Lead for what
those meetings *become*. Neither can win by pushing volume that does not close.
