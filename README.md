# R-bsts-stress-analysis
Analysis of stress data from wearable devices using R and Bayesian time series models, with the aim of detecting interpersonal stress events based on changes in stress levels.

Wearable Stress Analysis: Detecting Interpersonal Stress Events
📖 Overview
This repository contains an analysis of stress data collected from a wrist-worn wearable device (Garmin vivosmart 5) to detect interpersonal stress events.
The study focuses on:

Continuous stress measurement using Personal Health Records (PHR)
Missing data imputation with Bayesian Kalman Filter
Intervention effect evaluation using Bayesian Structural Time Series (BSTS)

🎯 Research Objective
To verify whether stress levels increase after interpersonal stress events and evaluate the effect of intervention (discussion) on stress reduction.

🛠 Tools & Environment
Device: Garmin vivosmart 5
App: Garmin Connect
Language: R (RStudio 2025.05.1 Build 513)
Key Packages:KFAS (Kalman filtering)
bsts (Bayesian Structural Time Series)
ggplot2 (Visualization)
dplyr, tidyr (Data wrangling)

📂 Repository Structure
wearable-stress-analysis/
├── README.md
├── data/
│   ├── raw/        # Original CSV from Garmin Connect
│   └── processed/  # Imputed data
├── scripts/
│   ├── 01_preprocessing.R
│   ├── 02_missing_imputation.R
│   ├── 03_bsts_analysis.R
│   └── 04_visualization.R
├── results/
│   ├── figures/    # Plots (time series, intervention effect)
│   └── tables/     # Statistical outputs
└── docs/
    └── report.pdf  # Full research report

🔍 Analysis Workflow
Data PreprocessingLoad raw stress data
Handle missing values
Explore daily patterns
Missing Value ImputationApply Bayesian Kalman Filter using KFAS
Intervention Effect EvaluationUse BSTS to estimate causal impact of intervention
VisualizationTime series plots
Intervention effect comparison

📊 Key Findings
Stress levels showed a decreasing trend over the observation period.
Intervention effect was suggestive but not statistically significant (p = 0.441).
High uncertainty due to missing data and single-subject design.

▶ How to Reproduce

Clone this repository:
git clone https://github.com/yourusername/wearable-stress-analysis.git

Install required R packages:
install.packages(c("KFAS", "bsts", "ggplot2", "dplyr", "tidyr"))

Run scripts in order:
source("scripts/01_preprocessing.R")
   source("scripts/02_missing_imputation.R")
   source("scripts/03_bsts_analysis.R")
   source("scripts/04_visualization.R")

📌 Future Improvements
Introduce covariates (e.g., distance to stressor)
Reduce missing data ratio
Explore Single Case Design for robust inference

📜 LicenseMIT License
