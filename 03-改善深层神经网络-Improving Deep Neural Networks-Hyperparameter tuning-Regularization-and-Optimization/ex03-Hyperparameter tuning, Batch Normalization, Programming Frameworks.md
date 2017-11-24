#Hyperparameter tuning, Batch Normalization, Programming Frameworks

### 1
If searching among a large number of hyperparameters, you should try values in a grid rather than random values, so that you can carry out the search more systematically and not rely on chance. True or False?

True

False
正确

### 2
Every hyperparameter, if set poorly, can have a huge negative impact on training, and so all hyperparameters are about equally important to tune well. True or False?

True

False
正确
Yes. We've seen in lecture that some hyperparameters, such as the learning rate, are more critical than others.

### 3

During hyperparameter search, whether you try to babysit one model (“Panda” strategy) or train a lot of models in parallel (“Caviar”) is largely determined by:

Whether you use batch or mini-batch optimization

The presence of local minima (and saddle points) in your neural network

The amount of computational power you can access
正确

The number of hyperparameters you have to tune

### 4
If you think β (hyperparameter for momentum) is between on 0.9 and 0.99, which of the following is the recommended way to sample a value for beta?

![](https://ws2.sinaimg.cn/large/006tKfTcly1flsxt8ir4aj30h50cvgm5.jpg)

### 5
Finding good hyperparameter values is very time-consuming. So typically you should do it once at the start of the project, and try to find very good hyperparameters so that you don’t ever have to revisit tuning them again. True or false?

True

False
正确

### 6
。
In batch normalization as presented in the videos, if you apply it on the lth layer of your neural network, what are you normalizing?

b[l]

a[l]

z[l]
正确

W[l]

### 7

In the normalization formula
![](https://ws4.sinaimg.cn/large/006tKfTcly1flsxufvb8zj303901odfo.jpg)
 why do we use epsilon?


In case μ is too small

To speed up convergence
这个选项的答案不正确

To avoid division by zero

To have a more accurate normalization

### 8
Which of the following statements about γ and β in Batch Norm are true?

The optimal values are γ=σ2+ε‾‾‾‾‾‾√, and β=μ.
未选择的是正确的

They set the mean and variance of the linear variable z[l] of a given layer.
正确

There is one global value of γ∈ℜ and one global value of β∈ℜ for each layer, and applies to all the hidden units in that layer.
未选择的是正确的

β and γ are hyperparameters of the algorithm, which we tune via random sampling.
未选择的是正确的

They can be learned using Adam, Gradient descent with momentum, or RMSprop, not just with gradient descent.
正确

###  9
After training a neural network with Batch Norm, at test time, to evaluate the neural network on a new example you should:

Skip the step where you normalize using μ and σ2 since a single test example cannot be normalized.

If you implemented Batch Norm on mini-batches of (say) 256 examples, then to evaluate on one test example, duplicate that example 256 times so that you’re working with a mini-batch the same size as during training.

Perform the needed normalizations, use μ and σ2 estimated using an exponentially weighted average across mini-batches seen during training.
正确

Use the most recent mini-batch’s value of μ and σ2 to perform the needed normalizations.

### 10

Which of these statements about deep learning programming frameworks are true? (Check all that apply)

Deep learning programming frameworks require cloud-based machines to run.
未选择的是正确的

Even if a project is currently open source, good governance of the project helps ensure that the it remains open even in the long term, rather than become closed or modified to benefit only one company.
正确

A programming framework allows you to code up deep learning algorithms with typically fewer lines of code than a lower-level language such as Python.
正确
