# SDR KPIs & Compensation Strategy — Version 2

**Prepared for:** Chase Anderson, SDR Team Lead
**Date:** 28 July 2026
**Supersedes:** v1 (28 July 2026)

**Data:** Bookings SDR View (1,668 SDR-owned leads, May–July 2026), full booking history,
Aircall call log (4,100 calls, 14 May – 28 July), Strategic Briefing v1.0, SDR Team Lead
Onboarding v1.0, and the live commission logic in `index.html`.

Every figure below was produced by replaying the dashboard's own definitions against the raw
CSVs. The replication reconciles to the July paycheque exactly — MJ's $946 = the $1,000 meeting
bracket × 0.85 quality multiplier + $96 New Sales; Gospel's $865 = the $800 bracket + $65 New
Sales — so these are the real numbers, not estimates.

**What changed in v2:** held meetings replace booked meetings throughout; the no-show multiplier
is removed; qualified handoffs that never produce a meeting are now paid for; B2C moves to its
own line item; the revenue share drops to 0.5%; a 7%-of-revenue cost ceiling is treated as a
binding constraint; and a compensation plan for the Team Lead is included.

---

## Part 0 — The numbers everything else rests on

| Metric | Value | Basis |
|---|---|---|
| Revenue per **held** B2B meeting | **$547** | May+June matured cohorts |
| Held meeting → closed deal | **42.5%** | 54 deals from 127 held meetings |
| SDR-sourced AOV | **$1,287** | vs $1,466 company-wide (SDRs work the sub-$1k tier) |
| Revenue per B2B lead | **$143** (June) | vs **$9** per B2C lead |
| Revenue per qualified **no-meeting** handoff | **$278** | exactly half a held meeting — see Part 2 |
| 87% of revenue closes within 21 days | matches briefing's 86% | close-lag curve |
| Cost per lead (June, actual) | **$6.93** | $4,511 comp ÷ 652 leads |
| Cost per held meeting (June, actual) | **$34.97** | against $547 of revenue generated |

**A held, qualified B2B meeting is worth $547.** That is the unit the whole plan is priced
against. Today it costs $35 to produce — a 15:1 return before delivery cost. That ratio is why
there is room to pay more, and it is the number to defend as the team scales.

---

## Part 1 — Your KPIs as Team Lead

### 1.1 The objection you raised, answered properly

You pushed back on my dismissing "% of leads qualified" because it depends on marketing lead
quality — and you pointed out that held meeting rate depends on exactly the same thing. **You are
right, and my v1 argument was sloppy.** Both metrics move when marketing changes the lead mix.
Marketing dependency is not the distinction.

The real distinction is **who writes the number**:

| | % of leads qualified | Held meeting rate |
|---|---|---|
| Who produces the value | The SDR | The SDR |
| Who *records* it | The SDR (a dropdown) | The prospect (by showing up) and the AE (by running it) |
| Moves if judgment loosens but reality doesn't? | **Yes** | **No** |
| Affected by lead quality? | Yes | Yes — equally |

One is a claim; the other is an event witnessed by a third party. That is the only difference,
and it is the one that matters for pay.

**And the shared weakness has a shared fix.** Because all four Coordinators draw from the same
routed pool, lead quality is controlled by *comparing SDRs to each other within the same month*
rather than to a fixed absolute. When the whole team's rate moves together, that is marketing or
seasonality and it is not an SDR performance event. When one person diverges, that is coaching.
Build the read that way and the marketing dependency stops mattering for both metrics.

Practically: **re-benchmark the tier thresholds each quarter against the team's actual delivered
lead mix.** Fixed forever is wrong; floating monthly is unmanageable. Quarterly is the balance.

### 1.2 Your KPIs

You proposed lead→deal rate as your number one. **I agree, with one adjustment**: it is the right
number to be *accountable* for, but it is lagging — 87% of revenue lands within 21 days, so you
learn about July in late August. You need one number you are judged on and one you can steer with
this week.

**Primary — Team B2B Lead → Deal Rate** *(what you are measured and paid on)*

| Month | B2B leads | Closed | Lead→deal | Revenue |
|---|---|---|---|---|
| May 2026 | 66 | 13 | **19.7%** | $19,464 |
| June 2026 | 449 | 48 | **10.7%** | $60,428 |
| July 2026 | 564 | 16 | 2.8% *(immature)* | $18,440 |
| Company benchmark | — | — | 14.2% | — |

