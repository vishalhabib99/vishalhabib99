# Hi, I'm Vishal 👋

**Lead AI Product Manager & Builder — Agentic AI** · leading the 0→1 Agentic AI Digital Advisor at **Vanguard**, now in limited client beta · ex-T-Mobile, eBay · Stanford GSB

10+ years launching 0→1 products and scaling platforms 1→100 across **fintech, SaaS, enterprise platforms, marketplaces & e-commerce**: **$9B+ in revenue platforms, 29M+ MAU, $300M+ in cost savings**. On the side I build the eval and trust tooling I wish every AI team had, and publish the failures with the passes.

**▶️ 78-second walkthrough** (AI-narrated):





https://github.com/user-attachments/assets/66bbb79d-57c6-477d-90c6-b671f763c344





## 🩺 Flagship: mcp-doctor, evals & guardrails for AI agents and the MCP tools they call

[`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor) answers two questions: **can an agent actually use your server, and can you trust what the agent does with it?** **[Scan your server →](https://github.com/vishalhabib99/mcp-doctor/issues/new?template=scan-request.yml)**

- 🔍 **Scan:** open an issue with your repo URL, get a report that leads with what will break an agent, then quality and security ([example](https://github.com/vishalhabib99/mcp-doctor/issues/9)), no install. Or run it in CI with the [GitHub Action](https://github.com/vishalhabib99/mcp-doctor#github-action), or as a [plugin for Claude Code, Codex or Cursor](https://github.com/vishalhabib99/mcp-doctor#plugin-for-claude-code-codex-and-cursor).
- 🛡️ **[`guard`](https://github.com/vishalhabib99/mcp-doctor#guard--catch-tool-calls-that-report-success-but-didnt-work):** an unguarded agent read a web page, then planted a `.git` hook and leaked a `.env` token; guard stopped both. One line puts an MCP server or a coding agent's built-in tools (Claude Code, Codex, Cursor) behind a live check for likely prompt-injection leaks and "successes" that didn't happen.
- 🧪 **[`fuzz` and `verdict`](https://github.com/vishalhabib99/mcp-doctor#fuzz-and-verdict--launch-the-server-and-check-it):** launches a server and checks it fails cleanly, `--truth` checks a "success" is a real answer, and `verdict` turns it all into SHIP, FIX-FIRST or BLOCK.
- 🤖 **[`fix-upstream`](https://github.com/vishalhabib99/mcp-doctor/blob/main/plugin/skills/fix-upstream/SKILL.md):** an agent that turns a finding into a tested PR I approve first. Replayed on 15 fixes maintainers had already merged, it made the same edits; its first real PR [merged at AMD's intellikit](https://github.com/AMDResearch/intellikit/pull/202) in 41 minutes ([write-up](https://dev.to/vishalhabib99/before-i-let-an-agent-open-prs-on-strangers-repos-i-made-it-earn-it-27od)).
- 📊 **[Leaderboard](https://vishalhabib99.github.io/mcp-doctor/) and [census](https://github.com/vishalhabib99/mcp-doctor/tree/main/census/2026-10):** 24 public servers checked; 3,923 servers and 147,646 tools scanned.

**Where it stands:** [`jupyter-mcp-server`](https://github.com/datalayer/jupyter-mcp-server/pull/488) became the first outside CI user on Oct 16, after its maintainer asked for the Action. It finds [15,755 of 15,977 tools across 805 real servers](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/coverage.md), every miss published; scanning real servers surfaced [133 bugs in mcp-doctor itself](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/BUILD_LOG.md), all fixed ([postmortem](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/postmortem-69-bugs.md)).

**[A bet I made before knowing the answer](https://github.com/vishalhabib99/mcp-doctor/blob/main/docs/experiments/2026-09-scan-by-issue.md):** at least 10 outside scan requests by Oct 27. **4 so far** (as of Oct 23), from two maintainers I invited. The Oct 27 number goes here, hit or miss.

<img src="https://raw.githubusercontent.com/vishalhabib99/mcp-doctor/main/docs/demo.svg" alt="Animated mcp-doctor demo: a scan that opens with 1 finding that will break an agent, a release verdict (BLOCK, then SHIP), and guard catching a call that reported success without writing the file" width="700">

## ✅ Proof from outside
None of these maintainers work with me.

> "Thank you for the exact tools/list results and for explaining the effect on clients that use annotations for approval." ([`codebase-memory-mcp` maintainer](https://github.com/DeusData/codebase-memory-mcp/issues/2118#issuecomment-5609248676))

- **65 fixes landed in 62 outside repos**, merged by their own maintainers. Biggest: [`langflow`](https://github.com/langflow-ai/langflow/pull/15565) (156K★, built on [my PR](https://github.com/langflow-ai/langflow/pull/15523), me as co-author) · [`mcp-for-blender`](https://github.com/ahujasid/mcp-for-blender/commit/250c00deca845c04df8c72e5b324291ee4969054) (32.2K★, me as commit author) · [`DeepCode`](https://github.com/HKUDS/DeepCode/pull/261) (16.8K★, drafted by my fix-upstream agent) · [`davinci-resolve-mcp`](https://github.com/samuelgursky/davinci-resolve-mcp/pull/274) (3.7K★, [shipped in v4.8.29](https://github.com/samuelgursky/davinci-resolve-mcp/releases/tag/v4.8.29) with credit) · [`jupyter-mcp-server`](https://github.com/datalayer/jupyter-mcp-server/pull/480) (1.3K★, [2 fixes](https://github.com/datalayer/jupyter-mcp-server/pull/482), then it [added the mcp-doctor Action](https://github.com/datalayer/jupyter-mcp-server/pull/488))
  <details><summary>The other 59 merged fixes</summary>

    [`ha-mcp`](https://github.com/homeassistant-ai/ha-mcp/pull/2327) (5.2K★) · [`dbhub`](https://github.com/bytebase/dbhub/pull/470) (3.7K★) · [`google_workspace_mcp`](https://github.com/taylorwilsdon/google_workspace_mcp/pull/1230) (3.4K★) · [`shadcn-ui-mcp-server`](https://github.com/Jpisnice/shadcn-ui-mcp-server/pull/62) (3.1K★) · [`stealth-browser-mcp`](https://github.com/vibheksoni/stealth-browser-mcp/pull/36) (3.3K★) · [`zennotes`](https://github.com/ZenNotes/zennotes/pull/929) (2.6K★) · [`docmd`](https://github.com/docmd-io/docmd/pull/260) (2.5K★) · [`kordoc`](https://github.com/chrisryugj/kordoc/pull/147) (2.7K★) · [`llm-wiki-compiler`](https://github.com/atomicstrata/llm-wiki-compiler/pull/270) (2.2K★) · [`telegram-mcp`](https://github.com/chigwell/telegram-mcp/pull/266) (1.9K★) · [`chunkhound`](https://github.com/chunkhound/chunkhound/pull/437) (1.5K★) · [`garmin_mcp`](https://github.com/Taxuspt/garmin_mcp/pull/443) (1.4K★) · [`solomd`](https://github.com/zhitongblog/solomd/pull/407) (1.4K★) · [`rhinomcp`](https://github.com/jingcheng-chen/rhinomcp/pull/62) (1.2K★) · [`Qiskit/mcp-servers`](https://github.com/Qiskit/mcp-servers/pull/225) (IBM) · [`aimock`](https://github.com/CopilotKit/aimock/pull/529) (985★, 2 fixes: [#529](https://github.com/CopilotKit/aimock/pull/529), [#533](https://github.com/CopilotKit/aimock/pull/533)) · [`retentioneering-tools`](https://github.com/retentioneering/retentioneering-tools/pull/179) (938★) · [`AgentChat`](https://github.com/Shy2593666979/AgentChat/pull/55) (924★) · [`Android-MCP`](https://github.com/CursorTouch/Android-MCP/pull/36) (905★) · [`memorix`](https://github.com/AVIDS2/memorix/pull/329) (864★) · [`jadx-mcp-server`](https://github.com/zinja-coder/jadx-mcp-server/pull/69) (810★) · [`maverick-mcp`](https://github.com/wshobson/maverick-mcp/pull/318) (710★) · [`tokensave`](https://github.com/aovestdipaperino/tokensave/pull/713) (677★) · [`MisakaNet`](https://github.com/Ikalus1988/MisakaNet/pull/3515) (543★) · [`ignidash`](https://github.com/schelskedevco/ignidash/pull/69) (292★) · [`llm-context.py`](https://github.com/cyberchitta/llm-context.py/pull/29) · [`unsplash-mcp-server`](https://github.com/hellokaton/unsplash-mcp-server/pull/18) · [`jdocmunch-mcp`](https://github.com/jgravelle/jdocmunch-mcp/pull/163) · [`MacOS-MCP`](https://github.com/CursorTouch/MacOS-MCP/pull/69) · [`MCP-PostgreSQL-Ops`](https://github.com/call518/MCP-PostgreSQL-Ops/pull/71) · [`LivePilot`](https://github.com/dreamrec/LivePilot/pull/99) · [`cognicore-env`](https://github.com/cognicore-dev/cognicore-env/pull/152) · [`chiasmus`](https://github.com/yogthos/chiasmus/pull/55) · [`open-meteo-mcp`](https://github.com/cmer81/open-meteo-mcp/pull/81) · [`devglobe`](https://github.com/sajeetharan/devglobe/pull/463) · [`osm-mcp-server`](https://github.com/yuiseki/osm-mcp-server/pull/43) · [`concord-mcp`](https://github.com/Get-Concord-AI/concord-mcp/pull/185) · [`taskdog`](https://github.com/Kohei-Wada/taskdog/pull/1253) · [`knowledge-rag`](https://github.com/lyonzin/knowledge-rag/pull/236) · [`mcp-jenkins`](https://github.com/lanbaoshen/mcp-jenkins/pull/106) · [`palinode`](https://github.com/phasespace-labs/palinode/pull/240) · [`ai-toolbox`](https://github.com/desplega-ai/ai-toolbox/pull/38) · [`geml`](https://github.com/geml-spec/geml/pull/42) · [`CONTINUUM`](https://github.com/Cyrax321/CONTINUUM/pull/1643) · [`phone-mcp`](https://github.com/hao-cyber/phone-mcp/pull/14) · [`mcp-server-for-revit-python`](https://github.com/mcp-servers-for-revit/mcp-server-for-revit-python/pull/65) · [`adeu`](https://github.com/dealfluence/adeu/pull/163) · [`django-orm-lens`](https://github.com/FROWNINGdev/django-orm-lens/pull/138) (2 fixes: [#138](https://github.com/FROWNINGdev/django-orm-lens/pull/138), [#161](https://github.com/FROWNINGdev/django-orm-lens/pull/161)) · [`srclight`](https://github.com/srclight/srclight/pull/46) · [`intellikit`](https://github.com/AMDResearch/intellikit/pull/202) · [`eval-view`](https://github.com/hidai25/eval-view/pull/273) · [`people-context`](https://github.com/JinyangWang27/people-context/pull/193) · [`django-admin-mcp`](https://github.com/7tg/django-admin-mcp/pull/127) · [`lsp-mcp-server`](https://github.com/ProfessioneIT/lsp-mcp-server/pull/15) · [`EDA_MCP`](https://github.com/SiliCAD/EDA_MCP/pull/68) · [`ctxvault`](https://github.com/Filippo-Venturini/ctxvault/pull/37) · [`dokimi`](https://github.com/intel/dokimi/pull/243) (Intel)

    </details>
- Also: [`codebase-memory-mcp`](https://github.com/DeusData/codebase-memory-mcp/issues/2118) (47.4K★) relabeled all 12 tools I flagged; [`excel-mcp-server`](https://github.com/haris-musa/excel-mcp-server/releases/tag/v1.0.0) (4.3K★) reimplemented both my fixes, credited.

## 🧱 More repos, by vertical

The common thread: AI output is only worth shipping when it can be checked against a source of truth, whether that's an IRS rule, a tool's own schema, or a platform's API contract.

**🏦 Fintech**
- 🛡️ [`fin-assist`](https://github.com/vishalhabib99/fin-assist): catches stale and wrong money figures in an AI agent's answer before a customer sees it. It checks each figure against 102 dated, sourced IRS, SSA and Medicare figures and corrects stale ones; on retirement answers it also flags advice and promissory language, citing IRS or FINRA.<br>
  Blind-tested on eight sets written by agents that never saw the code, with every miss published; a fact-checking judge took wrong facts sent from 5 of 15 to 0 of 25. Its registry caught a real tax-bracket bug in [`ignidash`](https://github.com/schelskedevco/ignidash/pull/69), an open-source retirement planner: the maintainer merged my fix. `pip install fin-assist` · [paste an AI answer to check it](https://vishalhabib99.github.io/fin-assist/check/) · [model risk pack](https://github.com/vishalhabib99/fin-assist/blob/main/docs/model-risk/README.md)

**🛒 Marketplaces & E-commerce**
- 🏷️ [`listing-claim-check`](https://github.com/vishalhabib99/listing-claim-check): checks an AI-written listing against the seller's own item specifics and decides PUBLISH or REVIEW. **[Try it →](https://vishalhabib99.github.io/listing-claim-check/)**<br>
  v0.1 failed its blind run and v0.2 passed a fresh one, then a [red team](https://github.com/vishalhabib99/listing-claim-check#results) got all 22 attacks through, published as-is.
- 🧩 [eBay case study](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/case-studies/2026-09-ebay-marketplace-platform.md): the platform behind $300M+ in savings, and why clear contracts matter for agents.

**🏢 SaaS & enterprise platforms**
- 🔗 [`agent-handoff-check`](https://github.com/vishalhabib99/agent-handoff-check): checks every agent-to-agent handoff against what the customer authorized and decides ACT, ESCALATE or BLOCK. **[Try it →](https://vishalhabib99.github.io/agent-handoff-check/)**<br>
  A red team got 3 unauthorized calls through; after one design change, a fresh blind run let 0 of 18 through and blocked 0 of 14 legitimate calls.
- 📡 [T-Mobile case study](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/case-studies/2026-09-tmobile-enterprise-agentic-platform.md): four architecture decisions behind the agentic platform (25M users, 60% containment) and what I'd do differently.

**🧭 For AI product managers**
- 🧭 [`ai-pm-skills`](https://github.com/vishalhabib99/ai-pm-skills): Claude Code skills (`/build-or-not`, `/eval-plan`, `/agent-trust-review`), each tested against gates set before the first run. **[See real runs →](https://vishalhabib99.github.io/ai-pm-skills/)**
- 📋 [`agentic-product-playbook`](https://github.com/vishalhabib99/agentic-product-playbook): 7 ways AI agents fail in production, plus templates. **[3-minute Agent Readiness Scorecard →](https://vishalhabib99.github.io/agentic-product-playbook/)**
- 🔎 [What 129 maintainer replies told me](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/research/2026-10-what-maintainers-told-me.md): user research from 118 outside PRs. Maintainers answer within a day or never, and adoption hinged on a security review.
- 📄 [`ai-pm-portfolio`](https://github.com/vishalhabib99/ai-pm-portfolio): PRDs, prototypes and honestly reported evals, failures included.

<details><summary><b>🗺️ Where my work sits in the AI stack</b>: shipped at work vs. built in the open</summary><br>

| Layer | Shipped at work | Built in the open |
|---|---|---|
| **Apps & human-in-the-loop** | 🏦 Vanguard Digital Advisor experience · 🏢 T-Mobile agentic support platform | 🏦 [Contribution room calculator](https://vishalhabib99.github.io/fin-assist/room/) · 🏦 [Human review queue](https://github.com/vishalhabib99/fin-assist#human-review-queue-is-the-review-itself-working) · 🛒 [Listing checker demo](https://vishalhabib99.github.io/listing-claim-check/) |
| **Agents & orchestration** | 🏦 Agentic AI Digital Advisor (0→1) · 🏢 Autonomous enterprise agent platform | [`GuardedSession`](https://github.com/vishalhabib99/mcp-doctor#fuzz-and-verdict--launch-the-server-and-check-it): ACT, ESCALATE or BLOCK on each live tool call · 🏢 [`agent-handoff-check`](https://github.com/vishalhabib99/agent-handoff-check): authority can only narrow across handoffs |
| **Tools & APIs (MCP)** | 🛒 eBay API standardization across hundreds of teams | [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor) and its [`fuzz`](https://github.com/vishalhabib99/mcp-doctor#fuzz-and-verdict--launch-the-server-and-check-it) · 🏦 `check_answer` and `contribution_room` MCP tools · 🛒 `check_listing` MCP tool |
| **Evals & quality** | 🏦 Model evals for correctness, groundedness, safety, latency · 🏢 IntentCX evaluation framework | 🏦 [Blind, pre-registered evals](https://github.com/vishalhabib99/fin-assist#results) · 🛒 [Failed blind run, fresh pass, then broken by a red team](https://github.com/vishalhabib99/listing-claim-check#results) · 🏢 [RAG prototype on blind tickets](https://github.com/vishalhabib99/ai-pm-portfolio/tree/main/prototypes/ticket-triage-rag#tried-retry-retrieval-when-the-match-is-ambiguous): accuracy fell from 60% to 38% · ⚛️ [Quantum circuit grader](https://github.com/vishalhabib99/circuit-claim-check): right on all 90 real answers, yet 4 red teams got 27 wrong circuits passed ([write-up](https://dev.to/vishalhabib99/my-grader-got-every-real-answer-right-four-red-teams-still-broke-it-632)) · [`/eval-plan`](https://github.com/vishalhabib99/ai-pm-skills) |
| **Guardrails, governance & risk** | 🏦 FINRA/SEC-compliant responsible AI design · 🏢 Governance aligned to NIST AI RMF | 🏦 [Model risk pack](https://github.com/vishalhabib99/fin-assist/blob/main/docs/model-risk/README.md) (SR 26-2 + NIST AI 600-1) · 🏦 [Prompt-injection red team](https://github.com/vishalhabib99/fin-assist#prompt-injection-can-a-draft-talk-the-checker-into-passing-it), before and after the fix · [`mcp-doctor verdict`](https://github.com/vishalhabib99/mcp-doctor#fuzz-and-verdict--launch-the-server-and-check-it) release gate · [`guard`](https://github.com/vishalhabib99/mcp-doctor#guard-for-coding-agents-claude-code-hooks): holds secret leaks and `.git`-hook plants in coding agents · 🏢 [Red-teamed handoff checks](https://github.com/vishalhabib99/agent-handoff-check#results) |
| **Cost & pricing** | 🏢 Accuracy, cost and latency tuned per interaction type | 🏢 [Which model, and how to price it](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-09-ai-feature-unit-economics.md) |
| **Product decisions** | 0→1 strategy, launch gates, adoption and containment metrics | [PRD: Agent Outcome Trust Score](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/prds/2026-09-agent-outcome-trust-score.md) · [`/build-or-not`](https://github.com/vishalhabib99/ai-pm-skills) · [Agent Readiness Scorecard](https://vishalhabib99.github.io/agentic-product-playbook/) · [What I decided not to build](https://github.com/vishalhabib99/ai-pm-portfolio/blob/main/memos/2026-10-what-i-decided-not-to-build.md) |

</details>

## ✍️ Writing
- [Before I let an agent open PRs on strangers' repos, I made it earn it](https://dev.to/vishalhabib99/before-i-let-an-agent-open-prs-on-strangers-repos-i-made-it-earn-it-27od): it had to reproduce my past merged fixes first (dev.to)
- [I scanned 3,923 MCP servers. 1 in 4 tools has an undocumented parameter.](https://dev.to/vishalhabib99/i-scanned-3923-mcp-servers-1-in-4-tools-leaves-the-model-guessing-1n99): public servers with 20+ stars, 147,646 tools (dev.to)
- [Building T-Mobile's First Enterprise Agentic AI Platform: 25M Users, 75% Adoption, and What I'd Do Differently](https://www.linkedin.com/pulse/building-t-mobiles-first-enterprise-agentic-ai-platform-vishal-habib-bftoc/) (LinkedIn)

## 💼 Career, by vertical

<details><summary>Vanguard · T-Mobile · eBay · earlier roles</summary><br>

- 🏦 **Fintech: Vanguard.** Product strategy for **Digital Advisor** and **Personal Advisor** ($6B+ LOB, 4M+ MAU) at the world's second-largest asset manager (~$12T AUM). Architecting the Agentic AI Digital Advisor from 0→1, now in limited client beta (7+ use cases, launch gates met): LLM orchestration, agent workflows, model evals and FINRA/SEC-compliant responsible AI. Also launched **T-Mobile Money** and, earlier, digital lending modernization at Axis Bank.
- 🏢 **SaaS & enterprise platforms: T-Mobile.** Product lead for T-Life, the flagship app ($3B+ LOB, 25M+ MAU); mentored 3 PMs and led a 40+ person org. Launched one of the first autonomous enterprise Agentic AI platforms in US telecom: **75% adoption, 60% containment, 80% CSAT, 30% fewer support calls**. Built the IntentCX AI governance and eval framework (NIST AI RMF), adopted by 3 more teams. AI personalization: **+27% engagement, +15% conversion**.
- 🛒 **Marketplaces & E-commerce: eBay.** Drove **$300M+ in savings** and **+35% adoption** through platform modernization and API standardization across hundreds of teams; 40% faster deploys, 99.9% availability on seller APIs.
- 🩺 **Earlier, healthcare: Premera Blue Cross.** Billing and payment redesign that cut task completion time 25%.

</details>

<details><summary>Recognition</summary><br>

- **Vanguard AI Summit (2026):** built and presented the AI Agents Evaluations & Guardrails Framework, now adopted by 6 Vanguard orgs.
- **Patent filed:** sole inventor on a U.S. provisional patent application (No. 63/980,243, May 2026) for agentic AI orchestration and governance.
- **Top Product Leader, T-Mobile (2025)**, for building and launching the enterprise agentic AI platform.
- **Keynote speaker, T-Mobile Technology Innovation Summit (2025):** AI strategy keynote to 1,200+ attendees.

</details>

<details><summary>Education & certifications</summary><br>

- **Stanford Graduate School of Business:** Executive Program, Harnessing AI for Breakthrough Innovation and Strategic Impact (2026)
- MBA, Business Strategy and Marketing, Indiana University of Pennsylvania · MS, Information Technology Management, Campbellsville University
- Certifications: PMP · SAFe POPM · AWS Solutions Architect Associate · CSPO · PMI-PBA · Google AI Essentials

</details>

<details><summary>What this portfolio doesn't cover</summary><br>

- **Semantic hallucination** in general needs a judge model; only `fin-assist` uses one, for IRS and FINRA fact checks.
- **Live agent red-teaming**: `guard` catches leaks live, but nothing here attacks an agent to find new holes.

</details>

## 📫 Reach me
[Email](mailto:vishalhabib99@gmail.com) · [LinkedIn](https://www.linkedin.com/in/vishal-habib/) · [Website](https://vishalhabib.netlify.app/) · [dev.to](https://dev.to/vishalhabib99) · [Book 1:1 time](https://topmate.io/vishal_habib21)
