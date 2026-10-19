# Recipient label redactions - October 19, 2026

Four local delivery TIFFs and their four tagged PDFs have opaque pixel redactions of the recipient mailing labels, including recipient name, address and routing/customer code. Publisher addresses and surrounding page content are preserved. The ARKs and filenames are unchanged.

| ARK | Item | Scan page |
| --- | --- | --- |
| ark:/87293/d3v40k92m | Ah_Men_House_Party_1975 | 28 |
| ark:/87293/d3fx7484m | Ah_Men_Ship_to_Shore_1976 | 35 |
| ark:/87293/d3t43jd4b | Ah_Men_Sunsastions_1976 | 36 |
| ark:/87293/d34f1mv7k | The_Male_express_01_19750416 | 7 |

Male Express scans 6 and 7 were checked; the recipient label is on scan 7. Scan 6 contains an advertisement with a business address and is unchanged.

The corresponding access transcripts, native OCR caches, semantic manifests, HTML reading editions, sidecar notices and checksums were updated. Redacted source PDFs and explicit semantic suppression regions prevent the active accessibility rebuild from restoring the labels. Preserve the privacy_redaction fields and semantic-overrides-recipient-redactions.json during future collection rebuilds; do not re-copy archival source files over the redacted access TIFFs.

Verification: all pixels outside each mask are unchanged in the TIFFs and embedded PDF rasters. Every other PDF scan image remains byte-identical; every other page's semantic content is unchanged. The old label raster is absent from the rebuilt PDF objects. Matching recognized label phrases and OCR words in the masked region are removed. All four PDFs passed qpdf and independent tag/MCID/ParentTree/font checks. The only veraPDF failure remains the intentionally omitted PDF/UA identification, as before; this work does not certify ADA or PDF/UA compliance. Updated TIFFs and rendered PDF pages were visually inspected.

Sync and DAMS import remain manual. Upload/replace the affected TIFF, PDF, transcript and sidecar files, then refresh the corresponding DAMS/IIIF cached derivatives as required by your deployment. The live DAMS copies are not changed by this local work.

Only collection/ and items/ are delivery directories. Exclude work/ from syncing: it contains private, unredacted historical originals and the new before-change backup. The original archival source files are preserved. Active rebuild sources are the redacted PDFs in this directory's source/ folder. verification.json, promotion-receipt.json and the fresh audit contain current checks and fingerprints.

Final local audit: 43 items, 5152 JSON-LD files, 4978 local media; 0 errors, 0 warnings, 0 missing binaries. Changes applied and current delivery fingerprints verified.
