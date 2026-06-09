---
id: AGENTS
aliases: []
tags: []
---

# AGENTS.md — Jarvis Assistant Operating Manual

## Purpose

This file is the single source of truth for how the Jarvis AI assistant operates inside this vault. Read this file first before doing anything.

---

## 1. Vault Overview

```
second-brain-template/
├── AGENTS.md          ← assistant rules (never modify unless asked)
├── README.md          ← vault overview
├── index.md           ← vault map (update when structure changes)
├── log.md             ← change log (append every mutation)
├── .gitignore
├── inbox/              ← capture zone (one file per topic, lands here first)
├── todo/              ← task management
│   ├── 1.todo.md     ← pending tasks
│   ├── 3.done.md     ← completed tasks (with completion date)
│   └── plan/          ← project plans (architecture + build phases)
├── dailyNote/         ← daily journal (YYYY-MM-DD.md)
├── templates/         ← reusable templates
│   ├── daily.md
│   ├── note.md
│   ├── project.md
│   ├── area.md
│   ├── resource.md
│   └── archive.md
├── assets/imgs/       ← static images
└── wiki/              ← PARA knowledge base
    ├── 1.project/     ← active projects with deadline
    ├── 2.area/        ← ongoing responsibilities (no deadline)
    ├── 3.resource/    ← reference material
    │   ├── bookmarks.md
    │   ├── command/
    │   ├── history/
    │   ├── person/
    │   ├── snippet/
    │   ├── tools/
    │   └── prompt/
    └── 4.archive/     ← inactive items
```

---

## 2. PARA Quick Reference

| Category       | Definition                              | Deadline? | Example                       |
| -------------- | --------------------------------------- | --------- | ----------------------------- |
| **1.project**  | Active project with outcome + deadline  | Yes       | Launch website, Learn Rust    |
| **2.area**     | Ongoing responsibility, no end date     | No        | Health, Finances, Career      |
| **3.resource** | Reference material for interest/utility | No        | Git commands, Book notes      |
| **4.archive**  | Inactive items from any category        | N/A       | Completed projects, old notes |

```
1.project ──(done)──► 4.archive
2.area ──(inactive)──► 4.archive
3.resource ──(irrelevant)──► 4.archive
4.archive ──(revived)──► 1.project / 2.area / 3.resource
```

---

## 3. Ingest Pipeline

### Rules

1. **ALL new content starts in `inbox/`** — one file per topic, no exceptions
2. **CHECK TEMPLATES FIRST** — use matching template as base. Never write without consulting templates.
3. **Ingest = classify + distribute** — read inbox, classify by PARA category, write to correct wiki location using matching template
4. **After ingest, delete the file from `inbox/`**
5. **Log every ingest** — append to `log.md`
6. **Never skip the pipeline** — never write directly to wiki (unless user overrides)
7. **If no template matches, create one first** — write a new template under `templates/`, then use it. Never write a note without a template.
8. **Update index.md** — when structure changes (new file, moved file, new folder)

### Classification

```
  PHASE 1: PARA CATEGORY
  deadline? ──YES──► 1.project/
  ongoing?  ──YES──► 2.area/
  reference?─YES──► 3.resource/
  else ───────────► dailyNote / discard

  PHASE 2: CONTENT SHAPE (resources only)
  CLI commands?   ──► command/
  Code blocks?    ──► snippet/
  Tool/app info?  ──► tools/
  Person/contact? ──► person/
  Links saved?    ──► bookmarks.md
  Timeline/log?   ──► history/
```

### Compound Topic Rules

| #   | Rule                                                                  |
| --- | --------------------------------------------------------------------- |
| 1   | **3+ distinct content shapes** for same topic → create hub + children |
| 2   | Hub file at `wiki/3.resource/<topic>.md` using `resource.md` template |
| 3   | Each child uses its own template in the correct subfolder             |
| 4   | Hub links to all children, children link back to hub                  |
| 5   | **1-2 shapes** → single file using primary shape's template           |
| 6   | Log each file created as a separate ingest entry                      |

