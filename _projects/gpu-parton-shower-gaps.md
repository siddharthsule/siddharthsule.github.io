---
layout: page
title: Parton Showers on GPUs with GAPS
img: assets/img/gpu.jpg
importance: 2
permalink: /projects/gpu-parton-shower-gaps/
---

While we have been seeing exciting progress in theory, we must also prepare for a computational challenge - [studies at CERN](https://cds.cern.ch/record/2802918?ln=en) predict that compute usage is set to surpass the allocated budget in the upcoming Run 4. When studying the details, a key contribution comes from Monte Carlo Event Generators. There is also a need to address the ever-increasing compute resources required for theory and phenomenology studies using event generators.

As a possible solution, we have been looking towards GPUs for faster, more energy-efficient simulations, or at the least, an alternative to CPU clusters. Through this we have developed GAPS, a GPU Hard Process and Parton Shower Simulation Code. We designed our code to work on CPUs and GPUs, and ran benchmarks for a simple $e^+e^-$ collider. The results show that the time taken for a GPU was equivalent to 275 CPU Cores, equating to 5 times lower power consumption.

You can refer to our paper below. Our next paper and code, to simulate LHC physics is underway.

[M. H. Seymour and S. Sule, An Algorithm to Parallelise Parton Showers on a GPU, SciPost Physics Codebases 33, 2024](https://scipost.org/SciPostPhysCodeb.33)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cpugpu.jpg" title="execution time" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
