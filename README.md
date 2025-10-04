# DA5401 Assignment 5: Manifold Learning for Data Visualization

## Student Information
- **Name**: Saggurthi Dinesh
- **Roll Number**: BE21B032
- **Email**: be21b032@smail.iitm.ac.in
- **Course**: DA5401 - Data Analytics Laboratory
- **Assignment**: Assignment 5

## Project Structure
```
DA5401_A5/
├── DA5401_A5_Manifold_Visualization.ipynb # Main notebook
├── yeast.arff # Dataset file
└── README.md # This file
```

## Requirements
- **Python**: 3.8+
- **Required Packages**:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

## Installation
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

# Yeast Gene Expression Manifold Learning

## Dataset Overview

- **File:** `yeast.arff`
- **Format:** ARFF (Attribute-Relation File Format) — Loadable via SciPy
- **Source:** Yeast Gene Expression Data
- **Features:** 103 numeric attributes representing gene expression levels
- **Target:** 14 binary labels indicating functional categories
- **Type:** Multi-label classification problem

### Data Challenges

The dataset contains various veracity issues, including:

- Noisy labels
- Experimental outliers
- Ambiguous samples due to overlapping functional boundaries

---

## Project Breakdown

### Part A: Data Loading and Preprocessing [5 points]

- Loaded `yeast.arff` dataset
- Performed feature preprocessing and scaling
- Conducted exploratory data analysis (EDA)

### Part B: Manifold Learning Implementation [25 points]

#### t-SNE Implementation [10 points]

- Applied **t-SNE** for 2D dimensionality reduction
- Visualized **local neighborhood structures**
- Analyzed **probabilistic similarity preservation**

#### Isomap Implementation [15 points]

- Applied **Isomap** for manifold learning
- Tuned `n_neighbors` parameter for connected manifold
- Preserved **global geometric structure**

---

## Part C: Comparative Analysis and Interpretation [20 points]

- Performed **quantitative and qualitative comparison** of t-SNE and Isomap
- Analyzed manifold structure implications for classification
- Evaluated data challenges through visualization

---

## Key Results

| Algorithm | Distance Correlation | Primary Strength              |
|-----------|----------------------|-------------------------------|
| Isomap    | 0.4739               | Global Structure Preservation |
| t-SNE     | 0.4046               | Local Cluster Separation      |

### Key Findings

- **Isomap**: Successfully "unrolled" the data manifold, revealing a continuous structure and smooth transitions across functional classes.
- **t-SNE**: Generated tight, well-separated clusters, highlighting fine-grained local similarities.
- **Algorithm Selection**: Choice depends on analysis goals:
  - Use **Isomap** for preserving global geometry
  - Use **t-SNE** for exploring local topology
- **Classification Insight**: The data's moderate manifold complexity implies the need for non-linear classification models.
---


