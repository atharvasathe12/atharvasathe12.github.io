---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /research
---

{% include base_path %}

<!-- ===================================================================== -->
<!-- 1. ACTUATOR LINE MODEL                                                  -->
<!-- ===================================================================== -->
<div class="research-card" id="alm">
  <span class="research-number">Project 1 &middot; Postdoctoral research</span>
  <h2>Analytical corrections for coarse-grid actuator line simulations</h2>
  <p class="research-meta">
    <strong>Mentors:</strong> <a href="https://engineering.jhu.edu/faculty/charles-meneveau/">Prof. Charles Meneveau</a>, <a href="https://engineering.jhu.edu/faculty/dennice-gayme/">Prof. Dennice Gayme</a><br>
    <strong>Presented at:</strong> APS DFD 2026, ARROW-SEA 2026, CEAFM&ndash;Burgers&ndash;GWU Symposium 2026, JHU Mechanical Engineering Seminar Series 2026
  </p>
  <div class="badges">
    <span class="badge badge--new">Manuscript in preparation &middot; Wind Energy Science</span>
  </div>

  <h3>Overview</h3>
  <p>
    The actuator line model (ALM), introduced by Sørensen and Shen (<i>J. Fluids Eng.</i>, 2002), brings blade-level aerodynamics to large-eddy simulations (LES) of wind-turbine flows at a fraction of the cost of blade-resolved computations.
    Its accuracy, however, has long been known to depend strongly on the width of the Gaussian kernel used to project the blade forces onto the grid.
  </p>
  <p>
    On the coarse grids necessary for large-scale wind-farm simulations, the larger kernel widths required for numerical stability over-diffuse the trailed vorticity, weakening the induced velocity and leading to overpredicted blade loads and power (figure&nbsp;1).
    Wide kernels also smear the loads along the span and project a significant fraction of the force outside the rotor radius, distorting the force distribution applied to the flow and increasing the effective rotor diameter.
  </p>

  <figure class="research-fig">
    <a href="{{ base_path }}/images/nearwake_uniform_res_Q0.2_rain.png"><img src="{{ base_path }}/images/alm_nearwake_vorticity_web.png" alt="Wake vortex structure of a wind turbine at three grid resolutions" loading="lazy"></a>
    <figcaption>
      <strong>Figure 1.</strong> Wake vortex structure behind a wind turbine at three grid resolutions, with the kernel width set to twice the grid spacing (&epsilon; = 2&Delta;).
      Isosurfaces of the Q-criterion at Q&thinsp;(D/U<sub>&infin;</sub>)<sup>2</sup> = 0.2 are coloured by vorticity magnitude.
      On the finest grid (c), the helical tip vortices are sharply resolved.
      As the grid coarsens, the wider kernel over-diffuses the trailed vorticity, and on the coarsest grid (a) only a weak, smeared ring remains.
      This weaker vorticity underpredicts the induced velocity, so the uncorrected ALM overpredicts blade loads and power.
    </figcaption>
  </figure>

  <p>
    To address these deficiencies, we introduce the <strong>filtered annulus-momentum (FAM) correction</strong>, which accounts for the smeared and spilled loading and complements the filtered lifting-line (FLL) correction (Martínez-Tossas et al., <i>Wind Energy</i>, 2024) for the trailed vorticity.
    The combined corrections are assessed for the NREL 5 MW, DTU 10 MW, IEA 15 MW and IEA 22 MW reference turbines at resolutions from 3 to 30 LES grid points per blade.
  </p>

  <div class="stat-grid">
    <div class="stat"><span class="stat-value">&lt;1%</span><span class="stat-label">power error versus blade-element momentum theory</span></div>
    <div class="stat"><span class="stat-value">&lt;0.4%</span><span class="stat-label">power change from 3 to 30 points per blade (&gt;15% uncorrected)</span></div>
    <div class="stat"><span class="stat-value">3</span><span class="stat-label">LES grid points per blade suffice</span></div>
    <div class="stat"><span class="stat-value">&lt;0.5%</span><span class="stat-label">added cost per time step</span></div>
  </div>

  <h3>Highlights</h3>
  <ol>
    <li><strong>Resolution-independent predictions.</strong> Without any turbine-specific adjustment, the predictions for all four turbines become essentially independent of resolution, with the power varying by less than 0.4% from 3 to 30 grid points per blade, compared with more than 15% for the uncorrected ALM.</li>
    <li><strong>Power within 1%</strong> of the reference blade-element momentum (BEM) predictions for all four turbines, including on the coarsest grid.</li>
    <li><strong>Radial load distributions</strong> along the blade are equally accurate.</li>
    <li><strong>Accurate on very coarse grids</strong>, with as few as 3 LES grid points per blade.</li>
    <li><strong>No parameter tuning required.</strong> The same corrections apply to every turbine and grid.</li>
    <li><strong>Negligible cost</strong>, under 0.5% of the computational time per step in a typical pseudospectral LES solver.</li>
  </ol>

  <figure class="research-fig">
    <a href="{{ base_path }}/images/power_forces_combined_15MW_prod.pdf"><img src="{{ base_path }}/images/alm_power_loads_web.png" alt="Power and blade loads with the FAM and FLL corrections" loading="lazy"></a>
    <figcaption>
      <strong>Figure 2.</strong> (a) Mean power with the FAM and FLL corrections, normalized by the BEM prediction, for four reference turbines at resolutions from 3 to 30 grid points per blade. All cases stay within &plusmn;1% of BEM.
      (b, c) Axial and tangential force distributions along the blade of the IEA 15 MW turbine at every resolution, compared with the BEM reference and the uncorrected ALM.
    </figcaption>
  </figure>

  <p>
    By largely removing the sensitivity of the ALM to the kernel width, the FAM and FLL corrections together enable accurate blade-level predictions on grids with as few as 3 LES grid points per blade, making them well suited to large-scale wind-farm simulations.
    I am now using this capability to extend the Johns Hopkins Turbulence Databases (JHTDB) with a large offshore wind-farm case, which will capture blade-level data for every turbine along with a 60 km region downstream of the farms to study farm-scale wake interactions.
  </p>
