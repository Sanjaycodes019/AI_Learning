# Deep Learning (DL)

## What is DL?
- Deep Learning is a subtype of machine learning that uses neural networks with multiple layers.
- DL is especially strong for image recognition, language processing, and speech.
- It learns features automatically from raw data.

## Core concepts
- **Neurons**: basic units that compute weighted sums and activations.
- **Layers**: groups of neurons. Deep models have many layers.
- **Activation functions**: introduce nonlinearity (ReLU, sigmoid, softmax).
- **Backpropagation**: updates network weights using gradients.
- **Epoch**: one full pass over the training data.

## Example: Simple neural network with Keras

```python
from tensorflow import keras
from tensorflow.keras import layers

model = keras.Sequential([
    layers.Dense(16, activation='relu', input_shape=(4,)),
    layers.Dense(8, activation='relu'),
    layers.Dense(3, activation='softmax')
])

model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['accuracy'])

# Example data placeholder
import numpy as np
X = np.random.random((100, 4))
y = np.random.randint(0, 3, 100)

model.fit(X, y, epochs=5, batch_size=16)
```

This example builds a small neural network for classification.

## What to learn next
- How convolutional layers work for images
- How transformers work for language
- How to tune learning rate, batch size, and architecture
- When to use DL vs traditional ML
