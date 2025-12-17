# Circuit Mechanisms

This is the project report for *Circuit mechanisms*.  
We present the motivation, methods, experiments, results, and a mechanism-focused analysis supported by figures.

## Contents
See the navigation sidebar.

# Predicting an Action Potential Before It Happens
Motivation and guiding question
Neurons do not fire action potentials at random. Long before a spike is generated, the membrane potential already reflects a complex interplay between synaptic inputs, intrinsic conductances, and recent activity. This raises a fundamental question: can the occurrence of an imminent action potential be predicted using only subthreshold membrane potential dynamics?
In this project, we address this question by focusing exclusively on short time windows preceding spike initiation, deliberately excluding the spike itself. By isolating these pre-spike dynamics, we aim to determine whether the membrane potential trajectory already contains reliable information about an upcoming action potential.
Figure 1 illustrates this central idea: a membrane potential trace is shown over time, with an action potential highlighted and a short pre-spike window shaded immediately before spike onset.

Cell types and working hypotheses
Our analysis spans four major cortical neuron classes: excitatory pyramidal neurons (EXC) and three inhibitory interneuron types—parvalbumin-positive (PV), somatostatin-positive (SST), and vasoactive intestinal peptide-positive (VIP) neurons. These classes differ substantially in their electrophysiological properties, firing patterns, and roles in cortical computation.
We hypothesize that each neuronal class exhibits a characteristic pre-spike signature, composed of a specific combination of subthreshold membrane potential features. In particular, we focus on three simple descriptors: the slope of the membrane potential preceding the spike, the mean membrane potential, and the variability of the membrane potential within this period.
Fast-spiking PV interneurons are expected to display steep pre-spike slopes and reduced membrane potential variability, reflecting rapid and reliable spike initiation. In contrast, EXC, SST, and VIP neurons may show a slower or more variable buildup toward threshold, consistent with their integrative and modulatory functions.
Figure 2 conceptually contrasts pre-spike membrane potential trajectories across neuron classes, highlighting expected differences in slope and variability.

Time scales of pre-spike dynamics
Spike initiation unfolds over multiple temporal scales. Very short time windows may capture rapid threshold-crossing dynamics, while longer windows may reflect slower integrative processes that prepare the neuron for spiking.
To probe this, we analyze pre-spike membrane potential dynamics using multiple window durations (20 ms, 10 ms, and 5 ms), each ending strictly before spike onset. This multi-scale approach allows us to assess how predictive information evolves as the neuron approaches the spike threshold.
Figure 3 schematically illustrates the different pre-spike window lengths aligned to spike onset, emphasizing how each window captures a distinct temporal scale of membrane potential dynamics.
Pre-spike versus baseline membrane activity
To determine whether subthreshold features truly signal an imminent action potential, we compare membrane potential dynamics in two conditions: pre-spike windows and baseline windows.
For each detected action potential, we define a pre-spike window placed immediately before spike initiation. To ensure that these windows reflect purely subthreshold activity, any window containing an action potential—including a preceding spike—is excluded from the analysis.
In parallel, we sample baseline windows of identical duration from periods in which no action potential occurs and no spike follows within a predefined safety margin. These baseline windows represent membrane potential fluctuations not associated with imminent spike generation.
By comparing feature distributions between pre-spike and baseline windows across cell types and time scales, we quantify whether simple subthreshold features can reliably distinguish spiking from non-spiking states.
Figure 4 shows example feature distributions for pre-spike and baseline windows, illustrating how these features separate spiking and non-spiking membrane states.
