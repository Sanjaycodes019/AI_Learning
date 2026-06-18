# Machine Learning (ML)

## What is ML?
- Machine Learning is an approach to AI where systems learn from data.
- Instead of hard-coded rules, ML uses examples to find patterns.
- ML is used for prediction, classification, clustering, and recommendation.

## Core concepts
- **Training data**: examples used to teach the model.
- **Features**: input values used by the model.
- **Labels**: correct outputs used in supervised learning.
- **Model**: the learned function mapping features to outputs.
- **Evaluation**: measuring model quality using metrics like accuracy.

## Example: Simple supervised learning

```python
from sklearn.linear_model import LinearRegression
import numpy as np

# Training data: house area and price
X = np.array([[50], [70], [90], [110], [130]])
y = np.array([150, 200, 250, 300, 350])

model = LinearRegression()
model.fit(X, y)

new_house = np.array([[100]])
predicted_price = model.predict(new_house)
print(f"Predicted price: {predicted_price[0]:.2f}")
```

This example learns a relationship between house size and price.

## What to learn next
- Supervised vs unsupervised learning
- Regression and classification
- Model validation and train/test split
- Overfitting and underfitting
- Common algorithms: decision trees, k-NN, logistic regression, SVM
