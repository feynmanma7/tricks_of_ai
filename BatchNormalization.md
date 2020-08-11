# BatchNormaliztion

For a mini-batch,  for each dimension of $X$, 

count (MLE) for $\mu$  and $\sigma^2$ of current mini-batch,

> $\mu = \frac{1}{N}\sum_{i=1}^N x_i$

> $\sigma^2 = \frac{1}{N}(x_i - \mu)^2$



Then, $\hat{x_i}=\frac{x_i-\mu}{\sqrt{\sigma^2+\epsilon}}$

Compute $y_i$ using **learned parameters** $\gamma$ and $\beta$, 

> $y_i = \gamma \hat{x_i} + \beta$

