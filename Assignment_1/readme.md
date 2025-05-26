## Assignment 1 - Thresholding and Histogram Analysis

### Overview
This assignment focuses on basic image processing techniques including grayscale conversion, histogram analysis, and binary thresholding. 
The goal is to explore how grayscale histograms can be used to determine suitable threshold values for converting RGB images into binary black-and-white images.

### Objectives
- Load and process five RGB images from the images/ folder.
- Convert each image to grayscale using the transformation:
  
$$
s = T(z) = 0.3 \cdot Z_r + 0.6 \cdot Z_g + 0.1 \cdot Z_b
$$
- Compute and display the histogram of grayscale pixel intensities using a custom function.
- Determine a threshold value based on the histogram and convert the grayscale image to a binary image.
- Explore the effect of two alternative threshold values (one higher and one lower than the original) to compare different binary outputs.
- Perform a pixel count analysis (black vs white) for all binary images and discuss the effects of threshold variations.
