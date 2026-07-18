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

Hi there 👋🏻, I am Yi Gao (高熠), a third-year undergraduate student at the SWUFE-UD Data Science Institute. I am currently working with Dr. Pengxiang Ding at SymBiosis on **humanoid dexterous loco-manipulation with compliant human-robot interaction**.

Previously, I spent a summer at the Solution & Development Center, Lenovo Robotics Research Institute (Shanghai), where I worked on robot agents for real-world patrol scenarios.

My research interests lie in **spatial intelligence, world models, and embodied AI**. I am particularly interested in building learning systems that help embodied agents integrate perception, memory, decision-making, and action to acquire useful behaviors from diverse data and act reliably in the physical world. I am always open to collaborations, discussions, and new connections.

# Publications
<span class='anchor' id='publications'></span>

**CE4Patrol: Multi-Layer Context Reasoning for Industrial Anomaly Inspection**<br>
Yi Gao, et al.<br>
*WACV 2026 Workshop Submission / Manuscript*

# Experience
<span class='anchor' id='experience'></span>

## Compliance-Aware Policy-Tracker Interface for Humanoid Contact-Rich Loco-Manipulation
**SymBiosis**<br>
*Research Project, 2026 - Present*

- Investigating whether humanoid high-level policies should output explicit compliance intent in addition to motion intent for contact-rich loco-manipulation.
- Designing a structured 3D compliance token over `body_part`, `level`, and `lower_body_priority`, together with a lightweight grounding layer for existing humanoid trackers.
- Studying motion-only versus motion-plus-compliance interfaces with force-aware and tracking-aware evaluation in HumanoidArena-style settings.
- Positioning the work against SONIC, SoftMimic, CHIP, and HumanoidArena, with the main goal of policy-level action semantics rather than a controller-only patch.

## Context-Grounded Robot Agent for Industrial Patrol
**Lenovo Robotics Research Institute (Shanghai), Solution & Development Center**<br>
*Research Experience in Robot Agent Development, 2025.07 - 2025.12*

- Developed a context-grounded robot agent prototype for quadruped patrol in industrial environments, integrating visual perception, spatio-temporal context, safety-rule memory, and action protocols into a unified decision-making pipeline.
- Collected and organized real-world indoor/outdoor patrol data using a DEEPRobotics X30 quadruped platform, including 200+ video clips for evaluating context-dependent anomaly reasoning.
- Built an automated VLM evaluation workflow with image/video data collection, XML-style structured annotation, prompt-based reasoning, and comparative testing across QwenVL and GLM-family models.
- Designed a hierarchical context construction module that retrieves location/time-specific rules and maps detected violations to executable safety actions, enabling traceable decisions rather than passive visual classification.
- Drafted **CE4Patrol**, a WACV workshop submission on multi-layer context reasoning for industrial robot patrol, focusing on the gap between generic VLM perception and embodied, action-aware autonomy.
