# Quantitative Geochemical and Geotechnical Assessment of Gully Erosion Susceptibility in the Anambra Basin, Southeastern Nigeria

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NNwobi-354/soil-properties-gully-development-anambra/blob/main/Statistical_Modelling_Soil_Properties_Gully_Development_Anambra.ipynb)
[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

This repository contains the dataset, statistical analysis workflow, and machine learning models for the geoscientific research study evaluating the intrinsic geochemical, mineralogical, and geomechanical controls driving severe gully erosion in the Anambra Basin, Southeastern Nigeria.

By contrasting baseline control terrains in the Imo Shale Formation (**Awka**) with active gully corridors in the Nanka Sands Formation (**Idemili**), this study establishes that gully vulnerability is fundamentally governed by a geochemical trade-off between unbonded quartzic framework grains and cohesive clay-sesquioxide binders ($\text{Fe}_2\text{O}_3$, $\text{Al}_2\text{O}_3$, $\text{MgO}$).

---

## Research Workflow & Methodology

The analytical pipeline follows a multi-stage quantitative workflow implemented entirely in Python:

1. **Laboratory Data Extraction & Structuring**:
   * **Geochemical Screening**: Major elemental oxides ($\text{SiO}_2$, $\text{Al}_2\text{O}_3$, $\text{Fe}_2\text{O}_3$, $\text{MgO}$, $\text{TiO}_2$, $\text{K}_2\text{O}$, $\text{Na}_2\text{O}$, $\text{CaO}$) and Silica-to-Sesquioxide Ratios ($\text{SSR}$).
   * **Mineralogical Scoring**: Quantitative Mineral Scores for Quartz, Kaolinite, Smectite, Goethite, and Hematite.
   * **Hydro-Textural Testing**: Particle Size Distribution (Sand, Silt, Clay fractions) and Atterberg Limits (Liquid Limit, Plastic Limit, Plasticity Index).

2. **Multivariate Pattern Recognition**:
   * Principal Component Analysis (PCA) for variance decomposition and dimensional reduction.
   * Unsupervised Ward's Hierarchical Clustering evaluated via Adjusted Rand Index (ARI).

3. **Predictive Diagnostic Modeling**:
   * $L_2$-Regularized Binary Logistic Regression to classify stable vs. active gully terrains based on core geochemical predictors.
   * Performance validation using Receiver Operating Characteristic (ROC-AUC) curves.

4. **Erodibility Index & Hazard Benchmarking**:
   * Formulation of a continuous **Soil Erodibility Index (SEI)** via PCA-weighted min-max normalization.
   * Optimization of a critical hazard decision threshold ($\text{SEI} \ge 0.54$) using Youden's $J$ statistic.

5. **Network Topology & System Modeling**:
   * Pairwise correlation network modeling ($\vert{}r\vert{} \ge 0.60$) displaying antagonistic partitioning between friable quartzic nodes and cohesive binder nodes.

---

## Repository Structure

```text
soil-properties-gully-development-anambra/
│
├── Statistical_Modelling_Soil_Properties_Gully_Development_Anambra.ipynb  # Primary Google Colab Workflow
├── data/
│   └── soil_analysis_cleaned_summary.csv                                # Processed CSV of laboratory results
├── README.md                                                            # Repository documentation
└── LICENSE                                                              # License details
