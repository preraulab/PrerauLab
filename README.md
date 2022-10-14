<p align="center">
<img src="https://prerau.bwh.harvard.edu/images/github-splash.png" width="650" />
</p>

## Table of Contents
* [Code](#code)
  * [Toolboxes](#toolboxes)
    * [Multitaper Spectral Analysis](#multitaper-spectral-analysis)
    * [Transient Oscillation Dynamics Toolbox](#transient-oscillation-dynamics-toolbox)
    * [Sleep Apnea Dynamics](#sleep-apnea-dynamics)
    * [Modeling the Sleep Onset Process](#modeling-the-sleep-onset-process)
  * [Paper Code](#paper-specific-code)
* [Tools](#tools)
  * [Estimating AHI Uncertainty](#estimating-ahi-uncertainty)
  * [EDF De-Identification Tool](#edf-de-identification-tool)

# Code
## Toolboxes
### Multitaper Spectral Analysis
### Transient Oscillation Dynamics Toolbox
<p align="center">
<img src="https://prerau.bwh.harvard.edu/wp-content/uploads/2022/10/TF-peak-Flow-Chart_small.png" width="650" />
</p>

We have developed a new approach to creating individualized 
electroencephalogram (EEG) fingerprints of brain activity during sleep, 
which can be used to identify biomarkers of neurological health and 
disease. We first identify tens of thousands of short, spindle-like EEG 
waveforms called time-frequency peaks (TF-peaks) across a night of 
sleep. Then, we create visual summaries of brain state by characterizing
 the activity of TF-peaks as a function of sleep depth and also cortical
 timing, called SO-power and SO-phase histograms. These summaries, like 
fingerprints, appear to be unique to individuals yet consistent night to
 night, providing a highly informative new visualization technique and 
powerful basis for understanding neurological health and disease.

We have developed an open source toolbox and tutorial to create 
slow-oscillation power (SO-power) and phase (SO-phase) histograms from 
the extracted TF-peak data.
<br/><br/>
<a href="https://github.com/preraulab/watershed_TFpeaks_toolbox" target="_blank" rel="noopener">Click here to view the toolbox code repository on Github</a>
<br/><br/>
### Sleep Apnea Dynamics
<p align="center">
<img src="https://prerau.bwh.harvard.edu/wp-content/uploads/2022/10/OSA_dynamics_prerau_web.png" width=700 />
</p>

Obstructive sleep apnea (OSA), in which breathing is reduced or 
ceased during sleep, affects at least 10% of the population and is 
associated with numerous comorbidities. Current clinical diagnostic 
approaches characterize severity and treatment eligibility using the 
average respiratory event rate over total sleep time (apnea hypopnea 
index, or AHI). This approach, however, does not characterize the 
time-varying and dynamic properties of respiratory events that can 
change as a function of body position, sleep stage, and previous 
respiratory event activity. Here, we develop a statistical model 
framework based on point process theory that characterizes the relative 
influences of all these factors on the moment-to-moment rate of event 
occurrence.

We provide a code toolbox and tutorial to walk through the framework,
 from constructing model input to model fitting, as well as the code to 
visualize the model.

<a href="https://github.com/preraulab/Apnea_dynamics_toolbox" target="_blank" rel="noopener">Click here to view the toolbox code repository on Github</a>
<br/><br/>

### Modeling the Sleep Onset Process
<p align="center">
<img src="https://prerau.bwh.harvard.edu/wp-content/uploads/2022/10/SOP.png" width=700 />
</p>

How can we tell when someone has fallen asleep? Understanding the way we fall asleep is an important problem in sleep medicine, since sleep disorders can disrupt the process of falling asleep. In the case of insomnia, subjects may fall asleep too slowly, whereas during sleep deprivation or narcolepsy, subjects fall asleep too quickly. Current methods for tracking the wake/sleep transition are time-consuming, subjective, and simplify the sleep onset process in a way that severely limits the accuracy, power, and scope of any resulting clinical metrics. We have developed a new physiologically principled method that dynamically combines information from brainwaves, muscle activity, and a novel minimally-disruptive behavioral task, to automatically create a continuous dynamic characterization of a person’s state of wakefulness.

We provide a code toolbox and video tutorial to explain the general concepts and results from the paper.

<a href="https://github.com/preraulab/sleep_onset_modeling" target="_blank" rel="noopener">Click here to view the toolbox code repository on Github</a>
<br/><br/>
<br/><br/>

## Paper Specific Code
<h3><a href="https://github.com/preraulab/watershed_TFpeaks_toolbox/tree/transient_oscillation_paper" target="_blank" rel="noopener">Transient Oscillation Dynamics During Sleep Provide a Robust Basis for Electroencephalographic Phenotyping and Biomarker Identification</a></h3>
<em>Patrick A Stokes, Preetish Rath, Thomas Possidente, Mingjian He, Shaun Purcell, Dara S Manoach, Robert Stickgold, Michael J Prerau, Transient Oscillation Dynamics During Sleep Provide a Robust Basis for Electroencephalographic Phenotyping and Biomarker Identification, Sleep, 2022;, zsac223, https://doi.org/10.1093/sleep/zsac223</em>
<h3><a href="https://github.com/preraulab/TF_sigma_peaks_SLEEP2021" target="_blank" rel="noopener">Sleep spindles comprise a subset of a broader class of electroencephalogram events</a></h3>
<em>Tanya Dimitrov, Mingjian He, Robert Stickgold, Michael J Prerau, Sleep spindles comprise a subset of a broader class of electroencephalogram events, Sleep, 2021;, zsab099, https://doi.org/10.1093/sleep/zsab099</em>
<h3><a href="https://github.com/preraulab/IEEE_peak_tracking_paper" target="_blank" rel="noopener">Estimation of time-varying spectral peaks and decomposition of EEG spectrograms</a></h3>
<em>Stokes PA, Prerau MJ. Estimation of Time-Varying Spectral Peaks and Decomposition of EEG Spectrograms. IEEE Access. 2020;8:218257-218278. doi: 10.1109/access.2020.3042737. Epub 2020 Dec 4. PMID: 33816040; PMCID: PMC8015841.</em>

<br/><br/>
# Tools
## Estimating AHI Uncertainty
Currently, the AHI (apnea-hypopnea index: average number of nightly apnea-related breathing events per hour) is treated as a single number that definitively describes the patient’s condition. However, differences in sleep quality across nights, changes in sleep and breathing patterns within a single night, and variability from the limited amount of data collected in a single sleep study can potentially cause a great deal of variability associated with this measurement. Slight alteration in AHI value could mean that an AHI will be on one side of the threshold in one sleep study and the other side of the threshold on a subsequent sleep study, which can be the difference between eligibility and denial of treatment. It is therefore important to understand the uncertainty of the AHI statistic to determine the degree to which it is possible to be confidence in a given diagnosis.
<br/><br/>
To address these problems, we have developed two methods of estimating a confidence interval on the AHI based on what type of data are available.
<br/><br/>
<a href="https://prerau.bwh.harvard.edu/ahi/" target="_blank" rel="noopener">Click here to use this tool.</a>
<br/><br/>
## EDF De-Identification Tool
European Data Format (EDF) is one of the primary ways polysomnography and EEG data are stored. De-identification of EDF files is a necessary step for safe sharing of data, removing any identifying information from the file headers. Often EDF de-identification tools are part of some larger toolbox or software package, making distribution to clinical sites and personnel more difficult.
<br/><br/>
Here we provide standalone GUI-based programs for PC, Mac, and Linux as well as functional source code in MATLAB and python to facilitate de-identification of EDF files.
<br/><br/>
<a href="https://prerau.bwh.harvard.edu/edf-de-identification-tool/" target="_blank" rel="noopener">Click here to use this tool.</a>
