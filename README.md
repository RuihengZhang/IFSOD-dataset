# IFSOD-dataset
Dataset approched by A Benchmark and Frequency Compression Method for Infrared Few-Shot Object Detection

This dataset aims to provide an open evaluation scheme for small sample object detection tasks. It aims to enrich the training categories and sample pose changes. Contains over 4800 images, over 23000 instances, covering 8 scenes and 18 coarse-grained categories. We have established three random partitions for categories. Each partition contains base classes and new class images that comply with the few sample setting.


## 1. Dataset Overview

Provide detailed information about the dataset, including:
- **Number of samples**: 4800+ images
- **Data format**: images in JPG format and XML annotations

## 2. Dataset Samples

Below are some sample examples from the dataset to give users a better idea of its structure and content.

### Sample 
![Sample 1](images/visdata.png)
- Description: This sample shows [what the image/data represents]. The corresponding label is [label name or value].

<!-- ### Sample 2 -->
<!-- ![Sample 2](images/sample_image2.png) -->
<!-- - Description: This sample demonstrates [what the image/data represents]. The label is [label name or value]. -->

<!-- You can explore more samples by downloading the full dataset from [link to the dataset]. -->

## 3. Split

| Class        | Split I                        | Split II                       | Split III                     |
|--------------|--------------------------------|--------------------------------|-------------------------------|
| **Base Class** |                                |                                |                               |
|              | Armored Car (217)              | Kettle (122)                   | People (14860)                |
|              | Car (4167)                     | Pram (196)                     | Umbrella (217)                |
|              | Bike (716)                     | Goose (193)                    | Luggage (614)                 |
|              | Dog (166)                      | Bus (510)                      | Bike (716)                    |
|              | People (14860)                 | Dog (166)                      | Pram (196)                    |
|              | Switching (241)                | Car (4167)                     | Etricycle (262)               |
|              | Truck (153)                    | Duck (112)                     | Ebike (568)                   |
|              | Tricycle (139)                 | Switching (241)                | Car (4167)                    |
|              | Goose (193)                    | People (14860)                 | Duck (112)                    |
|              | Kettle (122)                   | Tricycle (139)                 | Kettle (122)                  |
|              | Etricycle (262)                | Ebike (568)                    | Truck (153)                   |
|              | Umbrella (217)                 | Etricycle (262)                | Armored Car (217)             |
|              | Guidepost (240)                | Umbrella (217)                 | Guidepost (240)               |
| **Novel Class** |                             |                                |                               |
|              | Duck (10)                      | Armored Car (10)               | Bus (10)                      |
|              | Ebike (10)                     | Truck (10)                     | Switching (10)                |
|              | Pram (10)                      | Bike (10)                      | Tricycle (10)                 |
|              | Bus (10)                       | Luggage (10)                   | Dog (10)                      |
|              | Luggage (10)                   | Guidepost (10)                 | Goose (10)                    |

## 4. Dataset Comparison Table

The table below provides a comparison of different datasets, including their images, instances, resolution, and other attributes.

| Dataset      | Images   | Instances | Resolution      | Instance Density | Classes | Scenes | Meaningless Classes | Unresolved Classes |
|--------------|----------|-----------|-----------------|------------------|---------|--------|---------------------|--------------------|
| **RGB-T234** | 233,928  | 116,660   | (628,459)       | 0.500            | 145     | 8      | 60                  | 43                 |
| **M3FD**     | 9,200    | 34,408    | (1001,744)      | 3.74             | 6       | 13     | 0                   | 0                  |
| **LLVIP**    | 15,485   | 41,579    | (1028,1024)     | 2.685            | 1       | 7      | 0                   | 0                  |
| **IFSOD-dataset (Ours)** | 4,815   | 23,333    | (662,489)       | 4.846            | 18      | 12     | 0                   | 0                  |

## 5. Performance Comparison Table

