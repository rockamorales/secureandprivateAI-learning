# Tensors in pytorch
### What is a tensor?

* Tensors is a generalization of matrices. 

  * A vector is a 1-dimensional tensor, 
  * a matrix is a 2-dimensional tensor, 
  * an array with three indices is a 3-dimensional tensor (RGB color images for example). 
* The fundamental data structure for neural networks are tensors and PyTorch (as well as pretty much every other deep learning framework) is built around tensors.

### How to create a tensor?
* ```features = torch.randn(1, 5)``` creates a tensor with shape ```(1, 5)```, one row and five columns, that contains values randomly distributed  according to the normal distribution with a mean of zero and standard deviation of one.
* ```weights = torch.randn_like(features)``` creates another tensor with the same shape as features, again containing values from a normal distribution.
* A tensor can be constructed from a Python list or sequence using the torch.tensor() constructor:
```
>>> torch.tensor([[1., -1.], [1., -1.]])
tensor([[ 1.0000, -1.0000],
        [ 1.0000, -1.0000]])
>>> torch.tensor(np.array([[1, 2, 3], [4, 5, 6]]))
tensor([[ 1,  2,  3],
        [ 4,  5,  6]])
```

* A tensor of specific data type can be constructed by passing a torch.dtype and/or a torch.device to a constructor or tensor creation op:

```
>>> torch.zeros([2, 4], dtype=torch.int32)
tensor([[ 0,  0,  0,  0],
        [ 0,  0,  0,  0]], dtype=torch.int32)
>>> cuda0 = torch.device('cuda:0')
>>> torch.ones([2, 4], dtype=torch.float64, device=cuda0)
tensor([[ 1.0000,  1.0000,  1.0000,  1.0000],
        [ 1.0000,  1.0000,  1.0000,  1.0000]], dtype=torch.float64, device='cuda:0')
```
* See tensor documentation: https://pytorch.org/docs/stable/tensors.html

### How to work with tensors?

