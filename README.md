# PVCA: Cellular Automata and Spatiotemporal Big Data Driven Framework for Solar Photovoltaic Deployment

## 📖 Introduction

This repository contains the official implementation and demonstration code for the paper: **"PVCA: Cellular Automata and Spatiotemporal Big Data Driven Framework for Solar Photovoltaic Deployment"**.

The PVCA  framework integrates Cellular Automata with spatiotemporal big data to simulate and optimize the spatial layout of solar photovoltaic (PV) installations. To ensure that the code can be executed locally on most standard computers, this demonstration utilizes a **lower spatial resolution strategy** (including an additional resampling step to convert 50m PV data to 100m) to reduce computational overhead while maintaining the integrity of the model logic.

## 📂 Repository Structure

The project is organized into several Jupyter Notebooks following the research workflow:

### Core Methodology

* **`S1_CalculateShapleyScore.ipynb`**: Calculates non-linear effects and implements spatialization. It quantifies the influence of various driving factors on PV deployment using Shapley values.
* **`S2_ConstructionSuitabilityAtlas.ipynb`**: Establishes the PV Construction Suitability Atlas. It synthesizes multi-source big data to generate the foundational suitability maps required for CA simulation.
* **`S3_PVCA_Simulation_Examples.ipynb`**: Provides interactive simulation examples. It demonstrates how the PVCA framework drives the spatiotemporal evolution of PV capacity under different scenarios.

### Statistical Analysis & Preprocessing

* **`Z1_StatisticalSampling_CategoricalVariables.ipynb`**: Statistical sampling and analysis for categorical variables (e.g., land use types, administrative divisions).
* **`Z_StatisticalSampling_ContinuousVariable.ipynb`**: Statistical sampling and data cleaning for continuous variables (e.g., solar irradiance, slope, distance to grid).

## 🛠️ Usage & Performance Optimization

1. **Spatial Resampling**: Please note that this version includes a specific step to downsample 50m data to 100m. This is intentional to ensure the model remains accessible for local testing without high-end server requirements.
2. **Execution Order**: It is recommended to run the notebooks in the sequence of **S1 $\rightarrow$ S2 $\rightarrow$ S3** to ensure that intermediate variables and suitability maps are correctly generated.
3. **Customization**: Users can modify the transition rules and parameters within `S3` to explore how different policy constraints or environmental factors impact the future layout of solar energy.

## 🚀 Environment Setup

The following libraries are required to run the notebooks:

* `numpy`, `pandas` (Data manipulation)
* `geopandas`, `rasterio` (Geospatial analysis)
* `matplotlib`, `seaborn` (Visualization)
* `shap` (For Shapley value calculations in S1)
* `scikit-learn` (Machine learning utilities)
* `... ... ...
---
