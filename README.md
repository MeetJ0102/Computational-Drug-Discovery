# Computational-Drug-Discovery

This project is part of a series focused on Computational Drug Discovery (CDD). We prepare bioactivity data for machine learning model development, specifically targeting the SARS coronavirus 3C-like proteinase. The notebook demonstrates how to retrieve, clean, and preprocess bioactivity data from the ChEMBL database.

**Project Overview**
The primary goal of this project is to collect bioactivity data related to the SARS coronavirus 3C-like proteinase from the ChEMBL database and prepare it for machine learning applications. This involves:

- Installing necessary libraries.
- Retrieving and filtering bioactivity data.
- Handling missing values.
- Preprocessing data by labeling compounds based on their activity levels.
  
**Key Steps**

1. Installing and Importing Libraries
ChEMBL Web Service: This Python package is used to access the ChEMBL database and retrieve bioactivity data.
Other Libraries: Additional libraries like pandas are used for data handling and manipulation.
2. Target Protein Search
Objective: Identify and select the SARS coronavirus 3C-like proteinase as the target protein for the study.
Process: The target protein is searched within the ChEMBL database, and the relevant bioactivity data is retrieved, specifically focusing on data reported as IC$_{50}$ values in nanomolar (nM) units.
3. Data Retrieval and Saving
Bioactivity Data: The retrieved data is filtered to include only relevant entries and then saved as a CSV file (bioactivity_data.csv).
Google Drive Integration: The notebook demonstrates how to save and access files using Google Drive, making it easy to store and retrieve data in future sessions.
4. Handling Missing Data
Missing Values: The notebook checks for missing values in the standard_value column and drops any entries with missing data, ensuring a clean dataset for analysis.
5. Data Preprocessing
Labeling Compounds: Compounds are labeled as "active," "inactive," or "intermediate" based on their IC$_{50}$ values:

Active: IC$_{50}$ < 1000 nM
Inactive: IC$_{50}$ > 10,000 nM
Intermediate: 1000 nM ≤ IC$_{50}$ ≤ 10,000 nM
Data Iteration: The notebook iterates through key fields like molecule_chembl_id and canonical_smiles to prepare the data for further analysis.

**How to Use**

**Prerequisites**
- Python 3.x
- Jupyter Notebook or Jupyter Lab
- Libraries: pandas, ChEMBL web service, and others as specified in the notebook.
