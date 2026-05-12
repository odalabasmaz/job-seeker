# job-seeker

A Claude Code skill for evaluating job opportunities against a senior engineer's profile. Researches companies across Glassdoor, Kununu, Levels.fyi, LinkedIn, and Remotely.de — and produces structured evaluation reports with salary data, employee sentiment, stack fit, and a clear apply/skip verdict.

## Skills

### `job-evaluator`

Triggered automatically when you mention a company name or job posting URL. Produces a structured report covering:

- Employee sentiment (Glassdoor, Kununu)
- Salary benchmarks (Levels.fyi, Glassdoor)
- Open positions (LinkedIn, Remotely.de)
- Candidate fit across stack, work model, compensation, equity, and culture

## Installation

```bash
claude skill install job-evaluator.skill
```

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

### Example output

Running the skill against 10 companies in the observability/SaaS/cloud space produced the following results:

---

#### 📊 TOP 10 COMPANY FIT SUMMARY

> Scoring: **✅ = 14%**, **⚠️ = 7%**, **❌ = 0%** across 7 criteria (stack, role, work model, salary, equity, language, IC culture)

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

#### 🏢 ELASTIC — 85% fit
**Industry:** Observability & Search SaaS | **Size:** ~3,800 | **Work Model:** Remote-first globally

##### ⚡ QUICK OVERVIEW
| Criteria | Value | Source |
|----------|-------|--------|
| Glassdoor Score | 4.0 / 5 | Glassdoor (850+ reviews) |
| Kununu Score | data not found | Kununu |
| CEO Approval | 71% Glassdoor / 89/100 Comparably | Mixed |
| Would Recommend | 77% | Glassdoor |
| Salary Competitiveness | ⭐⭐⭐⭐ | Levels.fyi |

##### 💰 SALARY & PACKAGE
- **Target Role Base Salary:** €115K–€158K base (Principal SWE, Germany). Median total comp €133K–€178K incl. equity + bonus.
- **Equity/Stock:** RSUs — liquid (NYSE: ESTC). $258M annual stock-based compensation spend.
- **Bonus:** Performance-based; amount not publicly confirmed for Germany.
- **Benefits:** Home office stipend, health insurance, flexible PTO, L&D budget.

##### ✅ PROS
- Truly remote-first — distributed by design, no RTO pressure
- AWS-native stack; Kubernetes and Java used across engineering
- Liquid RSUs on a public exchange
- Principal-level salary confirmed above €120K base in Germany
- 40+ countries of employees — English-first by default

##### ❌ CONS
- CEO approval among ICs on Glassdoor is only 37% — disconnect between engineers and leadership
- Frequent restructures and shifting reporting lines flagged in 2025–2026 reviews
- Career growth at senior IC levels described as slow
- ESTC stock price volatile — RSU value fluctuates meaningfully

##### 🎯 CANDIDATE FIT
| Criteria | Status | Notes |
|----------|--------|-------|
| Tech Stack (AWS, Java/Kotlin, K8s) | ✅ | AWS primary cloud, Java widely used, K8s-native |
| Target Role Available | ✅ | Principal SWE and SRE roles open in Germany/Europe |
| Work Model (Remote/Hybrid-Munich) | ✅ | Fully distributed — Munich is first-class |
| Salary €120K+ Base | ✅ | Confirmed €115K–€158K base for Principal in Germany |
| Equity Available | ✅ | Liquid RSUs (NYSE: ESTC) |
| English Working Environment | ✅ | English-only, 40+ countries |
| Engineering/IC Culture | ✅ | Explicit IC ladder, Staff/Principal levels, SRE-native |

##### 🏁 OVERALL VERDICT
**Decision:** 🟢 APPLY

**Rationale:** Strongest all-round fit. Remote-first globally means Munich requires zero compromise. Principal-level salary confirmed above €120K in Germany, RSUs are liquid, and the engineering stack is a direct match. The only friction is internal restructuring instability and lower IC approval of leadership — manageable for a candidate at this seniority.

---

#### 🏢 DYNATRACE — 79% fit
**Industry:** Observability & AIOps SaaS | **Size:** ~4,700 | **HQ:** Linz, Austria (major Munich R&D hub) | **Work Model:** Hybrid / Flex Remote

