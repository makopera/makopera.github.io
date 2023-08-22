---
layout: post
title: NUMO dynamics validation
description:
date: 2016-07-21 00:00:00 +0800
author: michal
image: '/images/kovasznay_u_norm_present1.png'
tags: ["research", "NUMO"]
tags_color: '#b25642'
featured:
---

The first milestone in the development of NUMO was to make sure the equations driving the dynamics of the ocean are solved correctly. The underlying dynamics (i.e. velocity and pressure) in the model are governed by the incompressible Navier-Stokes equation (INSE). You can read more details on the equations and numerical methods that solve them on the [Projects](/projects/) page.

To validate the implementation of INSE in NUMO, we have used two benchmarks with analytic solutions: Kovasznay flow and Taylor vortex. For the purpose of these tests, we do not include buoyancy and Coriolis source terms.

## Kovasznay flow

The first solution was provided by Kovasznay [^1] in 1948, which represents a steady state laminar flow behind a two-dimensional grid. Here we solve this flow using a full 3D model and expect z component of velocity to vanish. The exact solution  $\mathbf{u}_e = [ u_e, v_e]$  is given by:


[^1]: Kovasznay, L. I. G. *Laminar flow behind a two-dimensional grid.* Mathematical Proceedings of the Cambridge Philosophical Society. Vol. 44. No. 01. Cambridge University Press, 1948.

