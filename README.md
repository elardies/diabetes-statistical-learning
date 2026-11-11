# Diabetes Risk Analysis — Statistical Learning in R

An academic statistical learning project examining relationships between clinical measurements and diabetes outcomes using **R**. The study combines data preprocessing, supervised modeling, dimensionality reduction, and unsupervised clustering to explore diabetes-related risk patterns.

**Authors:** Elena Lardies and Daniela Bialy  
**Project type:** University coursework. Bachelor in Data Science and Engineering. Universidad Carlos III de Madrid.

## Dataset

The project analyzes `diabetes.csv`, with **768 observations** and **9 original variables**, including pregnancies, glucose, blood pressure, skin thickness, insulin, BMI, diabetes pedigree function, age, and the binary diabetes outcome.

## Methods

- Exploratory data analysis, visualizations, correlations, and outlier inspection
- Treatment of clinically implausible zero values as missing observations, with KNN-based imputation for selected variables
- Feature engineering of a `HighRisk` indicator based on glucose and BMI
- Logistic regression and resampling-based model assessment
- Principal component analysis (PCA) and factor analysis
- Clustering with k-means, partitioning around medoids (PAM), hierarchical clustering, expectation-maximization (EM), and kernel k-means

## Selected findings

- **Glucose** was the strongest individual predictor among the logistic regression models examined, with a reported ROC AUC of approximately **0.77–0.80**.
- PCA and factor analysis were used to explore variation and latent structure in the clinical measurements.
- Clustering revealed potential patient subgroups, although some partitions showed substantial overlap. For example, the report notes a low average silhouette width of approximately **0.18** for the initial four-cluster k-means solution.

These findings are exploratory and should not be interpreted as clinical conclusions.

## Files

- `project 1- diabetes.Rmd` — R Markdown analysis notebook
- `diabetes.csv` — dataset
- `PROJECT 1-REPORT.pdf` — coursework report

## Running the analysis

1. Install **R**, **RStudio**, and the required R packages referenced in the notebook.
2. Put the `.Rmd` file and `diabetes.csv` in the same folder.
3. Open the `.Rmd` in RStudio and update or remove the original author's hard-coded `setwd(...)` path so that it points to your local project folder.
4. Run the notebook chunks to explore the analysis. To **Knit** the HTML report, note that the notebook references `my-theme.css`; either provide that stylesheet or remove the `css: my-theme.css` line from the YAML header.

## Scope and limitations

This is a university exploratory analysis, not a clinically validated diagnostic system. Some preprocessing and model evaluation choices may need revision for a leakage-free predictive benchmark. The repository documents the original coursework and its reported results.
