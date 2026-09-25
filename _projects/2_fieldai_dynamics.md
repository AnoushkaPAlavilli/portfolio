---
layout: page
title: Dynamics Model Learning for Skid-Steer Robots
description: physics-structured dynamics model learning and online adaptation at FieldAI
img: assets/img/publication_preview/fieldai.png
importance: 2
category: work
related_publications: true
---

During a summer internship on FieldAI's Federal Off-road Driving Team, I developed a
semi-structured dynamics model learning framework for skid-steer mobile robots. 

This work explores how physics structure and online adaptation can make learned dynamics models more robust to changing off-road conditions. We learn a low-dimensional model of unmodeled forces and adapt it online to simulated environmental disturbances including stream currents and unknown, sliding payloads. We also integrated this dynamics model with MPPI in simulation. We plan to deploy this work on hardware and extend the dynamics model to cross-embodiment applications.

This work was accepted as a poster at the IEEE IROS 2026 Workshop on Bridging Perspectives in
Navigation {% cite alavilli2026onlineadapt %}.

<p>
  <a
    href="{{ '/assets/pdf/iros26_workshop_poster_PDF.pdf' | relative_url }}"
    target="_blank"
    rel="noopener"
    style="display:inline-block;padding:0.4rem 0.9rem;border:1px solid rgba(128,128,128,0.4);border-radius:6px;text-decoration:none;"
  >
    Download Poster (PDF)
  </a>
</p>

<iframe
  src="{{ '/assets/pdf/iros26_workshop_poster_PDF.pdf' | relative_url }}"
  title="Dynamics Model Learning for Skid-Steer Robots — IROS 2026 Workshop Poster"
  style="width:100%;height:80vh;min-height:600px;border:1px solid rgba(128,128,128,0.4);border-radius:6px;"
>
</iframe>
