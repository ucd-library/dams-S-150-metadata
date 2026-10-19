# Outloud split update - October 19, 2026

The collection now has **43 items and 43 PDFs**, with 2,467 TIFFs and 2,467 transcripts. Outloud is now two 16-page items: **Outloud (Spring 2003)** (`Outloud_2003`) and **Outloud (Winter 2003)** (`Outloud_Winter_2003`). Winter filenames run 001-016. Spring retains its existing ARK; Winter has one pending ARK request. Updated audit: /Users/enebeker/dams-S-150-metadata/work/outloud-split-20261019/audit-final.json; 0 errors, 0 missing binaries, 1 expected missing-ARK warning. Sync/import remain manual.

Current split details, backups and validation: /Users/enebeker/dams-S-150-metadata/work/outloud-split-20261019/HANDOFF.md

---

## Earlier October 9 handoff (historical baseline)

# S-150 PDF accessibility remediation

Collection: **LGBTQ Serials (placeholder title)**  
Root: /Users/enebeker/dams-S-150-metadata  
Date: October 9, 2026

All **42 PDFs / 2,467 scan pages** were re-OCRed from the preserved TIFF masters with Tesseract 5.5.2 and the best English model, at up to 5,000 pixels on the longest side. The original compressed scan images, page dimensions and scan order were preserved. Twenty-eight representative rendered pages compared pixel for pixel with the prior PDFs.

The PDFs contain document/section tags, headings, paragraphs, lists, page bookmarks, document title and language, embedded Unicode text, **2,702 visually reviewed Figure alternatives**, **168 manually transcribed tables/forms**, and **149 reviewed text replacements**. Captions are associated with their figures and table headers carry column scopes. All 2,467 scans were visually reviewed for meaningful figures; this does not mean every OCR paragraph was proofread. Reflowable HTML reading editions accompany the PDFs as local access/review files.

## Validation and limits

The target is WCAG 2.1 Level AA for ADA Title II, with PDF/UA-1 used for machine-verifiable PDF structure. All 42 PDFs passed qpdf syntax and independent structure/font/image-preservation checks. VeraPDF UA-1 reports 2 compliant files and 40 files failing only the deliberately omitted identification declaration, with no other machine-verifiable failures. All 2,467 compressed scan images and placement matrices matched the originals exactly. The technical evidence is in technical-validation-summary.json, technical-validation.json and verapdf-ua1.json. Those checks do not establish complete WCAG or legal compliance. See [the target and source memo](/Users/enebeker/dams-S-150-metadata/work/accessibility-20261009/accessibility-target-and-evidence.md).

The two short newsletters, The Davis Voice and the cataloged Gay News item with the Gay Students Newsletter masthead, have visually corrected text and reviewed logical reading order. Those two include the PDF/UA-1 identification declaration. The remaining 40 PDFs deliberately omit that declaration: final OCR proofreading and logical reading-order review are unfinished. The expected missing-identification validator result must not be represented as full PDF/UA compliance.

**These PDFs are substantially remediated, but ADA Title II/WCAG compliance has not been established.** Remaining checks include:

- Proofread uncertain OCR and confirm article, advertisement and caption order in the 40 longer PDFs, including continuations across scans.
- Review the per-page complex-content findings: matching quizzes, candidate/endorsement rosters, directories, product/price associations, poetry line breaks and remaining rotated text. Identified tables and selected difficult advertisements were transcribed; this was not exhaustive line-by-line review.
- OutLOUD has structured crossword clues and source answer lists, with missing printed answers identified. Grid intersections are not encoded. Two Magpie crossword grid/story-clue associations and musical pitch/rhythm need further equivalent alternatives.
- Test meaningful reading, navigation and reflow in actual assistive technology and PDF readers. Acrobat was available but its automation interface exposed neither a usable document accessibility tree nor screenshots. Successful screen-reader and PDF reflow tests could not be verified. The HTML editions provide visible, resizable text and semantic tables for review.
- Review catalog/source anomalies without changing source evidence: Gay News masthead/title mismatch; the first Male Express issue starts with an advertisement; OutLOUD combines Spring and Winter 2003 source sets; issue17 includes a 1992 Queer L.A. insert; several dark/narrow scans and inconsistent printed names/amounts are retained and flagged.

The complete page log is [accessibility-review.csv](/Users/enebeker/dams-S-150-metadata/work/accessibility-20261009/accessibility-review.csv). Detailed visual notes, the early pending semantic inventory, and the table/Magpie handoffs are included. A low-confidence score is a review priority, not a corrected transcription or a compliance result.

## Locations and recovery

- Current PDFs: /Users/enebeker/dams-S-150-metadata/items/<key>/media/<key>.pdf
- Updated transcripts: /Users/enebeker/dams-S-150-metadata/items/<key>/media/text/
- Evidence, semantic manifests, grounded annotations and review logs: /Users/enebeker/dams-S-150-metadata/work/accessibility-20261009/
- Reflowable reading editions: [index.html](/Users/enebeker/dams-S-150-metadata/work/accessibility-20261009/reading-editions/index.html)
- Backup of every replaced PDF, transcript, sidecar and build/delivery record: /Users/enebeker/dams-S-150-metadata/work/pre-accessibility-20261009/
- Refreshed local package audit: /Users/enebeker/dams-S-150-metadata/work/audit-20261009-accessibility.json

TIFF masters, item catalog metadata, authority labels, existing real ARKs and rights statements are preserved. The rights statement remains In Copyright — Educational Use Permitted. The collection ARK is ark:/87293/d3c53fc01.

## Reproducibility and manual delivery

The evidence folder contains the writer, assembler, native OCR extractor, best English model, full OCR region cache, visual annotations, reviewed semantic manifests and per-item reports. The staged PDFs and original working copies also remain in the chat workspace at /Users/enebeker/Documents/Codex/2026-10-05/i/work/s150-accessibility. To recreate OCR from the masters, run reocr_all.py with the bundled Python; build_ready.py then assembles candidates from the cached OCR and reviewed annotations. The build state records pre_accessibility_path so later builds use the backed-up original scan PDF rather than accumulating overlays. Do not run the promotion script again without inspecting the existing backup and current hashes.

Syncing, DAMS importing and publication remain **manual**. The import package remains collection/ and items/. Keep work/ as local build evidence. Do not describe a passing local collection audit as an accessibility certification.

Final local package audit: 5,147 JSON-LD files; 42 items; 4,977 local media; 0 missing binaries, 0 errors and 0 warnings. This is a package-structure result, not an accessibility compliance determination.
