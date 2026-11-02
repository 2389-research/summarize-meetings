<!-- ABOUTME: Reference — verbatim YAML/Markdown templates for People, Concept, Project, and Summary files. -->
<!-- ABOUTME: Used by the summarize-meetings skill so the body can stay concise. -->

# Templates

## People Note Stub

```yaml
---
title: "Firstname Lastname"
date: YYYY-MM-DD
tags: [people]
aliases: []
type: person
company: (if known from meeting)
role: (if known from meeting)
how-we-met: "Met in [[Meeting Note Title]] context"
last-contact: YYYY-MM-DD
status: active
related: ["[[Summary File]]"]
---

# Firstname Lastname

## Context
- **Company/Org:** (if known)
- **Role:** (if known)
- **How we met:** From [[Meeting Note Title]]

## Notes
- (context extracted from meeting)

## Key Quotes

## Action Items
```

**File naming:** `People/Firstname Lastname.md` — Title Case, NEVER kebab-case for people.

---

## Concept Note

```yaml
---
title: "Concept Name"
date: YYYY-MM-DD
tags: [concept]
type: concept
status: active
related: ["[[Summary File]]", "[[Person Who Articulated It]]"]
---

# Concept Name

## What is it?
(extracted from meeting context)

## Why it matters
(inferred from discussion)

## Connections
- [[Summary File]]
- [[Person]] — who articulated or contributed to this concept

## Sources / References
- [[Summary File]] — extracted from meeting on YYYY-MM-DD
```

---

## Project Stub

```yaml
---
title: "Project Name"
date: YYYY-MM-DD
tags: [project]
type: project
status: active
started: YYYY-MM-DD
related: ["[[Summary File]]"]
---

# Project Name

Mentioned in [[Summary File]]: (brief context)
```

---

## Summary File

Write to: `Meetings/YYYY-MM-DD-slugified-meeting-title-summary.md`

**Slug generation:** Use the most descriptive part of the filename. Drop common prefixes like "hangout-", "call-". Keep it recognizable.

```yaml
---
title: "Summary: Meeting Title"
date: YYYY-MM-DD
tags: [meeting-summary]
type: meeting
source: "[[Original Transcript Filename]]"
status: reference
related: ["[[Person 1]]", "[[Project X]]", "[[Concept Y]]"]
---
```

```markdown
# Summary: Meeting Title

> Source: [[Original Transcript Filename]]
> Date: Month DD, YYYY
> Attendees: [[Person 1]], [[Person 2]]

## Meeting Summary

(A strong 2-4 paragraph narrative summary capturing the substance of the
conversation. What was the meeting about? What were the key themes? What
decisions were made or directions set? What was the energy/vibe? This should
read like a well-written meeting recap that someone who wasn't there could
read and fully understand what happened and why it mattered.)

## Key Topics

(Organized by discussion thread — use subheadings for distinct topics)

## People
| Person | Role/Context |
|--------|-------------|
| [[Person Name]] | context/role/relevance from this meeting |

## Action Items
- [ ] Task description — owner if known

## Project Ideas
- [[Project Name]] — what was discussed, potential next steps

## Blog Ideas
- **Idea title** — why it's worth writing about, angle to take

## Knowledge Graph
- [[Entity A]] <-> [[Entity B]] — nature of relationship/connection

## Concepts
- [[Concept Name]] — brief description and why it matters

## Ideas
- Idea description — enough context to act on later

## Key Quotes
> "Notable quote" — [[Speaker]]
```
