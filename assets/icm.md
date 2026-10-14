# ICM Organization Instructions

Apply these rules when extending or reorganizing this workspace.

## Create structure as needed

- Let the current task determine folders and responsibilities. Do not scaffold speculative stages or reserve a workflow in advance.
- Give each folder a clear purpose. Reuse an appropriate existing location before adding one.
- When a sequential workflow is established, use numbered stage folders (`01_name`, `02_name`) to express execution order. Each stage does one job. Choose the parent location and stage names for the actual workflow.
- Separate persistent references and configuration from working inputs and generated artifacts. Use `references/` for stage-specific guidance and `output/` for stage results; choose shared reference locations when needed.
- Keep different tasks or runs distinct. Preserve original inputs and human edits.

## Maintain the context hierarchy

- Root `AGENTS.md`: workspace identity and essential agent rules; keep it short.
- Root `CONTEXT.md`: task routing to existing instructions, folders, and shared resources.
- Local `CONTEXT.md`: a stage contract, or a routing index for a collection of resources.
- Reference files: persistent conventions, style guides, and constraints.
- Working artifacts: material specific to the current task or run.

Keep routing, instructions, references, and working artifacts separate. Create local context files when a folder needs its own contract or navigation; do not add them mechanically to every folder.

## Write useful context files

For a routing index, state the scope and map task triggers to paths and their purposes. Add only routes whose targets exist. Specify whether paths are relative to the context file or workspace root.

Before executing a stage, create its `CONTEXT.md` with:

- **Inputs:** a table identifying paths, required sections, and whether each input is reference or working material. Identify the current run and exact upstream artifacts.
- **Process:** the stage's single responsibility and applicable constraints. Use local scripts for mechanical operations.
- **Outputs:** destination paths, formats, and completion checks, with a human review boundary before dependent work proceeds.

Use Markdown or JSON for readable handoffs and decisions. Where binary assets or deliverables are necessary, accompany them with text manifests containing paths, source identifiers, and relevant metadata.

## Keep routes and handoffs accurate

- Load only the routed instructions, local contract, and declared inputs needed for the task.
- Consume the latest reviewed artifacts. Honor continuation already authorized by the user; never infer approval from file existence.
- Update affected routes and contracts when files move or responsibilities change. Flag downstream results that become stale.
- Before finishing, verify that new files fit their folder's purpose, route targets exist, and input/output paths agree.
