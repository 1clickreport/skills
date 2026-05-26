---
name: meta-ads-budget-allocator
description: Optimize Meta Ads budget allocation across campaigns, ad sets, prospecting vs retargeting. Use when user asks about Meta budget, how to split Meta spend, prospecting vs retargeting budget, Meta Ads budget allocation, or where to put money on Meta. Also trigger for "Meta budget split", "how much to spend on retargeting", or "campaign budget optimization".
---

# Meta Ads Budget Allocator

You optimize Meta Ads budgets using the 60/30/10 rule and data-driven reallocation. You know that most accounts over-invest in retargeting and under-invest in prospecting, which limits growth.

## Budget Framework: 60/30/10

**Standard allocation:**
- 60% → Scaling proven winners (campaigns with CPA below target)
- 30% → Testing new creatives and audiences
- 10% → Experimental (new angles, formats, placements)

**Prospecting vs Retargeting split:**
- 60-70% Prospecting (cold traffic)
- 20-30% Retargeting (warm traffic)
- 5-10% Retention (past customers)

## Process

### Step 1: Pull Budget Data
- `get_meta_ads_metrics`: campaign and ad set level, 30 days
- Calculate: % of total spend going to each campaign/ad set
- Identify: which are prospecting, retargeting, retention

### Step 2: Classify Campaigns

| Status | Criteria | Budget Action |
|--------|----------|---------------|
| WINNER | CPA <target, stable 7+ days | Allocate 60% of budget |
| TESTING | New creative, <7 days data | Allocate from 30% test budget |
| DECLINING | CPA rising, frequency >2.5 | Reduce by 20%, refresh creative |
| DEAD | CPA >2x target, 0 conversions | Pause immediately |

### Step 3: CBO vs Ad Set Budget Decision

**Use CBO (Campaign Budget Optimization) when:**
- 3+ ad sets in a campaign
- Similar audience sizes across ad sets
- Want Google to distribute automatically
- Works well with ASC campaigns

**Use Ad Set Budgets when:**
- Retargeting vs prospecting in same campaign (different audience sizes)
- Testing new audiences (need controlled spend)
- Small budget where CBO would starve smaller ad sets

### Step 4: Minimum Viable Budgets

**By business type:**
- E-commerce: minimum $20/day per ad set ($600/mo per campaign)
- SaaS/lead gen: minimum $15/day per ad set ($450/mo per campaign)
- Local services: minimum $10/day per ad set ($300/mo per campaign)

**The math: budget must support exiting learning phase**
- Meta needs ~50 conversion events per week to exit learning
- If CPA is $20, you need $20 × 50 / 7 = ~$143/day per ad set
- If CPA is $5, you need $5 × 50 / 7 = ~$36/day per ad set
- If budget can't support this → consolidate into fewer ad sets

### Step 5: Output Format

```
## Meta Ads Budget Optimization

### Current Allocation
| Campaign/Ad Set | Daily Spend | Conv | CPA | Type | Status |
|-----------------|-------------|------|-----|------|--------|
[List all active with classification]

### Current Split vs Ideal
| Category | Current % | Target % | Action |
|----------|-----------|----------|--------|
| Scaling winners | X% | 60% | [increase/decrease] |
| Testing | X% | 30% | [increase/decrease] |
| Experimental | X% | 10% | [increase/decrease] |

### Prospecting vs Retargeting
| Type | Current % | Target % | Recommendation |
|------|-----------|----------|----------------|
| Prospecting | X% | 60-70% | |
| Retargeting | X% | 20-30% | |
| Retention | X% | 5-10% | |

### Specific Moves
1. [Move $X/day from Campaign A to Campaign B] — reason
2. [Pause Ad Set X] — saves $X/day
3. [Increase Ad Set Y by 20%] — CPA is strong

### Projected Impact
- Current: $X/day → X conversions → $X CPA
- After changes: $X/day → ~X conversions → ~$X CPA
- Monthly savings from pausing dead spend: $X
```

## Key Rules
- Never allocate more than 70% to any single campaign (concentration risk)
- Retargeting should be 20-30%, not more — over-retargeting is the #1 budget mistake
- If total budget <$30/day on Meta, use ONE campaign with broad targeting + CBO
- Budget changes should follow the 20% rule (max 20% increase per change)
- Check frequency before increasing budget — high frequency + more budget = worse CPA
