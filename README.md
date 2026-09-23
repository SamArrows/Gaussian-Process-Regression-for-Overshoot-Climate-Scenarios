The core notebooks for training models have -GP in their titles. Note that the notebooks are set up to load data directly on JASMIN --> you would need to change the file paths to load the downloaded datasets if not using JASMIN. These datasets are far too large and are not included in submission.

For training error correction GP, run the LSTM-GP notebook with train error corrector set to true in the top cells. Also choose which region, by searching for nums_of_interest in the notebook, going to the middle, and setting the number to correspond with AR6 regions https://regionmask.readthedocs.io/en/stable/defined_scientific.html#ar6-regions

Note that we can also remove ocean or land pixels during the error correction modelling by toggling these boolean values at the top of the notebook.

For training other diagnostics, set metric to "tas={metric}" or "tas,rtmt={metric}"; use "tas" to predict tas by itself.

The plot_rasters is for EO visualisation used in the final fig to highlight future work. Data provided should allow for some of the constituent plots to be recreated. 
_plotting handles some other plots, such as the lat-lon cross-sectional plots.

The cnn-gp-outputs folder contains some of the results in numpy files from different models, which the plotting notebooks should automatically be able to read and plot, recreating plots in the paper.

--------
Citations for the EO folder's data:
- Soil Moisture ==> Reichle, R., De Lannoy, G., Koster, R., Crow, W., Kimball, J., Liu, Q., Bechtold, M., 2025. Smap l4
global 3-hourly 9 km ease-grid surface and root zone soil moisture geophysical data, version 8. URL:
https://nsidc.org/data/spl4smgp/versions/8, doi:10.5067/T5RUATAQREF8.

- Canopy Height ==> Simard, M., Pinto, N., Fisher, J.B., Baccini, A., 2011. Mapping forest canopy height globally with
spaceborne lidar. Journal of Geophysical Research: Biogeosciences 116

- Population Density ==> CIESIN - Center for International Earth Science Information Network - Columbia University, 2017. Gridded Population of the World, Version 4 (GPWv4): Population Density, Revision 11 (Version 4.11). NASA Socioeconomic Data and Applications Center (SEDAC), Palisades, NY. Available at: https://doi.org/10.7927/H49C6VHW [Accessed 4 August 2026].
