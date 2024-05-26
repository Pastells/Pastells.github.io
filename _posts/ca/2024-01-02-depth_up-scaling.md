---
layout: post
title: Depth Up-Scaling
date: 2024-01-02
description: Explicació del mètode "Depth Up-Scaling"
tags: LLMs ML
categories: ML
related_posts: false
---

L'article de [SOLAR10.7B](https://arxiv.org/abs/2312.15166) introdueix l'augment
de profunditat "Depth Up-Scaling" (DUS) com a competència a la mescla d'experts "mixture-of-experts" (MoE). Es basa en una idea senzilla: agafar un
model existent, duplicar-li les capes i preentrenar-lo contínuament "continued
pretraining" perquè doni millors resultats. El problema rau en la concatenació
de l'última capa del model original amb la primera capa del seu duplicat. Per
facilitar l'entrenament continuat del model resultant, els autors eliminen les
$$m$$ capes finals del model original i les $$m$$ capes inicials de la còpia.
Mitjançant aquesta tècnica, després de la concatenació, el model pateix una
caiguda de rendiment inicial, però es recupera ràpidament durant la fase
continuada de preentrenament.

Tot i que els autors no ho diuen, eliminar les capes inicials i finals té sentit
des del punt de vista de la interpretabilitat mecanicista "mechanistic
interpretability" (vegeu el fil
[d'Anthropic sobre "transformer circuits"](https://transformer-circuits.pub/2021/framework/index.html)),
atès que la primera i la darrera capa tenen tasques especialitzades.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/DUS.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

Els autors utilitzen Mistal 7B, amb una arquitectura Llama 2 de 32 capes, com a
model base. Prenen $$m=8$$, de manera que el model resultant té $$2*(32-8)=48$$
capes. No proven altres opcions per $$m$$, així que ben segur apareixeran
millores del mètode en un futur pròxim.

Nous Research ja ha entrenat un model
[Hermes 2 a sobre de SOLAR10.7B](https://huggingface.co/NousResearch/Nous-Hermes-2-SOLAR-10.7B),
i sembla que funciona molt bé.
