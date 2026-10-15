---
name: word-academic-standardizer
description: Standardize Chinese academic Word documents with a conservative thesis-style layout while preserving content, native Word structure, formulas, references, tracked changes, comments, and embedded objects. Use for .docx formatting, structure normalization, numbering, captions, TOC, sections, and layout QA; do not use for rewriting content or changing academic meaning.
metadata:
  short-description: Safely normalize academic Word formatting
---

# Word Academic Standardizer

Use for Chinese academic .docx files: dissertations by default, plus course papers, research reports, literature reviews, and technical reports. Produce a maintainable Word document, not a visual-only cleanup.

Preserve text, section logic, equations, data, references, citations, comments, tracked changes, bookmarks, hyperlinks, and embedded/OLE objects. Apply only changes supported by evidence.

## Authority and risk

Apply rules in this order: user instruction; supplied university or organization template; consistent existing document pattern; the defaults in references; isolated unexplained formatting.

Classify changes:
- A: low-risk direct formatting, page setup, ordinary paragraph spacing, simple image/table sizing, layout-only empty paragraph cleanup, and safe field refresh.
- B: structural heading recognition, manual-number conversion, captions, sections, TOC, cross-references, page restarts, floating-object changes, and multi-page tables. Do only with consistent evidence.
- C: semantic text/data/equation changes, citation remapping, complex merged-table reconstruction, MathType conversion, accepting revisions, deleting comments, removing objects, or changing protected content. Detect and report only.

When uncertain, preserve the source and report the location, evidence, and manual-review recommendation.

## Workflow

1. Read the document and any supplied template.
2. Read relevant references: formatting-defaults.md, recognition-and-repair.md, qa-and-protection.md.
3. Snapshot paragraphs, characters, sections, styles, headings, tables, images, equations, fields, bookmarks, hyperlinks, comments, revisions, protection, and embedded objects.
4. Build an A/B/C repair plan before mutation.
5. Create or update native Word styles, multilevel numbering, captions, fields, and sections.
6. Apply A fixes, then justified B fixes. Never perform C mutations.
7. Update TOC, figure/table lists, captions, cross-references, bookmarks, and page fields where supported.
8. Compare the output with the snapshot.
9. Render the DOCX with the bundled documents renderer and inspect every page at 100% zoom. Re-render after layout-sensitive changes.
10. Deliver the normalized DOCX, a concise issue report, and the untouched original.

Follow the documents skill's artifact-operation marker and render-and-verify workflow. Use bundled workspace runtimes, not system Python, Node, LibreOffice, or global packages.

## Invariants

- Prefer native Word styles, fields, captions, numbering, and section mechanisms.
- Use automatic heading numbering; do not leave duplicate manual numbers.
- Preserve editable OMML, MathType, and OLE equations.
- Preserve floating wrapping, complex merged tables, SmartArt, anchors, hyperlinks, bookmarks, comments, and revisions unless a user explicitly requests a high-risk action.
- Use real page-number fields.
- Do not solve layout by changing content, shrinking below configured minimums, or inserting repeated spaces and blank paragraphs.
- Keep the process idempotent and report unresolved uncertainty.

## Default profile

A4; margins 30 mm left and 25 mm on the other sides; 15 mm header/footer distance; Songti 12 pt body, Times New Roman for Latin text and digits, Heiti headings; justified body with two-character first-line indent and 1.5 line spacing; heading levels 1, 1.1, 1.1.1, 1.1.1.1; three-line tables; chapter-based captions; Roman front-matter page numbers; Arabic numbering from main text; native three-level TOC.

Read the references for complete parameters and repair boundaries.
