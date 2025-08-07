---
title: '"What are Hamiltonian Monte Carlo models, and should I use them?"'
excerpt: "An essay for my 'Advanced Bayesian Statistics' module. It explores different monte carlo methods for posterior sampling, with a focus on Hamiltonian Methods.<br/><img src='/images/hmc.png' width='400'>"
collection: portfolio
---

This was a project I undertook independently in my Advanced Bayesian Statistics module during my fourth year of study. The essay explore the advantages of Hamiltonian methods, in which a sample space is explored by a particle with a position and momentum. If you're interested, you can read the full eassy [here](https://docs.google.com/document/d/e/2PACX-1vTcuqR1X_lbW_nduYRzejT7xooMIV1MQQnP1RY5JLAX09N-jUCSVOoCaeuGHdigEE7Irl3FCEzpHN5g/pub).

For a brief summary, here are the conclusions from the essay:

So what are HMC models? They are simply an extension of Metropolis-Hastings methods in which new parameter vectors are proposed based on a system of Hamiltonian dynamics. This system can take many forms, but in all cases allows for fast exploration of sample spaces without sacrificing acceptance probability, particularly in correlated or high-dimensional spaces typical random walks tend to struggle with.

Should I use HMC models? Obviously it depends. For inference in lower-dimensional space where full conditionals are convenient to sample from, you may prefer Gibbs. Metropolis-Hastings methods can be useful in similar cases where full conditionals are less convenient. Both need to compute gradients and can be more intuitive and convenient to implement (though the gap in implementation is closing over time). However, in higher dimensional spaces or even two dimensional spaces that are initially inconvenient for a random walk and may need transformation the answer is a resounding yes. I would recommend NUTS as it requires less manual tuning and is increasingly available in packages like STAN, but any HMC model will make your life much easier as a statistician.

Key skills I developed through this essay and similar include:
 * Bayesian Statistics
 * Research Skills
 * Mathematical and Statistical concepts