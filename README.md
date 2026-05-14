# job-seeker

A Claude Code skill for evaluating job opportunities against a personal career profile. Given one or more company names or URLs, it researches Glassdoor, Kununu, Levels.fyi, Comprehensive.io, LinkedIn, Greenhouse, Xing, Indeed.de, Monster.de, Remotely.de, Layoffs.fyi, Hiring.cafe, Builtin.com, and Wellfound.com — and produces structured, source-cited evaluation reports.

The skill is **profile-driven**: all fit assessments, salary thresholds, and role filters are derived from `PROFILE.md`. Edit that file with your own details before first use.

---

## Skills

### `job-evaluator`

Triggered automatically when you mention a company name or job posting URL. Produces a structured report covering:

- Employee sentiment (Glassdoor, Kununu)
- Salary benchmarks (Levels.fyi, Comprehensive.io)
- Layoff history (Layoffs.fyi)
- Open positions (LinkedIn, Greenhouse, Xing, Indeed.de, Monster.de, Remotely.de, Hiring.cafe, Builtin.com, Wellfound.com, careers page)
- Candidate fit across stack, work model, compensation, equity, culture, and stability

All data points are cited. Missing data is marked `"data not available"` — never inferred.

---

## Setup Your Profile

`PROFILE.md` is gitignored — your personal data (salary, employer, contact info) never gets committed.

```bash
cp PROFILE.example.md PROFILE.md
```

Then fill in your details:

- Name and current role
- Target roles (Principal, Staff, SRE, EM, etc.)
- Tech stack and domain expertise
- Work model preferences (remote / hybrid / city)
- Minimum base salary and equity expectations
- Language requirements

The skill reads this file at runtime and personalises every report to your profile.

---

## Usage

### Single company

```
Evaluate Elastic for me
```

```
Should I apply to Dynatrace? Here's the job: https://careers.dynatrace.com/jobs/...
```

```
What do employees say about Grafana Labs?
```

### Multiple companies

```
Compare Datadog, Elastic, and Dynatrace — which fits best?
```

---

## Output

Each report includes:

- **⚡ Quick Overview** — Glassdoor/Kununu scores, CEO approval, recommendation rate, recent layoffs
- **⚠️ Layoff History** — Events from Layoffs.fyi with dates, size, and reasons
- **💰 Salary & Package** — Market ranges, equity, bonus, benefits
- **✅ Pros / ❌ Cons** — Most common employee feedback
- **🎯 Candidate Fit** — Assessed against your PROFILE.md (stack, role, location, salary, equity, culture, stability)
- **💼 Open Positions** — Matching roles from all job sources (LinkedIn, Greenhouse, Xing, Indeed.de, Monster.de, Remotely.de, Hiring.cafe, Builtin.com, Wellfound.com) with direct apply links
- **🔗 Sources** — Every source searched with link or explicit "no results"
- **🏁 Decision** — 🟢 Apply / 🟡 Research More / 🔴 Skip

Multiple companies get a side-by-side comparison table at the end.

---

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | Skill definition — research steps, report template, data integrity rules |
| `PROFILE.example.md` | Generic profile template — copy to `PROFILE.md` and fill in your details |
| `PROFILE.md` | Your personal profile — **gitignored**, never committed |
| `README.md` | This file |

---

## Example Output

Running the skill against 10 companies in the observability/SaaS/cloud space:

### 📊 TOP 10 COMPANY FIT SUMMARY

> Scoring: **✅ = 14%**, **⚠️ = 7%**, **❌ = 0%** across 7 criteria

