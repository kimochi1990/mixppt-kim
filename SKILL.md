---
name: mixppt-kim
description: Create, redesign, beautify, review, and quality-check presentations, PowerPoint files, PPTX decks, slides, and presentation PDFs. Use when the user wants a new visually polished deck, an editable PPTX plus matching PDF, a redesign of an existing PPTX/PDF, stronger storytelling, a coherent visual system, or presentation art direction and QA.
---

# MixPPT Kim

## Outcome

Deliver an editable, presentation-ready `.pptx` and a visually matching `.pdf`. Act as the art director and workflow orchestrator; delegate file-format work to the installed specialist skills.

## Required workflow

1. Inspect all source material. Preserve original files unless the user explicitly requests in-place editing.
2. Infer audience, purpose, language, duration, and brand constraints. Ask only for information that cannot be safely inferred and would materially change the result.
3. Build the story spine before styling. Read [storytelling.md](references/storytelling.md).
4. Propose two or three context-specific art directions and recommend one. Read [art-direction.md](references/art-direction.md).
5. For visually consequential work, confirm the outline and one representative sample slide before producing the full deck.
6. Generate or redesign the editable PPTX using the presentation specialist.
7. Export a matching PDF using the presentation runtime or PDF specialist.
8. Render every slide and page. Inspect a montage for rhythm and representative full-resolution pages for defects.
9. Correct issues and repeat rendering until the quality gates pass.
10. Deliver both artifacts and briefly disclose content cuts, font substitutions, missing capabilities, or other material compromises.

## Dispatch

Before using a dependency, read its complete `SKILL.md` and follow it faithfully.

- PPTX creation, editing, rendering, and validation: `presentations:Presentations`.
- PDF inspection, export, rendering, and validation: `pdf:pdf`.
- Bespoke hero imagery, illustration, texture, or visual concepts: `imagegen`.
- DOCX and other document sources: `documents:documents`.
- Spreadsheet-backed charts, tables, and analysis: `spreadsheets:Spreadsheets`.

Use only the dependencies needed for the task. If one is unavailable, state the limitation and select the safest available fallback; never claim an artifact was produced when it was not.

## New deck route

1. Extract facts, hierarchy, evidence, and desired decision or audience response.
2. Create a title-only narrative that stands on its own.
3. Map the narrative to slide purposes and select an art direction.
4. Build a representative sample containing real content, not placeholder copy.
5. Generate the full editable deck, matching PDF, and speaker notes when requested or useful for live delivery.

## Existing file route

1. Preserve the source and work on a copy.
2. Inventory slide/page count, content, masters, fonts, colors, imagery, charts, citations, and notes.
3. Diagnose narrative, hierarchy, density, consistency, and rendering problems.
4. Distinguish visual restyling from structural rewriting. Report intentional cuts or material rewrites.
5. Rebuild native slide elements where editable output is expected; do not flatten the whole deck into images merely for convenience.

## Quality gates

Read and execute [qa-checklist.md](references/qa-checklist.md). At minimum:

- The slide titles alone communicate a coherent story.
- Every slide has one clear communicative purpose.
- No overflow, overlap, clipping, broken glyphs, unintended font fallback, low-resolution images, or temporary placeholders remain.
- Charts and tables are legible, correctly labeled, and visually emphasize the conclusion.
- Contrast and typography are accessible at presentation distance.
- PPTX and PDF slide/page counts, order, content, and appearance match.
- Expected elements in the PPTX remain editable.

## Deliverables

- Editable `.pptx`.
- Matching `.pdf`.
- Speaker notes when requested or useful.
- Source workspace when it materially improves future iteration.

Use clear filenames. Do not overwrite the user's source by default.

## Failure rules

- Missing fonts: use an appropriate installed substitute and disclose it.
- Corrupt or unsupported input: attempt read-only recovery, identify the blocked content, and preserve the original.
- Export mismatch: treat PPTX as the editable source of truth, correct it, and regenerate the PDF.
- Image-generation failure: use typography, diagrams, native shapes, or properly licensed/user-provided imagery.
- Dense content: edit, split, or restructure; do not solve fit problems by shrinking body text below legibility.
- Uncertain claims or missing citations: request or verify sources; never fabricate evidence.

## References

- Visual systems and composition: [art-direction.md](references/art-direction.md)
- Narrative and evidence: [storytelling.md](references/storytelling.md)
- Final verification: [qa-checklist.md](references/qa-checklist.md)
- GitHub research basis: [github-sources.md](references/github-sources.md)
