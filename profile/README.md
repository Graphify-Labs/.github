<p align="center">
  <a href="https://graphify.com"><img src="https://raw.githubusercontent.com/Graphify-Labs/graphify/v8/docs/logo.png" width="300" height="140" alt="Graphify"/></a>
</p>

# Graphify

**Understand your code — don't grep it.** We turn any folder of code, docs, PDFs, images, or video into a knowledge graph you *query, trace, and prove things about* instead of searching by hand.

[Website](https://graphify.com) · [graphify (open source)](https://github.com/Graphify-Labs/graphify) · [PyPI](https://pypi.org/project/graphifyy/) · [Discord](https://discord.gg/598Ad9zQZ) · [LinkedIn](https://www.linkedin.com/company/graphify-labs)

We ship two things, one idea: a **graph** of how your project actually fits together. The open-source tool builds that map on your machine for free. The enterprise platform builds a *smarter, verified* map — one that proves your changes are safe, remembers, learns, and runs entirely inside your own infrastructure.

---

## graphify — open source, fully local

Type `/graphify` in your AI coding assistant and it maps an entire project into a persistent knowledge graph. Code is parsed locally with tree-sitter (deterministic, no LLM, nothing leaves your machine); docs, PDFs, images, and video get a semantic pass through your assistant's model or a configured key. You get three files: an interactive `graph.html`, a plain-language `GRAPH_REPORT.md`, and a GraphRAG-ready `graph.json`.

- **A real graph, not a vector index.** No embeddings, no vector store. You *traverse* it — ask a question, trace the shortest path between two things, or explain one concept and its neighbours.
- **Code maps for free.** tree-sitter AST across ~40 languages resolves `calls` / `imports` / `inherits` edges with no API cost and no code leaving your machine.
- **An honest audit trail.** Every edge is tagged `EXTRACTED` (explicit in the source) or `INFERRED` (resolved by graphify) — you always know what was read vs derived.
- **Structure you wouldn't think to ask for.** *God nodes* surface what everything flows through; Leiden community detection groups the graph into labelled subsystems.

```bash
uv tool install graphifyy && graphify install     # register the skill with your assistant
/graphify .                                        # Claude Code, Cursor, Codex, Copilot, Gemini CLI…
```

Docs: [how it works](https://github.com/Graphify-Labs/graphify) — the extraction pipeline, community detection, and confidence scoring.

---

## Graphify Enterprise — the verified, on-prem platform

The open-source tool tells you how your code fits together. **Enterprise tells you whether a change is safe — without your code ever leaving your building.** It's the same graph, made trustworthy for teams shipping AI-written code.

- **Verified, not just reviewed.** Where a reviewer *guesses* a change looks fine, Graphify runs formal verification: it **proves** an edit behaves identically, or hands you the **exact input that breaks it — as a runnable test.** When it genuinely can't be sure, it says so. No false confidence.
- **Runs in your VPC — code never leaves.** On-prem by default: CPU-local graph, retrieval, memory, and verification. No source or chat logs in someone else's cloud. The privacy claims are true *by construction*, not by policy.
- **A grounded memory + fact-checker for your AI agents.** Over MCP, Cursor / Claude Code / Codex get provenance-carrying, honest-abstain answers — and can verify their own changes *before* you ever see the PR.
- **PR review + merge gate for teams.** Every pull request gets a structural review and a codebase-aware verification, posted as a check — with an enforceable gate.
- **It learns from you.** When a trusted maintainer says a finding is wrong, it remembers and suppresses it going forward — and always cites *why*. Preferences are advisory; correctness always wins.
- **Enterprise-ready.** SSO, project scoping, a tamper-evident audit trail, and secret redaction before any model call.

> **The one-liner:** every other AI code reviewer guesses. Ours proves — and it runs in your house.

---

## How they fit: open core

| | **graphify** (free) | **Enterprise** |
|---|---|---|
| The graph | ✅ built locally | ✅ richer-typed, deeper resolution, cross-repo |
| Query & trace | ✅ | ✅ tuned for agents |
| **Formal verification** | — | ✅ prove-or-counterexample |
| **Grounded memory + fact-check** | — | ✅ over MCP, with provenance |
| **Team PR review + merge gate** | — | ✅ |
| **On-prem / SSO / RBAC / audit** | — | ✅ |
| Deployment | your machine | your VPC (or our cloud — same app) |

Start free on the open-source tool. Upgrade when you need to *prove* your code is right, share across a team, and keep everything inside your own infrastructure.

**Talk to us:** [founders@graphify.com](mailto:founders@graphify.com) · [graphify.com](https://graphify.com) · [Discord](https://discord.gg/598Ad9zQZ)

_We think you're gonna like it here._
