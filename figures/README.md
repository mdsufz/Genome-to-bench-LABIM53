# Manuscript figures and provenance

This directory contains the five publication assets supplied with manuscript
version 9. Their filenames, evidence source, methods and SHA-256 checksums are
recorded in `manifest.tsv`. The images are preserved as supplied; the
repository does not claim to include the underlying software output or editable
source project files.

## Figure files

- `Figure_1_circular_genome_comparison.png` - circular comparison of LABIM53
  with 12 *B. nitratireducens* genomes.
- `Figure_2_taxonomy_resolution.png` - ANI heatmap and Bayesian/maximum-
  likelihood 16S rRNA + *gyrB* phylogenies.
- `Figure_3_pangenome_and_COG.png` - pan-genome matrix and COG classification.
- `Figure_4_nutrient_solubilisation.png` - plate assays.
- `Graphical_abstract_genome_to_bench.png` - conceptual workflow.

## Fixed Figure 4 mapping

The supplied manuscript legend and labelled image establish the mapping:

- **Figure 4A:** Aleksandrov medium, potassium solubilisation.
- **Figure 4B:** NBRIP medium, phosphate solubilisation.

This replaces the reversed mapping previously recorded in the repository.

## Figure 3 count discrepancy

Figure 3A and its legend report **12,044 gene clusters**. The Results text
reports **12,047**, comprising 3,513 core + 3,558 accessory + 4,976
strain-specific clusters, which also sums to 12,047. Because the original Roary
output is unavailable, the supplied figure has not been altered and neither
number is described as independently validated. Regeneration instructions are
provided in `docs/04_pangenome_and_functional_annotation.md` for any future
reanalysis.

## Provenance scope

For this manuscript-companion repository, a final figure plus its legend,
method and documented limitations is sufficient. Original GUI/web-service
sessions and intermediate output files are optional provenance enhancements,
not a prerequisite for using the workflow instructions.
