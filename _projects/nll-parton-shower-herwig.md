---
layout: page
title: Improving Parton Shower Physics in Herwig 7
img: assets/img/lhc.jpg
importance: 1
permalink: /projects/nll-parton-shower-herwig/
---

The next era of particle physics is rapidly approaching. With the upcoming
[High-Luminosity LHC](https://home.cern/science/accelerators/high-luminosity-lhc) and
proposals for a [Future Circular Collider](https://home.cern/science/accelerators/future-circular-collider),
experiments will deliver collision data with unprecedented precision.
Our simulation tools must match that accuracy.

While significant progress has been made in fixed-order calculations, the
event-generator and resummation communities are now pushing parton showers to
higher logarithmic accuracy. As of 2025, several formalisms achieve
Next-to-Leading-Log (NLL) accuracy — including:

- **PanLocal** and **PanGlobal**  
  <https://gsalam.web.cern.ch/panscales/>
- **FHP** (Forshaw–Holguin–Plätzer)  
  <https://arxiv.org/abs/2003.06400>
- **Alaric**  
  <https://arxiv.org/abs/2404.14360>
- **Apollo**  
  <https://arxiv.org/abs/2403.19452>

— with exploratory steps toward NNLL precision.

This project integrates the **PanGlobal** and **FHP** showers into
[Herwig](https://herwig.hepforge.org/), alongside its existing
**Catani–Seymour** shower, enabling NLL-accurate predictions within
mainstream collider simulations.

Preliminary results are shown below. More details will be added once our
publication is released. In the meantime, please see my recent presentation:

📌 [NLL Showers in Herwig – LHC Monte Carlo Working Group (Oct 2025)](https://indico.cern.ch/event/1553687/contributions/6702923/)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/thr.jpg" title="Thrust" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/y23.jpg" title="Durham y23" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Thrust and the Durham $y_{23}$ Observables. Made from LEP Simulations at NLO with cluster hadronisation.
</div>
