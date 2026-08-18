> ⏳ **CODE EMBARGO NOTICE**
> This project is currently under peer review for publication as an original scientific article. To comply with journal embargo policies and prevent scooping, the source code and methodology are temporarily withheld. The complete repository will be made fully public immediately upon the article's official publication.

# HPV Viral Persistence Prediction: Data Preprocessing Pipeline 🧬💻

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📌 About The Project
This repository contains the comprehensive data cleaning, imputation, and preprocessing pipeline designed to prepare clinical and genomic data for Machine Learning models. The ultimate goal of the broader research is to predict the viral persistence of the Human Papillomavirus (HPV) after one year of follow-up.

### 🏛️ Institutional Acknowledgment
This project was developed at the **National Institute of Public Health of Mexico (Instituto Nacional de Salud Pública - INSP)**, specifically within the **Center for Research in Infectious Diseases (Centro de Investigación en Enfermedades Infecciosas - CISEI)**. 

## ⚠️ Data Privacy & Confidentiality Notice
The dataset used in this project contains highly sensitive and confidential medical, genomic, and sociodemographic information from real patients. 

To strictly adhere to privacy regulations, ethical guidelines, and patient confidentiality, **no raw or processed data files (`.csv`) are included in this repository**. This repository is intended solely to showcase the code, logic, and methodological pipeline used for data preparation.

## ⚙️ Methodology & Pipeline
The Python script (`limpieza_de_datos.py` / Jupyter Notebook) covers the following critical steps:

1. **Feature Engineering & Standardization:** 
   * Renaming variables to a standardized English format for better readability.
   * Cleaning and categorizing unstructured text data (e.g., standardizing municipality names into numerical categories).
2. **Outlier Detection & Handling:** 
   * Visualization of standardized distributions (Z-scores) using Seaborn violin plots.
   * Automated, iterative removal of implausible extreme values (outliers with Z > 3) specifically for cytokine mRNA expression levels.
3. **Advanced Missing Value Imputation:**
   * Dropping variables with > 50% missing data.
   * Implementing Multiple Imputation by Chained Equations (MICE) using `IterativeImputer` backed by a `RandomForestRegressor` to rigorously handle missing data.
   * Post-processing to restore categorical integers.
4. **Data Formatting for Machine Learning:**
   * Mapping categorical variables (sociodemographic, clinical, and genetic models: Codominant, Dominant, Recessive) to descriptive strings.
   * Applying One-Hot Encoding to prepare all features for classification algorithms.
   * Removing zero-variance features to optimize model performance.

## 🛠️ Built With
* [Pandas](https://pandas.pydata.org/) - Data manipulation and analysis.
* [Scikit-Learn](https://scikit-learn.org/) - Iterative Imputation and Data Scaling.
* [Seaborn](https://seaborn.pydata.org/) & [Matplotlib](https://matplotlib.org/) - Data visualization and outlier analysis.
* [SciPy](https://scipy.org/) - Statistical operations (Z-scores).

## 💡 How to use this repository
Since the data is private, you cannot run this code "out-of-the-box" without the original `.csv` files. However, this codebase serves as a robust template for:
* Handling complex clinical datasets.
* Automating outlier removal.
* Rigorous imputation of missing values in healthcare data.
