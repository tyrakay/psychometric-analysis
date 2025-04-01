# Item Response Analysis: Logistic Regression and Reliability Assessment

## Overview
This script performs a comprehensive psychometric analysis by employing logistic regression to model item responses, estimate key parameters such as item discrimination and difficulty, and assess internal reliability metrics. The approach integrates classical test theory with item response theory (IRT) principles to ensure robust evaluation of response patterns.

## Requirements
- Python 3.x
- pandas, numpy, matplotlib, scikit-learn

## Methodology
### 1. Data Preprocessing:
- Filters items with insufficient response data (threshold: ≥50 responses per item).
- Computes **raw ability estimates** for each respondent by averaging their item scores.
- Constructs a **user-item response matrix** for subsequent modeling.

### 2. Item Response Modeling (2PL IRT):
- Implements a **Two-Parameter Logistic (2PL) Model** via logistic regression to estimate:
  - **Discrimination (a):** Sensitivity of an item in distinguishing between respondents with different ability levels.
  - **Difficulty (b):** Ability level required for a 50% probability of a correct response.
- Fits a logistic regression model per item using ability estimates as predictors.

### 3. Visualization of Item Characteristic Curves (ICCs):
- Plots ICCs to illustrate the probability of a correct response across a range of ability levels.
- Utilizes the logistic function to model response probabilities as a function of discrimination and difficulty parameters.

### 4. Reliability and Model Fit Evaluation:
- Computes **Cronbach’s Alpha** to assess internal consistency and scale reliability.
- Estimates **log-likelihood values** for each item to quantify model fit and predictive adequacy.

## Outputs
- **Refined Item-Response Matrix**: A structured dataset for psychometric modeling.
- **Estimated Item Parameters**: Discrimination and difficulty coefficients for each item.
- **Graphical Representations**: ICC plots visualizing item behavior.
- **Reliability Metrics**: Cronbach’s Alpha for internal consistency validation.
- **Model Fit Indicators**: Log-likelihood values for performance assessment.

## Usage
Ensure `psy_data` is formatted with `user_id`, `item_id`, `score`, and `raw_difficulty` before execution. Running the script will generate parameter estimates, diagnostic plots, and reliability evaluations for psychometric assessment.

## Author
Tyra Koranteng

