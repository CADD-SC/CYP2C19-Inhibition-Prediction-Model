# CYP2C19-Inhibition-Prediction-Model
Machine learning-based prediction model for CYP2C19 inhibition prediction

## Introduction ## 

Welcome to our repository, here we provide machine learning model to efficiently predict the CYP2C19 inhibition of target drug compounds in early stage of drug discovery process. CYP2C19 is another important member of the Cytochrome P450 enzyme family, playing a crucial role in the metabolism of several drugs, including proton pump inhibitors, antiepileptics, and certain antidepressants. Inhibition of CYP2C19 can significantly alter the pharmacokinetics of these medications, leading to increased risk of side effects and drug toxicity.

## Classification criteria ##
The model uses an IC<sub>50</sub> threshold:

</strong> If <em>IC<sub>50</sub></em> < 10 μM, the compound is <strong>Inhibitor</strong> and belongs to class 1. If <em>IC<sub>50</sub></em> ≥ 10 μM, it is <strong>Not an Inhibitor</strong> and belongs to class 0.

## Dependencies ##

- Python ≥ 3.9
- scikit-learn ≥ 1.26.4
- numpy == 11.5.0
- hpsklearn == 1.0.3
- hyperopt == 0.2.7
- xgboost == 2.0.3
- rdkit
- pandas

## Execution ##
**To run the prediction:**

```
$ python model.py --prediction --file_name [filename] --model_path CYP2C19.pkl
```
<strong>Note:</strong> For the prediction step, prepare a .csv file containing SMILES without bioclass (e.g., test_set.csv)

**To run the validation:**

```
$ python model.py --validation --file_name [filename] --model_path CYP2C19.pkl
```
<strong>Note:</strong> For the validation step, prepare a .csv file containing SMILES with bioclass (0 or 1) (e.g., valid_set.csv)

**Output:**

Our model generates output in binary value (1 or 0), where 1 indicates compound to be permeable, while 0 indicates non-permeable.

 
**Please ensure that all the necessary files (CYP2C19.pkl, data_preprocessing.py, scaler, features.txt, input_file.csv, model.py) are kept in the working directory**

**To download the prediction model file (CYP2C19.pkl), please refer to the "Tags --> v2.3.4" tab**
