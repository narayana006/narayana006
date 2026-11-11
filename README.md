# Narayana Vemburaj

Engineering at Equifax.

I build open-source tools for site reliability engineering, Apache Kafka operations, AWS, Google Cloud and teams shipping software with large language models. Each project below is MIT licensed. "Working" projects have code, tests and CI; "Planned" projects are a design only, and every README states exactly what works today.

## SRE and reliability

| Project | Status | What it does |
|---|---|---|
| [incident-review-copilot](https://github.com/narayana006/incident-review-copilot) | Working | Score and review postmortems: flags missing timings, blame language, vague or unowned action items. |
| [alert-noise-auditor](https://github.com/narayana006/alert-noise-auditor) | Working | Analyze alert history to find flapping, never-actioned and duplicate alerts, and suggest threshold changes or deletions. |
| [change-risk-scorer](https://github.com/narayana006/change-risk-scorer) | Working | Score the risk of a PR or deploy by blast radius, config changes, timing and recent incidents, and post it as a PR comment. |
| [k8s-explain](https://github.com/narayana006/k8s-explain) | Working | Pipe kubectl output in, get a plain-English diagnosis, likely fix and verification commands out. |
| [terraform-plan-explainer](https://github.com/narayana006/terraform-plan-explainer) | Working | Turn a Terraform plan into a plain-English summary that calls out destructive and high-risk changes before you apply. |
| [log-triage](https://github.com/narayana006/log-triage) | Working | Collapse noisy logs into patterns, surface what is new or spiking, and summarise the likely cause. |
| [capacity-forecast](https://github.com/narayana006/capacity-forecast) | Working | Forecast when services will run out of CPU, memory, disk or quota from existing Prometheus metrics. |
| [cert-expiry-watch](https://github.com/narayana006/cert-expiry-watch) | Working | Find TLS certificates that are about to expire across domains, Kubernetes secrets and cloud load balancers. |
| [deploy-diff-summary](https://github.com/narayana006/deploy-diff-summary) | Working | Explain what actually changed between two releases: commits, config, container images and infrastructure, in plain English. |
| [toil-tracker](https://github.com/narayana006/toil-tracker) | Working | Measure operational toil from tickets and pages and rank the best candidates for automation. |
| [cloud-cost-anomaly](https://github.com/narayana006/cloud-cost-anomaly) | Working | Detect unusual cloud spend from billing exports and explain which service, account or tag caused it. |
| [error-budget-report](https://github.com/narayana006/error-budget-report) | Working | Generate a weekly error budget report from your SLO definitions and metrics, with what consumed the budget. |
| [ai-postmortem](https://github.com/narayana006/ai-postmortem) | Working | Build an incident timeline and a blameless postmortem draft from Slack exports, PagerDuty log entries, alert logs and deploy events. |
| [incident-pattern-miner](https://github.com/narayana006/incident-pattern-miner) | Working | Cluster past incidents by theme to find repeat failure modes and produce quarterly reliability reports. |
| [runbook-agent](https://github.com/narayana006/runbook-agent) | Working | Turn Markdown runbooks into agent-executable steps: read-only diagnostics run automatically, changes require human approval. Ships as an MCP server. |
| [slo-suggest](https://github.com/narayana006/slo-suggest) | Working | Suggest availability and latency SLOs from your access logs, and generate OpenSLO YAML plus Prometheus burn-rate alerts. |
| [oncall-handoff](https://github.com/narayana006/oncall-handoff) | Working | Summarize an on-call shift from exported pages, Slack messages and tickets into a clear handoff note. |
| [statuswall](https://github.com/narayana006/statuswall) | Planned | One dashboard for all vendor status pages (AWS, Google Cloud, Azure, GitHub, Cloudflare, ...) with historical uptime from public data. |
| [incident-comms-drafter](https://github.com/narayana006/incident-comms-drafter) | Working | Draft status page updates, executive summaries and support briefs from an incident channel export, checked against your house style. |
| [gameday-planner](https://github.com/narayana006/gameday-planner) | Working | Propose failure-injection experiments for game days from your architecture and past incidents. |
| [gcp-stockout-guard](https://github.com/narayana006/gcp-stockout-guard) | Working | Find Google Cloud capacity stockouts in Compute Engine error logs and rank fallback zones, using saved Capacity Advisor responses. |
| [ai-incident-management-companion](https://github.com/narayana006/ai-incident-management-companion) | Working | Companion code for the book AI-Driven Incident Management: fixtures, calculations, figures and labs. |

## Apache Kafka

| Project | Status | What it does |
|---|---|---|
| [kraft-quickstart](https://github.com/narayana006/kraft-quickstart) | Working | Run a realistic multi-node Apache Kafka cluster in KRaft mode locally with Docker Compose: no ZooKeeper. |
| [zk-to-kraft-check](https://github.com/narayana006/zk-to-kraft-check) | Working | Check whether an Apache Kafka cluster is ready to migrate from ZooKeeper to KRaft, and list what blocks it. |
| [kraft-quorum-inspect](https://github.com/narayana006/kraft-quorum-inspect) | Working | Show the health of a Kafka KRaft controller quorum at a glance: leader, voters, observers and replication lag. |
| [kafka-lag-explain](https://github.com/narayana006/kafka-lag-explain) | Working | Report Kafka consumer lag and explain the likely cause: slow consumer, stuck partition, rebalance storm or traffic spike. |
| [kafka-topic-auditor](https://github.com/narayana006/kafka-topic-auditor) | Working | Audit Kafka topics for risky settings: low replication, weak durability, skewed partitions and topics nobody uses. |
| [kafka-reassign-planner](https://github.com/narayana006/kafka-reassign-planner) | Working | Generate a balanced, throttled Kafka partition reassignment plan that moves as little data as possible. |
| [kafka-config-diff](https://github.com/narayana006/kafka-config-diff) | Working | Compare broker and topic configuration between Kafka clusters or against a baseline file. |
| [schema-compat-ci](https://github.com/narayana006/schema-compat-ci) | Working | Fail the build when an Avro, Protobuf or JSON schema change would break Kafka consumers, checked against Schema Registry. |
| [kafka-acl-audit](https://github.com/narayana006/kafka-acl-audit) | Working | Audit Apache Kafka ACLs from kafka-acls output: flag wildcard principals and resources, overly broad operations, and duplicate or shadowed rules. |
| [kafka-client-config-lint](https://github.com/narayana006/kafka-client-config-lint) | Working | Lint Kafka producer and consumer configs against durability, latency or throughput profiles, with an explanation for every finding. |
| [kafka-partition-skew](https://github.com/narayana006/kafka-partition-skew) | Working | Find partition skew in Apache Kafka topics from kafka-log-dirs output: uneven partition sizes, hot brokers and disks, and likely key problems. |
| [kafka-consumer-reset-plan](https://github.com/narayana006/kafka-consumer-reset-plan) | Working | Plan Kafka consumer group offset resets safely: preview the new offsets and lag, and print the exact kafka-consumer-groups command, never running it. |
| [kafka-connect-doctor](https://github.com/narayana006/kafka-connect-doctor) | Working | Diagnose Kafka Connect connectors from the REST API status: failed tasks, classified errors, and a safe restart plan. |

## AWS command line and SDK

| Project | Status | What it does |
|---|---|---|
| [aws-whoami-plus](https://github.com/narayana006/aws-whoami-plus) | Working | Show exactly which AWS identity, account, region and role chain your shell is using, and when the session expires. |
| [aws-profile-switch](https://github.com/narayana006/aws-profile-switch) | Working | Switch AWS profiles and SSO sessions quickly from the terminal, with fuzzy search and automatic login. |
| [s3-du](https://github.com/narayana006/s3-du) | Working | A du for Amazon S3: show how much storage each bucket and prefix uses, by storage class, without listing every object. |
| [aws-unused-finder](https://github.com/narayana006/aws-unused-finder) | Working | Find AWS resources you are paying for but not using: unattached volumes, idle IPs, old snapshots, empty load balancers and more. |
| [iam-policy-explain](https://github.com/narayana006/iam-policy-explain) | Working | Explain an AWS IAM policy in plain English and flag wildcards, privilege escalation paths and public access. |
| [cw-logs-multitail](https://github.com/narayana006/cw-logs-multitail) | Working | Tail several CloudWatch Logs groups at once in one merged, colour-coded stream with filters. |
| [ssm-env-sync](https://github.com/narayana006/ssm-env-sync) | Working | Keep .env files and AWS Systems Manager Parameter Store in sync: diff, pull and push with a dry-run first. |
| [boto3-patterns](https://github.com/narayana006/boto3-patterns) | Working | Small, runnable boto3 examples of the patterns every AWS script needs: pagination, retries, waiters, concurrency and assumed roles. |
| [aws-tag-audit](https://github.com/narayana006/aws-tag-audit) | Working | Check AWS resources against your tagging policy: missing, empty or invalid tags, with a report by owner and service. |
| [sg-exposure-check](https://github.com/narayana006/sg-exposure-check) | Working | Find AWS security groups that expose sensitive ports to the internet, and show which instances, load balancers and databases they actually reach. |
| [aws-quota-watch](https://github.com/narayana006/aws-quota-watch) | Working | Show AWS service quotas that are close to their limits, using Service Quotas and CloudWatch usage metrics. |
| [cfn-drift-report](https://github.com/narayana006/cfn-drift-report) | Working | Turn AWS CloudFormation drift results into a readable report: which resources drifted, what changed, and by how much. |
| [ecr-image-cleanup-plan](https://github.com/narayana006/ecr-image-cleanup-plan) | Working | Plan Amazon ECR image cleanup: find untagged, old and unused images, estimate storage saved, and generate a lifecycle policy, dry-run first. |

## AWS Lambda

| Project | Status | What it does |
|---|---|---|
| [lambda-cold-start-bench](https://github.com/narayana006/lambda-cold-start-bench) | Working | Measure AWS Lambda cold start times across memory sizes from REPORT log lines, with cold versus warm statistics and a chart. |
| [lambda-rightsize](https://github.com/narayana006/lambda-rightsize) | Working | Recommend a memory setting for each AWS Lambda function from its REPORT logs or CloudWatch Logs Insights exports, with estimated savings. |
| [lambda-dlq-redrive](https://github.com/narayana006/lambda-dlq-redrive) | Working | Inspect, filter and safely replay failed events from AWS Lambda dead-letter queues. |
| [lambda-uptime-ping](https://github.com/narayana006/lambda-uptime-ping) | Working | A tiny scheduled AWS Lambda that checks your URLs and posts to Slack when one is down or slow. |
| [lambda-url-shortener](https://github.com/narayana006/lambda-url-shortener) | Working | A minimal serverless URL shortener on AWS Lambda and DynamoDB, as a small reference project. |
| [lambda-python-starter](https://github.com/narayana006/lambda-python-starter) | Working | A clean starting point for Python AWS Lambda functions: structure, typed handlers, tests, local invoke and CI. |

## Google Cloud

| Project | Status | What it does |
|---|---|---|
| [gcp-iam-explain](https://github.com/narayana006/gcp-iam-explain) | Working | Explain a Google Cloud IAM policy in plain English and flag basic roles, public members, external domains and risky bindings. |
| [gcp-firewall-audit](https://github.com/narayana006/gcp-firewall-audit) | Working | Audit Google Cloud VPC firewall rules: internet-exposed ports, overly broad rules, disabled and shadowed rules. |
| [gcp-label-audit](https://github.com/narayana006/gcp-label-audit) | Working | Check Google Cloud resources against a labeling policy using a Cloud Asset Inventory export: missing, empty or invalid labels by project and type. |
| [gcp-idle-resources](https://github.com/narayana006/gcp-idle-resources) | Working | Find Google Cloud resources you pay for but do not use: unattached disks, unused static IPs, old snapshots and stopped VMs with disks. |
| [gcp-quota-check](https://github.com/narayana006/gcp-quota-check) | Working | Show Google Cloud Compute Engine quotas close to their limits across regions, from gcloud output, with CI-friendly exit codes. |

## AI engineering

| Project | Status | What it does |
|---|---|---|
| [prompt-regress](https://github.com/narayana006/prompt-regress) | Working | Regression tests for LLM prompts: YAML cases, LLM-judge + deterministic asserts, diff reports in CI. |
| [llm-cost-guard](https://github.com/narayana006/llm-cost-guard) | Working | Per-user and per-feature token budgets, spend tracking and alerts for LLM-powered apps. |
| [repo-to-context](https://github.com/narayana006/repo-to-context) | Working | Pack a code repository into LLM-ready context: gitignore-aware, token-budgeted, importance-ranked. |
| [pii-scrub](https://github.com/narayana006/pii-scrub) | Working | Redact PII and secrets before text reaches an LLM, then restore them in the response. |
| [structured-extract](https://github.com/narayana006/structured-extract) | Working | Schema in, validated JSON out: extract structured data from messy text with retries, repair and per-field confidence. |
| [llm-observe](https://github.com/narayana006/llm-observe) | Working | Self-hosted, minimal LLM tracing: one-line SDK wrapper, SQLite storage and a local web UI for prompts, latency, cost and errors. |
| [mcp-starter-kit](https://github.com/narayana006/mcp-starter-kit) | Working | Tested starter templates for building Model Context Protocol (MCP) servers in TypeScript and Python. |
| [agent-skills-collection](https://github.com/narayana006/agent-skills-collection) | Working | Reusable agent skills (SKILL.md plus scripts) for release notes, migrations, security reviews and SEO audits, with a skill linter. |
| [rag-eval-lite](https://github.com/narayana006/rag-eval-lite) | Working | Measure RAG quality offline: retrieval recall, precision, MRR and nDCG, deterministic answer checks, and an HTML report. |
| [doc-ingest](https://github.com/narayana006/doc-ingest) | Working | One command from text, Markdown, HTML, DOCX and PDF files to clean, section-aware JSONL chunks with source metadata. |
| [agent-patterns](https://github.com/narayana006/agent-patterns) | Working | Small, runnable reference implementations of common AI agent patterns, each under 200 lines. |
| [ai-alert-explainer](https://github.com/narayana006/ai-alert-explainer) | Working | Turn an alert into an ACT / WATCH / IGNORE verdict with reasons and a confidence score: rule-based, with an optional model step. |
| [expo-ai-starter](https://github.com/narayana006/expo-ai-starter) | Working | Expo / React Native starter with a streaming AI chat screen and a backend proxy that keeps API keys out of the app. |
| [ai-pr-reviewer-action](https://github.com/narayana006/ai-pr-reviewer-action) | Working | GitHub Action that reviews pull requests against plain-English rules in .ai-review.md, commenting only on high-confidence findings. |

## Get in touch

Open an issue on any project with feedback, a use case or a feature idea.
