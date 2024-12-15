# Image Stitching Project

This project demonstrates an **Image Stitching** algorithm to create seamless panoramic images by combining multiple overlapping images. The process involves feature detection, geometric transformations, and blending techniques to produce a unified wide-angle image.
---

## Overview

Image stitching is a critical technique in photography, mapping, computer vision, and many other fields. This implementation focuses on:
- Detecting and matching key points in overlapping images.
- Computing geometric transformations (e.g., translation, rotation, scaling, and homography).
- Aligning, warping, and blending images into a seamless panorama.

---

## Key Steps

1. **Feature Detection and Matching**:
   - Detect salient features using **Difference of Gaussian (DoG)** and **SIFT (Scale-Invariant Feature Transform)**.
   - Match keypoints using **Brute Force Matching** and filter matches with **Lowe's Ratio Test**.

2. **Geometric Transformation**:
   - Estimate homography matrices using **RANSAC (Random Sample Consensus)** to handle perspective transformations.

3. **Warping and Blending**:
   - Align images using geometric transformations.
   - Blend images using techniques like gradient-based blending to eliminate visible seams.

---

## Dependencies

1. To run this project, the following dependencies are required:
    - **Python 3.8 or higher**
    - Libraries:
      - `numpy`
      - `opencv-python`
      - `matplotlib`

2. Install the dependencies with:
   ```bash
   pip install -r requirements.txt

## Outputs
### Examples of Stitched Images
- Image Pair 1: Successful stitching with well-aligned features.
- Image Pair 2 & 3: Issues with lighting and exposure requiring correction.
- Image Pair 4: Seamless stitching due to consistent tones and brightness.

### Improved Algorithm
- Handled exposure and color variations for Image Pair 2 using OpenCV’s features invariant technique.
- Produced balanced and distortion-free panoramas.

## Challenges and Improvements
### Challenges:
- **Color and Exposure Variations**: Variations lead to visible seams. Improvements include preprocessing with color correction.
Parallax and Perspective Shifts:
    - Misalignments due to varying camera viewpoints.
    - Homography adjustments partially address this issue.
- **Computational Cost**: Feature detection and RANSAC are computationally intensive. Optimized implementations are recommended.

## Improvements:
- Implemented Invariant Features Technique for distortion correction and automatic image ordering.
- Enhanced blending for smoother transitions.
