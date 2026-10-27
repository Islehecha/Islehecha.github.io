---
permalink: /
title: "Xinyu Song (宋欣宇)"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. student in Control Science and Engineering at **Southern University of Science and Technology (SUSTech)** and **Peng Cheng Laboratory (PCL)**, advised by **Prof. Zhiyun Lin (IEEE Fellow)** and **Assoc. Researcher Lingbo Liu**. My research focuses on **Embodied AI, Dynamic Information Field Search, Generative Ergodic Planning (Diffusion / Bridge Models), World-Action Models (WAM), and Reinforcement-Learning-Based Robust Control**.

Throughout my graduate research, I have authored or co-authored **8 academic papers** (including **6 as first author or advisor-first/student-second author**) across top-tier journals and conferences such as *IEEE Transactions on Cybernetics* (SCI, CAS Q1), *IEEE Transactions on Industrial Informatics* (SCI, CAS Q1), *IEEE Robotics and Automation Letters (RAL)*, *IEEE Transactions on Circuits and Systems II: Express Briefs* (SCI, CAS Q2), *International Journal of Fuzzy Systems*, and *CCC* / *CISC* (Best Conference Paper Award).

Research Interests
======
* **Dynamic Information Field Search & Generative Ergodic Planning:** Conditioning diffusion models on world-model-predicted information maps with differentiable ergodic test-time guidance (`Diffusion-Ergodic`).
* **World-Action Models (WAM) & Vision-Language Navigation (VLN):** Actionability-aware diffusion bridge modeling (`Bridge-WAM`) and closed-loop embodied navigation in Habitat.
* **Simplex Robust Reinforcement Learning Control:** Coordinating hierarchical piecewise controllers via reinforcement learning for safety-critical motion synthesis under physical disturbances.
* **Stochastic Nonlinear Systems & Multi-Agent Control:** Command-filtered adaptive backstepping finite-time control and multi-manipulator consensus under random vibration.

Education
======
* **Ph.D. in Control Science and Engineering**, Southern University of Science and Technology ("Double First-Class" University) & Peng Cheng Laboratory (National Strategic Research Institution), 2023.09 - Present
  * Advisors: Prof. Zhiyun Lin (IEEE Fellow), Assoc. Researcher Lingbo Liu
  * Topic: Generative Ergodic Planning and Robust Robot Execution for Dynamic Information Field Search
* **M.S. in Control Science and Engineering**, Qingdao University (Key Comprehensive University of Shandong Province), 2020.09 - 2023.06
  * Advisor: Assoc. Prof. Lin Zhao (Changjiang Young Scholar)
  * GPA: **3.61/4.0 (Top 20%)** · Honors: Outstanding Graduate, Second-Class Academic Scholarship, Outstanding Student Leader
* **B.S. in Automation**, Wuhan University of Science and Technology (Key University of Hubei Province / National Midwest Higher Education Revitalization Program), 2015.09 - 2019.06
  * GPA: **3.43/4.0 (Top 10%)** · Honors: Outstanding Graduation Thesis, Outstanding Student

Research & Project Experience
======
### 1. Generative Ergodic Planning & Robust Robot Execution for Dynamic Information Field Search (2023.09 - Present)
* **Background & Objective:** Addressing local-optima traps and high online replanning overhead in high-dimensional non-convex dynamic target search, as well as physical safety-boundary violations under severe disturbances. Designed an end-to-end closed-loop architecture integrating global information-theoretic exploration with formal low-level safety guarantees.
* **Role & Contributions (Project Owner / First Author, 0-to-1 Architecture & Implementation):**
  * **World-Model Information Field Modeling:** Built the closed-loop pipeline (*Local Observation + Target Detection + Map State → World-Model-Driven Predictable Information Map → Execution Feedback Loop*), iteratively updating search priors from online execution feedback.
  * **Diffusion-Ergodic Planner:** Reformulated ergodic trajectory planning over information maps as a conditional diffusion generation problem; learned global structural priors of high-quality ergodic guides offline and integrated differentiable ergodic metrics for test-time guidance online.
  * **Piecewise Simplex Robust RL Control:** Designed a high-level RL coordinator over a hierarchy of formal piecewise controllers to translate generative ergodic guides into executable waypoint/region transitions while guaranteeing strict physical safety boundaries and planning-control consistency.
  * **Key Outputs:** Led **2 first-author papers** in ***IEEE Transactions on Cybernetics* (SCI, 中科院 1 区, Major Revision)** and ***RAL* (Under Review)**.

