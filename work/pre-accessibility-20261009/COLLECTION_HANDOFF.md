# LGBTQ Serials (placeholder title)

Collection root: /Users/enebeker/dams-S-150-metadata

42 items; 2,467 source TIFFs; 42 searchable PDFs with 2,467 scan pages total; 2,467 page transcripts; 26 supplied authority labels and one collection cover. One scan is one PDF page, including scans of two-page spreads. Actual filenames and scan order are preserved. The source masters and catalog are unchanged. TIFF copies use APFS copy-on-write cloning; source and output SHA-256 checksums matched.

## Files

- Collection: collection/lgbtq-serials.jsonld.json
- Labels: collection/lgbtq-serials/labels.jsonld.json, copied byte-for-byte from /Users/enebeker/Documents/Codex/2026-10-08/in/outputs/labels.jsonld.json
- Items: items/<key>.jsonld.json
- PDFs: items/<key>/media/<key>.pdf
- Images: items/<key>/media/images/
- Machine-generated page transcripts: items/<key>/media/text/
- Build record: work/collection-build.json
- Source/catalog match inventory: work/inventory.json
- Binary paths, sizes, and SHA-256 checksums: work/binary-manifest.csv
- ARK requests: work/ark-requests.csv
- Structural audit: work/audit-001.json
- Pages with little or no recognized text: work/ocr-review.csv
- Rendered PDF review samples: work/pdf-review/

## Metadata and rights

The supplied catalog names, dates, subject terms, and FAST identities were retained. Subject terms are plain keywords; FAST identifiers resolve to the exact matching URI in the supplied labels file. Fourteen source folder names differ from the catalog only in capitalization; the actual source case is preserved in item keys. Year, month and full dates retain their precision. No issue or volume information was silently corrected. The Gay News catalog title differs from the visible Gay Students Newsletter masthead, and the first Male Express issue begins with a Serpent Eight advertisement; these need catalog/order review.

The user specified In Copyright — Educational Use Permitted (http://rightsstatements.org/vocab/InC-EDU/1.0/) for items and PDFs. No metadata license was supplied or inferred.

## Checks and review

Local structural audit: 0 errors, 0 missing binaries, 43 warnings. Warnings are missing ARKs. Every TIFF decoded successfully. Every PDF has the expected page count; OCR text was checked after merging. Covers, middle pages and final pages were rendered for all 42 PDFs for visual review. Generated metadata hashes are recorded to detect manual edits before a later run.

PDF access images were reduced to at most 3,300 pixels on the longest side and JPEG quality 90; masters remain unchanged. OCR used Tesseract English and retains each scan's orientation. Each page has a text transcript, including empty transcripts for blank or unrecognized pages. OCR text has not been human-reviewed and can contain errors. Cover descriptions were visually reviewed; interior alt text is a sequence/navigation label rather than a full visual description. PDFs are searchable but untagged and not accessibility-certified. Manual OCR, reading order, image descriptions, and screen-reader review remain.

## Identifiers and manual delivery

No ARKs were supplied. The 43 requests (42 items plus collection) are ready in work/ark-requests.csv. No fake identifiers were assigned, and no EZID API calls were made.

Run the adapted minting helper in a terminal and enter the EZID password at its prompt:

```sh
python3 /Users/enebeker/.codex/skills/digital-collection-builder/scripts/mint_arks.py --csv /Users/enebeker/dams-S-150-metadata/work/ark-requests.csv --apply
```

Keep the request CSV and its journal together. After minting, bind identifiers by the filename stable-key column and refresh the audit; the package remains a draft until that step is complete.

Sync: manual/pending. Import: manual/pending. Publication: not performed. Binary sync destination and target DAMS environment were not supplied. Use collection/ and items/ as the package; keep work/ as local build evidence. After importing into the selected environment, verify labels, subject links, thumbnails, page order, and PDF browsing/downloads.

Visual sample review completed: 124 rendered pages across all 42 PDFs. No generated cropping or layout defects were observed in the reviewed samples.

After minting, the local binding helper is available at work/apply_s150_arks.py. It checks the saved metadata hashes and completed minting journal before applying the ARKs by stable key. A fresh audit and updated handoff are then required.
