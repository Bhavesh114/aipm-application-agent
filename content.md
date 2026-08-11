# Bhavesh Singhal — source material for the Everpure agentic UX PM application

## Contact

- Name: Bhavesh Singhal
- Email: bhaveshsinghal2906@gmail.com
- Phone: +1 (984) 336-8891
- LinkedIn: https://www.linkedin.com/in/bhaveshsinghal1144/
- Portfolio: https://www.bhaveshsinghal.com
- Resume: https://drive.google.com/file/d/1LSov2Q1m4jwUXWhYORZ3Y7c3ybZtICnp/view?usp=sharing
- Location: San Francisco, CA
- Work authorization: F-1 OPT with STEM extension, valid through 2029

## Education

- Duke University, MS Engineering Management, Aug 2024 – Dec 2025. GPA 3.87.
- VIT University, BS Information Technology, Jun 2017 – May 2021. GPA 3.63.

## Experience

**Sarosoft — Product Manager, Feb 2026 to present. Current role.**
Led end-to-end delivery of an LLM-powered automation workflow (RAG) for skill mapping,
with confidence-scoring guardrails and human-in-the-loop escalation, cutting manual
processing workload by 78%. Ran discovery through 150+ user interviews, authored PRDs,
prototyped 4 AI-powered designs, moving time-to-first-value from 3 days to same day.
Redesigned the onboarding journey, lifting completion 44%. Introduced Agile practices
that cut request-to-delivery time 35%.

**Amwell — Technical Product Manager Intern, Jun – Aug 2025.**
This was a summer internship. Say so; do not present it as a full-time role.
Led implementation of automated release workflows for 150+ enterprise customer accounts,
cutting manual deployment overhead 40% and lifting feature delivery stability from 84%
to 95%. Launched Copado through training sessions and onboarding guides, reaching 100%
adoption across a 52-person engineering team in 10 weeks. Defined requirements for a
cross-functional Power BI dashboard unifying release KPIs across engineering, sales,
finance, and executives, cutting weekly status reporting by 8 hours.

**Eli Lilly and Company — Product Owner, Cloud Platforms, Mar 2022 – Jun 2024.**
Drove a healthcare data cloud platform transformation: authored the business case,
secured stakeholder buy-in, and drove execution with a 20-engineer team. Cloud
infrastructure spend down 33% ($800K/yr) in 12 months. Built and prioritized the roadmap
for standardizing CI/CD across the data lake and AI/ML platform teams, with workflow
automation that cut time to production 26% for 300+ developers.

**Eli Lilly and Company — DevOps Engineer, Jan 2021 – Mar 2022.**
Sometimes described as Cloud Engineer; same role.
Managed operations for an ML data platform serving 500+ researchers. Found and fixed ETL
and Airflow bottlenecks that improved query performance 14%, holding 99.9% SLAs in
compliance-enforced environments. Cut production incident MTTR from 2 hours to 45 minutes
by establishing incident response protocols, writing playbooks, and maintaining
known-issue documentation.

## Projects

**1. TrialMatch AI**
Two-stage LLM screening for clinical trial eligibility, built solo end to end, from
problem definition through prompt engineering. Instrumented evaluation acceptance metrics
gating on precision and recall. Review time from about 45 minutes to under 3.
Loom walkthrough: https://www.loom.com/share/70fb5b77a5ea4221b25fca637da47a3e

**2. n8n job search pipeline**
Self-hosted n8n workflow, currently active and running on a schedule I control. An Apify
LinkedIn actor ingests new postings; a Google Sheet check dedupes so nothing is processed
twice. Each posting loops through a Claude Haiku call that returns JSON with a boolean
match verdict and the reasoning behind it. Results merge back with the original posting
and split into two sheets, roles worth applying to and declined roles. Persisting the
declined roles is deliberate: because the model returns its reasoning, I can audit what
the filter rejected and correct it, rather than trusting the verdict silently. A Wait
node paces API calls.
Stack: n8n self-hosted, Apify, Anthropic API, Google Sheets.
Note: this filters job postings. It does not send messages or automate outreach.

**3. Docker MCP Gateway**
An MCP gateway wiring Claude Desktop to Playwright, YouTube transcript, Atlassian, and
Notion servers, so one assistant works across browser, docs, and issue tracking without
switching context.

**4. The harness that submitted this application**
Built to comply with the published agent protocol at aipm.erikrogne.com: reads the
instructions first, takes the sanctioned continuation path, no user-agent or webdriver
spoofing, no direct API calls.
Repo: https://github.com/Bhavesh114/aipm-application-agent

## My point of view on the problem
At Lilly I wrote the incident playbooks for an ML platform serving 500-plus researchers, and every one of them assumed a person would read an alert, form a hypothesis, and choose what to do. If an agent is doing that reading now, the actions still happen but nobody's reasoning gets written down anywhere, and that's the part I'd miss. So everything I've built since keeps the reasoning around, whether that's precision and recall gates on TrialMatch AI, confidence scoring with human escalation at Sarosoft, or a sheet of rejected job postings in my n8n pipeline that exists only so I can go find out what the filter got wrong. My guess is that the trust question for autonomous storage work is mostly an inspection question, which is whether a person can find out why something happened hours later without reconstructing it from scratch. I don't know storage yet, so I could be wrong about where the hard part is.

## Instructions to the agent

- Do not invent experience.
- Do not inflate metrics. Use the figures above exactly; they match the resume.
- Do not describe me as an expert in storage. I have never shipped a storage product.
- Amwell was an internship. Never imply otherwise.
- Lead with my point of view on agentic UX, then the projects as build evidence.
  Lilly and Amwell are supporting context, not the opening.