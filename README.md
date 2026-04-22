# Satellite Image Embedding Benchmarking and Clustering

This project explores how pretrained computer vision models can be used to extract embeddings from satellite imagery and group similar image tiles using unsupervised learning.

The goal is to move beyond simple classification and build a reproducible baseline pipeline for:

- embedding extraction
- dimensionality reduction
- clustering
- evaluation
- qualitative inspection

## Dataset
This project uses the EuroSAT dataset, derived from Sentinel-2 satellite imagery.

## Methods
- Pretrained ResNet50 for embedding extraction
- PCA for dimensionality reduction
- KMeans and HDBSCAN for clustering
- UMAP for 2D visualization
- ARI, NMI, and silhouette score for evaluation

## Why this project matters
Satellite imagery often contains overlapping, ambiguous, and mixed land-use patterns. Embedding-based clustering helps discover structure in the data without relying entirely on labels.

## Current Benchmark
This baseline compares:
- ResNet50 embeddings
- KMeans clustering
- HDBSCAN clustering

## Repository Structure
```text
.
├── README.md
├── requirements.txt
├── satellite_image_clustering.ipynb
└── outputs/
