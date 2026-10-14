# {{workspace_name}}

{{workspace_purpose}}

Use Interpretable Context Methodology (ICM) to organize this workspace.

Read root `CONTEXT.md` to find applicable instructions. Before creating, moving, or reorganizing project files, folders, or context documents, follow its workspace organization route.

Let concrete work determine the structure; create only what the current task needs. Keep context scoped to the task.

## Git maintenance

- Check `git status` before making changes and before finishing. Preserve existing user changes; review the diff for unintended edits.
- Keep changes focused. Stage only files belonging to the task, and keep secrets, temporary files, and generated binaries out of Git unless explicitly requested.
- Run appropriate checks before proposing a commit and report the changes and validation results.
- Ask the user for explicit approval before committing, pushing, or merging. Approval for one action does not authorize the others; do not infer approval from a request to implement changes.
- Before requesting approval, summarize the proposed action, affected branch or remote, and relevant changes. Do not reset, discard changes, rewrite history, or force-push without explicit authorization.
