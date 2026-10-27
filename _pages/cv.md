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
* **Ph.D. in Control Science and Engineering**, Southern University of Science and Technology (国家“双一流”建设高校) & Peng Cheng Laboratory (国家级新型科研机构), 2023.09 - Present
  * Advisors: Prof. Zhiyun Lin (**IEEE Fellow**), Assoc. Researcher Lingbo Liu
  * Topic: Generative Ergodic Planning and Robust Robot Execution for Dynamic Information Field Search
  * Coursework: Matrix Analysis and Its Applications
* **M.S. in Control Science and Engineering**, Qingdao University (山东省属重点综合大学), 2020.09 - 2023.06
  * Advisor: Assoc. Prof. Lin Zhao (**青年长江学者**)
  * GPA: **3.61/4.0 (Top 20%)**
  * Research: Adaptive Finite-Time Control and Multi-Agent Coordination for Stochastic Nonlinear Systems
  * Honors: Outstanding Graduate (2023), Second-Class Scholarship (2022), Outstanding Student Leader
* **B.S. in Automation**, Wuhan University of Science and Technology (中西部高校基础能力建设工程重点高校), 2015.09 - 2019.06
  * GPA: **3.43/4.0 (Top 10%)**
  * Coursework: Principles of Automatic Control, Modern Control Theory
  * Honors: Outstanding Graduation Thesis, Outstanding Student

Research & Project Experience
======
* **Generative Ergodic Planning & Robust Robot Execution for Dynamic Information Field Search** (2023.09 - Present)
  * **Role:** **Project Owner (First Author), 0-to-1 System Architecture & Implementation**
  * **World-Model Information Field:** Built the closed-loop architecture (*Local Observation + Target Detection + Map State → World-Model-Driven Predictable Information Map → Execution Feedback Loop*) for single-robot dynamic target search.
  * **Diffusion-Ergodic Planner:** Reformulated ergodic trajectory planning over information maps as conditional diffusion generation, combining offline structural priors of high-quality ergodic guides with online differentiable ergodic test-time guidance.
  * **Piecewise Simplex Robust RL Control:** Coordinated a hierarchy of formal piecewise controllers via high-level reinforcement learning to guarantee strict physical safety boundaries and planning-control consistency under external disturbances.
  * **Outputs:** 2 first-author papers in ***IEEE Transactions on Cybernetics* (SCI, 中科院 1 区, Major Revision)** and ***RAL* (Under Review)**.
* **Actionability-Aware Diffusion Bridge World-Action Model (`Bridge-WAM`) for VLN**
  * **Role:** **Project Owner, 0-to-1 Modeling, Evaluation Pipeline & Habitat Closed-Loop Integration**
  * **Actionability-Aware Diffusion Bridge:** Modeled current-to-future visual feature transitions via diffusion bridges with an actionability-aware objective to preserve action-discriminative cues for continuous action decoding.
  * **Benchmark Metrics:** On `val-unseen`, ground-truth visual change + language reduced **Action MSE by 34.68%** over language-only; `Bridge-WAM` reduced future feature change prediction error by **34.73%** over matched EDM, outperforming EDM across **all 18 configurations (3 random seeds × 6 loss weights)**, and reduced multi-step rollout Action MSE by **4.00% ($H=1$), 6.50% ($H=3$), and 3.34% ($H=5$)** across **3,000 / 1,000 / 500** unseen windows.
  * **Habitat Closed-Loop Execution:** Integrated the full online inference and control pipeline in Habitat, collecting **20,000 online transitions** across 50 episodes per method in two scenes.
* **Adaptive Finite-Time Control & Multi-Agent Coordination for Stochastic Nonlinear Systems** (2020.09 - 2023.06)
  * **Role:** **Project Owner (First Author), 0-to-1 Theoretical Modeling & Manipulator Simulation**
  * **Command-Filtered Adaptive Backstepping:** Designed command-filtered backstepping finite-time controllers with error compensation and Fuzzy/RBFNN approximators, eliminating the "explosion of complexity" and proving **practical mean-square finite-time stability** via stochastic Lyapunov theory.
  * **Outputs:** Applied to single/multi-manipulator tracking under random vibration; published **3 SCI papers (2 in *IEEE TCAS-II* [中科院 2 区], 1 in *IJFS* [中科院 3 区])** and **1 EI conference paper (CISC Best Conference Paper Award)**.

Publications
======
1. **Song X.Y.**, Li Y.Q., Yang J.K., Lu H.B.\*, Liu L.B.\*, Lin Z.Y.\*, Lin L.. Reinforcement Learning to Coordinate a Hierarchy of Piecewise Controllers for Robust Motion Synthesis. *IEEE Transactions on Cybernetics*. **(SCI, 中科院 1 区)**. **(Major Revision)**.
2. **Song X.Y.**, Li Y.Q., Guo X.Y., Yang J.K., Lu H.B., Liu L.B., Lin Z.Y., Lin L.. Diffusion-Ergodic: A Generative Framework for Information-Theoretic Exploration. *RAL*. **(Under Review)**.
3. Guo X.Y., Bai Y.J., **Song X.Y.**, Xu R.T., Liang X.D.\*, Wang M.\*. Safety-Aware Test-Time Adaptation for Dual-Arm Coordination from Vision-Language-Action Models. *IEEE Transactions on Industrial Informatics*. **(SCI, 中科院 1 区)**，待投。
4. Guo X.Y., **Song X.Y.**, Wang M.\*, Peng B.\*. Adaptive Finite-Time Consensus Protocol for Multiple Mechanical Manipulator Under Stochastic Vibration Conditions Based on Command Filtered Backstepping Method. *CCC*. 2025. **(CAA-A, EI 会议)**.
5. **Song X.Y.**, Zhao L.\*. Adaptive fuzzy finite-time consensus tracking for high-order stochastic multi-agent systems with input saturation. *International Journal of Fuzzy Systems*. 2022. **(SCI, 中科院 3 区)**.
6. **Song X.Y.**, Zhao L.\*. Finite-time command filtered adaptive control for robot manipulators in random vibration environment. *IEEE Transactions on Circuits and Systems II: Express Briefs*. **(SCI, 中科院 2 区)**.
7. Zhao L.\*, **Song X.Y.**. Finite-time control of high-order discrete-time systems. *IEEE Transactions on Circuits and Systems II: Express Briefs*. **(SCI, 中科院 2 区, 导师一作学生二作)**.
8. **Song X.Y.**, Zhao L.\*. Adaptive neural tracking control for stochastic nonlinear systems via finite-time command filtered backstepping. *The 17th CISC2021*. 2021. **(EI 会议, 优秀会议论文)**.

Skills
======
* **Embodied AI & Robotics:** ROS, Gazebo, Habitat, motion control, closed-loop simulation & benchmark evaluation
* **Deep Learning & Generative Models:** PyTorch, Transformer, Diffusion Models (EDM, Conditional Diffusion, Test-Time Guidance), Diffusion Bridge, Flow Matching, VLA / WAM, Deep RL (PPO, SAC, TD3, DDPG, DQN, A3C)
* **Engineering & Vibe Coding:** Python, C/C++, Linux/Ubuntu, CMake, Git, Shell, Claude Code, Cursor, Codex, Copilot, Skill / MCP / Sub-Agent / Context Engineering workflows
* **Control Modeling & Simulation:** Matlab/Simulink, stochastic nonlinear control, command-filtered backstepping, Simplex safety architecture, Lyapunov stability analysis
* **English:** CET-6 (512)
