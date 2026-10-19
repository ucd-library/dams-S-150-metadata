# Late Male Express table review — frozen handoff

`semantic-overrides-male-express-late.json` is frozen at 36 scanned pages, 58 tables, and 517 rows. All normalized bounds, row widths, and duplicate-table checks pass. SHA-256: `1f1248ade87857f4f3dc4feaf42e9e6af94b4fa9976d5157f921757c5c705f73`.

This file contains visually verified transcriptions of the issue12 scan29 Operation Concern and Circus Circus statements; issue13 scan31 Atlantis House monthly expenses; Saully, Dorothy, Closet, and Monterey award results; pool standings and prizes; official Los Angeles court voting; magazine popularity voting; advertising and bath-house rates; restaurant menus; historical blank entry, travel, gift, and membership coupon forms; competition prize schedules; grouped publication credits; selected calendars and event schedules; and complete venue/address associations from the flagged maze, radial, and star-layout directories.

## Source anomalies preserved

- Operation Concern prints the 1974 ending balance as 9,335.00 but the 1975 beginning balance as 9,334.87. The 13-cent difference is retained. Missing Circus Circus amount cells remain blank rather than invented zeroes; notes explain them.
- Issue12 scan55 article and photograph caption reverse Karen and Judy's Closet King runner-up ranks. The article table retains the article values and flags the disagreement.
- Issue10 scan112 prints Roman Holiday Baths at 14435 Victory Bl.; issue11 scan62 prints 14435 Ventura Blvd. Both historical addresses are retained in their own pages.
- Issue14 scan21 prints the first Halloween category as “Best Bus”; issue15 scan30 prints “Rohnda”; issue15 scan7 prints “Eleven Spice Lamb Karma.” These are transcribed without speculative correction.
- Issue15 scan7 has no printed price for Catch of the Day. Its price cell explicitly says “Not printed.”
- Issue15 scan79 has only a two-column advertisement/price schedule. No contract-price columns appear in the scan despite the earlier review note describing them.

## Remaining complex content and limits

The requested financial and flagged genuine tabular data are transcribed. Several additional structures noted in the visual-review annotations are ordinary lists or dialogue rather than data tables; their complete text and semantic order have **not** been manually verified by this table-review pass. In particular, matching quizzes/answer keys (issue10 scans18–19; issue13 scan12), paired wordplay rosters and puzzles (issue13 scans4/30; issue14 scans4/60; issue15 scan14), continuation nomination rosters (issue11 scans67–68), and the multi-column political endorsement lists (issue15 scans2–3) still need explicit list/reading-order verification if the automated writer does not preserve these associations.

Other dated-list pages remain in OCR/annotation coverage without exact table overrides: issue10 scans90/99; issue11 scans44/54; issue12 scan57; issue13 scans44/65/67; issue14 scans88/108; issue15 scans35/46/60/76. These can be represented as date/event list entries; they should not be claimed to have received complete line-by-line manual transcription in this pass.

Rotated and diagonal display text, interview question/answer hierarchy, reading order across spreads, source handwritten signatures, full OCR accuracy, and screen-reader behavior are separate document-level validation work. Machine PDF/UA validation does not by itself establish WCAG 2.1 AA or ADA Title II compliance.

The issue10 scan112 maze table is the detailed venue/address text equivalent of the informative graphic. Retain the map Figure and its concise alt text alongside this associated table. The maze is schematic; its paths are not driving directions. Directory arrangements around logos or stars do not encode coordinates.

## Other frozen deliverables from this reviewer

- `annotations-catalogs.json`: all 333 catalog pages; 485 grounded Figure alternatives.
- `semantic-overrides-catalogs.json`: 54 tables on 16 catalog pages.
- `annotations-male-express-final.json`: all 304 pages of issues16–18; 201 grounded Figure alternatives.
- `semantic-overrides-male-express-final.json`: 39 tables on 24 pages.

Issue17 scans110–112 contain a 1992 Queer L.A. insert within the 1975 issue's source sequence. This source-provenance anomaly remains flagged. Issue17 scan59 has an informative world-map Figure plus an associated menu table; retain both.

All outputs were written under the working directory. No collection production files or assembler/writer files were edited.
