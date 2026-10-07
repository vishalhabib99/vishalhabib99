# Hi, I'm Vishal 👋

**Lead AI Product Manager & Builder — Agentic AI** · leading the 0→1 Agentic AI Digital Advisor at **Vanguard** · ex-T-Mobile, eBay · Stanford GSB

10+ years launching 0→1 products and scaling platforms 1→100 across **fintech, SaaS and enterprise platforms, and marketplaces**: **$9B+ in revenue platforms, 29M+ MAU, $300M+ in cost savings**. On the side I build the eval and trust tooling I wish every AI team had, and I publish the failures along with the passes.

**What ties it together:** AI output is only worth shipping when it can be checked against a source of truth, whether that's an IRS rule, a tool's own schema, or a platform's API contract.

**⏱️ Got 2 minutes? Start here:**
1. **[A real report from a real user](https://github.com/vishalhabib99/mcp-doctor/issues/5)**: an outside maintainer opened an issue and a bot graded their MCP server. No install needed.
2. **[A red team that broke my own checker](https://github.com/vishalhabib99/listing-claim-check#results)**: all 22 in-scope attacks got through, and I published it as-is.
3. **[Try a checker yourself](https://vishalhabib99.github.io/agent-handoff-check/)**: an agent-to-agent handoff, decided ACT, ESCALATE or BLOCK, in your browser.
4. **[A 155K★ project built its fix on my PR](https://github.com/langflow-ai/langflow/pull/15565)**: Langflow's maintainer adapted my fix for MCP tool arguments and credited me as co-author.

## ✅ Proof from outside
None of these maintainers work with me. Each change shipped because the evidence was clear enough for them to act on.

> "Thank you for the exact tools/list results and for explaining the effect on clients that use annotations for approval." ([`codebase-memory-mcp` maintainer](https://github.com/DeusData/codebase-memory-mcp/issues/2118#issuecomment-5609248676))<br>
> "Thanks for shipping this and keeping the regression case." ([an outside tester whose agent found the bug](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions/3322#discussioncomment-18514875))

- Fixes merged upstream, all reviewed and merged by the projects' own maintainers:
  - [`langflow`](https://github.com/langflow-ai/langflow/pull/15565) (155K★): MCP tool arguments named after component methods, such as `index`, were sent as the method instead of the configured value. The maintainer built the fix on [my PR](https://github.com/langflow-ai/langflow/pull/15523) and credits me as co-author.
  - [`mcp-for-blender`](https://github.com/ahujasid/mcp-for-blender/commit/250c00deca845c04df8c72e5b324291ee4969054) (30K★): optional tool arguments now accept an explicit null, re-applied by the maintainer on a refactor with me as commit author.
  - [`davinci-resolve-mcp`](https://github.com/samuelgursky/davinci-resolve-mcp/pull/274) (3.4K★): 16 optional arguments on 9 tools rejected an explicit null, now 0. [Shipped in v4.8.29](https://github.com/samuelgursky/davinci-resolve-mcp/releases/tag/v4.8.29) with a credit in the release notes.
  - [`jupyter-mcp-server`](https://github.com/datalayer/jupyter-mcp-server/pull/480) (1.3K★), 2 fixes: [`connect_to_jupyter`](https://github.com/datalayer/jupyter-mcp-server/pull/480) now checks the server before reporting success, and [`tools/list`](https://github.com/datalayer/jupyter-mcp-server/pull/482) no longer reads the server mode before it is set.
  <details><summary>6 more merged fixes: ha-mcp, shadcn-ui-mcp-server, telegram-mcp, open-meteo-mcp, devglobe, osm-mcp-server</summary>

  - [`ha-mcp`](https://github.com/homeassistant-ai/ha-mcp/pull/2327) (4.9K★)
  - [`shadcn-ui-mcp-server`](https://github.com/Jpisnice/shadcn-ui-mcp-server/pull/62) (3K★): bad tool input now returns a clear error instead of crashing
  - [`telegram-mcp`](https://github.com/chigwell/telegram-mcp/pull/266) (1.8K★): 111 of 131 tools rejected an explicit null for their optional arguments, now 0
  - [`open-meteo-mcp`](https://github.com/cmer81/open-meteo-mcp/pull/81): [shipped in v2.5.1](https://github.com/cmer81/open-meteo-mcp/releases/tag/v2.5.1), with a maintainer follow-up built on it
  - [`devglobe`](https://github.com/sajeetharan/devglobe/pull/463): closes the maintainer's tool-contract issue
  - [`osm-mcp-server`](https://github.com/yuiseki/osm-mcp-server/pull/43): both geocoding tools failed with 403 Forbidden until the fix added the User-Agent Nominatim requires

  </details>
- Both of my fixes to `excel-mcp-server` (4.2K★) were reimplemented in its v1.0.0 rewrite, [credited in the changelog](https://github.com/haris-musa/excel-mcp-server/releases/tag/v1.0.0)
- Maintainers shipped fixes after my findings: [`codebase-memory-mcp`](https://github.com/DeusData/codebase-memory-mcp/issues/2118) (45.9K★) relabeled all 12 mislabeled read-only tools (10 in v0.11.0, the [last 2](https://github.com/DeusData/codebase-memory-mcp/pull/2404) merged 09-30); plus [`mcp-server-chart`](https://github.com/antvis/mcp-server-chart/issues/323) (4.4K★) and [`agent-inspect`](https://github.com/rajudandigam/agent-inspect/issues/362)
- Two contributors on the official [MCP spec discussion](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions/3322) tested my tools and reported two real bugs and a spec gap; all three are fixed or shipped as new checks
- A [public leaderboard](https://vishalhabib99.github.io/mcp-doctor/) grading 24 MCP servers, 3 of them added by an outside maintainer through the [no-install scan](https://github.com/vishalhabib99/mcp-doctor/issues?q=label%3Ascan-request), and [real skill runs](https://vishalhabib99.github.io/ai-pm-skills/) you can read without installing anything

<details><summary><b>🗺️ Where my work sits in the AI stack</b>: what I shipped at work vs. built in the open, layer by layer</summary><br>

| Layer | Shipped at work | Built in the open |
|---|---|---|
| **Apps & human-in-the-loop** | 🏦 Vanguard Digital Advisor experience · 🏢 T-Mobile agentic support platform | 🏦 [Contribution room calculator](https://vishalhabib99.github.io/retirement-answer-check/room/) · 🏦 [Review queue](https://github.com/vishalhabib99/retirement-answer-check#human-review-queue-is-the-review-itself-working) that tests whether reviewers catch what the checker missed · 🛒 [Listing checker demo](https://vishalhabib99.github.io/listing-claim-check/) |
| **Agents & orchestration** | 🏦 Agentic AI Digital Advisor (0→1) · 🏢 Autonomous enterprise agent platform | [`GuardedSession`](https://github.com/vishalhabib99/mcp-trust-check#a-decision-on-every-call-act-escalate-or-block): decides ACT, ESCALATE or BLOCK on each live tool call · 🏢 [`agent-handoff-check`](https://github.com/vishalhabib99/agent-handoff-check): checks every agent-to-agent handoff so authority can only narrow |
| **Tools & APIs (MCP)** | 🛒 eBay API standardization across hundreds of teams | [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor), [`mcp-fuzz`](https://github.com/vishalhabib99/mcp-fuzz), [`mcp-reality-check`](https://github.com/vishalhabib99/mcp-reality-check) · 🏦 `check_answer` and `contribution_room` MCP tools · 🛒 `check_listing` MCP tool |
| **Evals & quality** | 🏦 Model evals for correctness, groundedness, safety, latency · 🏢 IntentCX evaluation framework | 🏦 [Blind, pre-registered evals](https://github.com/vishalhabib99/retirement-answer-check#results) · 🛒 [A failed blind run, a fresh blind pass, then a red team that broke it](https://github.com/vishalhabib99/listing-claim-check#results) · 🏢 [A small RAG prototype retested on blind tickets](https://github.com/vishalhabib99/ai-pm-portfolio/tree/main/prototypes/ticket-triage-rag#tried-retry-retrieval-when-the-match-is-ambiguous): accuracy fell from 60% to 38%, and the agentic retry step fixed 1 of 16 · ⚛️ [An exact grader for AI-written quantum circuits](https://github.com/vishalhabib99/circuit-claim-check): right on all 90 real answers, yet 4 red teams got 27 wrong circuits graded pass ([write-up](https://dev.to/vishalhabib99/my-grader-got-every-real-answer-right-four-red-teams-still-broke-it-632)) · [`/eval-plan`](https://github.com/vishalhabib99/ai-pm-skills) |
| **Guardrails, governance & risk** | 🏦 FINRA/SEC-compliant responsible AI design · 🏢 Governance aligned to NIST AI RMF | 🏦 [Model risk pack](https://github.com/vishalhabib99/retirement-answer-check/blob/main/docs/model-risk/README.md) (SR 26-2 + NIST AI 600-1) · 🏦 [Prompt-injection red team](https://github.com/vishalhabib99/retirement-answer-check#prompt-injection-can-a-draft-talk-the-checker-into-passing-it), before and after the fix · [`mcp-trust-check`](https://github.com/vishalhabib99/mcp-trust-check) release gate, policy, audit log, PII checks · 🏢 [Red-teamed handoff checks](https://github.com/vishalhabib99/agent-handoff-check#results) with a tamper-evident record of who handed what to whom |
| **Cost & pricing** | 🏢 Accuracy, cost and latency tuned per interaction type: latency roughly halved on low-stakes queries | 🏢 [Which model, and how to price it](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-09-ai-feature-unit-economics.md): verified model pricing, 4 routing options, per-seat economics |
| **Product decisions** | 0→1 strategy, launch gates, adoption and containment metrics | [PRD: Agent Outcome Trust Score](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/prds/2026-09-agent-outcome-trust-score.md), an evidence-first scorecard for deciding whether an agent is ready for production · [`/build-or-not`](https://github.com/vishalhabib99/ai-pm-skills) · [Agent Readiness Scorecard](https://vishalhabib99.github.io/agentic-product-playbook/) · [What I decided not to build](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-10-what-i-decided-not-to-build.md): 6 ideas and why each stopped · [Who owns trust for agent tools](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-10-who-owns-trust-for-agent-tools.md): where the money is, and what I'd build at a platform or a gateway |

</details>

## 🧱 Portfolio

**🏦 Fintech**
- 🛡️ [`retirement-answer-check`](https://github.com/vishalhabib99/retirement-answer-check): checks an AI's draft answer to a retirement-account question before a customer sees it, and decides SEND or REVIEW with an IRS or FINRA source for every flag.<br>
  Pattern rules alone let 5 of 15 blind wrong facts through; adding a fact-checking judge brought that to 0 of 25. Also: [contribution room calculator](https://vishalhabib99.github.io/retirement-answer-check/room/) · [model risk pack](https://github.com/vishalhabib99/retirement-answer-check/blob/main/docs/model-risk/README.md)

**🛒 Marketplaces**
- 🏷️ [`listing-claim-check`](https://github.com/vishalhabib99/listing-claim-check): checks an AI-written listing against the seller's own item specifics and decides PUBLISH or REVIEW. **[Try it →](https://vishalhabib99.github.io/listing-claim-check/)**<br>
  v0.1 failed its blind run and v0.2 passed a fresh one, then a [red team](https://github.com/vishalhabib99/listing-claim-check#results) got all 22 attacks through. Published as-is.
- 🧩 [eBay case study](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/case-studies/2026-09-ebay-marketplace-platform.md): the platform behind $300M+ in savings, and why clear contracts matter for AI agents too.

**🏢 SaaS & enterprise platforms**
- 🔗 [`agent-handoff-check`](https://github.com/vishalhabib99/agent-handoff-check): checks every agent-to-agent handoff against what the customer authorized and decides ACT, ESCALATE or BLOCK. **[Try it →](https://vishalhabib99.github.io/agent-handoff-check/)**<br>
  A red team got 3 unauthorized calls through; after one design change, a fresh blind run let 0 of 18 through and blocked 0 of 14 legitimate calls.
- 📡 [T-Mobile case study](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/case-studies/2026-09-tmobile-enterprise-agentic-platform.md): four architecture decisions behind the agentic platform (25M users, 60% containment) and what I'd do differently.
- 📊 [Which model, and how to price it](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-09-ai-feature-unit-economics.md): model cost is under 5% of the value delivered, so the real constraint is draft quality.

**🧰 Trust tooling for the tools AI agents call (MCP)**
- 🩺 [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor): **for MCP server maintainers who need to know whether an agent can actually use their tools.** Open an issue with your repo URL and a bot replies with a graded report, or add the [GitHub Action](https://github.com/vishalhabib99/mcp-doctor#github-action) and every pull request gets the safe fixes as one-click suggestions (new in v1.15). **[Scan your server →](https://github.com/vishalhabib99/mcp-doctor/issues/new?template=scan-request.yml)**<br>
  Finds [11,228 of 11,411 tools across 603 real servers](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/coverage.md), with every miss published. Scanning real servers surfaced [77 bugs in mcp-doctor itself](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/BUILD_LOG.md), all fixed ([postmortem](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/postmortem-69-bugs.md)). [What the first users taught me →](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/what-users-taught-me.md)<br>
  [A bet I made before knowing the answer](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/experiments/2026-09-scan-by-issue.md): at least 10 outside scan requests by Oct 27, or I stop promoting mcp-doctor. 3 so far (as of Oct 6), all from one maintainer I invited. The result gets posted here either way.
- 🧪 [`mcp-fuzz`](https://github.com/vishalhabib99/mcp-fuzz) checks that a live server fails cleanly · 🩻 [`mcp-reality-check`](https://github.com/vishalhabib99/mcp-reality-check) catches "successful" responses that aren't · 🛡️ [`mcp-trust-check`](https://github.com/vishalhabib99/mcp-trust-check) runs all three as one [GitHub Action](https://github.com/marketplace/actions/mcp-trust-check) that decides SHIP, FIX-FIRST or BLOCK.

<img src="https://raw.githubusercontent.com/vishalhabib99/mcp-doctor/main/docs/demo.png" alt="mcp-doctor scanning homeassistant-ai/ha-mcp: Quality 96% grade A, Security 98% grade A, 88 tools found, with per-tool OK and WARN lines" width="600">

**🧭 For AI product managers**
- 🧭 [`ai-pm-skills`](https://github.com/vishalhabib99/ai-pm-skills): Claude Code skills (`/build-or-not`, `/eval-plan`, `/agent-trust-review`), each tested against gates set before the first run. **[See real runs →](https://vishalhabib99.github.io/ai-pm-skills/)**
- 📋 [`agentic-product-playbook`](https://github.com/vishalhabib99/agentic-product-playbook): 7 ways AI agents fail in production, plus templates. **[3-minute Agent Readiness Scorecard →](https://vishalhabib99.github.io/agentic-product-playbook/)**
- 📄 [`ai-pm-portfolio`](https://github.com/vishalhabib99/ai-pm-portfolio): PRDs, prototypes and honestly reported evals, failures included.

## ✍️ Writing
- [My grader got every real answer right. Four red teams still broke it.](https://dev.to/vishalhabib99/my-grader-got-every-real-answer-right-four-red-teams-still-broke-it-632) (dev.to)
- [5 ways AI agents fail, and the checks I built in public](https://www.linkedin.com/feed/update/urn:li:share:7512673002552135680/): accuracy, safety, security, quality and evals, one number each (LinkedIn)
- [Building T-Mobile's First Enterprise Agentic AI Platform: 25M Users, 75% Adoption, and What I'd Do Differently](https://www.linkedin.com/pulse/building-t-mobiles-first-enterprise-agentic-ai-platform-vishal-habib-bftoc/) (LinkedIn)

<details><summary>More writing</summary><br>

- ["0 of 18 got through" isn't a launch. Here's the number that is.](https://dev.to/vishalhabib99/0-of-18-got-through-isnt-a-launch-heres-the-number-that-is-34p4) (dev.to)
- [My prompt-injection fix caught 0 of 20 attacks. The part I almost didn't build caught all of them.](https://dev.to/vishalhabib99/my-prompt-injection-fix-caught-0-of-20-attacks-the-part-i-almost-didnt-build-caught-all-of-them-oi0) (dev.to)
- [I set the pass bar before testing my Claude Code skills. The first run failed.](https://dev.to/vishalhabib99/i-set-the-pass-bar-before-testing-my-claude-code-skills-the-first-run-failed-1ef5) (dev.to)
- [My tools were rigorous. They were also hard to try.](https://www.linkedin.com/posts/vishal-habib_agenticai-mcp-aiproductmanagement-share-7510079742864334848-qohk/) — why mcp-doctor now runs with no install (LinkedIn)
- [I Built Three Tools to Audit MCP Servers for Agentic AI. Here's What They Found — and What I Learned Shipping Them.](https://www.linkedin.com/pulse/i-built-three-tools-audit-mcp-servers-agentic-ai-heres-vishal-habib-kmv3c/) (LinkedIn)
- [I built three tools to audit MCP servers. Each one found a bug in itself first.](https://dev.to/vishalhabib99/i-built-three-tools-to-audit-mcp-servers-each-one-found-a-bug-in-itself-first-5dlc) (dev.to)

</details>

## 💼 Career, by vertical

<details><summary>Vanguard · T-Mobile · eBay · earlier roles</summary><br>

- 🏦 **Fintech: Vanguard.** Leading product strategy for **Digital Advisor** and **Personal Advisor** ($6B+ LOB, 4M+ MAU) at the world's second-largest asset manager (~$12T AUM). Architecting the Agentic AI Digital Advisor from 0→1: LLM orchestration, autonomous agent workflows, model evaluation frameworks (correctness, groundedness, safety, latency) and FINRA/SEC-compliant responsible AI design. Also in fintech: launched **T-Mobile Money** (fee-free digital banking, high-yield savings) and, earlier, digital lending modernization at Axis Bank.
- 🏢 **SaaS & enterprise platforms: T-Mobile.** Product lead for T-Life, the flagship app ($3B+ LOB, 25M+ MAU); managed 3 PMs and a 40+ person cross-functional org. Launched one of the first autonomous enterprise Agentic AI platforms in US telecom: **75% adoption, 46% automation, 60% containment, 80% CSAT, 30% fewer support calls**. Built the IntentCX AI governance & model evaluation framework (aligned to NIST AI RMF), adopted org-wide by 3 additional teams. AI personalization on the T-Life home feed: **+27% engagement, +15% conversion** across 50+ A/B experiments a year.
- 🛒 **Marketplaces: eBay.** Drove **$300M+ in savings** and **+35% adoption** via marketplace platform modernization and API standardization across hundreds of engineering teams; monolith to microservices with 40% faster deploys and 99.9% availability on seller-facing APIs.
- 🩺 **Earlier, healthcare: Premera Blue Cross.** Billing and payment redesign that cut task completion time 25%.

</details>

<details><summary>Recognition</summary><br>

- **Patent filed:** sole inventor on a U.S. provisional patent application (No. 63/980,243, May 2026) for an agentic AI/ML orchestration and governance system: dynamic execution governance, non-transitive delegation, risk-aware orchestration, and verifiable compliance.
- **Top Product Leader, T-Mobile (2025)**, for building and launching the enterprise agentic AI platform.
- **Keynote speaker, T-Mobile Technology Innovation Summit (2025):** AI strategy keynote to 1,200+ attendees on scaling enterprise agentic AI platforms.

</details>

<details><summary>Education & certifications</summary><br>

- **Stanford Graduate School of Business:** Executive Program, Harnessing AI for Breakthrough Innovation and Strategic Impact (2026)
- MBA, Business Strategy and Marketing, Indiana University of Pennsylvania · MS, Information Technology Management, Campbellsville University
- Certifications: PMP · SAFe POPM · AWS Solutions Architect Associate · CSPO · PMI-PBA · Google AI Essentials

</details>

<details><summary>Why this portfolio exists, and what it doesn't cover</summary><br>

At work I build evals for AI agents: is the answer correct, grounded, safe and fast? These projects apply the same checks one layer down, to the tools an agent calls. `mcp-doctor` checks that a tool is documented well enough to use, `mcp-fuzz` checks that it fails safely and responds fast, and `mcp-reality-check` checks that its answers are true to what it did. `retirement-answer-check` and `listing-claim-check` check what the AI wrote against the source of truth the business already has. `agent-handoff-check` takes it up a level, to teams of agents handing work to each other: the source of truth is what the customer actually authorized.

Not covered, by design:
- **Semantic hallucination** ("is this answer actually true" in general): needs an LLM judge, which would break the deterministic, no-API-cost design the MCP tools share. (`retirement-answer-check` does add a judge, but only for narrow fact checks against IRS and FINRA sources, not open-ended truth.)
- **Live agent red-teaming**: `mcp-doctor`'s security score audits a tool's own code and description for injection risk, not whether a live agent can be manipulated at runtime.

</details>

## 📫 Reach me
[Email](mailto:vishalhabib99@gmail.com) · [LinkedIn](https://www.linkedin.com/in/vishal-habib/) · [Website](https://vishalhabib.netlify.app/) · [dev.to](https://dev.to/vishalhabib99)
