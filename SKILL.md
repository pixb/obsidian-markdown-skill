---
name: obsidian-markdown-skill
description: Create and edit Obsidian Flavored Markdown with wikilinks, embeds, callouts, properties, and other Obsidian-specific syntax. Use when working with .md files in Obsidian, or when the user mentions wikilinks, callouts, frontmatter, tags, embeds, or Obsidian notes.
license: MIT
metadata:
  author: pix
  version: 1.0.0
  created: 2026-09-21
  last_reviewed: 2026-09-21
  review_interval_days: 30
  category: writing
  tags:
    - obsidian
    - markdown
    - notes
activation: /obsidian-markdown-skill
provenance:
  maintainer: pix
  source_references:
    - https://help.obsidian.md
---

# /obsidian-markdown-skill

This skill enables agents to create and edit valid Obsidian Flavored Markdown.

## Trigger Examples

- "Create a new note in Obsidian format with a task list."
- "Edit my daily note to add a callout for an important event."
- "Convert this standard Markdown to Obsidian Flavored Markdown."
- "How do I link to a specific heading in another note?"
- "What is the syntax for a block quote with a footnote?"

## Gotchas

- **No Wikilinks in Standard Markdown**: Standard Markdown editors do not render `[[wikilinks]]`. Use `[text](url)` for external links.
- **Frontmatter is YAML**: Obsidian uses YAML for frontmatter. Ensure proper indentation and syntax.
- **Block IDs**: Block IDs (e.g., `^my-id`) must be at the end of the paragraph, not on a new line (except for lists and quotes).
- **Embeds vs Links**: `![[Note]]` embeds the note, while `[[Note]]` links to it.
- **Callout Nesting**: Nested callouts require a blank line between the outer and inner callout markers.

## Overview

Obsidian uses a combination of Markdown flavors:

- [CommonMark](https://commonmark.org/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [LaTeX](https://www.latex-project.org/) for math
- Obsidian-specific extensions (wikilinks, callouts, embeds, etc.)

## Properties (Frontmatter)

Properties use YAML frontmatter at the start of a note:

```yaml
---
title: My Note Title
date: 2024-01-15
tags:
  - project
  - important
aliases:
  - My Note
  - Alternative Name
cssclasses:
  - custom-class
status: in-progress
rating: 4.5
completed: false
due: 2024-02-01T14:30:00
---
```

### Property Types

| Type | Example |
| ------ | --------- |
| Text | `title: My Title` |
| Number | `rating: 4.5` |
| Checkbox | `completed: true` |
| Date | `date: 2024-01-15` |
| Date & Time | `due: 2024-01-15T14:30:00` |
| List | `tags: [one, two]` or YAML list |
| Links | `related: "[[Other Note]]"` |

## Tags

```markdown
#tag
#nested/tag
#tag-with-dashes
#tag_with_underscores
```

Tags can contain:

- Letters (any language)
- Numbers (not as first character)
- Underscores `_`
- Hyphens `-`
- Forward slashes `/` (for nesting)

## Keywords

`obsidian`, `markdown`, `wikilinks`, `embeds`, `callouts`, `frontmatter`, `tags`, `properties`, `block-ids`, `mermaid`, `latex`, `math`, `task-lists`, `footnotes`, `internal-links`, `note-taking`, `knowledge-management`

## Detailed Syntax

For comprehensive syntax examples (lists, tables, math, diagrams, etc.), see `references/obsidian-syntax.md`.
