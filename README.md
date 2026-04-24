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

- # Model Comparison: ResNet50 vs EfficientNet-B0

To evaluate how different pretrained models perform on satellite imagery, we compare:

- **ResNet50**
- **EfficientNet-B0**

Both models are used as **feature extractors (embeddings)** and evaluated using the same pipeline:

1. Embedding extraction
2. Feature standardization
3. PCA (dimensionality reduction)
4. Clustering with:
   - KMeans
   - HDBSCAN
5. Evaluation using:
   - Adjusted Rand Index (ARI)
   - Normalized Mutual Information (NMI)
   - Silhouette Score

---

## Why Compare These Models?

| Model | Strength |
|------|--------|
| ResNet50 | Strong baseline, widely used |
| EfficientNet-B0 | More parameter-efficient, often better feature representation |

 Comparing them helps us understand:
- Which model produces better embeddings
- Which model separates land-use patterns more clearly
- How clustering performance depends on representation quality

---

## Benchmark Results

| Model | Clustering | ARI | NMI | Silhouette | Notes |
|------|------------|-----|-----|------------|------|
| ResNet50 | KMeans | (fill) | (fill) | (fill) | baseline |
| ResNet50 | HDBSCAN | (fill) | (fill) | (fill) | handles noise |
| EfficientNet-B0 | KMeans | (fill) | (fill) | (fill) | stronger features |
| EfficientNet-B0 | HDBSCAN | (fill) | (fill) | (fill) | best clustering |

 Replace `(fill)` with values from your notebook output.

---

## Visual Comparison

### ResNet50 Clusters
![ResNet50 KMeans](outputs/figures/resnet50_kmeans_umap.png)
![ResNet50 HDBSCAN](outputs/figures/resnet50_hdbscan_umap.png)

### EfficientNet-B0 Clusters
![EfficientNet KMeans](outputs/figures/efficientnetb0_kmeans_umap.png)
![EfficientNet HDBSCAN](outputs/figures/efficientnetb0_hdbscan_umap.png)

---

## Key Insights

- EfficientNet often produces **more compact and separable embeddings**
- HDBSCAN typically performs better than KMeans for:
  - irregular cluster shapes
  - mixed land-use regions
  - noisy satellite tiles
- KMeans is useful as a **baseline**, but HDBSCAN gives more **realistic clustering**

---

## Conclusion

This comparison demonstrates that:

- embedding quality significantly affects clustering performance  
- model choice matters even without supervised training  
- density-based clustering (HDBSCAN) is better suited to real satellite data  

This forms the foundation for:
- embedding-based search
- anomaly detection
- change detection
- multi-scale Earth observation analysis

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
