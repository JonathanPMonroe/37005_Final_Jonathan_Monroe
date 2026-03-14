# Reconstructing Missing Social Network Links with Structural Baselines and AI Models

This repository contains notebooks used to evaluate several **link prediction methods** on real-world network datasets.

The experiments compare classical structural heuristics with embedding-based machine learning models.

For an in-depth explanation of the experiments and processes used in this project, please reference the following post:

https://open.substack.com/pub/jonathanmonroe/p/reconstructing-missing-social-network?utm_campaign=post-expanded-share&utm_medium=web

All datasets used in the project come from the **Stanford Network Analysis Project (SNAP)**.

SNAP dataset collection (by Jure Leskovec and Andrej Krevl):  
https://snap.stanford.edu/data/

---

## Notebooks

### `data_exploration.ipynb`

Initial exploration of the SNAP datasets.  
Computes basic network statistics and generates structural visualizations.

---

### `baseline_link_prediction.ipynb`

Implements classical link prediction heuristics:

- Common Neighbors
- Adamic–Adar
- Jaccard Similarity

Edges are removed from each network and the heuristics are evaluated on their ability to recover the missing edges.

---

### `ai_link_prediction.ipynb`

Implements machine learning approaches for link prediction:

- Node2Vec node embeddings
- Multilayer Perceptron (MLP)
- Deep Q-Network (DQN)

Embeddings and structural features are used to predict missing edges.

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

## Running the Notebooks

Run the notebooks in the following order:

1. `Notebooks/data_exploration.ipynb`
2. `Notebooks/baseline_link_prediction.ipynb`
3. `Notebooks/ai_link_prediction.ipynb`

The notebooks automatically download the datasets from SNAP.

