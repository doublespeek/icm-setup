---
name: icm-setup
description: Set up a new project with Interpretable Context Methodology (ICM) organization instructions, minimal AGENTS.md and CONTEXT.md routing, and basic Git maintenance. Use when the user requests an ICM workspace or this starter system for a new project.
---

# ICM Setup

Create a minimal, reusable workspace foundation. Let future work determine the folders and workflows; do not design a domain pipeline during setup.

## Establish the destination

Use the user's target directory, or the current project root when unambiguous. Use the supplied project name and brief purpose. If purpose is missing, ask for a short description; continue independent inspection while waiting. Do not infer a technology stack or workflow from the purpose.

Inspect existing agent instructions, target files, and Git status before changing anything. Do not overwrite project content. In an existing workspace, merge only missing generic setup rules while preserving local instructions and routes; surface conflicting rules for the user to resolve.

## Create the foundation

Read the templates in `assets/` and create:

- `AGENTS.md` from `assets/AGENTS.md`: substitute `{{workspace_name}}` and `{{workspace_purpose}}` only.
- `CONTEXT.md` from `assets/CONTEXT.md`: substitute the same values. For a new workspace, its only route is workspace organization → `instructions/icm.md`.
- `instructions/icm.md` from `assets/icm.md`: use the generic conventions as written.

Keep detailed ICM guidance out of `AGENTS.md` and `CONTEXT.md`; agents load it through the organization route. Do not include the paper URL or require fetching it. Do not create stage folders, domain instructions, sample content, reserved folder names, or technology-specific configuration. Preserve the distinction between routing, stage contracts, references, and working artifacts.

These templates are the source of the starter instructions. Do not copy instructions from another active project or incorporate its evolving conventions.

## Establish basic Git maintenance

The AGENTS template requires explicit approval before each commit, push, or merge. Setting up this workspace is not approval for those actions.

If the target has no repository and is not inside an existing repository, initialize a local repository on `main`, unless the user declines Git setup. If an enclosing repository exists, use it; do not create a nested repository. Preserve existing branches, configuration, remotes, and history. Do not create a remote or commit during setup.

Create a minimal `.gitignore` for local OS files, secrets, logs, and caches if needed; preserve existing ignore rules. Add dependency/build/output patterns only for tools and paths actually present. Keep safe environment example files trackable. Do not ignore all Markdown or JSON artifacts: they carry the system's instructions and handoffs.

## Verify and deliver

Check that template substitutions are complete, the organization route resolves, and all three documents have their intended roles. Confirm that no domain workflow or external paper link was introduced. Review changes and Git status; verify ignore behavior if `.gitignore` changed.

Report the created or updated files, repository state, and any unresolved conflict. If proposing an initial commit, summarize its files and branch, then ask for explicit approval. Do not commit, push, or merge without approval for that action.