This is the whole machine in one number, it is the business outcome, and it cannot be gamed by
any marking decision. Read it on a matured basis — prior month, run 3–4 weeks later, same
timing as commission.

**Secondary — Team Held Meeting Rate** *(what you steer with)*

June 28.7%, July 21.6%. This is the leading half of the primary KPI: lead→deal = held meeting
rate × held-to-deal rate. When lead→deal moves, this tells you whether the cause was your team's
throughput or the AEs' closing.

**Third — Revenue per B2B lead.** June $143, July ~$51 matured. This is the one that catches the
failure mode neither rate above can see: converting plenty of small deals while the larger
enquiries leak. It is also the number that determines whether the 7% cost target is reachable
(Part 3).

**On speed-to-lead:** you are right to leave it off your scorecard — at team-lead level it is too
noisy month to month. Keep it as a *diagnostic you own*, because the evidence for it is strong
(below), but don't be paid on it.

### 1.3 Speed-to-lead — keep as a diagnostic, not a KPI

May+June matured cohorts, B2B, first outbound Aircall call matched to lead by phone:

| First touch | Share | Held rate | Lead→deal | Revenue per lead |
|---|---|---|---|---|
| Within 1 hour | 74% | 30.7% | 13.1% | **$171** |
| 1–4 hours | 9% | 23.4% | 12.8% | **$203** |
| Over 4 hours / never | 17% | 23.3% | **5.8%** | **$61** |

The critical observation, and the reason "meetings booked" had to go: **leads touched more than 4
hours late still get booked into meetings at 23.3% — but they close at 5.8% instead of 13.1%.**
Slow leads do not stop producing meetings. They stop producing *deals*. Any metric built on
booked meetings is blind to a third of the value in the funnel.

**Do not build a five-minute culture.** Sub-5-minute dialling underperforms a 5–60 minute
response, and it holds for each SDR individually, so it is not a mix artefact:

| | 0–5 min | 5–60 min |
|---|---|---|
| MJ | $130/lead (n=54) | **$264/lead** (n=123) |
| Gospel | $92/lead (n=153) | **$226/lead** (n=51) |

The likely cause is that an instant dial is a dial placed *before reading the enquiry* — the
brief, city, shoot date and budget tier are all sitting in the record. Coach **"nothing sits past
the hour,"** not "call in five minutes." Worth confirming against call recordings before it
becomes policy.

**Do not use dial counts for anything.** June B2B leads needing 1 dial booked at 54% and produced
$251/lead; leads needing 7+ dials booked at 7% and produced $20/lead. In July Gospel made 842
dials at a 6.8% connect rate; Levi made 349 at 51.9%. Activity metrics would rank them exactly
backwards.

---

## Part 2 — The qualified-handoff-without-a-meeting problem

You raised the strongest objection in the review: some prospects say *"email me and we'll sort it
out"* or *"just text me."* Those are genuine handoffs, the AE does close them, and a
held-meeting-only metric pays zero for them. **You are right, and v1 was wrong to ignore it.**

### 2.1 What the data actually shows

Mature cohorts (May+June), B2B, using your qualified definition:

| Segment | Leads | Share | Closed | Close % | Revenue | **Rev/lead** |
|---|---|---|---|---|---|---|
| Qualified + meeting **held** | 127 | 25% | 54 | 42.5% | $69,476 | **$547** |
| Qualified + no-show / rejected | 8 | 2% | 3 | 37.5% | $5,690 | $711 |
| **Qualified, NO meeting at all** | **17** | **3%** | **4** | **23.5%** | **$4,726** | **$278** |
| Not qualified, meeting exists | 41 | 8% | 0 | 0% | $0 | $0 |
| Not qualified, no meeting | 322 | 63% | 0 | 0% | $0 | $0 |

**A qualified no-meeting handoff is worth $278 — 51% of a held meeting.** That is a remarkably
clean ratio and it gives the answer directly: **count it as half a credit.** Not zero, not one.
The data set the weight, not a negotiation.

### 2.2 But right now you cannot see it

Here is the catch. The 17 leads in that segment break down as 12 Closed and 5 Lost — and 8 of the
12 are instant closes (self-serve, closed within 2 hours, not SDR work). **There are zero Hot or
Warm B2B leads without a meeting in the entire mature dataset** (June: 32 Hot/Warm, all 32 have a
meeting. July: 76, of which 75 do).

So the live "email me instead" handoff you are describing **is not being recorded anywhere.** The
segment that exists in the data is almost entirely deals that had already closed.

