---
name: second-brain-init
description: Create or retrofit a lightweight repository Second Brain, with optional GitNexus enrichment. Use when asked to implement, bootstrap, or design persistent project knowledge without duplicating code structure, symbols, dependencies, callers, Git history, or changelogs.
---

# Initialize a Second Brain

Build the smallest useful memory layer for a repository.

This workflow works without GitNexus; use GitNexus only when it is already available.

1. Inspect `AGENTS.md`, existing documentation, repository status, manifests, entry points, and tests. Search before opening broad areas of code.
2. If GitNexus is available and the repository is indexed, query its context, clusters, and relevant execution flows. Otherwise continue with direct repository search and code inspection; do not install GitNexus or fail solely because it is unavailable.
3. If the user supplies Markdown sources or an Obsidian vault path, read only the requested files and relevant linked notes. Treat them as source material, not content to copy wholesale.
4. Extract only knowledge that is durable and hard to infer: architectural intent, domain invariants, decision rationale, non-obvious constraints, active roadmap outcomes, migrations or accepted debt, and important development workflows.
5. Create `.brain/` with a few topic files. Omit any empty category. Prefer `architecture.md`, `invariants.md`, `state.md`, and `workflows.md` only when each has real content.
6. Add a compact router to `AGENTS.md`: read only relevant brain pages, use GitNexus when available or search the repository directly, inspect minimum code, check impact, implement, test, and update the brain only if durable knowledge changed.
7. Verify every sentence. Remove file maps, symbol lists, dependency descriptions, code summaries, commit history, completed task logs, speculative backlog items, and boilerplate.

Do not instruct agents to read the whole repository or `.brain`. Preserve generated GitNexus blocks when present and place custom instructions outside their markers.

