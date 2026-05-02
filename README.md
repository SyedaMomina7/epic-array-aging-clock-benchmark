# 🧬 EPIC Array Aging Clock Analysis (Bio-Learn)

## 📌 Overview

This project presents a comprehensive comparative analysis of multiple **DNA methylation–based aging clocks** using EPIC array data, inspired by the Bio-Learn study.

Biological aging is a complex, multi-dimensional process that cannot be captured by a single biomarker. To address this, we evaluate and benchmark multiple aging clock models across independent datasets, focusing on:

* Inter-model relationships
* Predictive accuracy
* Biological age deviations

This repository demonstrates how different aging clocks behave across datasets and highlights their strengths, limitations, and agreement patterns.

---

## 🎯 Objectives

The primary goals of this project are:

* To analyze multiple biomarkers of aging derived from DNA methylation data
* To implement and compare **at least 8 established aging clock models**
* To evaluate model performance across **two independent EPIC array datasets**
* To generate interpretable visualizations for:

  * Correlation between aging clocks
  * Deviations from chronological age (ΔAge)
  * Model prediction accuracy

---

## 📁 Datasets Used

Two independent datasets were selected from the Bio-Learn study to ensure robustness and generalizability of findings.

### 🔹 Dataset A

* **Description:** DNA methylation dataset derived from EPIC array platform
* **Data Type:** CpG methylation beta values
* **Technology:** Illumina EPIC Array
* **Sample Size:** *[Insert actual number]*
* **Age Range:** *[Insert range]*
* **Purpose:** Primary evaluation dataset for model comparison

---

### 🔹 Dataset B

* **Description:** Independent EPIC array dataset used for validation
* **Data Type:** CpG methylation beta values
* **Technology:** Illumina EPIC Array
* **Sample Size:** *[Insert actual number]*
* **Age Range:** *[Insert range]*
* **Purpose:** Cross-dataset validation of aging clock performance

---

## 🧠 Aging Clock Models Implemented

The following aging clocks were implemented and evaluated:

| Model               | Description                                |
| ------------------- | ------------------------------------------ |
| **Horvath Clock**   | Multi-tissue predictor using 353 CpG sites |
| **Hannum Clock**    | Blood-based methylation age predictor      |
| **PhenoAge**        | Incorporates phenotypic aging markers      |
| **GrimAge**         | Predicts lifespan and mortality risk       |
| **SkinBlood Clock** | Optimized for skin and blood tissues       |
| **PedBE Clock**     | Pediatric epigenetic clock                 |
| **DunedinPoAm**     | Measures pace of aging rather than age     |
| **DNAmTL**          | Estimates telomere length from methylation |

These models capture different biological aspects of aging, making their comparison particularly informative.

---

## ⚙️ Methodology

### 1. Data Preprocessing

* Normalization of DNA methylation beta values
* Quality control and filtering of CpG sites
* Alignment of features required for each aging clock

### 2. Model Application

* Each aging clock model was applied to both datasets
* Predicted biological age was computed for every sample

### 3. Age Deviation Calculation

* Biological age deviation was computed as:

[
\Delta Age = Predicted\ Age - Chronological\ Age
]

* This metric reflects accelerated or decelerated aging

### 4. Comparative Analysis

* Cross-model correlations
* Prediction accuracy assessment
* Visualization of deviation patterns

---

## 📈 Visualizations

### 🔹 1. Correlation Matrix

These matrices illustrate the relationships between different aging clocks, helping identify clusters of similar models and redundancy.

#### Dataset A

<img width="418" height="350" alt="clock_corelation_dataset1" src="https://github.com/user-attachments/assets/e8397d17-e021-4772-a1d4-f07e67218592" />

#### Dataset B

<img width="412" height="341" alt="clock_corelation_dataset2" src="https://github.com/user-attachments/assets/4fdbee90-e0d6-48ca-876a-d2d2254739e1" />

---

### 🔹 2. Age Deviation Heatmap

These heatmaps visualize how each model deviates from chronological age across samples.

* Red → Age acceleration
* Blue → Age deceleration

#### Dataset A

<img width="795" height="243" alt="age_deviation heatmap1" src="https://github.com/user-attachments/assets/6fe0a5c1-039f-4129-bf53-383d8069858b" />

#### Dataset B

<img width="746" height="242" alt="age_deviation heatmap2" src="https://github.com/user-attachments/assets/f011ce65-7412-4acc-88c2-955db2a77902" />

---

### 🔹 3. Predictions vs Chronological Age

These plots compare predicted biological age with actual chronological age.

* The diagonal line represents perfect prediction
* Spread indicates model error and variability

#### Dataset A

<img width="712" height="293" alt="clockpre_vs_chronologicalage1" src="https://github.com/user-attachments/assets/90eb4b29-34a5-48b5-bd9f-1c9dfa70cda8" />

#### Dataset B

<img width="700" height="292" alt="clockpre_vs_chronologicalage2" src="https://github.com/user-attachments/assets/032f4b9b-41f6-4698-b60a-3443d9b4b031" />

---

## 📊 Key Insights

* Certain clocks (e.g., Horvath, Hannum) show strong correlation, indicating shared biological signals
* Some models capture unique aging dimensions (e.g., GrimAge, DunedinPoAm)
* Variability across datasets highlights the importance of cross-cohort validation
* Age deviation patterns reveal heterogeneity in biological aging across individuals

---

## 📦 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

### Core Libraries

* pandas
* numpy
* seaborn
* matplotlib
* scikit-learn

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/biolearn-aging-clocks-analysis.git
cd biolearn-aging-clocks-analysis
```

2. Open the notebook:

```
notebooks/biological_clocks.ipynb
```

3. Run all cells to:

* Process datasets
* Apply models
* Generate visualizations

4. Output images will be saved in:

```
/images/
```

---

## 📚 Reference

Bio-Learn Study:
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0118453

---

## 👩‍💻 Author

**Syeda Momina**

---

## 📌 Notes

* Results depend on preprocessing and normalization steps
* Not all clocks are universally applicable across tissues
* Some models require specific CpG coverage
* This project is intended for research and educational purposes

---

## ⭐ Future Work

* Add more datasets for broader validation
* Include statistical performance metrics (RMSE, MAE, R²)
* Explore machine learning-based aging predictors
* Perform feature importance analysis

---
---