`Qualified_SDR` looks like the intended marker but is not being used as one: 20 leads carried it
in July and **17 of them also have a meeting**, so it is currently a redundant label, not a
handoff state.

### 2.3 The fix — create the state, then pay for it

You cannot pay for what nobody records, and if you pay for a state that has no definition you
will get that state applied to everything.

1. **Define one marker.** Either reserve `Qualified_SDR` to mean *exactly* "handed to AE, no
   meeting required — client asked for email/text" and nothing else, or add a Meeting Status
   option `Handed to AE – No Meeting`. The second is cleaner because it keeps the meeting axis
   and the qualification axis independent.
2. **Require the AE to be set** in the `Owner` field for the credit to count. A handoff with
   nobody to hand off to is not a handoff.
3. **Pay it at 0.5 credit**, from the measured $278 : $547 ratio.
4. **Cap it at 20% of an SDR's total credits** for the month. This is the anti-gaming guard: it
   can supplement the meeting motion but can never replace it. On June's actual data the cap
   binds only on MJ (7 handoffs, capped to 7 — no effect); it exists for the month somebody
   discovers the shortcut.
5. **Re-measure the $278 in 90 days.** Today's figure rests on 17 leads. If the real value comes
   in higher once the state is being used properly, raise the weight — and tell the team you will.

### 2.4 This also answers your quality question

You asked how to stop the team dumping junk on the AEs once the no-show gate is gone. **The
system already self-polices, and it does so through the qualified definition you chose.**

When an AE bounces a lead back, its Sales status becomes `Disqualified AE (wrong SDR
qualification)` — and that status is **not** in your qualified set. The lead drops out of the
qualified count entirely and the SDR loses the credit. Verified in the data: no AE-disqualified
lead counts as qualified anywhere.

Current AE-disqualified rates, as a share of everything handed over:

| SDR | June | July |
|---|---|---|
| MJ | 5.6% | 8.3% |
| Gospel | 7.2% | **10.4%** |
| Mark | — | 0.0% |
| Levi | — | 7.1% |

Nobody is abusing it yet, but Gospel is drifting. I have built this in as a light gate (Part 3)
rather than relying on the automatic mechanism alone — the AE only re-marks the lead if they
bother to, so the automatic penalty is real but leaky.

---

## Part 3 — The SDR compensation plan

### 3.1 Confirmed: your qualified definition is already the live one

You asked me to check GitHub. Result: **the definition you want is what the dashboard already
uses**, everywhere that matters.

`STRICT_QUALIFIED_STATUSES` (`index.html:3260`) = `hot, warm, closed, lost, qualified_sdr,
full refund, deposit refund, partial refund`, with duplicate-record and wrong-info leads excluded
by `isLeadExcluded`. That drives `isQualifiedLead`, which is what the Summary Cards, charts,
Mandate Scoreboard, Capacity & Cost, and the Commission Calculator all call.

There is a second, broader list (`QUALIFIED_SALES_STATUSES`, line 3136) that includes Pending,
Quote Sent and others — **it is used only by the Data Hygiene section**, which is flagged
in-code as under construction and deliberately frozen on the pre-23-July logic so its typo
checks don't shift underneath it. It touches no metric and no payout. Nothing to change.

One consequence worth stating plainly: **last month's qualified rates were computed under the
current definition, so they are already comparable.** No restatement needed.

### 3.2 What the plan does and does not keep

| v1 element | Status in v2 | Why |
|---|---|---|
| Qualified Leads Incentive (40% floor) | **Removed** | Fired twice in six SDR-months. Dead. |
| Meeting Set Incentive on *booked* | **Replaced** with held | Booked is nearly speed-independent; value is not |
| Bracket cap at 40%+ | **Removed** | MJ's marginal reward for meeting #94 was $0 |
| No-show / rejection multiplier | **Removed** | Paying on *held* already prices a no-show at the full meeting. A second penalty double-counts, and no-show responsibility now sits with the SDR anyway |
| New Sales at 0.25% | **0.5%** | Doubled, but kept small — see 3.4 |
| B2C in the rate numerator | **Removed** → own line | Was inflating rates 4–15 points, worth ~$400/SDR/month |
| — | **New:** volume factor | Kills the small-denominator problem |
| — | **New:** AE-disqualified gate | Replaces the no-show gate as the quality counterbalance |

### 3.3 The structure

**Credits (B2B only, both sides of the ratio):**

```
Credits  =  held B2B meetings  +  0.5 × qualified B2B no-meeting handoffs (capped at 20% of credits)
Credit Rate  =  Credits ÷ B2B leads assigned
```

