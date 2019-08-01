---
layout: post
title: "Recovering Potential from Fake CMB"
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

## Generating a Fake CMB

In the following CMBs, we will choose coefficients such that their magnitude decays as a power law and their phases vary uniformly in the range 0 to $$2\pi$$.

### Power Spectrum

The power spectrum of spherical harmonics is defined as:

$$S(\ell)=\frac{1}{2\ell+1}\sum_{m=-\ell}^\ell |a_{\ell m}|^2$$

Since we will model the power spectrum as a power law, then

$$S(\ell)=\alpha \ell^\beta$$

In particular, this means we can get the magnitude squared of the coefficients from a Gaussian distribution with mean $$S(\ell)$$.

### Imposing the Real Condition

Since the CMB is a real valued function, then we need to impose a condition on the coefficients of the spherical harmonic expansion so that their sum is real. Since

$$(-1)^m Y_{\ell}^{m*} = Y_\ell^{-m}$$

then if

$$(-1)^m a_{\ell m}^* =  a_{\ell\ -m}\\\implies (a_{\ell m}Y_{\ell}^m)^* = a_{\ell\ -m}Y_{\ell}^{-m}$$

Summing over $$m$$ will then lead to a real result.

{% include plotly/recovering-potential/phase-distribution.html %}

---

{% include plotly/recovering-potential/fake-cmb.html %}

---

## Recovering Potential

For the next part of this post, we will assume that there is no covariance in the CMB. The covariance will be included at later point.

Using the fact that

$$f_n= A^{-1}_{nn'}B_{n'}$$

where

$$A_{nn'}=R^* _ {ny}R_{yn'}+C^{-1}_{nn'}$$

and

$$B_{n'}=R_{n'y}a_{y'}$$

we can determine the $$f_n$$ values.

{% include plotly/recovering-potential/recovered-potential.html %}

---

## Recovered CMB

We can now use the response matrix and the recovered Fourier coefficients to extract the coefficients $$a_{\ell m}$$. Then, evaluating

$$\Phi(\vec{x}=1)=\sum_{\ell}\sum_{m=-\ell}^\ell a_{\ell m}Y_\ell^m$$

we can get the recovered CMB.

{% include plotly/recovering-potential/cmb-comparison.html %}

Notice that the procedure did a good job at preserving the CMB features.

---
