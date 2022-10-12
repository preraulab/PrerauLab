<p align="center">
<img src="https://prerau.bwh.harvard.edu/images/github-splash.png" width="350" />
</p>

# PrerauLab
Summary of the What and Where of the Prerau Lab Code 

## Table of Contents
* [Code](#code)
  * [Toolboxes](#toolboxes)
  * [Paper Code](#paper-specific-code)
* [Tools](#tools)

<h1><a id="Code"></a>Code</h1>
<h2><a id="Toolboxes"></a>Toolboxes</h2>
<h3>Watershed TF-Peaks &amp; SO-Power and Phase Histograms</h3>
This repository contains code to detect time-frequency peaks (TF-peaks) in a spectrogram of EEG data using the watershed image segmentation algorithm. TF-peaks represent transient oscillatory neural activity at specific frequencies with sleep spindles (a key neural biomarker) comprising a subset of TF-peaks. The watershed method treats the spectrogram image as a topography and identifies the catchment basins (troughs), into which water falling on the terrain would collect, thus identifying local maxima. To reduce over-segmentation, neighboring regions are merged based on a novel merge rule designed to form complete, distinct TF-peaks in the spectrogram topography.
<br/><br/>
This repository also contains code to create slow-oscillation power (SO-power) and phase (SO-phase) histograms from the extracted TF-peak data. These histograms characterize the distribution of TF-peak rate (density) as function of oscillation frequency and SO-power or SO-phase. This creates a comprehensive representation of transient oscillation dynamics at different time scales, providing a highly informative new visualization technique and powerful basis for EEG phenotyping and biomarker identification in pathological states.
<br/><br/>
<a href="https://github.com/preraulab/watershed_TFpeaks_toolbox" target="_blank" rel="noopener">Click here to view the toolbox code repository on Github</a>
<br/><br/>
<h3>Sleep Apnea Dynamics</h3>
Obstructive sleep apnea (OSA), in which breathing is reduced or ceased during sleep, affects at least 10% of the population and is associated with numerous comorbidities. Current clinical diagnostic approaches characterize severity and treatment eligibility using the average respiratory event rate over total sleep time (apnea hypopnea index, or AHI). This approach, however, does not characterize the time-varying and dynamic properties of respiratory events that can change as a function of body position, sleep stage, and previous respiratory event activity. Here, we develop a statistical model framework based on point process theory that characterizes the relative influences of all these factors on the moment-to-moment rate of event occurrence.
<br/><br/>
Herein, we provide code to walk through the framework, from constructing model input to model fitting, as well as the code to visualize the model.
<br/><br/>
<a href="https://github.com/preraulab/Apnea_dynamics_toolbox" target="_blank" rel="noopener">Click here to view the toolbox code repository on Github</a>
<br/><br/>
<h2><a id="PaperCode"></a>Paper Specific Code</h2>
<h3><a href="https://github.com/preraulab/watershed_TFpeaks_toolbox/tree/transient_oscillation_paper" target="_blank" rel="noopener">Transient Oscillation Dynamics During Sleep Provide a Robust Basis for Electroencephalographic Phenotyping and Biomarker Identification</a></h3>
<em>Patrick A Stokes, Preetish Rath, Thomas Possidente, Mingjian He, Shaun Purcell, Dara S Manoach, Robert Stickgold, Michael J Prerau, Transient Oscillation Dynamics During Sleep Provide a Robust Basis for Electroencephalographic Phenotyping and Biomarker Identification, Sleep, 2022;, zsac223, https://doi.org/10.1093/sleep/zsac223</em>
<h3><a href="https://github.com/preraulab/TF_sigma_peaks_SLEEP2021" target="_blank" rel="noopener">Sleep spindles comprise a subset of a broader class of electroencephalogram events</a></h3>
<em>Tanya Dimitrov, Mingjian He, Robert Stickgold, Michael J Prerau, Sleep spindles comprise a subset of a broader class of electroencephalogram events, Sleep, 2021;, zsab099, https://doi.org/10.1093/sleep/zsab099</em>
<h3><a href="https://github.com/preraulab/IEEE_peak_tracking_paper" target="_blank" rel="noopener">Estimation of time-varying spectral peaks and decomposition of EEG spectrograms</a></h3>
<em>Stokes PA, Prerau MJ. Estimation of Time-Varying Spectral Peaks and Decomposition of EEG Spectrograms. IEEE Access. 2020;8:218257-218278. doi: 10.1109/access.2020.3042737. Epub 2020 Dec 4. PMID: 33816040; PMCID: PMC8015841.</em>

<br/><br/>
<h1><a id="Tools"></a>Tools</h1>
<h2>Estimating AHI Uncertainty</h2>
Currently, the AHI (apnea-hypopnea index: average number of nightly apnea-related breathing events per hour) is treated as a single number that definitively describes the patient’s condition. However, differences in sleep quality across nights, changes in sleep and breathing patterns within a single night, and variability from the limited amount of data collected in a single sleep study can potentially cause a great deal of variability associated with this measurement. Slight alteration in AHI value could mean that an AHI will be on one side of the threshold in one sleep study and the other side of the threshold on a subsequent sleep study, which can be the difference between eligibility and denial of treatment. It is therefore important to understand the uncertainty of the AHI statistic to determine the degree to which it is possible to be confidence in a given diagnosis.
<br/><br/>
To address these problems, we have developed two methods of estimating a confidence interval on the AHI based on what type of data are available.
<br/><br/>
<a href="https://prerau.bwh.harvard.edu/ahi/" target="_blank" rel="noopener">Click here to use this tool.</a>
<br/><br/>
<h2>EDF De-Identification Tool</h2>
European Data Format (EDF) is one of the primary ways polysomnography and EEG data are stored. De-identification of EDF files is a necessary step for safe sharing of data, removing any identifying information from the file headers. Often EDF de-identification tools are part of some larger toolbox or software package, making distribution to clinical sites and personnel more difficult.
<br/><br/>
Here we provide standalone GUI-based programs for PC, Mac, and Linux as well as functional source code in MATLAB and python to facilitate de-identification of EDF files.
<br/><br/>
<a href="https://prerau.bwh.harvard.edu/edf-de-identification-tool/" target="_blank" rel="noopener">Click here to use this tool.</a>
