## Assignment 2 - Edge Detection in Spatial and Frequency Domains

### Overview
This assignment explores edge detection techniques using OpenCV, focusing on both spatial domain filters and frequency domain transformations. 
The goal is to understand how different filters detect edges and how preprocessing (like Gaussian smoothing) affects results.

### Objectives
- Use 3–5 images with varying detail (e.g., natural scenes, buildings, text).
- Apply and analyze edge detection in:
  - **Spatial Domain** using:
    - *Gaussian Filtering* (3x3, 5x5, 7x7) for noise reduction
    - *Sobel Operator* for gradient-based edge detection
    - *Laplacian Operator* for second derivative edges
    - *Canny Edge Detection* with tunable thresholds
  - **Frequency Domain** using:
    - *Fourier Transform* with custom High-Pass Filters
- Reconstruction of edge-enhanced images via inverse transform
