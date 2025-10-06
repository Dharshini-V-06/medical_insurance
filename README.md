# **Medical Insurance**

## **Project Overview**

The goal of this project is to explore and preprocess the **insurance dataset** to understand factors affecting medical insurance charges. Using exploratory data analysis (EDA) and data preprocessing, the dataset is prepared for predictive modeling to estimate insurance charges based on demographic, lifestyle, and health-related features.

---
Dataset Link: [Medical insurance](https://www.kaggle.com/datasets/thedevastator/prediction-of-insurance-charges-using-age-gender)
## **Dataset Columns**

| Column   | Description                                                   |
| -------- | ------------------------------------------------------------- |
| age      | Age of the policyholder                                       |
| sex      | Gender of the policyholder (male/female)                      |
| bmi      | Body Mass Index, indicates body fat                           |
| children | Number of children covered by insurance                       |
| smoker   | Smoking status (yes/no)                                       |
| region   | Residential area (northeast, northwest, southeast, southwest) |
| charges  | Medical insurance charges (target variable)                   |

---

## **Analysis & Processing Steps**

1. **Data Understanding**

   * Checked dataset structure, missing values, duplicates, and summary statistics using `df.info()`, `df.shape`, `df.isnull().sum()`, `df.duplicated().sum()`, and `df.describe()`.

2. **Exploratory Data Analysis (EDA)**

   * Visualized distributions of numeric features (`age`) using histograms.
   * Created scatterplots for `age vs charges` and `bmi vs charges`, colored by `smoker`.
   * Displayed top 3 records for highest `charges` and highest `bmi`.
   * Visualized the distribution of `region` using a pie chart.
   * Calculated correlation between `bmi` and `charges`.

3. **Categorical Encoding**

   * Used **Label Encoding** for `sex`, `smoker`, and `region` to convert text into numeric form.
   * One-hot encoding was explored but not applied in the final dataset.

4. **Outlier Detection & Handling**

   * Created boxplots for numeric columns (`age`, `bmi`, `children`, `charges`) to visualize outliers.
   * Detected outliers using the **IQR method**.
   * Capped outliers in the `charges` column to limit extreme values while keeping all rows.

---

## **Tech Stack**

* **Python Libraries:**

  * `pandas` – data handling
  * `matplotlib`, `seaborn` – visualization
  * `scikit-learn` – encoding

---

## **Conclusion**

* Higher **BMI** and **smoker status** have a positive correlation with insurance charges.
* Age shows some influence on charges.
* Regions have a minor impact on charges.
* Outlier capping ensures extreme `charges` values do not skew analysis.
* The dataset is now ready for predictive modeling for insurance charges.

---
