# Creating Intracranial Tasks: Collated Tutorial

## 1) Start with the scientific question
- Define the exact cognitive process you want to isolate and write explicit hypotheses before looking at neural data.[^mercier2022]
- Sketch expected figures/results early so design decisions map to analyses.[^axmacher2023]

## 2) Choose and adapt a paradigm
- Do a focused literature review first; adapt vetted iEEG-compatible tasks when possible.[^axmacher2023]
- Prefer paradigms that exploit iEEG strengths (timing precision, single-trial resolution, local signals).[^stolk2018]

## 3) Plan trials, duration, and feasibility before coding
- Simulate total run time:
  - `(trial duration + ITI) x number of trials`.
- Keep total task duration patient-friendly and split into short runs/blocks so interrupted sessions still yield analyzable data.
- Design runs so each run includes all key conditions; later runs should add power, not add missing conditions.
- Estimate trial count needs by analysis type:
  - Robust effects (e.g., strong HFA changes): fewer trials may work.
  - Connectivity analyses: more trials required.[^bastos2016]
  - Complex computational or multilevel models: more trials required.[^lvwang2023][^gelmanhill2006]
  - Trial-by-trial regressions: ensure enough trials per condition.

## 4) Account for real iEEG sampling constraints
- Plan for participant exclusions:
  - Poor task performance,
  - Seizure/clinical interruption,
  - Lesion-related exclusions.
- Plan for channel exclusions (e.g., interictal epileptiform activity), especially in MTL targets.
- For MTL-focused studies, use validated localization/segmentation pipelines for hippocampus and amygdala.[^iglesias2015][^saygin2017][^stolk2018]
- For multi-region connectivity questions, budget extra recruitment time for clean data in both regions.[^bastos2016]

## 5) Design trial structure carefully
- Choose between blocked and interleaved/event-related designs based on the neural question and confound profile.
- Randomize trial order (or pseudo-randomize with constraints) to reduce order and drift confounds.
- Counterbalance condition order across runs/participants when blocks are used.
- Consider jittered ITIs to reduce temporal predictability and anticipatory activity.
- Match control conditions on difficulty, sensory load, and motor demands when possible.

## 6) Build timing and synchronization correctly
- Use a photodiode marker for visual onset timing.
- Size the photodiode rectangle large enough for stable detection.
- Present photodiode marker at each stimulus onset.
- Do not assume software event timestamps equal on-screen onset; account for display latency and hardware/software jitter.[^stolk2018][^fieldtriphumanecog]
- Do dry runs to characterize latency and jitter before patient recording.

## 7) Implement robust logging and documentation
- Log rich behavioral metadata:
  - Reaction times,
  - Button presses,
  - Any task-relevant movement/interaction measures.
- Keep a procedural checklist for consistent execution across sessions.
- Script patient instructions for consistency (including translated versions if needed).

## 8) Pilot and refine
- Run a behavioral pilot with healthy controls first; analyze and iterate before patient sessions.
- Confirm participants understand instructions and can complete the task as intended.
- Debrief pilots:
  - Confusing instructions?
  - Boredom/fatigue?
  - Unintended strategies?
- Iterate task timing/difficulty before patient sessions.

## 9) Clinical-environment operating rules
- Prioritize patient comfort; pause/stop when needed.
- Minimize interference with clinical workflow and emergency access.
- Prefer setups that can be moved quickly if clinical care needs immediate access.

## 10) Analysis guardrails and common pitfalls
- Avoid too few trials; underpowered designs can severely hamper inference.[^combrisson2022]
- Avoid comparing conditions with systematically different processing times unless modeled explicitly.[^gelmanhill2006][^lvwang2023]
- Avoid unequal trial counts between conditions for power/connectivity comparisons unless corrected statistically.[^bastos2016]
- Distinguish periodic oscillations from aperiodic/evoked effects (do not infer oscillations from averages alone).[^donoghue2021][^specparam][^bycycle]
- Avoid circular analysis (double dipping):
  - Electrode selection,
  - Frequency band selection,
  - ROI selection,
  - Time-window selection,
  - "Task-active" feature selection on the same test data.
- Remember many connectivity methods produce across-trial estimates, not trial-by-trial measures.[^bastos2016][^barnettseth2014]
- Control the false-positive burden with principled modeling and multiple-comparison strategies.[^gelman2012]

