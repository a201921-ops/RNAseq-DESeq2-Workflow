# RNA-seq Differential Expression & Phenotypic Response Workflow

## Project Overview
This repository provides an end-to-end RNA-seq transcriptomic analysis pipeline implemented in R using Bioconductor standard packages (`DESeq2`, `pheatmap`, `clusterProfiler`). 
The workflow bridges **genomic transcription dynamics** with observed **biological phenotypes**, identifying key molecular drivers underlying treatment responses.

## Key Workflow Modules
1. **Quality Control & Preprocessing**: Library size normalization and filtering of low-count noise genes.
2. **Statistical Modeling**: Negative Binomial GLM fitting and dispersion estimation via `DESeq2`.
3. **Hypothesis Testing**: Multiple testing correction using Benjamini-Hochberg FDR (`padj < 0.05`, `|log2FC| > 1`).
4. **Data Visualization**: 
   - Sample clustering & replicate consistency assessment via PCA (`plotPCA`).
   - Global expression shifts visualization via Volcano Plot.
   - Expression pattern clustering via Hierarchical Heatmaps (`pheatmap`).
5. **Functional Interpretation**: Mapping genomic signatures to biological pathways and observable phenotypic variations.

## Pipeline Outputs
- **PCA Plot**: Verification of biological replicate clustering.
- **Differential Gene Matrix**: CSV export of statistically significant candidate genes.
- **Hierarchical Clustering Heatmap**: Showing clear separation between experimental conditions.

## Tech Stack
- **Language**: R (v4.x)
- **Core Libraries**: `DESeq2`, `BiocManager`, `pheatmap`, `ggplot2`
