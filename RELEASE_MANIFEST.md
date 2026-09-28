# Release manifest

## Included

- 11 first-party Python scripts from the active ROGII research workspace;
- three first-party research notes with local absolute paths removed;
- `ROGII_PUBLIC_SCHEMA_MANIFEST.json` (190,574 bytes; SHA-256
  `6805c9518d8a1be6eaff8ef6045c8a5a16a47ab4db2a8a1c306838cb4d1b29af`),
  containing field-level classifications and file receipts but no source row
  values;
- `ROGII_PUBLIC_AGGREGATE_SUMMARY.json` (1,105 bytes; SHA-256
  `dc905a0b8b2f27e0ad23ad0adc16e1e5c2fb697781bc79b981f03fa650d7a546`),
  recording the raw-NO-GO/metadata-only decision and public aggregate policy;
- an explicitly opt-in Kaggle queue helper: kernel publication now requires the
  explicit `--execute` flag, while the default remains dry-run-only;
- a self-contained output collector that resolves its validator from `src/`
  and propagates validator failure through its exit status;
- this repository's data-source and boundary documentation.

## Excluded

- organizer-provided competition inputs and sample/submission files;
- all 12 reviewed local Parquet feature/OOF artifacts (3,962,031,815 bytes)
  and the larger derived CSV corpus. The completed field-level review found
  identifiers/quasi-identifiers, official-input-derived geometry, candidate
  paths/predictions, targets/evaluation signals, OOF output, and split
  assignments; raw and pseudonymized row-level publication are **NO-GO**;
- all per-well, oracle, fold, features/OOF CSVs and candidate-cache NPZ files;
- copied upstream model weights, caches, `__pycache__`, downloaded
  leaderboards, scraped pages, discussion copies, and third-party kernels;
- first-party model and submission artifacts from this initial **source**
  release. Eligible artifacts may be published separately only with their
  producing revision, source/model provenance, file hashes, and a documented
  artifact host;
- credentials, cookies, tokens, local paths, and private mapping material.

## Verification

The release is scanned for absolute local paths, common credential patterns,
forbidden data/output directories, and large files. Both JSON metadata files
must parse, contain no source row values, and match the hashes above. The
Python source is syntax-checked. A fresh clone must contain the documented
source, notes, and metadata-only receipts without any excluded Parquet, CSV,
cache, submission, model, or competition-input payload.
