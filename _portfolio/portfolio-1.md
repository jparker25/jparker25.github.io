---
title: "STReaC Toolbox"
excerpt: "Python toolbox for classification of spike train response period as compared to a reference period.<br/><img src='/images/average_example.pdf'>"
collection: portfolio
---

The [STReaC toolbox](/publication/Parker_Aristieta_Gittis_Rubin_2023) is a recently published Python toolbox for analyzing and classifying responses of spike trains compared to a reference period, often called the baseline period. This toolbox was developed to assist in classifying spike trains from the pars reticulata of the substantia nigra (SNr), an output nucleus of the basal ganglia (BG), during optogenetic stimulation of two nuclei of th BG that provide (classically) inhibitory input to the SNr: the globus pallidus externa (GPe) and striatum (STR). However, our aim is that this software can be used by anyone hoping to classifying spike train responses. We have developed the toolbox such that it is easy to use and user-friendly with plenty of parameters to adjust, if needed, for different experimental set-ups and analysis.

Below is a brief overview of how it works and more details can be found on the GitHub repository (link below).

### Brief summary
![Average Example](/images/average_example.pdf)

The STReaC toolbox is best explained through an example. In this figure, the analysis of one neuron is portrayed. Panel A provides the raster plot of a single neuron's trials, where the reference (baseline) period is in negative time, the stimulus starts at time 0, and both periods last for 10s. The red bar at the top indicates the laser for the optogenetic stimulation.

The STReaC toolbox reads in the spike times corresponding to each trial and transforms the discrete spike events into smooth, continuous functions. The first function, called the spike density function (SDF), is a function with height proportional to periods of high firing. Panel B displays the corresponding SDFs for each of the stimulus periods in panel A. The SDF is constructed by centering a Gaussian of a specific bandwidth $$\sigma$$ (default 25ms) at each spike, then summing up all Gaussians. 

The second function, called the interspike interval function (ISIF), is a function with height proportional to periods of low firing, or pauses betweein firing. Panel C displays the corresponding ISIFs for each of the stimulus periods in panel A. The ISIF is constructed as a moving average of the linearly interpolated function of interspike intervals corresponding to each spike time. The moving average is performed over $$\mu$$ (default 250) points. 

Then, the average SDF and average ISIF is computed and the area under the curve is compared to corresponding areas in the reference period. That is, for each trial, the area under the curve is computed for both the SDF and ISIF then these values are aggregated across all trials to determine a complete reference area distribution. The average SDF is then partitioned into equal bins(shown by vertical dashed lines in panel D) and areas under the curve for each partition is compared with a threshold of the reference area distribution. If any area is greater than this threshold, then the neuron is considered to be excited during that bin. The analogous process is completed for the average ISIF and respective reference ISIF area distribution. 

After the previous step, the number of excited bins and inhibited bins are tallied. These values are cross-referenced with a classification table to determine the neuron's average response. In the example here, we have 4 excited bins and 0 inhibited bins, so we would determine if these values cross the excited bin threshold (EBT) and/or inhibited bin threshold (IBT) to determine the response. Using the example classification table below, we see that the provided example would be considered an excited response. 

| Classification  | EBT | IBT | Constraints |
| :-------: | :----: | :----: | :--: |
| Complete Inhibition | - | - | $$f \lt f_{min}$$ |
| Partial Inhibition  | $$\lt$$ | $$\ge$$ | - |
| Adapting Inhibition | $$\lt$$ | $$\ge$$ | More inhibited bins in first half |
| Excitation | $$\ge$$ | $$\lt$$ | - |
| Biphasic IE | $$\ge$$ | $$\ge$$ | Last excited bin is after last inhibited bin |
| Biphasic EI | $$\ge$$ | $$\ge$$ | Last inhibited bin is after last excited bin |
| No Effect | $$\lt$$ | $$\lt$$ | - |

### Data Structure
There is a large directory that contains a subdirectory of neuron type to be classified. For our experimental data, this was stimulation of the GPe or STR. Within each subdirectory should be further subdirectories for each neuron with leading 0s. Finally, within each neuron directory there are three files. The first, `spikes.txt`, contains all relevant spike times over the entire experiment. The second, `light_on.txt`, contains times indicating when each trial begins. The third, `meta_data.txt`, contains colon delimited information about the neuron. If done correctly, the directory structure might look something like the following:

```
Experimental_Group_01
├── Neuron_0001
│   ├── light_on.txt
│   ├── meta_data.txt
│   └── spikes.txt
├── Neuron_0002
│   ├── light_on.txt
│   ├── meta_data.txt
│   └── spikes.txt
└── Neuron_0003
    ├── light_on.txt
    ├── meta_data.txt
    └── spikes.txt

```


### External Links
Please visit [the STReaC toolbox publication](https://www.sciencedirect.com/science/article/abs/pii/S0165027023002194?via%3Dihub) for the peer-reviewed publication and more details. Please cite appropriately if using this toolbox in your own work.

For information on implementation and code, please visit he repository [the STReaC toolbox](https://github.com/jparker25/streac) that is hosted on GitHub. 