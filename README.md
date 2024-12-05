# CITEseq_AML_Analysis

This repository contains a streamlined pipeline for the multimodal analysis of single-cell CITE-seq data from engineered acute myeloid leukemia (AML) cell lines. It provides a complete workflow, from data preprocessing to cell type annotation, with benchmarking for memory-efficient file handling.

## Features
- Data Loading: Processes .h5 format files using muon.
- Quality Control: Filters low-quality cells and genes based on key metrics.
- Normalization: Performs library size normalization and log-transformation.
- Feature Selection: Identifies highly variable genes for dimensionality reduction.
- Clustering: Uses Leiden clustering to group cells into meaningful clusters.
- Cell Type Annotation: Annotates clusters based on marker genes.
- Visualization: Generates UMAP embeddings and dot plots for marker gene expression.
- Benchmarking: Evaluates memory usage and speed for .h5ad file access (backed vs. unbacked).

## Setup

### 🔗 Clone the Repository

Clone this repository and navigate to the project directory:

```bash
git clone git@github.com:mulbagalamaq/CITEseq_AML_Analysis.git
cd CITEseq_AML_Analysis
```
### ⚙️ Install Dependencies

```bash
pip install -r requirements.txt
```

### Benchmarks
The benchmarking script compares memory usage and access speed of .h5ad files in two modes:

#### 🚀 Unbacked Mode:
- Faster read times.
- Higher memory usage during runtime.
####  🧠 Backed Mode:
- More memory-efficient.
- Slower read times.

The benchmarking results are logged for detailed performance analysis, helping optimize dataset handling strategies.
