# CarboCurator LLM Glycan Data

This repository contains versioned data exports produced by the CarboCurator LLM text-mining pipeline. Each release consists of a [BiomarkerKB-conformant](https://wiki.biomarkerkb.org/Data_Submission/Data_Upload) TSV file with a companion release record describing its controlled-vocabulary versions.

> [!IMPORTANT]
> Make sure you are using the **correct version** of the [bGSL resource](https://github.com/clinical-biomarkers/bGSL-data) when processing this data.

## Repository contents

```text
releases/
	YYYY-MM-DD/
		biomarkers_llm_glycan_YYYY-MM-DD.tsv
		RELEASE.md
```

## Data format

### Columns

| Column                         | Description                                                                                          |
| ------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `unique_entry_id`              | Unique identifier for each biomarker. Consists of article index + biomarker index                    |
| `component_index`              | Index of the biomarker component within a multicomponent biomarker.                                  |
| `entity_index`                 | Index of the entity component. A glycoprotein biomarker has a glycan and a protein entity component. |
| `assessed_biomarker_entity`    | Name of the assessed entity.                                                                         |
| `assessed_biomarker_entity_id` | Identifier for the assessed entity when available.                                                   |
| `assessed_entity_type`         | Entity type, for example `glycan` or `protein`.                                                      |
| `biomarker_controlled_vocab`   | Text describing the biomarker association or direction.                                              |
| `condition`                    | Name of the associated condition.                                                                    |
| `condition_id`                 | Condition identifier from Disease Ontology (`DOID`).                                                 |
| `best_biomarker_role`          | Assigned biomarker role(s); multiple values may be separated by semicolons.                          |
| `specimen`                     | Specimen name.                                                                                       |
| `specimen_id`                  | Specimen identifier, Cell Ontology (`CL`) or Uberon (`UBERON`).                                      |
| `evidence_source`              | Source publication identifier.                                                                       |
| `evidence`                     | Supporting text extracted or selected by the pipeline. Multiple excerpts may be separated by a \|.   |
| `organism`                     | Organism name.                                                                                       |
| `organism_id`                  | Organism identifier.                                                                                 |

## Provenance and controlled vocabularies

The release record is the authoritative place to document the pipeline/model versions, generation date, and controlled-vocabulary versions used for a release. In particular, record the exact **bGSL controlled-vocabulary version** used to produce or validate the glycan identifiers.

Identifier namespaces appearing in the data include `bGSL`, `DOID`, `CL`, `UBERON`, `NCBITaxon`, and `UPKB`. The namespace alone does not identify the precise vocabulary release.
