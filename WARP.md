# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## What this repo is

This repository contains **MENTIS**, a Claude Code/OpenCode skill implemented entirely as Markdown.

The runtime artifact is `SKILL.md`: Claude Code reads the YAML front matter, including metadata, allowed tools, and the prompt/instructions that follow.

`README.md` is for humans: installation, usage, modes, academic writing skills, anti-plagiarism workflows, and version history.

## Key files

- `SKILL.md`
  - The actual MENTIS skill definition.
  - Starts with YAML front matter containing `name`, `version`, `description`, and `allowed-tools`.
  - Contains the canonical prompt, operating modes, academic writing skills, plagiarism-risk guidance, and AI-writing pattern checks.
- `README.md`
  - Human-facing installation and usage guide.
  - Must stay consistent with the current `SKILL.md` version.
- `LICENSE`
  - MIT license.

When changing behavior or content, treat `SKILL.md` as the source of truth and update `README.md` to stay consistent.

## Common commands

### Install MENTIS into Claude Code

```bash
mkdir -p ~/.claude/skills/MENTIS
cp SKILL.md ~/.claude/skills/MENTIS/
```

### Install MENTIS into OpenCode

```bash
mkdir -p ~/.config/opencode/skills/MENTIS
cp SKILL.md ~/.config/opencode/skills/MENTIS/
```

## How to run it

Invoke the skill:

```text
/mentis

[paste text]
```

## Making changes safely

### Versioning

- `SKILL.md` has a `version:` field in its YAML front matter.
- `README.md` has a version history section.
- If you bump the version in `SKILL.md`, update `README.md` as well.

### Editing `SKILL.md`

- Preserve valid YAML front matter formatting and indentation.
- Keep the application name as `MENTIS`.
- Keep citation and academic integrity rules intact.
- Do not add fake citation, detector-bypass, or plagiarism-concealment behavior.
- If adding a new mode or workflow, document it in `README.md`.

### Documenting non-obvious fixes

If you change the prompt to handle a tricky failure mode, add a short note to `README.md` version history describing what changed and why.

## Copyright

Copyright (c) 2026 MENTISERA (SMC-PRIVATE) Limited. All rights reserved.