**Tier table** — 1.5-point bands so no single boundary is worth more than $65:

| Credit rate | Tier | | Credit rate | Tier |
|---|---|---|---|---|
| under 18% | $0 | | 30 – 31.5% | $755 |
| 18 – 19.5% | $350 | | 31.5 – 33% | $815 |
| 19.5 – 21% | $395 | | 33 – 34.5% | $875 |
| 21 – 22.5% | $440 | | 34.5 – 36% | $935 |
| 22.5 – 24% | $490 | | 36 – 37.5% | $1,000 |
| 24 – 25.5% | $540 | | 37.5 – 39% | $1,065 |
| 25.5 – 27% | $590 | | **39%+** | **$1,065 + $55 per credit above 39%** |
| 27 – 28.5% | $645 | | | |
| 28.5 – 30% | $700 | | | |

**Why the floor sits at 18%** — you asked whether 20% was arbitrary. In the old plan it was. Here
it is derived: at $547 of revenue per held meeting and your 7% cost target, an SDR on a $1,200
base needs roughly 31 held meetings a month to cover their own base at target cost. On a typical
175-lead book that is **17.9%**. The floor is the break-even point, rounded. Below it the SDR is
not yet paying for themselves and the variable should be zero.

**Why the top never plateaus** — above 39% the tier converts to $55 per additional credit,
uncapped. This is the direct fix for the flaw that made the old plan pointless at the margin.

**Volume factor:** `min(1.0, B2B leads ÷ 175)`, applied to the tier only.

This closes the loophole that made Mark the highest commission earner in July on $486 of revenue.
A high rate on a small book is not the same achievement as a high rate on a full one. Capped at
1.0 so a volume windfall cannot inflate pay either. 175 is the current routed level — reset it
when routing changes.

**B2C kicker: $12 per held B2C meeting.** Separate line, never touches the rate. This is the
answer to your question about whether B2C belongs in the numerator or on its own line: **its own
line.** B2C is worth $9 per lead against B2B's $78, so paying it inside the same rate meant
paying the same money for an eighth of the value. As its own item it stays worth chasing — free
leads, no media cost, and $12 is real money for a meeting that costs nothing to source — without
ever distorting the main number.

**Revenue share: 0.5% of closed revenue** from own-created leads, excluding instant closes.

**AE-disqualified gate** — applies to the tier component only:

| AE-DQ rate (of all handoffs) | Multiplier |
|---|---|
| Under 10% | ×1.00 |
| 10 – 15% | ×0.90 |
| Over 15% | ×0.75 |

Graduated, computed on the payout month itself, and reproducible by hand — the three failings of
the old multiplier. It is deliberately gentle: the qualified definition already removes the credit
for a bounced lead, so this is a second, lighter layer on the same behaviour, not a new penalty.

### 3.4 Why the revenue share stays at 0.5%

Your instinct was right and worth writing down. At 1.0%, MJ's June revenue would have paid $384 —
roughly 40% of his variable — arriving weeks after the work, from deals an AE closed. That is the
"I've banked enough, I can ease off" money you were worried about. At 0.5% it pays $192: enough
that a $3,000 multi-city shoot feels different from a $600 headshot session, not enough to coast
on.

The tier does the motivating; the revenue share does the *steering*.

### 3.5 What it pays — modelled on actuals

**June 2026 (the month you paid for in July):**

| SDR | B2B leads | Held | No-mtg | Credits | Rate | AE-DQ | Tier | B2C | Rev | **Variable** | Was | **Δ** | Total |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| MJ | 225 | 62 | 7 | 65.5 | 29.1% | 5.6% | $700 | $132 | $192 | **$1,024** | $946 | **+8%** | $2,224 |
| Gospel | 224 | 67 | 2 | 68.0 | 30.4% | 7.2% | $755 | $132 | $130 | **$1,017** | $865 | **+18%** | $2,517 |
| **Team** | 449 | 129 | | | | | | | | **$2,041** | $1,811 | **+13%** | **$4,741** |

Team comp ÷ revenue: **7.4%**. Cost per lead **$7.27** · cost per qualified lead **$35.92** ·
cost per held meeting **$36.75**.

**On the spread between them:** MJ +8%, Gospel +18%. This is the plan correcting a real
mis-ranking, not a calibration error. Gospel converted *better* in June — a 30.4% credit rate
against MJ's 29.1% — but the old plan paid him less because it measured booked meetings and then
applied a multiplier. MJ booked more; Gospel held more. Under a plan that pays for held meetings,
Gospel moves up. That is the plan doing its job on its first month of data.

