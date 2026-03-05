# PVCA: Cellular Automata and Spatiotemporal Big Data Driven Framework for Solar Photovoltaic Deployment

## 📖 Introduction

This repository contains the official implementation and demonstration code for the paper: **"PVCA: Cellular Automata and Spatiotemporal Big Data Driven Framework for Solar Photovoltaic Deployment"**.

The **PVCA (Photovoltaic Cellular Automata)** framework integrates Cellular Automata with spatiotemporal big data to simulate and optimize the spatial layout of solar photovoltaic (PV) installations.

> **Note on Performance:** To ensure that the code can be executed locally on most standard computers, this demonstration utilizes a **lower spatial resolution strategy**. This includes an additional resampling operation, significantly reducing computational overhead while maintaining model integrity.

## 🛠️ Hybrid Workflow (ArcMap + Python)

The methodology follows a hybrid approach, leveraging the spatial processing power of **ArcMap** for foundational data preparation and **Python/Jupyter** for core modeling.

### 1. GIS Preprocessing (ArcMap)

Before running the provided scripts, the following operations are conducted within **ArcMap**:

* **Geospatial Preprocessing**: Projection transformations, clipping, and alignment of multi-source spatial datasets.
* **Basic Spatial Calculations**: Generation of Euclidean distances, slope/aspect analysis from DEM, and zonal statistics.
* **Data Preparation**: Initial cleaning of raw spatiotemporal big data.
* **PV Status Analysis**: Spatial distribution analysis of current photovoltaic installations to establish the baseline for simulation.
* ... ... ...

### 2. Core Modeling & Simulation (Jupyter Notebooks)

Once the GIS layers are prepared, the analysis proceeds through the following notebooks:

* **`S1_CalculateShapleyScore.ipynb`**: Calculates non-linear effects and implements spatialization. It quantifies the influence of driving factors on PV deployment using Shapley values.
* **`S2_ConstructionSuitabilityAtlas.ipynb`**: Establishes the PV Construction Suitability Atlas by synthesizing processed GIS layers.
* **`S3_PVCA_Simulation_Examples.ipynb`**: Interactive simulation demonstrating the spatiotemporal evolution of PV capacity.
* **`Z1_StatisticalSampling_CategoricalVariables.ipynb`**: Statistical sampling for categorical variables (e.g., land use).
* **`Z2_GeoDataPreprocessingAlignment.ipynb`**：Preprocessing of geographic data.
* **`Z3_StatisticalSampling_ContinuousVariable.ipynb`**: Statistical sampling and cleaning for continuous variables (e.g., Meteorology, society, distance, elevation).
* ... ... ...

## 🚀 Getting Started

1. **Prepare GIS Data**: Use ArcMap to export your spatial variables as TIFF or ASCII formats compatible with `rasterio`/`numpy`.
2. **Environment Setup**:
```bash
pip install numpy pandas geopandas rasterio matplotlib seaborn shap scikit-learn ... ... ...
```

3. **Run Sequence**: Execute notebooks in the order **S1 $\rightarrow$ S2 $\rightarrow$ S3**. Ensure that the resampling logic in the scripts matches your desired output resolution.

## 📄 Citation

If you use this framework or code in your research, please cite the original paper:
*PVCA: Cellular Automata and Spatiotemporal Big Data Driven Framework for Solar Photovoltaic Deployment*
