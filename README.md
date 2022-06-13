# 7_class_Unet
> 目前整理好 test flow, train flow 並未整理
## Folder Structure
> 為了可以跟其他 code 共用 data 資料，data 放在上一層
NEEDED 代表需要從外部下載，其他則會由 code 產生
 
```
├─data
│  ├─1_o_image_PBLtest  # NEEDED: The image of orignal size
│  └─resize_data
└─Unet_7_class          # This repository
    ├─result   
    │  ├─raw_seg
    │  └─seg_resize
    └─weight            # NEEDED: The download link is in the 'Steps' of 'Testing flow'
    └─1_img_resize.ipynb
    └─2_test_model.ipynb
    └─3_label_resize.ipynb
    
```
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
    1. Find `TODO:` key word to modify path of your own before runing each script, e.g. 
        ![image](https://user-images.githubusercontent.com/32629259/173272267-00ffb2ef-d7d6-4679-8140-6ceb095700bf.png)
    2. Run `1_img_resize.ipynb` to resize x-ray
    3. Download `0801_7_classes_2_train_ten_classes_100.h5` from [here](https://drive.google.com/file/d/1L-YzU81Gxwb8Pk9bSFcUgBSrQVrA-p8h/view?usp=sharing) and put it under `./weight`
    4. Run `2_test_model.ipynb` to do the segmentation
    5. Run `3_label_resize.ipynb` to resize the result back
