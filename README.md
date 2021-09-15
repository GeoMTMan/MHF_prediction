# MHF_prediction
Prediction of marine heat flow based on the random forest method and geological and geophysical features

## Data set description
**Features.csv**: Geological and geophysical features used to predict HF in the oceanic crust. Data sources：Müller et al. (2008); Amante and Eakins (2008); Szwillus et al. (2019); Afonso et al. (2019); Goutorbe et al. (2011); Zingerle et al. (2020); Sinem Ince et al. (2019); Alekseev et al. (2015); Montelli et al. (2006); Hosseini et al. (2018); 	Coffin et al. (1997).

**NGHF.csv**: The heat flow data are from A new global heat flow database (NGHF). Reference: Lucazeau F (2019) Analysis and mapping of an updated terrestrial heat flow data set. Geochem Geophys Geosyst 20(8):4001–4024
## Model description
Given the measurement quality information provided by the NGHF database, we generate three data sets containing A-rated (N = 3038), A- and B-rated (N = 6703), and A-, B- and C-rated (N = 10,263).

1. ***.pkl**:the MHF predictors obtained after training on different datasets. The trained model in pkl format can be imported via sklearn. A specific example is as follows. 

  `import joblib`

  `rf_reg = joblib.load('rf_reg_A.pkl') `
  
  The predictor can be used to make MHF predictions as long as the required feature data is provided. Feature data should include:'Ocean crust age', 'Topography', 'Moho depth', 'LAB',
       'Lithosphere thickness', 'Rho_Crust', 'Rho_Lithosphere',
       'Rho_Asthenosphere', 'Geoid', 'Gravity_anomaly_freeair',
       'Gravity_anomaly_bg', 'Log_Conductivity_5Km', 'Log_Conductivity_10Km',
       'Log_Conductivity_50Km', 'Log_Conductivity_100Km', 'Vs_anomaly_20km',
       'Vs_anomaly_80km', 'Vs_anomaly_140km', 'Vp_anomaly_20km',
       'Vp_anomaly_80km', 'Vp_anomaly_140km', 'Distance to ridge',
       'Mean distance to volcanoes'. Global oceanic feature data is available in the **Data set folder**. Of course you can also try to find regional, higher resolution feature data.

2. MHF predictions are given in pdf, grd, xyz file formats.

## Citation
If you make use of this research in published work, please cite Li *et al.* (2021).

## References
Li, M., Huang, S., Dong, M. et al. Prediction of marine heat flow based on the random forest method and geological and geophysical features. Mar Geophys Res 42, 30 (2021). https://doi.org/10.1007/s11001-021-09452-y
