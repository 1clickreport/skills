# 1ClickReport Skills for Claude

> 15 production-tested Claude Agent Skills for marketing analytics, campaign management, and agency operations across Google Ads, Meta Ads, GA4, and Search Console.

These skills are designed to be used alongside the **[1ClickReport MCP server](https://github.com/1clickreport/mcp)** — Claude automatically invokes the right skill based on your prompt, then uses 1ClickReport's 40 MCP tools to fetch real data from your connected ad accounts.

## What is a Claude Agent Skill?

Skills are **modular capabilities that extend Claude's functionality**. Each skill packages instructions, methodology, and triggers so Claude automatically engages it when the user's prompt matches. Skills make Claude behave like a domain expert (e.g., a senior Google Ads strategist or a Meta creative auditor) instead of generic.

## Skills index

### Agency operations (5 skills)

| Skill | Triggers when user asks about |
|---|---|
| **[agency-account-audit](agency-account-audit/SKILL.md)** | Multi-platform account audit, account health check, full marketing review |
| **[agency-budget-optimizer](agency-budget-optimizer/SKILL.md)** | Budget allocation across channels, where to spend, shifting spend |
| **[agency-client-report](agency-client-report/SKILL.md)** | Client reports, monthly/weekly summaries, executive performance summaries |
| **[agency-search-term-optimizer](agency-search-term-optimizer/SKILL.md)** | Wasted spend, search term analysis, negative keyword opportunities |
| **[agency-weekly-review](agency-weekly-review/SKILL.md)** | Weekly check-ins, "what happened this week", Monday performance reviews |

### Cross-channel strategy (1 skill)

| Skill | Triggers when user asks about |
|---|---|
| **[cross-channel-budget-optimizer](cross-channel-budget-optimizer/SKILL.md)** | Google Ads vs Meta Ads spend mix, channel-level budget decisions |

### Google Ads (4 skills)

| Skill | Triggers when user asks about |
|---|---|
| **[google-ads-audit](google-ads-audit/SKILL.md)** | Google Ads account audit, 7-category scoring, "what's wrong with my ads" |
| **[google-ads-bidding-strategist](google-ads-bidding-strategist/SKILL.md)** | Smart Bidding strategy, manual CPC vs target CPA vs target ROAS choice |
| **[google-ads-campaign-builder](google-ads-campaign-builder/SKILL.md)** | Building a new Google Ads campaign from scratch with proper structure |
| **[google-ads-keyword-researcher](google-ads-keyword-researcher/SKILL.md)** | Keyword research, search volume, keyword opportunities for Ads or SEO |

### Meta Ads (5 skills)

| Skill | Triggers when user asks about |
|---|---|
| **[meta-ads-audit](meta-ads-audit/SKILL.md)** | Meta Ads account audit (75-point framework), Facebook Ads health check |
| **[meta-ads-audience-strategist](meta-ads-audience-strategist/SKILL.md)** | Meta targeting strategy in the Advantage+ era, audience planning |
| **[meta-ads-budget-allocator](meta-ads-budget-allocator/SKILL.md)** | Meta budget split, prospecting vs retargeting allocation |
| **[meta-ads-creative-auditor](meta-ads-creative-auditor/SKILL.md)** | Creative fatigue detection, finding winning ads, creative testing plans |
| **[meta-ads-scaling-playbook](meta-ads-scaling-playbook/SKILL.md)** | Scaling Meta campaigns without killing performance |

---

## How to install

### Option 1 — Install via Claude.ai

Skills must be installed manually until Anthropic provides a directory install path. For now:

1. Clone this repo:
   ```bash
   git clone https://github.com/1clickreport/skills.git
   ```

2. Copy individual skill folders into your Claude skills directory:
   - **Claude Code**: `~/.claude/skills/<skill-name>/`
   - **Claude Desktop**: same path

3. Restart Claude — the skill auto-triggers based on your prompts.

### Option 2 — Use the bundled ZIPs

Pre-built ZIPs of each skill (and bundle ZIPs grouping related skills) are available at:

→ [1clickreport.com/skills](https://www.1clickreport.com/skills/)

Direct downloads with one-click install instructions.

---

## How skills work with the 1ClickReport MCP

The skills assume you've connected the **[1ClickReport MCP server](https://github.com/1clickreport/mcp)** to Claude (URL: `https://mcp.1clickreport.com/mcp`). Each skill's instructions reference specific MCP tools like `get_google_ads_metrics`, `audit_google_campaign`, `analyze_ga4_funnel`, etc.

Without the 1ClickReport MCP connected, skills still work as "thinking frameworks" — Claude will follow the methodology but won't have live data to apply it to.

With the MCP connected, skills become **executable strategies**: Claude pulls live data via MCP tools, applies the skill's framework, and returns ranked recommendations grounded in your actual ad account state.

---

## File structure

```
<skill-name>/
  SKILL.md   ← frontmatter (name + description + triggers) + instructions
```

Each `SKILL.md` follows the standard Claude Agent Skill format:

```yaml
---
name: <skill-name>
description: <one-paragraph description with trigger phrases>
---

<skill body — methodology, framework, decision rules>
```

---

## License

MIT — see [LICENSE](LICENSE).

These skills are documentation/instructions, not executable code. Free to use, modify, fork, and distribute.

---

## Maintainer

Built by [Suryansh Jaiswal](https://www.linkedin.com/in/suryanshjaiswal/) — founder of [1ClickReport](https://www.1clickreport.com), operated by AI Labs LLC (Sharjah Media City Free Zone, UAE).

- Email: suryansh@1clickreport.com
- Product: https://www.1clickreport.com
- MCP server: https://github.com/1clickreport/mcp
- Skills downloads: https://www.1clickreport.com/skills/
