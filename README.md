# Codex Second Brain

Two dependency-free Codex skills for keeping small, durable repository knowledge. GitNexus is an optional accelerator, not a requirement.

- `second-brain-init` inspects a repository directly and creates a progressively retrieved `.brain` plus compact routing in `AGENTS.md`.
- `second-brain-maintain` updates that knowledge after significant changes or synchronizes selected Markdown and Obsidian documents.

## Division of responsibility

`.brain` stores architectural intent, domain invariants, decision rationale, non-obvious constraints, active roadmap state, migrations or accepted debt, and repeatable development workflows.

Source code and source documents remain the source of truth. When GitNexus is available, the skills use it for files, symbols, dependencies, callers, execution flows, and blast radius; otherwise they inspect the repository with Codex's normal search and file tools. The brain still rejects changelogs, transient task notes, file maps, source summaries, and boilerplate.

## Requirements

- Codex with repository skills enabled.
- An existing `AGENTS.md`, or permission for the initialization skill to create one.

Optional: an indexed GitNexus repository and its MCP tools.

## Install

### Public plugin directory

After the plugin is approved and published, open **Plugins** in the ChatGPT desktop app, search for **Codex Second Brain**, select the plus button, and start a new chat after installation.

In Codex CLI:

```text
codex
/plugins
```

Search for **Codex Second Brain**, install it, then start a new Codex session. The IDE extension does not support plugins; use the standalone skill installation below instead.

### Install now from GitHub

The simplest local installation is through Codex's built-in skill installer:

```text
$skill-installer Install second-brain-init and second-brain-maintain from https://github.com/AndreaScuto/codex-second-brain/tree/master/skills
```

Alternatively, clone or download this repository and copy both directories under `skills/` into one of Codex's skill locations.

For every repository you use:

```text
$HOME/.agents/skills/second-brain-init/
$HOME/.agents/skills/second-brain-maintain/
```

For one repository only:

```text
<project>/.agents/skills/second-brain-init/
<project>/.agents/skills/second-brain-maintain/
```

Each directory must contain its `SKILL.md` directly. Codex normally detects new skills automatically; restart Codex if they do not appear.

## Plugin package

This repository is also packaged as a skills-only plugin for ChatGPT and Codex through `.codex-plugin/plugin.json`. It does not require an MCP server or external service.

Public directory publication requires submission and review through the OpenAI Platform plugin portal. Until approval, use the GitHub installation above. The publisher must provide a verified developer identity, support and policy URLs, listing metadata, and test cases.

## Use

Ask Codex to use `second-brain-init` once when adding the knowledge layer to a repository. It inspects existing instructions, documentation, repository state, relevant code, and GitNexus flows when available before writing the smallest useful `.brain`.

Use `second-brain-maintain` after a significant architectural, domain, migration, debt, or development-workflow change. You can also give it one or more Markdown files, including notes from an Obsidian vault, to synchronize durable instructions and current roadmap state. It edits only the relevant page, replaces stale imported knowledge instead of appending duplicates, and leaves `.brain` untouched for ordinary code changes.

```text
Use second-brain-init for this repository. GitNexus is not available.
Use second-brain-maintain to sync docs/roadmap.md into .brain.
```

The intended session flow is:

```text
task -> relevant .brain page -> optional GitNexus or repository search -> minimum code -> impact -> change + tests -> durable knowledge update, if needed
```

## License

Apache-2.0.

