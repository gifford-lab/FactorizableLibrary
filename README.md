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

#### GPU: 
- The following instructions require access to GPUs with CUDA support. If a user does not have access, please use the Google Colab notebooks provided below to run SAPS.

#### Install dependencies: 
Using conda: 
```
conda create -n factorizable
conda activate factorizable
conda install --file requirements.txt
```

Using pip:
```
pip install -r requirements.txt
```

#### Train model in notebook
After installing dependencies, open Jupyter notebook: 
```
cd FactorizableLibrary/
jupyter notebook model_training/TrainModel.ipynb
```
Follow instructions in the notebook to run each cell and train a model. You can use one of the datasets provided in `data/`, or you can generate your own *.pkl data file and replace the path in the execution portion of the notebook. 

#### Generate model in notebook
Once you have trained a model, it should be stored in `weights/`. Next, open the script for library generation. 
```
jupyter notebook library_generation/GenerateLibrary.ipynb
```
Follow instructions in the notebook to run each cell and generate a SAPS library. You can change the path to different model weights files to change the optimization objective of the library. You can also adjust the entropy parameter as specified in the notebook.

## Google CoLab demos
We have provided demo notebooks in which example models can be trained using pu\
blicly available Google GPUs for illustrative purposes. These can be accessed h\
ere:
- TrainModel-demo: https://colab.research.google.com/drive/1wLpSYQOW_uiTXaaSz_r\
HVYrtNZEKCbB_?usp=sharing
- GenerateLibrary-demo: https://colab.research.google.com/drive/1eunbFA1dkTKF6d\
cp1qu_4rKAPOhG2xmo?usp=sharing