##### ⚡ QUICK OVERVIEW
| Criteria | Value | Source |
|----------|-------|--------|
| Glassdoor Score | 3.9 / 5 | Glassdoor (1,470+ reviews) |
| Kununu Score | #1 IT employer Austria (Statista/Kununu) | Kununu/Statista |
| CEO Approval | 87/100 (Top 5% of peers) | Comparably |
| Would Recommend | 72% | Glassdoor |
| Salary Competitiveness | ⭐⭐⭐⭐ | Levels.fyi |

##### 💰 SALARY & PACKAGE
- **Target Role Base Salary:** P5/P6 in Munich estimated €110K–€140K base. Negotiate explicitly to clear €120K.
- **Equity/Stock:** RSUs + ESPP (NYSE: DT). $538.9M unrecognized RSU compensation as of Sept 2025.
- **Bonus:** Annual short-term incentive (STI) tied to company performance.
- **Benefits:** Public transport reimbursement, corporate health insurance, pension, €1,500 learning budget, language classes, bike parking on Munich campus.

##### ✅ PROS
- Munich R&D hub — hybrid from Munich with no relocation needed
- Kotlin actively used in engineering (dedicated internal Kotlin community)
- NYSE: DT liquid RSUs + ESPP
- Direct stack overlap: AWS, Kubernetes, Java/Kotlin, observability
- Ranked Europe's Best Employer (FT 2025), #1 IT employer Austria
- CEO rated Top 5% of peers on Comparably

##### ❌ CONS
- Glassdoor rating declined 5% in the last 12 months
- IC career growth consistently criticized — limited upward mobility, hierarchical structure
- Fully remote only for "specific roles" — most engineering is hybrid minimum 2 days/week
- Salary may require strong negotiation to clear €120K base at Principal level

##### 🎯 CANDIDATE FIT
| Criteria | Status | Notes |
|----------|--------|-------|
| Tech Stack (AWS, Java/Kotlin, K8s) | ✅ | AWS, Kubernetes, Kotlin — near-perfect match |
| Target Role Available | ✅ | Senior SWE (SRE background), Principal Solution Architect open |
| Work Model (Remote/Hybrid-Munich) | ✅ | Munich engineering hub — hybrid 2d/week manageable |
| Salary €120K+ Base | ✅ | Likely at P5/P6 — negotiate explicitly |
| Equity Available | ✅ | Liquid RSUs + ESPP (NYSE: DT) |
| English Working Environment | ✅ | International engineering org, English-first |
| Engineering/IC Culture | ⚠️ | IC ladder exists but career growth criticism persistent |

##### 🏁 OVERALL VERDICT
**Decision:** 🟢 APPLY

**Rationale:** Best Munich-specific fit in the entire list. Engineering hub is in Munich, stack is near-perfect (AWS, Kubernetes, Kotlin), liquid RSUs on NYSE: DT, and SRE-background roles actively posted. Salary needs explicit negotiation to clear €120K base. IC career growth concerns are real but manageable for someone entering at Principal level.

---

#### 🏢 HASHICORP (IBM) — 64% fit
**Industry:** Infrastructure Software / DevOps | **Size:** ~2,500 (brand); IBM subsidiary | **Work Model:** Hybrid/Remote — IBM-policy dependent

##### ⚡ QUICK OVERVIEW
| Criteria | Value | Source |
|----------|-------|--------|
| Glassdoor Score | 4.0 / 5 | Glassdoor (472 reviews) |
| Kununu Score | data not found | Kununu |
| CEO Approval | data not found post-IBM | Glassdoor |
| Would Recommend | 67% | Glassdoor |
| Salary Competitiveness | ⭐⭐⭐⭐⭐ | Levels.fyi Germany: €153K–€231K total comp |

##### 💰 SALARY & PACKAGE
- **Target Role Base Salary:** Germany total comp confirmed €153K–€231K (median €178K) — highest in this comparison.
- **Equity/Stock:** HashiCorp options canceled in IBM acquisition (Feb 2025). Now IBM RSUs (NYSE: IBM) — liquid but low-growth.
- **Bonus:** IBM standard performance bonus.
- **Benefits:** IBM full suite — health, dental, pension, PTO.

##### ✅ PROS
- Highest confirmed Germany salary ceiling in the comparison (€178K median total comp)
- Tech stack is a direct match: Terraform, Vault, Consul, Kubernetes, AWS — SRE core tooling
- WLB rated 4.2/5 — among highest in this comparison
- Staff SWE roles actively posted

##### ❌ CONS
- IBM acquisition (Feb 2025) killed IC culture — bureaucracy and management bloat visible in 2025–2026 reviews
- Original equity story gone — IBM RSUs offer no high-growth upside
- 49% positive business outlook — morale dampened post-acquisition
- Remote flexibility reduced under IBM's hybrid preference

