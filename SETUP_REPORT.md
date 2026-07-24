# SETUP_REPORT.md — DR0 Autonomous Setup

## Versions (Phase 0)

| Tool | Version |
|---|---|
| git | 2.43.0 |
| node | v22.22.2 |
| uv | 0.8.17 |
| uvx | 0.8.17 |
| claude | 2.1.218 (Claude Code) |

## What was created

- **Phase 1:** `.claude/{skills,agents,commands}`, `runs/`, `sources/{pdfs,notes}`,
  `kb/`, `docs/`, `.gitignore`, `README.md`.
- **Phase 2:** `.mcp.json` (papersflow HTTP + semantic-scholar uvx server),
  `docs/mcp.zotero.snippet.json` (deferred zotero entry).
- **Phase 3:** Vendored Claude Scholar skills/agents/commands (see below).
- **Phase 4:** `zotero-mcp-server[semantic]` installed via `uv tool install`
  (user-level, the one permitted exception). Binary verified functional.
- **Phase 5:** `CLAUDE.md` — station constitution / research protocol.
- **Phase 6:** `HUMAN_TODO.md` — remaining human-only setup steps.

## Vendored from Claude Scholar

- Source: https://github.com/Galaxy-Dawn/claude-scholar (MIT, `main`)
- Vendored commit: `2f7766fd541a723d4ddc6230b3277f948d61b093`
- Files copied: 38
- Copied:
  - `skills/research-ideation`, `skills/citation-verification`,
    `skills/writing-anti-ai`, `skills/paper-self-review`,
    `skills/planning-with-files` → `.claude/skills/`
  - `agents/literature-reviewer.md` → `.claude/agents/`
  - `commands/research-init.md`, `commands/zotero-review.md`,
    `commands/zotero-notes.md` → `.claude/commands/`
  - `LICENSE` → `docs/LICENSE-claude-scholar`
- Skipped (not found upstream, per skip-and-log): `skills/scientific-writing`
  (no skill by this exact name in the upstream repo).
- De-conflict pass: `citation-verification/SKILL.md` frontmatter referenced
  the un-vendored `ml-paper-writing` skill; description rewritten to be
  discipline-neutral (humanities/arts scope). All other vendored SKILL.md
  frontmatter was already discipline-neutral — no changes needed.
- Not copied (explicitly excluded per mission): hooks, rules, CLAUDE.md,
  settings templates, ML/experiment/Kaggle/Nature/Obsidian skills, and any
  other non-whitelisted files.

## Connectivity checks (Phase 2)

- `papersflow` (`https://doxa.papersflow.ai/mcp`): `curl` returned HTTP code
  `000` (no connection within 10s timeout) from this sandbox's network. Not
  retried further per spec (single attempt). This does not block setup —
  the server activates on approval in a real session; flagged as a
  deviation below for the user to verify from their own network.
- `semantic-scholar` (`uvx semantic-scholar-mcp --help`): resolved and ran
  successfully, initializing the MCP server (24 tools loaded); uvx cache
  warmed. Exit clean.
- Project-scoped MCP servers activate on the next `claude` session in this
  repo; the user must approve them when prompted.

## Zotero MCP (Phase 4)

- `uv tool install "zotero-mcp-server[semantic]"` succeeded; installed
  executables `zotero-cli`, `zotero-mcp` (v0.6.2).
- `zotero-mcp --help` confirmed functional.
- No `.mcp.json` entry added yet (would fail without local Zotero running).
  Snippet staged at `docs/mcp.zotero.snippet.json`. Remaining Zotero setup
  (install app, enable local API, `zotero-mcp setup`, merge snippet) is in
  `HUMAN_TODO.md`.

## Deviations

1. `skills/scientific-writing` does not exist in the vendored upstream repo
   under that exact name — skipped, no substitute searched for, per
   Prime Directive 4.
2. `papersflow` MCP endpoint was unreachable (HTTP `000`) from this sandbox
   during the connectivity check. Likely a sandboxed-network artifact, not
   necessarily a real outage — user should verify connectivity from their
   own machine before relying on it; if it truly is down, this is an
   upstream-service issue outside this repo's control.

## Acceptance criteria check

- [x] `.mcp.json` valid, two servers, zero user-scope config written (except
      the one permitted `uv tool install` binary).
- [x] `.claude/` contains only whitelisted, de-conflicted items; attribution
      preserved (`docs/LICENSE-claude-scholar`).
- [x] `CLAUDE.md`, `README.md`, `HUMAN_TODO.md`, `SETUP_REPORT.md`,
      `SETUP_PLAN.md` all present.
- [x] `~/.claude` untouched; no interactive step was run.
