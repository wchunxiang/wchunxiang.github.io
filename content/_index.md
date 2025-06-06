---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "4rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: sun-tornado.svg #stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false
  # - block: markdown
  #   content:
  #     title: '📚 My Research'
  #     subtitle: ''
  #     text: |-
  #       Use this area to speak to your mission. I'm a research scientist in the Moonshot team at DeepMind. I blog about machine learning, deep learning, and moonshots.

  #       I apply a range of qualitative and quantitative methods to comprehensively investigate the role of science and technology in the economy.🧠✨
        
  #       Please reach out to collaborate 😃
  #   design:
  #     columns: '1'

  # - block: markdown
  #   content:
  #     title: '📚 Expertise'
  #     subtitle: ''
  #     text: |-
  #      <div class="expertise-block">
        
  #       ### Miniature soft robotics
  #       > Solidworks, Nanoscribe, Formlab, Ultimaker, LPKF Laser, VSM, Matlab...
  #       1. Robot design
  #       1. Fabrication
  #       1. Mechanical model
  #       1. Magnetic actuation
        
  #       ### Computer vision
  #       > Python, OpenCV, Scikit-learn, Pytorch, Tensorflow...
  #       1. Image processing
  #       1. Object detection, segmentation, tracking
  #       1. Generative models
  #       1. Medical imaging: X-ray, Ultrsound, Photo-acoustic.
        

  #       ### Robotic control: 
  #       > ROS, Franka-emika Arm, C++...
  #       1. Closed-loop robotic control systems:
  #         - Dual-robotic arm integrating ultrasound imaging and magnetic actuation
  #         - C-arm fluoroscopy and magnetic actuation
  #       2. Optimal filtering (e.g. Adaptive Kalman Filter, Particle Filter)
  #       3. Path planning
  #       4. Robotic arm control
  #       5. Robotic micromanipulation
        

  #       ### Multimedia Technology
  #       > Ps, Ai, Pr, C4D, Keyshot

  #   design:
  #     columns: 1
  #     view: article-grid
      # For the Showcase view, do you want to flip alternate rows?
      # flip_alt_rows: true 
      # spacing:
      #   padding: [0, 0, 0, 0]
  - block: resume-skills
    content:
      title: Skills
      username: admin
    design:
      show_skill_percentage: false
  
  # - block: markdown
  #   content:
  #     title: '📚 My Research'
  #     subtitle: ''
  #     text: |-
  #       Use this area to speak to your mission. I'm a research scientist in the Moonshot team at DeepMind. I blog about machine learning, deep learning, and moonshots.

  #       I apply a range of qualitative and quantitative methods to comprehensively investigate the role of science and technology in the economy.🧠✨
        
  #       Please reach out to collaborate 😃
  #   design:
  #     columns: '1'

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
  
  - block: markdown
    content:
      title: ''
      subtitle: ''
      text: |-
       <div class="expertise-block">
       
       ---
        To explore further details, please navigate to other tabs (Upper right).😃
       ---
    design:
      columns: '1'



  # - block: collection
  #   content:
  #     title: Recent Publications
  #     text: ""
  #     filters:
  #       folders:
  #         - publication
  #       exclude_featured: false
  #   design:
  #     view: citation

  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     view: article-grid
  #     columns: 1
  # - block: collection
  #   id: news
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: date-title-summary
  #     # Reduce spacing
  #     spacing:
  #       padding: [0, 0, 0, 0]
  - block: cta-card
    demo: true # Only display this section in the Hugo Blox Builder demo site
    content:
      title: 👉 Build your own academic website like this
      text: |-
        This site is generated by Hugo Blox Builder - the FREE, Hugo-based open source website builder trusted by 250,000+ academics like you.

        <a class="github-button" href="https://github.com/HugoBlox/hugo-blox-builder" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star HugoBlox/hugo-blox-builder on GitHub">Star</a>

        Easily build anything with blocks - no-code required!
        
        From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.
      button:
        text: Get Started
        url: https://hugoblox.com/templates/
    design:
      card:
        # Card background color (CSS class)
        css_class: "bg-primary-700"
        css_style: ""
---
