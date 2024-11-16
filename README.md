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
