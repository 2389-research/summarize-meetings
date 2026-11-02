<!-- ABOUTME: Reference — Granola transcript YAML structure and known quirks. -->
<!-- ABOUTME: Used by the summarize-meetings skill so the body can stay concise. -->

# Granola Transcript Format

Most transcripts come from Granola and have this structure:

```yaml
---
doc_id: uuid
source: granola
created_at: ISO timestamp
title: Meeting Title
participants:
- Person Name
duration_seconds: N
labels: []
creator: '[[Vault Owner]]'
attendees:
- '[[Person Name]]'
summary_text: |-
  ### Section Header
  - Bullet points of AI-generated summary
generator: muesli 1.0
---

# Meeting Title

_Date: YYYY-MM-DD_

## Participants
- **Name**, Role, Company, (email)

## Notes
(Granola-captured notes — may be sparse or detailed)

---

## Transcript

Speaker 1: ...
Speaker 2: ...
```

**Key fields to use:**
- `attendees` — canonical list of who was there
- `summary_text` — Granola's AI summary (useful cross-reference but don't rely solely on it)
- `participants` — sometimes has role/company info
- The transcript body has the real content

**Common transcript quirks:**
- Speaker attribution may be missing or wrong
- Names may be misspelled or use nicknames
- Some transcripts lack `summary_text` entirely
- Very long transcripts (100K+) may have repetitive content from multi-hour sessions
