# Article access and input modes

## Mode A: URL

For an NYT URL, attempt ordinary retrieval with the tools available in the current environment. “Full article available” means the article body can be read reliably enough to preserve its original order and analyze its sentences. A title, abstract, search snippet, related article, cached fragment, or third-party summary is not the full article.

Stop if access is blocked by CAPTCHA, paywall, subscription or login requirements, browser security policy, automated-access protection, robots restrictions, or another access limitation. Do not bypass the control. Do not keep searching for substitute copies in order to reconstruct the missing article. Ask the user to paste the complete text using the exact Chinese fallback sentence in `SKILL.md`.

## Mode B: user-provided text

The user's pasted article text is the primary source. Preserve its original order for the walkthrough. When copying text includes webpage furniture, remove only obvious navigation, ads, subscription prompts, recommendations, and unrelated interface material. Keep meaningful captions, headings, bylines, dates, and article paragraphs.

If the paste appears incomplete—such as ending mid-sentence, containing only an excerpt, or omitting the body—do not call it a complete article. Ask for the missing text. Do not fill gaps from search results or memory.

## Source labeling

Use two explicit source labels in the article note:

- **Primary article source:** the NYT URL when the full URL article was successfully retrieved, or “User-provided article text” when the user pasted the text.
- **Background research sources:** external sources used only for context, definitions, chronology, institutions, data, or broader implications.

Sentence-level translation, grammar analysis, and article claims must be grounded in the primary source. Background sources may clarify what the article assumes, but they cannot replace missing article paragraphs or prove that the NYT reported something not present in the primary source.