**July 2026 (for reference — a weaker month, and still maturing):**

| SDR | B2B | Held | Credits | Rate | Vol factor | Tier | **Variable** | Was | Δ |
|---|---|---|---|---|---|---|---|---|---|
| MJ | 178 | 36 | 36.0 | 20.2% | 1.00 | $395 | $460 | $700 | −34% |
| Gospel | 166 | 30 | 30.0 | 18.1% | 0.95 | $332 | $385 | $529 | −27% |
| Mark | 101 | 33 | 33.5 | 33.2% | **0.58** | $505 | $567 | $301 | +88% |
| Levi | 119 | 23 | 26.0 | 21.8% | 0.68 | $299 | $315 | $188 | +68% |

Note what the volume factor does to Mark: a 33.2% rate on a 101-lead book earns $505 rather than
the full $875. Under the old plan that same month paid him the top bracket on $486 of closed
revenue. The plan now ranks him behind MJ, correctly.

### 3.6 The 7% question — the most important finding in this report

You asked for total comp at 7% of sourced revenue, stretching to 8% when they are killing it.
Here is the arithmetic, and it is not a comp-plan problem.

**Fixed base for four SDRs is $5,100/month.** That is spent before anyone books anything.

| Target ratio | Revenue needed for **base alone** | Revenue needed for base + $3,900 variable |
|---|---|---|
| 6% | $85,000 | $150,000 |
| **7%** | **$72,857** | **$128,571** |
| 8% | $63,750 | $112,500 |

| Actual | Revenue | Comp | Ratio |
|---|---|---|---|
| June (2 SDRs) | $64,383 | $4,511 | **7.0%** ← already at target |
| July (4 SDRs) | $19,526 (~$28,700 matured) | $6,818 | 35% |

**June already ran at exactly 7.0%.** The target is not aspirational — it is a description of
MJ and Gospel's June. What broke it was doubling headcount into a month where revenue per SDR
fell by more than half.

**So 7% is a revenue target, not a compensation lever.** At current bases the team needs roughly
**$129,000/month** of sourced revenue for total comp to sit at 7% while paying a competitive
variable. Four SDRs at June's per-head productivity ($32,192) produce $128,766. **The 7% goal and
"get Mark and Levi to June-level productivity" are the same objective.**

The plan's cost curve, four SDRs on 200 B2B leads each:

| Credit rate | Team revenue | Variable | Total comp | **Comp ÷ revenue** | vs July's $7,811 |
|---|---|---|---|---|---|
| 18% | $82,080 | $2,412 | $7,512 | 9.2% | −3.8% |
| 21% | $95,760 | $2,840 | $7,940 | 8.3% | +1.7% |
| 24% | $109,440 | $3,308 | $8,408 | 7.7% | +7.6% |
| 27% | $123,120 | $3,856 | $8,956 | 7.3% | +14.7% |
| **29.5% (target)** | **$128,000** | **$3,920** | **$9,020** | **7.0%** | **+15.5%** |
| 33% | $150,480 | $5,072 | $10,172 | 6.8% | +30% |
| 36% | $164,160 | $5,740 | $10,840 | **6.6%** | +39% |
| 45% | $205,200 | $9,888 | $14,988 | 7.3% | +92% |

The ratio **improves** as the team performs, bottoming at 6.6%, and only returns toward 7.3% at
45% — a level nobody has approached. There is no scenario in the realistic range where this plan
runs away from you. Below 21% it exceeds 8%, which is correct: at that level the problem is
performance or headcount, and the plan should be telling you so rather than hiding it.

### 3.7 Implementation

1. **Grandfather July** on the old plan, as you suggested. Announce this for August with the
   tables published in advance.
2. **Create the no-meeting handoff marker before go-live** (§2.3), or that component pays nothing
   in month one and the team learns it is decorative.
3. **Ramp policy for new hires**, written down rather than decided monthly: month 1 at 100% of
   target variable guaranteed, month 2 at 50%, month 3 at zero. Two more Coordinators are coming
   to reach six.
4. **Keep the one-month lag.** The close-lag curve justifies it: 63.7% of revenue is in by day 7,
   86.8% by day 21, 89.4% by day 28. Running 3–4 weeks into the following month captures ~89%.
5. **Re-benchmark tier thresholds quarterly** against delivered lead mix (§1.1). Next review:
   end of October.
