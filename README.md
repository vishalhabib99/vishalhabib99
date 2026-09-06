# Hi, I'm Vishal 👋

**Product Leader — Agentic AI, AI/ML-Powered Customer Experiences & Platform Products**

AI-native product leader with 10+ years defining strategy, vision, roadmap, and launching 0-to-1 products and 1-to-100 platforms across fintech, wealth management, telecom, retail, ecommerce, and healthcare — spanning B2B, B2C, and B2B2C.

## 💼 Currently
Leading product strategy for **Digital Advisor** and **Personal Advisor** at **Vanguard** ($6B+ LOB, 4M+ MAU) — architecting the next-generation Agentic AI Digital Advisor from 0-to-1, including model evaluation frameworks (correctness, groundedness, safety, latency) and FINRA/SEC-compliant responsible AI design.

## 🚀 Selected work
- **Vanguard** — Agentic AI Digital Advisor (0→1): LLM orchestration, autonomous agent workflows, personalized financial guidance at scale, with regulatory guardrails and model governance.
- **T-Mobile** — Launched one of the first autonomous enterprise Agentic AI platforms in US telecom: **75% adoption, 46% automation, 60% containment, 80% CSAT, 30% fewer support calls**. Built the IntentCX AI governance & model evaluation framework (aligned to NIST AI RMF), adopted org-wide by 3 additional teams.
- **eBay** — Drove **$300M+ in savings** via marketplace platform modernization and API standardization across hundreds of engineering teams.

## 🎓 Background
Stanford University Graduate School of Business · Google AI certifications (AI Essentials, Responsible AI, Prompting, AI Tools for Productivity)

## 🧱 Portfolio
- 📄 [`ai-pm-portfolio`](https://github.com/vishalhabib99/ai-pm-portfolio) — PRDs, working prototypes, and honestly-reported evals (including failures, not just wins)
- 🩺 [`mcp-doctor`](https://github.com/vishalhabib99/mcp-doctor) — static-analysis CLI that audits MCP server implementations for the things that break an agent calling them (`pip install mcp-server-lint`, or a GitHub Action). Dogfooded against 33+ real MCP servers in the wild across Python, TypeScript, and Go — up to 50k★, including GitHub's own official `github-mcp-server` and HashiCorp's `terraform-mcp-server` — found and fixed 27 genuine bugs, verified against each repo before/after. One fix led to a [merged PR](https://github.com/homeassistant-ai/ha-mcp/pull/2327) into `ha-mcp` (4.5K★, active); a separate clean pass surfaced a real doc-coverage gap [filed upstream](https://github.com/haris-musa/excel-mcp-server/issues/158) in `excel-mcp-server` (4.1K★, active).
- 🧪 [`mcp-fuzz`](https://github.com/vishalhabib99/mcp-fuzz) — mcp-doctor's companion (`pip install mcp-runtime-check`): instead of reading source, it launches a real MCP server and calls its tools with inputs derived from their own JSON schema, checking whether the server fails cleanly (a structured error) or crashes/hangs on missing or wrong-typed input. 17+ real-world passes so far, including Ant Design's official `mcp-server-chart` (4.3K★) — all 27 tools crash instead of erroring cleanly on realistic bad input, [filed upstream](https://github.com/antvis/mcp-server-chart/issues/323) — and a clean pass on `context7` (61K★). Also found and fixed a real classification bug in mcp-fuzz itself (a well-formed server error response was being scored as a crash); a first, over-broad fix attempt would have silently invalidated the `mcp-server-chart` finding above, caught by re-verifying both repos before shipping the real fix as v0.1.2.
- 🩻 [`mcp-reality-check`](https://github.com/vishalhabib99/mcp-reality-check) — completes the trilogy (`pip install mcp-reality-check`): mcp-doctor asks *is it documented*, mcp-fuzz asks *does it fail safely*, this asks *does it actually work*. Calls each tool once with a realistic (not placeholder) input and checks the response for a refusal disguised as success ("I don't have access to..." wrapped in `isError: false`), empty content on a claimed success, and violations of a tool's own declared output schema — all fully deterministic, no LLM judge, no API key, no per-call cost. 5 real-world passes so far, all clean.

## 📫 Reach me
- Website: [vishalhabib.netlify.app](https://vishalhabib.netlify.app/)
- LinkedIn: [in/vishal-habib](https://www.linkedin.com/in/vishal-habib/)
- GitHub: [@vishalhabib99](https://github.com/vishalhabib99)
