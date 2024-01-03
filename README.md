# **Kepler Exoplanet Candidates**

In this project, I explore and use the Kepler from the NASA Exoplanet Archive: http://exoplanetarchive.ipac.caltech.edu

The dataset contains information about Data Columns in Kepler Objects of Interest. It has the following features

['koi_pdisposition', 'koi_score', 'koi_fpflag_nt', 'koi_fpflag_ss',
       'koi_fpflag_co', 'koi_fpflag_ec', 'koi_period', 'koi_period_err1',
       'koi_period_err2', 'koi_time0bk', 'koi_time0bk_err1',
       'koi_time0bk_err2', 'koi_impact', 'koi_impact_err1', 'koi_impact_err2',
       'koi_duration', 'koi_duration_err1', 'koi_duration_err2', 'koi_depth',
       'koi_depth_err1', 'koi_depth_err2', 'koi_prad', 'koi_prad_err1',
       'koi_prad_err2', 'koi_teq', 'koi_insol', 'koi_insol_err1',
       'koi_insol_err2', 'koi_model_snr', 'koi_tce_delivname', 'koi_steff',
       'koi_steff_err1', 'koi_steff_err2', 'koi_slogg', 'koi_slogg_err1',
       'koi_slogg_err2', 'koi_srad', 'koi_srad_err1', 'koi_srad_err2', 'ra',
       'dec', 'koi_kepmag']

More information about the definitions can be found on: https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html

## Target Variable
The column 'koi_pdisposition' indicates whether Kepler Object of Interest (KOI) is a CANDIDATE or a FALSE POSITIVE.

## Features
As explained in the attached notebook, after some Exploratory Data Analysis (EDA) and handling of the null values, we are left with the following subset of the above columns that are used to train and predict whether the given KOI is classified as a CANDIDATE or a FALSE POSITIVE.

## Model Building
We built a Neural Network using TensorFlow and Keras libraries with an architecture of 35 --> 20 --> 10 --> 5 --> 1 layers in the neural network. The final neuron has a sigmoid activation which predicts the probability of a KOI to be a CANDIDATE exoplanet. The model is trained using the 'binary_crossentropy' loss function and the 'adam' optimizer.

## Evaluatio
