# PhotometricRedshift
Estimate the photometric redshift using a weighted-ensemble of Machine Learning models.

The ensemble includes k-Nearest Neighbors, XGBoost, Support Vector Machine, lightGBM, and an Orthogonal Distance Regression method based on ODRpack, which can account in the fit the errors for the predictor values.
The meta prediction is the weighted sum of the different predictions, where the weights are inversely proportional to the root-mean-square.
The expansion of the Universe makes that objects farther away from us are receding, resulting in a Doppler shift of their electromagnetic emission towards lower frequencies (hence redshift). wikipedia
Obtaining spectroscopic redshifts is a time-consuming endeavor compared to photometric redshifts, except that spectroscopic redshifts are much more precised and accurate. The challenge is to find the most precise and accurate photometric redshift determinations.
The data is described in Section 1.5.5 of Ref 1. The training set consists of u, g , r, i, z magnitudes and their associated erros of 60,000 galaxies from the SDSS spectroscopic sample from a total of ~600,000 galaxies.
Validation is performed on an additional 6000 galaxies. The left panel shows prediction error as a function of the spectroscopic redshift computed by Monte-Carlo simulation.

Here are the results for the train data

![fig_photoz_Ensemble_train](https://github.com/wfthi/PhotometricRedshift/assets/94956037/f3037ada-c55f-4b14-95ae-c9dce63263c4)

And here are the results for the test data

![fig_photoz_Ensemble_test](https://github.com/wfthi/PhotometricRedshift/assets/94956037/76d6c6ca-1bfa-41f9-a840-2490500b7353)

