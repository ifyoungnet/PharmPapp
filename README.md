# PharmPapp
![GitHub repo size](https://img.shields.io/github/repo-size/ifyoungnet/PharmPapp)
![GitHub License](https://img.shields.io/github/license/ifyoungnet/PharmPapp)
![GitHub watchers](https://img.shields.io/github/watchers/ifyoungnet/PharmPapp?style=social)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/numpy)
![KNIME](https://img.shields.io/badge/KNIME-4.7.2-yellow)

## Peptide Permeability Prediction: A Systematic Investigation Across Cell Lines, Structural Types, and Modifications
## Aims
PharmPapp aims to provide systematic evaluation of peptide permeability across diverse peptides (natural, modified, linear and cyclic) and cell lines (Caco-2, RRCK and PAMPA).
## Models
Five permeability datasets were obtained through systematic data collection (Caco2-L, Caco2-C, Caco2-A, RRCK-C, PAMPA-C). Six algorithms and four types of descriptors or fingerprints were applied in the modeling process. The five optimal models achieved good predictive performance, with an impressive R2 of 0.708, 0.658, 0.484, 0.553 and 0.528 on the test set, respectively.
## Explanation about the files
Five local model files: Caco2-A.zip; Caco2-C.zip; Caco2-L.zip; PAMPA-C.zip; and RRCK-C.zip: Read by ***Model Reader*** node.

Local model normalizer file: RRCK-C_Normalizer.zip: Read by ***Model Reader*** node.

Five example data files: example for Caco2_A.csv; example for Caco2_C.csv; example for Caco2_L.csv; example for PAMPA_C.csv; example for RRCK_C.csv. They can be loaded by ***CSV Reader***.

KNIME workflows: Example regression workflow for Caco2-A.knwf; Example regression workflow for Caco2-C.knwf; Example regression workflow for Caco2-L.knwf; Example regression workflow for PAMPA-C.knwf; Example regression workflow for RRCK-C.knwf.


## How to form your own prediction pipeline: 
The details of constructing your own workflow are shown in Figure 1, Figure 2 and Figure 3. 
Explanation of workflow: 
1) The local model file is read by the Model Reader node above, while the below reads the model-Normalizer.zip for normalizer; 
2) The node of File Reader is used to read the data that needs to be predicted; Please read your data as the examples we provided (example for RRCK-C.csv, example for Caco2-C.csv and example for PAMPA-C.csv). If you just want to predict molecules without experimental values or labels, you should ignore the ‘Permeability’ and disconnect the evaluation nodes for example ‘Numeric Scorer’. 
3) Select the corresponding prediction node according to the model read by the model reader; 
4) Output for the prediction result. In addition, evaluation nodes can be chosen according to your task.

Here is a snapshot:

![snapshot](https://github.com/ifyoungnet/PharmPapp/blob/main/snapshot%20for%20the%20workflow.png)

## Publication
> Xiaorong Tan, Qianhui Liu, Yanpeng Fang, Yingli Zhu, Fei Chen, Wenbin Zeng, Defang Ouyang, Jie Dong. Peptide Permeability Prediction: A Systematic Investigation Across Cell Lines, Structural Types, and Modifications. *Molecular Pharmaceutics*, submitted.

## Contact
  
  * Prof. Jie Dong: <jiedong@csu.edu.cn> 
