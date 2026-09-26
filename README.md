# Hi, I'm Vishal 👋

**Lead AI Product Manager & Builder — Agentic AI**

10+ years launching 0→1 products and scaling platforms across **fintech, SaaS and enterprise platforms, and marketplaces**. Today I lead agentic AI product strategy at Vanguard, and on the side I build the eval and trust tooling I wish every AI team had.

**What ties it together:** AI output is only worth shipping when it can be checked against a source of truth, whether that's an IRS rule, a tool's own schema, or a platform's API contract.

## 💼 Currently
Leading product strategy for **Digital Advisor** and **Personal Advisor** at **Vanguard** ($6B+ LOB, 4M+ MAU) — architecting the next-generation Agentic AI Digital Advisor from 0-to-1, including model evaluation frameworks (correctness, groundedness, safety, latency) and FINRA/SEC-compliant responsible AI design.

## 🚀 Selected work, by vertical
- 🏦 **Fintech: Vanguard.** Agentic AI Digital Advisor (0→1): LLM orchestration, autonomous agent workflows, personalized financial guidance at scale, with regulatory guardrails and model governance. Earlier in fintech: Axis Bank.
- 🏢 **SaaS & enterprise platforms: T-Mobile.** Launched one of the first autonomous enterprise Agentic AI platforms in US telecom: **75% adoption, 46% automation, 60% containment, 80% CSAT, 30% fewer support calls**. Built the IntentCX AI governance & model evaluation framework (aligned to NIST AI RMF), adopted org-wide by 3 additional teams.
- 🛒 **Marketplaces: eBay.** Drove **$300M+ in savings** via marketplace platform modernization and API standardization across hundreds of engineering teams.

## 🗺️ Where my work sits in the AI stack