| # | Company | Glassdoor | Stack Fit | Role Available | Work Model | Salary €120K+ | Equity | IC Culture | **Total Fit** |
|---|---------|-----------|-----------|----------------|------------|----------------|--------|------------|--------------|
| 1 | **Elastic** | 4.0/5 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **85%** |
| 2 | **Dynatrace** | 3.9/5 | ✅ | ✅ | ✅ | ✅ | ✅ | ⚠️ | **79%** |
| 3 | **Datadog** | 4.2/5 | ⚠️ | ✅ | ⚠️ | ⚠️ | ✅ | ✅ | **70%** |
| 4 | **Grafana Labs** | 4.1/5 | ⚠️ | ✅ | ✅ | ⚠️ | ⚠️ | ✅ | **70%** |
| 5 | **HashiCorp (IBM)** | 4.0/5 | ✅ | ✅ | ⚠️ | ✅ | ❌ | ⚠️ | **64%** |
| 6 | **SUSE** | 3.8/5 | ✅ | ✅ | ⚠️ | ❌ | ❌ | ⚠️ | **50%** |
| 7 | **PagerDuty** | 3.6/5 | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | **43%** |
| 8 | **New Relic** | 3.6/5 | ⚠️ | ⚠️ | ✅ | ⚠️ | ❌ | ❌ | **36%** |
| 9 | **Confluent** | 3.6/5 | ⚠️ | ❌ | ⚠️ | ⚠️ | ❌ | ⚠️ | **29%** |
| 10 | **Honeycomb** | 3.3/5 | ⚠️ | ❌ | ✅ | ❌ | ❌ | ⚠️ | **21%** |

---

### 🏢 ELASTIC — 85% fit
**Industry:** Observability & Search SaaS | **Size:** ~3,800 | **Work Model:** Remote-first globally

#### ⚡ QUICK OVERVIEW
| Criteria | Value | Source |
|----------|-------|--------|
| Glassdoor Score | 4.0 / 5 | Glassdoor (850+ reviews) |
| Kununu Score | data not available | Kununu |
| CEO Approval | 71% | Glassdoor |
| Would Recommend | 77% | Glassdoor |
| Salary Competitiveness | ⭐⭐⭐⭐ | Levels.fyi |
| Recent Layoffs (12 mo) | ✅ None | Layoffs.fyi |

#### 💰 SALARY & PACKAGE
- **Market Range (target roles):** €115K–€158K base (Principal SWE, Germany) — Levels.fyi
- **Equity:** RSUs — liquid (NYSE: ESTC)
- **Bonus:** Performance-based; amount not confirmed for Germany
- **Benefits:** Home office stipend, health insurance, flexible PTO, L&D budget

#### ✅ PROS
- Truly remote-first — distributed by design, no RTO pressure
- AWS-native stack; Kubernetes and Java used across engineering
- Liquid RSUs on a public exchange
- Principal-level salary confirmed above €120K base in Germany
- 40+ countries of employees — English-first by default

#### ❌ CONS
- CEO approval among ICs on Glassdoor is only 37%
- Frequent restructures and shifting reporting lines flagged in 2025–2026 reviews
- Career growth at senior IC levels described as slow

#### 🎯 CANDIDATE FIT
| Criteria | Status | Notes |
|----------|--------|-------|
| Tech Stack (AWS, Java/Kotlin, K8s) | ✅ | AWS primary cloud, Java widely used, K8s-native |
| Target Role Available | ✅ | Principal SWE and SRE roles open in Germany/Europe |
| Work Model (Remote/Hybrid-Munich) | ✅ | Fully distributed — Munich is first-class |
| Salary €120K+ Base | ✅ | Confirmed €115K–€158K base for Principal in Germany |
| Equity Available | ✅ | Liquid RSUs (NYSE: ESTC) |
| English Working Environment | ✅ | English-only, 40+ countries |
| Engineering/IC Culture | ✅ | Explicit IC ladder, Staff/Principal levels, SRE-native |

#### 🏁 OVERALL ASSESSMENT
**Decision:** 🟢 APPLY

**Rationale:** Strongest all-round fit. Remote-first globally means Munich requires zero compromise. Principal-level salary confirmed above €120K in Germany, RSUs are liquid, and the engineering stack is a direct match. The only friction is internal restructuring instability and lower IC approval of leadership.

---

## Requirements

This skill uses web search to fetch live data. You need the **Tavily MCP server** configured in Claude Code.

```bash
claude mcp add tavily-mcp \
  -e TAVILY_API_KEY=tvly-YOUR_KEY_HERE \
  -- npx -y tavily-mcp
```

Get a free API key at [tavily.com](https://tavily.com) (1,000 searches/month free, no credit card required).

### Permissions

Add to `.claude/settings.local.json`:

```json
{
  "permissions": {
    "allow": [
      "WebSearch",
      "WebFetch(domain:www.glassdoor.com)",
      "mcp__tavily-mcp__tavily_search",
      "mcp__tavily-mcp__tavily_research",
      "mcp__tavily-mcp__tavily_extract"
    ]
  }
}
```
