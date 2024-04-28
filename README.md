# PharmPapp
![GitHub repo size](https://img.shields.io/github/repo-size/ifyoungnet/PharmPapp)
![GitHub License](https://img.shields.io/github/license/ifyoungnet/PharmPapp)
![GitHub watchers](https://img.shields.io/github/watchers/ifyoungnet/PharmPapp?style=social)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/numpy)
![KNIME](https://img.shields.io/badge/KNIME-4.3.3-yellow)

## Peptide Permeability Prediction: A Systematic Investigation Across Cell Lines, Structural Types, and Modifications
##### PharmPapp aims to provide systematic prediction of peptide permeability.
## How to form your own prediction pipeline: 
The details of constructing your own workflow are shown in Figure 1, Figure 2 and Figure 3. 
Explanation of workflow: 
1) The local model file is read by the Model Reader node above, while the below reads the model-Normalizer.zip for normalizer; 
2) The node of File Reader is used to read the data that needs to be predicted; Please read your data as the examples we provided (example for RRCK-C.csv, example for Caco2-C.csv and example for PAMPA-C.csv). If you just want to predict molecules without experimental values or labels, you should ignore the ‘Permeability’ and disconnect the evaluation nodes for example ‘Numeric Scorer’. 
3) Select the corresponding prediction node according to the model read by the model reader; 
4) Output for the prediction result. In addition, evaluation nodes can be chosen according to your task.
