# Scanpy-3K_PBMC-Downstream-Analysis
this workflow modeled by Guidlines of [Scanpy Tutorial](https://scanpy-tutorials.readthedocs.io/en/latest/pbmc3k.html). Scanpy is a scalable toolkit for analyzing
single-cell gene expression data built jointly with anndata. It includes preprocessing, visualization, clustering, trajectory inference and differential expression 
testing. The Python-based implementation efficiently deals with datasets of more than one million cells.
#### the Dataset:
The dataset of 3K Peripheral Blood Mononuclear Cells (PBMCs) obtained from a Healthy Donor available from 10X Genomics, sequenced on the Illumina NextSeq 500.

Matrix Data File: 10X Genomics formatted single-cell RNA-seq count matrix of 2,700 single PBMCs

### Process description:
#### 1. preprocessing:

   - filtering the data with respect to the minimum counts of genes per cell and the minimum counts genes presence in number of cells
	 - removing the cells that obtain high expressed level of mitochondrial genes 
	 - normalization the data and log-transformed the data
	 - Dimensionality reduced with PCA and Neighborhood Graph computed and embedded
#### 2. Clustering:
          - the step proceded using Leiden cluster to obtain well-connnected cluster
#### 3. Finding marker genes:
          - ranking for highly differential genes computed in each cluster 
					- cell type marked using 
