### Final Project – Panoramic Image Stitching

## Overview
This project implements a basic image stitching pipeline using SIFT feature matching and a custom RANSAC algorithm to compute homographies between overlapping image pairs.
The final goal is to produce a panoramic image by stitching together three partially overlapping views of the same scene.

While the current implementation is limited to stitching three images, the structure is modular and can be extended to support stitching N images with additional logic (e.g., image ordering, chaining transformations).

## Project Workflow
The main steps performed for stitching the images are:

1. Load Images
  Three input images (img1.jpg, img2.jpg, img3.jpg) are loaded from the images/ directory.

2. SIFT Feature Detection & Matching
  - SIFT keypoints and descriptors are computed using OpenCV.
  - Keypoints are matched between consecutive image pairs.
  - Matching pairs are visualized.

3. Custom RANSAC for Homography Estimation
  - A custom RANSAC algorithm (implemented from scratch) is used to:
    - Filter out outlier matches
    - Estimate the homography matrix for each pair
  - Displays only the inlier matches.
  - Reports the number of inliers found.

4. Image Warping
  Homography is applied using cv2.warpPerspective to align the images spatially.

5. Blending and Stitching
  - Warped images are blended using multiple methods:
    - Simple averaging
    - Linear blending
    - OpenCV’s built-in pyramid blending (optional)
  - The best blending method is selected based on visual quality.

## Notes
- Homography estimation via RANSAC and least squares is done manually, without using *cv2.findHomography*.
- Only *three images* are stitched in this project, but the approach can be extended to **handle N images** with additional automation (e.g., chaining homographies).
