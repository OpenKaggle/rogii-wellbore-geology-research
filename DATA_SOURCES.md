# Data and upstream sources

| Material | Official/upstream source | Public handling here |
| --- | --- | --- |
| Competition overview, rules, and authorized inputs | [ROGII Wellbore Geology Prediction](https://www.kaggle.com/competitions/rogii-wellbore-geology-prediction) | Link only; no input files are included. |
| Kaggle kernels and discussions considered during research | Their individual Kaggle pages, recorded by the local research process | Link/provenance only; this repository does not mirror notebooks, discussion text, or kernels. |
| Model packages and runtime dependencies | Their respective upstream projects and licences | Link/version/lock information only when needed; no weights are included. |
| Local ROGII feature, OOF, per-well, oracle, fold, and candidate-cache artifacts | Generated locally from authorized inputs and first-party research scripts | Raw and row-level artifacts are **NO-GO**. Only the value-free schema/digest metadata in `ROGII_PUBLIC_SCHEMA_MANIFEST.json` and the aggregate-only policy in `ROGII_PUBLIC_AGGREGATE_SUMMARY.json` are included. |

Anyone reproducing this work must comply with the competition rules and every
upstream licence independently.

The public schema manifest is not a data redistribution: it records relative
artifact names, file hashes, sizes, row/column counts, field names/types, and
risk dispositions, but no field values, samples, minima/maxima, pseudonymous
well rows, or private mappings. A hash receipt proves which local artifact was
reviewed; it does not grant redistribution rights to that artifact.
