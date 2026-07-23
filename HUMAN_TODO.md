# HUMAN_TODO.md — Finish DR0 Setup (~20 min)

1. Install Zotero (https://zotero.org) → Settings → Advanced → enable "Allow
   other applications on this computer to communicate with Zotero" (local
   API).
2. Run `zotero-mcp setup` in a terminal and follow the prompts.
3. Merge `docs/mcp.zotero.snippet.json` into `.mcp.json` under `mcpServers`.
4. Optional: get a free Semantic Scholar API key
   (https://www.semanticscholar.org/product/api) and add it to `.mcp.json`:
   ```json
   "semantic-scholar": {
     "command": "uvx",
     "args": ["semantic-scholar-mcp"],
     "env": { "SEMANTIC_SCHOLAR_API_KEY": "..." }
   }
   ```
5. Create free browser accounts:
   - Ai2 Paperfinder — https://paperfinder.allen.ai
   - Ai2 ScholarQA
   - ResearchRabbit — https://researchrabbit.app (sync with Zotero)
   - NotebookLM
6. Start a fresh `claude` session in this repo, approve the project-scoped
   MCP servers when prompted, then run this smoke test:

   > Using the semantic-scholar tools, find 5 recent papers on explainable
   > AI in digital humanities; verify each exists; write the result to
   > runs/ as a mini-run following CLAUDE.md.

7. Review "Deviations" in SETUP_REPORT.md and resolve any that need human
   action (e.g. `papersflow` connectivity was unreachable at setup time —
   verify it resolves in your network before relying on it).
