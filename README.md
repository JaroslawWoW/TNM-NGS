# 🧬 Predicting Renal Tumor Staging Using Machine Learning

# 📄 Overview
This repository contains the code and analysis for a project aimed at evaluating whether machine learning models can predict the TNM staging (Tumor, Node, Metastasis) of renal adenoma and adenocarcinoma based on gene expression data (read counts).

The motivation behind this work was to explore the potential of transcriptomic profiling as a source of non-invasive diagnostic information to support cancer staging.

# 💡 Data
Source: National Cancer Institute (public repository).

Format: Gene expression data in the form of raw read counts.

Samples: Nearly 3,000 observations collected after pre-processing.

Challenge: Severe class imbalance, especially in the metastasis (M) stage.

To address class imbalance, the ADASYN (Adaptive Synthetic Sampling) technique was tested for the M stage, but ultimately these synthetic results were excluded from the final analysis due to questionable reliability.

# 🧪 Methods
Seven machine learning algorithms were trained and evaluated:

Decision Tree

Random Forest

k-Nearest Neighbors (k-NN)

Gradient Boosting

Extreme Gradient Boosting (XGBoost)

Neural Network

(Additional ensemble or variant methods, as appropriate)

## Evaluation
Metric: f1-score (to balance precision and recall in imbalanced data).

Validation: Stratified 5-fold cross-validation.

Implementation: Python-based environment, using scikit-learn, XGBoost, and PyTorch (or other relevant frameworks).

# 📊 Results
The models showed varying performance depending on the TNM subcomponent:

Stage	Best f1-score (%)
T	48%
N	52%
M	23%

Despite using diverse algorithms and hyperparameter tuning, the models failed to achieve clinically useful accuracy levels.

# ⚠️ Conclusions
The current gene expression dataset does not allow reliable TNM staging prediction for renal adenomas and adenocarcinomas.

The models cannot yet be recommended as diagnostic tools.

Possible future improvements include:

Increasing the sample size.

Further balancing the classes.

Incorporating additional omics data or clinical variables.

# ⚙️ Requirements
Python >= 3.8

scikit-learn

xgboost

imbalanced-learn

pandas, numpy, matplotlib, seaborn (for analysis & visualization)

# 👨‍🔬 About
This project was created as part of a bioinformatics research study focused on exploring machine learning applications in translational oncology.

# 📫 Contact
If you have questions or ideas for collaboration, feel free to open an issue or reach out directly!

# ⚖️ Disclaimer: This repository is for research purposes only and is not intended for clinical use.
