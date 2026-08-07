# Snapshot — New Commission Calculator explainer sections (pre-simplification)

**Date:** 2026-08-07. Taken immediately before simplifying the "How the new plan
works," "Worked example," and "What this costs the business — for the founder"
sections of the New Commission Calculator in `index.html`, so the original
wording is not lost. The underlying math and numbers were not changed —
only how much text is shown and where. Full reasoning behind every number
still lives in `docs/sdr-compensation-plan-v3.md`.

---

## "How the new plan works" (id: npExplainerBody) — before

```
VARIABLE = Tier(credit rate) × volume factor × AE-DQ gate
     + $12 × B2C credits
     + 0.25% × closed revenue
TOTAL   = Base + Bonus + Variable
```

1. **Credits.** **1 credit** for every B2B meeting that actually happens (Meeting
   Status = Meeting Done). **½ credit** for a B2B lead you qualify where no
   meeting is needed — the "just email me" handoffs. Half, because those are
   worth $278 per lead against $547 for a held meeting: 51%, measured, not
   negotiated.
2. **Credit rate = credits ÷ your B2B leads.** That rate sets the tier. B2B on
   both sides — B2C never enters it.
3. **Held, not booked.** Leads first touched more than 4 hours late still get
   booked into meetings at 23.3%, but they close at 5.8% instead of 13.1% and
   produce $61 per lead instead of $171. Booking is nearly speed-independent;
   value is not. A no-show earns nothing, which is why this plan has no
   separate no-show penalty.
4. **Volume factor.** min(1.00, B2B leads ÷ 160), on the tier only. At or above
   160 leads it never reduces anything. A high rate on a short book is not the
   same achievement as a high rate on a full one.
5. **B2C kicker.** $12 per B2C credit, on its own line. B2C credits are counted
   the same way B2B credits are — 1 for a held meeting, 0.5 for a qualified
   lead handed to an AE with no meeting — so the same work earns on both
   sides. B2C is worth about $9 per lead against B2B's $78, so it is worth
   chasing (the leads are free) but never worth distorting the main rate for,
   which is why it is paid flat instead of entering the credit rate.
6. **Revenue share.** 0.25% of revenue that closes on your leads. Small on
   purpose: enough that a $3,000 shoot feels different from a $600 one, not
   enough to coast on.
7. **AE-DQ gate.** Under 10% of handoffs bounced → full payout; 10–15% →
   ×0.90; over 15% → ×0.75. A bounced lead already loses its credit outright
   (Disqualified AE isn't a qualified status), so this is a second, lighter
   layer.
8. **No cap.** Above 39% every additional credit pays $55. At roughly a 40%
   credit rate the variable passes 100% of base — pay doubles.
9. **The one-month lag stays.** Leads count by the month they were created,
   and the payout runs the following month. Only 63.7% of revenue has closed
   by day 7 and 86.8% by day 21, so a deal booked at month end needs the lag
   to be counted at all.
10. **What never counts.** Duplicate-record and Wrong-info leads are stripped
    from both your credits and your lead count, so they can never drag the
    rate down.

## "Worked example — see the math on a real month" (id: npExampleBody) — before

A separate collapsible section, directly below "How the new plan works."
Driven by whichever SDR had the top credit rate for the selected month (not a
made-up scenario, so the numbers always reconcile to real data):

- SDR name and month
- B2B leads → meetings held → credits, qualified/no-meeting → credits,
  credits total
- Credits ÷ leads = credit rate → tier
- Volume factor / overage / AE-DQ gate adjustments, when they apply
- B2C credits × B2C rate
- Revenue × revenue share
- VARIABLE total
- "Next step" callout: credits needed to reach the next tier and what it's
  worth
- Footnote: "Every number above is read live from the loaded data for the
  selected month. Change the month picker and this example changes with it."

## "What this costs the business — for the founder" (id: npFounderBody) — before

Intro line: month, number of active Coordinators, and a note about any SDR
excluded from cost because they had no leads that month, plus a prompt to
enter Base pay if missing.

**Table: What the team produced** — B2B leads worked, meetings held, closed
deals (B2B), lead→deal rate, non-response rate (matured terminal), non-response
rate (broad/live), revenue sourced — each with a benchmark column (company
brief figures).

**Table: What it costs** — base + bonus, variable under the new plan, Team
Lead pay (if included by toggle), total compensation, cost per lead worked,
cost per meeting held, cost per closed deal — each with a "per unit" column.

**Table: New plan vs old, same month** — per-Coordinator credit rate, old
variable (modelled), new variable, % change; team row totals.

**Table: Why the numbers are set where they are** — half-credit weight, tier
floor, volume reference, B2C kicker, revenue share, top band — each with its
one-line derivation.

**Callout: "The one-line case."** A held B2B meeting is worth $547 and 42.5%
of them close at a $1,287 AOV. In {month} the team produced {N} held meetings
at {$X} each. The plan gets cheaper per dollar as it works: comp runs ~8.8%
of revenue in a poor month, 7.1% at June's level and 6.7% when the team is
very strong. The 7% ceiling is a revenue target, not a pay lever — at $5,100
of fixed base the team needs roughly $130,000/month sourced for total comp to
sit at 7%.

---

## What changed on 2026-08-07

- The "one-line case" callout moved out of the Founder section to a new,
  always-visible banner at the top of the New Commission Calculator (above
  "How the new plan works"), so the headline math is visible without
  expanding anything.
- "How the new plan works" was cut down to the mechanics only (what earns a
  credit, how the rate sets pay, what's added on top, no cap) in larger
  text; the numbered "why" reasoning above was moved out of the dashboard
  and lives in `docs/sdr-compensation-plan-v3.md` (Part 3, Appendix A/B).
- The worked example was folded into the same "How the new plan works"
  section instead of a separate accordion, so an SDR sees the rule and a
  real example together.
- The Founder section was reduced to two small value grids ("what each
  thing is worth" and "what it costs") — the "New plan vs old" and "why the
  numbers are set" tables were removed from the dashboard (both still exist
  in `docs/sdr-compensation-plan-v3.md`, Part 3.4–3.6 and Appendix A).
