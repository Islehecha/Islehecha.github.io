---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D. student in Control Science and Engineering, Southern University of Science and Technology & Peng Cheng Laboratory, 2023.9-present
  * Advisor: Prof. Zhiyun Lin (IEEE Fellow)
  * Topic: Generative ergodic search and robust motion control for dynamic target distributions
  * Coursework: Matrix Analysis and Its Applications
* M.S. in Control Science and Engineering, Qingdao University, 2020.9-2023.6
  * Advisor: Prof. Lin Zhao
  * GPA: 3.61/4.0, top 20%
  * Research: Adaptive finite-time control for stochastic nonlinear systems
  * Coursework: Robotics
  * Honors: Outstanding Graduate, Second-Class Scholarship, Outstanding Student Leader
* B.S. in Automation, Wuhan University of Science and Technology, 2015.9-2019.6
  * GPA: 3.43/4.0, top 10%
  * Coursework: Principles of Automatic Control, Modern Control Theory
  * Honors: Outstanding Graduation Thesis, Outstanding Student

Research
======
* Generative ergodic search and robust motion control for dynamic target distributions
  * Built a hierarchical closed-loop architecture for dynamic target search.
  * Designed diffusion-model-based generative planning and reinforcement-learning-based simplex robust control.
  * Applied the framework to time-varying target search and planning-control-consistent motion synthesis under severe physical disturbances.
* Adaptive finite-time control for stochastic nonlinear systems
  * Built stochastic nonlinear system models and command-filtered adaptive backstepping finite-time controllers.
  * Proved practical mean-square finite-time stability with Lyapunov stability theory.
  * Applied the method to manipulator tracking control under random vibration.

Skills
======
* Python
* C/C++
* Matlab/Simulink
* ROS
* Gazebo
* CET-6: 512

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
