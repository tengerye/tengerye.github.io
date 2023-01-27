# Machine Learning

## Features Engineering
Categorical features: one-hot encoding, [frequency encoding](https://www.kaggle.com/general/16927), ordinal encoding.
Continuous:
Break features: date

[Tips](https://www.kaggle.com/code/ryanholbrook/creating-features):
Linear models learn sums and differences naturally, but can't learn anything more complex.
Ratios seem to be difficult for most models to learn. Ratio combinations often lead to some easy performance gains.
Linear models and neural nets generally do better with normalized features. Neural nets especially need features scaled to values not too far from 0. Tree-based models (like random forests and XGBoost) can sometimes benefit from normalization, but usually much less so.
Tree models can learn to approximate almost any combination of features, but when a combination is especially important they can still benefit from having it explicitly created, especially when data is limited.
Counts are especially helpful for tree models, since these models don't have a natural way of aggregating information across many features at once.

[Missing values](https://www.kaggle.com/code/alexisbcook/handling-missing-values).

## Features Selection
Mutual information: the MI of X and y, but some times X1 has low MI with y, but it is important for X2.

Label leakage.
## Models
[Model comparison](https://static.coggle.it/diagram/WHeBqDIrJRk-kDDY/t/categories-of-algorithms-non-exhaustive).


## Evaluation metrics
### AUC
[Class-imbalance AUC](https://zhuanlan.zhihu.com/p/552278753).