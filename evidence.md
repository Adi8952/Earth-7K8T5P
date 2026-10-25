# Evidence (method only, labelled practice)

Back to [README.md](README.md). All numbers below come from practice datasets and are shown as method evidence, not Netflix results.

## D1: Reality dashboard (D1 practice)

| Metric | Value | Derived |
|---|---|---|
| Sessions | 163,219 | |
| Engaged sessions | 87,504 | 53.6% engagement rate |
| Key events | 4,236 | 2.6% of sessions |
| Revenue | 207,080.39 | about 1.27 per session |

**Insight:** Jan 9, 2026 produced 52,545 engaged sessions (60% of the total). The other 36 dates sit flat at about 1,000-1,200 each, so attention is a one-off spike, not a habit. The chart runs past today's date, which suggests sample data.

## M1-2: Touchpoint inventory (M1-2 practice)

| # | Touchpoint | Type | RACE |
|---|---|---|---|
| 1 | Instagram | Owned | Reach |
| 2 | Facebook | Owned | Reach |
| 3 | YouTube | Owned | Reach |
| 4 | X | Owned | Act |
| 5 | Google Play reviews | Earned | Act |
| 6 | News coverage | Earned | Reach |
| 7 | Google Search ads | Paid | Reach |
| 8 | Outdoor / metro | Paid | Reach |
| 9 | Netflix India SEO | Owned | Convert |
| 10 | Telecom / device bundles | Paid | Convert |
| 11 | LinkedIn | Owned | Reach |
| 12 | r/netflix | Earned | Engage |

- By type: 6 owned, 3 paid, 3 earned.
- By RACE stage: 7 Reach, 2 Act, 2 Convert, 1 Engage.
- None of the 12 is an owned retention channel (email, push, in-app).
- To check: row 3 lists YouTube as Owned but its channel says SEM/PPC (Paid); row 4 tags X as Act.

## Listening snapshot (practice)

- 13 viewer comments hand-labelled and compared with an AI labeller: 85% agreement.
- Of the 12 comments readable: 8 positive, 4 negative.
- By topic: movie 2/2 positive, content 3/3 positive, song 1 negative, character 3 positive vs 3 negative.
- The AI marked two human-labelled comments (one positive, one negative) as neutral, so it misses nuance.
- Small sample: directional only.

## D4: Customer segments (D4 practice)

400 customers, k-means with k = 4 on recency, orders, revenue and email clicks (silhouette 0.31, so groups overlap).

| Segment | Customers | Revenue share | Profile |
|---|---|---|---|
| Champions | 14.5% | 42.9% | About 14 orders, $1,437 each, last order about 42 days ago |
| Quiet regulars | 33.0% | 29.2% | About 5 orders, 2.4 email clicks |
| Email-responsive | 33.5% | 23.8% | About 4 orders, 9.1 email clicks |
| Lapsed | 19.0% | 4.1% | About 1.5 orders, last order about 254 days ago |

Email clicks do not predict spend here (correlation about -0.08).

## D5: Churn model (D5 practice)

1,200 subscribers, 21% churned (252). Logistic regression: AUC 0.89 held-out, 0.88 in 5-fold cross-validation (random forest 0.87).

| Driver | Churn rate |
|---|---|
| Last login 7 days ago or less | 8% |
| Last login more than 30 days ago | 65% |
| 5 or fewer sessions in 30 days | 54% |
| More than 20 sessions | 7% |
| Tenure 6 months or less | 38% |
| Tenure over 36 months | 7% |
| 1+ payment failures | 36-39% (18% with none) |

- The 176 subscribers inactive 30+ days (15%) produce 46% of all churn.
- Discount joiners did not churn more (19% vs 21%).
- At a 0.3 cut-off the model catches 68% of churners with 61% precision.
- First-12-month churn (K1 baseline): 37.6% (115 of 306).

## Data notes

- D4 and D5 are separate datasets; IDs do not link.
- D4 contains names and emails: use customer IDs only, and do not commit the raw D4 CSV to a public repo.
- Rerun the numbers with [d4_d5_analysis.py](d4_d5_analysis.py).
