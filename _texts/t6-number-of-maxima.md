---
layout: post
title: "On the Number of Extrema of Spherical Harmonics"
author: Ramiro Leal-Cavazos
rights: Public Domain
publication-date: 2019
---

---

## Contents
{:.no_toc}

* ToC
{:toc}

---

## Counting Extrema

An interesting problem that could lead to a different way of analyzing the CMB is looking at how the number of extrema of the spherical harmonics depend on their phase distribution.

Using random uniform distribution for the phases and a $$\ell^{\beta}$$ distribution for the power spectrum, I calculated the number of maxima found all the way up to $$\ell=85$$. As can be seen in the figure below:

{% include plotly/number-of-maxima/number-of-maxima-vs-ell.html %}

As we can see, for three of the four exponents evaluated, the number of maxima for high $$\ell$$ goes as some power of $$\ell$$.

To calculate the power of $$\ell$$, I started with the first 20 data points of each line and calculated the slope of their best fit line. I Then moved the interval of 20 points forward until $$\ell = 85 - 20=65$$, and calculated the slope of the best fit line at each point. The value of the slopes is given by the figure below:

{% include plotly/number-of-maxima/slopes-vs-ell.html %}

As we can see, the first two curves become proportional rather quickly to $$\ell^2$$, in agreement with the [analysis](https://rdcu.be/bXe3X) made by Cammarota and Marinucci. The curve with $$\beta=-2$$ takes longer, but it seems to be headed in the same direction. Increasing the value of $$\ell_\text{max}$$ will be needed to make any conclusions on this curve. Lastly, for $$\beta=-3$$, there are almost no new extrema appearing as $$\ell$$ increases.

## Future Steps

The next step is to see how the result of $$\ell^2$$ changes as the distribution of phases also changes. We can clearly see that distribution does have an effect on the outcome from the curves above, but a closer analysis is still needed.

### On Higher $$\ell$$

The original calculation was supposed to go all the way to $$\ell =120$$, however for some reason that is still undetermined, the calculation stopped counting extrema at $$\ell=85$$. This is the reason that in the plot above for number of maxima, the curves suddenly drop at the end.

It must also be noted that this calculation is very computationally expensive, for the number of functions needed to be evaluated goes as $$\ell^2$$. For this results, the calculation took a total of 4 hours and 40 minutes. Thus, in order to go to higher $$\ell$$, a better algorithm for evaluating spherical harmonics must be used.
