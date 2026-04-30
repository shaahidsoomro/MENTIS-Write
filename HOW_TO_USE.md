# How to Use MENTIS Writer

MENTIS Writer is an academic writing refinement system for dissertation, thesis, article, proposal, and research writing. It helps improve clarity, scholarly tone, paragraph flow, citation discipline, originality, and human academic voice.

Use it to revise writing ethically. Do not use it to fabricate sources, hide plagiarism, bypass academic integrity systems, or misrepresent authorship.

## Files in this project

- `SKILL.md` is the Claude/OpenCode skill file.
- `MENTIS_WRITE_PROMPT_LIBRARY.md` contains the full 118-skill academic prompt library.
- `README.md` gives the project overview.
- `LICENSE` explains the proprietary all-rights-reserved license.

## Use in Claude Code

Install the skill:

```bash
mkdir -p ~/.claude/skills/MENTIS-Writer
cp SKILL.md ~/.claude/skills/MENTIS-Writer/
```

Run it:

```text
/mentis-writer

[paste your text here]
```

### Claude example: dissertation revision

```text
/mentis-writer

Use Dissertation Advisor Mode.

Research context:
- Discipline: International Relations
- Topic: Pakistan and the SCO
- Chapter/section: Literature review
- Research problem: Existing explanations do not fully explain Pakistan's post-2017 SCO participation.
- Research questions:
- Theoretical framework: Complex interdependence and PSN framework
- Methodology:
- Case: Pakistan's SCO membership
- Time period: Post-2017
- Main argument:

Revise the following text into dissertation-quality academic prose.
Preserve citations exactly. Do not invent sources. Mark unsupported claims with [citation needed].

Text:
[paste text]
```

## Use in ChatGPT

ChatGPT does not automatically load local skill files. Use one of these methods:

1. Upload `MENTIS_WRITE_PROMPT_LIBRARY.md` and ask ChatGPT to use it.
2. Copy the relevant prompt from `MENTIS_WRITE_PROMPT_LIBRARY.md`.
3. Paste the base prompt, citation guard, selected skill, and your text.

### ChatGPT example: literature review synthesis

```text
Use MENTIS Writer.

Apply:
1. Universal base prompt
2. Citation integrity guard
3. MW-012 Thematic Synthesis
4. MW-050 Literature Review Chapter Development
5. Final academic quality audit

Requirements:
- Preserve all citations exactly.
- Do not invent sources, facts, dates, quotations, page numbers, or statistics.
- Mark unsupported claims with [citation needed].
- Convert author-by-author summary into thematic synthesis.
- Return only the revised version unless citation warnings are necessary.

Text:
[paste literature review]
```

## Use in OpenCode

Install the skill:

```bash
mkdir -p ~/.config/opencode/skills/MENTIS-Writer
cp SKILL.md ~/.config/opencode/skills/MENTIS-Writer/
```

Run it:

```text
/mentis-writer

[paste your text here]
```

## Best document workflow

Use this sequence for best results:

```text
1. Identify the document type.
2. Provide research context.
3. Choose the relevant MENTIS Writer skill or mode.
4. Paste the text.
5. Ask for revise_only, diagnostic, supervisor_ready, viva, or publication output.
6. Review citation warnings and fix missing evidence manually.
```

## Output modes

### revise_only

Use when you want only polished text.

```text
Mode: revise_only
Return only the revised text.
```

### diagnostic

Use when you want feedback and revision priorities.

```text
Mode: diagnostic
Return:
1. Strengths
2. Weaknesses
3. Revision priorities
4. Revised version
```

### supervisor_ready

Use when preparing text for a PhD supervisor.

```text
Mode: supervisor_ready
Revise this passage so it is ready for supervisor review.
Prioritize clarity, argument, citation integrity, theoretical defensibility, methodology alignment, and mature academic tone.
```

### viva

Use when preparing for oral defense.

```text
Mode: viva
Generate likely examiner questions and defensible answer structures based only on the provided dissertation material.
```

### publication

