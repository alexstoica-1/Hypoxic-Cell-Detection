# Hypoxic Cell Detection

A machine learning project to classify **hypoxic vs. normoxic** single cells from two breast cancer related cell lines using two sequencing technologies.

## Overview
- **Cell lines:** MCF7, HCC1806  
- **Technologies:** SmartSeq (deep, fewer cells), DropSeq (shallow, more cells)  
- **Labels:** `Hypoxic` / `Normoxic`  
- **Matrix shape:** genes as **rows**, cells as **columns**  
- **Objective:** build the best classifier per dataset and report accuracy on held-out data.

## Datasets
- **SmartSeq–MCF7**
- **SmartSeq–HCC1806**
- **DropSeq–MCF7**
- **DropSeq–HCC1806**

> SmartSeq provides deeper per‑cell coverage; DropSeq provides more cells with sparser counts.

## Exploratory Highlights
- Highly **sparse** matrices; many zero counts.
- Expression scale differs across cells/genes → **normalization** and **log transform** needed.
- **MCF7** shows clearer separation by condition than **HCC1806** in low‑dimensional projections.
- Feature >> sample → **dimensionality reduction / feature selection** is beneficial.

## Preprocessing
**Quality Control (per dataset)**
- Remove low‑quality cells using:
  - **Total reads**: SmartSeq threshold ≈ **100k**.
  - **Expressed genes**: SmartSeq threshold ≈ **5,000**; DropSeq filters at **50–70** genes.
  - **Mitochondrial %**: exclude cells **>10%**.
- Check duplicates (cells/genes); retain biologically duplicated “housekeeping” genes when appropriate.

**Normalization & Transform**
- Library‑size normalization (per cell).  
- **Log1p** transform to stabilize variance and reduce dominance of highly expressed genes.

**Feature Selection**
- Keep **high‑variance genes**; drop near‑constant genes.

## Unsupervised Learning
- **PCA** for visualization and compression.
- **Clustering** (K‑means, hierarchical) to probe structure.
- Findings: **SmartSeq–MCF7** shows clear hypoxic/normoxic separation; others are weaker or mixed.

## Supervised Learning
Models evaluated with grid search and 5‑fold CV; tested on held‑out data.

| Dataset | Best Model | Key Params | Test Accuracy |
|---|---|---|---|
| **DropSeq–MCF7** | **Kernel SVM (RBF)** | C=100, γ=0.001 | **97.5%** |
| **DropSeq–HCC1806** | **Kernel SVM (RBF)** | C=1, γ=scale | **94–95.5%** |
| **SmartSeq–MCF7** | **Linear SVM / Logistic / RF** | C=0.01 (SVM) | **≈100%** |
| **SmartSeq–HCC1806** | **SVM / Logistic** | C=0.01 (linear SVM) | **≈98.6%** |

Other models compared: **Logistic Regression, KNN, SVM, Kernel SVM, Naive Bayes, Random Forest**.  
Naive Bayes underperformed, especially on **HCC1806**.

## Conclusions
- Clearer biological separation in **MCF7** than **HCC1806**; **SmartSeq** outperforms **DropSeq** overall.  
- **SVMs** (especially RBF on DropSeq, linear on SmartSeq) provide the most reliable performance.

## Reproducibility
1. **Environment**: Python 3.13 with standard ML/SC libraries (numpy, pandas, scikit‑learn, scipy, matplotlib).
2. **Data prep**: apply QC thresholds, normalize, log1p, and select high‑variance genes.
3. **Training**: PCA → model grid search with 5‑fold CV → evaluate on held‑out test split.
4. **Reporting**: save metrics and confusion matrices per dataset/model.

## Repository Structure
```
.
├─ .gitignore                   # empty
├─ notebook_SEQ.ipynb           # entire project
└─ README.md
```