This table compares the performance of different methods across three novel splits. Results are given for various numbers of shots (1, 2, 3, 5, 10). The best results and the second-best results are highlighted in **bold**.

| Method              | Venue      | Backbone   | 1   | 2   | 3   | 5   | 10   | 1   | 2   | 3   | 5   | 10   | 1   | 2   | 3   | 5   | 10   |
|---------------------|------------|------------|-----|-----|-----|-----|-------|-----|-----|-----|-----|-------|-----|-----|-----|-----|-------|
|                     |            |            | Novel Split 1 |-----|-----|-----| Novel Split 2 |-----|-----|-----| Novel Split 3 |-----|-----|-----|
| FSRW               | ICCV2019   | YOLOv2     | 8.82  | 13.55  | 16.70  | 23.91  | 27.21  | 15.76  | 15.30  | 22.77  | 30.19  | 29.24  | 10.20  | 18.73  | 22.70  | 26.67  | 25.43  |
| Meta R-CNN         | ICCV2019   | FRCN-101   | 2.52  | 9.30   | 13.34  | 16.34  | 14.80  | 4.00   | 9.82   | 9.70   | 7.56   | 13.68  | 8.16   | 10.82  | 17.04  | 15.88  | 17.52  |
| TFA w/cos          | ICML2020   | FRCN-101   | 5.70  | 10.32  | 17.44  | 21.80   | 26.12  | 0.70   | 7.74   | 8.86   | 9.94   | 16.90  | 5.54   | 3.28   | 5.48   | 5.76   | 11.10   |
| MPSR               | ECCV2020   | FRCN-101   | 9.82  | **33.04** | 38.14  | 45.30  | 48.48  | 24.54  | 25.58  | 20.72  | 30.46  | 43.96  | 9.78   | 22.00  | 36.40  | 41.84  | 49.12  |
| FsDetView          | ECCV2020   | FRCN-101   | 1.82  | 13.86  | 15.86  | 15.16  | 14.72  | 4.00   | 7.98   | 10.20   | 7.99   | 9.94   | 3.82   | 7.96   | 14.52  | 15.76  | 15.10   |
| KFSOD              | CVPR2021   | FRCN-101   | 13.65 | 22.47  | 36.44  | 43.33  | **58.54** | 4.82   | 8.45   | 30.17  | 37.11  | 44.75  | 21.68  | 28.43  | 40.22  | 38.80  | 54.79  |
| FSCE               | CVPR2021   | FRCN-101   | **15.20** | 21.43  | 42.20  | 50.94  | 55.98   | 2.66   | 8.38   | 34.69  | 41.55  | 46.65  | 24.01  | 32.15  | 45.82  | **50.41** | **58.30** |
| CME                | CVPR2021   | FRCN-101   | 6.37  | 10.76  | 39.52  | 44.06  | 49.79  | 6.38   | 7.10   | 26.50  | 30.97  | 37.74  | 15.17  | 23.32  | 27.55  | 39.79  | 45.01  |
| FADI               | NeurIPS2021| FRCN-101   | 11.53 | 23.88  | 36.09  | 47.86  | 52.57  | 22.85  | 27.54  | 32.19  | 42.35  | 44.11  | 25.32  | **35.29** | 42.80  | 45.49  | 49.83  |
| DeFRCN             | ICCV2021   | FRCN-101   | 12.69 | 20.59  | 42.14  | 44.00  | 46.16  | 6.37   | 10.19  | 31.80  | 45.13  | 37.82  | 23.53  | 25.46  | 36.83  | 43.38  | 46.12  |
| FCT                | CVPR2022   | PVTv2      | 9.97  | 28.28  | **43.85** | **53.91** | 57.89   | **25.77** | **34.72** | **45.72** | **50.16** | **55.32** | **29.00** | 34.21  | **46.87** | 51.72  | 54.96  |


# Dataset Download

> **Important**: The dataset is available for download from the link below. Make sure to cite this dataset if you use it in your research.

[**Baidu yunpan**]( )
