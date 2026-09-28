# ROGII Wellbore Geology research

An OpenKaggle source-and-evidence archive for work around the
[ROGII Wellbore Geology Prediction](https://www.kaggle.com/competitions/rogii-wellbore-geology-prediction)
competition.

The repository keeps first-party training, selection, validation, and
Kaggle-operation tooling together with the decision notes that explain why a
method was tried. It is deliberately not a mirror of competition downloads,
third-party notebooks, public discussion pages, or copied upstream weights.
Eligible first-party model and submission artifacts may be released separately
only with their own provenance manifests and checksums; they are not implied
to be public merely because the source code is public.

## What is here

- `src/`: first-party scripts for structured segment selection, candidate-path
  generation, reranking, validation, controlled queueing, and reproducible
  status collection;
- `research/`: cross-project reasoning, engineering playbooks, and an
  intelligence ledger with private absolute/user-identifying paths removed;
- `ROGII_PUBLIC_SCHEMA_MANIFEST.json`: field names, logical types, risk
  classifications, relative artifact names, sizes, row/column counts, and
  SHA-256 receipts for the reviewed local derived-data corpus, with no source
  row values;
- `ROGII_PUBLIC_AGGREGATE_SUMMARY.json`: a compact publication decision and
  aggregate-only release contract;
- `DATA_SOURCES.md`: official and upstream source-handling summary;
- `RELEASE_MANIFEST.md`: the exact public boundary for this source release.

The scripts expect a reader to obtain permitted inputs independently and to
set paths/configuration locally. They do not bundle any competition rows or
derived tables.

## Evidence boundary

Detailed research evidence is useful: this project can publish methods,
metrics, decision records, generated summaries, and other first-party derived
work. The thing that stays out is the original download, a copied third-party
artifact, a credential, or material expressly restricted by its source.

The reviewed ROGII feature/OOF corpus now has an explicit two-tier decision:

- **Raw and row-level derived artifacts: NO-GO.** The 12 Parquet files and
  features/OOF/per-well/oracle/fold CSVs contain well identifiers or
  quasi-identifiers, official-input-derived geometry, candidate paths,
  prediction output, target/evaluation signals, or split assignments. They
  are not published here.
- **Metadata-only schema and receipts: GO.** The two root JSON files contain
  schema/header metadata, hashes, sizes, counts, classifications, and the
  aggregate release policy only. They contain no competition or derived row
  values and no well-identifier values from the source data.

Replacing `well` with a stable pseudonym would not make the row-level corpus
safe to publish: geometry, segment structure, predictions, targets, and
evaluation signals remain linkable. Any future public metric table must be
regenerated from a strict first-party whitelist, suppress groups with fewer
than 10 wells, and pass a separate competition-rights review. It must not copy
the reviewed raw CSVs.

See [OpenKaggle's publishing guide](https://github.com/OpenKaggle/.github/blob/main/PUBLISHING.md)
for the organization-wide policy.

## Reproduction

1. Read the official competition rules and obtain access to the input data.
2. Place the data only in a local ignored location of your choice.
3. Review each script's CLI/configuration before executing it. Submission and
   remote-status helpers are intentionally operational tools, not a request to
   take an irreversible competition action. In particular,
   `src/push_rogii_next.py` is dry-run-only by default and can call
   `kaggle kernels push` only when `--execute` is supplied explicitly.
4. Record your own data version, code revision, and output hashes alongside
   any new derived evidence.

This is an independent community archive, not a Kaggle or ROGII product.
