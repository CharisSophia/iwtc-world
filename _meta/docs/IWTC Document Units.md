This document defines **what counts as a single indexable document** for each type of source material in `_local/`.

These rules govern evidence indexing only. Polished or synthesized content (Storylines, Plotlines, World Mechanics, etc.) is **out of scope** for v1.

---
## Scope

Applies to the following `_local` directories:

- `pbp_transcripts/`
- `raw_session_notes/`
- `auto_transcripts/`
- `recollections/`
- `planning_notes/`

The `references/` directory is **explicitly omitted** from v1 and will be revisited later.

---
## Document Unit Rules

### PbP Transcripts

- **doc_type:** `pbp_transcript`
- **Document unit:** one file = one document
- **Rationale:**
    - File boundaries are intentional and meaningful
    - PbP transcripts are the highest-fidelity capture
    - Later chunking may occur, but file-level indexing preserves provenance

---
### Auto Transcripts

- **doc_type:** `auto_transcript`
- **Document unit:** one file = one document
- **Rationale:**
    - Typically represent a single live session
    - Linear, time-ordered capture
    - Treated like PbP transcripts for v1

---
### Raw Session Notes

- **doc_type:** `raw_session_notes`
- **Document unit:** one session × one storyline = one document
- **Rationale:**
    - A single session may cover multiple storylines
    - Each storyline segment represents a distinct evidentiary thread
    - This is the only v1 case where one file may yield multiple documents

---
### Recollections

- **doc_type:** `recollection`
- **Document unit:** one top-level section = one document
- **Partitioning rule:**
    - Split by top-level header formatting (`#`, `##`, etc.)
- **Rationale:**
    - Recollections are mentally authored, non-linear artifacts
    - Section boundaries encode intent and scope
    - Prevents conflation of unrelated memories

---

### Planning Notes

- **doc_type:** `planning_notes`
- **Document unit:** one top-level section = one document
- **Partitioning rule:**
    - Split by top-level header formatting (`#`, `##`, etc.)
- **Rationale:**
    - Planning notes capture intent, not outcomes
    - Section-level indexing avoids artificial chronology
    - Supports later comparison between plan and play

---
## Explicit Non-Rules

- Documents are **not** split by:
    - individual messages
    - character turns
    - emotional beats
    - combat rounds
- Chunking and semantic segmentation are **out of scope** for v1.

---
## Versioning Notes

- This document defines **v1** document units.
- Changes to document-unit rules must increment the version and document rationale.
- References will be introduced in a later version after review of published PDFs.