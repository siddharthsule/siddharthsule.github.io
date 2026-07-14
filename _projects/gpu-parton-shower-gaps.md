---
layout: page
title: Parton Showers on GPUs with GAPS
img: assets/img/gpu.jpg
importance: 2
permalink: /projects/gpu-parton-shower-gaps/
---

Upcoming LHC runs will not only push experimental precision — they will also
push computing demands to new limits. Recent [CERN studies](https://cds.cern.ch/record/2802918?ln=en)
indicate that simulation workloads are set to exceed the computing budget for
Run 4. Monte Carlo event generators are one of the largest contributors to
this increase, both for experimental and theoretical needs.

To address this challenge, we are exploring GPU acceleration for fast and
energy-efficient event simulation. Our goal is to provide a practical
alternative to CPU clusters while maintaining physics fidelity.

This effort has led to **GAPS**: a GPU-accelerated hard process and parton
shower event generator. GAPS supports both CPU and GPU execution and has been
benchmarked on LEP- and LHC-like simulations. We have demonstrated that a single modern GPU can simulate **1,000,000 events**
with **comparable throughput and lower energy consumption** than multi-node
CPU clusters.

More details can be found in our publications:

📄 **Publications**

- M. H. Seymour & S. Sule, *An Algorithm to Parallelise Parton Showers on a GPU*,  
  *SciPost Physics Codebases* **33** (2024)  
  <https://scipost.org/SciPostPhysCodeb.33>

- M. H. Seymour & S. Sule, *An NLO-Matched Initial and Final State Parton Shower on a GPU*,  
  *arXiv:2511.19633* (2025)  
  <https://arxiv.org/abs/2511.19633>

💻 **Code**

- **GAPS** — GPU-Amplified Parton Shower  
  <https://gitlab.com/siddharthsule/gaps>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cpugpu.png" title="execution time" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
