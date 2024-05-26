---
layout: post
title: Depth Up-Scaling
date: 2024-01-02
description: Explainer of the Depth Up-Scaling method
tags: LLMs ML
categories: ML
related_posts: false
---

The [SOLAR10.7B](https://arxiv.org/abs/2312.15166) paper introduces Depth
Up-Scaling (DUS) as a competitor to mixture-of-experts (MoE). It is based on a simple idea: take an existing model, double its layers, and
continuously pretrain it so it gives better results. The problem lays in the
concatenation of the last layer of the original model with the first layer of
its duplicate. The "layer distance" is greater than 1 at the seam where the two
models meet. To make it easier for the resulting model to be continuously
pretrained, the authors remove the final $$m$$ layers of the original model and
the initial $$m$$ layers of the duplicate. Using this techinque, after the
concatenation, the model suffers an initial performance drop, but rapidly
recovers during the coninued pretraining phase.

Although the authors don't mention it, removing the inital and final layers
makes sense from a mechanistic interpretability point of view (see the
[transformer circuits thread from Anthropic](https://transformer-circuits.pub/2021/framework/index.html)),
given that the first and final layers have specialized tasks.

<div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/DUS.png" class="img-fluid rounded z-depth-1" zoomable=true %}
</div>

The authors use Mistal 7B, with a 32-layer Llama 2 architecture, as their base
model. They take $$m=8$$, so that the resulting model has $$2*(32-8)=48$$ layers.
They do not try other options for $m$, so there surely will be improvements to
the method in the near future.

Nous Research has already trained a
[Hermes 2 model on top of SOLAR10.7B](https://huggingface.co/NousResearch/Nous-Hermes-2-SOLAR-10.7B),
and it seems to work really well.
