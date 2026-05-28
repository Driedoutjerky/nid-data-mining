# UNSW-NB15 Network Intrusion Detection Project

## Project Overview

This project applies data mining methods to the UNSW-NB15 network intrusion detection dataset.

The main task is **multiclass classification**: predicting the traffic class of each network record.

Target variable:

```text
attack_cat
```

### Classes
```bash
Normal
Generic
Exploits
Fuzzers
DoS
Reconnaissance
Analysis
Backdoors
Shellcode
Worms
```
---
## Note
- **DO NOT** commit raw dataset files.
- **DO NOT** commit processed dataset files.
- Each member should download the raw dataset locally and run the preprocessing notebook(01, and 02) to generate their own local processed files.

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
│   ├── raw/          # original dataset files, not committed
│   ├── processed/    # generated train/test files, not committed
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
1. Clone the repo
```bash
git clone <repo-url>
cd nid-data-mining
```
3. Download/place the original dataset files in `/data/raw`
```bash
UNSW-NB15_1.csv
UNSW-NB15_2.csv
UNSW-NB15_3.csv
UNSW-NB15_4.csv
NUSW-NB15_features.csv
```
3. Create or activate your Python environment, set directory to the repo folder, then install dependencies. (From Anaconda Prompt or any you prefer)
```bash
pip install -r requirements.txt
```
4. Before starting work, update your local repo
```bash
git pull origin main
```
5. Create a new branch
```bash
git checkout -b your-branch-name
```
6. Run Jupyter Notebook from the project folder or from the `notebooks/` folder. 
```bash
cd ..\YOUR-DIRECTORY\nid-data-mining\notebooks
jupyter notebook
```
7. Run notebooks in order:
```bash
01_data_understanding.ipynb
02_baseline_preprocessing.ipynb  --> This generates local processed data in data/processed/
```
8. After making changes:
- **DO NOT** commit raw dataset files.
- **DO NOT** commit processed dataset files.
```bash
git add FILE-NAME
git commit -m "Add class distribution analysis"
git push origin your-branch-name
```
