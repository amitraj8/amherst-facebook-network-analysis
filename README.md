# Social Network Analysis of Amherst College Facebook Connections

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![NetworkX](https://img.shields.io/badge/NetworkX-3.x-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## 📌 Overview
Analysis of the Amherst College Facebook friendship network from the 
[Network Repository (socfb-Amherst41)](https://networkrepository.com/socfb-Amherst41.php).
The project identifies communities, key influencers, and compares the real 
network against classical random-graph models.

## 📊 Dataset
| Property | Value |
|---|---|
| Nodes | 2,235 |
| Edges | 90,954 |
| Avg. Degree | 81.39 |
| Density | 0.0364 |
| Type | Undirected, unweighted, homogeneous |

## 🎯 Objectives
1. Characterize the network's structural properties
2. Detect communities (Louvain, Label Propagation, Girvan–Newman)
3. Identify key influencers via centrality measures
4. Compare against ER, BA, and WS models

## 🛠 Methods & Tools
- **Tools:** Python, NetworkX, Pandas, Matplotlib, SciPy
- **Centrality:** Degree, Betweenness, Closeness, Eigenvector
- **Models:** Erdős–Rényi, Barabási–Albert, Watts–Strogatz

## 📈 Key Findings

### Small-World Properties
- Clustering coefficient: **0.31** (~8.5× higher than ER)
- Average path length: **2.40** (short, small-world)
- Power-law-ish degree distribution with hubs

### Model Comparison
| Metric | Amherst | ER | BA | WS |
|---|---|---|---|---|
| Avg. Degree | 81.39 | 81.40 | 78.57 | 80.00 |
| Clustering | 0.31 | 0.04 | 0.09 | 0.55 |
| Avg. Path Length | 2.40 | 2.01 | 2.05 | 2.49 |

**Conclusion:** The Amherst network is a **hybrid of BA and WS** — hubs emerge 
from preferential attachment while local structure shows triadic closure.


## 🚀 Getting Started
```bash
git clone https://github.com/YOUR_USERNAME/amherst-facebook-network-analysis.git
cd amherst-facebook-network-analysis
pip install -r requirements.txt
jupyter notebook notebooks/Social_Network_Project.ipynb
