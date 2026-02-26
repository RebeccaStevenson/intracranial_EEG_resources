# iEEG Resources

## Intracranial EEG research guides

Mercier, M. R., et al. (2022). **Advances in human intracranial electroencephalography research, guidelines and good practices.** NeuroImage, 260, 119438. [https://doi.org/10.1016/j.neuroimage.2022.119438](https://doi.org/10.1016/j.neuroimage.2022.119438)

Axmacher, N. (Ed.). (2023). **Intracranial EEG: A guide for cognitive neuroscientists.** Springer International Publishing. [https://doi.org/10.1007/978-3-031-20910-9](https://doi.org/10.1007/978-3-031-20910-9)


# General Neurophysiology Analysis Resources

- **Analyzing Neural Time Series Data: Theory and Practice** - Mike X. Cohen  
  - [Textbook](https://www.amazon.com/Analyzing-Neural-Time-Data-Practice/dp/0262019876) (available on Amazon/MIT Press)
    - Covers pre-processing, signal processing, connectivity, analyses, and statistics (permutation testing)
    - [GitHub repository](https://github.com/mikexcohen/AnalyzingNeuralTimeSeries) containing MATLAB code and example scripts accompanying the textbook
  - Video lectures (playlists)
    - [Static signal processing](https://www.youtube.com/watch?v=fYtVHhk3xJ0&list=PLn0OLiymPak2jxGCbWrcgmXUtt9Lbjj_A)
    - [Time series analyses](https://www.youtube.com/watch?v=7ahrcB5HL0k&list=PLn0OLiymPak2BYu--bR0ADNBJsC4kuRWs)
    - [Synchronization](https://www.youtube.com/watch?v=ardi0hO6lOU&list=PLn0OLiymPak1wp4wMQ7tbYrtyFUatMVJs)
    - [Permutation-based statistics](https://www.youtube.com/watch?v=7W11BOlM02I&list=PLn0OLiymPak1Ch2ce47MqwpIw0x3m6iZ7)
- **FieldTrip Toolbox for Neurophysiological Data Analysis**  
  - [FieldTrip Tutorials](https://www.fieldtriptoolbox.org/tutorial/)  
    - [Human ECoG tutorial](https://www.fieldtriptoolbox.org/tutorial/intracranial/human_ecog/)
  - [FieldTrip Discussion List](https://www.fieldtriptoolbox.org/discussion_list/)  
  
- **MNE-Python Toolbox**
  - [MNE Tutorials](https://mne.tools/stable/auto_tutorials/index.html)
  - [Discussion Forum](https://mne.discourse.group/)

# Anatomy and localization

Stolk, A., et al. (2018). **Integrated analysis of anatomical and electrophysiological human intracranial data.** Nature Protocols, 13(7), 1699-1723. [https://doi.org/10.1038/s41596-018-0009-6](https://doi.org/10.1038/s41596-018-0009-6)

Hippocampal segmentation: Iglesias, J. E., et al. (2015). **A computational atlas of the hippocampal formation using ex vivo, ultra-high resolution MRI: Application to adaptive segmentation of in vivo MRI.** NeuroImage, 115, 117-137. [https://doi.org/10.1016/j.neuroimage.2015.04.042](https://doi.org/10.1016/j.neuroimage.2015.04.042).

Amygdala segmentation: Saygin, Z. M., Kliemann, D., & Iglesias, J. E. (2017). **High-resolution magnetic resonance imaging reveals nuclei of the human amygdala: Manual segmentation to automatic atlas.** NeuroImage, 155, 370-382. [https://doi.org/10.1016/j.neuroimage.2017.04.046](https://doi.org/10.1016/j.neuroimage.2017.04.046).

- **Toolboxes**
  - [FreeSurfer](https://surfer.nmr.mgh.harvard.edu/)

# Signal processing

- **Toolboxes**
  - [SpecParam (aka FOOOF)](https://github.com/fooof-tools/fooof)
    - **Description:** A Python toolbox for parameterizing neural power spectra into periodic & aperiodic components
  - [Bycycle](https://bycycle-tools.github.io/bycycle/)
    - **Description:** A Python package for quantifying features of neural oscillations in the time domain, as opposed to the frequency domain, using a cycle-by-cycle approach.

- **Additional resources**
  - [Methods for analyzing neural oscillations and aperiodic activity](https://www.youtube.com/watch?v=bRsMdtldwpQ&t=2139s) – Brad Voytek's SPR lecture
  - [Circles, Sines, and Signals](https://jackschaedler.github.io/circles-sines-signals/) – Visual guide to signal representation
  - [Oscillation Methods](https://oscillationmethods.github.io/docs/index.html) - online version of the code and figures for the [methodological considerations for studying neural oscillations](https://onlinelibrary.wiley.com/doi/10.1111/ejn.15361) project



# Connectivity and causality

Bastos, A. M., & Schoffelen, J.-M. (2016). **A tutorial review of functional connectivity analysis methods and their interpretational pitfalls.** Frontiers in Systems Neuroscience, 9, 175. [https://doi.org/10.3389/fnsys.2015.00175](https://doi.org/10.3389/fnsys.2015.00175)

Pagnotta, M. F., et al. (2018). **Assessing the performance of Granger-Geweke causality: Benchmark dataset and simulation framework.** Data in Brief, 16, 743-747. [https://doi.org/10.1016/j.dib.2017.12.045](https://doi.org/10.1016/j.dib.2017.12.045)

Pagnotta, M. F., et al. (2018). **Benchmarking nonparametric Granger causality: Robustness against downsampling and influence of spectral decomposition parameters.** NeuroImage, 183, 478-494. [https://doi.org/10.1016/j.neuroimage.2018.08.019](https://doi.org/10.1016/j.neuroimage.2018.08.019)

Sameshima, K., & Baccalá, L. A. (Eds.). (2014). **Methods in brain connectivity inference through multivariate time series analysis.** CRC Press.

- [MVGC Toolbox](https://github.com/lcbarnett/MVGC1?tab=readme-ov-file#readme)
  - Barnett, L., & Seth, A. K. (2014). The MVGC multivariate Granger causality toolbox: A new approach to Granger-causal inference. *Journal of Neuroscience Methods, 223*, 50–68. https://doi.org/10.1016/j.jneumeth.2013.10.018.


# Statistics


Gelman, A., & Hill, J. (2007). **Data Analysis Using Regression and Multilevel/Hierarchical Models.** Cambridge University Press. [https://doi.org/10.1017/CBO9780511790942](https://doi.org/10.1017/CBO9780511790942)

Gelman, A., Hill, J., & Yajima, M. (2012). **Why we (usually) don't have to worry about multiple comparisons.** Journal of Research on Educational Effectiveness, 5(2), 189-211. [https://doi.org/10.1080/19345747.2011.618213](https://doi.org/10.1080/19345747.2011.618213)

Combrisson, E., et al. (2022). **Group-level inference of information-based measures for the analyses of cognitive brain networks from neurophysiological data.** NeuroImage, 258, 119347. [https://doi.org/10.1016/j.neuroimage.2022.119347](https://doi.org/10.1016/j.neuroimage.2022.119347)

Lv, P., & Wang, L. (2023). **How can iEEG data be analyzed via multi-level models?** In N. Axmacher (Ed.), Intracranial EEG. Studies in Neuroscience, Psychology and Behavioral Economics. Springer. [https://doi.org/10.1007/978-3-031-20910-9_36](https://doi.org/10.1007/978-3-031-20910-9_36)

Mathis, M. W., Perez Rotondo, A., Chang, E. F., Tolias, A. S., & Mathis, A. (2024). **Decoding the brain: From neural representations to mechanistic models.** Cell, 187(21), 5814-5832. [https://doi.org/10.1016/j.cell.2024.08.051](https://doi.org/10.1016/j.cell.2024.08.051)



- **Toolboxes/functions**
  - **R studio**: [lme4](https://cran.r-project.org/web/packages/lme4/index.html), [brms](https://cran.r-project.org/web/packages/brms/index.html)
  - **MATLAB**: [fitlme](https://www.mathworks.com/help/stats/fitlme.html), [fitglme](https://www.mathworks.com/help/stats/fitglme.html)
  - **Python**: [statsmodels](https://www.statsmodels.org/)

- **Additional resources**
  - [Bodo Winter's LME tutorial](https://bodowinter.com/tutorial/bw_LME_tutorial2.pdf)  
  - [Coding Club primer on mixed effects modeling](https://ourcodingclub.github.io/tutorials/mixed-models/)
  
# Single unit analyses

Fried, I., Rutishauser, U., Cerf, M., & Kreiman, G. (Eds.). (2014). **Single Neuron Studies of the Human Brain: Probing Cognition.** The MIT Press. [https://mitpress.mit.edu/9780262027205/single-neuron-studies-of-the-human-brain/](https://mitpress.mit.edu/9780262027205/single-neuron-studies-of-the-human-brain/)

Kramer, M. A., & Eden, U. T. (2016). **Case Studies in Neural Data Analysis: A Guide for the Practicing Neuroscientist.** The MIT Press. [https://mitpress.mit.edu/9780262529372/case-studies-in-neural-data-analysis/](https://mitpress.mit.edu/9780262529372/case-studies-in-neural-data-analysis/)

- **Additional resources**
  - [Introduction to Neural Computation](https://ocw.mit.edu/courses/9-40-introduction-to-neural-computation-spring-2018/)
    - **Description:** A course offered through MIT OpenCourseWare that covers various topics in neural computation, including single-neuron analyses.

# Hyperscanning

Wang, J., Meng, F., Xu, C., Zhang, Y., Liang, K., Han, C., Gao, Y., Yu, X., Li, Z., Zeng, X., Ni, J., Tan, H., Yang, J., & Ma, Y. (2025). **Simultaneous intracranial recordings of interacting brains reveal neurocognitive dynamics of human cooperation.** Nature Neuroscience, 28(1), 161-173. [https://doi.org/10.1038/s41593-024-01824-y](https://doi.org/10.1038/s41593-024-01824-y)


# AI tools
- [Cursor AI](https://www.cursor.so/)
- [GitHub Copilot](https://github.com/features/copilot)
- [ChatGPT](https://chat.openai.com/), [Claude](https://www.anthropic.com/index/claude)
- [Notebook LM](https://notebooklm.google.com/)
- [Consensus](https://consensus.app/)
