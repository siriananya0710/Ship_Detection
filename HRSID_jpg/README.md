# Ship Detection using YOLOv8

## Problem statement
Detect ships in the given SAR Data. 
This repository contains my work for the intership qualification task at [Suhora](https://suhora.com/). 

## About Dataset
[Source](https://github.com/chaozhong2010/HRSID)
- The High-Resolution SAR Images Dataset (HRSID) contains 116 co-polarized and 20 cross-polarized SAR imageries.
- The original imageries for constructing HRSID are 99 Sentinel-1B imageries, 36 TerraSAR-X and 1 TanDEM-X images.
- Theabove136 panoramic SAR imageries cropped to 5604 high-resolution SAR images.
- These 5604 images have dimensions of 800 × 800 pixels, resolution of 96 dpi, and there are in .jpeg format.
- The colour depth of the images is 8 bits (one channel).
- The extracted 5604 high-resolution SAR images contain 16951 ship instances.
- The spatial resolutions of SAR images are 0.5, 1 and 3 meters per pixel.
- The annotations of each instance are the corresponding bounding box and the ship’s outline.
- The annotations of each SAR image constitute a .json file in MS COCO dataset format.

## Methodology
- Downloading the dataset and annotations.
- Splitting the dataset into train and test based on the split in annotations folder.
- Converting the annotations into YOLOv8 format.
- Downloading the model and training.
- Debugging - Package compatibility issue due between existing pytorch installations and the packages installed by ultralytics, OS error (unidentified files), kernel crashes.
- Environment configuration issue. Trying on different hardware.
- Employing a custom split and testing.
  
## Results
- Final Metrics found in: [runs/detect/train10](https://github.com/Lyra0710/Ship_Detection/tree/main/runs/detect/train10)
- Model predicts accurately on 4 images tested upon: Two images with ships and two pure background images.

Main notebook: [sar.ipynb](https://github.com/Lyra0710/Ship_Detection/blob/main/sar.ipynb)