</div>

<!-- ===================================================================== -->
<!-- 2. NUMERICAL DOMAIN                                                     -->
<!-- ===================================================================== -->
<div class="research-card" id="domain">
  <span class="research-number">Project 2 &middot; Ph.D. research</span>
  <h2>Impact of the numerical domain on turbulent flow statistics: scalings and considerations for canopy flows</h2>
  <p class="research-meta">
    <strong>Advisor:</strong> <a href="https://www.civil.columbia.edu/content/marco-giovanni-giometto">Prof. Marco G. Giometto</a><br>
    <strong>Presented at:</strong> APS DFD 2023, AGU Fall Meetings 2022 and 2023
  </p>
  <div class="badges">
    <a class="badge badge--done" href="https://doi.org/10.1017/jfm.2023.1041">Published in the Journal of Fluid Mechanics (2024)</a>
  </div>

  <h3>Overview</h3>
  <p>
    Large Eddy Simulations (LES) are widely used to study the effects of surface morphology on turbulence statistics, exchange processes, and turbulence topology in urban canopies. However, as LES are only approximations of reality, special attention is needed for the computational model setup to ensure an accurate representation of the physical processes of interest. This study shows that the choice of the numerical domain can significantly impact the accuracy of turbulent flow statistics, potentially causing a mismatch between numerical studies and experimental data.
  </p>

  <h3>Highlights</h3>
  <ol>
    <li>Demonstrated that a narrow domain (width/height &lt;&lt; 3.0) may be insufficient to accommodate both fast and slow turbulent streaks, leading to the artificial disruption of turbulent coherence. This results in an underprediction of second-order statistics.</li>
    <li>Showed that a short domain (length/height &lt;&lt; 6.0) may artificially enhance turbulent coherence due to excessive periodization, which leads to an overprediction of second-order statistics.</li>
    <li>Proved that the widely used conventional method for testing the impact of scale separation in canopy flow simulations contains significant flaws, especially in the presence of roughness-induced secondary flows, and proposed a novel alternative method that isolates the impact of scale separation with greater accuracy.</li>
    <li>Showed, using the aforementioned method, that domains with small scale separation may dampen turbulent fluctuations in the outer layer due to their close proximity to the upper boundary.</li>
    <li>Established that scale separation is not the sole parameter governing the existence of an inertial sublayer in the atmosphere; the underlying arrangement of canopy elements also plays a significant role, a fact previously unknown in the literature.</li>
  </ol>

  <figure class="research-fig">
    <img src="{{ base_path }}/images/fig5-1%202.png" alt="Artificial disruption of turbulent coherence due to a narrow domain" style="max-width: 715px;" loading="lazy">
    <figcaption><strong>Figure.</strong> Artificial disruption of turbulent coherence due to narrow domain (highlight #1).</figcaption>
  </figure>
</div>

<!-- ===================================================================== -->
<!-- 3. SECONDARY FLOWS OVER MULTICOLUMN ROUGHNESS                           -->
<!-- ===================================================================== -->
<div class="research-card" id="secondary-flows">
  <span class="research-number">Project 3 &middot; Ph.D. research</span>
  <h2>On the structure and dynamics of secondary flows over multicolumn roughness in channel flow</h2>
  <p class="research-meta">
    <strong>Advisor:</strong> <a href="https://www.civil.columbia.edu/content/marco-giovanni-giometto">Prof. Marco G. Giometto</a><br>
    <strong>Collaborators:</strong> <a href="https://me.utdallas.edu/people/faculty/william-anderson/">Prof. William Anderson</a>, <a href="https://www.mech.utah.edu/directory/faculty/marc-calaf/">Prof. Marc Calaf</a><br>
    <strong>Presented at:</strong> APS DFD 2024 and 2025, AGU Fall Meeting 2024
  </p>
  <div class="badges">
    <a class="badge badge--done" href="https://doi.org/10.1017/jfm.2025.10965">Published in the Journal of Fluid Mechanics (2025)</a>
  </div>

  <h3>Overview</h3>
  <p>
    This research seeks to examine the parameters of roughness configurations that are crucial in determining the alignment of high- and low-momentum pathways induced by secondary flows. Since the alignment of these pathways significantly influences performance-critical quantities such as drag and heat transfer, identifying these parameters is essential to improving our predictive capabilities. To examine these effects in a physically relevant setting, we use wind turbines as roughness elements—reflecting their role as porous obstacles in applications such as wind farms and other complex surface environments.
  </p>

  <h3>Highlights</h3>
  <ol>
    <li>Discovered that the spanwise gap between edge-most roughness elements of adjacent columns is a key geometric parameter that dictates the polarity of secondary flows—a governing factor previously unrecognized in the literature.</li>
    <li>Showcased that secondary flows fundamentally alter <i>mke</i> entrainment pathways; notably, the expected increase in lateral entrainment with wider spanwise spacing can reverse due to the interplay between high-momentum fluid availability and strong advective downdrafts over roughness elements.</li>
    <li>Demonstrated that the strength of secondary flows is not diminished in intermediate configurations; rather, frequent polarity reversals lead to a misleading appearance of their absence in long-time-averaged fields.</li>
    <li>Showed that in all cases, including those with strong polarity in the time-averaged flow field, the high- and low-momentum pathways undergo chaotic, non-periodic reversals over time.</li>
    <li>Found that, despite markedly different mean flow structures, the vertical velocity signal exhibits similar quasi-periodic oscillations across all cases, indicating that frequent pathway switching reflects a near-zero mean state rather than an inherently chaotic fluctuation pattern.</li>
    <li>Established that variability in vertical momentum transport is a fundamental and persistent feature of roughness-induced secondary flows.</li>
  </ol>

  <figure class="research-fig">
    <img src="{{ base_path }}/images/Inst-flow-reversal.png" alt="Instantaneous reversal of secondary flow structures" loading="lazy">
    <figcaption><strong>Figure.</strong> Instantaneous reversal of secondary flow structures (highlight #3).</figcaption>
  </figure>
</div>

<!-- ===================================================================== -->
<!-- 4. SECONDARY FLOW POLARITY                                              -->
<!-- ===================================================================== -->
<div class="research-card" id="polarity">
  <span class="research-number">Project 4 &middot; Ph.D. research</span>
  <h2>Secondary flow polarity in turbulent boundary layers shaped by directional bias from surface roughness</h2>
  <p class="research-meta">
    <strong>Advisor:</strong> <a href="https://www.civil.columbia.edu/content/marco-giovanni-giometto">Prof. Marco G. Giometto</a>
  </p>
  <div class="badges">
    <span class="badge">Manuscript in preparation &middot; Journal of Fluid Mechanics</span>
  </div>

  <h3>Overview</h3>
  <p>
    Similar to project #3, this project aims to improve our predictive capabilities of roughness-induced secondary flow polarity, i.e. the alignment of low- and high-momentum pathways w.r.t roughness elements.
  </p>

  <h3>Highlights</h3>
  <ol>
    <li>Established aerodynamic roughness of the base wall as a new governing parameter of secondary flow polarity.</li>
    <li>Demonstrated, using POD analysis, how large-scale energetic modes reorganize in response to the presence or absence of mean secondary flows.</li>
  </ol>

  <figure class="research-fig">
    <img src="{{ base_path }}/images/urban_reversal_combined_hatched3.png" alt="Reversal of secondary flow polarity" loading="lazy">
    <figcaption><strong>Figure.</strong> Reversal of secondary flow polarity (highlight #1). Arrows: spanwise and vertical velocity.</figcaption>
  </figure>
</div>
