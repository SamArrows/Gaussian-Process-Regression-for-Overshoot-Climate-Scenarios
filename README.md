The core notebooks for training models have -GP in their titles. Note that the notebooks are set up to load data directly on JASMIN --> you would need to change the file paths to load the downloaded datasets if not using JASMIN. These datasets are far too large and are not included in submission.

For training error correction GP, run the LSTM-GP notebook with train error corrector set to true in the top cells. Also choose which region, by searching for nums_of_interest in the notebook, going to the middle, and setting the number to correspond with AR6 regions https://regionmask.readthedocs.io/en/stable/defined_scientific.html#ar6-regions

Note that we can also remove ocean or land pixels during the error correction modelling by toggling these boolean values at the top of the notebook.

For training other diagnostics, set metric to "tas={metric}" or "tas,rtmt={metric}"; use "tas" to predict tas by itself.

The plot_rasters is for EO visualisation used in the final fig to highlight future work. Data provided should allow for some of the constituent plots to be recreated.
_plotting handles some other plots, such as the lat-lon cross-sectional plots.
