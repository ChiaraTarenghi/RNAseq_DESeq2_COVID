# RNA-seq Differential Expression Analysis (COVID-19 vs Controls)

This project performs a **differential gene expression analysis** using the **GSE152641** dataset (whole blood, COVID-19 patients vs healthy controls) with **DESeq2**.

## Project Structure
```text
scripts/      # RNAseq_workflow.R (main script)
results/      # dds_ready.rds, DE_results.csv
figures/      # PCA_plot.png, heatmap_top20.png, volcano_plot.png
data/         # downloaded GEO data (not versioned, see data/README.txt)
```

How to Run

```r
setwd("RNAseq_DE_project")
source("scripts/RNAseq_workflow.R")
```

Outputs (preview)
## Outputs (preview)

![PCA](https://raw.githubusercontent.com/ChiaraTarenghi/RNAseq_DESeq2_COVID/main/figures/PCA_plot.png)
![Heatmap](https://raw.githubusercontent.com/ChiaraTarenghi/RNAseq_DESeq2_COVID/main/figures/heatmap_top20.png)
![Volcano](https://raw.githubusercontent.com/ChiaraTarenghi/RNAseq_DESeq2_COVID/main/figures/volcano_plot.png)

Dataset

GEO Accession: GSE152641

References

Love MI, Huber W, Anders S (2014). Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. Genome Biology.

License

MIT (code). Please refer to NCBI GEO for data usage terms.
