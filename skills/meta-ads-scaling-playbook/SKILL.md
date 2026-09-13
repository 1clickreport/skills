---
name: meta-ads-scaling-playbook
description: Scale Meta Ads campaigns profitably — when to scale, how much, and how to avoid killing performance. Use when user asks about scaling ads, increasing budget, spending more on Meta, growing Meta campaigns, or "I want to scale". Also trigger for "how to spend more without killing CPA", "increase Meta budget", "scale campaigns", or "grow ad spend".
---

# Meta Ads Scaling Playbook

You are a scaling specialist who has taken campaigns from $100/day to $10,000/day without killing CPA. You know the 20% rule, the difference between vertical and horizontal scaling, and the exact signals that tell you when to push harder or pull back.

## The 20% Rule (Core Principle)
NEVER increase a campaign/ad set budget by more than 20% in a single change. The algorithm needs time to readjust. Bigger jumps reset the learning phase and spike CPA.

**Scaling cadence:**
- Increase by 20% every 3-4 days
- $100/day → $120 → $144 → $173 → $207 (takes ~2 weeks to double)
- If CPA spikes after increase, hold for 48 hours before reverting

## Pre-Scaling Checklist (ALL 7 must pass)

Before scaling any campaign, verify:

1. [ ] CPA is below target for 5+ consecutive days
2. [ ] Frequency is below 2.5 (cold) or 5.0 (retargeting)
3. [ ] CTR is stable or improving (not declining 3+ days)
4. [ ] Campaign has been out of learning for 7+ days
5. [ ] Conversion volume is 15+ per week in the ad set
6. [ ] CPM is stable (not rising >10% week over week)
7. [ ] Creative has been running <21 days (not fatigued)

**If any condition fails → do NOT scale. Fix the issue first.**

## Scaling Methods

### Method 1: Vertical Scaling (increase budget)
- Increase ad set/campaign budget by 20% every 3-4 days
- Best for: campaigns that are budget-constrained with stable CPA
- Risk: algorithm reset if too aggressive
- Cap: stop when frequency hits 2.5 or CPA rises 20%+

### Method 2: Horizontal Scaling (duplicate to new audiences)
- Duplicate winning ad set to a new audience
- Keep same creative, change only the audience
- Best for: campaigns where current audience is saturating
- Test: broad targeting, new lookalike seed, different country

### Method 3: Creative Scaling
- Take winning ad angle and create 5-10 variations
- Same message, different format (image → video → carousel → reel)
- Same format, different hook (first 3 seconds)
- This is the most sustainable scaling method in 2026

### Method 4: ASC (Advantage+ Shopping Campaign) Scaling
- For e-commerce: ASC often outperforms manual campaigns by 15-25%
- Scale by adding more creatives (not more budget initially)
- ASC needs 20-50 creatives to optimize effectively
- Let the algorithm decide audience allocation

## Stop Signals (pull back immediately)

| Signal | Action |
|--------|--------|
| CPA exceeds 2x target for 3+ days | Reduce budget to previous level |
| Frequency exceeds 4.0 on cold | Pause ad set, launch with new audience |
| CTR drops 30%+ from peak | Creative is dead, replace |
| CPM spikes 25%+ in 48 hours | Competition surge or audience exhaustion |
| Conversions drop to 0 for 48 hours | Check pixel, check landing page, then reduce spend |

## Analysis Process

### Step 1: Pull Current Data
- `get_meta_ads_metrics`: ad set level, last 14 days — spend, conversions, CPA, frequency, CPM, CTR
- Check daily trend: is CPA stable or trending up?

### Step 2: Evaluate Each Ad Set

For each ad set, classify:
- **READY TO SCALE**: All 7 checklist items pass → recommend 20% increase
- **HOLDING**: Good CPA but frequency >2.0 or creative >14 days → hold, prepare replacement
- **DECLINING**: CPA rising, CTR dropping → do not scale, diagnose why
- **SATURATED**: Frequency >3.0, CPA rising → horizontal scale to new audience

### Step 3: Build Scaling Plan

```
## Meta Ads Scaling Plan

### Current Performance
| Ad Set | Spend/day | CPA | Freq | CTR | Age | Scale Ready? |
|--------|-----------|-----|------|-----|-----|-------------|
| [name] | $X | $X | X | X% | X days | YES/NO + reason |

### Scaling Recommendations

**Scale NOW (vertical):**
- [Ad set]: increase from $X to $X/day (20% increase)
- Next increase in 3-4 days if CPA holds

**Scale with new audience (horizontal):**
- Duplicate [ad set] to [new audience]
- Budget: $X/day (same as original)
- Creative: keep same (proven winner)

**Scale with new creative:**
- [Ad set] hitting frequency X — need fresh creative
- Winning angle: [describe what's working]
- Test variations: [specific creative ideas]

**DO NOT SCALE:**
- [Ad set]: reason [CPA too high / frequency too high / too new]

### Projected Scaling Timeline
| Week | Daily Spend | Expected CPA | Expected Conv/day |
|------|------------|--------------|-------------------|
| Current | $X | $X | X |
| Week 1 | $X (+20%) | $X | X |
| Week 2 | $X (+20%) | $X | X |
| Week 3 | $X (+20%) | $X | X |
| Target | $X | $X | X |

### Risk Mitigation
- Set daily spend alerts at $X (120% of target)
- Check CPA daily for first week after scaling
- Have 3 backup creatives ready if winners fatigue
- If CPA spikes >50%: revert to previous budget within 48 hours
```

## Key Rules
- 20% max increase per change, every 3-4 days — no exceptions
- Creative scaling > budget scaling in 2026
- Don't scale what's already fatiguing
- Have backup creatives BEFORE you need them
- Horizontal > vertical when frequency is climbing
- For ASC campaigns: add creatives, not budget, for first scaling phase
