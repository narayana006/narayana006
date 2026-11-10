# Narayana Vemburaj

Engineering at Equifax.

I build open-source tools for site reliability engineering and for teams shipping software with large language models. Each project below is MIT licensed. Most are at an early stage, and every README states exactly what works today.

## SRE and reliability

| Project | What it does |
|---|---|
| [ai-postmortem](https://github.com/narayana006/ai-postmortem) | Generate blameless postmortem drafts from incident Slack channels, PagerDuty/Opsgenie timelines and deploy logs. |
| [incident-review-copilot](https://github.com/narayana006/incident-review-copilot) | Score and review postmortems: flags missing timings, blame language, vague or unowned action items. |
| [incident-pattern-miner](https://github.com/narayana006/incident-pattern-miner) | Cluster past incidents by theme to find repeat failure modes and produce quarterly reliability reports. |
| [runbook-agent](https://github.com/narayana006/runbook-agent) | Turn Markdown runbooks into agent-executable steps: read-only diagnostics run automatically, changes require human approval. Ships as an MCP server. |
| [alert-noise-auditor](https://github.com/narayana006/alert-noise-auditor) | Analyze alert history to find flapping, never-actioned and duplicate alerts, and suggest threshold changes or deletions. |
| [slo-suggest](https://github.com/narayana006/slo-suggest) | Propose SLIs and SLOs from your existing access logs and Prometheus or Datadog metrics, and generate OpenSLO YAML plus burn-rate alerts. |
| [oncall-handoff](https://github.com/narayana006/oncall-handoff) | Summarize an on-call shift from pages, Slack and tickets into a clear handoff note. |
| [change-risk-scorer](https://github.com/narayana006/change-risk-scorer) | Score the risk of a PR or deploy by blast radius, config changes, timing and recent incidents, and post it as a PR comment. |
| [k8s-explain](https://github.com/narayana006/k8s-explain) | Pipe kubectl output in, get a plain-English diagnosis, likely fix and verification commands out. |
| [statuswall](https://github.com/narayana006/statuswall) | One dashboard for all vendor status pages (AWS, Google Cloud, Azure, GitHub, Cloudflare, ...) with historical uptime from public data. |
| [terraform-plan-explainer](https://github.com/narayana006/terraform-plan-explainer) | Turn a Terraform plan into a plain-English summary that calls out destructive and high-risk changes before you apply. |
| [log-triage](https://github.com/narayana006/log-triage) | Collapse noisy logs into patterns, surface what is new or spiking, and summarise the likely cause. |
| [capacity-forecast](https://github.com/narayana006/capacity-forecast) | Forecast when services will run out of CPU, memory, disk or quota from existing Prometheus metrics. |
| [cert-expiry-watch](https://github.com/narayana006/cert-expiry-watch) | Find TLS certificates that are about to expire across domains, Kubernetes secrets and cloud load balancers. |
| [deploy-diff-summary](https://github.com/narayana006/deploy-diff-summary) | Explain what actually changed between two releases: commits, config, container images and infrastructure, in plain English. |
| [incident-comms-drafter](https://github.com/narayana006/incident-comms-drafter) | Draft status page updates and stakeholder messages during an incident from the live incident channel. |
| [toil-tracker](https://github.com/narayana006/toil-tracker) | Measure operational toil from tickets and pages and rank the best candidates for automation. |
| [cloud-cost-anomaly](https://github.com/narayana006/cloud-cost-anomaly) | Detect unusual cloud spend from billing exports and explain which service, account or tag caused it. |
| [error-budget-report](https://github.com/narayana006/error-budget-report) | Generate a weekly error budget report from your SLO definitions and metrics, with what consumed the budget. |
| [gameday-planner](https://github.com/narayana006/gameday-planner) | Propose failure-injection experiments for game days from your architecture and past incidents. |
| [gcp-stockout-guard](https://github.com/narayana006/gcp-stockout-guard) | Spot Google Cloud capacity stockouts early and automate Compute Engine reservations, using the Compute Engine advice APIs and stockout error logs. |
| [ai-incident-management-companion](https://github.com/narayana006/ai-incident-management-companion) | Companion code for the book AI-Driven Incident Management: fixtures, calculations, figures and labs. |

## AI engineering

| Project | What it does |
|---|---|
| [prompt-regress](https://github.com/narayana006/prompt-regress) | Regression tests for LLM prompts: YAML cases, LLM-judge + deterministic asserts, diff reports in CI. |
| [mcp-starter-kit](https://github.com/narayana006/mcp-starter-kit) | Production-ready templates for building Model Context Protocol (MCP) servers in TypeScript and Python. |
| [llm-cost-guard](https://github.com/narayana006/llm-cost-guard) | Per-user and per-feature token budgets, spend tracking and alerts for LLM-powered apps. |
| [repo-to-context](https://github.com/narayana006/repo-to-context) | Pack a code repository into LLM-ready context: gitignore-aware, token-budgeted, importance-ranked. |
| [agent-skills-collection](https://github.com/narayana006/agent-skills-collection) | A curated collection of reusable agent skills (SKILL.md) for release notes, migrations, security reviews, SEO and App Store audits. |
| [rag-eval-lite](https://github.com/narayana006/rag-eval-lite) | Measure RAG quality on your own documents: synthetic QA generation, retrieval recall and answer faithfulness, HTML report. |
| [doc-ingest](https://github.com/narayana006/doc-ingest) | One pipeline from PDF, HTML and DOCX to clean, metadata-rich chunks for any vector store. |
| [pii-scrub](https://github.com/narayana006/pii-scrub) | Redact PII and secrets before text reaches an LLM, then restore them in the response. |
| [agent-patterns](https://github.com/narayana006/agent-patterns) | Small, runnable reference implementations of common AI agent patterns, each under 200 lines. |
| [structured-extract](https://github.com/narayana006/structured-extract) | Schema in, validated JSON out: extract structured data from messy text with retries, repair and per-field confidence. |
| [ai-alert-explainer](https://github.com/narayana006/ai-alert-explainer) | Explain any alert or signal in plain English: rule-based checks plus an LLM verdict with reasoning and confidence. |
| [expo-ai-starter](https://github.com/narayana006/expo-ai-starter) | Expo / React Native starter with streaming AI chat, voice input, secure backend proxy and App Store-ready defaults. |
| [llm-observe](https://github.com/narayana006/llm-observe) | Self-hosted, minimal LLM tracing: one-line SDK wrapper, SQLite storage and a local web UI for prompts, latency, cost and errors. |
| [ai-pr-reviewer-action](https://github.com/narayana006/ai-pr-reviewer-action) | GitHub Action for AI pull request review driven by plain-English rules in .ai-review.md, commenting only on high-confidence findings. |

## Get in touch

Open an issue on any project with feedback, a use case or a feature idea.
