[English](README.md) | [Español](README.es.md)

# LocalSheet Lite (MIT) — Zero-Upload Offline CSV Inspector

**LocalSheet Lite** is a single-file, 100% offline HTML utility for decoding messy CSV/TSV encodings, sniffing delimiters, and finding exact duplicate rows locally in your browser (`file://`)—with **zero uploads, zero installs, zero network requests, and strict CSP (`default-src 'none'` + `script-src 'sha256-...'` without `'unsafe-inline'`)**.

> Need **Native `.xlsx` Multi-Sheet Reading**, **Strict Column Auto-Classification (`>=70%`)**, **Multi-Series Sequence Gap Auditing (`Group Series By`)**, **Excel Destination Presets (`="00412"`)**, **Pre-Export Guard Modal**, **Explicit Ambiguous Date/Amount/Precision Breakdown**, **Control Totals**, **Exceptions Log CSV**, and **JSON v2 Profiles**?
> Those capabilities are part of **[LocalSheet Auditor (Full Version)](https://cesahz.gumroad.com/l/localsheet-auditor)** *(a local technical support tool — does not replace formal accounting or tax review)*.

---

## Quick Start
1. Download `localsheet-lite.html` (or clone this repository).
2. Double-click `localsheet-lite.html` to open it in Chrome, Edge, Firefox, or Brave (`file://`).
3. Drop any `.csv`, `.tsv`, or `.txt` file (or try `samples/03_inventario_duplicados_latin1.csv`).

## Why Single-File Offline HTML?
- **Verifiable Privacy:** Financial, HR, and client CSVs stay in browser memory (`0` network requests, strict `default-src 'none'` + hashed `script-src` CSP).
- **No Installer Friction:** Works directly on Windows, macOS, and Linux with zero `.exe` installers or admin rights.
- **Honest Scope:** Built for `.csv`, `.tsv`, and `.txt` files. Binary `.xlsx`/`.xls` uploads are safely rejected with clear guidance rather than parsing binary garbage. Core engine tested up to 10,000+ rows in automated Node/Chrome tests (no human usability testing).

## What's Included in Lite (MIT)
- Encoding auto-detection (`UTF-8`, `UTF-8 BOM`, `UTF-16LE/BE`, `Windows-1252 / Latin-1`)
- Statistical delimiter auto-detection (`,`, `;`, `\t`, `|`) + `sep=` support on import
- Strict RFC-4180 parsing & CSV formula neutralization (`=`, `+`, `@`, `-`)
- Fast exact-row duplicate detection & `UTF-8 BOM` deduplicated CSV export (without emitting `sep=;`)

## Feature Comparison: Lite (MIT) vs. Full Version

| Capability | Lite (MIT) | Full Version |
|---|---|---|
| Offline Single HTML (`file://`, Zero Network, Strict Hash CSP) | Yes | Yes |
| Encoding Detection (`UTF-8`, `UTF-8 BOM`, `UTF-16`, `Win-1252`) & Binary Guard | Yes | Yes |
| Delimiter Auto-Detection + `sep=` on Import | Yes | Yes |
| Exact Duplicate Detection & `UTF-8 BOM` CSV Export | Yes | Yes |
| CSV Formula Neutralization (`=`, `+`, `@`, `-`) | Yes | Yes |
| Native `.xlsx` Reader (Multi-Sheet, 1900/1904 Dates, Merged Cells) | — | **Yes** |
| Clipboard Excel Paste (`Ctrl+C` → `Ctrl+V`) & Skip Top Rows | — | **Yes** |
| Strict Column Auto-Classification (`>=70%`, Text/Phone Guard, Manual Overrides) | — | **Yes** |
| Composite-Key Duplicates + Side-by-Side Diff | — | **Yes** |
| Multi-Series Correlativity + `Group Series By` (`Date Year` / `Column`) | — | **Yes** |
| Explicit Breakdown (`N` Ambiguous Dates, `M` Ambiguous Amounts, `K` Precision) + Control Totals | — | **Yes** |
| Excel Destination Presets (`Excel English`, `Excel Español / LatAm`, `Generic`) + Pre-Export Guard Modal | — | **Yes** |
| Virtualized Grid, Row Drawer, 60s Undo, Reset, `.tsv`, `.xls` (HTML table), Exceptions CSV, PDF & JSON v2 | — | **Yes** |

## SHA-256 Verification
- `localsheet-lite.html`: `c3e3dcd51f283fcaf62223e197d0683b03fac590b677196fd29c8c7c1df84de`

## License
MIT License — see [LICENSE](LICENSE).
