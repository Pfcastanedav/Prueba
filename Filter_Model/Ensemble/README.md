# Summary of Ensemble

[<< Go back](../README.md)


## Ensemble structure
| Model              |   Weight |
|:-------------------|---------:|
| 1_Default_LightGBM |        1 |
| 2_Xgboost          |        1 |

## Metric details
|           |     score |     threshold |
|:----------|----------:|--------------:|
| logloss   | 0.0114859 | nan           |
| auc       | 0.999956  | nan           |
| f1        | 0.996125  |   0.721818    |
| accuracy  | 0.996578  |   0.721818    |
| precision | 1         |   0.982899    |
| recall    | 1         |   0.000290194 |
| mcc       | 0.993077  |   0.721818    |


## Metric details with threshold from accuracy metric
|           |     score |   threshold |
|:----------|----------:|------------:|
| logloss   | 0.0114859 |  nan        |
| auc       | 0.999956  |  nan        |
| f1        | 0.996125  |    0.721818 |
| accuracy  | 0.996578  |    0.721818 |
| precision | 0.999219  |    0.721818 |
| recall    | 0.993051  |    0.721818 |
| mcc       | 0.993077  |    0.721818 |


## Confusion matrix (at threshold=0.721818)
|              |   Predicted as 0 |   Predicted as 1 |
|:-------------|-----------------:|-----------------:|
| Labeled as 0 |            37259 |               23 |
| Labeled as 1 |              206 |            29437 |

## Learning curves
![Learning curves](learning_curves.png)
## Confusion Matrix

![Confusion Matrix](confusion_matrix.png)


## Normalized Confusion Matrix

![Normalized Confusion Matrix](confusion_matrix_normalized.png)


## ROC Curve

![ROC Curve](roc_curve.png)


## Kolmogorov-Smirnov Statistic

![Kolmogorov-Smirnov Statistic](ks_statistic.png)


## Precision-Recall Curve

![Precision-Recall Curve](precision_recall_curve.png)


## Calibration Curve

![Calibration Curve](calibration_curve_curve.png)


## Cumulative Gains Curve

![Cumulative Gains Curve](cumulative_gains_curve.png)


## Lift Curve

![Lift Curve](lift_curve.png)



[<< Go back](../README.md)
