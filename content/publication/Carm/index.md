---
title: "Synthetic data-driven tracking and robotic deployment of miniature medical devices via X-ray imaging"
authors:
- admin
author_notes:
- "First author"
date: "2025-06-02"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2025-06-02"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "preprint"
publication_short: ""

abstract: The clinical translation of miniature medical devices (MMDs) for minimally invasive surgery promises transformative advances in biomedical engineering. However, their effective deployment in complex anatomies under real-time X-ray guidance presents challenges like low imaging quality and precise control. Manual identification and operation are labor-intensive and error-prone, while deep learning-based automation is limited by the scarcity of annotated X-ray datasets of MMDs due to costly data collection, laborious annotation, and privacy constraints. Here, we introduce MicroSyn-X, a framework of training computer vision models for robotic teleoperation using synthesized high-fidelity, pixel-accurate labelled, and domain-randomized X-ray images, eliminating manual data curation. The integration of MicroSyn-X into a teleoperated robotic system enables real-time localization and navigation of magnetic soft and liquid MMDs within diverse ex vivo and dynamic in vivo environments, demonstrating robustness under challenging imaging conditions of low contrast, high noise, and occlusion. We also open source the first X-ray MMD dataset to enable benchmarking. Addressing data scarcity and enabling real-time robotic navigation, this work advances robot-assisted minimally invasive surgery toward next-generation precision interventions.

# Summary. An optional shortened abstract.
summary: MicroSyn-X is a framework using synthetic, labeled, and domain-randomized X-ray images to train computer vision models for real-time robotic teleoperation of miniature medical devices (MMDs).

tags:
- X-ray imaging
- Magnetic control
- Generative models
- Robotic arm
- In vivo animal experiments
featured: true

# links:
# - name: ""
#   url: ""
url_pdf: ""
url_code: ""
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: 'https://wchunxiang.github.io/'
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Framework of Micro-SynX'
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
#   Otherwise, set `slides: ""`.
slides: ""
---
The paper presents **MicroSyn-X**, a framework addressing real-time tracking and robotic deployment of miniature medical devices (MMDs) under X-ray guidance. Key techniques include:

* **Synthetic Data Generation**: Uses diffusion models (e.g., pix2pix stable diffusion) to create high-fidelity X-ray images with pixel-accurate labels, integrating user-defined masks and domain randomization (e.g., varying tissue types, noise levels, robot shapes) to mimic clinical scenarios without manual annotation.
* **CV Model Training**: Employs YOLO11-seg for real-time detection/segmentation, using patch-based strategies and data augmentation (geometric/color transformations) to enhance small-object detection in low-contrast, noisy environments.
![1](1.JPG)
* **Robotic System Integration**: Combines a 7-DOF robotic arm with magnetic actuation and C-arm fluoroscopy, using adaptive Kalman filtering for tracking and path planning based on preoperative CT/angiography data.
* **Validation**: Demonstrates robustness in *ex vivo* (porcine tissues) and *in vivo* (rabbit/rat models) environments, with an open-sourced X-ray MMD dataset for benchmarking.

MicroSyn-X bridges data scarcity and enables precision interventions via synthetic data-driven automation, outperforming real-data-trained models in challenging imaging conditions.


> This work is under submission.