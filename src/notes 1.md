Status: fixing paragraph detection for skewed pages (the front-matter page drifts left to right), then rebuilding and re-checking the front-matter footnotes.

I made 13 semantic HTML files, one per PDF, and none of them has been proofread. The text is only as clean as the PDFs' existing OCR, so expect errors, and I didn't check the output page by page against the PDFs.

Each file uses `<article>`, `<header>`, `<section>`, headings, paragraphs and lists. Quoted passages are `<blockquote>`, and the footnotes sit at the end as an ordered list in a section marked `role="doc-endnotes"`.

- **01-acknowledgments-and-preface**: has Acknowledgments, Preface, a Note on Transliteration subsection, and footnotes 1–3.
- **02-glossary**: a definition list of 167 abbreviations. I re-OCR'd these four pages, because the text layer scrambled the columns.
- **03 to 13**: the eleven chapters, each with its own footnotes at the end.

I left out photo and illustration captions, running page headers, page numbers and diagram labels.

Things to check:
- **OCR errors remain in the body text.** Examples are `P,ll` for "All" and `Korolev` spelled `Koroleu`. Some pages came through with no spaces between words, and I only partly repaired those.
- **Footnote markers in the body text were garbled by the OCR.** I stripped them, so the footnotes are not linked to where they were cited. A few footnote numbers are missing in some chapters (chapter 10, "Looking to the Future", has the most gaps).
- **Headings are not complete.** Bold headings were caught reliably, but some subheadings were missed or merged. For example, "Raketa" and "The Purges" in chapter one needed manual fixes.
- **Tables and diagram text are not reconstructed.** A few table rows appear as short paragraphs or bullets, for example in chapters 8 and 10.

The files are named by chapter, from `03-chapter-presage.html` through `13-chapter-three-steps-to-the-moon.html`.