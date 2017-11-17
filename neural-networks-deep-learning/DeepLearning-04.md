### 1

What is the "cache" used for in our implementation of forward propagation and backward propagation?

It is used to keep track of the hyperparameters that we are searching over, to speed up computation.

We use it to pass variables computed during backward propagation to the corresponding forward propagation step. It contains useful values for forward propagation to compute activations.

It is used to cache the intermediate values of the cost function during training.

We use it to pass variables computed during forward propagation to the corresponding backward propagation step. It contains useful values for backward propagation to compute derivatives.
正确
Correct, the "cache" records values from the forward propagation units and sends it to the backward propagation units because it is needed to compute the chain rule derivatives.

### 2

Among the following, which ones are "hyperparameters"? (Check all that apply.)

![](https://ws2.sinaimg.cn/large/006tNc79ly1fll5csv04mj30fu0kzwf6.jpg)


### 3

Which of the following statements is true?

The deeper layers of a neural network are typically computing more complex features of the input than the earlier layers.
正确

The earlier layers of a neural network are typically computing more complex features of the input than the deeper layers.

### 4

Vectorization allows you to compute forward propagation in an L-layer neural network without an explicit for-loop (or any other explicit iterative loop) over the layers l=1, 2, …,L. True/False?

True

False
正确
Forward propagation propagates the input through the layers, although for shallow networks we may just write all the lines (a[2]=g[2](z[2]), z[2]=W[2]a[1]+b[2], ...) in a deeper network, we cannot avoid a for loop iterating over the layers: (a[l]=g[l](z[l]), z[l]=W[l]a[l−1]+b[l], ...).

### 5


Assume we store the values for n[l] in an array called layers, as follows: layer_dims = [nx, 4,3,2,1]. So layer 1 has four hidden units, layer 2 has 3 hidden units and so on. Which of the following for-loops will allow you to initialize the parameters for the model?
![](https://ws1.sinaimg.cn/large/006tNc79ly1fll5em41ojj30hf0ie761.jpg)

### 6

Consider the following neural network.
![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/cwmw1nrfEeeJIwrF5BVsIg_e9a22da9e380c0350d2dfd47dcf34503_Screen-Shot-2017-08-06-at-12.42.46-PM.png?expiry=1511049600000&hmac=9eoujSVKF5eaZAGnkYNWydblYGztbyKfsejlNKI8S9I)

How many layers does this network have?

The number of layers L is 4. The number of hidden layers is 3.
正确
Yes. As seen in lecture, the number of layers is counted as the number of hidden layers + 1. The input and output layers are not counted as hidden layers.

The number of layers L is 3. The number of hidden layers is 3.

The number of layers L is 4. The number of hidden layers is 4.

The number of layers L is 5. The number of hidden layers is 4.

### 7
During forward propagation, in the forward function for a layer l you need to know what is the activation function in a layer (Sigmoid, tanh, ReLU, etc.). During backpropagation, the corresponding backward function also needs to know what is the activation function for layer l, since the gradient depends on it. True/False?

True
正确
Yes, as you've seen in the week 3 each activation has a different derivative. Thus, during backpropagation you need to know which activation was used in the forward propagation to be able to compute the correct derivative.

False

### 8

There are certain functions with the following properties:

(i) To compute the function using a shallow network circuit, you will need a large network (where we measure size by the number of logic gates in the network), but (ii) To compute it using a deep network circuit, you need only an exponentially smaller network. True/False?

True
正确

False

### 9
Consider the following 2 hidden layer neural network:
![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8sF12nrfEeeumw4MySoK5g_36df26a0659f76c6566ff4f3706e6ad2_Screen-Shot-2017-08-05-at-12.50.32-PM.png?expiry=1511049600000&hmac=lCeUqt4utk6sMXocvx-SkcKQ5VBadCtdRNZID-mHMu4)
Which of the following statements are True? (Check all that apply).
![](https://ws3.sinaimg.cn/large/006tNc79ly1fll5gihigjj30ai0octa6.jpg)

### 10


Whereas the previous question used a specific network, in the general case what is the dimension of W^{[l]}, the weight matrix associated with layer l?

![](https://ws4.sinaimg.cn/large/006tNc79ly1fll5gzt28mj30h807rglu.jpg)


