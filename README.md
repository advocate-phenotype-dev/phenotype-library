# Advocate Health CRIO Phenotype Library

A curated registry of computable clinical phenotype definitions developed
across the Advocate Health / Atrium Health network. Phenotypes are versioned,
chart-review validated, and built for deployment in real-world evidence studies,
quality measurement programs, and trial-ready cohort identification — primarily
on the OMOP CDM with Epic Clarity support where required.

Each entry is produced and deposited via the [`crio`](https://github.com/advocate-phenotype-dev/crio-py)
research informatics library, which enforces schema validation, versioning,
and reproducible cohort definition.

## Phenotype Catalog

| Phenotype | Version | Principal Investigator | Validation | PPV | OMOP |
|---|---|---|---|---|---|
| [Incident NSTEMI (RWE)](projects/f3d7c2a1-5b8e-4f9d-a2c1-7e6f0b4d3a8c/) | 1.2.0 | Dr. Priya Chandrasekaran | Peer-reviewed | 91.4% | Yes |
| [NSTEMI Quality Measure](projects/741c4621-b599-4743-93f9-146aff9dc6bc/) | 1.0.0 | Dr. Maya Chen | Validated | 96.3% | — |
| [NSTEMI Quality Phenotype](projects/b2e5f8a1-7c3d-4e9b-a6f2-1d8c0e4b7a95/) | 0.2.0 | Dr. Alicia Vance | Draft | — | — |
| [Heart Failure with Reduced Ejection Fraction (HFrEF)](projects/e79c9476-811d-4bfe-84e1-1fbe4098862f/) | 0.1.0 | Erich Huang | Validated | — | Yes |

PPV = positive predictive value from chart review or cohort diagnostics.
`registry.yaml` is the machine-readable index of all project UUIDs and versions.

## Structure

- `registry.yaml` — machine-generated index of all phenotype projects
- `projects/{uuid}/` — one directory per phenotype project

Each project directory contains:
- `advocate-phenotype.yaml` — the canonical project metadata schema
- `README.md` — auto-generated human-readable summary
- `src/` — cohort definitions, Clarity queries, validation outputs
- `docs/` — clinical description, inclusion/exclusion criteria, changelog

## Contributing

Phenotype deposits are managed via the `crio` Python and R libraries.
Do not edit project directories manually.

- [crio-py](https://github.com/advocate-phenotype-dev/crio-py)
- [crio-r](https://github.com/advocate-phenotype-dev/crio-r)

## External Registries

OMOP-aligned phenotypes eligible for external deposit are exported
to the [OHDSI Phenotype Library](https://github.com/OHDSI/PhenotypeLibrary)
with Advocate Health attribution.
