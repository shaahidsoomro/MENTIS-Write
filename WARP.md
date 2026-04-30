# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## What this repo is

This repository contains **MENTIS Writer**, a Claude Code/OpenCode skill implemented entirely as Markdown.

The runtime artifact is `SKILL.md`: Claude Code reads the YAML front matter, including metadata, allowed tools, and the prompt/instructions that follow.

`README.md` is for humans: installation, usage, modes, academic writing skills, anti-plagiarism workflows, and version history.

## Key files

- `SKILL.md`
  - The actual MENTIS Writer skill definition.
  - Starts with YAML front matter containing `name`, `version`, `description`, and `allowed-tools`.
  - Contains the canonical prompt, operating modes, academic writing skills, plagiarism-risk guidance, and AI-writing pattern checks.
- `README.md`
  - Human-facing installation and usage guide.
  - Must stay consistent with the current `SKILL.md` version.
- `LICENSE`
  - Proprietary all-rights-reserved license.
- `MENTIS_WRITE_PROMPT_LIBRARY.md`
  - Integration-ready prompt library for all 118 MENTIS Writer academic writing skills.
- `HOW_TO_USE.md`
  - Practical guide for using MENTIS Writer in Claude, ChatGPT, OpenCode, and document workflows.

When changing behavior or content, treat `SKILL.md` as the source of truth and update `README.md` to stay consistent.

## Common commands

### Install MENTIS Writer into Claude Code

```bash
mkdir -p ~/.claude/skills/MENTIS-Writer
cp SKILL.md ~/.claude/skills/MENTIS-Writer/
```

### Install MENTIS Writer into OpenCode

```bash
mkdir -p ~/.config/opencode/skills/MENTIS-Writer
cp SKILL.md ~/.config/opencode/skills/MENTIS-Writer/
```

## How to run it

Invoke the skill:

```text
/mentis-writer

[paste text]
```

## Making changes safely

### Versioning

- `SKILL.md` has a `version:` field in its YAML front matter. The current public release is `1.0.0`.
- `README.md` has a version history section.
- If you bump the version in `SKILL.md`, update `README.md` as well.

### Editing `SKILL.md`

- Preserve valid YAML front matter formatting and indentation.
- Keep the application name as `MENTIS Writer`.
- Keep citation and academic integrity rules intact.
- Do not add fake citation, detector-bypass, or plagiarism-concealment behavior.
- If adding a new mode or workflow, document it in `README.md`.

### Documenting non-obvious fixes

If you change the prompt to handle a tricky failure mode, add a short note to `README.md` version history describing what changed and why.

## Copyright

Copyright (c) 2026 MENTISERA Research. All rights reserved.

Developer: MENTISERA Research
Contact: hello@mentisera.pk
Website: writer.mentsiera.pk
