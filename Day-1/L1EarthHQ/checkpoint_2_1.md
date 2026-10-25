# Checkpoint 2 evidence (practice data)

Back to [README.md](README.md). Numbers are from practice datasets and shown as method evidence.

## D2: Attribution (D2 practice)

10 conversion paths worth $960 in total. Credit by model:

| Channel | First-click | Last-click | Linear | Time-decay | Position-based |
|---|---|---|---|---|---|
| Direct | $0 | **$580** | $211 | $344 | $254 |
| Paid Search | $170 | $310 | $202 | $242 | $230 |
| Email | $90 | $70 | **$165** | $153 | $114 |
| Paid Social | **$270** | **$0** | $159 | $88 | $148 |
| Organic Search | $210 | $0 | $151 | $101 | $119 |
| Organic Social | $150 | $0 | $38 | $10 | $60 |
| Referral | $70 | $0 | $35 | $23 | $35 |

```
Paid Social credit
First-click  ███████████████ $270
Linear       █████████ $159
Last-click   $0
```

- Last-click gives Direct 60% of credit and Paid Social, Organic Search and Organic Social nothing.
- First-click gives Paid Social the most (28%). It opens 4 of 10 paths.
- Email is in 4 of 10 paths, both opening and closing, so it is a connector.
- Lesson: Direct mostly collects people other channels introduced. Cutting paid social because last-click shows $0 would be wrong.
- Time-decay uses a half-weight per step back; position-based uses 40% first, 40% last, 20% shared.

## D3: Campaign results (D3 practice)

Total spend $18,400, revenue $35,480, ROAS 1.93, 397 conversions.

| Campaign | Spend | CTR | CVR | CPA | ROAS | Call |
|---|---|---|---|---|---|---|
| Google Search - Brand | $1,200 | 8.06% | 6.62% | $12.50 | **7.60** | Scale |
| Meta Retargeting - Site visitors | $1,500 | 1.50% | 2.42% | $25.86 | **3.48** | Scale |
| Meta Lookalike - Customers | $2,200 | 1.03% | 1.31% | $43.14 | 2.09 | Fix |
| Google Performance Max | $2,800 | 0.76% | 1.97% | $45.90 | 1.96 | Fix |
| Google Search - Category | $3,400 | 2.42% | 3.22% | $45.95 | 1.85 | Fix |
| Meta Prospecting - Interests | $3,000 | 0.88% | 0.75% | $71.43 | 1.19 | Fix |
| Google YouTube - Awareness | $2,500 | 0.35% | 0.31% | $277.78 | 0.29 | Pause as sales |
| Meta Reels - Awareness | $1,800 | 0.37% | 0.14% | $300.00 | 0.27 | Pause as sales |

```
ROAS
Brand search  ████████████████████████████████████ 7.6
Retargeting   █████████████████ 3.5
Lookalike     ██████████ 2.1
PMax          ██████████ 2.0
Category      █████████ 1.9
Interests     ██████ 1.2
YouTube       █ 0.3
Reels         █ 0.3
```

- Sales campaigns: $14,100 spend, ROAS 2.43. Awareness: $4,300 spend (23% of total), ROAS 0.28.
- Google ROAS 2.18, Meta 1.63.
- Awareness campaigns are judged on reach, not sales; ROAS of about 0.3 says only that they don't sell directly.

## Caveats

- Small practice datasets: D2 has 10 paths, D3 has 8 campaigns. Treat results as method evidence.
- D3 covers Google and Meta only; there is no influencer or CRM data, so those lines rest on D2 and D5 logic.
- ROAS is not profit. Margins are not given, so ROAS under about 2 may be unprofitable.
