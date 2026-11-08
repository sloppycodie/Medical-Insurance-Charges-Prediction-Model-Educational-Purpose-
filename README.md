# Medical Insurance Charges Prediction

A beginner-friendly machine learning project that explores a medical
insurance dataset and uses **Linear Regression** to predict individual
insurance charges.

The goal of this project was to practise the fundamental machine
learning workflow: exploring data, preparing features, training a model,
evaluating predictions, and comparing the model against a simple
baseline.

## Project Overview

-   **Problem type:** Supervised learning --- regression
-   **Target variable:** `charges`
-   **Main model:** Linear Regression
-   **Baseline:** Dummy Regressor using the median
-   **Train/test split:** 80% / 20%
-   **Random state:** 69

## Dataset

The dataset contains information about medical insurance beneficiaries.

  Feature      Description
  ------------ -----------------------------------------------
  `age`        Age of the beneficiary
  `sex`        Sex of the beneficiary
  `bmi`        Body mass index
  `children`   Number of children covered by the insurance
  `smoker`     Whether the beneficiary smokes
  `region`     Residential region
  `charges`    Medical insurance charges (prediction target)

The original dataset contained 1,338 rows. One duplicate row was
removed, leaving **1,337 rows** for the project.

> Make sure you have the dataset file (`insurance.csv`) before running
> the notebook. The dataset is not included in this repository unless
> you add it yourself.

## Workflow

1.  **Data inspection**
    -   Loaded the dataset with pandas.
    -   Inspected its dimensions, columns, data types, and summary
        statistics.
    -   Checked for missing values and duplicate rows.
    -   Removed the duplicate row.
2.  **Exploratory data analysis (EDA)**
    -   Used histograms to inspect distributions.
    -   Used boxplots to compare insurance charges across categories.
    -   Examined correlations between numerical features.
    -   Explored how age, BMI, smoking status, and other features relate
        to charges.
3.  **Feature preparation**
    -   Separated the features (`X`) from the target (`y`).
    -   Split the data into training and test sets.
    -   Applied One-Hot Encoding to categorical features: `sex`,
        `smoker`, and `region`.
    -   Combined the encoded categorical features with the numerical
        features.
4.  **Model training**
    -   Trained a Linear Regression model using the training data.
    -   Generated predictions for the test data.
5.  **Model evaluation**
    -   Evaluated predictions using Mean Absolute Error (MAE) and Root
        Mean Squared Error (RMSE).
    -   Compared Linear Regression against a median-prediction baseline.

## Results

The following results were obtained on the held-out test set:

  Model / Metric                         Result
  ---------------------------------- ----------
  Baseline MAE (median prediction)     8,675.82
  Linear Regression MAE                4,512.78
  Linear Regression RMSE               6,718.61

**Interpretation:** Linear Regression achieved a lower MAE than the
baseline. Its average absolute prediction error was about 4,512.78,
compared with about 8,675.82 for the baseline.

This indicates that the features provide useful predictive information.
However, the model is not expected to predict every person's charges
accurately.

## Tools and Libraries

-   Python
-   pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   scikit-learn
-   Jupyter Notebook

## How to Run

1.  Clone this repository:

    ``` bash
    git clone <your-repository-url>
    cd <your-repository-folder>
    ```

2.  Install the required libraries:

    ``` bash
    pip install numpy pandas matplotlib seaborn scikit-learn jupyter
    ```

3.  Put `insurance.csv` in the location expected by your notebook.

4.  Start Jupyter:

    ``` bash
    jupyter notebook
    ```

5.  Open and run the project notebook from top to bottom.

## Limitations and Future Improvements

This is an introductory learning project, not a production-ready
insurance pricing system.

Possible future improvements include:

-   Using cross-validation for a more robust evaluation.
-   Building a preprocessing pipeline.
-   Exploring feature interactions and other regression models.
-   Investigating the effect of outliers and the skewed target
    distribution.
-   Comparing additional models using the same evaluation approach.

These improvements are intentionally left for future study.

## What I Learned

Through this project, I practised:

-   Exploring and understanding a real-world dataset.
-   Performing basic exploratory data analysis.
-   Separating features and target variables.
-   Splitting data into training and test sets.
-   Encoding categorical variables with One-Hot Encoding.
-   Training a Linear Regression model.
-   Making predictions and evaluating them with MAE and RMSE.
-   Using a baseline model to judge whether a machine learning model
    adds value.

------------------------------------------------------------------------

**Note:** This project was built for learning and practising the
fundamentals of machine learning.
