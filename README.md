# PyHHB: Physiological-based estimations of human survivability and liveability to heat in a changing climate

This repository includes the Python Human Heat Balance (PyHHB) codes to assess survivability and liveability to heat by applying a human-environment heat exchange model intended to be used with climate model output data developed by Vanos et al. (2023). The source code available here helps to replicate the survivability (Figures 2, S2, S3) and liveability (Figures 4, S6, S7) matrices for the environmental and personal features included in the study.
In Vanos et al. (2023), the framework for heat survivability modeling was improved from the generalized use of wet bulb temperature (Tw) of 35°C as a limit to heat-stroke survival (Sherwood and Huber, 2010), and it was introduced an approach to assess liveability due to extreme heat exposure that can be applied in any climate regime and customized with population groups with potential co-morbidities. This new approach integrates well-established and fundamental principles from thermal physiology and human biophysics and accommodates 3- hand 6-h exposure windows aligning with outputs from climate models and past survivability studies.
For detailed information about the differences between this approach and the wet bulb temperature limit of 35°C, read the session "Considerations of New Model Estimating Physiological Survivability Limits and Liveability" in the paper's Supplemental material.

## How is defined the survivability limit?

The limit of survivability to heat stroke death is determined by detecting the conditions in which a person would reach a core temperature of 43°C in 3- or 6-hour exposure windows to allow for comparison with the Tw of 35°C assumption (heat stroke death after 6 hours) used in previous survivability assessments based on (Sherwood and Huber, 2010). 

## How is the maximum internal heat production (Mmax) defined as a liveability metric?

Mmax is the maximum safe internal heat production, or level of physical activity, that a person can generate without a sustained positive rate of heat storage in the prevailing environment, thus allowing safe, sustained work and play for an extended period.

## What does this repository contain?

- *Ancillary:* This folder contains necessary supporting images for the Mmax scale illustrating different activity levels based on metabolic equivalent units (Ainsworth et al., 2011). It also includes the matrices with pre-calculated Tw using the Davies-Jones method (Davies-Jones, 2008) to allow direct graphic comparison with the isothermal Tw=35°C in the tutorial for survivability matrix estimation.
- *Codes:*  This folder contains a Python script called HHB.py to be invoked in further routines as the PyHHB module (import HHB as PyHHB), and two Jupyter notebooks with tutorials to replicate the survivability (Figures 2, S2, S3) and liveability (Figure 4, S6, S7) matrices for the environmental and personal features included in the study. The equations to apply the human-environment exchange model in HHB.py follow the notation and rationale from Vanos et al. (2023) and Cramer and Jay (2019).
- *Outputs:* This folder contains the output files generated after running the tutorials.
- *Personal profiles:*  This folder contains text files that include the information required for setting up anthropometrics, activities, and clothing for a target population.
If you want to run this on your computer, we recommend running the survivability tutorial first once the survivability outputs are input for liveability analysis.

*Bibliography:*
Ainsworth, B. E., W. L. Haskell, S. D. Herrmann, N. Meckes, D. R. Bassett, C. Tudor-Locke, J. L. Greer, J. Vezina, M. C. Whitt-Glover, and A. S. Leon. 2011. 2011 compendium of physical activities: A second update of codes and MET values. Medicine and Science in Sports and Exercise, 43(8):1575–1581, https://doi.org/10.1249/MSS.0b013e31821ece12.
Cramer, M. N., and O. Jay. 2019. Cores of reproducibility in physiology partitional calorimetry. Journal of Applied Physiology, 126(2):267–277, https://doi.org/10.1152/japplphysiol.00191.2018.
Davies-Jones, R. 2008. An Efficient and Accurate Method for Computing the Wet-Bulb Temperature along Pseudoadiabats. Monthly Weather Review, 136(7):2764–2785, https://doi.org/https://doi.org/10.1175/2007MWR2224.1.
Sherwood, S. C., and M. Huber. 2010. An adaptability limit to climate change due to heat stress. Proceedings of the National Academy of Sciences of the United States of America, 107(21):9552–9555, https://doi.org/10.1073/pnas.0913352107.
Vanos, J., Guzman-Echavarria, G., Baldwin, J. W., Bongers, C., Ebi, K. L., & Jay, O. (2023). A physiological approach for assessing human survivability and liveability to heat in a changing climate. Nature Communications, XX(XX), XX. https://doi.org/XXXXX
