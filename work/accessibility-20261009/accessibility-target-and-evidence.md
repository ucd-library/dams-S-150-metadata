# S-150 PDF accessibility target and evidence

Research checked October 9, 2026. This memo concerns the 42 scanned historical serial PDFs (2,467 pages) described in the collection build; it does not certify those documents.

## Target

Use **WCAG 2.1 Level AA** as the Title II technical target, with **PDF/UA-1** as a complementary PDF structure target. DOJ expressly includes public universities and documents among the entities/content covered. The current DOJ fact sheet also records an April 20, 2026 deadline extension to April 26, 2027 (50,000 or more population) / April 26, 2028 (smaller entities and special districts). A passing PDF/UA machine report is evidence about PDF structure; it is not a complete Title II/WCAG determination. [DOJ fact sheet](https://www.ada.gov/resources/2024-03-08-web-rule/), [WCAG 2.1](https://www.w3.org/TR/WCAG21/)

## Meaningful checks for this collection

- Re-OCR from source scans, preserve all pages and their order, and reconcile extracted text with the visible content. Review uncertain words, skew/rotation, bleed-through, small type, ligatures, punctuation, and text embedded in artwork. Do not hallucinate illegible text; retain a review finding. W3C's OCR technique includes correcting suspects, tagging, and testing whether text is read accurately and in order. [W3C PDF7](https://www.w3.org/WAI/WCAG22/Techniques/pdf/PDF7.html)
- Represent the actual content with meaningful tags: document/sections, hierarchical headings, paragraphs, lists, tables with header associations, captions, links, and figures. Do not call a document remediated merely because every page has one paragraph tag. Test multi-column articles, sidebars, footnotes, continuation notices, advertisements, and page transitions in their logical reading sequence. Test keyboard focus for any interactive content. [W3C PDF3](https://www.w3.org/WAI/WCAG22/Techniques/pdf/PDF3.html)
- Give informative photographs, illustrations, logos, cartoons, charts, and other images content-specific alternatives that convey their information or purpose. Important words in images must be available as text. Descriptions must come from viewing the actual figure, not its filename. Generic alternatives such as “image on page 7” are not equivalent content. [W3C PDF1](https://www.w3.org/WAI/WCAG22/Techniques/pdf/PDF1.html)
- Mark only decorative or redundant visual content as artifacts. A background scan whose meaningful text and figures are represented completely by tagged accessible counterparts can be treated as redundant. Declaring a complete page scan an artifact without representing its meaningful illustrations would hide content. [W3C PDF4](https://www.w3.org/WAI/WCAG22/Techniques/pdf/PDF4.html)
- Check the remaining applicable WCAG AA criteria: title, document and passage languages, navigation, semantic relationships, correct sequence, text alternatives, text size/reflow, and contrast. For these historical layouts, test an actual reader's reflow at 400%/narrow width, and verify no information disappears or interleaves. Record applicability and results; do not assume scanned text or preserved original appearance is an automatic exception. [WCAG 2.1](https://www.w3.org/TR/WCAG21/)
- Verify meaningful reading with a screen reader/accessibility API, alongside visual comparison of rendered pages. Automated syntax checking cannot judge whether alt text conveys the figure, the correct article follows each paragraph, a heading hierarchy reflects content, or OCR is accurate. The PDF Association's Matterhorn Protocol distinguishes human and machine checkpoints; reading order is explicitly a human check. [Matterhorn Protocol](https://pdfa.org/resource/the-matterhorn-protocol/), [PDF Association reading-order technique](https://pdfa.org/techniques-for-accessible-pdf/order-of-marked-content-sequences-within-a-tag-correctly-set/UA1_Tpdf-G4_02/)

## Installed validator and reproducible commands

Observed `/opt/homebrew/bin/verapdf --version`: **veraPDF 1.30.0**, built June 3, 2026. The Homebrew wrapper uses `/opt/homebrew/Cellar/verapdf/1.30.2/libexec/`. Java prints reflective-field warnings on stderr; those are separate from PDF validation findings.

Validate the remediated staging directory (replace the final directory/report names as appropriate):

```sh
/opt/homebrew/bin/verapdf --flavour ua1 --format json --maxfailures -1 --maxfailuresdisplayed -1 --processes 2 --recurse /path/to/remediated-pdfs > /path/to/work/verapdf-ua1.json 2> /path/to/work/verapdf-ua1.log
```

Force `--flavour ua1`: auto-detection can select PDF/A and defaults to PDF/A-1b when the conformance metadata is absent. `--maxfailures -1` completes all checks; `--maxfailuresdisplayed -1` preserves all failure contexts. Capture stderr separately so it cannot corrupt JSON. Preserve validator build information, every per-file result, batch count, parsing failures, and logs. Inspect the report's actual compliance values and batch failures rather than treating command completion as success. Confirm every expected PDF appears exactly once. [veraPDF CLI validation](https://docs.verapdf.org/cli/validation/)

veraPDF explicitly limits PDF/UA checking to **machine-verifiable** requirements. A useful final status distinguishes: (1) OCR performed, (2) tagging and alternatives prepared, (3) automated PDF/UA results, (4) completed content/assistive-technology checks, and (5) unresolved findings by item/page. A full compliance claim requires all applicable checks to pass, including human checks. [veraPDF validation model](https://docs.verapdf.org/validation/)

## Historical-document exceptions: context only

Do not infer an exception from the age of the serials. Archived web content requires all of: qualifying age (including reproduction of older physical media), retention only for reference/research/recordkeeping, a clearly identified archive area, and no alteration since archiving. Preexisting conventional electronic documents must have been online before the entity's compliance date and must not currently be used to apply for/access/participate in services, programs, or activities. Whether the DAMS collection meets these conditions requires publication/use facts absent here. Even qualifying exceptions do not remove effective-communication obligations. The user's remediation request remains the work target regardless. [DOJ Title II regulations, §§35.104 and 35.201](https://www.ada.gov/law-and-regs/regulations/title-ii-2010-regulations/)

