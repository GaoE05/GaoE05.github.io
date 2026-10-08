---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<span class='anchor' id='about-me'></span>

Hi, I am **Yi Gao (高熠)**, a third-year undergraduate at the SWUFE-UD Data Science Institute, Southwestern University of Finance and Economics. I study Information Management and Information Systems in its four-year, China-based dual-degree program with the University of Delaware, with graduation expected in 2028.

I am interested in **robot learning for physical interaction**: how robots can respond to contact while retaining the motion and support needed to complete a task. I currently work with Dr. Pengxiang Ding at SymBiosis, where I independently lead **SoftSONIC**, a project on learning compliant adaptation of a frozen humanoid motion controller. Previously, I developed context-grounded robot agents for industrial patrol at Lenovo Robotics Research Institute (Shanghai).

**I am seeking a remote research collaboration in contact-rich manipulation or humanoid control, available immediately for 30 hours/week.** I can contribute to policy implementation, reproducible simulation experiments, data pipelines, and deployment-oriented evaluation.

[CV (PDF)]({{ '/Yi_Gao_CV.pdf' | relative_url }}) · [Email](mailto:3490352665@qq.com) · [GitHub](https://github.com/GaoE05)

# Research
<span class='anchor' id='research'></span>

## SoftSONIC: Learning Compliant Adaptation of a Frozen Humanoid Motion Prior
**SymBiosis** · *Research Intern & Ongoing Remote Collaboration, May 2026 – Present*<br>
*Research guidance: Dr. Pengxiang Ding*

Motion tracking specifies what a robot should do, but physical contact can require it to deviate from that motion. **Can we learn a reusable contact response on top of an existing whole-body controller, without retraining its motion prior?** SoftSONIC investigates this question by separating the nominal motion skill from a lightweight learned adaptation.

- **Method:** freeze the released [SONIC](https://nvlabs.github.io/GEAR-SONIC/) encoder and decoder, and learn a bounded **64-dimensional latent residual** from proprioceptive and previous-action history. PPO uses [SoftMimic-inspired](https://arxiv.org/abs/2510.17792) compliant motion targets and SONIC's native motion-quality rewards. Deployment requires no explicit external-force measurement for the residual actor.
- **Shared-policy study:** trained and evaluated one adapter across **32 motions**, with paired force/no-force comparisons and unseen-motion tests. Controlled studies of residual action spaces, observation conditioning, and reward variants examine the tradeoff between compliant response and nominal motion quality.
- **Real-robot progress:** deployed the adapter through a **50 Hz C++/TensorRT pipeline on a Unitree G1**. Standing, walking, and selected shared-policy motions show qualitative yielding under manual pulls, including preliminary observations on motions outside the 32-motion training set. Response strength varies across motions.
- **My contribution:** independently led the research question, method and data-pipeline development, experiment design and analysis, and deployment validation, with guidance from senior collaborators.

Current work scales compliance augmentation to thousands of loco-manipulation motion sources and tests broader shared-policy generalization. Large-scale training is in progress. Task-level evaluation with a fixed GR00T policy is a next step; the current hardware observations are not a calibrated stiffness or task-success benchmark.

*Updated October 8, 2026. Research in progress.*

# Experience
<span class='anchor' id='experience'></span>

## Context-Grounded Robot Agent for Industrial Patrol
**Lenovo Robotics Research Institute (Shanghai), Solution & Development Center**<br>
*Research Intern, July – December 2025*

- Developed a robot agent prototype that combines visual observations with location/time-specific rules and action protocols to support traceable industrial-patrol decisions.
- Collected and organized **200+ real-world video clips** using a DEEPRobotics X30 quadruped; built structured annotations and a VLM evaluation workflow comparing QwenVL and GLM-family models.
- Designed hierarchical context retrieval and drafted **CE4Patrol**, a manuscript on multi-layer context reasoning for industrial anomaly inspection.

## ACT and Imitation Learning
*Technical Project, February – March 2026*

Built an ACT-style Transformer with action chunking, reproduced an ACT training workflow in ManiSkill, and implemented a VAE to study latent-variable learning.

# Manuscripts
<span class='anchor' id='publications'></span>

**CE4Patrol: Multi-Layer Context Reasoning for Industrial Anomaly Inspection**<br>
Yi Gao, et al. · *Manuscript*
