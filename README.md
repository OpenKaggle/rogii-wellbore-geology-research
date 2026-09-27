# ROGII Wellbore Geology research

An OpenKaggle source-and-evidence archive for work around the
[ROGII Wellbore Geology Prediction](https://www.kaggle.com/competitions/rogii-wellbore-geology-prediction)
competition.

The repository keeps first-party training, selection, validation, and
Kaggle-operation tooling together with the decision notes that explain why a
method was tried. It is deliberately not a mirror of competition downloads,
third-party notebooks, public discussion pages, model weights, or submission
files.

## What is here

- `src/`: first-party scripts for structured segment selection, candidate-path
  generation, reranking, validation, controlled queueing, and reproducible
  status collection;
- `research/`: cross-project reasoning, engineering playbooks, and an
  intelligence ledger with private local paths removed;
- `DATA_SOURCES.md`: official and upstream acquisition records;
- `RELEASE_MANIFEST.md`: the exact public boundary for this source release.

The scripts expect a reader to obtain permitted inputs independently and to
set paths/configuration locally. They do not bundle any competition rows or
derived tables.

## Evidence boundary

Detailed research evidence is useful: this project can publish methods,
metrics, decision records, generated summaries, and other first-party derived
work. The thing that stays out is the original download, a copied third-party
artifact, a credential, or material expressly restricted by its source.

See [OpenKaggle's publishing guide](https://github.com/OpenKaggle/.github/blob/main/PUBLISHING.md)
for the organization-wide policy.

## Reproduction

1. Read the official competition rules and obtain access to the input data.
2. Place the data only in a local ignored location of your choice.
3. Review each script's CLI/configuration before executing it. Submission and
   remote-status helpers are intentionally operational tools, not a request to
   take an irreversible competition action.
4. Record your own data version, code revision, and output hashes alongside
   any new derived evidence.

This is an independent community archive, not a Kaggle or ROGII product.
