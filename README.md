# datagouv_project
# 🏥 Patient Master Data Governance

### Data Quality · Record Linkage · Entity Resolution · Golden Record

A data governance project focused on identifying duplicate patient records, improving data quality, and building a unified and reliable patient reference across multiple information systems.

---

## 📌 Project Overview

Healthcare organizations often store patient information in several independent systems, such as hospital admission applications, electronic patient records, and billing systems.

The same patient may appear multiple times with different identifiers, spelling variations, missing information, or inconsistent data.

These inconsistencies make it difficult to maintain a reliable view of each patient.

**The goal of this project is to design a data governance workflow that identifies potential duplicates, evaluates data quality, reconciles records, and builds a unified patient reference called a Golden Record.**

> The project uses synthetic data for educational and demonstration purposes.

## 🎯 Objectives

- Analyze the quality and structure of data from multiple sources.
- Identify missing values, duplicates, and inconsistencies.
- Define and apply data quality indicators.
- Standardize fields to improve record comparability.
- Match records that may refer to the same patient.
- Identify and review ambiguous matches.
- Build a Golden Record for each reconciled patient.
- Maintain traceability between source records and consolidated records.
- Evaluate the matching process using known reference labels in the synthetic dataset.

## 🗂️ Data Sources

The project uses three simulated information systems.

| Source | Description | Purpose |
|---|---|---|
| `adm` | Hospital admissions | Patient information associated with hospital stays |
| `dp_pat` | Electronic patient records | Patient identity and administrative information |
| `fac` | Billing system | Patient information associated with billing records |

These sources may contain overlapping information, missing values, formatting differences, and duplicate records.

## 🔍 Project Workflow

### 1. Data Profiling

Analyze each source to understand its structure and identify quality issues.

- Number of records and attributes
- Missing values
- Duplicate records
- Data types and distributions
- Potential anomalies

### 2. Data Quality Assessment

Evaluate data quality using indicators such as:

- **Completeness:** proportion of required values that are populated.
- **Uniqueness:** identification of duplicate records.
- **Consistency:** detection of conflicting values across systems.
- **Validity:** verification of formats and business rules.
- **Accuracy:** assessed where reliable reference data is available.

### 3. Data Standardization

Prepare the data for comparison by normalizing selected fields, such as names and administrative attributes.

Standardization helps reduce superficial differences without assuming that similar records necessarily belong to the same person.

### 4. Record Linkage & Entity Resolution

Compare records from different sources to identify potential matches.

The workflow distinguishes between:

- High-confidence matches
- Potential matches requiring review
- Records that should remain separate

### 5. Golden Record Construction

Consolidate reconciled records into a unified patient reference.

The Golden Record aims to provide a consistent view of each patient while preserving links to the original source records.

### 6. Traceability & Data Stewardship

Preserve the relationship between source records and consolidated entities.

Ambiguous or incorrect matches should be reviewable and correctable by a designated data steward.

### 7. Evaluation

Use reference labels available in the synthetic dataset to evaluate matching performance.

Possible evaluation metrics include:

- Precision
- Recall
- F1-score
- False positive rate

Reference labels are used for evaluation and simulated correction, not as inputs to the matching algorithm.

## 🛠️ Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Data profiling and visualization tools
- Git and GitHub

Additional libraries and methods are documented as the project evolves.

## 📁 Repository Structure

```text
patient-master-data-governance/
│
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── data_governance.ipynb
├── reports/
│   └── .gitkeep
└── src/
    └── data_quality.py
```

The structure may evolve as the project develops.

## 📊 Results

The notebook documents the results of the data profiling, quality assessment, record matching, and Golden Record construction stages.

Key indicators to report include:

- Number of records processed per source
- Missing-value rate
- Number of candidate matches
- Number of confirmed matches
- Number of records requiring manual review
- Matching precision, recall, and F1-score
- Number of Golden Records created

*Quantitative results will be added after the experiments have been completed and validated.*

## 🔐 Data Privacy

This project is intended for educational purposes and should use synthetic data only.

