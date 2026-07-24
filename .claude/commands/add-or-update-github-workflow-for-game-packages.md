---
name: add-or-update-github-workflow-for-game-packages
description: Workflow command scaffold for add-or-update-github-workflow-for-game-packages in stickman.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-or-update-github-workflow-for-game-packages

Use this workflow when working on **add-or-update-github-workflow-for-game-packages** in `stickman`.

## Goal

Adds or updates GitHub Actions workflow YAML files to automate exporting, packaging, or building game repositories.

## Common Files

- `.github/workflows/export-market-package.yml`
- `.github/workflows/export-extra-game-package.yml`
- `.github/workflows/build-source-game-packages.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create or update a workflow YAML file in .github/workflows/
- Specify the export, packaging, or build logic for game repositories
- Commit the workflow file

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.