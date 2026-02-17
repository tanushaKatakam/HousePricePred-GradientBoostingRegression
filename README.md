We implemented Gradient Boosting Regression on the California Housing dataset.
Gradient boosting is a powerful ensemble learning technique that builds a strong predictive model by sequentially combining multiple weak prediction models, also called as
weak learners, typically shallow decision trees. We demonstrated residual correction by plotting error reduction across boosting stages. We analyzed the effect of learning 
rate and number of estimators.We proved that Gradient Boosting performs sequential residual correction by observing that error decreases gradually as trees are added. The
decreasing RMSE curve confirms sequential residual minimization. Gradient Boosting reduces residual step-by-step. We use a learning rate factor when calculating it controls 
how much each new tree corrects the previous errors. More the number of trees lower will be the bias and better will be the model The final model is an additive combination of 
weak learners.

The decreasing error curve that we plotted confirms the boosting mechanism, and the final model provides a low-bias, controlled-variance estimator of house value.

In our case lower learning rate didn’t perform better because:
we didn’t increase the number of trees accordingly. The number of trees we used were 300, learning rate is directly proportional to number of trees Both must be balanced
Smaller learning rate improves generalization only when sufficient boosting rounds are used. In this dataset, 0.3 with 300 trees provided better bias-variance balance.

Lower learning rate often gives better generalization when:
-The dataset is complex
-Model can overfit
-Enough trees are used
-Hyperparameters are well tuned
-But it is not guaranteed to always give lower RMSE.


Project Conclusion:
-Implemented Gradient Boosting Regression for house price prediction.
-Demonstrated residual correction through decreasing RMSE across boosting stages.
-Analyzed impact of learning rate on convergence behavior.
-Achieved test RMSE ≈ 0.48 using optimal learning rate.
-Caculated R2 score model explains about 80.1% of the variance in house prices.
-Verified model performance using Actual vs Predicted visualization.
