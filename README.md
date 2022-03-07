# FactorizableLibrary

## Folder contents
#### `model_training/`:

- `data/`: contains datasets for each	target presented in manuscript
    - *.csv: sequence data with target enrichment labeled by train/test splits
    - *.pkl: easy	loading	pickle file with train/test splits for training
- `weights/`: output folder for trained weights
-_TrainModel.ipynb_: notebook containing functions for training scoring models for later use in SAPS
-_encoding.pkl_: sequence encoding used for training

#### `library_generation`:
- _GenerateLibrary.ipynb_: notebook containing functions to generate SAPS-designed library 

## Instructions for running notebooks

## Google CoLab demos
We have provided demo notebooks in which example models can be trained using publicly available Google GPUs for illustrative purposes. These can be accessed here:
- TrainModel-demo: https://colab.research.google.com/drive/1wLpSYQOW_uiTXaaSz_rHVYrtNZEKCbB_?usp=sharing
- GenerateLibrary-demo: https://colab.research.google.com/drive/1eunbFA1dkTKF6dcp1qu_4rKAPOhG2xmo?usp=sharing