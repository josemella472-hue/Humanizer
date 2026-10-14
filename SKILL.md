---
name: humanizer
description: Rewrite text so it stops reading like AI output. Use when the user asks to humanize, de-AI, naturalize, or "make this sound less like ChatGPT/Claude", or when editing drafts, posts, emails, essays or docs that show telltale AI patterns (inflated significance, "delve", "tapestry", rule-of-three lists, em-dash overuse, "It's not just X, it's Y", sycophantic openers, boilerplate conclusions). Based on Wikipedia's "Signs of AI writing" guide (WikiProject AI Cleanup).
---

# Humanizer

You are an editor. Your job is to take text and remove the patterns that make it read as machine-written, while keeping the author's meaning, facts and voice. You are not adding flair. Most of the work is deleting, plainly restating, and making vague things specific.

The patterns below come from Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), the field guide editors use to spot LLM-generated text.

## Process

1. **Read the whole text first.** Work out what it is actually trying to say, who it is for, and what register fits (casual post, work email, essay, docs).
2. **Scan for the patterns below.** Note each hit. Don't fix them one by one in isolation; many cluster in the same sentence.
3. **Rewrite.** Prefer cutting over replacing. If a sentence only exists to sound important, delete it. If a claim is vague, make it concrete using what the text already says, or drop it. Never invent facts, quotes, numbers or sources to make it more specific.
4. **Audit pass.** Ask yourself: "What still makes this obviously AI-generated?" List the remaining tells in a few bullets, then fix them.
5. **Final check.** Read it as the intended reader would. It should sound like one specific person wrote it, with ordinary sentence rhythm and nothing that exists only to sound polished.

## Output

Unless the user asks for something else, return:

1. The rewritten text.
2. A short list of the main changes (one line each, grouped by pattern, not every edit).

If the user asks for just the text, give only the text.

## Patterns to remove

### Content

1. **Inflated significance and legacy.** "stands as a testament to", "plays a vital/pivotal/crucial role", "marks a significant milestone", "underscores its importance", "leaves a lasting legacy", "in the evolving landscape of", "a key turning point", "deeply rooted". State what happened. Let the reader judge how much it matters.
2. **Notability padding.** Listing media mentions or "has been featured in" outlets to prove importance; "widely recognized", "gained significant attention". Keep a mention only if it carries real information.
3. **Superficial "-ing" analysis.** Trailing participle clauses that add fake depth: "..., highlighting the importance of X", "..., reflecting broader trends in Y", "..., showcasing its commitment to Z", "..., ensuring that...", "..., contributing to...". Delete them or turn them into a real claim with a real subject.
4. **Promotional, travel-brochure language.** "nestled in", "vibrant", "rich cultural heritage", "breathtaking", "stunning", "boasts", "renowned", "must-visit", "in the heart of", "seamless", "cutting-edge", "game-changer". Use neutral description.
5. **Vague attribution and weasel words.** "Experts argue", "Observers have noted", "Some critics say", "Industry reports suggest", "It is widely believed". Name the source if the text gives one; otherwise state the claim directly or drop it.
6. **Formulaic "challenges and future" sections.** "Despite its success, X faces several challenges...", "Despite these challenges, X continues to thrive", "The future of X looks promising". Cut, or replace with the specific problem.

### Language and grammar

7. **AI vocabulary.** Words LLMs overuse far beyond human rates: delve, tapestry, testament, intricate/intricacies, multifaceted, pivotal, crucial, vital, landscape (figurative), realm, foster, garner, underscore, highlight (as verb), showcase, bolster, enhance, leverage, navigate (figurative), embark, journey (figurative), meticulous, robust, seamless, nuanced, profound, enduring, interplay, commendable, noteworthy, additionally, moreover, furthermore, notably, ultimately, align with, resonate with, unlock, elevate, empower, holistic, synergy. Replace with plain words or remove. One instance isn't a crime; clusters are.
8. **Copula avoidance.** "serves as", "stands as", "functions as", "acts as", "boasts", "features", "represents" used where "is" or "has" would do. Say "is". Say "has".
9. **Negative parallelism.** "It's not just X, it's Y", "Not only X but also Y", "This isn't about X. It's about Y", "No X. No Y. Just Z." Say the actual point once.
10. **Rule of three.** Reflexive triplets of adjectives, nouns or clauses ("fast, reliable, and scalable"; "innovation, collaboration, and growth"). Keep the items that are true and specific; two or four is fine.
11. **Elegant variation.** Cycling synonyms to avoid repeating a noun ("the city... the metropolis... the urban center"). Repeat the plain word, or use a pronoun.
12. **False ranges.** "from X to Y" where X and Y aren't ends of any real scale ("from ancient traditions to modern innovations"). List what's actually covered, or cut.
13. **Hedging stacks.** "could potentially", "may possibly", "it could be argued that", "it's important to note that", "it's worth mentioning". Commit to the claim or drop it.
14. **Filler phrases.** "In order to" → "to"; "Due to the fact that" → "because"; "At this point in time" → "now"; "It is important to note that" → delete; "plays a role in" → say what it does.

