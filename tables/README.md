# Manuscript tables and provenance

This directory contains manuscript tables that could be recovered from the
supplied article.

## Table 1 - PlasFlow classifications

`Table_1_PlasFlow_classifications.tsv` was extracted directly from the native
Word table in `1_Rodrigues_L53_v9.docx`. The labels are retained as
**PlasFlow predictions** and must not be interpreted as proof of physical
chromosomes or plasmids.

The supplied manuscript table contains **34 rows**:

- 4 chromosome-labelled predictions;
- 30 plasmid-labelled predictions;
- 5,669,186 bp represented in total.

The Results text separately reports **36 scaffolds**, **31 plasmid-labelled + 5
chromosome-labelled sequences**, and **5,671,654 bp**. The table is therefore
short by two entries and 2,468 bp relative to the Results text. Without the
original PlasFlow output, the repository preserves both observations and does
not manufacture the missing rows.

## Table 2 - gene-mining results

Table 2 is referenced by the supplied manuscript, but it is not present as a
native Word table or embedded asset in that DOCX. The repository therefore
keeps the target schema in `metadata/pgpr_gene_targets.tsv` and the rerun
instructions in `docs/05_gene_mining.md`. The original tBLASTn output is not a
requirement for using the workflow template; it is only required if the exact
historical Table 2 results are to be independently rechecked.
