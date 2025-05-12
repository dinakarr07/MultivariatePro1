
# Insurance Data Analysis Project

## 📂 Files Included
- `project1.ipynb`: Main Jupyter Notebook with all data analysis and visualizations
- `insurance_updated.xlsx`: Input dataset containing insurance records
- `datasetinfo.pdf`: Documentation outlining variable descriptions and data structure
- `FinalReport.docx`: Documentation outlining Univariate, Bivariate and Multivariate Analysis
- `README.md`: Project description and structure (you are here)

## 📊 Project Description
This project performs a comprehensive statistical analysis on insurance data to explore relationships between numeric variables (`charges`, `BMI`, and `age`) and categorical variables (`smoker`, `region`). It involves transformation techniques, univariate, bivariate, and multivariate visualizations, and hypothesis testing using Hotelling’s T² test.

---

## 🧪 Analysis Breakdown

### 1. Univariate Analysis
- **Summary statistics** (mean, median, SD, IQR) were computed.
- Distributions were visualized using histograms and boxplots.
- **Box-Cox transformation** was applied to `charges` and `age` to approximate normality.
- Interpretation of center and spread metrics (mean/IQR) is provided per variable.

### 2. Univariate Analysis by Groups
- Boxplots and summaries grouped by:
  - `smoker` (Yes/No)
  - `region` (Southeast, Southwest, Others)
- Observations:
  - Smokers incur significantly higher charges.
  - BMI levels vary slightly by region.
  - Age distribution is uniform across groups.

### 3. Bivariate Analysis
- Pairwise scatterplot matrices were generated:
  - Colored by `smoker`
  - Colored by `region`
  - Colored by interaction of both
- Key Findings:
  - Charges increase with age.
  - Weak relationship between BMI and charges.
  - Smoker status strongly impacts charges, more than region.

### 4. Multivariate Analysis
- 3D scatter plots using `scatterplot3d`:
  - Axes: `charges`, `BMI`, `age`
  - Colored by `smoker`, `region`, and their interaction
- Visualized how multiple variables interact in relation to insurance costs.

### 5. Statistical Testing
- Conducted **Hotelling's T² test** to compare the sample mean vector with known values from the literature:
  - Literature mean vector (transformed): [10.73, 28.5, 27.75]
  - Sample mean vector: [10.85, 30.66, 39.21]
- Result:
  - T² = 57.357, p-value = 2.2e-16 → **Reject null hypothesis**
  - Indicates significant difference between sample and population means

---

## 📌 Dependencies
Make sure the following R packages are installed:

```r
install.packages(c("openxlsx", "dplyr", "ggplot2", "psych", "MVN", "scatterplot3d", "ellipse", "DescTools", "EnvStats", "heplots"))
```

---

## 📝 Conclusion
This project highlights how smoking status and age are major contributors to insurance charges. Region has a lesser impact. Data transformation improved normality for statistical testing. Multivariate plots and statistical tests confirmed significant differences from reference values.

---

## 📅 Author
Dinakar reddy Donthireddy
