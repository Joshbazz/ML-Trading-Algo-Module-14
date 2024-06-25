# Machine Learning Trading Bot

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

# Machine Learning Model Comparison

This report compares the performance of two different machine learning algorithms, Support Vector Machine (SVM) and Logistic Regression, on a binary classification task. The classification reports for both models are provided below, along with an analysis of their performance.

## Classification Reports

### SVM Model

```              precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092```

### Logistic Regression Model

```              precision    recall  f1-score   support

        -1.0       0.44      0.33      0.38      1804
         1.0       0.56      0.66      0.61      2288

    accuracy                           0.52      4092
   macro avg       0.50      0.50      0.49      4092
weighted avg       0.51      0.52      0.51      4092```

## Analysis

### Class -1.0 Performance
- **SVM Model**:
  - Precision: 0.43 (43% of the predicted -1.0 labels are correct)
  - Recall: 0.04 (4% of actual -1.0 labels are correctly identified)
  - F1-score: 0.07 (harmonic mean of precision and recall, very low indicating poor performance)
  - Support: 1804 (number of actual -1.0 labels)
  
- **Logistic Regression Model**:
  - Precision: 0.44 (44% of the predicted -1.0 labels are correct)
  - Recall: 0.33 (33% of actual -1.0 labels are correctly identified)
  - F1-score: 0.38 (harmonic mean of precision and recall, much better than the first report)
  - Support: 1804 (number of actual -1.0 labels)

### Class 1.0 Performance
- **SVM Model**:
  - Precision: 0.56 (56% of the predicted 1.0 labels are correct)
  - Recall: 0.96 (96% of actual 1.0 labels are correctly identified)
  - F1-score: 0.71 (good balance between precision and recall)
  - Support: 2288 (number of actual 1.0 labels)
  
- **Logistic Regression Model**:
  - Precision: 0.56 (56% of the predicted 1.0 labels are correct)
  - Recall: 0.66 (66% of actual 1.0 labels are correctly identified)
  - F1-score: 0.61 (balance between precision and recall, lower than the first report but more balanced)
  - Support: 2288 (number of actual 1.0 labels)

### Overall Performance
- **SVM Model**:
  - Accuracy: 0.55 (55% of all labels are correctly classified)
  - Macro avg (unweighted mean): Precision: 0.49, Recall: 0.50, F1-score: 0.39
  - Weighted avg (weighted by support): Precision: 0.50, Recall: 0.55, F1-score: 0.43

- **Logistic Regression Model**:
  - Accuracy: 0.52 (52% of all labels are correctly classified)
  - Macro avg (unweighted mean): Precision: 0.50, Recall: 0.50, F1-score: 0.49
  - Weighted avg (weighted by support): Precision: 0.51, Recall: 0.52, F1-score: 0.51

### Conclusion
The **Logistic Regression model** appears to be objectively better because it provides a more balanced performance across both classes, as indicated by the higher F1-scores for the -1.0 class and higher macro and weighted averages. The SVM model, while having a higher recall for the 1.0 class, performs poorly in identifying the -1.0 class. Therefore, the Logistic Regression model seems more robust and reliable for a classification task where performance across all classes is important.
