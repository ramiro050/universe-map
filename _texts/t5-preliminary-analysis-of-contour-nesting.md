---
layout: post
title: "Preliminary Analysis of Nesting of Contours"
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

## Making Trees

Using the method for finding the nesting of contours outlined in a previous [post]({{ site.baseurl }}/texts/t4-nesting-of-contours/), we can look at some of the effects that the phase distribution can have on the final tree.

### $$\ell=30$$ with Random Phase

Consider the following phase distribution:

{% include plotly/preliminary-analysis-of-contour-nesting/l30-random-phase-distribution.html %}

Such a distribution generates the following CMB projected onto a disk:

{% include plotly/preliminary-analysis-of-contour-nesting/l30-random-cmb.html %}

with the local maxima given by the red dots and the local minima given by the green dots.

### $$\ell=30$$ with Non-Uniform Phase

Similarly, consider a different phase distribution:

{% include plotly/preliminary-analysis-of-contour-nesting/l30-line-phase-distribution.html %}

This distribution generates the following CMB:

{% include plotly/preliminary-analysis-of-contour-nesting/l30-line-phase-cmb.html %}

### $$\ell=30$$ Trees

The two CMBs create the following trees:

![tree]({{ site.baseurl }}/assets/preliminary-analysis-of-contour-nesting/l30-trees.png){:height="700px"}

One of the differences I see between the two trees is that the uniform distribution has a smooth transition from maxima to minima as one moves from top to bottom in the tree. On the other hand, the non-uniform distribution has chunks in the tree with primarily maxima, chunks with primarily minima, and it ends with maxima at the bottom. This characteristics are preserved if one goes to lower $$\ell$$.

### $$\ell=15$$ Trees

The following are the trees generated from distributions with similar characteristics as the previous distributions, but only going up to $$\ell=15$$.

![tree]({{ site.baseurl }}/assets/preliminary-analysis-of-contour-nesting/l15-trees.png){:height="500px"}

Notice, the same things happens here. The uniform one has a uniform transition from minima to maxima, while the non-uniform has chunks of each, with a lot of maxima at the bottom.

## Future Steps

Moving forward, one way to better capture this transition from maxima to minima as one moves along the tree is to count the number of maxima and minima at every single row and plot the distribution for different trees. This will possibly lead to an easy way of capturing some differences among the trees.
