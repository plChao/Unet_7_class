# 7_class_Unet
> 目前整理好 test flow, train flow 並未整理
## Folder Structure
> 為了可以跟其他 code 共用 data 資料，data 放在上一層
## Install env
> 如果直接跑沒有環境問題，就可以跳過
1. using conda virtual environment
    1. Windows
        ```
        conda env create -f ./env.yml
        conda activate segment-gpu
        ```
    2. Linux: TODO
2. using Docker: TODO
## Testing flow
1. Overview
2. Steps
    1. Find `TODO:` key word to modify path of your own before runing each script
        1. Ex: 
    2. Run `1_img_resize.ipynb` to resize x-ray
    3. Download `0801_7_classes_2_train_ten_classes_100.h5` from [here](https://drive.google.com/file/d/1L-YzU81Gxwb8Pk9bSFcUgBSrQVrA-p8h/view?usp=sharing) and put it under `./weight`
    3. Run `2_test_model.ipynb` to do the segmentation
    4. Run `3_label_resize.ipynb` to resize the result back
