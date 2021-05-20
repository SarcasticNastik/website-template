---
title: "Pnc"
date: 2021-05-20T19:05:35+05:30
draft: true
---
# A First Course In Probability

<h6 style='text-align: right;'> By <a href="http://93.174.95.29/main/D3E81CBEAEC2AED78B2D9E489B59EAFC"> Sheldon M. Ross </a> </h6> 

###### tags: `Mathematics` `Probability`

## Chapter 1, 2, 3 - Basic stuff

###### :memo: Theoretical Takeaways
- Considering question 80, if a particular formulation gets stuck again, try to backtrack if the paradigm seems correct. Try to find different approaches for finding the same answer :wink:. 
- Considering the _Conditional Probability_, keep in mind to first cascade the conditional probability i.e. consider every sub-event to create sub-linear dependencies. Go on proving afterwards whether the events are independent or not. 
- __Gamblers Ruin__
    Consider $A$ and $B$ plays a game where they exchange 1 unit money, if they initially have `a` and `b` units respectively. This is purely analogous to a `RANDOM WALK`. Consider a line segment $[0, N]$, then the case when $A$ wins is analogous to the the walk ending in `N` and similarly for $B$. :astonished: 
`Does the game end?`
Adding the probabilities, we get answer as `1`.
- __Indicator Variables__ Random variables which have value $!$ for success of an event, and $0$ otherwise. Note that $E[I] = P(A)\ .$ Compositions of these Indicator Variables for each of the iteration is $X$, the random variable for such a distribution.

## Chapter 4 - Random Variables and their basic postulates

###### :memo: Theoretical Takeaways

- Go with the intuition. Think clearly about the formula (esp. regarding the **Expectancy** of the **Random Variables**), and try to formulate your intuition better.
- Suppose that you can't formalise an equality, try to think of other formulations. For example, try to prove the formulation for an inequality, and then use it to derive the result :astonished:.
- Refer to pg. 148 for the fact that **mathematical rigor should always be maintained** and it should not hinder your ability to think further. Thinking of the same problem with one formualtion might be tough, but considering a _not so dissimilar_ formulation might **really** work out.

###### :memo: Formal Theory

- For a random variable ${X}$, the function  ${F}$ defined as  $$ F(x) = P\\{X \leqslant x\\} \qquad \forall \ \ x \in \left( -\infty, \infty  \right) $$ 
    is called the **Cumulative Distribution Function**, as the function suggests.

- **Probability Mass function** for a discrete random variable is discrete :stuck_out_tongue:.

-  Let $X$ be a _random variable_ having a probability mass function ${p(x)}$. The **expectation** or the expected value of the random variable ${X}$ is defined as $$E\[X\] = \sum_{x:p(x) \gt 0} xp(x)$$ Looking closely, it corresponds to the _weighted average_ of the values which the random variable takes. If you are a physicist, think of it as the experiment for finding the _centre of mass_ of the object.

- :spiral_note_pad: **Important**: $E[X^2] \ne {E[X]}^2\ .$

- **Proposition:** 
    If $X$ is a random variable taking value ${a_i}$ with probability ${p(a_i)}$, then for any real-valued function ${g}$, $$E[g[X]] = \sum_i{g(x_i)p(x_i)} $$

- Expectancy is a **linear function**, i.e. $$ E\[aX + b\]=aE[X]+b $$

- The quantity defined as $$E[X^n]=\sum_{x:p(x)>0} x^np(x)$$ is called the **nth moment of X**. This also means that **mean** of $X$ is the **first moment of X**.

- If $X$ is a random variable with mean $\mu$, then the **variance** of $X$ is defined by $$Var[X]=E[(X-\mu^2)] =  E[X^2]-E[X]^2\ . $$
- :spiral_note_pad: $Var[X]$ is **not** a linear function. Rather, it varies as $$Var[aX+b]=a^2Var[X]\ .$$

### Bernoulli and Binomial Random Variables

