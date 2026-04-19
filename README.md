<p align="center">
<img src="https://prerau.bwh.harvard.edu/images/github-splash.png" width="650" />
</p>

# Prerau Laboratory — public code catalog

The [Prerau Laboratory](https://prerau.bwh.harvard.edu/) at Brigham and Women's Hospital / Harvard Medical School develops statistical-signal-processing and machine-learning tools for understanding sleep neurophysiology. This repository is the master index of our public code.

- **Website:** [sleepeeg.org](https://sleepeeg.org) · [prerau.bwh.harvard.edu](https://prerau.bwh.harvard.edu)
- **Contact:** Michael J. Prerau, Ph.D. — <prerau@bwh.harvard.edu>

## Contents

- [Core analysis toolboxes](#core-analysis-toolboxes)
- [Paper companion code](#paper-companion-code)
- [I/O and data tools](#io-and-data-tools)
- [Utilities & infrastructure](#utilities--infrastructure)
- [Sleep data / analysis](#sleep-data--analysis)
- [How to cite our work](#how-to-cite-our-work)

---

## Core analysis toolboxes

| Toolbox | Description | Key reference |
|---|---|---|
| [`multitaper_toolbox`](https://github.com/preraulab/multitaper_toolbox) | MATLAB, Python, and R implementations of the multitaper spectrogram (optional Rust backend) | Prerau et al., *Physiology* 2017 |
| [`DYNAM-O`](https://github.com/preraulab/DYNAM-O) | Dynamic Oscillation Toolbox v1.0 (MATLAB) — TF-peak + SO-power / SO-phase histograms | [doi:10.1093/sleep/zsac223](https://doi.org/10.1093/sleep/zsac223) |
| [`pyDYNAM-O`](https://github.com/preraulab/pyDYNAM-O) | Python port of DYNAM-O | [doi:10.1093/sleep/zsac223](https://doi.org/10.1093/sleep/zsac223) |
| [`Spindle_dynamics_toolbox`](https://github.com/preraulab/Spindle_dynamics_toolbox) | Individualized temporal patterns of human sleep spindle timing | Chen et al., *PNAS* 2025 |
| [`Apnea_dynamics_toolbox`](https://github.com/preraulab/Apnea_dynamics_toolbox) | Point-process models for respiratory event timing in OSA | [doi:10.1093/sleep/zsac189](https://doi.org/10.1093/sleep/zsac189) |
| [`sleep_onset_modeling`](https://github.com/preraulab/sleep_onset_modeling) | Bayesian particle-filter model of the sleep-onset process | [doi:10.1371/journal.pcbi.1003866](https://doi.org/10.1371/journal.pcbi.1003866) |
| [`MTSleepScoring`](https://github.com/preraulab/MTSleepScoring) | Interactive MATLAB GUI for manual sleep-stage scoring on multitaper spectrograms | — |
| [`artifact_detection`](https://github.com/preraulab/artifact_detection) | Iterative z-score artifact detection for continuous time-series data | — |
| [`rate_xvalidation`](https://github.com/preraulab/rate_xvalidation) | Cross-validated Hanning-kernel point-process firing-rate estimator | [doi:10.1152/jn.01036.2010](https://doi.org/10.1152/jn.01036.2010) (Prerau & Eden 2011) |
| [`learningcurves`](https://github.com/preraulab/learningcurves) | State-space and particle-filter learning-curve estimators | Prerau & Eden 2011 |
| [`multicomp_test`](https://github.com/preraulab/multicomp_test) | Permutation and FDR-controlled multiple-comparison tests for 1-D/2-D data | — |

## Paper companion code

Repositories published alongside a specific paper. Please cite the paper listed.

| Repo | Paper |
|---|---|
| [`TF_sigma_peaks_SLEEP2021`](https://github.com/preraulab/TF_sigma_peaks_SLEEP2021) | Dimitrov, He, Stickgold, Prerau. *Sleep* 2021 — [doi:10.1093/sleep/zsab099](https://doi.org/10.1093/sleep/zsab099) |
| [`IEEE_peak_tracking_paper`](https://github.com/preraulab/IEEE_peak_tracking_paper) | Stokes, Prerau. *IEEE Access* 2020 — [doi:10.1109/access.2020.3042737](https://doi.org/10.1109/access.2020.3042737) |
| [`Spindle_dynamics_toolbox`](https://github.com/preraulab/Spindle_dynamics_toolbox) | Chen et al. *PNAS* 2025 (cross-listed above) |
| [`Apnea_dynamics_toolbox`](https://github.com/preraulab/Apnea_dynamics_toolbox) | Chen, Redline, Eden, Prerau. *Sleep* 2022 (cross-listed above) |
| [`sleep_onset_modeling`](https://github.com/preraulab/sleep_onset_modeling) | Prerau et al. *PLOS Comp Biol* 2014 (cross-listed above) |
| [`DYNAM-O`](https://github.com/preraulab/DYNAM-O) / [`pyDYNAM-O`](https://github.com/preraulab/pyDYNAM-O) | Stokes, Rath, Possidente, He, Purcell, Manoach, Stickgold, Prerau. *Sleep* 2022 (cross-listed above) |

## I/O and data tools

| Repo | Description |
|---|---|
| [`read_EDF`](https://github.com/preraulab/read_EDF) | High-performance MEX-accelerated EDF/EDF+ reader for MATLAB |
| [`EDF_deidentify_toolbox`](https://github.com/preraulab/EDF_deidentify_toolbox) | Standalone GUI + MATLAB/Python source to de-identify EDF files |
| [`data_IO`](https://github.com/preraulab/data_IO) | EDF, BrainVision, MBF, Grass scoring, bytestream, log-file helpers |

## Utilities & infrastructure

| Repo | Description |
|---|---|
| [`preraulab_utilities`](https://github.com/preraulab/preraulab_utilities) | Meta-repository bundling the nine general-purpose utility sub-repos below |
| &nbsp;&nbsp;↳ [`binning`](https://github.com/preraulab/binning) | 1-D / N-D binning and sliding-window histograms |
| &nbsp;&nbsp;↳ [`conversion`](https://github.com/preraulab/conversion) | Numeric/struct/table/CSV conversion utilities |
| &nbsp;&nbsp;↳ [`data_processing`](https://github.com/preraulab/data_processing) | Run-/chunk-/interval-based signal utilities |
| &nbsp;&nbsp;↳ [`fig_tools`](https://github.com/preraulab/fig_tools) | Figure layout, axes linking, interactive pan/zoom |
| &nbsp;&nbsp;↳ [`graphical`](https://github.com/preraulab/graphical) | Higher-level plot primitives (shaded bounds, Gantt, phase histograms) |
| &nbsp;&nbsp;↳ [`nanstats`](https://github.com/preraulab/nanstats) | NaN-aware statistical helpers |
| &nbsp;&nbsp;↳ [`read_EDF`](https://github.com/preraulab/read_EDF) | EDF/EDF+ reader (cross-listed) |
| &nbsp;&nbsp;↳ [`workspace`](https://github.com/preraulab/workspace) | MATLAB workspace management |
| &nbsp;&nbsp;↳ [`CSSuicontrols`](https://github.com/preraulab/CSSuicontrols) | CSS-styled HTML-backed UI controls for `uifigure` apps |
| [`EventMarker`](https://github.com/preraulab/EventMarker) | Interactive event-marker manager for MATLAB plots |
| [`colormaps`](https://github.com/preraulab/colormaps) | Perceptually-uniform and custom colormaps for MATLAB |

## Sleep data / analysis

| Repo | Description |
|---|---|
| [`sleep`](https://github.com/preraulab/sleep) | Sleep EEG analysis toolbox: staging I/O, hypnograms, slow-wave extraction, simulations |

---

## How to cite our work

Each code repository includes a `CITATION.cff` file. When you use one of our tools in a publication, please cite **both** (a) the peer-reviewed paper listed in `CITATION.cff` (under `preferred-citation`) and (b) the software entry itself. GitHub exposes the citation in the sidebar of every repo — click **"Cite this repository"** to copy BibTeX or APA.

For general correspondence: <prerau@bwh.harvard.edu>.

<!-- Related projects, AHI confidence interval tool, and further resources are available at https://prerau.bwh.harvard.edu/ -->
