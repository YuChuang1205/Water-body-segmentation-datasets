## Water body segmentation datasets (OS-Water-1500 and GLH-Water-1000)

### OS-Water-1500 dataset
**Introduction:** This dataset is a water segmentation dataset that we create based on the WHU-OPT-SAR dataset and contains optical images and  synthetic aperture radar (SAR) images. This dataset covers Hubei Province, China, with an area of approximately 51,448.56 km<sup>2</sup>. The optical imagery comes from the GF-1 satellite, and the SAR imagery comes from the GF-3 satellite. After registration and resampling, the two have a unified ground resolution of 5 meters. The original WHU-OPT-SAR dataset contains a total of 100 pairs of optical-SAR images, with a single image size of approximately 5556×3704 pixels. We first split the training and test sets into a 4:1 ratio. We then crop the original large-scale image using a 1024×1024 sliding window to obtain fixed-scale samples, resulting in 1200 training samples and 300 test samples. Given that the original image annotations cover multiple categories (farmland, city, village, water, forest, road, and other), and this study focuses on water body segmentation, we extract the "water" category from the multi-category annotations and generated the corresponding binary label.  
**Link:** [[Google Drive](https://drive.google.com/file/d/1PEVWH88UsSLskaw3NXBE8SIR9mBZMZrV/view?usp=sharing)]

<p align="center">
  <img src="OS-Water-1500.png" alt="OS-Water-1500 dataset" width="800"/><br>  
</p> 


### GLH-Water-1000 dataset
**Introduction:** This dataset is an optical remote sensing image water segmentation dataset that we create based on the GLH-water dataset. The samples cover multiple regions around the world, with diverse scene types (forests, farmlands, bare land, cities, etc.) and rich water forms (rivers, lakes, small ponds, irrigation water bodies, etc.). The original dataset contains a total of 250 ultra-large images with a ground resolution of 0.3 m and a single image size of 12,800×12,800 pixels. We first split the training and test sets into a 4:1 ratio. Considering that the actual area covered by a single pixel in the original image is too small, directly cropping with a 1024×1024 sliding window is likely to produce low-information slices that are "all water" or "all non-water". To this end, we downsample the original large image to 2048×2048 pixels and then cropped it with a 1024×1024 sliding window, ultimately obtaining 800 training samples and 200 test samples. Binary labels (water/non-water) are generated based on the original pixel-level masks.  
**Link:** [[Google Drive](https://drive.google.com/file/d/1xuDIU2hyrRU6R-WP2iXHoib_zx70am6O/view?usp=sharing)]

<p align="center">
  <img src="GLH-Water-1000.png" alt="GLH-Water-1000 dataset" width="800"/><br>  
</p> 

