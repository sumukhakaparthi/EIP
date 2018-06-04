# Assignment 1
###### 6th May, 2018
###### B.V.S.G.Suraj, Batch 7

## 1x1 Convolutions:

![1x1 Conv](https://cdn-images-1.medium.com/max/1600/1*37xcqtruaRrQRAKRSYwJBg.png)

As the name suggests, the kernel (or filter) is of dimensions 1x1xm and it is convolved with an input image consisting of m channels. We get an output image which is linear combination of various channels of input. For different kernels, different output images are produced. We call this an output image of various channels.

There are 2 things to be observed:
1. 1x1 Convolutions produce same dimensional output and we have total control on the number of channels at output. So, we can use this for dimensionality reduction.
2. Since these kernels looks at one pixel at a time (unlike 3x3 which considers even the surrounding pixel data), this process ignores the spatial correlations among the same channel.

Even 3x3 does dimensional reduction but why are we using 1x1? Well, at times we only need dimensionality reduction. So, we go with this.

Looking at it in a different way, we are assigning a weight for each channel of the input and over training, the weights are re-assigned on every iteration until the best combination is achieved.

These units are generally added after ReLU so that we get more correlation among the data. As activation functions are used after convolution, using this before an activation function will be redundant as they both are non-linear functions. Contrary, we will be learning more complex information.

## Epochs:
While training models, all of the training data is fed to the algorithm multiple times. One iteration of this process is called an epoch.

One might consider this to be redundant as the training is done on the same data. The algorithm wouldn't have absorbed all the information when the data is presented once. This is why we shuffle the data every epoch and feed it to the algorithm again and again so that it learns more and different correlation among the data. Remember, the amount of learning diminishes every epoch.

One common confusion also persists due to their similarity in their nature. In real-case scenarios, there will be multiple minimas in the error function. And a random initialization of weights biases the algorithm to move towards a particular minima. So, various iterations with random weight initializations are done. Though this is leading to a better learning, this is not called epoch.

To drive this point home, I shall use a practical observation. When we are using multiple epochs, the accuracy on the training data keeps increasing. But when weights are initialized randomly, that is not the case. Accuracy jumps randomly. Though we might get better learning, epochs is all about fine tuning.

## 10 examples of use of MathJax in Markdown:

1. $$f(x) = x^2$$
2. $$\int x dx = \frac {x^2}{2} $$
3. $$Greek \, Letters : \alpha \beta $$
4. $$ \sum_{i=0}^ni^2 = \frac {n(n+1)(2n+1)}{6}$$
5. $$ \{curly \; brackets \; need \; some \; extrawork\}$$
6. $$ \left ({\sqrt x} \right) $$
7. $$ \log_7x$$
8. $$ \prod\,\left({a+1 \over b}\right)$$
9. $$ \left(\sqrt[100] {x^2} \right)$$
10. $$ Loss\,Function = \frac{1}{m} \sum_{i=0}^m(h(\theta)-y)^2 + \lambda\sum_{i=1}^m\theta_i^2$$