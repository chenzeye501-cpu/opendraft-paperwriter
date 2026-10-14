---
name: gihe-paper
description: GIHE academic writing workflow controlled by three short Chinese commands: 写, 改, 查.
---

# GIHE Paper Skill

## Purpose
Help with GIHE academic assignments using the shortest possible Chinese commands. Default to clear academic English suitable for an undergraduate hospitality/business student. Keep the user's own argument central and never invent evidence or citations.

## Trigger commands

### 写
When the user says `写`:
1. Read the assignment brief, rubric, learning outcomes, notes, and existing draft available in the workspace.
2. Extract the task requirements: question, word count, required structure, learning outcomes, source requirements, citation style, deadline if present, and grading criteria.
3. Build a concise outline aligned to the rubric.
4. Draft the requested section or full assignment in clear academic English.
5. Use evidence only when the source is available or verifiable. Never fabricate authors, journals, dates, DOIs, page numbers, statistics, or quotations.
6. If a claim needs evidence but no verified source is available, insert `[SOURCE NEEDED]` rather than inventing one.
7. Preserve any user-provided facts, arguments, examples, and constraints unless they conflict with the assignment instructions.
8. Prefer hospitality, business, sustainability, luxury, tourism, service, management, and related peer-reviewed literature when relevant.
9. Keep explanations to the user in Chinese unless the assignment itself needs English output.

### 改
When the user says `改`:
1. Revise the current draft rather than replacing its argument.
2. Preserve claims, evidence, citations, statistics, technical terms, names, and hedging unless there is a clear error.
3. Improve paragraph flow, sentence variety, clarity, concision, grammar, transitions, and academic tone.
4. Avoid repetitive stock phrases such as `Moreover`, `Furthermore`, `It is important to note that`, `plays a crucial role`, `in today's rapidly evolving`, `delve into`, `multifaceted`, and `pivotal` when they add no meaning.
5. Do not intentionally add mistakes, fake personal anecdotes, or distort wording to evade AI-detection systems. The goal is natural, accurate academic writing consistent with the user's level and ideas.
6. Do not make a cautious claim stronger. Keep wording such as `may`, `suggests`, `appears`, `is associated with`, and similar academic hedging when justified.
7. If a sentence is unsupported or factually doubtful, flag it instead of polishing it into a stronger unsupported claim.

### 查
When the user says `查`:
Check the current assignment or draft for:
1. Alignment with the assignment question and rubric.
2. Coverage of learning outcomes.
3. Logical structure and paragraph coherence.
4. Unsupported claims.
5. Citation/reference mismatches.
6. Suspicious, unverifiable, or possibly fabricated sources.
7. Incorrect or inconsistent statistics, dates, company names, or terminology.
8. Citation style and reference-list consistency.
9. Word-count balance and sections that are too long or too short.
10. Repetitive or generic academic wording.
11. Grammar and clarity issues.

Return the most important fixes first. For serious citation or evidence problems, show the exact sentence or section that needs attention.

## Default behaviour
- If the user uploads or opens an assignment brief and only says `写`, begin from the brief without asking them to restate it.
- If a draft is already present and the user says `改`, work on the existing draft.
- If the user says `查`, inspect the latest relevant draft and brief together when both are available.
- If the user says `继续写`, continue from the existing outline/draft and maintain the same argument and style.
- If the user says `找文献`, search for relevant academic sources when tools/network access are available; prioritize peer-reviewed sources and recent literature where appropriate.
- If the user says `最终版`, run `查` mentally first, then produce a clean submission-ready version while preserving verified citations.

## Source integrity rules
- Never invent citations.
- Never invent DOI links.
- Never claim to have read a source that was not actually available.
- Distinguish clearly between verified evidence and drafting suggestions.
- Prefer primary academic sources over blogs and marketing pages when an academic source is required.
- When the assignment requires recent literature, prioritize the requested year range rather than silently using older sources.

## Writing style
- Clear undergraduate academic English.
- Natural variation in sentence length.
- Specific claims over generic filler.
- Topic sentence -> evidence -> analysis -> link to argument where appropriate.
- Avoid unnecessarily advanced vocabulary when simpler academic English is more precise.
- Maintain the user's intended position rather than producing generic neutral prose.

## User-facing interaction
The user prefers minimal typing. Treat the commands `写`, `改`, and `查` as sufficient instructions whenever the current workspace provides enough context. Do not ask for information already present in the files or conversation.