---

## 4. Template Map

| Template           | Destination                    | type                | Extra    |
| ------------------ | ------------------------------ | ------------------- | -------- |
| `daily.md`         | `dailyNote/YYYY-MM-DD.md`      | `"daily"`           | —        |
| `note.md`          | Anywhere                       | `"literature-note"` | —      |
| `project.md`       | `wiki/1.project/*.md`          | `"project-note"`    | —        |
| `area.md`          | `wiki/2.area/*.md`             | `"area"`            | —        |
| `resource.md`      | `wiki/3.resource/*.md`         | `"resource"`        | `source` |
| `archive.md`       | `wiki/4.archive/*.md`          | `"archive"`         | —        |
| `profile.md`      | `wiki/2.area/me.md`            | `"area"`            | —        |
| `daily-schedule.md`| `wiki/2.area/daily-schedule.md` | `"area"`            | —        |

When a new note type appears, create the template first, then add a row here.

---

## 5. Formatting Rules

### 5.1 General

- Unix line endings (LF), UTF-8, no trailing whitespace, soft 100-char line limit

### 5.2 YAML Frontmatter

Every file **must** start with a YAML frontmatter block.

```yaml
---
title: "Note Title"
aliases:
  - "Alternate Name"
tags:
  - type/literature-note
  - para/resource
  - status/todo
created: YYYY-MM-DDTHH:MM:SSZ
updated: YYYY-MM-DDTHH:MM:SSZ
type: "literature-note"
id: "YYYYMMDDHHmm"
source: ""
---
```

| Field     | Type            | Required | Description                             |
| --------- | --------------- | -------- | --------------------------------------- |
| `title`   | string (quoted) | Yes      | Human-readable title                    |
| `aliases` | list of strings | No       | Alt names for `[[wikilink]]` resolution |
| `tags`    | list of strings | Yes      | Hierarchical: `category/subcategory`    |
| `created` | ISO 8601        | Yes      | `YYYY-MM-DDTHH:MM:SSZ`                  |
| `updated` | ISO 8601        | No       | Last modification timestamp             |
| `type`    | string (quoted) | Yes      | Note type classification                |
| `id`      | string (quoted) | Yes      | `YYYYMMDDHHmm`                          |
| `source`  | string (quoted) | No       | Origin URL or reference                 |

Tag taxonomy: `type/` (literature-note, project-note, daily, resource, archive) + `para/` (project, area, resource, archive) + `status/` (todo, in-progress, done).

### 5.3 Markdown Style

- `#` H1, `##` H2, `###` H3 — never skip levels
- **Bold** for emphasis, `code` for technical terms
- `-` for unordered, `1.` for ordered
- `[[wikilinks]]` for internal, `[text](url)` for external
- No inline HTML unless necessary

### 5.4 File Naming

All files use `kebab-case.md`. Daily notes: `YYYY-MM-DD.md`.

### 5.5 Section Structure (per note)

```markdown
# Title

> Brief one-line description.

## Overview

Context and summary.

## Content

Main body.

## References (optional)

- [[linked-note]]
- [external](url)
```

### 5.6 Log Entry Format

```markdown
## YYYY-MM-DD

### HH:MM — action description

- what changed
- where it went
```

---

## 6. Jarvis Behavior Rules

### DO

- Always read `AGENTS.md`, `index.md`, and `todo/1.todo.md` before working
- On every vault mutation (create, edit, move, delete), update `index.md` and `log.md`
- Maintain the PARA structure inside `wiki/`
- Ask the user when classification is ambiguous
- Keep notes concise and scannable
- Use tables for 3+ items with multiple attributes
- Use ASCII diagrams for process/structure

### DO NOT

- Never modify `AGENTS.md` unless the user explicitly requests it
- Never write directly to `wiki/` without inbox ingestion (unless user overrides)
- Never delete content — always move to `wiki/4.archive/`
- Never add comments or emoji unless the user asks
- Never invent or guess external URLs
