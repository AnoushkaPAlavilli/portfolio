---
layout: page
title: TinyMPC
description: model-predictive control on resource-constrained microcontrollers
importance: 1
category: work
related_publications: true
---

Model-predictive control is a powerful tool for controlling highly dynamic robotic systems
subject to complex constraints, but it is computationally demanding and often impractical on
the small, resource-constrained platforms where it would be most useful. TinyMPC is a
high-speed convex MPC solver with a low memory footprint, targeting the microcontrollers
common on small robots {% cite nguyen2024tinympc %}.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/tinympc.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
</div>
<div class="caption">
    TinyMPC running onboard a Crazyflie quadrotor.
</div>

Code is available on [GitHub](https://github.com/TinyMPC/TinyMPC), and more details are at
[tinympc.org](https://tinympc.org/).
