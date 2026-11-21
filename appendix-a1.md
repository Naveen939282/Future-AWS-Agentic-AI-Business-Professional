# Appendix A -- Templates (copy/paste)

## A1) Data Source Inventory Template

| Source | Type (structured/unstructured) | Owner | Freshness need | Key fields/docs | Access method | Connector type | Auth method | Risks |
| ------ | ------------------------------ | ----- | -------------- | --------------- | ------------- | -------------- | ----------- | ----- |
| | | | | | | | | |

## A2) Connector Selection Cheat Sheet

- **Business question(s) supported:**
- **Source-of-truth system:**
- **Data type** (structured/unstructured/both):
- **Connector category** (SaaS/database/file storage/web):
- **Authentication method** (OAuth/API key/username-password/IAM):
- **Storage mode** (SPICE import/Direct Query/Quick Index only):
- **Scope chosen** (what's included/excluded):
- **Refresh frequency:**
- **Owner + runbook link:**
- **Cost estimate** (SPICE storage, connector fees):

## A3) Refresh Runbook (one page)

- **Connector name:**
- **Owner:**
- **Expected update cadence:**
- **How to verify freshness:** (check last sync timestamp in Integrations; verify latest date in data)
- **Common failure causes:** (credential expiry, schema change, source downtime, rate limiting)
- **Step-by-step recovery:**
  1. Check sync error message in Integrations
  2. Verify credentials are still valid
  3. Check source system status
  4. Re-authenticate if needed
  5. Run manual sync
  6. Verify data after sync completes
  7. Escalate to admin if unresolved

## A4) Dashboard Design Brief

- **Dashboard name:**
- **Audience:** (who reads it)
- **Decision supported:** (what they'll decide)
- **Cadence:** (daily/weekly/monthly)
- **KPIs (3-5):** (list with definitions)
- **Segments needed:** (dimensions to break down by)
- **Drill-down path:** (what follow-up questions should be answerable)
- **Definitions and assumptions:** (how metrics are calculated, what's included/excluded)
- **Data source(s):** (which Quick Index connectors or Quick Sight datasets)
- **Freshness requirement:** (how current must the data be)
- **Layout plan:** (which sheets, what goes on each)

## A5) Insight Statement Template

- **Observation** (quantified): What happened? Include a number.
- **Meaning** (why it matters): What's the business impact?
- **Action** (what to do next): Specific action, owner, deadline.
- **Confidence level** (high/medium/low) + why:
- **How verified:** (cross-checked with dashboard, Q, source system)

## A6) Space Plan

- **Space name:**
- **Purpose statement:** (one sentence)
- **Primary audience:** (which team/role)
- **Permission roles:**
  - Owners: [names/roles]  -- why
  - Viewers: [names/roles]  -- why
- **Content structure:**
  - Folder 1: [name]  -- contents
  - Folder 2: [name]  -- contents
  - Folder 3: [name]  -- contents
- **"Start Here" content:** (what the onboarding document covers)
- **Maintenance workflow:** (who updates what, how often)

## A7) Q Exploration Log Template

| # | Question asked | Expected answer | Q's answer | Verified? | Match? | Notes |
|---|---------------|----------------|-----------|:---------:|:------:|-------|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |

## A8) Permission Test Checklist

| Action | Viewer expected | Viewer actual | Owner expected | Owner actual |
|--------|:-:|:-:|:-:|:-:|
| View dashboard | âœ… | | âœ… | |
| Download files | âœ… | | âœ… | |
| Upload files | âŒ | | âœ… | |
| Add/remove knowledge | âŒ | | âœ… | |
| Reorganize content | âŒ | | âœ… | |
| Share Space | âŒ | | âœ… | |
| Delete Space | âŒ | | âœ… | |
| Chat with Space data | âœ… | | âœ… | |

## A9) Data Preparation Plan Template

- **Source file/table:**
- **Target dataset name:**
- **Type fixes needed:** (list fields that need type changes)
- **Fields to rename:** (old name â†’ new name, with description)
- **Calculated fields to create:** (name, formula, description)
- **Joins needed:** (which tables, on what key, join type)
- **Rows to filter out:** (criteria)
- **Columns to exclude:** (list)
- **Dimension/measure corrections:** (fields to reclassify)
- **Storage mode:** (SPICE import / Direct Query)

## A10) Topic Configuration Template

- **Topic name:**
- **Dataset(s):**
- **Fields included:** (with semantic type, synonyms, and format for each)
- **Named filters:** (filter name â†’ field â†’ value)
- **Before/after test results:** (3 questions, answers before and after)

## A11) Custom Agent Configuration Template

- **Agent name:**
- **Description:**
- **Instructions:** (3â€“5 sentences defining behavior)
- **Knowledge sources:** (Spaces, Topics, knowledge bases)
- **Actions:** (action connectors, if any)
- **Guardrails:** (what the agent should refuse to do)
- **Test log:** (3 questions â†’ system agent answer â†’ custom agent answer â†’ comparison)

---

# Appendix B  -- Mini portfolio project (optional)

If your program requires a portfolio artifact, complete this mini-project:

## Project: "BrightMart Marketing Insights Workspace"

Create a Space that a real marketing team could adopt.

### Requirements

1. **1 integrated data source** (Quick Index connector) + verification log showing 3+ verification questions and answers
2. **1 interactive dashboard** (2â€“3 sheets) with filters, drill-down, cross-visual interaction, and a clear design brief  -- built on a **prepared dataset** using QuickSight Datasets (with renamed fields, calculated fields, and correct data types)
3. **1 Q exploration log** (5â€“10 verified Q&A entries with dashboard cross-checks), using a **configured Topic** with semantic types and synonyms
4. **1 executive summary** with 3 insights (using Observation + Meaning + Action template) and 3 recommended actions with owners
5. **A Space** that contains all of the above, organized with a clear structure, "Start Here" documentation, and appropriate permissions

### Evaluation criteria

| Criterion | What to demonstrate |
|-----------|-------------------|
| **Data integration** | Connector syncs successfully; data is verified and complete |
| **Data preparation** | Dataset has clean types, descriptive names, calculated fields, and field descriptions |
| **Dashboard design** | Design brief is complete; charts match decisions; interactivity works |
| **Topic configuration** | Topic improves Q accuracy; before/after comparison documented |
| **Analysis quality** | Q findings are verified; insights follow the template; actions are specific |
| **Communication** | Executive summary is clear to a non-technical reader; dashboard has context |
| **Collaboration** | Space is organized; permissions are configured; a new member could self-onboard |

### Submission checklist

- [ ] Space link (or screenshots of Space contents and structure)
- [ ] Dashboard link (or screenshots of all sheets with filters applied)
- [ ] PDFs of:
  - [ ] Executive summary with insights and actions
  - [ ] Q exploration log
  - [ ] Knowledge base verification log
  - [ ] Dashboard design brief
  - [ ] Data preparation plan
  - [ ] Topic before/after comparison
  - [ ] Permission test checklist
  - [ ] Custom agent test log (bonus)

---

# Appendix C  -- Quick reference tables

## Quick Sight visual types and when to use them

| Visual type | Best for | Field wells needed |
|------------|---------|-------------------|
| Bar chart (vertical/horizontal) | Comparing categories | X/Y axis + Value |
| Stacked bar | Part-to-whole comparison | X/Y axis + Value + Group/Color |
| Line chart | Trends over time | X axis (date) + Value |
| Combo chart | Two related measures on different scales | X axis + Bars + Lines |
| KPI | Single metric status | Value + (optional) Target value |
| Pie chart | Simple composition (â‰¤5 slices) | Value + Group/Color |
| Scatter plot | Relationship between two measures | X axis + Y axis + (optional) Group/Color |
| Table | Detailed records, lookup | Multiple fields |
| Pivot table | Cross-tabulation, summaries | Rows + Columns + Values |
| Histogram | Distribution shape | Value |
| Box plot | Distribution with outliers | Group + Value |
| Tree map | Hierarchical part-to-whole | Group by + Size + (optional) Color |
| Heat map | Patterns across two dimensions | Rows + Columns + Values |
| Geospatial map | Location-based data | Geospatial + (optional) Size/Color |

## SPICE capacity planning

| Data type | Size per cell |
|-----------|-------------|
| Decimal | 8 bytes + 4 bytes auxiliary |
| Date | 8 bytes + 4 bytes auxiliary |
| String | Length in UTF-8 encoding + 24 bytes auxiliary |

Estimate your dataset size: `(decimal_cells Ã— 12) + (date_cells Ã— 12) + (string_cells Ã— (avg_string_length + 24))` = approximate bytes. Divide by 1,073,741,824 for GB.

---

# Appendix D  -- Knowledge check answers

> **How to use:** Try to answer each knowledge check question before looking here. Self-assessment is most effective when you attempt the answer first.

## Module 2.1.0

1. **Dashboard vs. Space:** A dashboard is a published set of visuals for specific metrics; a Space is a team hub that can contain dashboards, files, knowledge bases, and more.
2. **Region:** SPICE capacity, datasets, and analyses are regional. Using the wrong region means you won't see your work or may lack capacity.
3. **System chat agent:** The default AI assistant created automatically when you sign up, with access to all resources based on your permissions.

## Module 2.1.1

1. **Structured:** A CSV of campaign spend by channel and date. **Unstructured:** A brand guidelines PDF or a competitive analysis slide deck.
2. **KPI arguments:** Different teams may pull from different source systems, use different definitions of the same metric, or look at different time ranges. Without a shared source of truth and agreed definitions, dashboards can show conflicting numbers.
3. **Quick Index role:** Quick Index connects to 50+ data sources and creates a unified, searchable, permission-aware knowledge layer. All teams can access the same data through a single platform rather than pulling from separate systems.

## Module 2.1.1  -- Practice reference answer

| Source System | Data Type | Update Frequency | Primary Users | Risk if Wrong | Connector Type |
|--------------|-----------|-----------------|---------------|--------------|----------------|
| Google Ads | Structured (spend, clicks, impressions) | Daily | Marketing team | Medium  -- budget waste | SaaS connector |
| Google Analytics | Structured (sessions, conversions, bounce rate) | Daily/hourly | Marketing, Product | Medium  -- bad optimization | SaaS connector |
| Salesforce CRM | Structured (leads, opportunities, revenue) | Real-time | Sales, Finance | High  -- wrong forecasts | SaaS connector (OAuth) |
| Zendesk | Semi-structured (tickets, ratings, text) | Real-time | Support, Product | Medium  -- missed patterns | SaaS connector |
| Google Drive | Unstructured (docs, slides, sheets) | As edited | All teams | Low  -- stale strategy docs | File storage connector |
| PostgreSQL DB | Structured (financial records) | Monthly | Finance, Exec | High  -- regulatory risk | Database connector |
| SharePoint | Unstructured (policies, handbook) | As edited | HR, All teams | Low  -- outdated policies | File storage connector |

## Module 2.1.9

1. **Dataset-level vs. analysis-level calculated fields:** Dataset-level fields are available to all analyses using that dataset and row-level fields are materialized in SPICE. Analysis-level fields are available only in that analysis and are computed at render time, allowing aggregation that adapts to drill-downs.
2. **Renaming/describing fields:** Cryptic names like `conv_rt` confuse both human users and AI. Descriptive names and descriptions make datasets self-explanatory and improve Quick Chat/Q accuracy.
3. **Append vs. Join:** Append stacks rows from tables with compatible schemas (e.g., combining monthly CSVs). Join combines columns from different tables linked by a shared key (e.g., enriching campaign data with channel names).

## Module 2.1.10

1. **ifelse() for division:** Without it, rows with zero in the denominator produce errors or null values that break visuals and skew aggregations.
2. **Skipping field renaming:** Every downstream user and AI system inherits the cryptic names. Dashboards have unreadable axis labels, Q misinterprets fields, and new team members can't understand the data.
3. **Field descriptions and Quick Chat:** Descriptions help Quick Chat/Q understand what data represents. When Q encounters "Spend," the description "Total ad spend in USD" confirms it should treat this as a currency measure, not a generic number.

## Module 2.1.16

1. **Synonym vs. named filter:** A synonym is an alternate name for a field (e.g., "cost" for "Spend"). A named filter maps a business term to a specific data filter (e.g., "email" â†’ Channel = "Email"). Synonyms help Q find the right field; named filters help Q apply the right row-level constraint.
2. **Wrong answers after Topic configuration:** The question phrasing might not match configured synonyms, the data might not contain the answer, the metric definition in the question might differ from how the calculated field works, or Q might still draw from general knowledge if not properly scoped.
3. **Semantic types:** They tell Q how to format and interpret values. "Currency in USD" means Q displays "$1,234" instead of "1234," and understands this is a monetary value for aggregation and comparison.

## Module 2.1.24

1. **Custom vs. system agent:** Use a custom agent when you have a specific domain with preferred data sources, consistent instructions, and guardrails  -- e.g., a team-specific analyst that always draws from one Space and follows your insight framework.
2. **Guardrails:** Without them, a domain agent might attempt to answer questions outside its expertise, giving confident but unreliable answers. Guardrails keep the agent focused and honest about its boundaries.
3. **Spaces + Topics together:** The Space provides the documents, dashboards, and knowledge the agent can reference. The Topic provides the structured data definitions (semantic types, synonyms, filters) that help the agent interpret questions accurately. Together, they give the agent both broad context and precise data understanding.

## Module 2.1.25

1. **Quick Research vs. Quick Chat:** Quick Chat answers single questions from available data. Quick Research conducts multi-step investigations across multiple sources (including web), generates a research plan, and produces a cited report. It's the difference between asking one question and commissioning a research project.
2. **Budget awareness:** Quick Research consumes agent hours from a finite monthly allocation. Without budget awareness, a team could exhaust their allocation on low-priority research, leaving nothing for critical investigations.
3. **Effective vs. vague objective:** An effective objective specifies what you want to learn, the context (industry, audience), timeframe, and intended use. "Research marketing trends" is vague. "Analyze e-commerce customer acquisition cost trends for mid-size retailers in Q4 2025, focusing on paid search and social channels, for our Q1 budget planning" is effective.

## Module 2.1.26

1. **Quick Flows vs. Quick Automate:** Quick Flows handles simple, natural-language-defined workflows for individual or team tasks. Quick Automate handles complex, multi-department processes requiring visual workflow design, versioning, and human-in-the-loop approvals.
2. **Action connectors:** They bridge Quick Suite to external systems (Jira, Slack, Salesforce, etc.), enabling automation to take real actions  -- not just generate insights.
3. **Human-in-the-loop:** Enterprise processes often involve decisions that require human judgment, regulatory compliance, or approval authority. Automated workflows without human checkpoints risk executing incorrect or unauthorized actions at scale.

*(Additional module answers follow the same pattern and are omitted for brevity. Refer to V2 for modules 2.1.2â€“2.1.8 and 2.1.11â€“2.1.23 answer keys.)*

---

# Appendix E  -- Frequently asked questions

## Is Quick Suite a Microsoft 365-style productivity suite?

No. A widely circulated Medium article describes Quick Suite as a productivity suite with word processing and email at $8/user/month. **This is misinformation.** Quick Suite is an AI-powered analytics, research, and automation platform  -- not an office productivity suite. It does not include word processing, email, or calendar tools. Pricing starts at $20/user/month (Professional) or $40/user/month (Enterprise), plus a $250/account/month infrastructure fee.

## What happened to Amazon QuickSight?

Amazon QuickSight became the Quick Sight component within Quick Suite. All QuickSight functionality, APIs, SDKs, and compliance certifications carried over. The QuickSight namespace in IAM and CLI remains unchanged.

## What happened to Amazon Q Business?

Amazon Q Business's natural language interface and enterprise data connectivity capabilities were integrated into Quick Suite as Quick Chat and Quick Index, respectively.

## Will the Space permission model expand beyond Viewer/Owner?

The GA launch includes Viewer and Owner roles. AWS may introduce intermediate roles in future releases. The course scope document anticipates this evolution, but the coursebook reflects what is available today.

---


