# SVM Parameter Optimization for Room Occupancy Estimation

This project aims to optimize Support Vector Machine (SVM) hyperparameters for predicting room occupancy using the Room Occupancy dataset from UCI library.

## Dataset

The dataset can be accessed at https://archive.ics.uci.edu/ml/datasets/Room+Occupancy+Estimation.

## Objective

To identify the best SVM kernel and corresponding hyperparameters to maximize model accuracy.

## Workflow
1. Data Preprocessing:
   - Dropped `Date` and `Time` columns.
   - Normalized feature values using `StandardScaler`.

2. Model Training:
   - Performed 10 iterations of randomized train-test splits.
   - For each split, evaluated different SVM kernels (`linear`, `poly`, `rbf`, `sigmoid`).
   - Recorded best accuracy and corresponding parameters.

3. Evaluation:
   - Accuracy score used as the evaluation metric.
   - Summary table generated across all samples.

4. Results:
 ![image](https://github.com/user-attachments/assets/5e4ad870-763a-4993-88c6-3c2d003d21bb)

5. Conclusion:
From the graph, we can conclude that the model is well trained and parameter have been optimized due to the less gap between training and cross-validation curve.
After an unstable start, the model achieves consistently high accuracy with minimal overfitting. The training and cross-validation scores align well, indicating robust generalization
The graph is made for the sample which has best accuracy. Sample 9 has the best accuracy of 0.97 having kernel = Poly, Nu = 1.27 and Epsilon = 6.87.

