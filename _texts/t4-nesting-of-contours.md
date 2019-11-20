---
layout: post
title: "(UNDER CONSTRUCTION) Parametrizing CMB into a Nesting of Contours"
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

## Nesting of Contours

In order to analyze the CMB disregarding any optical effects that might come about from distortions of different projections, we will extract the intrinsic structure of it by determining the nesting of its contours.

### Projection

To do this, we will first take the CMB on a sphere, puncture it at the global maximum, and flatten the sphere onto a disk. This places the global maximum on the circumference and everything else inside. The nesting of countours is then very easy to see.

An example is given by the figure below:

{% include plotly/nesting-of-contours/simple-cmb-disk.html %}

In the figure, the red dots represent local maxima and the green dots represent local minima.

Including the circumference, there are 3 local maxima, 3 local minima, and 4 saddle points. The nesting starting from the global maximum is then

![tree]({{ site.baseurl }}/assets/nesting-of-contours/tree-simple-cmb.png){:height="250px"}

## Algorithm

For low number of extrema, one can easily create a tree characterizing the nesting of the contours by hand. However, the number of extrema grows as $$\ell ^2$$, where $$\ell$$ is the highest degree of spherical harmonics used. Therefore, the rest of this post will be devoted to explaining how to efficiently get the nesting from any CMB using image processing.

### Reducing Dimension of Problem

At first glance, it seems that the problem requires to look in two dimensions, to see if a contour is inside another or not. However, it turns out that the problem of capturing the nesting of contours can be reduced to a one dimensional problem.
