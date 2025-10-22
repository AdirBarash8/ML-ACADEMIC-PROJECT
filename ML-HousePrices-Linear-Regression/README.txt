Overview - House Prices - ML

When asked to describe their dream house, most homebuyers might focus on features like the number of bedrooms or a charming white-picket fence. However, the real factors influencing home prices extend far beyond these simple attributes.

In this intriguing dataset from a playground competition, we're presented with 79 explanatory variables that capture nearly every aspect of residential properties in Ames, Iowa. This comprehensive dataset challenges us to predict the final sale price of each home, revealing the complex dynamics of real estate valuation.

From the height of the basement ceiling to the proximity to a railroad, every detail plays a role in price negotiations, illustrating that the true value of a home is determined by a myriad of interconnected factors.

In this practice, we undertook extensive data cleansing and engineered new features to enrich the dataset. We compared the performance of linear regression and stochastic gradient descent (SGD) models, utilizing various regularization techniques such as Ridge, Lasso, and Elastic Net to prevent overfitting and enhance model accuracy.

Additionally, we experimented with different feature selection algorithms, including forward and backward selection, to identify the most influential variables. These efforts aimed to optimize our predictive models and gain deeper insights into the factors that drive home prices.

**Project Summary**

***Part 1 – Model Exploration and Evaluation***
1. Initial Model Exploration

The project began with a comparative study of multiple regression algorithms — including Locally Weighted Linear Regression (LWLR), K-Nearest Neighbors (KNN), Decision Trees, and Support Vector Machines (SVM).
Each model’s predictive performance was rigorously assessed using Root Mean Square Error (RMSE) and cross-validation to ensure generalization quality.
Performance results were visualized through detailed score and loss graphs, providing insight into model stability and variance.

2. Dimensionality Reduction

To address the high dimensionality of the dataset and improve computational efficiency, Principal Component Analysis (PCA) was implemented.
After analyzing variance explained by each component, the optimal number of principal components was determined to be 14, balancing accuracy and model simplicity.

3. Ensemble Learning

The project expanded into ensemble methods — combining multiple learners to enhance performance and robustness.
Techniques such as Bagging, n-fold Bagging, and Boosting (AdaBoost) were tested using both the original dataset and PCA-transformed data.
Additionally, the SGDRegressor was incorporated into ensemble configurations to evaluate its contribution to predictive accuracy.
All ensemble models were evaluated through RMSE and cross-validation, with results presented in comparative visualizations.

***Part 2 – Model Comparison, Selection, and Final Predictions***
4. Comprehensive Model Comparison

Following extensive experimentation, a global evaluation of all trained models — including base regressors, ensemble variants, and PCA-based models — was conducted.
This stage focused on ranking model performance using validation RMSE and cross-validation scores, highlighting the top-performing models such as AdaBoost, Bagging SGD, and Best Model PCA.

5. Final Model Selection

Through analysis of validation metrics and consistency across folds, the ‘Best Model PCA’ emerged as the most reliable and accurate configuration.
This model demonstrated strong generalization while maintaining computational efficiency.

6. Prediction and Insights

The selected Best Model PCA was employed to generate final predictions on the test dataset.
Visual evaluation confirmed that the model successfully captured complex relationships between features and sale prices, validating the impact of earlier feature engineering and dimensionality-reduction efforts.

7. Conclusions

By continuously evaluating, visualizing, and comparing model performance throughout all project stages, the workflow ensured data-driven decision-making in model selection.
This iterative process led to meaningful improvements in accuracy and provided valuable insights into which property characteristics most strongly influence home prices.