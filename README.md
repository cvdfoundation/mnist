# MNIST  
The MNIST database of handwritten digits is one of the most popular image recognition datasets. It contains 60k examples for training and 10k examples for testing. This page intends to provide a mirror site for downloading MNIST database hosted on http://yann.lecun.com/exdb/mnist/. Please visit the original site for more details of dataset.

# Download
[Training images](https://storage.googleapis.com/cvdf-datasets/mnist/train-images-idx3-ubyte.gz),
[Training labels](https://storage.googleapis.com/cvdf-datasets/mnist/train-labels-idx1-ubyte.gz)

[Testing images ](https://storage.googleapis.com/cvdf-datasets/mnist/t10k-images-idx3-ubyte.gz),
[Testing labels](https://storage.googleapis.com/cvdf-datasets/mnist/t10k-labels-idx1-ubyte.gz)

# File Format
The following description of file format is directly copied from http://yann.lecun.com/exdb/mnist/.

The IDX file format is a simple format for vectors and multidimensional matrices of various numerical types.
The basic format is
```
magic number 
size in dimension 0 
size in dimension 1 
size in dimension 2 
..... 
size in dimension N 
data
```

The magic number is an integer (MSB first). The first 2 bytes are always 0. The third byte codes the type of the data: 
```
0x08: unsigned byte 
0x09: signed byte 
0x0B: short (2 bytes) 
0x0C: int (4 bytes) 
0x0D: float (4 bytes) 
0x0E: double (8 bytes)
```

The 4-th byte codes the number of dimensions of the vector/matrix: 1 for vectors, 2 for matrices....
The sizes in each dimension are 4-byte integers (MSB first, high endian, like in most non-Intel processors).
The data is stored like in a C array, i.e. the index in the last dimension changes the fastest.

# Acknowledgement
We thank Prof. Yann LeCun to kindly allow CVDF to host a copy of images and annotations in MNIST database and Google Cloud Platform to provide storage space.