##### 🎯 CANDIDATE FIT
| Criteria | Status | Notes |
|----------|--------|-------|
| Tech Stack (AWS, Java/Kotlin, K8s) | ✅ | Terraform, Vault, Kubernetes, AWS — exact SRE/DevOps match |
| Target Role Available | ✅ | Staff SWE - HashiCorp Secure (Vault, Radar, Boundary) open |
| Work Model (Remote/Hybrid-Munich) | ⚠️ | IBM hybrid preference; Munich not a primary site |
| Salary €120K+ Base | ✅ | Confirmed well above €120K base in Germany |
| Equity Available | ❌ | HashiCorp options canceled; IBM RSUs are liquid but low-growth |
| English Working Environment | ✅ | US-origin, English globally |
| Engineering/IC Culture | ⚠️ | Post-IBM acquisition: bureaucracy and morale decline documented |

##### 🏁 OVERALL VERDICT
**Decision:** 🟡 INVESTIGATE

**Rationale:** Highest salary ceiling in the comparison and a perfect DevOps stack match — use it as a compensation anchor in negotiations. But the IBM acquisition killed both the equity upside and the IC culture. Apply to understand what autonomy the brand retains under IBM, but don't make it a primary target.

---

## Search Tools & Configuration

The skill uses two layers of web search: Claude Code's built-in tools (free) and the Tavily MCP server (paid, more powerful).

### Tool Overview

| Tool | Provider | Cost | Best For |
|------|----------|------|----------|
| `WebSearch` | Claude Code (Anthropic) | Free | Quick lookups, news, Glassdoor links |
| `WebFetch` | Claude Code (Anthropic) | Free | Reading a specific URL (job posting, salary page) |
| `tavily_search` | Tavily MCP | 1–2 credits | Targeted web search with domain/date filtering |
| `tavily_research` | Tavily MCP | 4–250 credits | Deep multi-step research with AI synthesis |
| `tavily_extract` | Tavily MCP | 1–2 credits per 5 URLs | Extracting full content from specific pages |
| `tavily_crawl` | Tavily MCP | Map + extract cost | Indexing entire sites (e.g. careers pages) |

### Tavily Pricing

| Plan | Monthly Cost | Credits/Month | Notes |
|------|-------------|---------------|-------|
| **Researcher (Free)** | $0 | 1,000 | No credit card required |
| **Project** | $30 | 4,000 | |
| **Bootstrap** | $100 | 15,000 | |
| **Startup** | $220 | 38,000 | |
| **Growth** | $500 | 100,000 | |
| **Pay-as-you-go** | — | Variable | $0.008/credit |

**Credit cost by tool:**

| Tool | Search depth | Credits |
|------|-------------|---------|
| `tavily_search` | basic | 1 credit |
| `tavily_search` | advanced | 2 credits |
| `tavily_extract` | basic | 1 credit per 5 URLs |
| `tavily_extract` | advanced | 2 credits per 5 URLs |
| `tavily_research` | mini model | 4–110 credits |
| `tavily_research` | pro model | 15–250 credits |
| `tavily_map` | — | 1 credit per 10 pages |

> For typical job evaluation runs (6–8 searches per company), expect ~10–20 credits per company with `tavily_search` at basic depth.

### Setup

#### 1. Get a Tavily API key

Sign up at [app.tavily.com](https://app.tavily.com) — free tier (1,000 credits/month) requires no credit card.

#### 2. Configure the Tavily MCP server in Claude Code

Add to `~/.claude.json` under `mcpServers`:

```json
{
  "mcpServers": {
    "tavily-mcp": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "tavily-mcp"],
      "env": {
        "TAVILY_API_KEY": "tvly-YOUR_API_KEY_HERE"
      }
    }
  }
}
```

#### 3. Allow the tools in your project settings

Add to `.claude/settings.local.json`:

```json
{
  "permissions": {
    "allow": [
      "WebSearch",
      "WebFetch(domain:www.glassdoor.com)",
      "mcp__tavily-mcp__tavily_search",
      "mcp__tavily-mcp__tavily_research"
    ]
  }
}
```

Restrict `WebFetch` to specific domains (e.g. Glassdoor, Greenhouse, Levels.fyi) to avoid unintended fetches. Add domains as needed.

#### 4. Verify the MCP server is running

```bash
claude mcp list
```

You should see `tavily-mcp` listed as connected.

---

## License

MIT
