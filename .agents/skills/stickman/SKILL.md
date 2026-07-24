```markdown
# stickman Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and workflows used in the `stickman` TypeScript codebase. You'll learn about file organization, import/export conventions, testing patterns, and how to automate game package builds using GitHub Actions workflows.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `game-engine.ts`, `player-controller.ts`

### Import Style
- Use **relative imports** for referencing other modules.
  - Example:
    ```typescript
    import { Player } from './player';
    ```

### Export Style
- Use **named exports** for all exported entities.
  - Example:
    ```typescript
    // In player.ts
    export function movePlayer() { ... }
    export const PLAYER_SPEED = 5;
    ```

### Commit Patterns
- Commits are freeform, with no enforced prefix.
- Average commit message length: ~56 characters.

## Workflows

### Add or Update GitHub Workflow for Game Packages
**Trigger:** When you want to automate export, packaging, or building processes for game repositories via GitHub Actions.  
**Command:** `/add-game-workflow`

1. Create or update a workflow YAML file in `.github/workflows/`.
2. Specify the export, packaging, or build logic for game repositories.
3. Commit the workflow file.

**Files Involved:**
- `.github/workflows/export-market-package.yml`
- `.github/workflows/export-extra-game-package.yml`
- `.github/workflows/build-source-game-packages.yml`

**Example:**
```yaml
# .github/workflows/build-source-game-packages.yml
name: Build Source Game Packages

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install dependencies
        run: npm install
      - name: Build packages
        run: npm run build:packages
```

## Testing Patterns

- **Framework:** Unknown (not detected)
- **Test File Pattern:** Files named with `*.test.*` (e.g., `player.test.ts`)
- **Example:**
  ```typescript
  // player.test.ts
  import { movePlayer } from './player';

  test('player moves correctly', () => {
    expect(movePlayer(1)).toBe(true);
  });
  ```

## Commands

| Command             | Purpose                                                        |
|---------------------|----------------------------------------------------------------|
| /add-game-workflow  | Add or update a GitHub Actions workflow for game packaging/building |
```
