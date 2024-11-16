
# Heart Disease Prediction Using Logistic Regression

This project implements a predictive model for heart disease diagnosis using Logistic Regression. The model leverages patient data to classify whether a patient has heart disease based on various health metrics. The dataset used for this study is the Heart Disease dataset, which contains several features related to the patient's health.

## Project Overview

The code performs the following steps:

1. **Data Importation**: 
   - The heart disease dataset is imported from a CSV file using Pandas, which allows for efficient data manipulation and analysis.

2. **Data Exploration**:
   - Initial data exploration is done using `data.head()` to check the first few records and `data.info()` to understand the data types and structure. 

   ### Example Data
   ```plaintext
   Age    Sex    ChestPainType    RestingBP    Cholesterol    FastingBS    RestingECG    MaxHR    ExerciseAngina    Oldpeak    ST_Slope    HeartDisease
   40     M      ATA              140          289             0            Normal        172      N                0.0       Up          0
   ```

3. **Data Visualization**:
   - The dataset is visualized using histograms and boxplots to understand the distributions and identify potential outliers. Below are visualizations for the **Age** feature:

   ### Age Boxplot
   ![Age Boxplot](https://github.com/lingRowan/Heart_Disease_Prediction/blob/main/boxplot.png)

   ### Age Histogram
   ![Age Histogram](https://github.com/lingRowan/Heart_Disease_Prediction/blob/main/histogram.png)

   - A heatmap is created to visualize correlations between numerical features, providing insight into relationships within the data:

   ### Correlation Heatmap
   ![Correlation Heatmap](https://github.com/lingRowan/Heart_Disease_Prediction/blob/main/Corr.png)

4. **Handling Categorical Variables**:
   - Categorical variables are transformed into numeric format using one-hot encoding, which prepares the data for modeling.

5. **Model Training**:
   - A Logistic Regression model is instantiated and trained using the training dataset. The model attempts to predict the presence of heart disease based on the input features.
   - The model's performance is evaluated on the training set, with a convergence warning indicating that more iterations may be needed for optimal fitting.

6. **Model Evaluation**:
   - The class predictions and the probabilities of positive predictions are obtained.
   - A classification report is generated, showcasing precision, recall, F1-score, and overall accuracy of the model on the test dataset. The model achieved an accuracy of approximately 88%.

7. **Survival Function**:
   - A function, `survie`, is defined to facilitate predictions for new patients based on input health metrics. This function allows users to input individual patient data and obtain predictions and probabilities for heart disease classification.

### Example Usage

```python
survie(model, Age=60, RestingBP=145, Cholesterol=200, FastingBS=0, MaxHR=150, Oldpeak=1.5, HeartDisease=0, Sex_F=True, ...)
```
