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
higher logarithmic accuracy. As of 2026, several formalisms achieve
Next-to-Leading-Log (NLL) accuracy — including:

- **PanLocal** and **PanGlobal**  
  <https://gsalam.web.cern.ch/panscales/>
- **FHP** (Forshaw–Holguin–Plätzer)  
  <https://arxiv.org/abs/2605.02622>
- **Alaric**  
  <https://arxiv.org/abs/2404.14360>
- **Apollo**  
  <https://arxiv.org/abs/2403.19452>

Exploratory steps toward NNLL precision are now underway.

This project integrates the **PanGlobal** and **FHP** showers into
[Herwig](https://herwig.hepforge.org/), alongside its existing
**Catani–Seymour** shower, enabling NLL-accurate predictions within
mainstream collider simulations.

We discovered spurious low-$p_T$ effects, where these showers generated very hard, very collinear emissions, that alter the predicted particle spectra, a systematic error the field had overlooked. To understand the impact of this effect, we introduced a dynamic shower cutoff that bounds the generation to the range of the older showers.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/lp_aob.png" title="Lund Plane" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Lund Plane. The Catani–Seymour (CS) and Angular Ordered (AO) showers produce similar distributions, whereas the PanGlobal (PG0) and FHP do not. We introduce an AO-like boundary (AOB) to cut the extra region of phase space.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/prim_cl.png" title="Primary Cluster Mass" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/prim_cl_aob.png" title="Primary Cluster Mass (With AOB)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Primary Cluster Mass Spectrum for the non-AOB and AOB showers. The extra behaviour of the new showers maps exactly to this shift in the peak.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cmul.png" title="Charged Multiplicity" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cmul_aob.png" title="Charged Multiplicity (With AOB)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Charged Multiplicity spectra. Turning the AO-Like Boundary on leads to a significant improvement with respect to data.
</div>
