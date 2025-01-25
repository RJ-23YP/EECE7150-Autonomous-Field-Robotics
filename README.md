# EECE 7150 - Autonomous Field Robotics

## Overview
This course is designed to survey some of the most important papers, techniques, and algorithms in the field of autonomous field robotics, with a particular emphasis on land-based, aerial, and marine applications. The course includes both theoretical paper presentations and hands-on implementation of the algorithms on Northeastern robots. Topics covered include SLAM, visual odometry, image processing, projective geometry, and deep learning applications in robotics.

---

## Course Details

- **Instructor**: Hanumant Singh  
- **Class Schedule**: Mondays & Wednesdays, 5:50 PM - 7:30 PM  
- **Office Hours**: TBD  

---

## Grading Breakdown
- **Paper Presentation**: 20%  
- **Projects**: 80%

### Additional Recommendation:
Students are strongly encouraged to attend robotics-related talks, symposiums, and events at Northeastern University.

---

## Textbooks and References
- **Primary Reference**:  
  *Multiple View Geometry in Computer Vision* by Hartley and Zisserman (for projective geometry and camera models)
  
- **SLAM and Probabilistic Robotics**:  
  *Probabilistic Robotics* by Thrun, Burgard, and Fox (for SLAM foundations)  

---

## Course Topics and Schedule

| Lecture # | Topics                                                                                  | Projects/Assignments                   |
|-----------|-----------------------------------------------------------------------------------------|----------------------------------------|
| **1**     | ROS background, Driving NU autonomous robots (car, Husky), Monte Carlo techniques       |                                        |
| **2**     | Projective Geometry in 2D (CH 2 MVG), Homography Mapping (Part 1)                      | Project 1a: Homography Mapping         |
| **3**     | Projective Geometry in 3D (CH 3 MVG), Estimation of Projective Transforms              |                                        |
| **4**     | Project 1a Due, Camera Models (CH 6.1 MVG)                                              | Project 1b Assigned                   |
| **5**     | Filtering Techniques: Alpha-beta filters, 1D Kalman filter                              |                                        |
| **6**     | Bayesian Filtering, Multivariate Kalman filtering, SLAM, Visual-Inertial Odometry (VIO) |                                        |
| **7**     | SLAM in 2D, Graph-based representations                                                 |                                        |
| **8**     | Project 1b Due, Underwater Mosaicking (Pizarro Paper), GTSAM for optimization           | Project 2: Underwater Image Dataset   |
| **9**     | Sensor Calibration (Multibeam, Camera-IMU, Kalibr Tool)                                |                                        |
| **10**    | iSAM Paper Review, GTSAM deep dive                                                     |                                        |
| **11**    | Epipolar Geometry, Fundamental and Essential Matrices                                  | Project 2 Presentations, Project 3a Assigned |
| **12**    | Continuation of Epipolar Geometry                                                      |                                        |
| **13**    | Bag of Words                                                                            |                                        |
| **14**    | ORB-SLAM                                                                               | Project 3b Assigned                   |
| **15**    | ICP (Iterative Closest Point Algorithm)                                                |                                        |
| **16**    | Lego Loam (LiDAR-based SLAM)                                                           | Project 3b Due                        |
| **17**    | VINS Mono, Kimera                                                                      |                                        |
| **18**    | RTAB-SLAM                                                                              |                                        |
| **19**    | Role of Machine Learning in Robotics                                                   |                                        |
| **20-25** | Paper Presentations                                                                    |                                        |
| **26**    | Final Project Presentations                                                            |                                        |

---

## Major Assignments & Homeworks

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
1. **Harris Corner Detector**: Harris & Stephens, 1988.
2. **SIFT**: Lowe, 2004.
3. **ORB**: Rublee et al., 2011.
4. **ORB-SLAM**: Mur-Artal & Tardos, 2017.
5. **Lego-LOAM**: Shan & Englot, 2018.
6. **VINS-Mono**: Qin et al., 2018.
7. **Kimera**: Rosinol et al., 2020.
8. **iSAM2**: Kaess et al., 2012.
9. **NERFs**: Advanced deep learning for 3D scene reconstruction.

---

## Key Technologies
- **Python**: Core programming language.
- **OpenCV**: For image processing, feature detection, and pose estimation.
- **GTSAM**: For factor graph optimization and SLAM algorithms.
- **Matplotlib**: Visualization of graphs, images, and keypoints.
- **SIFT/FLANN**: Keypoint detection and robust feature matching.
- **RANSAC**: Outlier rejection for homography estimation.

---

## Contribution Guidelines
Students are encouraged to:
1. Collaborate with peers for discussions on projects and concepts.
2. Explore additional resources (papers, libraries) to enhance understanding.
3. Share findings and insights during paper presentations.

---

## Final Remarks
This course emphasizes a practical, hands-on approach to mastering key concepts in autonomous robotics, complemented by rigorous theoretical exploration of seminal papers. Students will gain experience in real-world implementations, equipping them with the skills necessary for advanced robotics research and development.
