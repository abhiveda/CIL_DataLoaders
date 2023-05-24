###### CIL_DataLoaders
DataLoaders for Class Incremental Learning on Medical Images

For each Dataset requirements file is present in sub-folder.

#### BraTS_2021 -
1. Store the data in sub folder with following name - /home/whr/Data/BraTS/brats21/RSNA_ASNR_MICCAI_BraTS2021_TrainingData/
2. Install Requirements
3. Check configs.py for setup configurations and argument options, defaults are present in the file as well. Run train_brats2021.py

#### M&M -
1. Install Requirements
2. Install torchsample for data augmentation pip install git+https://github.com/ozanoktay/torchsample/
3. Download data and add to a folder like : MaxStyle/data/MICCAI2022_multi_site_prostate_dataset/reorganized

#### AMOS+BCV - 
### Install requirements
Create a new virtual environment and install all dependencies by:
```
pip install -r requirement.txt
```
### Data preparation
Download the origin dataset from their corresponding official website.

Enter the `dataset_conversion` fold and find the dataset you want to use and the corresponding dimension (2d or 3d)

Edit the `src_path` and `tgt_path` the in `xxxdataset.py`, where the `src_path` is the path to the origin dataset, and `tgt_path` is the target path to store the processed dataset.

Then, `python xxxdataset.py`

After processing is finished, put the processed dataset into `dataset/` folder or use a soft link.

#### AMOS+BCV+WORD -
**Dataset Pre-Process**  
1. Download the dataset according to the dataset link and arrange the dataset according to the `dataset/dataset_list/PAOT.txt`.  
2. Modify the ORGAN_DATASET_DIR value in label_transfer.py (line 51) and NUM_WORKER (line 53)  
3. `python -W ignore label_transfer.py`

