# Evidence scope and known limitations

This repository is a reusable workflow template and manuscript companion for
*Bacillus nitratireducens* LABIM53. It contains the supplied final figures, the
manuscript table that could be recovered as structured data, reported values,
provenance notes and instructions for rerunning the analyses.

The historical command-line, GUI and web-service output directories were not
available when the repository was assembled. Their absence does not prevent
reuse of the methods. It does mean that the repository must not be described as
an independently reproduced archive of the original run.

## Evidence included

- five supplied publication images under `figures/`, with SHA-256 checksums;
- the native manuscript PlasFlow table as
  `tables/Table_1_PlasFlow_classifications.tsv`;
- LABIM53 BioProject **PRJNA1114765** and GenBank master accession
  **JBLFHU000000000.1**;
- taxa recoverable from the supplied Figure 1 and Figure 2 labels;
- reported assembly, BUSCO, annotation, HPLC and nutrient-solubilisation values;
- command templates and documented GUI/web steps.

## Unresolved discrepancies

### Pan-genome total

The Results text reports 12,047 clusters and components that sum to 12,047.
Figure 3A and its legend report 12,044. The original Roary output is unavailable,
so both observations are retained and the supplied figure is not altered.

### PlasFlow table

The Results text reports 36 scaffolds and a 5 + 31 prediction split. The native
manuscript table contains 34 rows and a 4 + 30 split. Its rows total 5,669,186
bp, 2,468 bp below the reported 5,671,654-bp assembly. The repository does not
invent the two missing records.

### Table 2 and sequence accessions

Table 2 is referenced in the supplied DOCX but is neither a native Word table
nor an embedded asset. The manuscript also does not report the UniProt or most
comparison-genome accessions. The repository records the recoverable biological
relationships and provides rerun instructions; unavailable identifiers are
labelled `not_reported_in_manuscript`.

### dDDH

The Discussion mentions digital DNA-DNA hybridisation, but no method, result or
output was supplied. dDDH is therefore outside the supported workflow and
should not be claimed on the basis of this repository.

## Release wording

A release may state that the repository provides manuscript assets, structured
reported evidence and reusable workflow instructions. It should also state that
historical analysis outputs are unavailable and that the discrepancies above
have not been independently resolved.
