# Functional Network Dysconnectivity in Schizophrenia  
### An ICA–FNC Analysis of the COBRE Dataset

---

## Research Question

Schizophrenia is increasingly conceptualized as a disorder of large-scale brain network dysconnectivity rather than isolated regional dysfunction.

**This project follows the pipeline in Arbabshirani et al.(2013) and asks:**

> Can alterations in functional network connectivity (FNC) distinguish schizophrenia patients from healthy controls?

---

## Key Insight of This Project

Across 45 functional network connections, only one survived FDR correction:

> **Default Mode Network (DMN) – Somatomotor connectivity is significantly reduced in schizophrenia**

This suggests that schizophrenia may involve disrupted coordination between internally generated mental processes and externally driven sensorimotor systems.

## Dataset

- COBRE resting-state fMRI dataset  
- Subjects:  
  - Schizophrenia (SZ): 71  
  - Healthy Controls (HC): 74  
- Preprocessed using NIAK pipeline  

---

## Methods

### 1. Group ICA

- PCA dimensionality reduction  
- FastICA (n = 25 components)  
- Extraction of large-scale intrinsic networks  

---

### 2. Network Selection

- Spatial correlation with Yeo 7-network atlas  
- Retained 10 components corresponding to canonical networks:
  - Default Mode Network (DMN)
  - Somatomotor
  - Visual
  - Attention networks
  - Frontoparietal

---

### 3. Dual Regression

- Subject-specific time courses  
- Subject-specific spatial maps  

---

### 4. Functional Network Connectivity (FNC)

- Pearson correlation between ICA time courses  
- Fisher z-transformation applied  

---

### 5. Statistical Analysis

- Welch’s t-test (HC vs SZ)  
- False Discovery Rate (FDR) correction  
- Effect size (Cohen’s d)  

---

### 6. Classification

- Logistic Regression (L1 regularization)  
- Cross-validation + permutation testing  

---

## Key Findings

### 1. Network-Level Dysconnectivity

A single connection survived FDR correction:

> **DMN ↔ Somatomotor connectivity is significantly reduced in schizophrenia**

- t = 3.70  
- p = 0.00036  
- q = 0.016 (FDR-corrected)  
- Cohen’s d = 0.74  

---

### 2. Interpretation

This may reflect disrupted coordination between:

- internally directed processes (DMN)  
- externally driven sensorimotor processing  

consistent with the **dysconnection hypothesis of schizophrenia**.

---

### 3. Classification Performance

- Test AUC: **0.85**  
- Permutation p-value: **0.001**  

Indicating that network-level connectivity features carry predictive information about diagnosis.

---

## Future Directions

- Dynamic functional connectivity (dFNC)  
- Graph theoretical analysis  
- Multimodal fusion (sMRI + fMRI)  
- Application to other psychiatric disorders  

---