The *Bernoulli random variable* exists for a binary situation (win/loss). Let the probability of an event be $p$ and that of its complimentary event be $1-p$. Then, the **probability mass function** of a binomial random variable is given as $$p(i)={n \choose i}p^i(1-p)^{n-i}\ .$$
- **Property:** $$E[X^k]=npE[(Y + 1)^{k - 1}]$$ where $Y$ is a random variable with the parameters $(n-1, p)$ .

    - **Corollary :**  $$E[X]=np$$ $$Var[X]=np(1-p)$$

- **Proposition :** 
    If $X$ is a binomial random variable with parameters $(n, p)$, where ${0 < p < 1}$, then as $k$ goes from $0$ to $n$, $P\{X = k\}$ first increases monotonically and then decreases monotonically, reaching its largest value when $k$ is the largest integer less than or equal to $(n + 1)p$, i.e. $$k=\sup\{k \in \Bbb W : k \le (n+1)p\}\ .$$

### Poisson Random Variable
A random variable $X$ taking values $i \in \Bbb W$ is **Poisson Random Variable** with the _parameter $\lambda$_, for some $\lambda > 0$, such that $$p(i)=P[X=i]=e^{-\lambda}{\frac{\lambda^i}{i!}}\ .$$
If there are $n$ independent binomial trials, when $n$ is large and $p$ is sufficiently small, the _number of successes occuring_ is approximately $\lambda=np$.
- **Property :** The $Variance$ aned $Expected\ Value$ of a Poisson Random Variable both equal to $\lambda$.
Poisson's paradigm is also applicable in scenarios of _weak independence_( Refer to [Random Doubts](/@wVzILbm9Q8W2digM93fHAA/HyG_se-oL)).

$\mathbf {Poisson's\ Paradigm}$ :
Consider $n$ events, with $p_i$ probability that event $i$ occurs, $\forall\ i = 1, \dots,  n .$ If the $p_i$ are sufficiently small, and the trials are independent or at most weakly dependent, then the number of these events that occur have a Poisson distribution with mean $\sum_{i=1}^np_i$.
If having difficulty in realising this distribution, just consider this as a continuous function having known discrete values, which have already benn studied.
For choosing a $\lambda$ for Poisson distribution, consider it as mean of probabilities for the event occuring as such.

:warning: **Maintain rigor for as to each and every step of the proof of reasoning**.

**Using Poisson's paradigm**
> First check what the question demands for (the variables, the constants and all).
> 

<!-- Complete notes for chapter 4 when free  -->
<!-- Question regarding The replacement of ball, with the same ball being replaced. Write down the observations. -->
---

## Chapter 5

<!-- TODO -->

### Independent Random Variables

$$P\{X \in A, Y \in B\} = P\{X \in A\}P\{Y \in B\}$$ for sets of real numbers $A$ and $B$, i.e. Events $E_a = {X \in A}$ and resp. should be independent.
Given equation is equivalent to $$P\{X \le a, Y \le b\} = P\{X \le a\}P\{Y \le b\}$$ for all $a, b$.
Also, independence $\implies F(a, b) = F_x(a)F_y(b)\qquad \forall\ a, b.$ For discrete, change accordingly.
For _jointly continuous case_, $f(x, y) = f(x)f(y)\qquad \forall\ x, y.$

<!-- TODO --> [Coupon's Collector Problem](http://mat.uab.cat/matmat_antiga/PDFv2014/v2014n02.pdf)
[Covariance and Correlation](https://web.stanford.edu/class/archive/cs/cs109/cs109.1178/lectureHandouts/150-covariance.pdf)

[Moment Generating Functions](https://bookdown.org/probability/beta/moment-generating-functions.html)

[Poisson Process MIT](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-262-discrete-stochastic-processes-spring-2011/course-notes/MIT6_262S11_chap02.pdf)

[Poisson Process CMU (Formal)](https://www.stat.cmu.edu/~genovese/class/iprob-S06/notes/handoutN.pdf)

[Poisson Process CMU (More Formal)](https://www.stat.cmu.edu/~genovese/class/iprob-S06/notes/handout7.pdf)

[MCMC](https://www.cc.gatech.edu/~vigoda/MCMC_Course/)

[Monte-Carlo State space](http://www.columbia.edu/~ks20/stochastic-I/stochastic-I-MCII.pdf)

[
