# Advocate Health CRIO Phenotype Library

A version-controlled registry of computable phenotype definitions
produced by Advocate Health / Wake Forest University School of Medicine
investigators using the `crio` research informatics library.

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
