# Paper Abstract

We analyze the Pantheon+ Type Ia supernova dataset allowing for a transition in the standardized absolute magnitude \( M \) at a characteristic distance scale inferred directly from the data. This transition was first introduced and investigated by Perivolaropoulos & Skara using a frequentist \( \chi^2 \) minimization approach in the context of a flat \( \Lambda \)CDM cosmological background, including tests of low-redshift systematics such as the volumetric redshift scatter bias.  

Here, we build upon and extend their analysis by examining the inferred transition within both frequentist and Bayesian statistical frameworks, and by exploring its impact on cosmological parameter estimation in flat \( \Lambda \)CDM, \( w_0 \)CDM, and CPL models, as well as within a cosmographic expansion of the luminosity distance up to second order in redshift. Both frequentist and Bayesian approaches are employed, including \( \chi^2 \) minimization with AIC and BIC information criteria, Markov Chain Monte Carlo sampling, and nested sampling for parameter estimation and model comparison.  

Across all models, the data favor the presence of two distinct absolute-magnitude populations separated by  
\[
\Delta M = M_{>} - M_{<} \simeq 0.19~\mathrm{mag},
\]
corresponding to a brighter local population (\( M_{<} \)) at distances below  
\[
d_{\mathrm{crit}} \approx 20~\mathrm{Mpc}.
\]
The inclusion of this transition leads to a statistically significant improvement in the quality of fit, while leaving most cosmological parameters largely unaffected. The most pronounced impact is a systematic increase of the inferred Hubble constant, with \( H_0 \) rising by approximately \( 2\% \) across all tested models. In all cases, the best-fit transition scale is consistently found near \( 20~\mathrm{Mpc} \), indicating a persistent low-redshift deviation from homogeneous SNe Ia standardization within the tested frameworks.

---

## Repository Structure and Contents

The repository contains the analysis code, derived statistical results, and plotting utilities used in the accompanying paper.

- **Final Plots**  
  All plots appearing in the paper.

- **Saved Samples** & **contour_data**  
  Stored `.npy` and `.npz` files containing posterior samples and parameter-space contour data for each model.  
  These files include **only derived statistical results** and **do not contain supernova-level data**.

- **LCDM_chi_square.ipynb**  
  LCDM model parameter inference using a standard **chi-square minimization** with and without a transition in **M**, and model comparison between the two.

- **LCDM_MCMC&NestedSampling.ipynb**  
  LCDM model parameter inference using Bayesian inference via **MCMC** for posterior samples and **Nested Sampling** for model comparison, considering the original model and a transition in **M**.

- **Removal_of_z<0.01_LCDM.ipynb**  
  LCDM model parameter inference using a standard **chi-square minimization**, removing all non-Cepheid SNe with \( z < 0.01 \), to account for the volumetric redshift scatter bias effect.

- **q0_chi_square.ipynb**  
  Cosmographic expansion up to second order parameter inference using a standard **chi-square minimization** with and without a transition in **M**, and model comparison between the two.

- **q0_MCMC.ipynb**  
  Cosmographic expansion up to second order parameter inference using Bayesian inference via **MCMC** for posterior samples and **Nested Sampling** for model comparison, considering the original model and a transition in **M**.

- **w0_CDM_chi_square.ipynb**  
  \( w_0 \)CDM model parameter inference using a standard **chi-square minimization** with and without a transition in **M**, and model comparison between the two.

- **w0CDM_MCMC.ipynb**  
  \( w_0 \)CDM model parameter inference using Bayesian inference via **MCMC** for posterior samples and **Nested Sampling** for model comparison, considering the original model and a transition in **M**.

- **CPL_model.ipynb**  
  CPL model parameter inference using Bayesian inference via **MCMC** for posterior samples and **Nested Sampling** for model comparison, considering the original model and a transition in **M**.

---

## Data Availability

All analyses rely on derived statistical quantities only. Users must obtain the Pantheon+ data directly from the official collaboration sources in order to reproduce the results.

---

## License

All code and derived results in this repository are released under the **MIT License**.  
See the `LICENSE` file for details.
