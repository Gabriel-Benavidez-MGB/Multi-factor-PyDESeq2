# Multi-factor-PyDESeq2

# Multi-factor Differential Expression Analysis with PyDESeq2

This repository contains a Jupyter notebook implementing a **multi-factor differential gene expression (DGE) analysis** using [`PyDESeq2`](https://github.com/owkin/PyDESeq2), a Python implementation of the DESeq2 pipeline. The analysis explores how gene expression is affected by two experimental factors using a real-world dataset from the **airway epithelium**.

## 📁 Folder Structure

├── Multi-factor_PyDESeq2.ipynb # Main analysis notebook
├── data/
│ ├── airway_counts.csv # Raw gene count matrix
│ └── airway_metadata.csv # Sample metadata (e.g., condition, cell line)

## 🧪 Dataset Description

The data comes from an airway epithelial cell experiment, where RNA-seq was used to measure gene expression in treated vs. untreated conditions across different cell lines.  
- `airway_counts.csv`: Raw read counts for each gene (rows: genes, columns: samples)
- `airway_metadata.csv`: Sample-level information including treatment condition and cell line

## 🧠 Analysis Highlights

- Multi-factor design: `~ cell + dex`  
- Differential gene expression testing via Wald test  
- Output includes:
  - Dispersion estimates
  - PCA plot of sample distances
  - Top differentially expressed genes (adjusted p-values)
  - Volcano plot

## 🛠️ Tools & Libraries

- Python 3.10+
- [`pydeseq2`](https://github.com/owkin/PyDESeq2)
- `pandas`, `matplotlib`, `seaborn`, `numpy`
