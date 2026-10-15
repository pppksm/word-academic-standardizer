# Protection and quality assurance

## Snapshot
Record file type, size/version, paragraph and character counts, sections, margins, headers/footers, page fields, styles, heading counts, tables and merged-cell patterns, images/drawings, equations/OLE, hyperlinks, bookmarks, fields, TOC/caption fields, comments, tracked changes, protection, and embedded relationships. Keep the original and write a separate output.

## Checks
Compare output with the snapshot. Flag text or paragraph changes, object/equation/table counts, merged cells, bookmarks, hyperlinks, comments, revisions, fields, sections, and citation counts. A structural change must be documented as an intentional A/B repair; C changes are forbidden automatically.

Automate checks for page size/margins, fonts, indentation, line spacing, styles, heading hierarchy, numbering, TOC/captions/cross-references, page numbers, image/table width, empty paragraphs, and missing fields.

Render with the bundled render_docx.py, inspect every page at 100%, and check clipping, overlap, missing glyphs, broken tables, isolated headings, separated captions, equation cropping, header/footer errors, landscape continuity, and line breaks. Re-render after layout-sensitive corrections. XML/text extraction alone is insufficient.

## Reporting
Every issue contains ID, risk A/B/C, location, issue type, evidence, current state, action, verification, risk, and recommendation. Report uncertainty explicitly.

A second run must not add spaces, numbers, breaks, captions, styles, or page resets. If structural work fails, roll it back, keep safe completed repairs, and report the dependency failure. Deliver only after structural comparison, field update, repair documentation, C-level report, full rendered inspection, and original-file preservation.
