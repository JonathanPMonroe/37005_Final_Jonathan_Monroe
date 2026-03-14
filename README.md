# Reconstructing Missing Social Network Links with Structural Baselines and AI Models

This repository contains notebooks used to evaluate several **link prediction methods** on real-world network datasets.

The experiments compare classical structural heuristics with embedding-based machine learning models.

For an in-depth explanation of the experiments and processes used in this project, please reference the following post:

https://open.substack.com/pub/jonathanmonroe/p/reconstructing-missing-social-network?utm_campaign=post-expanded-share&utm_medium=web

All datasets used in the project come from the **Stanford Network Analysis Project (SNAP)**.

SNAP dataset collection (by Jure Leskovec and Andrej Krevl):  
https://snap.stanford.edu/data/

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

## Running the Notebooks

Run the notebooks in the following order:

1. `Notebooks/data_exploration.ipynb`
2. `Notebooks/baseline_link_prediction.ipynb`
3. `Notebooks/ai_link_prediction.ipynb`

The notebooks automatically download the datasets from SNAP.

