# Cancer Drug Response Prediction (CDRP)

An automated multi-model machine learning pipeline for predicting cancer drug response in colorectal cancer (COREAD) cell lines using binary genetic mutation fingerprints.

## Overview

This project implements a competitive ML framework that evaluates 12 different regression models to predict IC50 values (drug sensitivity) from genomic mutation data. The pipeline automatically selects the best-performing model for each drug using 5-fold cross-validation.

## Key Features

- **66-Gene Binary Fingerprint Matrix**: Converts mutation data into stable genomic signatures
- **12 ML Models**: Linear Regression, Lasso, Ridge, ElasticNet, SGD, KNN, Decision Tree, Random Forest, Gradient Boosting, XGBoost, SVR, MLP
- **Drug-Specific Model Selection**: Each drug gets its optimal model based on CV_MSE
- **Personalized Ranking Engine**: Generates Top-N therapy recommendations for patients
- **Glass-Box Interpretability**: Feature importance analysis for clinical decisions

## Dataset

- **Source**: Genomics of Drug Sensitivity in Cancer (GDSC) / CancerRxGene
- **Cancer Type**: Colorectal Adenocarcinoma (COREAD)
- **Features**: 66 binary mutation indicators (0=wild-type, 1=mutated)
- **Target**: IC50 values (log10 transformed)

## Methodology
# Machine-Learning-Based-Prediction-of-Drug-Sensitivity-Using-Genetic-Fingerprints
Multi-model machine learning pipeline for predicting cancer drug response (IC50) from genetic mutation fingerprints in colorectal cancer. Evaluates 12 algorithms and selects the best model per drug for personalized therapy recommendations.


## Installation

```bash
git clone https://github.com/Soudip123/Drug-Response-Prediction.git
cd Drug-Response-Prediction
pip install -r requirements.txt

## Requirments

pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
xgboost>=1.5.0
matplotlib>=3.4.0
seaborn>=0.11.0
