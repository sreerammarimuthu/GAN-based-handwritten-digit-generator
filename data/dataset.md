## Dataset

MNIST is a dataset composed of handwritten numbers and their labels. Each MNIST image is a 28x28 grey-scale image, which is labeled with an integer value between 0 and 9, corresponding to the actual value in the image. MNIST is provided in Pytorch as 28x28 matrices containing numbers ranging from 0 to 255. There are 60000 images and labels in the training data set and 10000 images and labels in the test data set. Since this project is an unsupervised learning project, you can only use the 60000 images for your training.

Download MNIST dataset directly in Pytorch (with following code):

```python
from torchvision import datasets

mnist_trainset = datasets.MNIST(root='./data', train=True, download=True, transform=None)
mnist_testset = datasets.MNIST(root='./data', train=False, download=True, transform=None)
```

