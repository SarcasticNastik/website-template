---
title: "Ml"
date: 2021-05-20T20:12:26+05:30
tags: ["ML", "DL", "Classifiers"]
---

# AML random notes

## Introduction to Machine Learning 

#### Week 
1. **[Loss functions](https://heartbeat.fritz.ai/5-regression-loss-functions-all-machine-learners-should-know-4fb140e9d4b0 "More about loss functions")**

![Losses in Regression](https://miro.medium.com/max/972/1*3MsFzl7zRZE3TihIC9JmaQ.png)

- **L1 vs L2** 

     _L1_ better for _outliers_, but _L2_ easier to solve. 
    L1 is useful when data is corrupt with outliers.
    Consider _L1 vs L2_ as _mean vs median_ (think about their minimas).
    _L1_ has constant gradient.
    
    **Cons** : 
        Cases where both give undesirable predictions.
        
- **Huber loss**
    Linear above delta, quadratic below it. ![Huber loss](https://miro.medium.com/max/1050/1*0eoiZGyddDqltzzjoyfRzA.png)
    **$\delta$** is critical hyperparameter. (Need to train it)
    Better than _L1 and L2_ as best of both worlds. Has variants for smoothening the curve.

- **Log-Cosh Loss**
    ![](https://miro.medium.com/max/872/1*hj5n5273jYX7rclO7bnfJg.png)
    Smoother than _L2_.
    `It has all the advantages of Huber loss, and it’s twice differentiable everywhere`. Why 2nd derivative? Great that you asked. It's when using Newton’s method to find the optimum as in XGBoost.
    ![](https://miro.medium.com/max/1400/1*FNxOsZLqXVZNFOxGoG9A1Q.png)
    
    **Cons** : 
    `Log-cosh loss isn’t perfect. It still suffers from the problem of gradient and hessian for very large off-target predictions being constant, therefore resulting in the absence of splits for XGBoost.` 
        Takeaway - :warning: TODO
        
- __[Quantile Loss](https://en.wikipedia.org/wiki/Quantile_regression)__
    The Elephant in the room
    :warning: TODO

- __[Focal Loss](https://medium.com/@ayodeleodubela/what-does-focal-loss-mean-for-training-neural-networks-770636f76379)__
    :warning: TODO

2. **Gradient Descent**

    ##### Optimization problem :
    $$\mathcal L(w) \rightarrow {\underset {\ w} min}\ .$$

    - [Stopping criterion](https://math.stackexchange.com/questions/1618330/stopping-criteria-for-gradient-method) :

    1. $\lVert w^t - w^{t-1}\rVert < \epsilon\quad$ where $w^t = w^{t-1} - \eta_t\nabla L(w^{t-1})\  and  \ \epsilon.$ 
