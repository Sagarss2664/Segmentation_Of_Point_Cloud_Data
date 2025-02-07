# Segmentation and Classification of 3D Point Cloud Data Using RANSAC and Geometric Features

### Authors:
- **Vishwanath Hubbali** (01fe22bcs236@kletech.ac.in)  
- **Sagar Shegunashi** (01fe22bcs259@kletech.ac.in)  
- **Pavan Karaveeramath** (01fe22bcs017@kletech.ac.in)  
- **K Koushik Kumar Reddy** (01fe22bcs239@kletech.ac.in)  
- **Dr. P.G. Sunitha Hiremath** (pgshiremath@kletech.ac.in)  
- **Mr. Sujay R** (r.sujay2512@gmail.com)  

---

## Abstract
Understanding and interpreting urban environments is becoming increasingly important in fields like autonomous driving, urban planning, and environmental monitoring. This project focuses on creating an efficient and intuitive system to segment and classify 3D point cloud data from the KITTI dataset into key categories: roads, trees, buildings, and vehicles. Using a combination of the RANSAC algorithm for plane segmentation, DBSCAN for clustering, and geometric feature analysis, the system ensures precise classification of urban features. The system achieves an overall efficiency of 55%, providing a scalable and effective solution for real-world applications.

## Introduction
Segmentation helps divide dense 3D point cloud data into smaller, understandable chunks, while classification assigns meaningful labels such as "tree," "building," or "road." This research focuses on analyzing real-world 3D point cloud data from the KITTI-360 dataset and implementing algorithms to accurately classify various objects.

## Literature Review
Several approaches have been explored for 3D point cloud segmentation, including:
- RANSAC and clustering techniques for geometric segmentation.
- Deep learning methods like PointNet and PointNet++ for feature learning.
- Transformer-based models like the Superpoint Transformer for efficient segmentation.

## Methodology
The proposed methodology follows these steps:
1. **Data Acquisition**: The KITTI-360 dataset is used, and point cloud data is loaded in `.ply` format.
2. **Plane Detection Using RANSAC**: Identifies flat surfaces like roads.
3. **Clustering Using DBSCAN**: Groups remaining points into clusters based on density.
4. **Classification**: Objects are classified based on their geometric features:
   - Trees (green)
   - Buildings (blue)
   - Roads (grey)
   - Vehicles (red)
   - Unidentified objects (white)

### Model Architecture
Below is the model architecture for the segmentation process:

![Model Architecture](images/extracted_image_2_1.png)

## Results and Analysis
Evaluation of the proposed algorithm was performed on multiple datasets, measuring class-wise accuracy and overall efficiency. The classification accuracy per object category is as follows:

| Class       | Accuracy (%) |
|------------|-------------|
| Trees      | 59.14       |
| Vehicles   | 11.18       |
| Buildings  | 58.56       |
| Road/Plane| 97.49       |
| Unidentified | 12.31    |

The overall efficiency of the system is **55.38%**.

## Sample Results
Comparison of segmentation results with ground truth:

**Ground Truth vs Algorithm Output:**




## Conclusion
The developed system successfully segments and classifies 3D point cloud data into distinct object categories using a combination of RANSAC, DBSCAN, and geometric analysis. The approach demonstrates high efficiency in recognizing large structures like roads and buildings while facing challenges with smaller objects like trees and vehicles.

## Future Work
Potential improvements include:
- Adapting classification thresholds dynamically based on dataset properties.
- Training the system on more diverse datasets to enhance accuracy.
- Implementing real-time adaptability for autonomous applications.

## References
1. Fischler, M. and Bolles, R., "Random Sample Consensus: A Paradigm for Model Fitting," ACM Communications, 1981.
2. R. Q. Charles et al., "PointNet: Deep Learning on Point Sets," IEEE CVPR, 2017.
3. D. Robert et al., "Efficient 3D Semantic Segmentation with Superpoint Transformer," ArXiv, 2023.