No real patient records, personal identifiers, medical information, passwords, or API keys should be published in this repository.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Ramadiaw12/datagouv_project.git
cd patient-master-data-governance
```

### 2. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook located in the `notebooks/` directory.

## 🎓 Project Context

Academic project in Data Governance, focused on data quality, master data management, record linkage, and the construction of a unified patient reference.

**Status:** In progress.

## 👩‍💻 Author

**RD**

Data Governance · Data Engineering · Artificial Intelligence# 🏥 Patient Master Data Governance

### Data Quality · Record Linkage · Entity Resolution · Golden Record

A data governance project focused on identifying duplicate patient records, improving data quality, and building a unified and reliable patient reference across multiple information systems.

---

## 📌 Project Overview

Healthcare organizations often store patient information in several independent systems, such as hospital admission applications, electronic patient records, and billing systems.

The same patient may appear multiple times with different identifiers, spelling variations, missing information, or inconsistent data.

These inconsistencies make it difficult to maintain a reliable view of each patient.

**The goal of this project is to design a data governance workflow that identifies potential duplicates, evaluates data quality, reconciles records, and builds a unified patient reference called a Golden Record.**

> The project uses synthetic data for educational and demonstration purposes.

## 🎯 Objectives

- Analyze the quality and structure of data from multiple sources.
- Identify missing values, duplicates, and inconsistencies.
- Define and apply data quality indicators.
- Standardize fields to improve record comparability.
- Match records that may refer to the same patient.
- Identify and review ambiguous matches.
- Build a Golden Record for each reconciled patient.
- Maintain traceability between source records and consolidated records.
- Evaluate the matching process using known reference labels in the synthetic dataset.

## 🗂️ Data Sources

The project uses three simulated information systems.

| Source | Description | Purpose |
|---|---|---|
| `adm` | Hospital admissions | Patient information associated with hospital stays |
| `dp_pat` | Electronic patient records | Patient identity and administrative information |
| `fac` | Billing system | Patient information associated with billing records |

These sources may contain overlapping information, missing values, formatting differences, and duplicate records.

## 🔍 Project Workflow

### 1. Data Profiling

Analyze each source to understand its structure and identify quality issues.

- Number of records and attributes
- Missing values
- Duplicate records
- Data types and distributions
- Potential anomalies

### 2. Data Quality Assessment

Evaluate data quality using indicators such as:

- **Completeness:** proportion of required values that are populated.
- **Uniqueness:** identification of duplicate records.
- **Consistency:** detection of conflicting values across systems.
- **Validity:** verification of formats and business rules.
- **Accuracy:** assessed where reliable reference data is available.

### 3. Data Standardization

Prepare the data for comparison by normalizing selected fields, such as names and administrative attributes.

Standardization helps reduce superficial differences without assuming that similar records necessarily belong to the same person.

### 4. Record Linkage & Entity Resolution

Compare records from different sources to identify potential matches.

The workflow distinguishes between:

- High-confidence matches
- Potential matches requiring review
- Records that should remain separate

### 5. Golden Record Construction

Consolidate reconciled records into a unified patient reference.

The Golden Record aims to provide a consistent view of each patient while preserving links to the original source records.

### 6. Traceability & Data Stewardship

Preserve the relationship between source records and consolidated entities.

Ambiguous or incorrect matches should be reviewable and correctable by a designated data steward.

### 7. Evaluation

Use reference labels available in the synthetic dataset to evaluate matching performance.

Possible evaluation metrics include:

- Precision
- Recall
- F1-score
- False positive rate

Reference labels are used for evaluation and simulated correction, not as inputs to the matching algorithm.

## 🛠️ Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Data profiling and visualization tools
- Git and GitHub

Additional libraries and methods are documented as the project evolves.

## 📁 Repository Structure

```text
patient-master-data-governance/
│
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── data_governance.ipynb
├── reports/
│   └── .gitkeep
└── src/
    └── data_quality.py
```

The structure may evolve as the project develops.

## 📊 Results

The notebook documents the results of the data profiling, quality assessment, record matching, and Golden Record construction stages.

Key indicators to report include:

- Number of records processed per source
- Missing-value rate
- Number of candidate matches
- Number of confirmed matches
- Number of records requiring manual review
- Matching precision, recall, and F1-score
- Number of Golden Records created

*Quantitative results will be added after the experiments have been completed and validated.*

## 🔐 Data Privacy

This project is intended for educational purposes and should use synthetic data only.

No real patient records, personal identifiers, medical information, passwords, or API keys should be published in this repository.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Ramadiaw12/datagouv_project.git
cd patient-master-data-governance
```

### 2. Create a virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook located in the `notebooks/` directory.

## 🎓 Project Context

Academic project in Data Governance, focused on data quality, master data management, record linkage, and the construction of a unified patient reference.

**Status:** In progress.

## 👩‍💻 Author

**RD**

Data Governance · Data Engineering · Artificial Intelligence