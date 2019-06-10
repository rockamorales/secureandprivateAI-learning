# Tensors in pytorch
### What is a tensor?

* Tensors is a generalization of matrices. 

* A vector is a 1-dimensional tensor, 
* a matrix is a 2-dimensional tensor, 
* an array with three indices is a 3-dimensional tensor (RGB color images for example). 
* The fundamental data structure for neural networks are tensors and PyTorch (as well as pretty much every other deep learning framework) is built around tensors.

### How to create a tensor?
* ´´´ features = torch.randn((1, 5)) ´´´ creates a tensor with shape ´´´(1, 5) ´´´, one row and five columns, that contains values randomly distributed  according to the normal distribution with a mean of zero and standard deviation of one.

### How to work with tensors?
