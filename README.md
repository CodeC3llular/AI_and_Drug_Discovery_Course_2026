# AI_and_Drug_Discovery_Course_2026
QSAR Data Curation for KRAS Target - Assignment 2

# AI and Drug Discovery Course 2026

## Assignment 2: QSAR Data Curation Using ChEMBL

**Student:** Michelle Mupanduki 
**Course:** AI and Biotechnology/Bioinformatics  
**Date:** January 2026

---

##  Assignment Overview

This repository contains the QSAR data curation workflow for Assignment 2 of the AI and Drug Discovery course. The objective is to retrieve, process, and curate bioactivity data from the ChEMBL database for subsequent QSAR modeling.

---

##  Selected Target

**Target Name:** GTPase KRas  
**ChEMBL ID:** CHEMBL2189121  
**Organism:** Homo sapiens  
**Target Type:** Single protein

---

##  Bioactivity Records

- **Initial records retrieved:** 5760 compounds
- **Final curated dataset:** 5730 compounds
- **Bioactivity measurement:** IC50 (nM)
- **Classification threshold:**
  - Active: IC50 ≤ 1000 nM - 2925 compounds
  - Intermediate: 1000 nM < IC50 < 10000 nM - 1851 compounds
  - Inactive: IC50 ≥ 10000 nM - 1224 compounds

---

##  Data Curation Workflow

### 1. **Target Selection**
- Search ChEMBL database for KRAS targets
- Select GTPase KRas (CHEMBL2189121) based on data availability

### 2. **Data Retrieval**
- Query ChEMBL web services for IC50 bioactivity data
- Retrieve compound structures (SMILES) and activity values

### 3. **Data Preprocessing**
- Remove records with missing bioactivity values
- Remove records with invalid or missing SMILES structures
- Filter for standardized units (nM only)
- Remove duplicate compounds

### 4. **Bioactivity Classification**
- Classify compounds into three categories based on IC50 values
- Create balanced dataset suitable for QSAR modeling

### 5. **Data Export**
- Save curated dataset in CSV format
- Store both raw and preprocessed data

---

##  Repository Structure

```
AI_and_Drug_Discovery_Course_2026/
│
├── assignment_2_QSAR_data_curation.ipynb   
├── README.md                                 
├── bioactivity_raw_data.csv                  
├── bioactivity_preprocessed_data.csv         
└── assignment_summary.pdf                    
```

---

##  Technologies Used

- **Python 3.x**
- **Libraries:**
  - chembl_webresource_client (ChEMBL API access)
  - pandas (data manipulation)
  - numpy (numerical operations)
- **Platform:** Google Colab

---

##  How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/[your-username]/AI_and_Drug_Discovery_Course_2026.git
   ```

2. Open the notebook in Google Colab

3. Mount your Google Drive and run all cells sequentially

4. The curated dataset will be saved in your Google Drive

---

##  Expected Outputs

- `bioactivity_raw_data.csv`: Raw bioactivity data from ChEMBL
- `bioactivity_preprocessed_data.csv`: Cleaned and classified dataset ready for QSAR modeling

---

##  Notes

- The number of bioactivity records may vary depending on ChEMBL database updates
- Data curation follows best practices for QSAR dataset preparation
- The curated dataset is suitable for subsequent molecular descriptor calculation and QSAR model development

---

##  Author

**Michelle Mupanduki**  
M.S. Biotechnology  
Northeastern University

---

##  References

- ChEMBL Database: https://www.ebi.ac.uk/chembl/
- Course Repository: https://github.com/AI-Biotechnology-Bioinformatics/Drug_Discovery_AI_Course_2026

---

## Contact

For questions or clarifications, please contact through the course platform.

---

*Last Updated: January 2026*
