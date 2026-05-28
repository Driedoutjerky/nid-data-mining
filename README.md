# UNSW-NB15 Network Intrusion Detection Project

## Project Overview

This project applies data mining methods to the UNSW-NB15 network intrusion detection dataset.  
The main task is binary classification: predicting whether a network traffic record is normal or malicious.

Target variable:

- `label = 0`: Normal traffic
- `label = 1`: Attack traffic

The project also uses `attack_cat` for class distribution analysis, but `attack_cat` is not used as an input feature for binary classification because it would cause data leakage.

---
## Note
- **DO NOT** commit raw dataset files.

## Dataset

Dataset: UNSW-NB15  
Required files: in `/data/raw`

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
│   ├── raw/          # original dataset files, not committed, should have the required files of dataset.
│   ├── processed/    # generated train/test files, not committed, 
│   └── outputs/      # small result tables
├── notebooks/        # Jupyter notebooks for analysis
├── reports/          # figures and report materials
├── README.md
├── requirements.txt
└── .gitignore
```

## Setup
1. Clone the repo]
2. Download/place the original dataset files in `/data/raw`
```bash
UNSW-NB15_1.csv
UNSW-NB15_2.csv
UNSW-NB15_3.csv
UNSW-NB15_4.csv
NUSW-NB15_features.csv
```
4. Create or activate your Python environment, set directory to the repo folder, then install dependencies.
```bash
pip install -r requirements.txt
```
3. Before starting work,
```bash
git pull origin main
```
3. Create a new branch
```bash
git checkout -b your-branch-name
```
4. Run Jupyter Notebook from the project folder or from the `notebooks/` folder. 
```bash
cd C:\Projects\nid-data-mining\notebooks
jupyter notebook
```
5. Run notebooks in order:
```bash
01_data_understanding.ipynb
02_baseline_preprocessing.ipynb  --> This generates local processed data in data/processed/
```
7. After making changes:
```bash
git add .
git commit -m "Add class distribution analysis"
git push origin your-branch-name
```
