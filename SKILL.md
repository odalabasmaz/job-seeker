---
name: job-evaluator
description: Generates a comprehensive job evaluation report based on a company name or website, tailored to Orhun Dalabasmaz's career profile and expectations. Scans Glassdoor, Kununu, Levels.fyi, LinkedIn, and Remotely.de. Use this skill when the user provides one or more company names or URLs, conducts job research, or uses phrases like "evaluate this company", "should I apply here", "what's the salary range", or "what do employees say".
---

# Job Evaluator Skill

This skill is used to quickly evaluate companies during Orhun Dalabasmaz's job search process.

## Candidate Profile (Fixed — use in every report)

- **Name:** Orhun Dalabasmaz
- **Experience:** 15+ years
- **Current Role:** Principal Engineer @ Atlassian, Munich
- **Target Roles:** Principal Engineer, Staff Engineer, SRE, Engineering Manager, Solutions Architect, Team Lead
- **Priority:** Compensation and job content over role type
- **Tech Stack:** Java/Kotlin, Python, Spring, AWS (Neptune, EKS, DynamoDB, SQS, Lambda, KMS, S3, CloudFormation), Docker, Kubernetes, Microservices, Kafka, Grafana, Splunk, Datadog, Neo4j, Gremlin/Cypher, CI/CD (Bitbucket/Jenkins), MCP, Claude/Gemini AI integrations
- **Expertise:** SRE, DevOps, Cloud Architecture (AWS-focused), Distributed Systems, People Management, Technical Leadership, Roadmap Planning, Cross-functional Collaboration, FedRAMP/SOC2/GDPR Compliance
- **Cloud Preference:** AWS (multi-cloud acceptable)
- **Work Model:** Remote (anywhere) OR Hybrid/On-site (Munich only)
- **Employment:** Full-time
- **Salary:** Minimum €120,000 base + equity preferred
- **On-call:** Acceptable
- **Travel:** Low amount acceptable (conferences, office visits)
- **People Management:** Flexible (IC or EM)
- **Industry:** SaaS/Cloud preferred, open to others
- **Language:** English working environment required (German not mandatory)

---

## Research Steps

When the user provides a company name or URL, search the following sources via web_search:

1. **Glassdoor:** `[company name] Glassdoor reviews` → Overall score, CEO approval, recommendation rate, pros/cons
2. **Kununu:** `[company name] Kununu Bewertungen` → German market employee reviews
3. **Levels.fyi:** `[company name] levels.fyi engineer salary Germany` → Salary data
4. **LinkedIn:** `[company name] Principal Engineer SRE jobs Munich` → Open positions
5. **Remotely.de:** `[company name] remotely.de` → Remote job listings
6. **General:** `[company name] employee benefits Germany equity RSU` → Perks and benefits

If data is unavailable, write "data not found" — **never estimate**.

---

## Report Format

Generate the following report for each company:

---

### 🏢 [COMPANY NAME]
**Industry:** | **Size:** | **HQ:** | **Work Model:**

#### ⚡ QUICK OVERVIEW
| Criteria | Value | Source |
|----------|-------|--------|
| Glassdoor Score | X.X / 5 | Glassdoor |
| Kununu Score | X.X / 5 | Kununu |
| CEO Approval | XX% | Glassdoor |
| Would Recommend | XX% | Glassdoor/Kununu |
| Salary Competitiveness | ⭐⭐⭐⭐⭐ | Levels.fyi/Glassdoor |

#### 💰 SALARY & PACKAGE
- **Target Role Base Salary:** (cite source)
- **Equity/Stock:** RSU / ESOP / Stock options available?
- **Bonus:** Structure?
- **Benefits:** Health, pension, learning budget, equipment, etc.

#### ✅ PROS
(From employee reviews — most frequently mentioned)
- ...

#### ❌ CONS
(From employee reviews — most frequently mentioned)
- ...

#### 🎯 CANDIDATE FIT
| Criteria | Status | Notes |
|----------|--------|-------|
| Tech Stack (AWS, Java/Kotlin, K8s) | ✅/⚠️/❌ | |
| Target Role Available | ✅/⚠️/❌ | |
| Work Model (Remote/Hybrid-Munich) | ✅/⚠️/❌ | |
| Salary 120k+ Base | ✅/⚠️/❌ | |
| Equity Available | ✅/⚠️/❌ | |
| English Working Environment | ✅/⚠️/❌ | |
| Engineering/IC Culture | ✅/⚠️/❌ | |

#### 🔗 SOURCES & OPEN POSITIONS
- 🔍 Glassdoor: [link]
- 🔍 Kununu: [link]
- 💰 Levels.fyi: [link]
- 💼 LinkedIn Listings: [found positions]
- 🌐 Remotely.de: [found positions]

#### 🏁 OVERALL VERDICT
**Decision:** 🟢 APPLY | 🟡 INVESTIGATE | 🔴 SKIP

**Rationale:** (2–3 sentence summary — why this decision?)

---

## Multiple Companies

If the user provides more than one company, append a comparison table at the end:

### 📊 COMPARISON TABLE
| Company | Glassdoor | Salary Fit | Stack Fit | Model Fit | Decision |
|---------|-----------|------------|-----------|-----------|----------|
| ... | | | | | 🟢/🟡/🔴 |

---

## Important Notes

- Reports are written in **English**
- Write "data not found" for missing data — never estimate
- Use €120k base as the salary threshold for comparison
- Equity matters: flag with ⚠️ if RSU/ESOP is absent
- Remote: any city accepted; hybrid/on-site: Munich only
