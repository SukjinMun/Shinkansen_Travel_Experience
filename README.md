# Shinkansen Travel Experience Hackathon
![Screenshot 2024-12-31 051437](https://github.com/user-attachments/assets/9246a5e8-1d36-4c44-b87b-a759b25836f3)
## Table of Contents
- [1.0 About](#10-about)
- [2.0 Project Workflow Summary](#20-project-workflow-summary)
- [3.0 Pipeline Overview](#30-pipeline-overview)
- [4.0 Key Features](#40-key-features)
- [5.0 Known Issues & Future Updates](#50-known-issues--future-updates)
- [6.0 License](#60-license)
- [7.0 Credits](#70-credits)

---

## 1.0 About
The goal of this Hackathon was to predict whether a passenger was satisfied or not, based on their **overall traveling experience** on the Shinkansen Bullet Train. The competition ran from **Aug 25, 2024, 7:00 PM – Aug 29, 2024, 7:00 PM**, with an allowed team size of 1–3 members.

**Key Achievement:**  
- Developed a **machine learning pipeline** to predict passenger satisfaction, **achieving 93.4% accuracy** and securing **24th place out of 76 teams**.  
- Optimized performance using **feature engineering**, **hyperparameter tuning**, and **ensemble models** (Random Forest, CatBoost, Neural Networks).

---

## 2.0 Project Workflow Summary
1. **Data Loading & Preprocessing**  
   - Combined survey and travel data into unified DataFrames.  
   - Handled missing values via KNN imputation.  
   - Encoded categorical features (Label Encoding) and scaled numerical features (StandardScaler).

2. **Feature Engineering**  
   - Created custom features like `Total_Delay` (departure + arrival delay) and `Overall_Rating` (aggregated from multiple survey columns).  
   - Performed correlation checks and selected top features using Chi-Square, RFE, and Permutation Importance.

3. **Model Training & Evaluation**  
   - Evaluated multiple algorithms: **Logistic Regression, Random Forest, CatBoost, Neural Network, AdaBoost, XGBoost**.  
   - Used **GridSearchCV** and **Optuna** for hyperparameter tuning.  
   - Addressed potential class imbalance with **SMOTE** where needed.

4. **Ensemble & Final Submission**  
   - Implemented **StackingClassifier** with CatBoost, XGBoost, and AdaBoost as base models, plus a Logistic Regression meta-learner.  
   - Generated final CSV submissions and ranked **24th** in the competition.

---

## 3.0 Pipeline Overview
1. **Data Cleaning**: Label encoding, missing-value imputation, outlier checks.  
2. **Feature Engineering**: Creating new features, removing highly correlated or low-importance attributes.  
3. **Model Selection & Tuning**: Baseline models, advanced tuning (GridSearch, Optuna).  
4. **Ensemble**: Combined top performers for improved predictions (Stacking).  
5. **Submission**: Produced final prediction CSV files for hackathon leaderboard.

---

## 4.0 Key Features
- **Extensive EDA**: Pairplots, heatmaps, boxplots for data insights.  
- **Robust Feature Selection**: Chi-Square, RFE, Permutation Importance.  
- **Ensemble Methods**: CatBoost, Random Forest, XGBoost, Neural Networks, plus stacking.  
- **Accurate & Efficient**: Achieved ~93.4% on test data.  
- **Well-Documented**: Clear steps for data cleaning, modeling, and result generation.

---

## 5.0 Known Issues & Future Updates
- **Potential Overfitting**: Large ensembles risk overfitting if not carefully tuned.  
- **Resource Constraints**: Hyperparameter tuning can be memory-intensive in Colab.  
- **Next Steps**: Investigate incremental learning approaches or Bayesian optimization for faster/broader search.

---

## 6.0 License
This project is released under the [MIT License](./LICENSE). You can freely use, modify, and distribute it, subject to the license terms.

---

## 7.0 Credits
- **Team Sublime_Jin** for data analysis, feature engineering, and modeling.  
- Hackathon organizers for dataset provision and competition framework.  
- **Libraries**: NumPy, Pandas, Scikit-learn, TensorFlow, CatBoost, XGBoost, Optuna, imbalanced-learn.

---
