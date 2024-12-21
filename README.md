# Concrete Strength Dataset Analysis

This project involves the analysis of a concrete strength dataset with the goal of improving the performance of a linear regression model through various data preprocessing techniques.
I have performed Regression Analysis by using Least Square Method and Gradient Descent Algorithm. Splitted the dataset into Training and Test data to check for the performance. Checked for all the assumptions I have made, computed performance of my model and finally written a report on the results obtained. The description of the dataset is also provided.

## Project Overview

The objective of this analysis was to:
1. Handle duplicated values.
2. Detect and fix outliers.
3. Apply transformations to normalize independent features.
4. Perform feature scaling.
5. Assess the improvement in model accuracy after implementing these corrections.

## Data Preprocessing

### 1. Duplicated Values
- **Problem:** The dataset contained 25 duplicated rows.
- **Solution:** All duplicated values were identified and handled to avoid redundancy in the dataset.

### 2. Outlier Detection and Handling
- **Method Used:** Outliers were detected using box plots.
- **Solution:** Outliers were fixed using the Interquartile Range (IQR) method, which identifies outliers as values that fall outside the range of `Q1 - 1.5*(Q3-Q1)` and `Q3 + 1.5*(Q3-Q1)`.

### 3. Normalizing Independent Features
- **Observation:** Independent features were not normally distributed.
- **Solution:** The Box-Cox transformation was applied to convert independent features to a more normal distribution.

### 4. Feature Scaling
- **Importance:** Feature scaling ensures that all independent variables are on the same scale, preventing machine learning algorithms from weighing features with larger magnitudes disproportionately.
- **Method:** Feature scaling was applied to standardize the data before applying the linear regression model.

## Model Performance

Two linear regression models were trained to evaluate the effect of the preprocessing steps on model performance:
1. **Without Data Corrections:**
   - Accuracy: **71.487%**
   
2. **After Data Corrections (Handling duplicates, fixing outliers, normalizing features, and scaling):**
   - Accuracy: **82.837%**

This 11.35% improvement in accuracy highlights the significance of data preprocessing in building effective machine learning models.

## Conclusion

- Data preprocessing steps, including handling duplicates, outliers, feature normalization, and feature scaling, significantly improved the accuracy of the linear regression model.
- The accuracy of the model increased from **71.487%** to **82.837%** after implementing these corrections.

## Results

```python
print(f"Accuracy of the model without checking assumption of linear regression is {r2_score(y_test, y_pred) * 100:.3f}%")
print(f"Accuracy of the model after checking assumption of the linear regression model is {R_Square1*100:.3f}%")
```
* **Without Assumptions Check: 71.487%**
* **After Assumptions Check: 82.837%**

This `README.md` provides a concise and structured summary of your cement dataset analysis, highlighting the importance of each preprocessing step and its impact on model performance.

- - -

## **Contributing**

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes and commit them (`git commit -m 'Add feature-name'`).
4. Push to your branch (`git push origin feature-name`).
5. Open a pull request.

- - -

## **License**

This project is licensed under the [MIT License](LICENSE).

- - -

## **Contact**

For any inquiries or support, please reach out to:
- **Name**: Abhishek Singh
- **Email**: sabhisheksingh343204@gmail.com
- **LinkedIn**: [My LinkedIn Profile](https://www.linkedin.com/in/abhishek-singh-bba2662a9)

- - -
