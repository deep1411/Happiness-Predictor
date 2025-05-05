# Happiness Predictor

**Customer Unhappiness Analysis**

---

## 🏭 Background

This project was executed through **Apziva** for one of their logistics and delivery clients. As a rapidly scaling startup, they face a significant proportion of **unhappy customers** compared to happy ones. To improve customer experience, the goal was to uncover the key factors driving dissatisfaction so that targeted operational changes can be made at scale.

---

## 📊 Data Description

* **Y**: Target attribute indicating customer happiness (0 = unhappy, 1 = happy)
* **X1**: My order was delivered on time (1–5)
* **X2**: Contents of my order were as I expected (1–5)
* **X3**: I ordered everything I wanted to order (1–5)
* **X4**: I paid a good price for my order (1–5)
* **X5**: I am satisfied with my courier (1–5)
* **X6**: The app makes ordering easy for me (1–5)

Values range from 1 (strongly disagree) to 5 (strongly agree).

**Download the dataset:** [Google Drive link](https://drive.google.com/open?id=1KWE3J0uU_sFIJnZ74Id3FDBcejELI7FD)

---

## 🎯 Project Goals

1. **Identify Drivers of Unhappiness:** Pinpoint which service aspects most strongly correlate with unhappy customers.
2. **Predictive Modeling:** Build classifiers to distinguish between unhappy (0) and happy (1) customers.
3. **Feature Prioritization:** Recommend a minimal feature set for future surveys that captures core dissatisfaction drivers.

---

## ✅ Success Metrics

* **Accuracy ≥ 73%** on the validation set, or a compelling argument for alternative evaluation.
* **Clear insights** for operational teams to address primary dissatisfaction drivers.

---

## 🔧 Step-by-Step Workflow

1. **Clone the Repo**

   ```bash
   git clone https://github.com/deep1411/Happiness-Predictor.git
   cd Happiness-Predictor
   ```

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Open the Notebook**

   ```bash
   jupyter notebook Happiness_Predictor.ipynb
   ```

4. **Explore the Data**

   * Load and inspect for quality issues.
   * Visualize target imbalance (more unhappy than happy).
   * Plot feature distributions and a correlation matrix.

5. **Prepare for Modeling**

   * Split into features (X) and target (Y).
   * Train/validation split and feature scaling.

6. **Benchmark Models**

   * Use **LazyPredict** to quickly rank algorithms.
   * Select top performers for deeper analysis.

7. **Ensemble Techniques**

   * **Stacking Ensemble:** LGBM, XGBoost, RandomForest.
   * **Voting Ensemble:** Soft voting with LGBM, ExtraTrees, CatBoost.

8. **Feature Selection**

   * **SelectFromModel:** Prune by importance thresholds.
   * **RFE:** Choose the top 3 features.

9. **Hyperparameter Tuning**

   * Employ **Bayesian Optimization** to fine-tune LightGBM.

10. **Evaluate & Refine**

    * Compare accuracy against the 73% benchmark.
    * Finalize the minimal feature set.

---

## 📈 Key Insights & Recommendations

* **Unhappiness Drivers:**

  * **X1 (on-time delivery)**: Delays strongly correlate with unhappy customers.
  * **X5 (courier satisfaction)**: Poor courier experience is a major pain point.
  * **X6 (app usability)**: Difficulty using the app contributes significantly to complaints.

* **Minimal Survey Design:** Future surveys can focus on X1, X5, and X6—dropping less informative questions (like X2, X3, X4) to reduce respondent fatigue without sacrificing predictive power.

---

## 👤 About the Contributor

I executed this project with guidance from **Apziva** for their logistics client, delivering an end-to-end analytics solution—from exploratory data analysis to ensemble modeling, feature selection, and hyperparameter optimization. My work provided clear, actionable insights to reduce customer churn and improve service quality.

---

## 📬 Contact

For questions or collaboration inquiries, open an issue or reach me at **[d.bal@outlook.com](mailto:d.bal@outlook.com)**.