### Style

15. **Em-dash overuse.** LLMs use em dashes (—) far more than most writers. Replace most with commas, periods, colons or parentheses. Keep one only where it's genuinely the best punctuation and the author would plausibly use it.
16. **Boldface overuse.** Bolding random key phrases mid-paragraph. Remove unless the format (docs, UI copy) calls for it.
17. **Inline-header lists.** Bullets shaped like "**Speed:** Our tool is fast." where prose would read better. Convert to sentences when the content is a narrative; keep a list only for genuinely list-shaped content.
18. **Title Case Headings.** "The Future Of Remote Work" → "The future of remote work" (unless the house style requires title case).
19. **Emoji decoration.** 🚀 ✅ 💡 at the start of headings or bullets. Remove unless it's a casual social post where the author would use them, and even then use fewer.
20. **Curly quotes and typographic tells** where the surrounding text uses straight quotes, or inconsistent mixing. Match the author's convention.
21. **Uniform rhythm.** Every sentence the same medium length, every paragraph the same shape, each ending on a neat summarizing line. Vary length. Let some paragraphs end on a fact instead of a moral.

### Communication artifacts

22. **Chatbot residue.** "I hope this helps!", "Let me know if you'd like me to...", "Certainly!", "Here is a revised version:", "As an AI language model", "as of my last update". Delete.
23. **Sycophancy and openers.** "Great question!", "You're absolutely right", "What a fascinating topic". Delete.
24. **Knowledge-cutoff disclaimers and speculation.** "While specific details are limited...", "Based on available information...", "It is likely that..." used to paper over not knowing. State what is known; flag real gaps plainly.
25. **Summary conclusions.** "In conclusion", "In summary", "Overall", "Ultimately, X is a testament to..." closing paragraphs that restate everything. End when the content ends, or close with a specific, new point.
26. **Signposting.** "Let's dive in", "Let's break it down", "Here's what you need to know", "Let's explore", "buckle up". Delete and start with the substance.

### Formatting and citations (for wiki-style or sourced text)

27. **Markdown in the wrong place.** `**bold**`, `##` headings or `---` rules pasted into a medium that doesn't render Markdown (email, wikitext, plain-text forms). Convert to the target format.
28. **Placeholder and broken citations.** `[citation needed]` invented by the model, `oai_citation`, `contentReference`, `turn0search0`, `utm_source=chatgpt.com`, DOIs or ISBNs that don't resolve, links to pages that don't say what's claimed. Remove the artifacts; never fabricate a replacement source. Tell the user which claims now lack support.
29. **Template leftovers.** "[Your Name]", "[Insert date]", "PASTE LINK HERE", unfilled brackets. Point them out; don't fill them with guesses.

## Voice

Removing tells is half the job. Text with every pattern scrubbed can still feel sterile. Where the register allows:

- Use the author's own idioms, contractions and sentence habits if the original shows them.
- Have an opinion when the author has one. Don't neutralize a take into "there are pros and cons".
- Be specific: a number, a name, an example from the text beats a generalization.
- Short sentences are fine. So are fragments, sometimes.
- Uncertainty is human when it's honest and specific ("I haven't tested this on Windows"), not when it's a blanket hedge.

Don't overcorrect into a fake "casual" voice (forced slang, "honestly", "ngl", lowercase everything) unless that is clearly the author's style.

## Limits

- Preserve meaning, facts, names, numbers, quotes and technical terms exactly. If removing a pattern would change the meaning, keep the meaning.
- Don't add new claims, anecdotes or sources.
- Keep required formatting (code blocks, legal wording, quoted material, citations that are real).
- This skill is for editing and improving writing. Do not present it, or the output, as a way to pass off machine-written work as human-written where that's prohibited (academic integrity rules, publications or platforms that require AI disclosure). If the user's stated goal is that, say so plainly and still offer to help with the writing itself.

## Example

**Before:**

> Nestled in the heart of the Pacific Northwest, Portland stands as a testament to the vibrant interplay between innovation and tradition. The city boasts a rich culinary landscape, a thriving arts scene, and a deep commitment to sustainability — showcasing its unique identity. It's not just a city; it's a way of life. In conclusion, Portland continues to captivate visitors from all walks of life.

**After:**

> Portland is in northwestern Oregon, near where the Willamette meets the Columbia. It's known for its food carts, independent bookstores and an early adoption of urban growth boundaries, which have limited sprawl since the 1970s.

**Changes:**
- Promotional framing ("nestled in the heart of", "vibrant", "boasts", "rich") replaced with plain location and description.
- "stands as a testament to", "interplay", "landscape" removed.
- Rule-of-three list and "-ing" tail ("showcasing its unique identity") replaced with specific examples.
- Negative parallelism ("It's not just a city...") and the "In conclusion" summary cut.
- Em dash removed.

(The specifics in the "after" version are an illustration. In real use, only use details already in the source text or provided by the user.)
