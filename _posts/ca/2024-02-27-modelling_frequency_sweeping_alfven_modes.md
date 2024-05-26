---
layout: post
title: Modelització de modes d'Alfvén amb freqüència canviant a l'stellerator TJ-II
date: 2024-02-27
description: Descripció del meu últim article científic
tags: fusion physics
categories: physics
related_posts: false
---

_Aquest apunt l'ha escrit originalment en anglès
[Mervi Mantsinen](https://fusion.bsc.es/index.php/2024/02/27/our-new-journal-paper-in-nuclear-fusion-on-modeling-of-frequency-sweeping-alfven-modes/)_

**Les inestabilitats alfvéniques impulsades per partícules energètiques suposen un repte per al correcte
funcionament dels dispositius de fusió de confinament magnètic.** Aquests modes poden dissipar ions
ràpids que condueixen a la introducció de càrregues de calor significatives als components de plasma i a
la degradació del confinament global del plasma. Una classe d'inestabilitats d'Alfvén conegudes com a
modes propis d'Alfvén de cisalla invertida "reversed shear Alfvén eigenmodes (RSAE)" són particularment
perillosos en els dispositius on es donen les condicions perquè aquests apareguin, és a dir, amb perfils
de transformació rotacional de cisalla inversa. Les configuracions de cisalla inversa han estat d'interès
recentment per la seva millora en la qualitat del confinament magnètic. Tenint en compte això, és
necessari un estudi addicional dels RSAE.

[Els RSAE, també anomenats cascades d'Alfvén, s'han pogut observar](http://10.0.4.64/0029-5515/54/12/123002)
a [l'stellerator TJ-II](https://www.wikiwand.com/es/TJ-II) en descàrregues de plasma d'hidrogen amb
diferents configuracions magnètiques. **A la nostra recent publicació a la revista Nuclear Fusion,
simulem els esdeveniments en cascada utilitzant els codis [STELLGAP](ttps://doi.org/10.1063/1.1590316) i
[AE3D](https://doi.org/10.1063/1.3313818), i estudiem la relació entre la freqüència dels modes que
formen la cascada i el valor mínim del perfil de transformació rotacional.** Les simulacions prediuen
l'aparició d'una cascada de freqüència descendent formada per un conjunt de modes amb nombre de mode
poloidal $$m = 6$$ i número de mode toroidal $$n = -9$$ quan el valor mínim del perfil iota varia entre
aproximadament $$1.47 < \iota_{min} < 1.50$$, corroborat experimentalment. Els resultats presentats donen
suport a la utilitat de l'espectroscòpia MHD, una eina de diagnòstic per mitjà de la qual es pot fer
servir el gradient temporal de la freqüència d'una cascada d'Alfvén per determinar la variació en el
temps del perfil de transformació rotacional del plasma.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/alfven_simulation_results.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>
<div class="caption">
    Els resultats de la simulació es mostren en negre superposats amb un espectrograma experimental.
    Les barres d'error assumeixen un error de ± 10% en densitat i ± 0,005 d'error en iota.
    Reproduït a partir de la Fig 11 in A.G. Ghiozzi et al 2024 Nucl. Fusion 64 036005.
</div>

L'article complet escrit per Adriana Ghiozzi, juntament amb líder del
[grup de fusió del BSC](https://fusion.bsc.es/), Mervi Mantsinen, jo mateix i altres col·laboradors es
pot llegir (en obert) al següent enllaç:
[A.G. Ghiozzi _et al_ 2024 _Nucl. Fusion_ 64 036005](https://iopscience.iop.org/article/10.1088/1741-4326/ad1c93).
