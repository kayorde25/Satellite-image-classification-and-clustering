# Satellite Image Embedding Benchmarking and Clustering

This project evaluates pretrained vision models on satellite imagery by extracting image embeddings, reducing dimensionality, clustering tiles, and comparing cluster quality across methods. The goal is to move beyond simple classification and toward a reproducible pipeline for embedding-based search, clustering, and Earth observation analysis.

## Key Features
- Pretrained embedding extraction from satellite images
- Dimensionality reduction with PCA and UMAP
- Clustering with KMeans and HDBSCAN
- Quantitative evaluation with ARI, NMI, and silhouette score
- Qualitative inspection of clusters
- Reproducible notebook and script-based workflow

- Satellite-image-classification-and-clustering/
│
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_embedding_extraction.ipynb
│   ├── 03_clustering_kmeans_vs_hdbscan.ipynb
│   └── 04_model_comparison.ipynb
│
├── src/
│   ├── data.py
│   ├── embed.py
│   ├── cluster.py
│   ├── evaluate.py
│   ├── visualize.py
│   └── utils.py
│
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── sample_clusters/
│
└── docs/
    └── methodology.md


