# The Corporate Sales Record Cleaner | GetIntern Week 1

### 8-Week Data Science & ML Track - Phase 1: Data Cleaning & EDA

**Batch:** October 09, 2026

### Project Overview
Automated Data Sanitization Pipeline to clean raw corporate sales records. Every successful data science project begins with clean data - this project builds foundational skills in data ingestion, noise removal, and missing value handling using Pandas & NumPy.

### Dataset
- `raw_sales.csv` - Raw, uncleaned sales data with duplicates, missing values, and inconsistent text formatting
- `cleaned_sales.csv` - Final sanitized dataset after cleaning

### Cleaning Steps Performed

**1. Ingestion & Duplicate Removal**
- Loaded dataset using `pd.read_csv()`
- Audited for repeated records using `df.duplicated().sum()`
- Removed redundant rows using `df.drop_duplicates()`

**2. Missing Value Imputation**
- Inspected null vectors using `df.isnull().sum()`
- **Numerical Columns (Quantity, Price):** Imputed with `median` - median is robust to outliers compared to mean
- **Categorical Columns (City, Product, Payment Method, Customer Name):** Imputed with `mode` - most frequent value

**3. Text Standardization & Export**
- Standardized inconsistent strings using `.str.strip()` to remove extra whitespace
- Applied uniform lowercasing using `.str.lower()` for consistency
- Generated baseline summary statistics using `df.describe()`
- Exported final dataset as `cleaned_sales.csv`

### Before vs After Comparison

| Metric | Before Cleaning | After Cleaning |
|--------|----------------|----------------|
| Shape | (10, 7) | (9, 7) |
| Duplicate Rows | 1 | 0 |
| Missing Values | 6 | 0 |

### Tools Used
- Python
- Pandas, NumPy
- Google Colab

### How to Run
1. Open `Week1_Data_Cleaning_GetIntern.ipynb` in Google Colab
2. Runtime -> Run All
3. Check output files `raw_sales.csv` & `cleaned_sales.csv` in Files panel

### Author
M Narendra - Data Science Intern @ GetIntern.in