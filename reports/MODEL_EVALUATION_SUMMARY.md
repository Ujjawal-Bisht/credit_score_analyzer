# Credit Risk Model Evaluation Summary

This notebook evaluates a set of machine-learning models built on the cleaned German credit dataset after feature engineering and label encoding.

## Model Comparison

| Model | Accuracy | Precision | Recall | F1 Score | ROC AUC |
| --- | ---: | ---: | ---: | ---: | ---: |
| Decision Tree | 0.6242 | 0.6593 | 0.6818 | 0.6704 | 0.6434 |
| Random Forest | 0.6561 | 0.6700 | 0.7614 | 0.7128 | 0.6841 |
| Extra Trees | 0.6497 | 0.6897 | 0.6818 | 0.6857 | 0.6963 |
| XGBoost | 0.6051 | 0.6548 | 0.6250 | 0.6395 | 0.6624 |

## Best Model Selection

For this project, the Random Forest model is the preferred choice because it delivers the best balance of recall and F1 score while staying very close to Extra Trees on ROC AUC.

The Random Forest achieved recall of 0.7614 and F1 score of 0.7128, both higher than Extra Trees (0.6818 recall and 0.6857 F1). Its ROC AUC is also close at 0.6841 versus 0.6963 for Extra Trees, so the difference is small enough that the recall/F1 advantage makes Random Forest the better business choice for credit-risk detection.
