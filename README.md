# IoT-Driven Machine Learning Framework for Fraud Detection and Customer Risk Prediction in Retail Banking

## Author Information

**Prepared By:** Usman Ahmad
**Assigned By:** Dr. Adnan Amin
**University:** Institute of Management Sciences (IMSciences), Peshawar
**Department:** Computer Science
**Submission Year:** 2026

---

## Project Overview

This project presents a machine learning-based fraud detection system for retail banking using the Credit Card Fraud Detection Dataset. The objective is to identify fraudulent transactions accurately while supporting customer risk prediction and future IoT-based fraud prevention systems.

The proposed framework combines data preprocessing, feature engineering, class balancing using SMOTE, Random Forest classification, and performance evaluation using standard machine learning metrics.

This work also explores the future integration of IoT-generated behavioral data for real-time fraud monitoring and decision support in banking systems.

---

## Dataset Information

### Dataset Name

Credit Card Fraud Detection Dataset

### Dataset Source

Kaggle Dataset

### Dataset Link

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

### Dataset Statistics

* Total Samples: 284,807
* Total Features: 30 Input Features + 1 Target Variable
* Fraud Cases: 492
* Non-Fraud Cases: 284,315
* Fraud Percentage: 0.1727%

The dataset is highly imbalanced, which reflects real-world fraud detection challenges in retail banking.

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Feature and target separation
2. Standardization of the `Amount` feature using StandardScaler
3. Train-test split using 80/20 ratio
4. Stratified sampling using `random_state = 42`
5. Class balancing using SMOTE on training data only

### Train-Test Split

* Training Data: (227,845, 30)
* Testing Data: (56,962, 30)

---

## Proposed Model Workflow

```text
Input Data
↓
Data Preprocessing
↓
Feature Engineering
↓
Model Architecture
↓
Training
↓
Evaluation
↓
Output / Prediction
```

---

## Model Used

### Random Forest Classifier

Random Forest was selected because it performs well on imbalanced classification tasks, captures non-linear fraud patterns, reduces overfitting, and provides strong performance for financial fraud detection systems.

### Hyperparameters

```python
RandomForestClassifier(
    n_estimators = 100,
    random_state = 42,
    n_jobs = -1
)
```

---

## Tools and Libraries

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn (SMOTE)
* Matplotlib
* Seaborn
* LaTeX

---

## Evaluation Metrics

| Metric    |  Value |
| --------- | -----: |
| Accuracy  | 0.9994 |
| Precision | 0.8265 |
| Recall    | 0.8265 |
| F1 Score  | 0.8265 |
| ROC-AUC   | 0.9131 |

### Confusion Matrix

```text
[[56847   17]
 [   17   81]]
```

The model achieved excellent fraud detection performance with strong fraud recall and very low false positive rates.

---

## Results Summary

### Strengths

* Very high overall accuracy
* Strong fraud detection recall
* Low false positive rate
* Effective handling of class imbalance using SMOTE
* Reliable performance of Random Forest on banking datasets

### Limitations

* Fraud cases remain difficult due to rarity
* Some fraud cases are still missed
* Real-time IoT streaming was proposed conceptually and not implemented directly in dataset form

---

## Comparison with Existing Studies

| Study                  | Dataset                   | Model                    | Accuracy |
| ---------------------- | ------------------------- | ------------------------ | -------: |
| Taha & Malebary (2020) | Credit Card Fraud Dataset | LightGBM                 |    99.2% |
| Alarfaj et al. (2022)  | Credit Card Transactions  | Deep Learning + Ensemble |    99.4% |
| Alatawi (2025)         | IoT-Based Dataset         | Random Forest            |   99.99% |
| Proposed Study         | Credit Card Fraud Dataset | Random Forest + SMOTE    |   99.94% |

---

## Future Scope

This project can be extended toward:

* Real-time IoT fraud monitoring
* Customer behavioral analytics
* Banking fraud prevention systems
* MIS dashboard integration
* Decision support systems for retail banking

---

## Conclusion

This project successfully demonstrates that Random Forest with SMOTE is highly effective for fraud detection in retail banking. The system provides strong classification performance and creates a solid foundation for future IoT-driven real-time fraud prevention systems.

The framework is suitable for academic research, banking applications, and future IEEE publication development.

---

## License

This project is developed for academic research purposes only.

MIT License recommended.
