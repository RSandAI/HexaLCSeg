# HexaLCSeg Benchmark Dataset

This study aims to emphasize the importance of historical land cover maps and introduce a new benchmark dataset derived from very high-resolution historical Hexagon (KH-9) reconnaissance satellite images for use in deep learning-based image segmentation tasks. Our HexaLCSeg dataset comprises high-resolution monochromatic Hexagon images from the 1970s and 1980s covering Turkish and Bulgarian territories, encompassing a large geographic area

The HexaLCSeg dataset comprises eight panchromatic images accompanied by corresponding 3-channel RGB Ground Truth Masks, all with 8-bit radiometric resolution and a spatial resolution of 1 meter. The dataset is organized into a total of 10,000 patches, each sized at 256x256 pixels. 
We split our dataset into 70% training (7000 patches), 15% validation (1500 patches), and 15% testing (1500 patches). 

The dataset, related source code, and pre-trained models are available below.

Land Cover (LC) Classes Used In This Study
----------------------

Our dataset is inspired by the European Space Agency (ESA) WorldCover project and includes eight LC classes and related RGB codes were set for each class but we adjusted 0-pixel value as no data and replace the 0 values with 1 in ESA RGB code palette.
Additionally, a new sub-class for the trees, named Permanent Cropland is defined and its RGB code was set to 1-207-117. This class is important to differentiate permanent fruit trees from other trees, specifically crucial for past agricultural mapping purposes.

![alt text](LULCclasses.jpg)

Methodology
---------------------
In our study, we employed the geographic object-based image analysis (GEOBIA) approach to generate accurate land cover (LC) maps, which serve as the ground truth masks for our dataset. 

For deep learning-based image segmentation, we employed a total of 9 CNN models, implementing U-Net++ and DeepLabv3+ segmentation architectures with different hyperparameters, paired with SE-ResNeXt50 backbone that pre-trained with weight values from the 2012 ILSVRC ImageNet dataset.


Models, Metric Results and Weights
---------------------
| Architecture | Loss Function | Augmentation | F-1 Score | IoU | Weights |
|:------------------:|-------------------------:|-------------------------:| -------------------------:| -------------------------:| -------------------------:|
| DeepLabv3+ Resnext-50_32x_4d |x | y | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d |x | y | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d |x | y | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d |x | y | 94.35  | 89.46 |[weights](https://drive.google.com)|
| DeepLabv3+ Resnext-50_32x_4d |x | y | 94.35  | 89.46 |[weights](https://drive.google.com)|

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



