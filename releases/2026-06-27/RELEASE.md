---
version: "2026-06-27"
dataset: "CarboCurator LLM glycan biomarker text-mining export"
data_file: "biomarkers_llm_glycan_2026-06-27.tsv"
pipeline:
  name: "CarboCurator LLM text-mining pipeline"
  version: null
  version_source: null
  model: "gpt-oss:20b"
controlled_vocabularies:
  - name: "bGSL"
    version: "2026-06-07"
    version_source: null
---

## Release notes

- This release does not include the `organism` and `organism_id` columns.
