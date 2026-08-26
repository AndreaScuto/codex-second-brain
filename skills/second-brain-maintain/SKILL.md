---
name: second-brain-maintain
description: Maintain a repository's lightweight .brain after durable changes, or import and synchronize roadmap and instruction Markdown sources, including Obsidian notes. GitNexus is optional. Do not use for ordinary code edits, graph facts, changelogs, or transient task status.
---

# Maintain a Second Brain

Use this when durable project knowledge may have changed or the user asks to synchronize a Markdown source.

1. Read the `AGENTS.md` router and only the relevant `.brain` page.
2. For an explicit Markdown source, read only the requested files and the linked Obsidian notes needed to understand them. Keep the source document as the source of truth and record a relative Markdown link or Obsidian wikilink when useful.
3. Map architectural intent to `architecture.md`, invariants and constraints to `invariants.md`, active roadmap outcomes, migrations, and accepted debt to `state.md`, and repeatable instructions to `workflows.md`. Import concise current knowledge, not the whole document.
4. If GitNexus is available and indexed, query it for current structure and blast radius. Otherwise inspect the minimum relevant repository files directly. Never encode file, symbol, caller, or dependency maps in documentation.
5. Decide whether the change or source altered durable intent, an invariant, rationale, a non-obvious constraint, an active roadmap/migration/debt item, or a repeatable workflow. If not, stop without editing `.brain`.
6. Edit the smallest existing page. Create a page only for a distinct topic that will receive durable knowledge.
7. Synchronize idempotently: replace or delete stale knowledge previously derived from the same source instead of appending duplicates or history. Keep current status, rationale, dependencies, acceptance criteria, and operational consequences; remove code summaries, diffs, completed task notes, ownerless TODOs, and speculation.
8. Check links and review `git diff -- AGENTS.md .brain .agents/skills`. If code changed, run the repository's normal tests and, only when available, GitNexus change detection before commit.

