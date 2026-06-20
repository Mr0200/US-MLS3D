# US-MLS3D
# US-MLS3D

US-MLS3D is a mobile laser scanning point cloud benchmark dataset for urban street scene semantic segmentation. The dataset was collected along a typical urban arterial road in  China. It provides point-wise semantic annotations for real-world urban street scenes and is designed to support research on point cloud semantic segmentation, urban scene understanding, road boundary perception, and road asset extraction.

## Dataset Overview

US-MLS3D focuses on continuous urban street scenes in a northern Chinese city. The dataset covers approximately 2.7 km  and contains 81,659,039 points in total. Each point includes three-dimensional coordinates and laser intensity information.

The dataset is divided into 10 sub-regions according to spatial continuity:

```text
Block01
Block02
Block03
Block04
Block05
Block06
Block07
Block08
Block09
Block10
```
Each sub-region contains point cloud files organized by semantic class.

## Semantic Classes
US-MLS3D contains 7 semantic classes. The label mapping is shown below:
```text
| Class Name       | Label ID | Description                                                                                        |
| ---------------- | -------: | -------------------------------------------------------------------------------------------------- |
| ground           |        0 | Road surface, sidewalk, parking area and other ground structures                                   |
| curb             |        1 | Road curb and boundary structures between roadway and sidewalk                                     |
| car              |        2 | Parked or moving vehicles                                                                          |
| build            |        3 | Buildings and large roadside structures, such as bus stations and subway entrances                 |
| street_furniture |        4 | Street facilities, including poles, traffic signs, signal lights and related supporting structures |
| vegetation       |        5 | Trees, shrubs and green belts along the road                                                       |
| fence            |        6 | Guardrails and fence-like structures along roads or sidewalks                                      |
```
## Dataset Structure
The dataset is organized by sub-region. Each sub-region folder contains seven class-specific text files:
```text
US-MLS3D/
├── Block01/
│   ├── build.txt
│   ├── car.txt
│   ├── curb.txt
│   ├── fence.txt
│   ├── ground.txt
│   ├── street_furniture.txt
│   └── vegetation.txt
├── Block02/
│   ├── build.txt
│   ├── car.txt
│   ├── curb.txt
│   ├── fence.txt
│   ├── ground.txt
│   ├── street_furniture.txt
│   └── vegetation.txt
├── ...
└── Block10/
    ├── build.txt
    ├── car.txt
    ├── curb.txt
    ├── fence.txt
    ├── ground.txt
    ├── street_furniture.txt
    └── vegetation.txt
  ```
    Each .txt file stores point cloud data of a specific semantic class. Each row represents one point and follows the format:x y z intensity
    where x, y, and z are the three-dimensional coordinates of the point, and intensity is the laser return intensity.
## Data Split 

In the benchmark experiments, the dataset is divided into training, validation and test sets as follows:
```text
| Split          | Sub-regions                              |
| -------------- | ---------------------------------------- |
| Training set   | 1, 2, 3, 7, 9, 10 |
| Validation set | 4, 6                             |
| Test set       | 5, 8                             |
```
Researchers may use the same split for fair comparison with the benchmark results reported in the paper.

## Dataset Statistics

The dataset contains 81,659,039 points in total. The proportions of different semantic classes are as follows:
```text
| Class            | Proportion |
| ---------------- | ---------: |
| ground           |     44.69% |
| curb             |      1.05% |
| car              |      1.70% |
| build            |      1.47% |
| street_furniture |      0.54% |
| vegetation       |     49.63% |
| fence            |      0.92% |
```
The dataset presents a typical long-tailed class distribution in real urban street scenes. Large-scale classes such as ground and vegetation account for a high proportion, while small-scale and elongated objects such as curbs, street facilities and fences have relatively fewer points.
## Download

The US-MLS3D dataset will be publicly available for non-commercial academic research.

Download link:https://pan.baidu.com/s/1gEFLObC_NM6rkLOfPES9_A

Extraction code: please contact the authors 2024282140133@whu.edu.cn

If the download link is unavailable, please contact the authors.

## Usage Notes

The dataset is released for academic research and educational purposes only.

Users should not redistribute, sell, sublicense or use the dataset for commercial purposes without permission.

Users should cite the corresponding paper when using this dataset in publications, reports, presentations or other academic outputs.

The authors provide the dataset as is and make no warranties regarding its completeness, accuracy or fitness for a particular purpose.

## Contact

For questions about the dataset, please contact the authors.

Wenbo Wang: 2024282140133@whu.edu.cn

