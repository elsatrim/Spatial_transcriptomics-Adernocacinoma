# 🧬 Spatial Transcriptomics Analysis of Lung Tissue (10x Visium HD)

This project presents a complete workflow for the processing and analysis of **spatial transcriptomics data** from human lung adenocarcinoma using **10x Genomics Visium HD** technology. The goal is to explore **spatial gene expression patterns**, identify **tissue domains**, and characterize **cellular heterogeneity** within the tumor microenvironment.

---

## 📌 Overview

Spatial transcriptomics enables the study of gene expression while preserving spatial context within tissues. In this project, we:

- Perform **data preprocessing and quality control**
- Normalize gene expression data
- Identify **spatially variable genes (SVGs)**
- Detect **spatial domains (clusters)**
- Annotate clusters using **marker genes**
- Conduct **functional enrichment analysis**

---

## 🧪 Dataset

- **Source:** 10x Genomics  
- **Dataset:** Visium HD Spatial Gene Expression – Human Lung Cancer (Fixed Frozen)  
- **Sample:** Lung adenocarcinoma tissue  

🔗 https://www.10xgenomics.com/datasets/visium-hd-cytassist-gene-expression-human-lung-cancer-fixed-frozen

**Metadata:**
- Sex: Female  
- Age: 79  
- Processed using **Space Ranger pipeline**

---

## 🛠️ Tools & Libraries

- Python  
- Scanpy  
- Squidpy  
- gProfiler  
- CellMarker  

---

## 🔄 Analysis Pipeline

### 1. Data Loading & Visualization
- Loaded count matrices and spatial coordinates  
- Integrated spatial information into AnnData object  
- Visualized tissue image and gene expression patterns  

### 2. Quality Control & Preprocessing
- Computed QC metrics:
  - Total counts  
  - Number of genes  
  - Mitochondrial gene percentage  
- Filtered:
  - Low-quality spots  
  - Lowly expressed genes  

### 3. Normalization
- Library size normalization  
- Log-transformation of expression values  

### 4. Spatially Variable Genes (SVGs)
- Identified highly variable genes  
- Computed Moran’s I statistic  
- Selected genes with strong spatial structure  

### 5. Dimensionality Reduction
- Performed PCA on spatially variable genes  
- Visualized principal components  

### 6. Spatial Domain Detection
- Built gene expression and spatial neighbor graphs  
- Combined both graphs  
- Applied Leiden clustering  

➡️ Identified **8 spatial domains**

### 7. Marker Gene Identification
- Differential expression (Wilcoxon test)  
- Annotated clusters using CellMarker  

**Identified cell types:**
- Stromal cells  
- Alveolar macrophages  
- B-cells  
- Alveolar type II cells  
- Mesenchymal cells  
- Muscularis cells  
- Mast cells  
- Lymphatic endothelial cells  

### 8. Functional Enrichment Analysis
- Performed using gProfiler  

Example (Alveolar macrophages):
- Upregulated:
  - Immune response  
  - T-cell activation  
- Downregulated:
  - Cell migration  
  - Cell adhesion  

---

## 📊 Key Results

- Spatially structured gene expression patterns identified  
- Biologically meaningful tissue domains detected  
- Cell-type-specific regions annotated  
- Functional insights aligned with cancer biology literature  

---

## 🧠 Insights

- Spatial transcriptomics reveals tumor microenvironment organization  
- Immune regions show strong specialization  
- Combining spatial + transcriptomic data improves interpretation  

---

## ⚠️ Limitations

- Single dataset  
- Manual annotation  
- No advanced ML models  

---

## 🚀 Future Work

- Apply deep learning / representation learning  
- Integrate multiple datasets  
- Explore graph-based methods (GNNs)  
- Improve automated annotation  

---

## 📁 Project Structure
project/
├── data/
├── notebooks/
├── results/
└── README.md


---

## ▶️ How to Run (in bash)
pip install scanpy squidpy pandas numpy matplotlib


## Download dataset from 10x Genomics and run the notebook (in bash):
jupyter notebook


## 👩‍💻 Author
Elsa Sánchez Fernández
MSc Data Science – EPFL
