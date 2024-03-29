---
title: 'Single Cell Notes'
date: 2024-3-26
permalink: /posts/2024/3/sc/
tags:
  - bioinformatics
  - scRNA-Seq
  - scATAC-seq

---

### 



三个文件：

- barcodes.tsv : cell_id. Present the order of data
- Feature.tsv ： a text file which contains the identifies of the quantified gene (ENSG, Ensembl)
- Matrix.mtx  a text file contains a matrix of count value. The row are associated with the gene IDs and columns correspond to the cellular barcodes. 