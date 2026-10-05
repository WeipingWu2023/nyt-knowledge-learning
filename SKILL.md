---
name: nyt-knowledge-learning
description: Turn an accessible New York Times article URL or supplied article text into a source-grounded Obsidian learning note with sentence-level English support, natural Chinese translation, beginner background, durable knowledge links, and cross-article connections.
metadata:
  short-description: Learn English and durable knowledge from NYT articles
---

# NYT Knowledge & English Learning

Use this skill only when the user provides an NYT article URL or article text and wants a complete learning note. The article text supplied by the user is the authoritative primary source for sentence-level analysis. Do not invent, reconstruct, or silently fill missing article content. Read [references/access-and-input-modes.md](references/access-and-input-modes.md) before handling the input.

## Two input modes

### Mode A — URL

Try to retrieve the article normally with the tools currently available. Continue only when the full article is reliably accessible and readable. If CAPTCHA, browser security policy, authentication, subscription restriction, paywall, automated-access protection, or any other limitation prevents reliable retrieval of the full article:

1. Stop article analysis immediately.
2. Do not reconstruct the article from search snippets, headlines, related coverage, cached fragments, or external summaries.
3. Do not guess missing paragraphs, claim to have read the article, or create a partial learning note as if it were complete.
4. Tell the user exactly: `我无法可靠读取这篇 NYT 的完整正文。请把文章正文复制给我。你不需要整理格式，直接全部粘贴即可。`
5. Wait for the user to provide the article text. Do not continue background research or modify the vault for that article before the text arrives.

Never bypass CAPTCHA, paywalls, authentication, subscription controls, or website security controls.

### Mode B — user-provided text

Treat the user's pasted text as the authoritative primary article source. Identify the headline, author, publication date, section/topic, and article body when possible. Ignore obvious navigation, advertisements, subscription prompts, recommendations, and unrelated interface text accidentally included in the paste. If the article body appears incomplete, state what is missing and ask for the remainder before claiming a complete article analysis.

Keep `PRIMARY ARTICLE SOURCE` and `BACKGROUND RESEARCH SOURCES` visibly separate in the note. Use the primary article text for sentence-by-sentence translation and English teaching. Use external sources only to explain background, definitions, institutions, history, data, people, countries, events, or broader implications. External summaries must never substitute for missing NYT text.

## Vault contract

Work in the user's vault at `D:\Obsidian\NYT`. Preserve existing content. Use readable filenames and Obsidian `[[wikilinks]]`. Before creating a durable concept note, search `Knowledge` for an existing concept and update it when appropriate. Keep article notes in `Articles`, reusable English notes in `English learning`, and templates in `Templates`. Update `Dashboard/NYT Learning Dashboard.md` when a new article or durable connection makes it useful.

## Workflow

1. After the full article is available, read and understand it before drafting. Identify title, author, date, URL or input provenance, topic, thesis, main actors, timeline, and unresolved uncertainty.
2. When background is needed, research reliable primary or authoritative sources. Read [references/research-and-sources.md](references/research-and-sources.md) and include direct source links in the note. Label article claims separately from researched context.
3. Build the beginner mental model first: what happened, who is involved, what led to it, what may happen next, and why it matters.
4. Search the existing vault before creating or updating knowledge notes. Prefer an existing durable concept note and preserve its useful content.
5. Write one article note using the structure in [references/note-design.md](references/note-design.md) and the user's vault template `Templates/NYT Article Learning Template.md`.
6. Walk through the article in original order. Translate every sentence naturally into Chinese, but analyze English selectively: focus on difficult or high-value vocabulary, chunks, grammar, complex structures, and discourse logic. Easy sentences receive brief treatment.
7. Explain background concepts, cause → effect relationships, and domain context for a complete beginner. Mark uncertain, disputed, or time-sensitive claims clearly.
8. Create or update only durable Knowledge notes using `Templates/Knowledge Note Template.md`; add Obsidian `[[wikilinks]]` from both directions when useful.
9. Finish with review vocabulary/chunks, what was learned, knowledge connections, and clearly separated primary and background sources. Use an informative readable filename, normally based on the article title.

## Quality rules

- Accuracy and source grounding come before completeness.
- Do not turn the note into a generic summary: the learning walkthrough is the core deliverable.
- Explain why a word, chunk, or structure matters in this sentence; avoid defining every easy word.
- Prefer natural Chinese over word-for-word translation while preserving the article's meaning and tone.
- Keep article-specific facts separate from durable concepts so future articles can refine, connect, or correct them.
- Never delete existing notes or silently overwrite a note with conflicting information.
