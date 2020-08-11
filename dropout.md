# Dropout

# 0. Without Dropout

$y = WX$

# 1. Vanilla Dropout


## Training

$r \sim Ber(p)$

$V = X*r$

$y = WV$

$\mathbb{E}(y) = \mathbb{E}(WV) = W \mathbb{E}(Xr) = WX \mathbb{E}(r) = WX p$

## Test

Keep all of the nodes, for training data $X$, the predicted $y$ is $\tilde{y} = WX$

$\mathbb{E}(\tilde{y}) = WX$

To keep **the expectation of output** of trained model is identical in the training and test phrase, the keep ratio $p$ must be multiplied.

> $y = WX * p$

# 2. Inverted Dropout

## Test

To keep the test phrase without modified, $y = WX$, $\mathbb{E}(y) = WX$.

## Training

Note $p$ is the keep ratio.

Let $y = WX*r / p$, thus $\mathbb{E}(y) = WX * p / p = WX$, the expecation of the output of the model is same between training and test phrase.

Thus, 

> $y = WX * Ber(p) / p$ in the training phrase, 

> $y = WX$ in the test phrase.
