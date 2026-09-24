# Motion Artifact Detection in PPG Signals

Academic MATLAB project investigating motion and perfusion artifacts in photoplethysmogram (PPG) data. The work explores signal conditioning and overlapping-window analysis, with GUI experiments and supporting reports.

## Project overview

PPG measurements are affected by movement and baseline changes. This repository collects experiments for detecting and removing affected signal segments, inspecting the resulting waveforms, and studying physiological-rate estimation.

The project demonstrates MATLAB signal processing, window-based analysis, visualization, and GUI prototyping. It is a research archive; no clinical validation or generalizable accuracy claim is made here.

## Where to start

| Location | Contents |
| --- | --- |
| [Graphical User Interface](Graphical%20User%20Interface) | App Designer files, MATLAB scripts, and a user manual |
| [GUI manual](Graphical%20User%20Interface/Manual.docx) | Existing application usage documentation |
| [Earlier experiments](Final%20Code%20%28Use%20GUI%20instead%29) | Live scripts for overlapping-window and adaptive processing experiments |
| [Reports and presentations](Reports%20and%20Presentations) | Academic project context and reports |
| [Final results](Final%20Results) | Historical analysis artifacts; read the privacy considerations below before reuse |

## Method and implementation

The experimental workflow is to inspect a PPG recording, condition the signal, analyze overlapping windows, identify artifact-affected regions, and compare the resulting waveforms and summaries.

Concrete entry points:

- [butterworth.m](Graphical%20User%20Interface/butterworth.m) defines a bandpass filter with a 64 Hz sampling rate and 0.6–4 Hz cutoff settings.
- [BR_GUI.m](Graphical%20User%20Interface/BR_GUI.m) reads a perfusion/PPG CSV, filters a respiratory band, and estimates breathing rate from peak intervals.
- The GUI directory contains App Designer variants `app0.mlapp` through `app3.mlapp` and the `Final_working.mlx` live script. Consult the manual rather than assuming that the highest-numbered app is the canonical release.

These settings belong to the recorded experiments; they should not be applied to a different sampling rate or dataset without review.

## Inspecting or running the work

1. Use MATLAB with App Designer support. The filter code was generated with MATLAB 9.9 and Signal Processing Toolbox 8.5; a complete dependency/version inventory has not been established.
2. Read the GUI manual and inspect the selected app or live script before execution.
3. Review relative file references and expected CSV columns. For example, `BR_GUI.m` expects `perf1andppg1.csv` in the working directory.
4. Use only data you are authorized to process. Work on a copy and save new results separately from the historical outputs.

There is no automated setup or regression suite documented here. Existing figures and result files are historical artifacts, not independently reproduced benchmarks.

## Data and privacy considerations

The repository contains subject-organized results and data-derived files, including CSVs, figures, and reports. Subject numbering alone does not establish anonymization, consent, or redistribution permission.

Before reusing or redistributing these materials, verify participant consent, dataset provenance, institutional restrictions, authorship, and the contents/metadata of reports and figures. Public availability does not by itself grant a data or software license. Avoid publishing additional participant-level outputs until those questions are resolved.

This presentation update preserves the existing data and Git history. It does not certify the historical materials as safe to redistribute; any later data cleanup should be a separate, explicitly reviewed change.

## Author

[More engineering and research work](https://mafaq318.github.io/) · [GitHub profile](https://github.com/mafaq318)
