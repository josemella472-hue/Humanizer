# Humanizer

A Claude Code skill that edits text to remove the patterns that make writing read as AI-generated. It's based on Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) guide, maintained by WikiProject AI Cleanup.

It covers 29 patterns in six groups: content (inflated significance, promotional tone, vague attribution), language (AI vocabulary, "serves as", "not just X but Y", rule of three), style (em dashes, bold, emoji, title case), chatbot residue ("I hope this helps!"), conclusions and signposting, and formatting/citation artifacts. After rewriting, it runs an audit pass that asks what still reads as AI, then fixes what it finds.

## Install

Personal (all projects):

```bash
git clone https://github.com/josemella472-hue/Humanizer.git ~/.claude/skills/humanizer
```

Per project:

```bash
git clone https://github.com/josemella472-hue/Humanizer.git .claude/skills/humanizer
```

## Use

```
/humanizer

<paste your text>
```

Or just ask: "humanize this", "make this sound less like AI", "remove the AI tells from my draft". Claude loads the skill automatically when the request matches.

By default you get the rewritten text plus a short list of what changed. Ask for "just the text" to skip the list.

## What it won't do

- Change facts, numbers, names or quotes
- Invent sources or details to make things more specific
- Help pass off AI-written work as your own where that's against the rules (school assignments, publications that require disclosure)