Use when converting dissertation prose into article style.

```text
Mode: publication
Convert this dissertation passage into journal article style.
Narrow the scope, sharpen the argument, reduce excessive background, and preserve citations.
```

## Common use cases

### Humanize academic writing

```text
Use MENTIS Writer AI remover mode.

Remove AI-like writing patterns from this text while preserving meaning, citations, and academic tone.
Do not invent sources. Mark unsupported claims with [citation needed].

Text:
[paste text]
```

### Improve a problem statement

```text
Use MW-002 Problem Statement Refinement and MW-046 Problem Statement Writing.

Revise this into a focused dissertation-level problem statement.
Structure it around context, problem, gap, and research focus.

Text:
[paste text]
```

### Improve a research gap

```text
Use MW-003 Research Gap Identification and MW-015 Research Gap-to-Argument Connection.

Refine the research gap and connect it to the study's main argument.
Do not invent literature.

Text:
[paste text]
```

### Improve a theoretical framework

```text
Use MW-021 to MW-030.

Revise this theoretical framework section.
Clarify theory selection, concepts, limitations, analytical categories, and alignment with research questions.

Text:
[paste text]
```

### Improve methodology

```text
Use MW-031 to MW-042 and MW-116.

Revise this methodology section for design clarity, alignment, data source explanation, analysis procedure, limitations, ethics, and viva defense readiness.

Text:
[paste text]
```

### Check citations and evidence

```text
Use MW-073 to MW-082 and MW-116.

Review this passage for citation integrity.
Preserve citations exactly.
Mark unsupported claims with [citation needed].
Mark questionable source support with [check citation support].

Text:
[paste text]
```

### Reduce plagiarism risk ethically

```text
Use MENTIS Writer plagiarism-risk reduction mode.

Rewrite this text to reduce plagiarism risk ethically.
Do not remove citations.
Do not invent sources.
Do not paraphrase sentence by sentence.
Rebuild the structure in original wording.
Mark unsupported claims with [citation needed].

Text:
[paste text]
```

## Skill selection guide

Use these shortcuts:

- Introduction: MW-001 to MW-005, MW-043 to MW-049
- Literature review: MW-011 to MW-020, MW-050
- Theoretical framework: MW-021 to MW-030, MW-051
- Methodology: MW-031 to MW-042, MW-052
- Findings: MW-053, MW-007 to MW-009
- Discussion: MW-054, MW-006 to MW-010, MW-096
- Conclusion: MW-055, MW-005, MW-118
- Citation integrity: MW-073 to MW-082, MW-116
- Supervisor readiness: MW-091 to MW-096, MW-113, MW-114
- Viva defense: MW-094, MW-115
- Publication: MW-097 to MW-102

## Recommended full prompt

```text
Use MENTIS Writer.

Mode: supervisor_ready
Section type: literature review
Skills: MW-012, MW-014, MW-015, MW-050, MW-116

Research context:
- Discipline:
- Topic:
- Chapter/section:
- Research problem:
- Research questions:
- Theoretical framework:
- Methodology:
- Case:
- Time period:
- Main argument:

Requirements:
- Preserve meaning, citations, evidence, and authorial intent.
- Do not invent facts, sources, dates, quotations, statistics, or page numbers.
- Mark unsupported claims with [citation needed].
- Improve synthesis, scholarly tone, paragraph unity, and analytical depth.
- Remove generic AI-like phrasing and robotic transitions.
- Return a supervisor-ready revised version.

Text:
[paste text]
```

## Practical tips

- Provide the section type when possible.
- Provide citations in the text if you want them preserved.
- Provide a writing sample if you want voice matching.
- Ask for diagnostic mode when the draft is weak or incomplete.
- Ask for revise_only when the draft is already developed.
- Review every `[citation needed]`, `[clarification needed]`, and `[check citation support]` marker before submission.

## Important rule

MENTIS Writer improves academic writing. It does not replace research, evidence checking, supervisor feedback, citation verification, or the writer's own intellectual responsibility.
