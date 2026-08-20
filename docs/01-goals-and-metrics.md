[← Back to portfolio](../README.md) · Step 1 of 6 · [Next: Data Collection →](02-data-collection.md)

# 1. Goals & Metrics

Turning a business request into a question data can actually answer: fixing the KPI set,
the segments and the comparison period **before** a single query is written.

![Goals and metrics workflow](docs/goals_metrics_p1.png)

## The part that makes the difference

Most requests arrive broad and urgent: *"retention is down"*, *"can we spend more on
channel X?"*, *"send me last week's numbers"*. My first job is not to run a query — it is
to find the decision behind the request. A question with no decision attached is a request
for a chart, not for analysis.

| Asked as | What I ask back | Question we actually answer |
|---|---|---|
| "Retention is down, fix it" | Down for which cohort, on which product, against which baseline? Did a bonus campaign end? | Did D7 retention fall for players registered last week on mobile casino, versus the previous two weeks, excluding the promo cohort? |
| "Should we spend more on channel X?" | What is the budget decision, and what CAC would still be acceptable at current LTV? | At current spend, does channel X reach payback within 90 days, and how does its FTD quality compare with the other paid channels? |
| "This affiliate looks great" | Great on volume or on value? Registrations, or players who deposited and stayed? | For traffic from this partner: FTD rate, average first deposit and D30 retention, versus the affiliate portfolio average. |

## Definitions — where iGaming metrics quietly disagree

![Metric definitions and comparison periods](docs/goals_metrics_p2.png)

Most reporting disputes are not calculation errors. Two teams simply used two different
definitions. These are pinned down in writing before extraction:

- **Active player** — logged in, placed a bet, or deposited? Each gives a different number.
- **New player** — registration or first deposit? Marketing usually means one, finance the other.
- **GGR vs NGR** — NGR deducts bonuses, jackpot contribution, chargebacks and fees.
- **Retention D7** — exactly on day 7, or any activity within 7 days? Classic and rolling retention are never compared to each other.
- **ARPU vs ARPPU** — same numerator, different denominator.
- **Cohort anchor** — registration date answers acquisition questions, FTD date answers monetisation questions.
- **Day boundary & currency** — gaming days rarely end at midnight UTC; conversion rates are documented.

## Choosing the comparison period

Week over week is the default, but only with matched weekdays — a 6-day week against a
7-day week is a reporting bug, not a trend. Where seasonality dominates (sports calendar,
holidays, paydays), the baseline shifts to the same week last month or year. Any period
containing a bonus campaign is compared against a comparable promo period, never against
a quiet week. Retention is always compared at equal cohort age.

## Scope control — what I deliberately leave out

One question gets one primary metric. Instead of analysing everything, I name 1–2
**guardrail** metrics that must not silently degrade while we optimise the primary one.
Side questions are logged for a later cycle rather than quietly expanding this week's
scope. If nobody in the business owns a number, it does not belong on the dashboard.

## Output of this step

A one-page brief, agreed in writing before extraction begins:

`Question` · `Decision it feeds` · `Primary metric` · `Supporting metrics` · `Guardrails` ·
`Segments` · `Comparison period` · `Exclusions` · `Owner` · `Deadline`

This brief is the reference every later number is checked against — which is what makes
the results defensible when someone disagrees with them three weeks later.

📄 [Download this section as PDF](docs/iGaming_Goals_and_Metrics_EN.pdf)

---

[← Back to portfolio](../README.md) · [Next: Data Collection →](02-data-collection.md)
