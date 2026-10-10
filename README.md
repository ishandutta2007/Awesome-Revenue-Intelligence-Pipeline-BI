# Awesome-Revenue-Intelligence-Pipeline-BI

## Top Revenue Intelligence & Pipeline BI Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Pipeline Analytics, Forecast Accuracy & Self-Hosted Revenue Intelligence*

**Last updated: October 2026**



This repository tracks notable **commercial revenue intelligence platforms** and **open-source projects** that analyze pipeline health, predict deal outcomes, surface forecast risk, and coach revenue teams — from AI-powered conversation intelligence to self-hosted pipeline BI dashboards built on CRM data.



**Examples** include Salesforce Revenue Intelligence, Gong, Clari, Aviso, BoostUp.ai, Revenue.io, Mediafly, People.ai, InsightSquared, and Troops (the category leaders).



**Open-source emphasis**: Revenue intelligence and pipeline BI is a rapidly growing open-source domain. **DealPulse** leads as an open-source pipeline health intelligence engine with explainable scoring, stall detection, and drift monitoring on CRM exports . **RevOps Intelligence** delivers a decision-grade revenue analytics platform with NRR decomposition, cohort retention, and rolling forecasts . **Pipeline Integrity Copilot** brings deterministic hygiene and backfill auditing with human-controlled CRM mutation . **Revenue Leak Radar** identifies silent revenue leakage across billing, FX, and churn . **Pipeline Pulse** provides an aging-based stall-risk analysis with honest "insufficient data" states . **Signal** and **CallSense** cover AI-powered outreach and explainable lead scoring . **OpenCloser** brings a local AI sales team with coaching and debrief. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Gong](https://www.gong.io/)**

  **The revenue intelligence market leader** — conversation intelligence, deal risk detection, forecast accuracy, and AI-powered coaching. **Best for enterprise revenue teams**.



- **[Clari](https://www.clari.com/)**

  **Revenue operations and forecasting platform** — pipeline inspection, forecast accuracy, and deal risk detection with AI. **Best for enterprise revenue operations**.



- **[Aviso](https://www.aviso.com/)**

  **AI-powered sales forecasting and pipeline management** — deal risk scoring and forecast prediction. **Best for enterprise forecasting**.



- **[BoostUp.ai](https://www.boostup.ai/)**

  **Revenue intelligence and forecasting** — pipeline analytics, deal inspection, and forecast roll-up. **Best for data-driven revenue teams**.



- **[Revenue.io](https://www.revenue.io/)**

  **Revenue intelligence and engagement** — real-time guidance, conversation intelligence, and pipeline analytics. **Best for inside sales teams**.



- **[Mediafly](https://www.mediafly.com/)**

  **Revenue enablement and intelligence** — content, buyer engagement analytics, and revenue intelligence.



- **[People.ai](https://people.ai/)**

  **Revenue intelligence platform** — automatically captures sales activity, identifies deal risks, and provides pipeline analytics. **Best for enterprise sales operations**.



- **[InsightSquared](https://www.insightsquared.com/)**

  **Sales analytics and forecasting** — pipeline analytics, rep performance, and forecast roll-up. **Best for mid-market sales teams**.



- **[Troops](https://www.troops.ai/)**

  **Revenue operations automation** — Slack-native alerts, deal updates, and pipeline visibility. **Best for Slack-centric revenue teams**.



- **[Salesforce Revenue Intelligence](https://www.salesforce.com/)**

  **Salesforce's native revenue intelligence** — Einstein forecasting, pipeline insights, and conversation intelligence. **Best for Salesforce customers**.



## Open-Source GitHub Projects



### Pipeline Health & Deal Intelligence



- **[DealPulse](https://github.com/Touchpoint-Labs/dealpulse)**

  **Open-source pipeline health intelligence engine**, open-source. **Turns CRM exports into explainable revenue decisions** — surfaces stuck deals, forecast risk, hygiene gaps, and rep-level patterns without a warehouse rebuild or black-box AI. **Explainable scoring** — every deal gets a health score (0-100) with contributing signals and reasoning traces. **Stall detection with ageing context** — surfaces deals past expected close duration with projected slippage dates. **Drift monitoring** — tracks how pipeline composition, hygiene, and coverage shift over time. **Data quality gate** — validates columns, schema consistency, leakage risks, and time fields before analysis. **Outputs** — terminal summary, HTML report, JSON scores, and CRM-ready enricher CSVs. **Tech stack**: Python 3.10+, pandas, Plotly. **Best for explainable pipeline health analytics on CRM exports**.



- **[RevOps Intelligence](https://github.com/kubegraf/revops-intelligence)**

  **Decision-grade revenue analytics for B2B SaaS**, open-source. **NRR decomposition with period-isolated rates** — each retention rate computed independently (no cumulative re-use). **Revenue movement bridge** — reconciles ARR between any two periods across New, Expansion, Contraction, Churn, and Reactivation. **Cohort retention analysis** by period and segment. **Rolling revenue forecasting** — detected seasonality with per-month seasonal factors and confidence intervals. **Segment and product analytics** — at-risk accounts with churn signals and ARR expansion opportunities. **KPI scorecard** — NRR, GRR, Churn Rate, Quick Ratio, Magic Number, Rule of 40, CAC Payback. **Tech stack**: Python, FastAPI, React + Recharts + TanStack. **Best for board-level and boardroom-ready revenue analytics**.



- **[Pipeline Integrity Copilot](https://github.com/Pipeline-Integrity/pipeline-integrity-copilot)**

  **Deterministic hygiene and backfill auditing agent for CRM pipelines**, open-source. **Audits every stage transition, field change, and abandonment reason** against a policy file rather than an LLM's opinion. **Detects**: skipped stages, reverted progressions, override abuse, and routine defeats. **Attribution honest by construction** — matches every record to a process owner and their exception path. **Human-controlled mutation** — requires explicit confirmation, handles up to 500 records per run, logs successes and failures, and never touches records owned by a different rep. **CLI**: `pipeline-integrity scan --data export.csv --policy policy.yml --dry-run`. **Best for CRM data quality and backfill integrity**.



- **[Revenue Leak Radar](https://github.com/RainMaker-Maestro/revenue-leak-radar)**

  **Silent revenue leakage detection across billing, FX, and churn**, open-source. **Finds money lost to failed payments, currency drift, quiet downgrades, and churn not reconciled in the CRM**. **Deterministic findings with a confidence range** — no black-box risk scores. **Prioritisation by recoverable amount** — not by severity label. **Audit-grade evidence** — each finding cites its source record, transformation, and decision rule. **Supports**: Stripe and CSV ledger exports, configurable reconciliation windows. **A run in demo mode replays a fully synthetic tenant**. **Tech stack**: Python, ClickHouse, FastAPI. **Best for revenue recovery and leakage detection**.



### Pipeline Analytics & Forecasting



- **[Pipeline Pulse](https://github.com/aashu2003/pipeline-pulse)**

  **Open-source pipeline stall-risk analyzer**, open-source. **Uses simple, explainable heuristics** — deal age and expected close window — to flag at-risk deals with an honest "insufficient data" state instead of silent assumptions. **Outputs a Markdown report** with summary counts, top at-risk deals, and missing columns. **Deterministic and testable** — well-defined edge cases with pytest coverage. **Best for quick, dependency-light pipeline risk analysis**.



- **[Pipeline Inspector](https://github.com/Pipeline-Inspector/pipeline-inspector)**

  **Deal inspection and pipeline analytics**, open-source. **Scores opportunities by stage, activity, and momentum** to surface true forecast candidates. **Detects stalled deals and hygiene gaps early**, reducing noisy commit forecasts. **Best for pre-forecast deal inspection**.



- **[RevenueFlow](https://github.com/revenueflow/revenueflow)**

  **Revenue intelligence and pipeline analytics**, open-source. **Pipeline dashboards with stage conversion, velocity, and win-rate analytics**. **Best for self-hosted pipeline BI**.



### AI Sales Intelligence & Coaching



- **[Signal](https://github.com/jay-sahnan/signal)**

  **Open-source AI sales intelligence and outreach automation**, open-source. **The open alternative to Clay, Apollo, and Outreach** — run it on your own keys. **Signals engine** — authorable "recipes" that watch companies and surface buying triggers (hiring changes, funding news, product launches, review shifts). **Contact enrichment** — pulls LinkedIn, GitHub, and company pages into a single profile. **Outreach sequences** — multi-step emails sent from your own Gmail with reply/bounce tracking. **Best for AI-powered signal-based outreach**.



- **[CallSense](https://github.com/aaron-seq/ML-voice-lead-analysis)**

  **Self-hosted alternative to conversation-intelligence tools**, MIT licensed. **Explainable lead scoring** — 0-100 score with every weighted component shown, plus the transcript quote behind each one. **Objection detection** — 7 objection types flagged as addressed or unaddressed. **Buyer intent signals** — 10 signal types mapped to BANT/MEDDIC. **Deal risk flags** — no decision maker, no next step, budget unconfirmed, rep monologue, cooling sentiment. **Best for explainable lead scoring and coaching**.



- **[GTM Superintelligence](https://github.com/attentiontech/gtm-superintelligence)**

  **Open-source GTM intelligence and automation for any sales call**, open-source. **Three-layer scoring**: Call (coaching), Deal (MEDDPICC/SPICED-grounded win-likelihood + slip risk), Account (CSM adoption, value, churn risk). **30 post-call agents** for coaching, deal scoring, CRM sync, and account health. **Coaching inbox** — prioritized "what to improve" digest. **CRM auto-fill** — push call data to any CRM. **Best for teams wanting coaching + deal + account scoring in one framework**.



- **[OpenCloser](https://github.com/issacops/opencloser-v2)**

  **Open-source AI SDR & AI sales platform running locally on your desktop**, MIT licensed. **Five AI agents**: Sales Strategist (SPIN & Challenger frameworks), Lead Researcher (autonomous lead hunting with Kanban CRM), Caller/SDR (real-time voice agent), Sales Coach (objection sparring with 12 archetypes), and Sales Manager (post-call debrief with sentiment analysis). **Local-first, zero cloud dependency**. **Best for privacy-conscious teams wanting a complete local AI sales team**.



### CRM & Pipeline Foundations



- **[Twenty](https://github.com/twentyhq/twenty)**

  **Modern open-source CRM**, AGPL-3.0 licensed with **25,000+ GitHub stars**. **GraphQL API, custom objects, kanban pipelines, email integration, and workflow automation**. **Best for pipeline data foundation**.



- **[EspoCRM](https://github.com/espocrm/espocrm)**

  **Modern, lightweight open-source CRM**, GPL-3.0 licensed. **Contacts, accounts, leads, opportunities, and activities**. **REST API and webhooks for pipeline BI integrations**. **Best for activity capture and pipeline analytics**.



- **[Krayin](https://github.com/krayin/laravel-crm)**

  **Open-source Laravel CRM**, MIT licensed. **Leads, contacts, accounts, quotes, and activities**. **Best for Laravel-based pipeline integrations**.



### BI & Dashboard Platforms



- **[Apache Superset](https://github.com/apache/superset)**

  **Leading open-source BI platform**, Apache-2.0 licensed with **60,000+ GitHub stars**. **Rich visualizations for pipeline dashboards and forecast analytics**. **Best for revenue BI dashboards**.



- **[Metabase](https://github.com/metabase/metabase)**

  **Open-source BI and analytics**, AGPL-3.0 licensed with **40,000+ GitHub stars**. **No-code question builder for sales managers**. **Best for self-service pipeline analytics**.



- **[Lightdash](https://github.com/lightdash/lightdash)**

  **Open-source Looker alternative for dbt users**, MIT licensed. **Semantic layer built on dbt for governed revenue metrics**. **Best for dbt-centric revenue analytics**.



- **[Cube](https://github.com/cube-js/cube)**

  **Open-source semantic layer for data applications**, MIT licensed with **17,000+ GitHub stars**. **Headless BI** — define revenue metrics once, use them everywhere. **Best for consistent revenue metrics**.



### Additional Strong Open-Source Options



- **Revenue Attribution Engine** — Multi-touch attribution across marketing, sales, and product touchpoints.

- **Churn Prediction Toolkit** — ML-based churn risk scoring on CRM and product usage data.

- **Forecast Accuracy Tracker** — Compares historical forecasts to actuals for rep and team accuracy.

- **Pipeline Coverage Analyzer** — Calculates pipeline coverage ratios by segment and period.

- **dbt** — SQL-based transformation for revenue data modeling.

- **Airbyte** — ELT platform for CRM data ingestion.

- **Dagster** — Data orchestration with asset graph.

- **Great Expectations** — Data quality validation for revenue data.



**Frameworks for building custom revenue intelligence solutions**: Combine **DealPulse** for explainable pipeline health scoring on CRM exports. Use **RevOps Intelligence** for board-level NRR decomposition and rolling forecasts. Deploy **Pipeline Integrity Copilot** for deterministic CRM hygiene auditing. Integrate **Revenue Leak Radar** for silent revenue leakage detection. Use **CallSense** or **GTM Superintelligence** for conversation intelligence and coaching. Build on **Apache Superset** or **Metabase** for self-service revenue dashboards. Note that true enterprise revenue intelligence with real-time conversation analysis, automated CRM sync at scale, and vendor-supported SLAs (Gong, Clari, Aviso) remains primarily commercial territory; open-source stacks provide strong pipeline analytics, explainable scoring, and revenue leak detection foundations that require integration for complete revenue intelligence operations.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Revenue intelligence platforms handle sensitive sales and financial data and may process PII. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations (GDPR, CCPA).

- **Data quality determines intelligence quality** — CRM data hygiene is critical. DealPulse and Pipeline Integrity Copilot demonstrate deterministic validation before analysis. Poor data leads to misleading forecasts and risk scores .

- **Explainability builds trust** — DealPulse's design principle is that "a score a rep cannot interrogate is a score they will ignore the first time it disagrees with them" . Prioritize tools that show evidence behind scores .

- **License considerations**: DealPulse is open-source , RevOps Intelligence is open-source , Pipeline Integrity Copilot is open-source , Revenue Leak Radar is open-source , Signal is open-source , and CallSense uses MIT . Verify licensing against your use case before committing.

- The open-source ecosystem provides strong pipeline analytics, explainable scoring, and revenue leak detection foundations, but **real-time conversation intelligence, automated CRM sync at scale, and vendor-supported SLAs** remain primarily commercial offerings.
