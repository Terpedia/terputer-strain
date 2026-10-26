# Commercial cannabis terpene profiles: variability and name-independent terpotypes

**Study status:** analysis results were executed in Google Colab on 2026-09-04; causal interpretation remains prospective.

## Abstract

An archive of 43,018 commercial cannabis chemical profiles was analyzed for within-name variability and name-independent chemical structure. Upstream analysis screened replicated labels with Kruskal–Wallis tests, false-discovery-rate correction, and epsilon-squared effect sizes; it also classified nine common terpene features without using names. The reported seven-class solution had silhouette 0.278, and 93.9% of 574 replicated names crossed multiple classes. These results indicate that labels are imperfect proxies for chemistry. Because matched genotype, cultivation, and assay metadata are absent, the analysis cannot assign observed variation to genetic or environmental causes.

## Data and methods (source-reported)

The archive export has 43,018 rows. Upstream analysis screened labels with at least five records; nine common terpene features were used for a name-independent composition model, with 32,050 complete positive profiles classified. The selected seven-class model had silhouette 0.278; mean 80% subsample ARI was 0.650, median assignment strength 0.418, and the negative-silhouette fraction 0.036. Name concordance was modest (weighted purity 0.406; normalized mutual information 0.112). See `data/colab_results_summary.md` and the cited derived CSVs.

## Limits

These are archive-level associations subject to sampling, measurement, source, and label provenance. Commercial names are not verified cultivars or genotypes. The source lacks matched genetic and cultivation variables. Terpotype clusters are descriptive partitions of the selected profiles, not validated biological taxonomies. The notebook included here inventories the raw export and reproduces arithmetic checks from the frozen summary; it does not retrain the upstream model.

## Reproducibility

Data and selected outputs are included under `data/`. Full model implementation and the original Colab notebook remain in the upstream `strain` repository. Consult its `pyproject.toml`, `notebooks/strain_analysis_colab.ipynb`, and `src/strain_analysis/` for exact analysis code.
