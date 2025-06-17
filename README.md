
# RNA-seq Differential expression Guide

This is a general guide for performing a differential expression study on RNAseq data using DESeq2 in R. The guide can be viewed through the html links provided at each step in the description below.

- [Features](#features)
- [Guidelines](#guidelines)
- [Usage](#usage)
## Features

1. 01_data_import: https://VanHeeschTools.github.io/rna-seq-DE-guide/01_data_import.html
* import sample metadata, gtf file and transcript count data


## Guidelines
* Never hardcode patient IDs
* Use clear, descriptive object names
* Only load the libraries you’re actually using in each script separately
* Identify which library a function belongs to (e.g. `dplyr::filter()`)
* Comment each step in your code
* Save each final object to a .RDS file
* Use paths that are relative to your project folder instead of hardcoded file paths
* Create a README.md file describing the steps taken throughout your analysis
## Usage
When working on your own project, it’s important to create a clear folder structure and to separate each step of your analysis with descriptive names that reflect their order of execution. Here is an example:

```
de_analysis/
 ├── data/
     ├── sample1_name
        └── quant.sf
     ├── sample2_name
        └── quant.sf
     └── sample_metadata.tsv
 ├── plots/
     ├── heatmap.png
     └── volcano_plot.png
 ├── results/
     ├── gtf_df.RDS
     ├── meta_df.RDS
     ├── txi_counts.RDS
     └── dds.RDS
 ├── scripts/
     ├── 01_data_import.Rmd
     ├── 02_qc_and_filtering.Rmd
     ├── 03_deseq2_analysis.Rmd
     ├── 04_functional_annotation.Rmd
     ├── 05_visualisation.Rmd
     ├── optional/
        ├── go_enrichment_analysis.Rmd
        ├── kegg_pathway_analysis.Rmd
        └── subgroup_DE_analysis.Rmd
 ├── de_analysis.Rproj
 ├── de_analysis.RData
 └── README.md
```

