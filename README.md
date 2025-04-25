# Home-Credit-Default-Risk-Project
Home Credit aims to make credit accessible to more individuals by providing loans to people with limited credit history. However, this mission introduces significant risk. The company needs an effective and scalable way to assess the likelihood that an applicant will default on a loan.

Objective:
Our project seeks to build a predictive model to assess the probability of a client repaying a loan, enabling Home Credit to make more informed, risk-balanced lending decisions.
We built and compared multiple models to address the class imbalance and predictive challenge in the Home Credit dataset, including:

Baseline Model: A majority class classifier, which predicted all loans as repaid (91% accuracy due to class imbalance).

Logistic Regression: Implemented with and without interaction terms (e.g., INCOME_CREDIT_RATIO). Although it achieved a moderate AUC (~0.61), recall was very low.

Naive Bayes: Explored but had limitations due to feature independence assumptions.

Decision Tree: Interpretable but prone to overfitting, used for comparative insight.

XGBoost (Final Model): A robust gradient boosting classifier, optimized with hyperparameter tuning and 5-fold cross-validation. It achieved a mean AUC of ~0.76, significantly outperforming all other models.

To tackle the class imbalance, we used SMOTE and experimented with threshold tuning to balance recall and precision, ultimately selecting a decision threshold of 0.1576 to maximize the F1-score.

I contributed to the Naive Bayes modeling, handled preprocessing techniques like binning, SMOTE, and median imputation, and evaluated model performance using metrics such as accuracy, confusion matrix, and ROC AUC. I also contributed to the final report and helped integrate individual notebooks into a unified deliverable.

The final model allows Home Credit to:

Minimize default risk by better identifying applicants who are likely to default.

Increase revenue by still approving credit-worthy applicants even under risk constraints.

Balance risk vs reward by optimizing the decision threshold using the F1 score rather than raw accuracy.

This model has the potential to reduce financial losses while maintaining credit accessibility, aligning with Home Credit’s mission and business objectives.

Severe class imbalance made accuracy a misleading metric.

Training time for models like CatBoost was excessive without GPU acceleration.

Overfitting in initial tree-based models and oversampling approaches.

Data quality issues such as missing values and inconsistent feature formats required extensive cleaning and engineering.
Accuracy is not always the best performance metric, especially in imbalanced datasets.

Tree-based models like XGBoost, when paired with careful feature engineering and threshold tuning, offer powerful predictive capabilities.

Model interpretability and real-world business implications should guide model selection and evaluation—not just raw performance metrics.

