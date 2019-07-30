---
layout: post
title: "Obtaining the Response Matrix"
author: Ramiro Leal-Cavazos
rights: Public Domain
publication-date: 2019
toc:
- Potential Expansion
- Example
---

---

## Potential Expansion

Given a potential $$\Phi(\vec{x})$$ defined at points on a cubic grid of side $$L$$, we can expand into a Fourier series:

$$
  \Phi(\vec{x})=
  \frac{1}{L^3}\sum_{\vec{n}=0}^{\vec{L}-1}f_\vec{n} e^{i\vec{k}\cdot\vec{x}}
$$

where $$\vec{n}=(n_x,n_y,n_z)$$ represents the integer coordinates of each point on the cubic grid, $$\vec{L}=(L,L,L)$$, and $$\vec{k}=2\pi\vec{n}/L$$.

Now, using the plane wave expansion,

$$
  e^{i\vec{k}\cdot\vec{x}}=
  \sum_{\ell=0}^\infty (2\ell+1)i^\ell j_\ell(kx)P_\ell(\hat{k}\cdot\hat{x})
$$

we can rewrite the potential as

$$
  \Phi(\vec{x})=
  \frac{1}{L^3}\sum_{\vec{n}=0}^{\vec{L}-1}\sum_{\ell=0}^\infty
  (2\ell+1)i^\ell j_\ell(kx)P_\ell(\hat{k}\cdot\hat{x})f_\vec{n}\label{eq:phiLegendre}\tag{1}
$$

Now, as a boundary condition we have the CMB, which can be written in terms of spherical harmonics:

$$
  \Phi(\theta,\phi)=\sum_{\ell=0}^\infty\sum_{m=-\ell}^\ell a_{\ell m}Y_\ell^m(\theta,\phi)
$$

Evaluating equation (\ref{eq:phiLegendre}) at $$x=x_0$$, we can set it equal to the CMB to obtain:

$$
  \frac{1}{L^3}\sum_{\vec{n}=0}^{\vec{L}-1}\sum_{\ell=0}^\infty
  (2\ell+1)i^\ell j_\ell(kx_0)P_\ell(\hat{k}\cdot\hat{x})f_\vec{n}
  =\sum_{\ell=0}^\infty\sum_{m=-\ell}^\ell a_{\ell m}Y_\ell^m(\theta,\phi)\label{eq:legendreEqSpherical}\tag{2}
$$

Now, using the addition theorem for spherical harmonics, we can written

$$
  P_\ell(\hat{k}\cdot\hat{x})=
  \frac{4\pi}{2\ell+1}
  \sum_{m=-\ell}^\ell (Y_{\ell}^m(\hat{k}))^* Y_{\ell}^{m}(\hat{x})
$$

Plugging this into equation (\ref{eq:legendreEqSpherical}), we get

$$
  \frac{4\pi}{L^3}\sum_{\vec{n}=0}^{\vec{L}-1}\sum_{\ell=0}^\infty\sum_{m=-\ell}^\ell
  i^\ell j_\ell(kx_0)(Y_\ell^m(\theta',\phi'))^* Y_\ell^m(\theta,\phi)f_\vec{n}
  =\sum_{\ell=0}^\infty\sum_{m=-\ell}^\ell a_{\ell m}Y_\ell^m(\theta,\phi)
$$

where $$\theta',\phi'$$ are the the polar and azimuthal angles made by $$\hat{k}$$ with the vertical axis, respectively.

Using the orthogonality of spherical harmonics, we get

$$
  \frac{4\pi}{L^3}\sum_{\vec{n}=0}^{\vec{L}-1}
  i^\ell j_\ell(2\pi nx_0/L)(Y_\ell^m(\theta',\phi'))^* f_\vec{n}
  =a_{\ell m}
$$

Thus, we can write the response matrix

$$
  R_{\ell,m,n_x,n_y,n_z}=\frac{4\pi}{L^3}
  i^\ell j_\ell(2\pi nx_0/L)(Y_\ell^m(\theta',\phi'))^*
$$

such that $$a_{\ell m}=R_{\ell,m,n_x,n_y,n_z}f_{n_x,n_y,n_z}$$, where Einstein's summation convention is being used.

---

## Example
