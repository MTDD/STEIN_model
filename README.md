# STEIN_model

MODEL INFORMATION

Quantifying erosion rates in high mountain areas is not straightforward due to the stochastic processes which often dictate alpine erosion rates. Among those, frost-cracking and permafrost thaw both contribute to erosion rates in cold, high-alpine regions, but the relative contributions of both are not well-constrained. The STEIN model (stochastically-eroding in situ cosmogenic nuclide model) is a 1D numerical model that simulates surface concentrations of cosmogenic Be-10, C-14, and He-3, alongside the bedrock thermal field, under variable erosion rates and types. Simulations can evolve under the following erosion types: “stochastic,” “uniform,” "episodic," and "no erosion." Each non-uniform erosion scenario is accompanied by a uniformly-eroding output at the Be-10 derived erosion rate. The scripts in this text can be used to reproduce the results of Dennis and Scherler (2022) using the parameter values listed in Appendices A and B of that publication.

To run the model, download the scripts and open the file 'STEINwrapper.ipynb'. Be sure this file is in the same folder as the folder containing all of the other functions. Within the STEINwrapper script, values for the following parameters can be defined:

-Total Time,
-Erosion Rate,
-Scenarios,
-Pareto Shape Parameter (c),
-Mean Annual Temperature,
-Seasonal Temperature Amplitude.

All other variables can be adjusted in the file SetParams.ipynb, which contains the function defining the constant values.

The model is run using the functions RunSimulationsStoch(), RunSimulationsEpisodic(), or RunSimulationsConstant(), depending on which style of erosion is desired. The corresponding files for these functions are RunSimulationsStoch.ipynb, RunSimulationsEpisodic.ipynb, and RunSimulationsConstant.ipynb. The syntax for each of these functions is defined at the top of the respective files.

The scripts will generate a sequence of output files which are automatically saved using the save_fxn(). The model can take some time for each individual evaluation (up to several hours), depending on the integration time (total model time) input.

References:
Dennis, D. and Scherler, D. (2022), A Combined Cosmogenic Nuclides Approach for Determining the Temperature-Dependence of Erosion, in press.
