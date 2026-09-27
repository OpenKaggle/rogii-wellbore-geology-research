# Release manifest

## Included

- 11 first-party Python scripts from the active ROGII research workspace;
- three first-party research notes with local absolute paths removed;
- this repository's data-source and boundary documentation.

## Excluded

- organizer-provided competition inputs and sample/submission files;
- 3.96 GiB of local Parquet feature/OOF artifacts and the larger derived CSV
  corpus, pending a field-level schema/rights review and an appropriate
  artifact host;
- copied upstream model weights, caches, `__pycache__`, downloaded
  leaderboards, scraped pages, discussion copies, and third-party kernels;
- first-party model and submission artifacts from this initial **source**
  release. Eligible artifacts are published separately with their producing
  revision, source/model provenance, file hashes, and a documented artifact
  host;
- credentials, cookies, tokens, local paths, and private mapping material.

## Verification

The initial release is scanned for absolute local paths, common credential
patterns, forbidden data/output directories, and large files. The Python source
is syntax-checked. A fresh clone must contain the documented source and notes
without the excluded artifact categories.
