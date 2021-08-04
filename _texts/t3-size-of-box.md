---
layout: post
title: "Effects of Size of the Box on Map"
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

## Why this is Important

When recovering the potential, it is important that the features we see in it are not dependent on the size of the box or the orientation of the box with respect to the CMB, for we want the potential features to be as much as possible dependent only on the CMB.

Therefore, this post will be dedicated to looking at the different effects that changing the properties of the box or of the CMB size can have on the final outcome. Furthermore, different ways that one could optimize for the size of the box are explored.

---

## Fake CMB

In order to analyze the behavior of the potential retrieved relative to the size and orientation of the box, we first need to create a fake CMB. For this post, the CMB generated by the spherical harmonic coefficients:

$$a_{2\ \pm 2}=10,\quad a_{1\ 0}=20,\quad a_{3\ \pm 1}=\pm 10,\quad a_{6\ 0}=20$$

was used.

Note that the coefficients are chosen in such a way that the sum of complex spherical harmonics results in a real CMB.

This particular CMB looks as follows:

{% include plotly/size-of-box/fake-cmb.html %}

---

## Varying Box Size and CMB Radius

One of the ways that we can make sure that the potential recovered is a good approximation for the potential with such a CMB is by looking at the CMB recovered from that potential. By comparing at each point by how much it differs from the original CMB, we can get a feeling for how good the procedure is working.

In this procedure, the size of the box represents the space in discrete Fourier space that is being recovered from the CMB. However, the potential recovered also depends on the radius of the CMB sphere inside the box.

In the following plot, we can see the effect that varying the size of the box and the radius of the CMB has on the recovered potential.

{% include plotly/size-of-box/cmb-change-vs-cmb-radius.html %}

Notice that all the curves follow a similar pattern of being high in the beginning, then rapidly decreasing when the CMB radius is around a fifth of the box size. We can also see that for this particular CMB, the size of the box that improved the most was $$L=5$$.

---

## What Happens During the Drop?

Let's now look a little closer at the drop in the plot above. In particular, lets look at what the potential looks like for $$L=5$$ when the radius of the CMB (as a fraction of the box size) varies in the range $$[0.083, 0.312]$$.

{% include plotly/size-of-box/potential-with-varying-cmb-radius.html %}
 <br/>

Notice that the potential varies widely in structure. Moreover, at around $$r=0.3$$, the equipotential surfaces becomes very close to the CMB sphere. As we will see, this has to do with the fact that for those values of radii, the minimum and maximum of the recovered potential are very large in magnitude.

---

## Minimum and Maximum of Potential

In the following plot, we can see the minimum and maximum of the recovered potential as a function of the radius of the CMB sphere. For reference, the CMB min and max is also included.

{% include plotly/size-of-box/potential-min-max-vs-cmb-radius.html %}

Since there is no reason why the CMB should be a minimum in magnitude for all of space, then we can use this to optimize the radius of the CMB sphere relative to the box.

An interesting property is that the min and max of the potential varies less and less as the box size increase, and it approaches the min and max of the CMB.

**Note:** The plot for the other sized boxes can be made visible by clicking on their respective legend element in the plot.

---