# DR0 — Deep Research Station

A self-contained, project-scoped deep-research workstation for scholarship
across humanities, arts, theatre/scenography, digital humanities, philosophy,
and AI/XAI.

## Architecture (three layers)

1. **Retrieval** — MCP servers (`semantic-scholar`, `papersflow`, and later
   `zotero`) for academic literature, plus general web search for grey
   literature and non-English sources.
2. **Synthesis** — Claude Code skills/agents/commands vendored from Claude
   Scholar, adapted for humanities/arts research.
3. **Persistence** — `runs/` (per-research-run evidence trail) and `kb/`
   (durable, promoted knowledge notes).

See `CLAUDE.md` for the working protocol and `HUMAN_TODO.md` to finish setup.
