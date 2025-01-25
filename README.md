# EECE 7150 - Autonomous Field Robotics

## Overview
This course is designed to survey some of the most important papers, techniques, and algorithms in the field of autonomous field robotics, with a particular emphasis on land-based, aerial, and marine applications. The course includes both theoretical paper presentations and hands-on implementation of the algorithms for geometric vision which have advanced applications in Field Robotics. Topics covered include SLAM, visual odometry, image processing, projective geometry, structure from motion and deep learning applications in robotics.

---

## Textbooks and References
- **Primary Reference**:  
  *Multiple View Geometry in Computer Vision* by Hartley and Zisserman (for projective geometry and camera models)
  
- **SLAM and Probabilistic Robotics**:  
  *Probabilistic Robotics* by Thrun, Burgard, and Fox (for SLAM foundations)  

---

## Major Topics covered and implemented

### **HW1: Stationary Distribution of a Markov Chain**
- **Objective**: Simulate a Markov Chain to estimate stationary distribution and validate using a closed-form solution.
- **Key Steps**:
  1. Implement a Markov Chain simulator.
  2. Determine stationary distribution using simulations.
  3. Compute stationary distribution analytically using eigen decomposition.
- **Highlights**:
  - Monte Carlo simulations with reproducible results.
  - Convergence analysis for probability distribution over transitions.

---

### **HW2: Image Replacement and Panoramic Stitching using Homography**
- **Objective**: Implement homography-based transformations for image replacement and create panoramic mosaics.
- **Parts**:
  1. **Image Replacement**:
      - Replace an image using homography with 4 and 8-point matches.
      - Comparison of results for robustness and accuracy.
  2. **Panoramic Stitching**:
      - Stitch multiple images using homography transformations.
      - Challenges with cylindrical warping and blending techniques.
- **Key Learnings**:
  - Understanding and applying homography matrices.
  - Using RANSAC for outlier rejection in point matching.
  - Identifying limitations of linear blending and planar homography.

---

### **HW3: Deep-Sea Image Registration and Mosaicking using GTSAM**
- **Objective**: Perform robust image registration and stitching for underwater images using GTSAM for factor graph optimization.
- **Steps**:
  1. Image preprocessing with CLAHE for contrast normalization.
  2. Keypoint detection and descriptor extraction using SIFT.
  3. Feature matching using FLANN-based matcher.
  4. RANSAC for homography estimation.
  5. Construct GTSAM factor graph:
     - Incorporate noise models for pose estimation.
     - Optimize with Levenberg-Marquardt to reduce uncertainties.
  6. Stitch final mosaics using optimized pose transformations.
- **Observations**:
  - Initial mosaics using homography showed visible seams and distortions.
  - GTSAM-based mosaics improved accuracy with optimized pose estimates but blending issues persisted.
- **Future Improvements**:
  - Apply exposure compensation for brightness consistency.
  - Use advanced blending techniques (e.g., multi-resolution splines).

---

## Papers Discussed
1. **ORB-SLAM 2**: Mur-Artal & Tardos, 2017.  
2. **Harris Corner Detector**: Harris & Stephens, 1988.  
3. **SIFT**: Lowe, 2004.  
4. **ORB**: Rublee et al., 2011.  
5. **Lego-LOAM**: Shan & Englot, 2018.  
6. **VINS-Mono**: Qin et al., 2018.  
7. **Kimera**: Rosinol et al., 2020.  
8. **iSAM2**: Kaess et al., 2012.  
9. **NERFs**: Advanced deep learning for 3D scene reconstruction.  

---

## Tools and Technologies
- **Python 3**: Core programming language.
- **OpenCV**: For image processing, feature detection, and pose estimation.
- **GTSAM**: For factor graph optimization and SLAM algorithms.
- **Matplotlib**: Visualization of graphs, images, and keypoints.
- **SIFT/FLANN**: Keypoint detection and robust feature matching.
- **RANSAC**: Outlier rejection for homography estimation.

---

