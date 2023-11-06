---
title: "Introducing the STReaC (Spike Train Response Classification) toolbox"
collection: publications
permalink: /publication/Parker_Aristieta_Gittis_Rubin_2023
excerpt: 'This paper showcases a new classification toolbox for spike trains.'
date: 2023-10-30
venue: 'Journal of Neuroscience Methods'
paperurl: 'https://doi.org/10.1016/j.jneumeth.2023.110000'
citation: 'John E. Parker et al. "Introducing the STReaC (Spike Train Response Classification) toolbox". In: <i>Journal of Neuroscience Methods</i> (2023), p. 110000. doi: https://doi.org/10.1016/j.jneumeth. 2023.110000'
---
Abstract: <i>Background:</i>
This work presents a toolbox that implements methodology for automated classification of diverse neural responses to optogenetic stimulation or other changes in conditions, based on spike train recordings.

<i>New Method:</i>
The toolbox implements what we call the Spike Train Response Classification algorithm (STReaC), which compares measurements of activity during a baseline period with analogous measurements during a subsequent period to identify various responses that might result from an event such as introduction of a sustained stimulus. The analyzed response types span a variety of patterns involving distinct time courses of increased firing, or excitation, decreased firing, or inhibition, or combinations of these. Excitation (inhibition) is identified from a comparative analysis of the spike density function (interspike interval function) for the baseline period relative to the corresponding function for the response period.

<i>Results:</i>
The STReaC algorithm as implemented in this toolbox provides a user-friendly, tunable, objective methodology that can detect a variety of neuronal response types and associated subtleties. We demonstrate this with single-unit neural recordings of rodent substantia nigra pars reticulata (SNr) during optogenetic stimulation of the globus pallidus externa (GPe).

<i>Comparison with existing methods:</i>
In several examples, we illustrate how the toolbox classifies responses in situations in which traditional methods (spike counting and visual inspection) either fail to detect a response or provide a false positive.

<i>Conclusions:</i>
The STReaC toolbox provides a simple, efficient approach for classifying spike trains into a variety of response types defined relative to a period of baseline spiking.
