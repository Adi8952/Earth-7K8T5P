# Checkpoint 3: Action and Control

**Team Netflix · Earth 7K8T5P** · Builds on [Checkpoint 2](../Checkpoint2/README.md) · Evidence: [evidence.md](../Checkpoint2/evidence.md)

> **Note to self: what can DoomCopy never copy?**
> What members have chosen to tell us, with permission, about what they enjoy. DoomCopy can match our price and our ads on day one. It cannot match consented viewing history, and it cannot buy the trust that makes members keep sharing it. Every action below either collects that data with consent or uses it to bring a member back.

---

## 1. Action: 100-day timeline

Budget lines (#1 to #10) are the ones in Checkpoint 2. Total stays **$250,000**.

| Phase | Days | What happens | CP2 lines | Owner (role) | Done when |
|---|---|---|---|---|---|
| **1. Build and baseline** | 1-30 | Set up consent capture and preference centre. Build tracking and a dashboard. Build flows F1 to F4 (section 2) in HubSpot. Write the approved-facts and approved-offer tables for AI drafting. Run the first AI drafts through human approval. Start brand-search defence and retargeting (already efficient). Brief and contract creators. Build the CRO test. | 1, 2, 3, 9 | CRM lead (flows), Data analyst (tracking, dashboard), Privacy officer (consent), Performance manager (search, Meta) | Flows pass a test send to staff accounts only. Baselines for win-back rate, inactive-30+ share and key-event rate are written down. Privacy page and consent wording signed off. |
| **2. Launch and learn** | 31-70 | Flows go live to real members, with the holdout running. CRO test A vs B starts. Lookalike and Google category/PMax fixes start (negatives, tighter keywords, lookalike seed from customers). First 6 to 8 creator posts with disclosure. Community posting starts. Weekly rival-ad check on brand terms. **Day 50: release the $15,000 reserve** to the line with the best ROAS (rule in section 3). | 4, 5, 6, 7, 8, 10 | CRM lead, Performance manager, Influencer manager, Community manager, Product/CRO manager | CRO test reaches its planned sample. Holdout has at least 375 members in each arm (section 3). First read of F1/F2 results. |
| **3. Decide and scale** | 71-100 | Read the holdout and the CRO test at the planned sample, not earlier. Scale what beat its target, fix or stop what did not. Re-run the D3 scale / fix / pause table on new data. Write the day-100 report for the CMO. | All | CMO (decisions), Data analyst (report), all line owners | Every line has a scale / fix / pause call backed by a number. K1 first read reported. |

**Decision gates**

| Day | Gate | Rule |
|---|---|---|
| 30 | Ready to launch? | Consent check passes, tracking verified, no AI message without human approval. If not, launch slips; budget does not move. |
| 50 | Reserve release | Move the $15,000 to the best-performing line **by ROAS**, only if it is under the cap of its own audience size (brand search is capped by search volume). |
| 70 | CRO and holdout read | Ship B only if it reaches the planned sample and the lift holds at 95% confidence. Otherwise keep A. |
| 100 | Review | Scale at ROAS 3+, fix between 1 and 3, pause below 1 unless D2 shows it assists (same rule as CP2). |

**What can change in 100 days.** K1 (first-12-month churn, 37.6% to 33.6%) is a slow metric. Inside 100 days we expect to see leading signs first: win-back rate in the flows versus the holdout, and the share of subscribers inactive 30+ days (14.7% today). The K1 read at day 100 is a first reading, not the final verdict.

---

## 2. Automation flows to build in HubSpot

HubSpot is the working choice here: one place for contact properties, lists, branching workflows and a consent record. MailerLite would work for a lean team but we keep one tool to hold consent and flows together.

Every flow starts with the same gate: **contact has marketing consent for that channel, and has not unsubscribed.** If not, the contact is skipped.

| Flow | Trigger (from D5) | Message idea | Channel | Exit |
|---|---|---|---|---|
| **F1. Early drift** | 14 days since last login (24.1% churn in the 14-29 day band) | "Next episode" for something the member started | Email, then push | Member logs in |
| **F2. Win-back** | More than 30 days since last login (65.3% churn, 14.7% of subscribers, 45.6% of all churn) | "New in your genre", from approved titles only | Email, push, in-app | Member logs in, or after 3 messages with no response |
| **F3. Payment recovery** | 1 or more payment failures in 90 days (36.5% churn, 14.8% of subscribers) | Plain reminder to update the payment method | Email, in-app | Payment succeeds |
| **F4. First-year welcome** | Tenure 12 months or less (37.6% churn, 25.5% of subscribers; this is K1) | "Pick 3 titles you like" (same idea as the CRO test) | In-app, email | Member completes onboarding or reaches month 12 |
| **F5. Champions protect** | Top segment from D4 (14.5% of customers, 42.9% of revenue) | New releases in their taste. No discount. | Email | Ongoing, capped at a set number of messages per month |

**Signal check that changes the CP2 loop.** CP2 says nudges at 7, 14 and 30 days. In the D5 data, members 7-13 days inactive churn at 9.6% and members under 7 days at 8.9%, so a 7-day nudge has little signal. First nudge moves to **day 14**. Churn jumps to 24.1% at 14-29 days and 62.8% at 30+ days.

**AI use** stays as in CP2: AI drafts subject lines and variants from the approved-facts table, never receives personal data, and a human approves every message. 10% of live messages are spot-checked weekly.

---

## 3. Control

### Dashboard mock-up

Reuse the L3 Data Studio layout (header, KPI row, channel table, trend). Baselines below come from the practice data; the live values stay empty until launch.

```
+----------------------------------------------------------------------------+
| NETFLIX 100-DAY PLAN        Date range: [Day 1 - 100]   Segment: [All v]    |
+--------------+--------------+--------------+--------------+----------------+
| K1 First-yr  | Inactive 30+ | Win-back vs  | Blended ROAS | CRO key-event  |
| churn        | share        | holdout      | (all paid)   | rate (A vs B)  |
| base 37.6%   | base 14.7%   | base: day 30 | base 1.93    | base 2.6%      |
| target 33.6% | live  --     | live  --     | live  --     | target 3.2%    |
+--------------+--------------+--------------+--------------+----------------+
| Channel table: spend | ROAS | CPA | call (Scale / Fix / Pause)              |
|  Brand search   base ROAS 7.60  CPA $12.50  target CPA under $15            |
|  Retargeting    base ROAS 3.48  target above 3.0                            |
|  Lookalike      base ROAS 2.09  target 2.5                                  |
|  Category+PMax  base CPA ~$46   target $35                                  |
+----------------------------------------------------------------------------+
| Trend: days since login bands (under 7 | 7-13 | 14-29 | 30+) per week       |
| Flow table: sent | opened | returned | holdout returned | unsubscribed       |
+----------------------------------------------------------------------------+
| Weekly checks: brand-term impression share (target 90%+) | AI spot-check   |
+----------------------------------------------------------------------------+
```

Review rhythm: CRM and search numbers weekly, channel calls every two weeks, CMO review at days 30, 70 and 100.

### Attribution model choice (from L4)

**Primary model for budget decisions: position-based (40% first, 40% last, 20% shared).** Reasons from D2:

- Last-click gives Direct $580 of $960 (60%) and Paid Social, Organic Search and Organic Social nothing. Direct mostly collects people other channels introduced.
- First-click gives Paid Social the most ($270, 28%), but ignores who closed the sale.
- Position-based credits both ends: Paid Social $148, Email $114, Paid Search $230, Direct $254. Email sits in 4 of 10 paths, so it is credited as a connector.
- We still show last-click next to it on the dashboard so the CMO can see the gap.

**Limit:** D2 has only 10 paths. No attribution model proves cause. That is why the holdout below exists.

### Churn signal to watch (from L5)

**Days since last login.** At more than 30 days it flags 14.7% of subscribers who hold 45.6% of all churn, with a 65.3% churn rate. Watch the 14-29 day band weekly as the early warning (24.1% churn). Backups in the same data: fewer than 5 sessions in the last 30 days (55.3% churn) and 1+ payment failures (36.5%).

### Holdout test

- **Question:** does the F2 win-back flow reduce churn, or would those members have returned anyway?
- **Design:** members who cross 30 days inactive are randomly assigned to *flow* or *holdout*. Holdout gets no marketing messages from F2 (service and billing messages still go).
- **Primary metric:** share who churn within 60 days of crossing 30 days inactive. The 60-day window is an assumption; D5 has no time window, so confirm it with your data owner.
- **Size:** baseline 65.3%. To detect a 10-point drop (to 55.3%) at 95% confidence and 80% power, we need **about 375 members per arm**. A 7-point drop needs about 755 per arm. We collect until the planned size, as members cross day 30, and do not stop early.
- **Second holdout (measurement, CP2 line 9):** pause one brand-term ad group in one market for 2 weeks to see how many brand searches still convert through organic. Run only if the brand-search line is close to its volume cap.

### Privacy and consent design

Link: [Privacy page](../Privacy/README.md) *(replace with your real path; the Checkpoint 1 zip I received held only empty folders)*.

- **Consent first:** each channel (email, push, in-app) has its own opt-in, recorded in HubSpot with date and source. No consent, no message.
- **Plain language:** the sign-up and the preference centre say what we use viewing data for, in one or two sentences.
- **Easy opt-out:** one-click unsubscribe in every message. Opt-outs are honoured before the next send.
- **Data minimum:** flows use the fields they need (days since login, plan, segment), not full viewing history. AI prompts hold segment names and approved facts only, never personal data.
- **Retention:** keep contact and flow data only as long as the member relationship and the law require. Legal sets the number.
- **Markets:** follow local rules where members live (for example GDPR in the EU, India's DPDP Act). Confirm with legal before launch.
- **Influencers:** paid-partnership label and "#ad" on every post (CP2).

### Top three risks

| # | Risk | Early warning | Mitigation | Owner |
|---|---|---|---|---|
| 1 | **We over-trust practice data.** D2 has 10 paths, D3 has 8 campaigns, D3 has no margins (ROAS is not profit) and no influencer or CRM data. | Results at day 30 to 50 differ sharply from the practice numbers | Treat every number as a starting hypothesis. Holdouts decide cause. Get margins before scaling any line with ROAS under 2. | Data analyst |
| 2 | **A message breaks consent or states something false.** AI could invent a title, price or offer; a contact could be messaged without opt-in. | Spot-check finds an unapproved claim; unsubscribe or complaint rate rises | Approved-facts table, human approval of every message, consent gate at the start of every flow, weekly 10% spot-check. A single failure pauses that flow. | Privacy officer, CRM lead |
| 3 | **DoomCopy reacts.** It bids on our brand terms, or cuts price. | Brand-term impression share falls under 90%, or CPA on brand terms passes $15 | Weekly rival-ad check and trademark reports; shift weight to owned flows, which DoomCopy cannot copy; reserve held until day 50. | Performance manager, CMO |

---

## 4. Watcher self-audit (for the team that audits us)

**Every figure traced to data** (recomputed from the four practice CSVs):

| Claim | Source | Recomputed |
|---|---|---|
| Spend $18,400, revenue $35,480, ROAS 1.93, 397 conversions | D3 | 1.928 |
| Brand ROAS 7.60, CPA $12.50; Retargeting 3.48, $25.86 | D3 | match |
| Paid Social 28% under first-click ($270 of $960) | D2 | 28.1% |
| Email 17% under linear, 7% under last-click | D2 | 17.2% / 7.3% |
| Inactive more than 30 days: 14.7% of subscribers, 65.3% churn, 45.6% of churn | D5 | match |
| First-12-month churn 37.6% (306 subscribers) | D5 | 37.6% |
| 375 members per arm for the holdout | formula, two-proportion test | 375 |

**Assumptions, not data:** scale / fix / pause thresholds (3 and 1); 60-day holdout window; all targets (33.6%, 3.2%, 2.5, $35, $15); the 90% impression-share goal; the choice of position-based model; all role names. The AI listening-test figure (85% match) comes from your Mission Log, which I could not open, so it is unverified here.

**Two corrections to Checkpoint 2 (both fixed in the updated evidence.md and checkpoint_2.md; the 7-day nudge is also removed from the CP2 loop):**

1. `evidence.md` says Paid Social "opens 4 of 10 paths". The path file shows it opens **3** (P1, P4, P9). Organic Social opens P6. Fix the line; the 28% credit figure is still right.
2. CP2 gives about 12,400 sessions per variation for the CRO test. A standard two-proportion formula gives about 12,300. Use the number the Evan Miller calculator returns, and write it down.

---

## 5. Still to complete

- [ ] Replace the Privacy link and paste your real L3 Data Studio screenshot over the mock-up
- [ ] Confirm the holdout window (60 days) and the baseline for win-back rate on day 30
- [x] Fix the "4 of 10" line in `evidence.md` (done: 3 of 10)
- [ ] Cut to 8 slides and rehearse 7 minutes (next step)
