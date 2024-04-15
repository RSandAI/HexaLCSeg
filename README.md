# HexaLCSeg
A Historical Benchmark Dataset from Hexagon Satellite Images for Land Cover Segmentation. 
This repository demonstrates a novel open land cover benchmark dataset generated from historical Hexagon (KH-9) reconnaissance satellite images to be used in deep learning-based image segmentation task. 
The dataset, related source code, and pre-trained models are available below.


Aim
---------------------

In this research, 

Methodology
---------------------
The framework of this study is detailed as follow. 



Land Cover (LC) classes used in this study
----------------------
![alt text](LULCclasses.jpg)

Dataset and Weights
---------------------
| Model | F-1 Score | IoU | Weights |
|:------------------:|-------------------------:|-------------------------:| -------------------------:|
| DeepLabv3+ Resnext-50_32x_4d | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d | 94.35  | 89.46 |[weights](https://drive.google.com)|

The dataset and the weights can be found [here](https://drive.google.com).


Sample Outputs
---------------------
![alt text](outputs_0.png)
![alt text](outputs_1.png)




System-specific notes
---------------------
The code was implemented in Python(3.8) and PyTroch(1.14.0) on Windows OS. The *segmentation models pytorch* library is used as a baseline for implementation. Apart from main data science libraries, RS-specific libraries such as GDAL, rasterio, and tifffile are also required.


Citation
---------------------
Please kindly cite our paper if this code and the dataset used in the study is useful for your research.

Sertel, E., Kabadayı, M.E, Sengul, G. S. & Tumer, I. N, (2024). HexaLCSeg: A Historical Benchmark Dataset from Hexagon Satellite Images for Land Cover Segmentation, IEEE Geoscience and Remote Sensing Magazine, Accepted.



