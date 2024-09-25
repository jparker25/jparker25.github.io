---
permalink: /about/
excerpt: "About Me"
title: "About Me"
author_profile: true
layout: single
classes: wide
---

I currently hold a position as a Postdoctoral Associate in the [Department of Mathematics at the University of Pittsburgh](https://www.mathematics.pitt.edu), collaborating with [Dr. Jonathan Rubin](https://www.mathematics.pitt.edu/people/jonathan-rubin). Our research focuses on exploring the substantia nigra pars reticulata (SNr) and its response to dopamine depletion using a biophysical dynamical model. This work is conducted in partnership with the [Gittis lab](https://labs.bio.cmu.edu/gittis/) at [Carnegie Mellon University](https://www.cmu.edu). For more detailed information about my academic and research endeavors, please explore the various tabs on this site. I am always open to engaging with others in the scientific community, so please do not hesitate to contact me.

***
### Background
I earned my PhD in Applied Mathematics from the [University of New Hampshire](https://ceps.unh.edu/integrated-applied-mathematics), where I was mentored by [Dr. Kevin Short](https://findscholars.unh.edu/display/kmshort) and specialized in nonlinear dynamics. My doctoral research centered on the concept of stabilizing chaos in neural models through mutual stabilization, a process detailed further in my [publications](/publications/). I have a strong fondness for developing computational models and visualization tools to facilitate the analysis of mathematical models.

Beginning with my undergraduate studies in Physics at [Elon University](https://www.elon.edu/u/academics/arts-and-sciences/physics/), I have consistently engaged in mathematical and computational neuroscience, which remained the focus throughout my doctoral and postdoctoral research. My broader academic interests span mathematical biology, computational neuroscience, and climate dynamics. Moving forward, I am contemplating a shift towards climate research in my future professional endeavors, while still engaging in neuroscience through side projects.

***
### Postdoctoral Research (2021 - 2024)
During my postdoctoral tenure at the University of Pittsburgh, I engaged in a mathematical and computational neuroscience project to better understand the integrative mechanisms of the substantia nigra pars reticulata (SNr), a critical output nucleus of the basal ganglia. This project emphasized understanding the SNr’s response to various inhibitory inputs, commonly referred to as the direct and indirect pathways, under both normative and dopamine-depleted conditions, the latter being a key characteristic of Parkinson's disease pathology.

The foundational objective of this research was to interpret and extend the experimental findings detailed in prior studies, notably those by [Mastro, et al., 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5546121/) and [Freeze, et al., 2013](https://pubmed.ncbi.nlm.nih.gov/24259575/), as well as new experimental results from the [Gittis lab](https://labs.bio.cmu.edu/gittis/). Our approach involved refining a biophysically detailed model of the SNr, initially presented in [Phillips, et al., 2020](https://elifesciences.org/articles/55592). My specific contributions to this body of work include:

1. Developing the STReaC toolbox, a novel software framework designed to facilitate nuanced analysis of neuronal spike train responses to stimuli. Crafted in Python, this tool has been [published](/publication/Parker_Aristieta_Gittis_Rubin_2023) and is accessible with a public repository at [STReaC toolbox](https://github.com/jparker25/streac), for which I will continue to provide support and updates.
2. Enhancing the existing SNr model by:
   - Incorporating stochastic elements into the soma and dendritic current equations.
   - Modulating tonic conductances through stochastic processes.
   - Introducing heterogeneity within the network, particularly in conductance strengths.

We are in the process of drafting a manuscript that will detail these model advancements and their experimental corroboration under both normal and dopamine-depleted conditions.

***

### Doctoral Research (2016 - 2021)
My doctoral research explored the phenomenon of mutual stabilization in chaotic neuronal systems. Mutual stabilization refers to the process where two chaotic systems, upon interaction in a specific manner, are steered towards periodic orbits due to the nature of their interaction. This concept was initially illustrated using cupolets—chaotic unstable periodic orbit-lets—emerging from the interaction of two double scroll oscillators.

A significant finding of my dissertation was that two FitzHugh-Nagumo neurons, when interacting bidirectionally, can exhibit chaotic behavior. This chaos was managed and led to mutual stabilization by implementing a sigmoidal synaptic learning rule. The details of this research have been [published](https://doi.org/10.1063/5.0002328).

Another major contribution of my doctoral work was demonstrating the presence of cupolets in the chaotic dynamics of Hindmarsh-Rose neurons ([Parker and Short, 2022](/publication/Parker_Short_2022)) and how these cupolets can lead to mutual stabilization in interacting neuronal models ([Parker and Short, 2023, open-access](/publication/Parker_Short_2023)).