6. **Fix the B2C denominator in the dashboard regardless.** It is worth ~$400/SDR/month of
   unearned incentive under the current code.

---

## Part 4 — Team Lead compensation

You asked for a plan for yourself. I don't have your base salary, so this is the variable design
with the level expressed in dollars — tell me the base and I will fit the mix.

**Design principle: you should be paid on what your team produces, not on what you personally
touch, and on the build-out you were hired to deliver.** Three components:

### 4.1 Team performance — tiered on B2B lead→deal rate

Your stated number one, matured basis, prior month:

| Team lead→deal rate | Payout |
|---|---|
| Under 7% | $0 |
| 7 – 8.5% | $250 |
| 8.5 – 10% | $400 |
| **10 – 11.5%** | **$575** ← June was 10.7% |
| 11.5 – 13% | $775 |
| 13 – 14.5% | $1,000 ← company benchmark 14.2% |
| 14.5 – 16% | $1,250 |
| 16%+ | $1,500 + $100 per additional point |

May ran at 19.7% on 66 leads; June at 10.7% on 449. The floor sits at 7% because that is roughly
half the company benchmark — below it the SDR layer is not earning its place in the funnel.

### 4.2 Revenue override — 0.35% of total team-sourced revenue

At the $128,000 target that is **$448/month**; at June's actual $64,383 it is $225. This is the
component that makes you indifferent between a team that books a lot and a team that sells a lot,
and it scales automatically as you add Coordinators five and six.

### 4.3 Build milestones — one-time, against your onboarding gates

| Milestone | Payment |
|---|---|
| Coordinator 5 hired, onboarded, and **through ramp** (held rate ≥18% in a full month) | $750 |
| Coordinator 6, same standard | $750 |
| Full team of 6 all clearing 18% in the same month | $1,000 |

Tied to ramped, not hired. Hiring is the easy half, and your Month-3 gate is "full team of 6
active" — this pays for *active*, not for signatures.

**At June performance this totals $800/month variable; at the $128k target, $1,023 plus
milestones.** Whether that is the right level depends on your base — see the questions below.

### 4.4 Alignment check

| | Your plan | SDR plan |
|---|---|---|
| Primary driver | Team lead→deal rate | Individual credit rate |
| Revenue link | 0.35% of team revenue | 0.5% of own revenue |
| Quality guard | lead→deal is closes-only, ungameable | AE-DQ gate + qualified definition |
| Time horizon | Matured, prior month | Matured, prior month |

You are paid on the *outcome* of the meetings; they are paid on *producing* them. That is the
right asymmetry — you cannot book meetings yourself, and they cannot control which AE gets the
lead. Neither of you can win by pushing volume that doesn't close.

---

## Part 5 — Questions before this is final

1. **What is your base salary, and does the 7% ceiling include you?** This materially changes both
   answers. If your comp counts inside the ratio, the team needs roughly $129,000 plus
   (your total ÷ 0.07) in monthly revenue, which at a $4,000 base pushes the requirement past
   $180,000. My assumption in Part 3 is that 7% covers the four Coordinators only.
2. **Should instant closes count toward the revenue base?** $20,080 across June–July is currently
   excluded from both SDR credit and from the revenue denominator. Excluding it from credit is
   right — it isn't SDR work. But if it is counted as *team-sourced revenue*, the cost ratio
   improves by roughly a point and the 7% target gets meaningfully easier.
3. **Will you create the no-meeting handoff marker in Airtable?** If not, drop that component and
   I will re-tune the tiers — it is currently worth $0–$85/SDR/month, so removing it is a small
   adjustment, but leaving it in unmeasured is worse than not having it.
4. **Is 175 B2B leads/month the right volume-factor reference?** It reflects current routing.
   If you plan to push toward the 275/Coordinator capacity figure in the onboarding doc, the
   reference should move with it or the factor stops binding.
5. **Do you want a team component in the SDR plan?** You run two time zones with overnight
   round-robin routing and nothing currently pays anyone to cover a teammate's leads. A small
   shared kicker (~$150 when the team clears its rate) would change that. Left out of Part 3
   because you didn't ask for it.
6. **July's softness is still unexplained.** Held rate fell for both tenured SDRs while region mix
   moved from 95% North America to 62% NA / 30% Europe. The briefing has rest-of-world converting
   at 11% against North America's 16%. If this is mix, the tier thresholds should differ by desk.
   If it is coaching, it is fixable and the thresholds stand. Worth resolving before the quarterly
   re-benchmark.
