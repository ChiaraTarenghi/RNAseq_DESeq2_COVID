# RNA-seq Differential Expression Analysis (COVID-19 vs Controls)

This project performs a **differential gene expression analysis** using the **GSE152641** dataset (whole blood, COVID-19 patients vs healthy controls).  
The workflow is implemented in **R** with **DESeq2**, covering data download, quality control, PCA, heatmap, differential expression, and volcano plot.

## Project Structure
```text
scripts/      # RNAseq_workflow.R (main script)
results/      # dds_ready.rds, DE_results.csv
figures/      # PCA_plot.png, heatmap_top20.png, volcano_plot.png
data/         # downloaded GEO data (not versioned, see data/README.txt)
Workflow
Download data from GEO (GSE152641)

Build metadata from GEO sample annotations

Create DESeq2 object

Variance Stabilizing Transformation (VST)

PCA of samples

Heatmap of top 20 most variable genes

Differential expression analysis (COVID vs Control)

Shrinkage of log2 Fold Change (apeglm)

Volcano plot

How to Run
In R/RStudio (R ≥ 4.2):

r
Copy
setwd("RNAseq_DE_project")
source("scripts/RNAseq_workflow.R")
The script will install missing packages, download data if needed, and write outputs to results/ and figures/.

`## Outputs
- **Figures/**  

![PCA](figures/PCA_plot.png)  
![Heatmap](figures/heatmap_top20.png)  
![Volcano](figures/volcano_plot.png)

- **Results/**  
  - `dds_ready.rds`  
  - `DE_results.csv`

Dataset
GEO Accession: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE152641

References
Love MI, Huber W, Anders S (2014). Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. Genome Biology.

License
MIT (code). Please refer to NCBI GEO for data usage terms.