## 11) Reproducibility checklist
- Predefine hypotheses and primary analyses.
- Record all design choices and deviations.
- Characterize and report stimulus properties clearly.
- Share task code, timing logs, and analysis scripts where possible.[^stolk2018]

## Quick starter checklist
- Define hypothesis and planned figures.
- Simulate timing and trial counts.
- Verify feasibility under expected exclusions.
- Decide block/event structure + randomization/jitter.
- Implement photodiode and latency checks.
- Build comprehensive behavioral/event logging.
- Pilot, debrief, iterate.
- Run in short, interruptible, patient-safe blocks.
- Analyze with anti-circularity and ERP-vs-oscillation checks.

## References
[^mercier2022]: Mercier, M. R., et al. (2022). *Advances in human intracranial electroencephalography research, guidelines and good practices*. NeuroImage, 260, 119438. https://doi.org/10.1016/j.neuroimage.2022.119438
[^axmacher2023]: Axmacher, N. (Ed.). (2023). *Intracranial EEG: A Guide for Cognitive Neuroscientists*. Springer. https://doi.org/10.1007/978-3-031-20910-9
[^stolk2018]: Stolk, A., et al. (2018). *Integrated analysis of anatomical and electrophysiological human intracranial data*. Nature Protocols, 13(7), 1699-1723. https://doi.org/10.1038/s41596-018-0009-6
[^bastos2016]: Bastos, A. M., & Schoffelen, J.-M. (2016). *A tutorial review of functional connectivity analysis methods and their interpretational pitfalls*. Frontiers in Systems Neuroscience, 9, 175. https://doi.org/10.3389/fnsys.2015.00175
[^lvwang2023]: Lv, P., & Wang, L. (2023). *How can iEEG data be analyzed via multi-level models?* In N. Axmacher (Ed.), *Intracranial EEG* (pp. 579-586). Springer. https://doi.org/10.1007/978-3-031-20910-9_36
[^gelmanhill2006]: Gelman, A., & Hill, J. (2006). *Data Analysis Using Regression and Multilevel/Hierarchical Models*. Cambridge University Press. https://doi.org/10.1017/CBO9780511790942
[^iglesias2015]: Iglesias, J. E., et al. (2015). *A computational atlas of the hippocampal formation using ex vivo, ultra-high resolution MRI: Application to adaptive segmentation of in vivo MRI*. NeuroImage, 115, 117-137. https://doi.org/10.1016/j.neuroimage.2015.04.042
[^saygin2017]: Saygin, Z. M., et al. (2017). *High-resolution magnetic resonance imaging reveals nuclei of the human amygdala: Manual segmentation to automatic atlas*. NeuroImage, 155, 370-382. https://doi.org/10.1016/j.neuroimage.2017.04.046
[^fieldtriphumanecog]: FieldTrip Toolbox. (2026). *Analysis of human ECoG and sEEG recordings*. https://www.fieldtriptoolbox.org/tutorial/intracranial/human_ecog/
[^combrisson2022]: Combrisson, E., et al. (2022). *Group-level inference of information-based measures for the analyses of cognitive brain networks from neurophysiological data*. NeuroImage, 258, 119347. https://doi.org/10.1016/j.neuroimage.2022.119347
[^donoghue2021]: Donoghue, T., Schaworonkow, N., & Voytek, B. (2021). *Methodological considerations for studying neural oscillations*. European Journal of Neuroscience, 55(11-12), 3502-3527. https://doi.org/10.1111/ejn.15361
[^specparam]: fooof-tools. (2026). *specparam (formerly FOOOF): Parameterizing neural power spectra into periodic and aperiodic components*. https://github.com/fooof-tools/fooof
[^bycycle]: bycycle-tools. (2026). *bycycle documentation: cycle-by-cycle analysis of neural oscillations*. https://bycycle-tools.github.io/bycycle/
[^barnettseth2014]: Barnett, L., & Seth, A. K. (2014). *The MVGC multivariate Granger causality toolbox: A new approach to Granger-causal inference*. Journal of Neuroscience Methods, 223, 50-68. https://doi.org/10.1016/j.jneumeth.2013.10.018
[^gelman2012]: Gelman, A., Hill, J., & Yajima, M. (2012). *Why we (usually) don't have to worry about multiple comparisons*. Journal of Research on Educational Effectiveness, 5(2), 189-211. https://doi.org/10.1080/19345747.2011.618213
