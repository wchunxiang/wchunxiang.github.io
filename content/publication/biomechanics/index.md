---
title: "In situ sensing physiological properties of biological tissues using wireless miniature soft robots"
authors:
- admin
author_notes:
- "First author"
date: "2023-06-07"
doi: "DOI: 10.1126/sciadv.adg3988"

# Schedule page publish date (NOT publication's date).
publishDate: "2023-06-07"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Science Advances"
publication_short: ""

abstract: Implanted electronic sensors, compared with conventional medical imaging, allow monitoring of advanced physiological properties of soft biological tissues continuously, such as adhesion, pH, viscoelasticity, and biomarkers for disease diagnosis. However, they are typically invasive, requiring being deployed by surgery, and frequently cause inflammation. Here we propose a minimally invasive method of using wireless miniature soft robots to in situ sense the physiological properties of tissues. By controlling robot-tissue interaction using external magnetic fields, visualized by medical imaging, we can recover tissue properties precisely from the robot shape and magnetic fields. We demonstrate that the robot can traverse tissues with multimodal locomotion and sense the adhesion, pH, and viscoelasticity on porcine and mice gastrointestinal tissues ex vivo, tracked by x-ray or ultrasound imaging. With the unprecedented capability of sensing tissue physiological properties with minimal invasion and high resolution deep inside our body, this technology can potentially enable critical applications in both basic research and clinical practice.

# Summary. An optional shortened abstract.
summary: Wireless miniature soft robots offer a minimally invasive way to continuously monitor physiological properties of soft tissues, like pH and viscoelasticity, by precisely recovering tissue properties from their shape and external magnetic fields.

tags:
- Mechanics 
- Image processing 
- Magnetic control
- Medical imaging
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
url_source: 'https://www.science.org/doi/full/10.1126/sciadv.adg3988'
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Concept of in situ sensing the physiological properties of soft tissues by a wireless miniature soft robot.'
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

---
### Interdisciplinary Expertise

* **Soft Robotics:** Design of magnetically actuated, bioadhesive-enabled microdevices.
* **Biomechanics:** Analysis of tissue-robot interactions using beam theory and viscoelastic models.
* **Image processing:** Robot shape extraction and analysis.
* **Medical Imaging:** Integration of X-ray/ultrasound with real-time robotic sensing.
* **Materials Science:** Development of pH-responsive hydrogels and biocompatible adhesives.
-------

### 1. Wireless Miniature Soft Robot Design and Actuation

* **Magnetoelastic Soft Body:** The robot is made from **Ecoflex silicone rubber** mixed with **NdFeB microparticles** for magnetic responsiveness. It features **ring-shaped footpads with microspikes** and **chitosan-based bioadhesive patches** for controlled tissue attachment.
* **Multimodal Locomotion:** A customized **Halbach array** generates external magnetic fields, enabling versatile movements like walking, climbing, crawling, and swimming for navigation in complex tissues.
* **Magnetic Control:** **Static magnetic fields** induce buckling for adhesion and pH sensing, while **rotating magnetic fields** (0.1–15 Hz) enable dynamic deformation for viscoelasticity sensing.

![1](1.jpg)

---
### 2. Sensing Mechanisms for Tissue Properties

#### Static Interaction (Adhesion and pH Sensing)

* **Buckling-Based Adhesion Sensing:** The robot's buckling motion under magnetic fields is modeled using **Euler-Bernoulli beam theory**. Analyzing the threshold magnetic field for detachment quantifies tissue adhesion.
* **pH-Responsive Adhesive Patch:** A three-layer patch (elastomer, hydrogel, pH-sensitive bioadhesive) uses **catechol-boronate complexation** for pH-dependent adhesion. Adhesion strength correlates linearly with pH (sensing range: pH 1–8, sensitivity: 1 pH unit).

![2](2.JPG)

#### Dynamic Interaction (Viscoelasticity Sensing)

* **Frequency Sweeping Method:** Rotating magnetic fields induce periodic robot deformations. Analyzing the frequency response of tissue strain ($\epsilon_{yy}$) relative to magnetic field amplitude allows estimation of **storage modulus ($E'$) and loss modulus ($E''$)** using a magnetoelastic model.
* **Mechanical Calibration:** Synthetic materials like agarose and gelatin gels are used to calibrate the relationship between $\epsilon_{yy}/B_y$ and $E'$, with relative errors less than 8% for $E'$ and less than 12% for $E''$.

![3](3.JPG)

---
### 3. Medical Imaging and Data Analysis

* **X-Ray and Ultrasound Imaging:** Real-time imaging (30 FPS for X-ray) tracks robot shape changes. X-ray provides high contrast, with a radiation dose less than 410 $\mu$Sv/hour (safe for in vivo use).
* **Image Processing:** Robot edges are extracted, and centerlines are fitted with **B-splines**. **Digital image correlation (DIC)** analyzes tissue displacement fields to compute strain.

![6](6.JPG)
---
### 4. Biomechanical Modeling and Validation

* **Magneto-Mechanical Model:** The robot-tissue interaction is modeled using **distributed magnetic torque and force balance equations**. Adhesion force ($F_a$) and viscoelastic parameters are derived from robot geometry and magnetic inputs.
* **Ex Vivo Validation:** Tests on porcine and murine gastrointestinal tissues (stomach, small intestine, colon) validate sensing accuracy. For example, adhesion errors on mouse stomach tissues are less than 10%, and viscoelastic moduli align with rheometer measurements.

![4](4.JPG)
![5](5.JPG)
---
### 5. Biomedical Applications and Translational Expertise

* **Disease Modeling:** The robot differentiates healthy and diseased tissues (e.g., TNK1-expression mice with impaired intestinal barriers) by detecting pH and viscoelasticity changes.
* **Minimally Invasive Design:** The robot's millimeter-scale size (6.5 mm $\times$ 2 mm $\times$ 15 mm) and untethered locomotion allow access to confined spaces with minimal invasion, avoiding surgical implantation.
* **Biocompatibility:** Surface coatings (PDMS, parylene C) prevent toxic particle exposure; future cell viability tests are planned.
> For more details, refer to "Wang, Chunxiang, et al. "In situ sensing physiological properties of biological tissues using wireless miniature soft robots." Science advances 9.23 (2023): eadg3988."