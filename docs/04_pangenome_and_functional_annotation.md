# 04 — Pan-genome & Functional Annotation

**Goal:** annotate genes and characterise the core/accessory/strain-specific repertoire and functional categories.
**Tools:** Prokka v1.14.6, Roary, COGclassifier.

## 4.1 Annotation — Prokka v1.14.6

Annotate LABIM53 **and** the 13 public *B. nitratireducens* genomes consistently (Roary needs GFF3 from the same annotator). Record the exact assembly accessions in `metadata/accessions/pangenome_genomes.tsv`.

```bash
for g in data/genomes_pangenome/*.fasta; do
  name=$(basename "$g" .fasta)
  prokka --kingdom Bacteria --genus Bacillus --species nitratireducens \
    --prefix "$name" --outdir results/prokka/"$name" \
    --cpus <threads> "$g"
done
```

**Reported outcome (LABIM53):** 5,718 CDS, 3 rRNA, 42 tRNA, 1 tmRNA.

## 4.2 Pan-genome — Roary → **Fig 3A**

```bash
roary -e --mafft -p <threads> \
  -f results/roary \
  results/prokka/*/*.gff
```

**Results-text outcome (14 genomes = 13 public + LABIM53):** 11,769 gene
clusters - 3,520 core, 3,547 shell and 4,702 cloud. These
components sum to 11,769.

The command below is an optional future consistency check if a regenerated or
historical `gene_presence_absence.csv` becomes available; the original output
is not required to use this workflow template:

```bash
python scripts/validate_pangenome_counts.py
```

The supplied gene presence/absence matrix (with the accompanying tree) is
version-controlled as `figures/Figure_3_pangenome_and_COG.png`.
To render the tree + matrix figure, Roary ships `roary_plots.py`:

```bash
python roary_plots.py results/roary/accessory_binary_genes.fa.newick \
  results/roary/gene_presence_absence.csv
```

## 4.3 Functional categories — COGclassifier → **Fig 3B**

Run on the LABIM53 protein FASTA (e.g. Prokka `LABIM53.faa`):

```bash
COGclassifier -i results/prokka/LABIM53/LABIM53.faa \
  -o results/cogclassifier_LABIM53
```

Produces the per-category counts plotted in **Figure 3B** (single-letter COG codes J, A, K, … S).
