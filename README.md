# scRNA-seq Analysis: iPSC Differentiation to Tenogenic Lineage

This repository contains the R code used for single-cell RNA sequencing (scRNA-seq) analysis in the following publication:

> Papalamprou A, Yu V, Jiang W, Sheyn J, Stefanovic T, Chen A, Castaneda C, Chavez M, Sheyn D.
> **Single Cell Transcriptomics-Informed Induced Pluripotent Stem Cells Differentiation to Tenogenic Lineage.**
> *eLife* (2026). DOI: [to be inserted upon publication]

Raw sequencing data are publicly available in the NCBI Gene Expression Omnibus (GEO) under accession number **[GSE229008](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE229008)**.

## Overview

This analysis covers scRNA-seq data generated from human iPSCs differentiated stepwise through presomitic mesoderm (PSM), somite (SM), sclerotome (SCL), and syndetome (SYN) stages, with and without WNT inhibitor (Wnt-C59) treatment. Key steps include:

- Quality control and filtering
- Normalization, integration, and clustering (Seurat v4.1.0)
- Pseudotime trajectory analysis (Monocle v2.18.0)
- Cell type annotation and visualization

## Software Requirements

| Tool | Version |
|------|---------|
| R | 4.1.2 |
| RStudio | 1.4.1103 |
| Cell Ranger | 3.0.0 |
| Loupe Cell Browser | 3.0.0 |
| Seurat | 4.1.0 |
| Monocle | 2.18.0 |

## Usage

Raw FASTQ files were processed with Cell Ranger (v3.0.0) to generate feature-barcode matrices. Downstream analysis was performed in R using Seurat and Monocle. Scripts are organized by analysis stage.

**Quality control parameters applied:**
- Cells retained: nFeature_RNA between 200–8000
- Cells retained: percent mitochondrial reads < 20%

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Contact

Dmitriy Sheyn, PhD — [Dmitriy.Sheyn@csmc.edu](mailto:Dmitriy.Sheyn@csmc.edu)
Orthopaedic Stem Cell Research Laboratory, Cedars-Sinai Medical Center, Los Angeles, CA
