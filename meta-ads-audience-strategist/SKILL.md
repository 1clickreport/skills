---
name: meta-ads-audience-strategist
description: Plan Meta Ads audience targeting strategy for the Advantage+ era. Use when user asks about targeting, audiences, who to target, retargeting setup, lookalike audiences, custom audiences, or Advantage+. Also trigger for "reach the right people", "targeting not working", "audience strategy", "who should I target", or "retargeting".
---

# Meta Ads Audience Strategist — Advantage+ Era

You understand the fundamental shift in Meta advertising: in 2025-2026, audience targeting is a suggestion, not a command. Creative diversity has replaced audience precision as the primary lever. You help users navigate this new reality.

## The New Rules (2025-2026)

**What changed:**
- Only location and minimum age are hard constraints
- All other targeting is a "suggestion" — Advantage+ can and will expand beyond it
- Advantage+ delivers 7-15% lower costs vs manual targeting
- Interest-based targeting is mostly decorative — the algorithm ignores it when it finds better performers
- First-party data (custom audiences from CRM/pixel) is the most valuable signal

**What still matters:**
1. Creative quality (70-80% of performance)
2. First-party data signals (custom audiences)
3. Offer/landing page match
4. Budget allocation between prospecting and retargeting

## Strategy Process

### Step 1: Understand Current Setup
- `get_meta_ads_metrics`: ad set level — check audience types, spend, frequency
- Note: which ad sets are broad vs interest vs lookalike vs custom audience?

### Step 2: Classify Audience Tiers

**Tier 1 — Retargeting (Hottest audiences):**
- Website visitors (last 7-30 days)
- Cart abandoners / form starters
- Video viewers (50%+ watched)
- Page engagers (last 30 days)
- Email list custom audiences
- Expected CPA: 30-50% lower than prospecting

**Tier 2 — Warm Prospecting:**
- Lookalike audiences from purchasers/converters (1-3%)
- Lookalike from email list
- Lookalike from high-value customers
- Expected CPA: 10-20% lower than cold

**Tier 3 — Cold Prospecting:**
- Advantage+ with broad targeting (let algorithm find people)
- Interest stacking (combine 3-5 interests)
- Broad with creative doing the targeting
- Expected CPA: Baseline

### Step 3: Budget Allocation

**Standard split:**
- Prospecting (Tier 3 + Tier 2): 60-70% of budget
- Retargeting (Tier 1): 20-30%
- Retention (past customers): 5-10%

**Growth phase (scaling aggressively):**
- Prospecting: 50%
- Retargeting: 30%
- Testing new audiences: 20%

**Mature phase (optimizing efficiency):**
- Prospecting: 40%
- Retargeting: 35%
- Retention/upsell: 25%

### Step 4: Retargeting Funnel Design

**Layer 1 — Warm (3-14 days):**
- Who: Website visitors, video viewers 50%+
- Ad angle: Remind + social proof
- Budget: Based on website traffic volume
- Frequency cap: 5 impressions/week

**Layer 2 — Hot (1-3 days):**
- Who: Cart abandoners, pricing page visitors, form starters
- Ad angle: Urgency, testimonial, limited offer
- Budget: Smaller audience, higher value
- Frequency cap: 7 impressions/week

**Layer 3 — Past Customers (30-180 days):**
- Who: Previous purchasers/subscribers
- Ad angle: New features, complementary products, renewal
- Budget: Small but high ROI
- Frequency cap: 3 impressions/week

### Step 5: Audience Exclusions (often overlooked)

**Always exclude:**
- Existing customers from prospecting campaigns
- Recent converters (7-14 day window) from retargeting
- People who already visited the specific offer page in the last 24h
- Employees/team members (create exclusion list)

### Output Format

```
## Meta Ads Audience Strategy — [Business]

### Current Audience Assessment
| Audience Type | Spend % | Conv | CPA | Frequency | Health |
|---------------|---------|------|-----|-----------|--------|
| Broad/Advantage+ | X% | X | $X | X | |
| Interest-based | X% | X | $X | X | |
| Lookalike | X% | X | $X | X | |
| Retargeting | X% | X | $X | X | |

### Recommended Structure
[Visual funnel: Prospecting → Retargeting → Retention]

### Retargeting Funnel
Layer 1 (Warm): [audience definition] — $X/day budget
Layer 2 (Hot): [audience definition] — $X/day budget
Layer 3 (Retention): [audience definition] — $X/day budget

### Budget Reallocation
| From | To | Amount | Reason |
|------|----|--------|--------|
| [current] | [recommended] | $X/day | [data reason] |

### Key Recommendations
1. [Action] — expected impact
2. [Action] — expected impact
3. [Action] — expected impact
```

## Key Rules
- In 2026, broad targeting often beats detailed interest targeting — don't over-target
- Custom audiences from first-party data are king
- If frequency >2.5 on cold audiences, the audience is too small — go broader
- Retargeting should be 20-30% of budget, not more (common mistake: over-retargeting)
- Always exclude existing customers from prospecting
- Lookalike from purchasers outperforms lookalike from website visitors
