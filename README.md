# Link Prediction Experiments on SNAP Network Datasets

This repository contains notebooks used to evaluate several **link prediction methods** on real-world network datasets.

The experiments compare classical structural heuristics with embedding-based machine learning models.

All datasets used in the project come from the **Stanford Network Analysis Project (SNAP)**.

SNAP dataset collection:  
https://snap.stanford.edu/data/

---

# Repository Structure
├── notebooks
│ ├── baseline_heuristics.ipynb
│ └── ai_link_prediction.ipynb
├── README.md


---

# Notebooks

### baseline_heuristics.ipynb

This notebook evaluates classical link prediction heuristics:

- Common Neighbors
- Adamic–Adar
- Jaccard Similarity

The notebook removes a fraction of edges from each network and measures how well these heuristics recover the missing edges.

---

### ai_link_prediction.ipynb

This notebook evaluates machine learning approaches:

- Node2Vec embeddings
- Multilayer Perceptron (MLP)
- Deep Q-Network (DQN)

Node embeddings are learned from the observed graph and used to construct edge-level features for prediction.

---

# Datasets

All networks are downloaded directly from **SNAP**.

### Facebook Social Circles

Nodes: 4039  
Edges: 88,234  

Dataset link:  
https://snap.stanford.edu/data/facebook_combined.txt.gz

---

### ArXiv GR-QC Collaboration Network

Nodes: 5242  
Edges: 14,496  

Dataset link:  
https://snap.stanford.edu/data/ca-GrQc.txt.gz

---

### Email Communication Network

Nodes: 1005  
Edges: 16,706  

Dataset link:  
https://snap.stanford.edu/data/email-Eu-core.txt.gz

---

# Running the Notebooks

Run the notebooks in the following order:

1. `notebooks/baseline_heuristics.ipynb`
2. `notebooks/ai_link_prediction.ipynb`

The notebooks will automatically download the required datasets from SNAP.

---

# Data Source

Stanford Network Analysis Project (SNAP)

Jure Leskovec and Andrej Krevl  
*SNAP Datasets: Stanford Large Network Dataset Collection*

https://snap.stanford.edu/data/
