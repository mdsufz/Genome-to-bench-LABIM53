# Correction implementation record

This file maps the revised priority list to the repository changes. It records
what is complete and what still requires original analysis material or a remote
GitHub action.

| Priority item | Repository implementation | Status |
| --- | --- | --- |
| Move GitHub to final location | Intentionally not performed; migration is being handled manually. The quick-start clone command uses `<final-repository-url>`. | Excluded by owner |
| Standardise strain name | Replaced the former strain label with LABIM53 across documentation, scripts, configuration, metadata and example paths. | Complete |
| Align reproducibility claim | README now describes workflow documentation and command templates, with explicit verification boundaries. | Complete |
| Concatenated 16S + *gyrB* phylogeny | Added deterministic concatenation, shared FASTA/NEXUS output, IQ-TREE and MrBayes routing, and taxon-set checks. The supplied final Figure 2 is now version-controlled. | Workflow complete; historical alignment and settings unavailable |
| Figure 4 panel labels | Added the supplied final image and corrected all documentation to A = Aleksandrov/potassium and B = NBRIP/phosphate, matching the manuscript legend. | Complete |
| PlasFlow wording and counts | Extracted the native manuscript Table 1 (34 rows: 4 chromosome-labelled + 30 plasmid-labelled predictions) and documented its difference from the Results text (36 rows: 5 + 31). | Recoverable evidence complete; two-row discrepancy unresolved |
| Pan-genome count | Recorded 12,047 from the Results/component sum and 12,044 from Figure 3A/legend without altering the supplied figure. | Three-cluster discrepancy documented; original Roary output unavailable |
| dDDH inconsistency | Explicitly excluded dDDH from the supported workflow because no method or output was supplied. | Repository complete; unsupported manuscript claim must be removed |
| Gene-mining metadata | Added 30 gene-trait records for potassium and phosphorus solubilisation, covering 20 unique UniProt targets and their cited evidence from Dissertation Appendix A, Table A1. | Complete |
| Accession lists | Added the confirmed accessions for LABIM53, the 12 Figure 1 comparison genomes, the 14 public comparative-genomics strains and accession-supported ANI/phylogeny taxa. | Complete |
| Figure/table provenance | Added the five supplied image assets, checksummed manifests and the recoverable PlasFlow table. Table 2 was not present as a native table or embedded asset, so its schema and rerun instructions are retained. | Supplied assets complete; historical source outputs unavailable |
| Configuration layer | Added `config/config.yaml`, `config/samples.tsv` and shared readers; removed focal-sample hard-coding from stage scripts. | Complete |
| Repository polish | Applied British English, corrected the MIT statement, expanded `CITATION.cff`, and applied repository description/topics. Release wording must disclose the historical-output limitation. | Complete except release publication |

The repository no longer uses generic blocking markers for unavailable
historical material. Instead, every limitation states whether a value is
reported in the manuscript, visible in a supplied asset, absent from the
manuscript, or dependent on an unavailable historical output. A public release
must retain those distinctions and must not claim independent reproduction of
the historical analyses.

