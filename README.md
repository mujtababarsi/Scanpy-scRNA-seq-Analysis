# Scanpy scRNA-seq Analysis
this workflow modeled by Guidlines of [Scanpy Tutorial](https://scanpy-tutorials.readthedocs.io/en/latest/pbmc3k.html) which is inspired by [(Satija et al., 2015)](https://www.nature.com/articles/nbt.3192). Scanpy is a scalable toolkit for analyzing
single-cell gene expression data built jointly with anndata. It includes preprocessing, visualization, clustering, trajectory inference and differential expression 
testing. The Python-based implementation efficiently deals with datasets of more than one million cells.
## Preprocessing & Clustering 3K PBMC
##### the Dataset:   The dataset of 3K Peripheral Blood Mononuclear Cells (PBMCs) obtained from a Healthy Donor available from 10X Genomics, sequenced on the Illumina NextSeq 500. Matrix Data File: 10X Genomics formatted single-cell RNA-seq count matrix of 2,700 single PBMCs

#### 1.preprocessing:
* filtering the data with respect to the minimum counts of genes per cell 
and the minimum counts genes presence in number of cells
* Removing the cells that obtain high expressed level of mitochondrial genes 
* Normalization the data and log-transformed the data
* Dimensionality reduced with PCA and Neighborhood Graph computed and embedded
#### 2.Clustering:
* Leiden cluster is used to obtain well-connnected cluster
#### 3.Finding marker genes:
* Ranking for highly differential genes computed in each cluster 
* Cell type marked
## Trajectory inference for hematopoiesis in mouse
##### the Dataset: Reconstructing myeloid and erythroid differentiation for data of [Paul et al. (2015).](https://www.cell.com/cell/fulltext/S0092-8674(15)01493-2?_returnURL=https%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS0092867415014932%3Fshowall%3Dtrue)
#### Process description:
#### 1.Preprocessing and Visualization:
* the data preprocessed with zheng17 recipe 
* PCA and neighborhood computed
* draw graph computed and plotted 
#### 2.Clustering and PAGA:
* louvain cluster is used and embedded
* Recompute the embedding using PAGA-initialization
* Reconstruct gene changes along PAGA paths for a given set of genes
## Analysis and visualization of spatial transcriptomics data
##### the Dataset:
## Integrating spatial data with scRNA-seq using scanorama
