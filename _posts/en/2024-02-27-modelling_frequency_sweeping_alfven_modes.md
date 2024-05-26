---
layout: post
title: Modelling of frequency-sweeping Alfvén modes in the TJ-II stellerator
date: 2024-02-27
description: Description of my latest paper on Nuclear Fusion
tags: fusion physics
categories: physics
related_posts: false
---

_This post was originally written by
[Mervi Mantsinen](https://fusion.bsc.es/index.php/2024/02/27/our-new-journal-paper-in-nuclear-fusion-on-modeling-of-frequency-sweeping-alfven-modes/)_

**Alfvénic instabilities driven by energetic particles pose a challenge to the efficient operation of
magnetic confinement fusion devices.** These modes can dispel fast ions leading to the introduction of
significant heat loads onto plasma facing components and degradation of overall plasma confinement. One
class of Alfvénic instabilities known as reversed shear Alfvén eigenmodes (RSAEs) are of particular risk
in devices with reversed shear rotational transform profiles. Reversed shear configurations have recently
been of interest because of their enhancement to confinement quality. With this in mind, further study of
RSAEs is necessary.

[RSAEs, also called Alfvén cascades, were observed](http://10.0.4.64/0029-5515/54/12/123002) in the
[TJ-II flexible heliac](http://fusionwiki.ciemat.es/wiki/TJ-II) in hydrogen plasma discharges with
varying magnetic configurations. **In
[our recent journal publication in Nuclear Fusion](https://iopscience.iop.org/article/10.1088/1741-4326/ad1c93),
we simulate the cascade events using the [STELLGAP](ttps://doi.org/10.1063/1.1590316) and
[AE3D](https://doi.org/10.1063/1.3313818) codes and study the relationship between the frequency of the
modes that form the cascade and the minimum value of the rotational transform profile.** The simulations
predict the appearance of a cascade sweeping downward in frequency formed by a set of modes with poloidal
mode number $$m = 6$$, and toroidal mode number $$n  = – 9$$ when the minimum value of the iota profile
is varied between approximately $$1.47 < \iota_{min} < 1.50$$, which is corroborated by experiment. **The
results presented support the utility of MHD spectroscopy**, a diagnostic tool whereby the temporal
gradient of the frequency of an Alfven cascade can be used to determine the variation in time of the
plasma’s rotational transform profile.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/alfven_simulation_results.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>
<div class="caption">
    Simulation results shown in black overlaid with experimental spectrogram.
    Error bars assume ±10% error in density and ±0.005 error in iota.
    Reproduced from Fig 11 in A.G. Ghiozzi et al 2024 Nucl. Fusion 64 036005.
</div>

The full journal paper written by Adriana Ghiozzi together with the
[BSC fusion group](https://fusion.bsc.es/) leader, Mervi Mantsinen, myself and collaborators can be found
at the following link:
[A.G. Ghiozzi _et al_ 2024 _Nucl. Fusion_ 64 036005](https://iopscience.iop.org/article/10.1088/1741-4326/ad1c93).
