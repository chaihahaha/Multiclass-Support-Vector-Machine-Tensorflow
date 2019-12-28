# Multiclass Support Vector Machine Tensorflow

This is a multiclass SVM implmented on Tensorflow by Shitong CHAI. Copyright Reserved.

### Use increase_dims() to increase the dimension of input features

### Example
```python
from svm import *
import numpy as np
from sklearn.decomposition import KernelPCA

kpca = KernelPCA(kernel="rbf", gamma=1)
train_x = kpca.fit_transform(raw_X) # or train_x=increase_dims(raw_x)

svm = svm_model(number_of_classes,train_x.shape[1],learning_rate,regularization)

svm.fit(train_x,train_y,iterations)

svm.predict(test_x)
```
To save weights and load weights:
```python
svm.save("svm.pickle")
```

```python
svm=svm_model(n_classes,dimension)
svm.load("svm.pickle")

```
