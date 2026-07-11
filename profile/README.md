<p align="center">
  <a href="https://graphifylabs.ai"><img src="https://raw.githubusercontent.com/Graphify-Labs/graphify/v8/docs/logo.png" width="300" height="140" alt="Graphify"/></a>
</p>

<p align="center">
  <b>Turn any folder of code, docs, PDFs, images, or video into a knowledge graph you query instead of grep.</b>
</p>

<p align="center">
  <a href="https://graphifylabs.ai">Website</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Graphify-Labs/graphify">graphify (open source)</a>
  &nbsp;·&nbsp;
  <a href="https://pypi.org/project/graphifyy/">PyPI</a>
  &nbsp;·&nbsp;
  <a href="https://discord.gg/598Ad9zQZ">Discord</a>
  &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/company/graphify-labs">LinkedIn</a>
</p>

---

We build **graphify**: type `/graphify` in your AI coding assistant and it maps an entire project into a persistent **knowledge graph** you can query, trace, and explain rather than grepping through files. Code is parsed locally with tree-sitter (deterministic, no LLM, nothing leaves your machine); docs, PDFs, images, and video get a semantic pass through your assistant's model or a configured API key. The result is three files: an interactive `graph.html`, a plain-language `GRAPH_REPORT.md`, and a GraphRAG-ready `graph.json`.

## Why graphify

- **A real graph, not a vector index.** No embeddings, no vector store. You traverse it: ask a question, trace the shortest path between two things, or explain one concept and its neighbours.
- **Code maps for free, fully local.** tree-sitter AST across ~40 languages resolves `calls` / `imports` / `inherits` edges with no API cost and no code leaving your machine.
- **An honest audit trail.** Every edge is tagged `EXTRACTED` (explicit in the source) or `INFERRED` (resolved by graphify), so you can tell what was read from what was derived.
- **Structure you would not think to ask for.** God nodes surface what everything flows through; Leiden community detection groups the graph into subsystems with plain labels.

## Start here

- **Install:** `uv tool install graphifyy` then `graphify install` to register the skill with your assistant.
- **Run it:** `/graphify .` in Claude Code, Cursor, Codex, Gemini CLI, GitHub Copilot, and more.
- **Read the docs:** [github.com/Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify)
- **See how it works:** the extraction pipeline, community detection, and confidence scoring in [docs/how-it-works.md](https://github.com/Graphify-Labs/graphify/blob/v8/docs/how-it-works.md).
- **Say hi:** [Discord](https://discord.gg/598Ad9zQZ).
