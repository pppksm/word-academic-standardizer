# Recognition and repair

Use native Word evidence first: paragraph style, outline level, numbering, fields, captions, sections, and object relationships. Then use text patterns, typography, spacing, neighbors, and document position. Never infer structure from one weak signal.

## Recognition
High-confidence headings use Heading 1–4, outline levels, native numbering, or stable patterns 1 Title, 1.1 Title, 1.1.1 Title, 1.1.1.1 Title. Candidates such as 第1章, 一、, （一）, or unnumbered short lines need context. Increase confidence when short, without sentence-ending punctuation, larger Heiti/bold, heading spacing, and a consistent neighboring hierarchy. Decrease confidence for list items, captions, references, headers/footers, code, URLs, experiment steps, and complete sentences.

Abstract and keywords are recognized from 摘要/ABSTRACT and 关键词/Keywords regions. TOC is identified by TOC fields/styles, right-aligned page numbers, or repeated dot leaders. References require a clear title plus repeated bibliographic patterns and stable numbering. Captions must be adjacent to the matching figure/table. Equations take priority from OMML, MathType/OLE, or independent centered math-like paragraphs. Lists use native numbering first; textual markers need neighboring-list evidence.

## Safe numbering conversion
Convert manual heading numbers to one native multilevel list only when levels are high-confidence, at least two peers confirm the pattern, the sequence has no unexplained conflict, and field/bookmark/cross-reference risk is absent. Record visible text and numbers, bind Heading 1–4, remove only duplicate prefixes, update fields, and compare before/after sequences. Roll back or report on jumps, duplicates, resets, or broken references. Never convert uncertain legal/standard clauses, experiment steps, mixed systems, or meaningful manual numbering.

## Objects
Simple inline images may be centered, fit to the text width, and preserve aspect ratio. Preserve floating wrap, anchors, SmartArt, grouped drawings, text boxes, links, bookmarks, and OLE. Simple tables may fit the width, use three-line styling, repeat headers, and stable captions. Never delete columns, merge/reorder data, or reconstruct complex headers automatically. Do not convert MathType/OLE equations or rewrite equations.

## Repair levels
A: ordinary fonts, body indentation/spacing, layout-only empty paragraphs, safe page setup, simple overflow, stale fields. B: heading styles/numbering, captions, chapter breaks, section-aware page numbers, TOC inclusion, image-caption pairing, simple table continuation. C: semantic text/data, equations, citation remapping, complex tables, accepting revisions, deleting comments/objects, protected content, uncertain structure.

Repair page/section baselines and styles first; ordinary paragraphs/components second; structural fields and numbering last; render after each layout-sensitive batch.
