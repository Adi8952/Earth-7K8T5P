# Checkpoint 1: Situation and Objectives

**Team Netflix · Earth 7K8T5P** · Evidence detail: [evidence.md](evidence.md) · Code: [d4_d5_analysis.py](d4_d5_analysis.py)

## 1. Situation

1. **Scale.** Netflix passed 325M paid memberships in Q4 2025 and earned $45.2B revenue in 2025 (+16%) at a 29.5% operating margin. Source: [Subscription Insider](https://www.subscriptioninsider.com/article-type/news/netflix-q4-paid-memberships-top-325m-as-ads-and-pricing-set-the-2026-operating-model)
2. **Profit is strong.** Q3 2026 revenue grew 12% year on year and operating margin hit 34.6% (28.2% a year earlier). Source: [Netflix 8-K, SEC](https://www.sec.gov/Archives/edgar/data/0001065280/000106528026000290/ex991_q326.htm)
3. **Ads are growing, but delivery lags.** The ad tier reaches 250M+ monthly active viewers (190M in Nov 2025), yet 2026 ad revenue guidance was cut to about $2.7B from about $3B because ad product features rolled out late. Sources: [Variety](https://au.variety.com/2026/tv/news/netflix-claims-ad-tier-reaches-250-million-viewers-36559/), [24/7 Wall St.](https://247wallst.com/cards/netflix-q3-2026-earnings-nflx-01m5deq0f119rjb4fjrht5sjde)
4. **Prices keep rising.** All US plans went up in March 2026 and the ad tier moved from $7.99 to $8.99. Higher prices raise the cost of a poor experience, so retention is the main risk. Source: [Quartz](https://qz.com/netflix-raises-streaming-plans-2026)
5. **Our evidence points to the same retention gap (method only).** 60% of engaged sessions came from one day (D1 practice), only 1 of 12 touchpoints sits at the Engage stage (M1-2 practice), and churn is 65% for subscribers inactive 30+ days vs 8% for those active within 7 days (D5 practice). Full tables: [evidence.md](evidence.md)

### DoomCopy threat analysis

| Touchpoint | Can DoomCopy copy it? | Why |
|---|---|---|
| Price / plans | Yes | Public and instant |
| Ads / creatives | Yes | Visible to everyone |
| Sign-up / UI flow | Partly | Visible, but not tuned to our data |
| Content library | Partly | Licensing and production are costly |
| Consented viewing data | No | Earned over years with permission |
| Segments + next-best action | No | Needs the data above |
| Test-and-learn habit | No | Culture, not a feature |
| Trust in how we use data | No | Built slowly, lost fast |

**Note to self:** the one thing DoomCopy can never copy is the trust that lets us hold consented data. Segments, flows and tests all sit on top of it.

## 2. Objectives

**North Star:** Weekly Active Viewing Households (WAVH), meaning accounts with 3+ viewing days in a week.

| KPI | Measure | Baseline | 100-day target | Evidence |
|---|---|---|---|---|
| **K1 Retention** | Churn among subscribers in their first 12 months | 37.6% (D5 practice) | 33.6% (-4 pp) | D5, M1-2 Engage gap |
| **K2 Engagement** | Engaged sessions / all sessions | 53.6% (D1 practice) | 58.6% (+5 pp) | D1 dashboard |
| **K3 Conversion** | Key events / sessions | 2.6% (D1 practice) | 3.2% | D1 dashboard, D4 segments |

Enabler (not a KPI): grow consented, opted-in profiles so the segments and flows behind K1-K3 can run.

## 3. Search interest (Google Trends, last 12 months)

![Netflix vs rival](images/trends_netflix_vs_rival.png)

Takeaway: `[FILL: one line, e.g. spikes follow big releases, so launch timing is a lever]`

## 4. Still to complete

- [ ] Add `images/trends_netflix_vs_rival.png` and the takeaway line
- [ ] Journey map pain point (M1-1): step and drop-off, labelled (M1-1 practice), then add it to Situation bullet 5 or to evidence.md
- [ ] Check M1-2 rows 3 and 4 (see evidence.md)
