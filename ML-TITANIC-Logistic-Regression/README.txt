Overview - Titanic - ML

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1,502 out of 2,224 passengers and crew.

While luck played a role in survival, certain groups of people were statistically more likely to survive than others.

In this challenge, we aim to build a predictive model to answer the question: “What sorts of people were more likely to survive?” using passenger data such as name, age, gender, socio-economic class, and other relevant features.

**Project Summary**

***Part 1 – Data Preparation and Baseline Modeling***
1. Data Preprocessing

The project began with a thorough data-cleaning phase to ensure reliability and consistency:

Missing values were identified and handled appropriately.

Categorical variables were encoded into numerical form for model compatibility.

Exploratory Data Analysis (EDA) was conducted to explore feature relationships and understand how different attributes influenced the target variable (Survived).

2. Model Selection

To establish a baseline, we compared three classification algorithms:

SGDClassifier

Logistic Regression

Multilayer Perceptron (MLP)

The MLP model demonstrated the best performance across evaluation metrics and was selected for further experimentation.

3. Feature Engineering

We explored multiple feature sets to identify which variables contributed most to survival prediction.
A dedicated evaluation function was implemented to test various feature combinations and hyperparameters, providing systematic insights into feature importance.

4. Model Training and Evaluation

The chosen MLP model was trained on the full dataset and evaluated using multiple performance metrics.
After confirming its stability and accuracy, the model’s predictions were submitted to Kaggle for external benchmarking.

***Part 2 – Advanced Feature Selection and Model Optimization***

5. Feature Selection Techniques

To enhance model interpretability and performance, we applied both:

Backward Feature Selection (BFS)

Forward Feature Selection (FFS)

Although both methods produced comparable results, BFS yielded a more comprehensive set of six features, compared to FFS’s three.
We selected BFS for its broader representation and potential predictive advantage.

6. Hyperparameter Optimization

We utilized Grid Search to fine-tune model hyperparameters, ensuring each algorithm operated under its most effective configuration.

7. Comparative Evaluation

All candidate models were evaluated using:

Cross-validation accuracy

Confusion matrices

Key Performance Indicators (KPIs)

Graphical performance visualizations

This detailed analysis identified the AdaBoost model as the top performer, outperforming other tested algorithms.

8. Final Model Training and Prediction

The AdaBoost model, trained using the optimal BFS-selected feature set (X_selected_features_BW), was finalized and prepared for predicting survival outcomes on unseen test data.