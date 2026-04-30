# MENTIS Writer

MENTIS Writer is a strict academic and professional writing refinement skill. It removes weak AI-like writing patterns by improving specificity, argument ownership, source use, sentence rhythm, and paragraph logic.

It is based on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup, and extends that guidance with dissertation editing, plagiarism-risk review, Claude/ChatGPT integration, and academic refinement reports.

## What it does

- Removes AI-like phrasing, filler, generic transitions, inflated significance, and promotional wording.
- Improves academic clarity, coherence, paragraph unity, theoretical precision, and authorial voice.
- Supports "AI remover" usage for legitimate cleanup of robotic or ChatGPT-style prose.
- Reviews plagiarism-risk patterns such as close paraphrase, patchwriting, citation stripping, and copied structure.
- Preserves citations and marks unsupported claims with `[citation needed]`.
- Provides dissertation-quality revision modes for PhD-level academic writing.
- Produces optional academic refinement reports with improvement notes, citation warnings, and originality risks.
- Includes `MENTIS_WRITE_PROMPT_LIBRARY.md`, an integration-ready prompt library for all 118 academic writing skills.
- Includes `HOW_TO_USE.md`, a practical Claude, ChatGPT, OpenCode, and document workflow guide.

## Integrity rules

MENTIS Writer is for genuine revision, not concealment.

- Do not use it to bypass plagiarism checkers, AI detectors, institutional policies, or academic integrity systems.
- Do not fabricate citations, page numbers, quotations, references, statistics, or evidence.
- Preserve the author's meaning, citations, argument, disciplinary framing, and research stance.
- Cite borrowed ideas. Quote exact wording. Mark unsupported claims.

## Installation

### Claude Code

```bash
mkdir -p ~/.claude/skills/MENTIS-Writer
cp SKILL.md ~/.claude/skills/MENTIS-Writer/
```

### OpenCode

```bash
mkdir -p ~/.config/opencode/skills/MENTIS-Writer
cp SKILL.md ~/.config/opencode/skills/MENTIS-Writer/
```

OpenCode also scans `~/.claude/skills/`, so installing once into the Claude skills directory may work for both tools.

## Basic usage

### Claude Code

```text
/mentis-writer

[paste your text here]
```

### OpenCode

```text
/mentis-writer

[paste your text here]
```

### Natural language

```text
Please humanize this text:

[paste text]
```

## Main modes

MENTIS Writer detects intent from the user's request. If no mode is clear, it uses MENTIS Writer humanizer mode.

### MENTIS Writer humanizer mode

Use for general rewriting, flow improvement, robotic tone removal, and natural prose.

```text
Humanize this text. Preserve meaning and citations. Return only the revised version.

[paste text]
```

### AI remover mode

Use when the text sounds like ChatGPT or generic AI output.

```text
AI remover:

Remove AI-generated writing signs from the text below. Preserve meaning, citations, facts, and tone. Do not invent sources or details. Remove robotic phrasing, inflated claims, filler, vague attribution, and mechanical formatting. Return only the final cleaned text.

[paste text]
```

### ChatGPT cleanup mode

Use for text with ChatGPT-style artifacts such as polite preambles, title-case headings, excessive bolding, generic summaries, and over-balanced paragraphs.

```text
Revise the following text so it sounds like careful human writing, not ChatGPT output.

Rules:
- Preserve meaning.
- Preserve citations exactly.
- Do not invent facts or sources.
- Remove generic AI phrasing, inflated importance, vague attribution, filler, robotic transitions, and mechanical formatting.
- Mark unsupported claims as [citation needed].
- Return only the final revised text.

Text:
[paste text]
```

### Plagiarism-risk reduction mode

Use for ethical paraphrasing, originality improvement, and source-use review.

```text
Rewrite the following text to reduce plagiarism risk ethically.

Rules:
- Preserve the meaning and argument.
- Preserve all citations exactly.
- Do not remove citations.
- Do not invent sources, facts, quotations, page numbers, or statistics.
- Do not paraphrase sentence by sentence.
- Rebuild the structure in original wording.
- Keep direct quotations in quotation marks.
- Mark unsupported factual claims as [citation needed].
- Return only the revised text.

Text:
[paste text]
```

### Dissertation advisor mode

Use for PhD-level revision, thesis chapters, proposals, literature reviews, methodology sections, theoretical frameworks, findings, discussions, and conclusions.