| Layer | Shipped at work | Built in the open |
|---|---|---|
| **Apps & human-in-the-loop** | 🏦 Vanguard Digital Advisor experience · 🏢 T-Mobile agentic support platform | 🏦 [Contribution room calculator](https://vishalhabib99.github.io/retirement-answer-check/room/) · 🏦 [Review queue](https://github.com/vishalhabib99/retirement-answer-check#human-review-queue-is-the-review-itself-working) that tests whether reviewers catch what the checker missed · 🛒 [Listing checker demo](https://vishalhabib99.github.io/listing-claim-check/) |
| **Agents & orchestration** | 🏦 Agentic AI Digital Advisor (0→1) · 🏢 Autonomous enterprise agent platform | [`GuardedSession`](https://github.com/vishalhabib99/mcp-trust-check#a-decision-on-every-call-act-escalate-or-block): decides ACT, ESCALATE or BLOCK on each live tool call |
| **Tools & APIs (MCP)** | 🛒 eBay API standardization across hundreds of teams | [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor), [`mcp-fuzz`](https://github.com/vishalhabib99/mcp-fuzz), [`mcp-reality-check`](https://github.com/vishalhabib99/mcp-reality-check) · 🏦 `check_answer` and `contribution_room` MCP tools · 🛒 `check_listing` MCP tool |
| **Evals & quality** | 🏦 Model evals for correctness, groundedness, safety, latency · 🏢 IntentCX evaluation framework | 🏦 [Blind, pre-registered evals](https://github.com/vishalhabib99/retirement-answer-check#results) · 🛒 [A failed first blind run, then a fresh blind pass](https://github.com/vishalhabib99/listing-claim-check#results) · [`/eval-plan`](https://github.com/vishalhabib99/ai-pm-skills) |
| **Guardrails, governance & risk** | 🏦 FINRA/SEC-compliant responsible AI design · 🏢 Governance aligned to NIST AI RMF | 🏦 [Model risk pack](https://github.com/vishalhabib99/retirement-answer-check/blob/main/docs/model-risk/README.md) (SR 26-2 + NIST AI 600-1) · [`mcp-trust-check`](https://github.com/vishalhabib99/mcp-trust-check) release gate, policy, audit log, PII checks |
| **Cost & pricing** | 🏢 Accuracy, cost and latency tuned per interaction type: latency roughly halved on low-stakes queries | 🏢 [Which model, and how to price it](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-09-ai-feature-unit-economics.md): verified model pricing, 4 routing options, per-seat economics |
| **Product decisions** | 0→1 strategy, launch gates, adoption and containment metrics | [`/build-or-not`](https://github.com/vishalhabib99/ai-pm-skills) · [Agent Readiness Scorecard](https://vishalhabib99.github.io/agentic-product-playbook/) |

## ✅ Proof from outside
- Fix [merged upstream](https://github.com/homeassistant-ai/ha-mcp/pull/2327) into `ha-mcp` (4.8K★)
- Maintainers shipped fixes after my findings: [`mcp-server-chart`](https://github.com/antvis/mcp-server-chart/issues/323) (4.3K★) and [`agent-inspect`](https://github.com/rajudandigam/agent-inspect/issues/362)
- Two contributors on the official [MCP spec discussion](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions/3322) tested my tools and reported two real bugs and a spec gap; all three are fixed or shipped as new checks
- A [public leaderboard](https://vishalhabib99.github.io/mcp-doctor/) grading 21 popular MCP servers, and [real skill runs](https://vishalhabib99.github.io/ai-pm-skills/) you can read without installing anything

## 🔗 Why this portfolio exists
At work I build evals for AI agents: is the answer correct, grounded, safe and fast? These projects apply the same checks one layer down, to the tools an agent calls. `mcp-doctor` checks that a tool is documented well enough to use, `mcp-fuzz` checks that it fails safely and responds fast, and `mcp-reality-check` checks that its answers are true to what it did. `ai-pm-skills` packages the product side of that work, deciding what to build and what "good enough to ship" means, for other PMs. `agentic-product-playbook` is the no-install version for any PM: the failure modes, templates and a 3-minute scorecard for deciding whether an agent is ready to launch. `retirement-answer-check` puts it all together on one regulated use case.

<details><summary>What this doesn't cover, by design</summary><br>

Two areas that used to be on this list have shipped, rebuilt so nothing is guessed. **Runtime authorization** is now a policy the operator writes, enforced before each call. **Logging** is now a tamper-evident audit log the wrapper writes itself, rather than a grade of the server's own logs. Both are in `mcp-trust-check`.

- **Semantic hallucination** ("is this answer actually true"): needs an LLM judge, which would break the deterministic, no-API-cost design all three tools share.
- **Live agent red-teaming**: `mcp-doctor`'s security score audits a tool's own code and description for injection risk, not whether a live agent can be manipulated at runtime.

</details>

## 🧱 Portfolio

**🏦 Fintech: verified AI answers about retirement money**

- 🛡️ [`retirement-answer-check`](https://github.com/vishalhabib99/retirement-answer-check) — Checks an AI assistant's draft answer to a retirement-account question before a customer sees it: SEND or REVIEW, with an IRS or FINRA source for every flag. Built end to end: PRD, launch gates set before the first run, blind held-out tests, release gated by `mcp-trust-check`. Pattern rules alone let 5 of 15 blind wrong facts through; adding a fact-checking judge brought that to 0 of 25. Personal project, public sources only.

  <details><summary>More detail</summary><br>

  - **[Contribution room calculator](https://vishalhabib99.github.io/retirement-answer-check/room/):** how much more you can put into a 401(k), IRA and Roth IRA in 2026, with an IRS link on every number. No model: the same deterministic logic ships as a `contribution_room` MCP tool, so an assistant can compute limits instead of quoting last year's from memory. Tested against the IRS's own worked example.
  - **[Model risk pack](https://github.com/vishalhabib99/retirement-answer-check/blob/main/docs/model-risk/README.md):** inventory, model card, validation report and monitoring plan. Written against SR 26-2, the April 2026 replacement for SR 11-7, which leaves generative AI out of scope, so the LLM judges are governed under NIST AI 600-1. Verdict: shadow mode only, with 3 open High findings, including prompt injection that hasn't been tested yet.

  </details>

**🛒 Marketplaces: AI listings that match the item**

- 🏷️ [`listing-claim-check`](https://github.com/vishalhabib99/listing-claim-check) — Checks an AI-written listing against the seller's own item specifics before it's published: PUBLISH or REVIEW, with the exact words behind every unbacked claim ("like new" on a used phone, "unlocked" on a carrier-locked one, a box that isn't included). **[Try it in your browser →](https://vishalhabib99.github.io/listing-claim-check/)** Gates were set before any code. v0.1 **failed** its first blind run (2 of 11 high-harm claims got through), so the design changed: any number no item specific backs goes to a person. On a fresh blind set, 0 of 11 got through.

**🏢 SaaS & enterprise platforms**

- 📊 [Which model, and how to price it](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-09-ai-feature-unit-economics.md) — unit economics for an AI support-drafting feature: verified Claude pricing (including the ~30% tokenizer difference), four routing options, per-seat pricing. The finding: model cost is under 5% of the value delivered, so the constraint is draft quality, and caching barely matters because retrieved docs can't be cached.
- 📡 [T-Mobile case study](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/case-studies/2026-09-tmobile-enterprise-agentic-platform.md) — four architecture decisions behind the agentic platform (25M users, 60% containment), their tradeoffs, and what I'd do differently.

**For AI product managers**

- 📋 [`agentic-product-playbook`](https://github.com/vishalhabib99/agentic-product-playbook) — 7 ways AI agents fail in production, plus the templates that catch them: agent PRD, eval plan, launch checklist, metrics glossary. **[Take the 3-minute Agent Readiness Scorecard →](https://vishalhabib99.github.io/agentic-product-playbook/)**

- 🧭 [`ai-pm-skills`](https://github.com/vishalhabib99/ai-pm-skills) — Claude Code skills for AI PMs: `/build-or-not`, `/eval-plan`, `/agent-trust-review`. Each is tested with evals whose gates were set before the first run, failures included. **[See real runs without installing →](https://vishalhabib99.github.io/ai-pm-skills/)**

  <details><summary>More detail</summary><br>

  - `/build-or-not` checks a feature idea against 4–8 real examples, using a bar set before looking, and writes a build / don't build / narrow decision record.
  - `/eval-plan` turns a PRD into pass/fail launch gates set before any results exist.
  - `/agent-trust-review` sorts an agent's risks into covered (with evidence), declined on purpose, and genuinely missing.
  - Built from the real build and no-build decisions behind the MCP tools below.

  </details>

  <img src="https://raw.githubusercontent.com/vishalhabib99/ai-pm-skills/main/docs/demo.gif" alt="A real /build-or-not run in Claude Code: 0 of 6 real examples clear the bar, so the decision is don't build" width="600">

- 📄 [`ai-pm-portfolio`](https://github.com/vishalhabib99/ai-pm-portfolio) — PRDs, working prototypes, and honestly-reported evals (including failures, not just wins)

**Trust & quality tooling for the tools AI agents call (MCP)**

- 🩺 [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor) — static audit of MCP servers for what breaks an agent calling them. Run on 40+ real servers up to 76k★: 43 real bugs found and fixed, one fix [merged upstream](https://github.com/homeassistant-ai/ha-mcp/pull/2327). [Public leaderboard](https://vishalhabib99.github.io/mcp-doctor/).

  <details><summary>More detail</summary><br>

  - `pip install mcp-server-lint`, or as a [GitHub Marketplace Action](https://github.com/marketplace/actions/mcp-doctor).
  - Tested on official servers from GitHub, HashiCorp, Red Hat, Brave, MathWorks and the MCP spec's own reference servers.
  - Checks documentation, security risks (dangerous exec, SSRF, tool poisoning), annotation contradictions, unpinned dependencies, breaking changes between versions (`--diff-against`), and tools whose descriptions an agent can't tell apart. Across 1,543 real tools, that last check found one issue, a real copy-paste bug, and no false positives.
  - Most fixes came from its own false positives on real repos; a recurring pattern was confirmed on other codebases before a fix shipped. [Full build log →](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/BUILD_LOG.md)

  </details>
- 🧪 [`mcp-fuzz`](https://github.com/vishalhabib99/mcp-fuzz) — launches a real MCP server and calls every tool with schema-derived inputs to check it fails cleanly. Runtime runs on 24 real servers up to 61K★; crash bugs filed upstream, one confirmed fixed, and an external maintainer shipped a fix in response to a finding.

  <details><summary>More detail</summary><br>

  - `pip install mcp-runtime-check`. Works over stdio or remote Streamable HTTP (`--url`).
  - Found all 27 tools in Ant Design's `mcp-server-chart` crashing on bad input ([fixed upstream](https://github.com/antvis/mcp-server-chart/issues/323)), plus bugs [filed on `shadcn-ui-mcp-server`](https://github.com/Jpisnice/shadcn-ui-mcp-server/issues/61) and [`codebase-memory-mcp`](https://github.com/DeusData/codebase-memory-mcp/issues/2118) (44.9K★).
  - Also checks latency, response size, concurrency, resource lifecycles and token cost, and runs as a live gate inside an agent session (`LatencyGate`).
  - [Full build log →](https://github.com/vishalhabib99/mcp-fuzz/blob/main/docs/BUILD_LOG.md)

  </details>
- 🩻 [`mcp-reality-check`](https://github.com/vishalhabib99/mcp-reality-check) — checks whether a "successful" tool response actually is: refusals disguised as success, empty content, output that breaks its own schema. Deterministic, no LLM judge. 18+ real-world runs.

  <details><summary>More detail</summary><br>

  - `pip install mcp-reality-check`. No API key, no per-call cost.
  - Runs as a batch audit or as a live gate (`guarded_call`) that catches a misleading "success" before it reaches the agent.
  - Scoped to correctness on purpose: a call can be perfectly safe and still misrepresent what it did.
  - [Full build log →](https://github.com/vishalhabib99/mcp-reality-check/blob/main/docs/BUILD_LOG.md)

  </details>
- 🛡️ [`mcp-trust-check`](https://github.com/vishalhabib99/mcp-trust-check) — all three as one [GitHub Action](https://github.com/marketplace/actions/mcp-trust-check) (stdio or HTTP). Plus a no-tool-calls survey of 10 hosted MCP servers that traced a real annotation bug in GitMCP (8.4K★), [reported with the root cause](https://github.com/idosal/git-mcp/issues/266).

  <details><summary>More detail</summary><br>

  - One combined score and PR comment instead of three, plus a [release decision](https://github.com/vishalhabib99/mcp-trust-check#release-decision-ship-fix-first-or-block): SHIP, FIX-FIRST, or BLOCK. An average can hide the one crash that matters. The decision can't, because the worst finding wins, and every reason is listed. Each decision also carries a [confidence level](https://github.com/vishalhabib99/mcp-trust-check#confidence-should-you-act-on-the-decision) (how much of the server was actually exercised) and a needs-human-review flag, so clear cases can pass automatically and the rest go to a person. Also a Python package (`GuardedSession`) that runs all three live checks on each real call, calling the tool only once, and [decides each call](https://github.com/vishalhabib99/mcp-trust-check#a-decision-on-every-call-act-escalate-or-block): ACT, ESCALATE to a person, or BLOCK, with a confidence level. It also enforces [an operator-written policy](https://github.com/vishalhabib99/mcp-trust-check#policy-audit-log-and-pii-guardrails-for-a-live-agent) before each call, keeps a tamper-evident audit log, and escalates responses that leak card numbers, SSNs or IBANs (0 false positives across 20,513 real files).
  - The [hosted-server survey](https://github.com/vishalhabib99/mcp-trust-check/tree/main/docs/hosted-survey-2026-09) (Hugging Face, Microsoft Learn, AWS, Cloudflare and 6 more) reads only what every client reads on connect. I chose not to fuzz other companies' production endpoints.
  - 🎥 [35s live demo](https://github.com/vishalhabib99/mcp-trust-check#demo) · [Full build log →](https://github.com/vishalhabib99/mcp-trust-check/blob/main/docs/BUILD_LOG.md)

  </details>

## ✍️ Writing
- [I set the pass bar before testing my Claude Code skills. The first run failed.](https://dev.to/vishalhabib99/i-set-the-pass-bar-before-testing-my-claude-code-skills-the-first-run-failed-1ef5) — the eval story behind ai-pm-skills, on dev.to
- [I Built Three Tools to Audit MCP Servers for Agentic AI. Here's What They Found — and What I Learned Shipping Them.](https://www.linkedin.com/pulse/i-built-three-tools-audit-mcp-servers-agentic-ai-heres-vishal-habib-kmv3c/) — the trilogy story on LinkedIn
- [Building T-Mobile's First Enterprise Agentic AI Platform: 25M Users, 75% Adoption, and What I'd Do Differently](https://www.linkedin.com/pulse/building-t-mobiles-first-enterprise-agentic-ai-platform-vishal-habib-bftoc/) — the platform story on LinkedIn
- [I built three tools to audit MCP servers. Each one found a bug in itself first.](https://dev.to/vishalhabib99/i-built-three-tools-to-audit-mcp-servers-each-one-found-a-bug-in-itself-first-5dlc) — the trilogy's origin story, on dev.to

## 🎓 Background
Stanford University Graduate School of Business

## 📫 Reach me
- Email: [vishalhabib99@gmail.com](mailto:vishalhabib99@gmail.com)
- LinkedIn: [in/vishal-habib](https://www.linkedin.com/in/vishal-habib/)
- Website: [vishalhabib.netlify.app](https://vishalhabib.netlify.app/)
- dev.to: [@vishalhabib99](https://dev.to/vishalhabib99)
