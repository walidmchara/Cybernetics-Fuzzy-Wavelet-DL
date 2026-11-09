# Experimental reproducibility

**Study:** Cybernetic Deep Learning and Fuzzy Clustering Framework for Dynamic Solar Irradiance Forecasting in Intelligent Vehicle Energy Systems  
**DOI:** https://doi.org/10.1080/01969722.2026.2673537

## Scope of implementation

The code integrates fuzzy-regime descriptors with wavelet-oriented temporal modeling and a recurrent forecasting head.

The recurrent dimensions, regime construction, wavelet parameters and weather-condition groupings must be checked against the published experimental protocol.

## Data handling and evaluation

Measured data are supplied as an external time-ordered CSV rather than packaged with the source code. Normalization statistics and fuzzy-regime parameters, where used, must be fitted on training observations only. Input windows must not include future target values.

The default training workflow uses chronological partitions for model development, residual calibration (when applicable), validation and final evaluation. Multiple cities, sites, meteorological regimes or horizons need separately documented holdout protocols; a successful single-series run is not evidence of generalization.

## Reporting requirements

A repeatable experiment records the source dataset and its license, feature definitions, sampling period, target units, forecast horizon, random seeds, optimizer budget, train/test boundaries and all metric definitions. The software check `python train.py --smoke` uses simulated signals and serves only to validate execution.

Paper-level numerical agreement has not been independently established. The results of new runs should be reported as new experiments, with explicit comparison settings rather than attributed to the published results.
