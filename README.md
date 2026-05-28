# UNSW-NB15 Network Intrusion Detection Project

## Project Overview

This project applies data mining methods to the UNSW-NB15 network intrusion detection dataset.  
The main task is binary classification: predicting whether a network traffic record is normal or malicious.

Target variable:

- `label = 0`: Normal traffic
- `label = 1`: Attack traffic

The project also uses `attack_cat` for class distribution analysis, but `attack_cat` is not used as an input feature for binary classification because it would cause data leakage.

---

## Dataset

Dataset: UNSW-NB15  
Required files:

```text
UNSW-NB15_1.csv
UNSW-NB15_2.csv
UNSW-NB15_3.csv
UNSW-NB15_4.csv
NUSW-NB15_features.csv
```

## Folder Structure
```
nid-data-mining/
├── data/
│   ├── raw/          # original dataset files, not committed
│   ├── processed/    # generated train/test files, not committed
│   └── outputs/      # small result tables
├── notebooks/        # Jupyter notebooks for analysis
├── reports/          # figures and report materials
├── README.md
├── requirements.txt
└── .gitignore
```
