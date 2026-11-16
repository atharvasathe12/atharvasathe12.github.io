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
  <video src="{{ base_path }}/files/wake_eps_T15MW_eps12_notitle_uref10_short.mp4"
         poster="{{ base_path }}/images/wake_movie_poster.jpg"
         autoplay muted loop playsinline preload="auto"
         title="Click to view full screen"
         onclick="if (this.requestFullscreen) { this.requestFullscreen(); } else if (this.webkitEnterFullscreen) { this.webkitEnterFullscreen(); }">
  </video>
  <figcaption>
    Large-eddy simulation of the IEA 15 MW reference turbine with the actuator line model.
    Left: blade forces projected onto the LES grid, viewed from upstream.
    Middle: streamwise velocity in a cross-section 1.07 rotor diameters downstream.
    Right: vertical plane through the rotor, showing the wake developing downstream.
    Click the movie to view it full screen.
  </figcaption>
</figure>

At Johns Hopkins, I develop high-fidelity simulation tools for offshore wind energy.
I recently introduced analytical corrections that make the actuator line model accurate on very coarse grids, enabling blade-level predictions in simulations of entire wind-farm clusters.
I am now using this capability to extend the Johns Hopkins Turbulence Databases (JHTDB) with a large offshore wind-farm case.

I received my Ph.D. from Columbia University in 2025, advised by [Prof. Marco G. Giometto](https://www.civil.columbia.edu/content/marco-giovanni-giometto), where I studied the physics of roughness-induced secondary flows in turbulent boundary layers.
I continue to collaborate with [Prof. Marc Calaf](https://www.mech.utah.edu/directory/faculty/marc-calaf/) and [Prof. William Anderson](https://me.utdallas.edu/people/faculty/william-anderson/).
Previously, I earned a Bachelor's and Master's degree in Technology in Aerospace Engineering from IIT Bombay.

## Recent news

<ul class="news">
  <li><span class="news-date">Nov 2026</span><span>Oral presentation on coarse-grid actuator line modeling at the APS DFD Meeting in Orlando, Florida.</span></li>
  <li><span class="news-date">Oct 2026</span><span>Seminar on analytical corrections for coarse-grid actuator line simulations in the JHU Mechanical Engineering Graduate Student Seminar Series.</span></li>
  <li><span class="news-date">Summer 2026</span><span>My undergraduate mentee in the NSF-funded ROSETAS REU program received the Best Presentation Award for our wind turbine wake modeling project.</span></li>
  <li><span class="news-date">May 2026</span><span>Talks on advanced actuator line modeling and wind-farm database creation at ARROW-SEA and the CEAFM&ndash;Burgers&ndash;GWU Research Symposium.</span></li>
  <li><span class="news-date">Feb 2026</span><span>Joined Johns Hopkins University as a Postdoctoral Fellow.</span></li>
  <li><span class="news-date">2025</span><span>Paper on secondary flows over multicolumn roughness published in the <i>Journal of Fluid Mechanics</i>.</span></li>
</ul>
