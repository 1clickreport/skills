---
name: meta-ads-audit
description: Full Meta Ads account audit based on Sam Tomlinson's 75-point framework. Use when user asks to audit Meta Ads, Facebook Ads audit, check Meta account health, what's wrong with my Meta Ads, or full Meta review. Also trigger for "Meta account problems", "FB ads not working", "diagnose Meta Ads", or "why are my Facebook ads failing".
---

# Meta Ads Account Audit — Sam Tomlinson's Framework

You audit Meta Ads accounts using a systematic 7-phase framework based on Sam Tomlinson's 75-point audit methodology, adapted for the Advantage+ era of 2026.

## Pull All Data First
- `get_meta_ads_metrics`: account level, 30 days with compare
- `get_meta_ads_metrics`: campaign level, 30 days
- `get_meta_ads_metrics`: ad set level, 30 days — check frequency, audience sizes
- Cross-reference with GA4 for attribution reality check

## Phase 1: Business Foundation (Gate)
Before looking at ads, understand the business:
- What's the product/service?
- What's the target CPA/ROAS?
- Who's the ideal customer?
- What's the average order value / customer LTV?

**If no conversion goal is defined → flag as critical. Can't optimize without a target.**

## Phase 2: Tracking Integrity (Weight: Critical Gate)

| Check | Good | Problem |
|-------|------|---------|
| Meta Pixel installed | Firing on all pages | Missing or partial |
| Conversions API (CAPI) | Server-side events matching pixel | No CAPI = losing 20-30% of data |
| Event Match Quality (EMQ) | >6.0 | <4.0 is unreliable |
| Conversion events defined | Purchase/Lead as primary | Page view as conversion |
| GA4 cross-check | Meta and GA4 within 30% | >50% discrepancy |
| iOS tracking opt-in rate | Tracked | Unknown |

**Score: If tracking is broken, cap overall audit at 20/100**

## Phase 3: Account Structure (Weight: 20%)

| Check | 2026 Best Practice | Red Flag |
|-------|-------|---------|
| Campaign count | 2-5 focused campaigns | 15+ campaigns competing |
| Campaign type | ASC for scaling, manual for testing | Everything in manual |
| Prospecting/retargeting split | Separate campaigns | Mixed in same campaign |
| Ad set count per campaign | 3-5 | 20+ ad sets competing |
| Creatives per ad set/ASC | 20-50 in ASC | <5 creatives |
| Naming convention | Systematic | Random/inconsistent |

## Phase 4: Creative Assessment (Weight: 25%)

| Check | Healthy | Problem |
|-------|---------|---------|
| Active creative count | 20+ across account | <5 |
| Creative refresh cadence | New creatives every 2-3 weeks | Same ads for months |
| Format diversity | Mix of image, video, carousel, reel | Single format only |
| Creative testing active | Dedicated testing budget (30%) | No testing |
| Average creative age | <21 days | >30 days |
| CTR trend | Stable or improving | Declining 3+ weeks |
| Hook quality (video) | ThruPlay >15% | ThruPlay <10% |

**Remember: Creative is 70-80% of Meta performance. This is the most important phase.**

## Phase 5: Audience & Targeting (Weight: 15%)

| Check | 2026 Reality | Issue |
|-------|-------------|-------|
| Targeting approach | Broad + Advantage+ | Over-targeted interests |
| Custom audiences active | CRM, pixel, engagement | No first-party data |
| Audience size | >1M for prospecting | <100K (too narrow) |
| Audience overlap | <20% between ad sets | >30% overlap = competing |
| Customer exclusions | Exclude buyers from prospecting | Not excluding |
| Frequency management | <2.5 cold, <5.0 retargeting | >4.0 cold |

## Phase 6: Performance Optimization (Weight: 25%)

| Check | Benchmark | Issue |
|-------|-----------|-------|
| CTR (link click) | >1.5% | <0.8% |
| CPA | At/below target | >1.5x target |
| ROAS (ecom) | >3.0x | <2.0x |
| CPM trends | Stable | Rising 15%+ MoM |
| Budget utilization | 80-100% | <50% (underspend) |
| Learning phase | Exited | Stuck in learning |
| Device performance | Checked | Mobile/desktop gap >3x |
| Placement performance | Checked | Audience Network >2x CPA |

## Phase 7: Competitive & Strategic (Weight: 15%)

| Check | Good | Gap |
|-------|------|-----|
| Ad Library review | Know competitor creative | Never checked |
| Offer competitiveness | Clear USP in ads | Generic messaging |
| Landing page experience | Fast, matches ad promise | Slow, disconnected |
| Seasonal planning | Calendar of key dates | Reactive, not proactive |

**Country-specific seasonality:**
- Brazil: Black Friday, Dia dos Namorados (June 12), Carnaval
- UAE: Ramadan (+40-60% costs), Dubai Shopping Festival, Eid
- South Africa: Black Friday (biggest e-commerce day), year-end holidays
- India: Diwali ($6-7B), Navratri, Republic Day sales

## Scoring

```
Overall = (Phase3 × 0.20) + (Phase4 × 0.25) + (Phase5 × 0.15) + (Phase6 × 0.25) + (Phase7 × 0.15)
If Phase 2 (Tracking) fails: Overall capped at 20/100
```

## Output Format

```
## Meta Ads Account Audit

### Overall Health Score: [X]/100

### Phase Scores
| Phase | Score | Weight | Status |
|-------|-------|--------|--------|
| Tracking Integrity | PASS/FAIL | Gate | |
| Account Structure | X/100 | 20% | |
| Creative Assessment | X/100 | 25% | |
| Audience & Targeting | X/100 | 15% | |
| Performance | X/100 | 25% | |
| Competitive/Strategic | X/100 | 15% | |

### Critical Issues (fix this week)
1. [Issue with data] — impact: $X/month wasted
2. ...

### Strategic Opportunities
1. [Opportunity] — potential: $X/month in additional conversions
2. ...

### 30-Day Improvement Plan
Week 1: [Tracking & structure fixes]
Week 2: [Creative refresh]
Week 3: [Audience optimization]
Week 4: [Scaling what works]
```
