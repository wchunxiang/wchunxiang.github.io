---
title: 'Research'
date: 2025-05-19
type: landing

design:
  # Section spacing
  spacing: '6rem'

# Page sections
sections:
  - block: markdown
    # content:
    #   title: 'Research Interests'
    #   subtitle: ''
    #   text: |-
    #     Chunxiang Wang received his B.Eng. in Automation from Harbin Institute of Technology (2015–2019). From 2018 to 2021, he was with the Research Institute of Intelligent Control and Systems, where he worked on robotic micromanipulation for zebrafish microinjection, participating the development of 3D calibration, visual feedback, non-invasive object capture, and 3D posture control algorithms. He also independently developed a multi-object tracking system for zebrafish larvae under high density and occlusions.

    #     Since 2021, he has been a Ph.D. student in the D-PI at MPI-IS and D-ITET at ETH Zürich. His research focuses on soft millirobots with novel functionalities, integrating computer vision and closed-loop magnetic actuation. His expertise spans soft robot design and mechanics, image processing, medical imaging, and magnetic control systems.

    #     **Peer Reviewer:** IEEE/ASME Transactions on Mechatronics (T-Mech), IEEE Transactions on Cybernetics, IEEE International Conference on Robotics and Automation (ICRA), and Research.
    
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      view: article-grid
      fill_image: false
      columns: 3



  - block: collection
    content:
      title: Recent Publications
      text: ""
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation
---