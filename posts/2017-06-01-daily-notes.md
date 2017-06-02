<!--
.. title: Daily notes - 1 June 2017
.. slug: 2017-06-01-daily-notes
.. date: 2017-06-01 08:34:44 UTC+02:00
.. tags: mathjax
.. category:
.. link:
.. description:
.. type: text
-->

I'm in the library and this is my plan for today:

  + Read the recovery data from the data base
  + Write an objective function based on the Buckley-Leverett formulation
  + Run the optimization problem in Julia
  + Optimize the rel-perm parameters

Funny story: the paper that has done core flooding and reported the recovery data at high temperature, does not report the viscosity of oil at high temperature. I had to calculate it using this correlation:
$$\ln(\frac{\mu}{\mu_0}) = B(\frac{1}{T}-\frac{1}{T_0})$$
I found the B value by fitting the above equation to the viscosity data of n-Dodecane. The viscosity data comes from the cool [CoolProp](http://www.coolprop.org) package.  

The recovery data is not a straight line at the beginning of the core flooding. It must be a problem in choosing the right moment to start the timer. I shifted the curve to make it consistent.  

The most important problem with using the analytical solution of the BL equation as an objective function is that very occasionally, the shock front cannot be found with a reasonable numerical accuracy. This blows up the objective function and the whole optimization procedure. Perhaps, I should try the numerical solution (upwind) that is slower, but (almost) always converges.  
