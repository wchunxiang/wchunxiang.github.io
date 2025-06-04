---
title: "DanioSense: Automated High-Throughput Quantification of Zebrafish Larvae Group Movement"
authors:
- admin
author_notes:
- "First author"
date: "2022-04-01"
doi: "doi: 10.1109/TASE.2021.3050408"

# Schedule page publish date (NOT publication's date).
publishDate: "2022-04-01"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Automation Science and Engineering"
publication_short: ""

abstract: The capability to obtain detailed motility information of model organisms is fundamental to reveal their functional and social behavior characteristics. Zebrafish is a powerful vertebrate model organism. Despite recent success in the automatic quantification of adult zebrafish movement, it remains a laborious task for group zebrafish larval tracking due to their similar appearance, frequent occlusions, and highly discontinuous kinematics. This article presents DanioSense (DS), an automatic tracker for group larval zebrafish, to overcome these tracking challenges. The integration of a light convolutional neural network and a centerline extraction algorithm enables the tracker to localize individuals even in occlusion cases where objects’ identities are prone to switch. With reliable detections, an adaptive Kalman filter is designed to optimally estimate locomotive parameters, which is also used for object reidentification accomplished by a two-stage data association protocol. Experimental results demonstrated a tracking accuracy of over 97%, median errors of 102 μm , and 8.8° for the position and orientation measurement, and a processing speed of over 30 frames/s with a normal computer configuration. DS provides detailed quantitative data for a large-scale larvae group in nearly real time, highly boosting the efficiency of characterizing individual phenotypes and analyzing social interactions.

# Summary. An optional shortened abstract.
summary: 'Daniosense'

tags:
- Multi-object trakcing
- Image processing 
- Adaptive Kalman filter
featured: true

# links:
# - name: ""
#   url: ""
url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://ieeexplore.ieee.org/abstract/document/9336279'
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Workflow of DanioSense'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`. {{</* video src="my_video.mp4" controls="yes" */>}}
slides: ""

---

## 1. **Challenges Addressed**
* **Occlusion Handling**: Addresses frequent intersections and identity switches among zebrafish larvae due to similar appearance and transparent bodies.
* **Discontinuous Kinematics**: Overcomes the challenge of erratic movements (static periods followed by sudden bursts), which make traditional motion models ineffective.
* **High-Throughput Requirements**: Meets the need for real-time tracking of large larval groups, crucial for biomedical research such as genetics and drug screening.


## 2. **Core Techniques**

### 2.1 **Image Preprocessing**
* **Foreground Extraction**:
    * **Intensity Thresholding**: Utilizes Gaussian filtering and user-defined intensity ranges for simple backgrounds.
    * **Background Subtraction (BS)**: Employs adaptive Gaussian mixture models, updated periodically, for complex or inhomogeneous backgrounds.
* **Blob Filtering**: Removes noise (e.g., bubbles, particles) through morphological operations (opening, erosion, dilation) and contour analysis (e.g., area, perimeter-to-area ratio).

### 2.2 **Detection Stage**
* **Centerline Extraction**: A fast parallel thinning algorithm (Zhang and Suen) is used to derive morphological skeletons, which enables head localization, orientation, and bend angle calculation. This is critical for resolving occlusions by identifying individual "spines" in overlapping blobs.
* **Head Detection with Light CNN**: A pre-trained Convolutional Neural Network (CNN) classifies anchor windows (centered on centerline endpoints/intersections) as head or non-head. Mean-shift clustering then filters outliers and determines final head positions, even in severe occlusion scenarios. The CNN architecture includes two convolutional layers (ReLu activation), subsampling, and a softmax output layer.

### 2.3 **Tracking Stage**
* **Adaptive Kalman Filter**: This filter fuses **constant velocity (CV)** and **constant acceleration (CA)** models to effectively handle discontinuous motion. It dynamically adjusts the process noise covariance ($Q_k$) based on residual errors ($\epsilon_k$) to detect maneuvers (bursts) and weights model outputs using likelihoods ($\mathcal{L}_k$) to optimize state estimates (position, velocity, orientation).
* **Two-Stage Data Association**:
    * **Stage 1**: Uses Intersection over Union (IOU) to associate blobs between frames, reducing computation for single objects.
    * **Stage 2**: Applies the Hungarian algorithm with a weighted Mahalanobis distance (incorporating CV/CA model predictions) for associating remaining objects.

### 2.4 **Visualization and Output**
* **Real-Time Tracking Display**: Provides a real-time visualization of head positions, orientations, occlusion events, and trajectory histories.
* **Behavioral Analysis Tools**: Includes ethograms to categorize behavior (static, cruise, burst) using velocity and residual errors, and 3D trajectory plots and scatter maps to visualize spatial-temporal patterns and social interactions.

## 3. **Key Innovations**
* **Occlusion Resolution**: Combines CNN and centerline extraction to accurately identify heads during intersections, effectively preventing identity switches.
* **Adaptive Filtering**: Offers robustness to discontinuous motion, outperforming traditional Kalman filters in noisy, burst-prone scenarios.
* **High-Throughput Efficiency**: Achieves real-time processing speeds of over 30 frames per second on standard hardware, with parallelized object tracking and multithreading, allowing scalability.

## 4. **Performance Metrics**
* **Accuracy**: Demonstrates a high Identification Rate (IR) of >97% for position/orientation and 91.1% for bend angle. Median errors are low, at 102 µm for position and 8.8° for orientation.
* **Efficiency**: Processes at speeds greater than 30 FPS for groups of up to 40 larvae, with potential for further scalability via hardware upgrades.
* **Robustness**: Exhibits low ID switches (IDS) and fragments (Frag) compared to baseline methods (Background Subtraction, Simple Data Association).

## 5. **Applications and Extensibility**
* **Biomedical Research**: The system enables large-scale chemical and genetic screens, neuropharmacology studies, and social behavior analysis in zebrafish larvae.
* **Cross-Species Adaptability**: The methodology can be retrained and fine-tuned for other fish-like animals by adjusting the CNN and centerline extraction processes.

## 6. **Comparison with Existing Methods**
* **vs. idTracker.ai**: DanioSense offers real-time tracking with lower computational cost, whereas idTracker.ai typically requires offline training and has higher hardware demands.
* **vs. ZebraZoom/BS**: DanioSense demonstrates superior occlusion handling and scalability, especially for large groups of more than 10 larvae.

## 7. **Future Work**
* Improve processing speed to accommodate high-speed cameras (>500 FPS).
* Enhance the CNN architecture for more complex environmental conditions.
* Expand visualization modules and facilitate multi-species applications.

This article presents a robust, automated system that addresses long-standing challenges in larval zebrafish tracking, enabling high-throughput behavioral analysis with broad implications for biomedical and ecological research.

> For more details, refer to "C. Wang, et.al., "DanioSense: Automated High-Throughput Quantification of Zebrafish Larvae Group Movement," in IEEE Transactions on Automation Science and Engineering, vol. 19, no. 2, pp. 1058-1069, April 2022, doi: 10.1109/TASE.2021.3050408."

## Video

Teach your course by sharing videos with your students. Choose from one of the following approaches:

{{< youtube D2vj0WcvH5c >}}

**Youtube**:

    {{</* youtube w7Ft2ymGmfc */>}}

**Bilibili**:

    {{</* bilibili id="BV1WV4y1r7DF" */>}}