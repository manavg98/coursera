# Optimization algorithms

### 1
Which notation would you use to denote the 3rd layer’s activations when the input is the 7th example from the 8th minibatch?

a[8]{7}(3)

a[3]{8}(7)
正确

a[8]{3}(7)

a[3]{7}(8)

### 2
Which of these statements about mini-batch gradient descent do you agree with?

One iteration of mini-batch gradient descent (computing on a single mini-batch) is faster than one iteration of batch gradient descent.
正确

You should implement mini-batch gradient descent without an explicit for-loop over different mini-batches, so that the algorithm processes all mini-batches at the same time (vectorization).

Training one epoch (one pass through the training set) using mini-batch gradient descent is faster than training one epoch using batch gradient descent.

### 3
Why is the best mini-batch size usually not 1 and not m, but instead something in-between?

If the mini-batch size is m, you end up with batch gradient descent, which has to process the whole training set before making progress.
正确

If the mini-batch size is m, you end up with stochastic gradient descent, which is usually slower than mini-batch gradient descent.
未选择的是正确的

If the mini-batch size is 1, you lose the benefits of vectorization across examples in the mini-batch.
正确

If the mini-batch size is 1, you end up having to process the entire training set before making any progress.

### 4
uppose your learning algorithm’s cost J, plotted as a function of the number of iterations, looks like this:
![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/KIycr3grEeeJIwrF5BVsIg_f1c324824bd9220c7ee985cce1521404_cost.png?expiry=1511654400000&hmac=xFeGPHVDFe8oKNRaJjXtkJPe6HS6AHYTYqI2svNA3S4)

Which of the following do you agree with?
If you’re using mini-batch gradient descent, this looks acceptable. But if you’re using batch gradient descent, something is wrong.
正确

If you’re using mini-batch gradient descent, something is wrong. But if you’re using batch gradient descent, this looks acceptable.

Whether you’re using batch gradient descent or mini-batch gradient descent, this looks acceptable.

Whether you’re using batch gradient descent or mini-batch gradient descent, something is wrong.

### 5
Suppose the temperature in Casablanca over the first three days of January are the same:

Jan 1st: θ1=10oC
Jan 2nd: θ210oC
(We used Fahrenheit in lecture, so will use Celsius here in honor of the metric world.)

Say you use an exponentially weighted average with β=0.5 to track the temperature: v0=0, vt=βvt−1+(1−β)θt. If v2 is the value computed after day 2 without bias correction, and vcorrected2 is the value you compute with bias correction. What are these values? (You might be able to do this without a calculator, but you don't actually need one. Remember what is bias correction doing.)

v2=10, vcorrected2=10

v2=7.5, vcorrected2=7.5

v2=7.5, vcorrected2=10
正确

v2=10, vcorrected2=7.5

###6

Which of these is NOT a good learning rate decay scheme? Here, t is the epoch number.

α=1t√α0

α=11+2∗tα0

α=etα0
正确

α=0.95tα0

###7
You use an exponentially weighted average on the London temperature dataset. You use the following to track the temperature: vt=βvt−1+(1−β)θt. The red line below was computed using β=0.9. What would happen to your red curve as you vary β? (Check the two that apply)
![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/W0boqHgrEee6mw7xN92yoA_3a1f4052dc56969b5d7da4024a46836d_temp.png?expiry=1511654400000&hmac=iGGPhQclGN4CJx5fW1YBHyGMI-iL6BXLxaysti8jv0I)

Decreasing β will shift the red line slightly to the right.
未选择的是正确的

Increasing β will shift the red line slightly to the right.
正确
True, remember that the red line corresponds to β=0.9. In lecture we had a green line $$\beta = 0.98) that is slightly shifted to the right.

Decreasing β will create more oscillation within the red line.
正确
True, remember that the red line corresponds to β=0.9. In lecture we had a yellow line $$\beta = 0.98 that had a lot of oscillations.

Increasing β will create more oscillations within the red line.
未选择的是正确的

###8
Consider this figure:
![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fv6gungsEeeJIwrF5BVsIg_6da8c45ffcd4075de23d8e93884937f1_GD.png?expiry=1511654400000&hmac=0MNW8QFDpq5trtr7bbz0IFA6yYr83YTxf5DZd1h_PzI)
These plots were generated with gradient descent; with gradient descent with momentum (β = 0.5) and gradient descent with momentum (β = 0.9). Which curve corresponds to which algorithm?

These plots were generated with gradient descent; with gradient descent with momentum (β = 0.5) and gradient descent with momentum (β = 0.9). Which curve corresponds to which algorithm?

(1) is gradient descent. (2) is gradient descent with momentum (large β) . (3) is gradient descent with momentum (small β)
这个选项的答案不正确

(1) is gradient descent. (2) is gradient descent with momentum (small β). (3) is gradient descent with momentum (large β)

(1) is gradient descent with momentum (small β), (2) is gradient descent with momentum (small β), (3) is gradient descent

(1) is gradient descent with momentum (small β). (2) is gradient descent. (3) is gradient descent with momentum (large β)

### 9

Suppose batch gradient descent in a deep network is taking excessively long to find a value of the parameters that achieves a small value for the cost function (W[1],b[1],...,W[L],b[L]). Which of the following techniques could help find parameter values that attain a small value for? (Check all that apply)

Try tuning the learning rate α
正确

Try initializing all the weights to zero
未选择的是正确的

Try better random initialization for the weights
正确

Try mini-batch gradient descent
正确

Try using Adam
正确

### 10

Which of the following statements about Adam is False?

Adam should be used with batch gradient computations, not with mini-batches.
正确

The learning rate hyperparameter α in Adam usually needs to be tuned.

Adam combines the advantages of RMSProp and momentum

We usually use “default” values for the hyperparameters β1,β2 and ε in Adam (β1=0.9, β2=0.999, ε=10−8)


