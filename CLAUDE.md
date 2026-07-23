# DR0 — Working Protocol

## Identity

This repo is DR0, a deep-research station for scholarship across humanities,
arts, theatre/scenography, digital humanities, philosophy (object-oriented
ontology, genetic criticism), and AI/XAI. Outputs are evidence-gated research
artifacts, not chat.

## Research Protocol

Every research run follows this pipeline:

- Each run gets a folder `runs/YYYY-MM-DD-<slug>/` containing `plan.md`,
  `report.md`, and `claims.md`.
- **Retrieval order:**
  1. `semantic-scholar` and `papersflow` MCP tools for journal literature.
  2. General web search for monographs, grey literature, and non-English
     (including Persian) sources — paper indexes have WEAK humanities
     coverage. Never treat an empty MCP result as "no literature exists."
  3. PDFs the user placed in `sources/pdfs/` are first-class sources.
- Every non-trivial claim in `report.md` carries a citation. Run
  `citation-verification` on the final draft; unverifiable citations are
  moved to an "unverified" section — never silently kept.
- `claims.md` is an evidence ledger: `claim | strength (verified /
  single-source / speculative) | sources`. Only verified claims may later
  be promoted to `kb/`.
- `kb/` holds durable, synthesized knowledge notes (markdown, wikilinks
  welcome). Promotion from a run into `kb/` happens only on explicit user
  request.

## Token Discipline for Research Runs

- Plan before searching.
- Batch MCP queries.
- Read abstracts before full texts; fetch full text only for shortlisted
  sources.
- Prefer 5 excellent sources over 25 skimmed ones.

## Language

Sources and reasoning may be Persian or English. Reports default to English
unless the user says otherwise. Preserve Persian titles in original script
with transliteration.

## Boundaries

- Never modify `~/.claude`.
- Never delete anything under `runs/` or `kb/`.
- Ask before any destructive git operation.