### 2. Actionability-Aware Diffusion Bridge World-Action Model (`Bridge-WAM`) for VLN
* **Background & Objective:** Tackling the *Prediction-to-Action Gap* in Vision-Language Navigation (VLN), where visually accurate future frame predictions do not necessarily improve continuous action decoding. Built a diffusion-bridge world-action model from current observations to future observations coupled with continuous action decoding, evaluated systematically against matched Elucidated Diffusion Model (EDM) baselines.
* **Role & Contributions (Project Owner, 0-to-1 Modeling, Benchmark Pipeline & Habitat Integration):**
  * **Actionability-Aware Diffusion Bridge:** Constructed cross-step visual feature transition modeling via diffusion bridges and introduced an actionability-aware joint optimization objective so predicted future visual features preserve discriminative action cues alongside visual fidelity.
  * **Offline & Multi-Step Rollout Benchmark:** Evaluated single-step and multi-step rolling horizons ($H=1, 3, 5$ across **3,000 / 1,000 / 500** unseen windows). On `val-unseen`, ground-truth visual change + language reduced **Action MSE by 34.68%** over language-only; `Bridge-WAM` reduced future feature change prediction error by **34.73%** over matched EDM, outperforming EDM across **all 18 configurations (3 random seeds × 6 loss weights)**, and reduced multi-step Action MSE by **4.00% ($H=1$), 6.50% ($H=3$), and 3.34% ($H=5$)**.
  * **Habitat Closed-Loop Integration:** Integrated the end-to-end pipeline (*Online Visual & Instruction Encoding → Future State Prediction → Continuous Action Generation → Waypoint Control → Atomic Action Execution → Metric Logging*) in Habitat, collecting **20,000 online transition steps** across 50 episodes per method in two scenes.

### 3. Adaptive Finite-Time Control & Multi-Agent Coordination for Stochastic Nonlinear Systems (2020.09 - 2023.06)
* **Background & Objective:** Overcoming the "explosion of complexity" in classical backstepping and handling input saturation and stochastic vibration in high-order nonlinear and multi-manipulator systems.
* **Role & Contributions (Project Owner / First Author, 0-to-1 Theory & Simulation):**
  * **Command-Filtered Adaptive Backstepping:** Formulated error-compensated command-filtered backstepping controllers with Fuzzy Logic / RBF Neural Network approximators and proved **practical mean-square finite-time stability** via stochastic Lyapunov theory.
  * **Key Outputs:** Applied to single/multi-manipulator tracking under random vibration; published **3 SCI journal papers** (including **2 in *IEEE TCAS-II* [CAS Q2]** and **1 in *IJFS* [CAS Q3]**) and **1 EI conference paper (CISC Best Conference Paper Award)**.

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

Technical Skills
======
* **Embodied AI & Robotics Simulation:** ROS, Gazebo, Habitat; end-to-end state encoding, world-model prediction, trajectory generation, and closed-loop waypoint control.
* **Deep Learning, Generative Models & RL:** PyTorch, Diffusion Models (EDM, Conditional Diffusion, Test-Time Guidance), Diffusion Bridge, Flow Matching, Transformer, VLA / WAM, PPO, SAC, TD3, DDPG, DQN.
* **Engineering & Agentic / Vibe Coding:** Python, C/C++, Linux/Ubuntu, CMake, Git, Shell; Claude Code, Cursor, Codex, Copilot; Agentic Workflows, Skill Systems, MCP, Sub-Agents, Context Engineering.
* **Nonlinear Control Modeling & Stability Analysis:** Matlab/Simulink, stochastic nonlinear systems, command-filtered backstepping, Simplex formal safety control, Lyapunov stability proofs.
