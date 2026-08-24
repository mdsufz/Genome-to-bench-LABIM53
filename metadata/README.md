# Metadata and evidence status

This directory records evidence recoverable from the supplied manuscript and
figures. It is intentionally separate from large sequence and result files.

- `pgpr_gene_targets.tsv` records gene-metabolite relationships described in
  the manuscript and distinguishes them from accessions that were not reported.
- `accessions/` records known accessions and the taxa visible in supplied
  figures. `not_reported_in_manuscript` is an evidence statement, not a request
  to invent or reconstruct an identifier.
- `reported_results.yaml` records manuscript values, figure/table values and
  any discrepancy between them.
- `repository_settings.yaml` records the public repository description/topics.

The repository is a manuscript companion and reusable workflow template. Exact
historical output files are not required for using the instructions. Where an
original output is unavailable, the repository provides the reported value,
the supplied final asset, a transparent limitation and rerun instructions.

Do not interpret `not_reported_in_manuscript` or `source_output_unavailable` as
independently validated data.
