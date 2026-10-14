# ICM Setup

A reusable Codex skill for initializing workspaces with Interpretable Context Methodology (ICM) organization and basic Git maintenance.

The skill creates a minimal foundation:

- `AGENTS.md` for workspace identity and essential agent rules.
- `CONTEXT.md` for routing tasks to applicable instructions.
- `instructions/icm.md` for organization rules and context conventions.

Folders and workflows grow from actual work rather than being scaffolded in advance. Existing project content, instructions, Git history, and remotes are preserved.

## Install

Clone this repository into your Codex skills directory:

```sh
git clone https://github.com/doublespeek/icm-setup.git "${CODEX_HOME:-$HOME/.codex}/skills/icm-setup"
```

If that directory already exists, keep or back up your existing skill before installing. Restart Codex to load the skill.

## Use

Ask Codex:

> Use $icm-setup to initialize this project. Its name is My Project, and its purpose is to organize research notes.

The skill inspects the destination, applies the templates, establishes basic local Git maintenance where appropriate, and verifies the resulting routes. Commits, pushes, and merges require explicit user approval.

## Contents

- `SKILL.md`: skill instructions.
- `agents/openai.yaml`: display metadata and default prompt.
- `assets/`: workspace templates.
