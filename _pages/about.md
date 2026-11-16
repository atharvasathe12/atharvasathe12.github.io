---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<p class="lead">
I am a Postdoctoral Fellow at the <a href="https://energyinstitute.jhu.edu/">Ralph O'Connor Sustainable Energy Institute (ROSEI)</a> at Johns Hopkins University, where I work with Profs. <a href="https://engineering.jhu.edu/faculty/charles-meneveau/">Charles Meneveau</a> and <a href="https://engineering.jhu.edu/faculty/dennice-gayme/">Dennice Gayme</a>.
My <a href="{{ base_path }}/research/">research</a> uses large-eddy simulations (LES) to understand and model turbulent boundary layers over complex surfaces, from urban-like roughness to large wind farms.
</p>

<figure class="hero-video wide-media">
  <video src="{{ base_path }}/files/wake_eps_T15MW_eps_light_u-magma_col2-magma_12000steps_5.115deg_uref10_only-eps12_notitle_stack.mp4"
         poster="{{ base_path }}/images/wake_movie_stack_poster.jpg"
         autoplay muted loop playsinline preload="auto"
         title="Click to view full screen"
         onclick="if (this.requestFullscreen) { this.requestFullscreen(); } else if (this.webkitEnterFullscreen) { this.webkitEnterFullscreen(); }">
  </video>
  <figcaption>
    Large-eddy simulation of the IEA 15 MW reference turbine with the actuator line model.
    Top left: blade forces projected onto the LES grid, viewed from upstream.
    Top right: streamwise velocity in a cross-section 1.07 rotor diameters downstream.
    Bottom: vertical plane through the rotor, showing the wake developing downstream.
    Click the movie to view it full screen.
  </figcaption>
</figure>

At Johns Hopkins, I develop high-fidelity simulation tools for offshore wind energy.
I recently introduced analytical corrections that make the actuator line model accurate on very coarse grids, enabling blade-level predictions in simulations of entire wind-farm clusters.
I am now using this capability to extend the Johns Hopkins Turbulence Databases (JHTDB) with a large offshore wind-farm case.

I received my Ph.D. from Columbia University in 2025, advised by [Prof. Marco G. Giometto](https://www.civil.columbia.edu/content/marco-giovanni-giometto), where I studied the physics of roughness-induced secondary flows in turbulent boundary layers.
Previously, I earned a Bachelor's and Master's degree in Technology in Aerospace Engineering from IIT Bombay.
