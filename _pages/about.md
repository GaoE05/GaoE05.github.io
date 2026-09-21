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

Hi, I am Yi Gao (高熠), a third-year undergraduate studying Information Management and Information Systems at the SWUFE-UD Data Science Institute, Southwestern University of Finance and Economics. I am enrolled in its four-year, China-based dual-degree program with the University of Delaware.

I work with Dr. Pengxiang Ding at SymBiosis on **learning compliant behavior for humanoid robots**, continuing remotely after a summer research internship. My current project, **SoftSONIC**, investigates whether a small learned residual can add compliant responses to a frozen motion-tracking policy.

My research interests are **robot learning, contact-rich manipulation, and humanoid whole-body control**. I am especially interested in how robots can respond to physical contact while retaining useful motion skills, and how these capabilities can support manipulation and tool use. Previously, I worked on context-grounded robot agents for industrial patrol at Lenovo Robotics Research Institute (Shanghai).

[CV (PDF)]({{ '/Yi_Gao_CV.pdf' | relative_url }}) · [Email](mailto:3490352665@qq.com) · [GitHub](https://github.com/GaoE05)

# Experience
<span class='anchor' id='experience'></span>

## SoftSONIC: Residual Learning for Humanoid Compliance
**SymBiosis**<br>
*Research Internship & Ongoing Remote Collaboration, May 2026 – Present*

- Independently responsible for the project implementation, experimental design, and analysis: developing a zero-initialized latent residual on top of a frozen SONIC motion tracker, using SoftMimic's compliant motion augmentation to construct training targets. The residual uses proprioception without external-force measurements at inference.
- Investigating learning failures through force-observation ablations, residual expressivity and closed-loop response probes, reward-scale analysis, and training-configuration checks.
- **Preliminary simulation results:** the project-specific compliance-progress score increased from **0.32 to 0.68** in an evaluation using 1,024 parallel environments with adaptive sampling disabled. Evaluation currently covers 10 standing motion clips with wrist perturbations; these are not held-out motions.
- Current work focuses on reducing tracking degradation without external forces and testing transfer to unseen motions. Broader motion generalization and real-robot validation remain open.

## Context-Grounded Robot Agent for Industrial Patrol
**Lenovo Robotics Research Institute (Shanghai), Solution & Development Center**<br>
*Research Experience in Robot Agent Development, 2025.07 - 2025.12*

- Developed a context-grounded robot agent prototype for quadruped patrol in industrial environments, integrating visual perception, spatio-temporal context, safety-rule memory, and action protocols into a unified decision-making pipeline.
- Collected and organized real-world indoor/outdoor patrol data using a DEEPRobotics X30 quadruped platform, including 200+ video clips for evaluating context-dependent anomaly reasoning.
- Built an automated VLM evaluation workflow with image/video data collection, XML-style structured annotation, prompt-based reasoning, and comparative testing across QwenVL and GLM-family models.
- Designed a hierarchical context construction module that retrieves location/time-specific rules and maps detected violations to executable safety actions, enabling traceable decisions rather than passive visual classification.
- Drafted **CE4Patrol**, a manuscript on multi-layer context reasoning for industrial robot patrol, focusing on the gap between generic VLM perception and embodied, action-aware autonomy.

# Manuscripts
<span class='anchor' id='publications'></span>

**CE4Patrol: Multi-Layer Context Reasoning for Industrial Anomaly Inspection**<br>
Yi Gao, et al.<br>
*Manuscript*
