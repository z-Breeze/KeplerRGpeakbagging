# Massive peak bagging of red giants in the Kepler field

A library of frequencies, amplitdes, and lifetimes of more than 250,000 individual l=0 to 3 oscillations modes of 6179 red giants from APOKASC sample. The parameters were extracted with the Automated Bayesian peak-Bagging Algorithm (ABBA).

Visulaisations (two pdf files per star) of the results are located in the directories *EchellePlots* and *SpectrumPlots*

The modefiles contains general information about the star in the header:
- *fmax*: The frequency of the maximum oscillation power in microHz as defined in Eq.2 in [Kallinger et al. (2014)](https://ui.adsabs.harvard.edu/abs/2014A%26A...570A..41K/abstract) with two super-Lorentzian functions with a fixed exponent of four. The 1 sigma uncertainty is given as fmax_e.
- *dnu*, *dnu02*, and *f_c*: The larger and small frequency separation determine in the central three radial modes around fmax and the frequency of the central radial mode as defined in Eq.2 of [Kallinger et al. (2010)](https://ui.adsabs.harvard.edu/abs/2010A%26A...509A..77K/abstract). All parameters are in microHz.
- *dnu_cor* and *alpha*: Values of the curvature corrected large separation in microHz and the corresponding dimensionless curvature parameter as defined in Eq.,4 of [Kallinger et al. (2018)](https://ui.adsabs.harvard.edu/abs/2018A%26A...616A.104K/abstract).
- *evo*: Evolutionary stage of the star determined from the phase shift of the central radial mode ([Kallinger et al. 2012](https://ui.adsabs.harvard.edu/abs/2012A%26A...541A..51K/abstract)) with 0 - RGB star, 1 - RC star, 2 - secondary clump star, and 3 - AGB star.

The individual mode parameters are given in the main block:
- *l*: mode degree
- *freq*: mode frequency in microHz
- *amp*: rms amplitude of the mode in ppm (i.e. the square root of the integrated power density under the mode profile)
- *tau*: mode lifetime in days (0 for unresolved modes fitted with a squared sinc-function)
- *ev* and *ev1*: mode evidence (i.e. the probability that the mode is not due to noise). A useful threshold is 0.91, which corresponds to *strong evidence* in probability theory. The *ev1* parameter is only valid for l=1 modes. 


To download the full repository (~650MB) type the following command 
```
git clone https://github.com/tkallinger/KeplerRGpeakbagging.git
```
Individual mode files can be downloaded using the Python function *read_modefile.py*

A summary of the global seismic parameters of all stars in the library is given in the file *summary.dat*
ID;fmax;fmax_e;dnu_cor;dnu_cor_e;dnu02;dnu02_e;fm;fm_e;dnu;dnu_e;alp;alp_e;evo

More details may be found in <arXiv link>

For further informations please contact me at tkallinger@me.com
