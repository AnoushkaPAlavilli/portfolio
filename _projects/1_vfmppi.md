---
layout: page
title: Value-Guided MPPI for Off-Road Navigation
description: hierarchical RL-MPPI for high-speed autonomous off-road driving
img: assets/img/publication_preview/IMG_1948.jpg
importance: 1
category: work
related_publications: true
---

Safe, high-speed autonomous driving over unstructured off-road terrain is difficult: terrain
geometrics like steep slopes can cause unsafe driving conditions, and building accurate,
explicit cost maps of the terrain is expensive. This work develops a hierarchical framework in which we use MPPI as a high-level waypoint path planner and an RL policy as a low-level controller to track these waypoints. We include the RL policy's value function as an execution-aware planning cost inside Model
Predictive Path Integral (MPPI) control, enabling bidirectional feedback between planning and
control without explicit terrain cost maps {% cite alavilli2026vfmppi %}.

We evaluate our results in the [BeamNG](https://beamng.tech/) simulator, demonstrating
86% navigation success versus 55% for baseline MPPI across unseen off-road evaluation tasks,
while substantially reducing vehicle jerk, acceleration, pitch, and roll. We also use online adaptation to update the value function with driving experience.

This work was accepted as a **full paper with oral presentation** at IEEE IROS 2026. Arxiv link coming soon!

Since publishing this work, we have deployed the algorithm on a full-size Yamaha ATV in
collaboration with the [Airlab](https://theairlab.org/) at CMU. Stayed tuned for sim-to-real work on this!

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/drone_footage_vf_mppi.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="assets/video/atv_deployment.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
</div>
<div class="caption">
    Drone footage of the Yamaha Viking ATV running the hierarchical RL-MPPI control in off-road terrain.
</div>


<p>
  <a
    href="{{ '/assets/pdf/iros26_poster_vf_guided_mppi_PDF.pdf' | relative_url }}"
    target="_blank"
    rel="noopener"
    style="display:inline-block;padding:0.4rem 0.9rem;border:1px solid rgba(128,128,128,0.4);border-radius:6px;text-decoration:none;"
  >
    Download Poster (PDF)
  </a>
</p>

<iframe
  src="{{ '/assets/pdf/iros26_poster_vf_guided_mppi_PDF.pdf' | relative_url }}"
  title="Value-Guided MPPI — IROS 2026 Poster"
  style="width:100%;height:80vh;min-height:600px;border:1px solid rgba(128,128,128,0.4);border-radius:6px;"
>
</iframe>
