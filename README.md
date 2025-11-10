# WRF-XGBoost-FAHP-Urban-Heat-Stress-Risk
A hybrid modeling framework integrating WRF, XGBoost, and Fuzzy AHP for multi-year urban heat stress risk assessment in Tehran (2019–2022).

### 🧠 Overview
This repository provides the complete workflow, datasets, and scripts developed for the study:

> **“A Hybrid WRF–XGBoost–FAHP Framework for Multi-Year Urban Heat Stress Risk Assessment in Tehran (2019–2022)”**

The framework integrates **numerical modeling (WRF)**, **machine learning downscaling (XGBoost)**, and **multi-criteria decision-making (Fuzzy AHP)** to model and evaluate urban heat stress risk in Tehran.

---

### 🌍 Study Scope
- **Study area:** Tehran Metropolitan Region, Iran  
- **Period:** Four major heatwave events between **2019–2022**  
- **Objective:** Improve spatial resolution and interpretability of urban heat stress mapping  

---

### ⚙️ Methodological Workflow
<img width="4794" height="5744" alt="2) Methodology" src="https://github.com/user-attachments/assets/de7067e4-c7bb-4d0a-aa6a-d123538d6653" />



#### 1️⃣ WRF-Based Numerical Downscaling
- Dynamic simulation of near-surface air temperature (**T2**)  
- Nested configuration refined from **0.25° → 1 km resolution**  
- Validation with ground-based meteorological stations  

#### 2️⃣ Machine Learning Downscaling (XGBoost)
- Further refinement of **T2 layer from 1 km → 100 m resolution**  
- Input features: LST, NDVI, NDBI, slope, elevation, and urban morphology indicators  
- Model optimized using **Bayesian hyperparameter tuning** and **5-Fold Cross-Validation**  
- Explainable AI (**SHAP**) applied for feature importance analysis  

#### 3️⃣ Heat Stress Risk Mapping (Fuzzy AHP)
- Integration of multi-year downscaled T2 maps with socio-economic and urban indicators  
- Weighted overlay using **Fuzzy Analytic Hierarchy Process (FAHP)**  
- Final outputs: multi-year averaged risk maps (2019–2022)  

---

### 📊 Key Results
| Model | Resolution | R² (%) | RMSE (°C) | MAE (°C) |
|--------|-------------|--------|------------|-----------|
| WRF T2 | 1 km | 73.34 | 0.885 | 0.677 |
| XGBoost Downscaled | 100 m | 79.14 | 0.753 | 0.603 |

✅ The hybrid approach improved spatial detail and reduced errors, demonstrating robust generalizability across multiple heatwave periods.

---
### 🛠️ Technical Environment
| Component | Version / Tool |
|------------|----------------|
| Python | 3.9+ |
| XGBoost | 2.0+ |
| Hyperopt | 0.2.7 |
| GDAL / Rasterio | 3.6+ |
| NumPy / Pandas / Scikit-learn | Latest stable |
| ArcGIS Pro / QGIS | For visualization |
| WRF Model | v4.3.3 |

---

### 🧾 Citation
If you use this repository or data in your research, please cite as:

> Ganjirad, M., Bagheri, H., (2025).  
> **A Hybrid WRF–XGBoost–FAHP Framework for Multi-Year Urban Heat Stress Risk Assessment in Tehran (2019–2022)**.  
> *(Manuscript under review)*.

---

### 📬 Contact
**Author:** Mohammad Ganjirad  
**Email:** [moh.ganjirad@gmail.com]  
**GitHub:** [https://github.com/mganjirad](https://github.com/mganjirad)

---

### 🪴 License
This project is licensed under the **MIT License** – free to use, modify, and share with proper attribution.

---

### 💡 Highlights
- Multi-year heatwave simulation (2019–2022) using WRF  
- Data-driven downscaling with explainable ML  
- Comprehensive socio-environmental risk assessment via FAHP  
- Reproducible and transferable framework for other urban regions  

