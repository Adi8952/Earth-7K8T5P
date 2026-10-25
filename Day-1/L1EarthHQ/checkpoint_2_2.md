# Checkpoint 2: Strategy and Tactics

**Team Netflix · Earth 7K8T5P** · Builds on [Checkpoint 1](../Checkpoint1/README.md)

## 1. Strategy

**Target segments**

| Segment | Why | Evidence |
|---|---|---|
| **Champions** (protect) | 14.5% of customers, 42.9% of revenue | D4 practice |
| **At-risk: inactive 30+ days** (win back) | 15% of subscribers, 46% of churn, 65% churn rate | D5 practice |

**Positioning line**

> For viewers who want something great to watch without hunting for it, Netflix is the streaming service that picks up where you left off and shows the next story you'll love, unlike DoomCopy, which can copy our price and our ads but not what we have learned, with permission, about what you enjoy.

**One retention loop: the watch-signal win-back loop**

```
Consented viewing data
        |
        v
D5 model flags drop in activity (7 -> 14 -> 30 days since login)
        |
        v
Personalised nudge (email / push / in-app): "next episode" or "new in your genre"
        |
        v
Member returns and watches  --->  new viewing data  --->  (back to the top)
```

- Why it works: it fills the Engage gap (1 of 12 touchpoints, M1-2) and uses the owned channels DoomCopy can't copy.
- KPI: K1, first-12-month churn 37.6% to 33.6% (D5 practice).

## 2. Tactics: $250,000 across channels

| # | Channel / tactic | D3 call | Budget | Share | One KPI (baseline to target) | Why (evidence) |
|---|---|---|---|---|---|---|
| 1 | Owned CRM: email, push, in-app win-back | New | $60,000 | 24% | First-year churn 37.6% to 33.6% | Email is in 4 of 10 paths and earns 17% of credit under linear vs 7% under last-click (D2); inactive 30+ days = 46% of churn (D5) |
| 2 | Search defence: brand terms | **Scale** | $30,000 | 12% | CPA $12.50 held under $15 | Brand search ROAS 7.6, CTR 8.1% (D3 practice); scale in steps, capped by search volume |
| 3 | Meta retargeting (site visitors) | **Scale** | $20,000 | 8% | ROAS 3.5 held above 3.0 | Second-best ROAS, CPA $25.86 (D3) |
| 4 | Meta lookalike prospecting | **Fix** | $20,000 | 8% | ROAS 2.1 to 2.5 | Beats interest targeting (2.1 vs 1.2); paid social starts 28% of path value (D2) |
| 5 | Google category search + Performance Max | **Fix** | $15,000 | 6% | CPA $46 to $35 | ROAS 1.85 and 1.96, CPA about $46 (D3); tighten keywords, add negatives |
| 6 | Influencer plan (with disclosure) | New | $35,000 | 14% | Cost per engaged session | Replaces raw awareness buying (ROAS 0.28, D3); creators add Reach and Engage with tracked links |
| 7 | CRO test: first-watch onboarding | New | $25,000 | 10% | Key-event rate 2.6% to 3.2% | Low key-event rate (D1 practice) |
| 8 | Community and Engage (r/netflix, fan content) | New | $10,000 | 4% | Active community posts per week | Only Engage touchpoint today (M1-2) |
| 9 | Measurement: holdouts and tracking | New | $20,000 | 8% | Share of spend under a holdout test | Last-click and first-click disagree sharply (D2) |
| 10 | Scale reserve, released at day 50 | Reserve | $15,000 | 6% | ROAS of the channel it moves to | Scale / fix / pause rule below |
| | **Total** | | **$250,000** | **100%** | | |

**Paused or not funded (D3 and M1-2):**
- YouTube Awareness (ROAS 0.29, CPA $278) and Reels Awareness (ROAS 0.27, CPA $300): pause as sales spend. D2 shows paid social starts paths, so judge any awareness test on cost per reach and assisted conversions, not last-click.
- Meta Prospecting - Interests (ROAS 1.19, CPA $71): rebuild as lookalikes (line 4).
- Outdoor / metro and telecom bundles: no D3 data, so held until measured.

**Scale / fix / pause rule (assumption, check against your L4 notes):** scale at ROAS 3 or higher, fix between 1 and 3, pause below 1 unless D2 shows it assists conversions. At day 50, move the $15,000 reserve to the best-performing line.

### Search defence (brand terms)

- Bid on exact brand terms ("Netflix", "Netflix India", "Netflix plans") so rivals can't take the top spot. D3 practice shows brand search is the most efficient line (ROAS 7.6).
- Watch rival ads on our brand terms weekly and report any trademark misuse to the search platform.
- KPI: CPA held under $15 (baseline $12.50), plus brand-term impression share 90%+, tracked weekly.

### Influencer plan with disclosure

- 6 to 8 creators (micro and mid-size), picked for audience fit with the two target segments, not follower count.
- Every post carries the platform's paid-partnership label plus a clear "#ad" in the first line or the first seconds of video.
- Creators say only what is true and approved; no claims about prices, free offers or release dates unless supplied by us.
- Each creator gets a unique tracking link so results feed D2 attribution.
- Follow local rules for each market (for example ASCI in India, FTC in the US).

### CRO test

- **Test:** current first-watch screen (A) vs "pick 3 titles you like" onboarding (B).
- **Primary metric:** key-event rate (baseline 2.6%, D1 practice).
- **Target:** 3.2% (about +23% relative).
- **Settings:** 95% confidence, 80% power, two-sided.
- **Sample size:** about **12,400 sessions per variation** (about 24,800 total). Confirm in the [A/B sample-size calculator](https://www.evanmiller.org/ab-testing/sample-size.html) with baseline 2.6% and minimum detectable effect 0.6 points absolute.
- **Duration:** total sample divided by daily eligible sessions; run at least 2 full weeks.
- **Stop rule:** do not stop early when the result looks good; stop only at the planned sample.

## 3. AI use and guardrail

- **Where:** AI drafts subject lines and short message variations for the win-back flow (tactic 1), by segment.
- **Guardrails:**
  - AI only receives approved facts (real titles, our catalog, approved offers). It never invents titles, dates, prices or offers.
  - No promises such as "free month" or "guaranteed" unless a human has put the offer in the approved offer table.
  - No personal data in prompts; use segment names, not people.
  - A human approves every message before it sends, and spot-checks 10% of live messages weekly.
  - Why: in our listening test the AI matched our labels only 85% of the time and missed nuance (practice data).

## 4. Still to complete

- [ ] Check the scale / fix / pause thresholds against your L4 notes and adjust the D3 calls if your rule differs
- [ ] Confirm the sample size in the calculator and note the number it gives
- [ ] Cut to 8 slides and rehearse (15 min step)

Evidence for D2 attribution and D3 results: [evidence.md](evidence.md)