```text
Act as a PhD-level dissertation writing advisor, academic editor, research mentor, and subject-specialist reviewer.

Revise the following text into dissertation-quality academic prose.

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
1. Preserve the original meaning, argument, evidence, and authorial intent.
2. Do not invent facts, references, quotations, page numbers, dates, statistics, or authors.
3. Preserve all existing citations exactly.
4. If a claim needs evidence, insert [citation needed].
5. Strengthen clarity, coherence, analytical depth, theoretical precision, and scholarly tone.
6. Remove generic AI-like phrasing and robotic transitions.
7. Improve paragraph unity and logical flow.
8. Use discipline-specific academic language.
9. Add analytical movement: claim -> context -> evidence -> analysis -> contribution.
10. Avoid overstatement; use careful academic qualification where needed.
11. Ensure the paragraph can be defended in a PhD viva.
12. Do not use decorative language, bullet-heavy prose, or promotional wording.

Text:
[paste text]
```

### Academic refinement report mode

Use when you want the revised text plus a short diagnostic report.

```text
You are an academic writing refinement assistant.

Your role is to improve clarity, coherence, originality, scholarly tone, paragraph flow, citation discipline, and human editorial quality.

Do not help users bypass plagiarism checkers, AI detectors, academic integrity systems, or institutional policies.

Do not fabricate citations, page numbers, quotations, references, statistics, or evidence.

Preserve the author's original meaning, citations, argument, disciplinary framing, and research stance.

If a claim lacks support, insert [citation needed].

Return:
1. Refined academic version
2. Key improvements made
3. Citation and evidence warnings
4. Originality and source-use risks

Text:
[paste text]
```

## Academic writing skills included

MENTIS Writer includes a 15-part academic writing framework:

1. Argument ownership
2. Sentence rhythm variation
3. Specificity
4. Analytical movement
5. Controlled imperfection
6. Concrete nouns over abstract filler
7. Strong topic sentences
8. Human transitions
9. Qualification
10. Comparative framing
11. Paragraph unity
12. Source-aware voice
13. Argumentative verbs
14. Controlled repetition of key terms
15. Final human read-aloud revision

## Anti-plagiarism writing skills included

MENTIS Writer also includes a 12-part plagiarism-risk framework:

1. Idea ownership
2. Proper paraphrasing
3. Citation discipline
4. Quotation control
5. Structural originality
6. Source synthesis
7. Note-taking
8. Patchwriting avoidance
9. Common knowledge judgment
10. Self-plagiarism prevention
11. Evidence integration
12. Similarity review

Golden rule:

```text
Do not copy wording.
Do not copy structure.
Do not copy ideas without citation.
Write from your own argument and cite every borrowed idea.
```

## LLM weaknesses corrected

MENTIS Writer audits and corrects common LLM writing weaknesses:

- Predictable sentence structure
- Generic academic wording
- Too much balance and not enough judgment
- Repetitive transitions
- Weak authorial voice
- Lack of theoretical depth
- Source-stacking
- Lack of context
- Over-polished smoothness
- Unsupported claims
- No counterargument
- Mechanical paragraph endings

## AI-writing signs detected

The skill checks for issues across:

- Content: significance inflation, notability padding, vague attribution, superficial analysis, formulaic challenges.
- Language: AI vocabulary clusters, copula avoidance, negative parallelisms, rule of three, synonym cycling, false ranges.
- Style: title-case headings, decorative bolding, inline-header lists, em dash overuse, shallow tables, fragmented headers.
- Communication: chatbot greetings, closing offers, knowledge-cutoff disclaimers, placeholder text.
- Markup: Markdown leftovers, broken wikitext, citation artifacts, search links, tracking links.
- Citations: broken links, invalid DOI/ISBN, unsupported sources, source laundering, fake precision.
- Plagiarism risk: close paraphrase, patchwriting, copied structure, citation stripping, unsupported synthesis.

## Voice calibration

To match a writer's voice, provide a writing sample:

```text
/mentis-writer

Here is a sample of my writing for voice matching:
[paste 2-3 paragraphs]

Now revise this text in my style:
[paste text]
```

The skill analyzes sentence rhythm, vocabulary, paragraph openings, punctuation habits, transitions, and formality before revising.

## Version history

- `1.0.0` - Initial MENTIS Writer release with AI-style cleanup, dissertation refinement, academic writing skills, anti-plagiarism workflows, and academic refinement reports.

## References

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [WikiProject AI Cleanup](https://en.wikipedia.org/wiki/Wikipedia:WikiProject_AI_Cleanup)

## License

Proprietary. All rights reserved.

No permission is granted to copy, modify, publish, distribute, sublicense, sell, host, commercialize, reverse engineer, or create derivative works from MENTIS Writer without prior written permission from MENTISERA Research.

## Legal

Copyright (c) 2026 MENTISERA Research. All rights reserved.

Designed, developed, and distributed by MENTISERA Research.

Developer: MENTISERA Research
Contact: hello@mentisera.pk
Website: writer.mentsiera.pk

Commercial use, redistribution, derivative work, or use of MENTISERA branding, hosted services, or proprietary distribution channels requires explicit written permission from MENTISERA Research.
