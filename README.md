# MSFMR 
Dataset construction documentation and source links for a face unmasking approach using CelebA, CelebA-HQ, FFHQ, and Masked Face datasets. Provides detailed descriptions of preprocessing steps, including face detection, cropping, and synthetic mask generation, for reproducible dataset construction. 

# Face Unmasking Dataset Construction Documentation 

## Overview 

This repository provides documentation and source references for a face unmasking approach using publicly available face datasets.

The goal is to enable reproducibility of the dataset creation process without redistributing any original images. 

--- 

## Original Datasets (Source Links) 

The following publicly available datasets were used in this study: 

- [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
- [CelebA-HQ](https://github.com/tkarras/progressive_growing_of_gans)
- [FFHQ](https://github.com/NVlabs/ffhq-dataset)
- [A Masked and Unmasked Face Dataset](https://data.mendeley.com/datasets/xyc9h3wjxf/1)

> ⚠️ Note: All datasets must be downloaded from their official sources. This repository does not contain or redistribute any raw images due to licensing restrictions.

--- 

## Dataset Construction Procedure 

The dataset was constructed using the following steps: 

### 1. Face Detection and Cropping Faces were detected and cropped using a face detection model trained using YOLOv8 to ensure consistent alignment and resolution. 

### 2. Synthetic Mask Generation Face masks were synthetically applied using the [MaskTheFace tool](https://github.com/aqeelanwar/MaskTheFace) to generate masked versions of the original images. 

### 3. Pair Construction Each original (unmasked) image was paired with its corresponding masked version to create training samples for the face mask removal task. 

--- 

## Processed Dataset

The processed paired masked-unmasked dataset generated for this study is publicly available on Kaggle:

- [Face Mask Remova Dataset on Kaggle](https://www.kaggle.com/datasets/yyazidd/face-mask-removal-dataset/data)

This dataset was constructed from publicly available sources using the preprocessing procedures described in this repository, including face detection, cropping, and synthetic mask generation.

> ⚠️ Note: The original datasets remain subject to their respective licenses and distribution policies. Researchers should also cite the original dataset sources listed in this repository when using this work.

---

## Reproducibility Note 

All dataset construction steps are described in this repository. Researchers can reproduce the dataset by downloading the original datasets from their official sources and applying the described preprocessing steps. 

--- 

## Data Availability Statement 

All datasets used in this work are publicly available from their official sources listed above. The dataset construction process is fully described in this repository. The processed paired dataset generated for this study is publicly available on Kaggle. Researchers are encouraged to cite the original dataset sources listed in this repository. The original datasets remain subject to their respective licenses and distribution policies. 

## References 

The following datasets were used in this study: 

- CelebA dataset:
  [1] Liu, Ziwei, et al. "Deep learning face attributes in the wild." Proceedings of the IEEE international conference on computer vision. 2015.

- CelebA-HQ:
  [2] Karras, Tero, et al. "Progressive growing of gans for improved quality, stability, and variation." arXiv preprint arXiv:1710.10196 (2017).

- FFHQ:
  [3] Karras, Tero, Samuli Laine, and Timo Aila. "A style-based generator architecture for generative adversarial networks." Proceedings of the IEEE/CVF conference on computer vision and pattern recognition. 2019.

- A Masked and Unmasked Face Dataset:
  [4] siradjuddin, Indah; Zakaria , Muhammad Ilham; Akhyar, Mohammad Habibul (2024), “A Masked and Unmasked Face Dataset”, Mendeley Data, V1, doi: 10.17632/xyc9h3wjxf.1

- MaskTheFace tool:
  [5] Anwar, Aqeel, and Arijit Raychowdhury. "Masked face recognition for secure authentication." arXiv preprint arXiv:2008.11104 (2020).
