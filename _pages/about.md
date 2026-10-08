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

Hi, I am **Yi Gao (高熠)**, a third-year undergraduate at the [SWUFE-UD Institute of Data Science](https://dids.swufe.edu.cn/EN/Home.htm), pursuing a **B.S. in Information Systems**. I am based in Chengdu, China, and expect to graduate in 2028.

I am interested in **robot learning for physical interaction**: how robots can respond to contact while retaining the motion and support needed to complete a task. I currently work with [Pengxiang Ding](https://dingpx.github.io/) at [SymBiosis Robotics](https://symbiosis-robotics.com/research/dpc/en/), where I independently lead **SoftSONIC**, a project on learning compliant adaptation of a frozen humanoid motion controller. Previously, I developed context-grounded robot agents for industrial patrol at Lenovo Robotics Research Institute (Shanghai).

**I am seeking a remote research collaboration in contact-rich manipulation or humanoid control, available immediately for 30 hours/week.** I can contribute to policy implementation, reproducible simulation experiments, data pipelines, and deployment-oriented evaluation.

[CV (PDF)]({{ '/Yi_Gao_CV.pdf' | relative_url }}) · [Email](mailto:gaoe05@qq.com) · [GitHub](https://github.com/GaoE05) · [Reading notes (Xiaohongshu)](https://www.xiaohongshu.com/user/profile/602392d40000000001006528)

# Research
<span class='anchor' id='research'></span>

## SoftSONIC: Learning Compliant Adaptation of a Frozen Humanoid Motion Prior
**[SymBiosis Robotics](https://symbiosis-robotics.com/research/dpc/en/)** · *Research Intern & Ongoing Remote Collaboration, May 2026 – Present*<br>
*Research guidance: [Pengxiang Ding](https://dingpx.github.io/)*

Motion tracking specifies what a robot should do, but physical contact can require it to deviate from that motion. **Can we learn a reusable contact response on top of an existing whole-body controller, without retraining its motion prior?** SoftSONIC investigates this question by separating the nominal motion skill from a lightweight learned adaptation.

- **Method:** freeze the released [SONIC](https://nvlabs.github.io/GEAR-SONIC/) encoder and decoder, and learn a bounded **64-dimensional latent residual** from proprioceptive and previous-action history. PPO uses [SoftMimic-inspired](https://arxiv.org/abs/2510.17792) compliant motion targets and SONIC's native motion-quality rewards. Deployment requires no explicit external-force measurement for the residual actor.
- **Shared-policy study:** trained and evaluated a shared residual policy on **32 training motions in simulation**, with paired force/no-force comparisons and separate tests on references excluded from residual-policy training. Controlled studies of residual action spaces, observation conditioning, and reward variants examine the tradeoff between compliant response and nominal motion quality.
- **Real-robot progress:** deployed the adapter through a **50 Hz C++/TensorRT pipeline on a Unitree G1**. Hardware trials show qualitative yielding under manual pulls during standing, walking, and selected motion replays, including a backward-walking reference excluded from the residual-policy training set. These observations remain preliminary, and response strength varies across motions.
- **My contribution:** independently led the research question, method and data-pipeline development, experiment design and analysis, and deployment validation, with guidance from senior collaborators.

Current work scales compliance augmentation to thousands of loco-manipulation motion sources and tests broader shared-policy generalization. Large-scale training is in progress. Task-level evaluation with a fixed GR00T policy is a next step; the current hardware observations are not a calibrated stiffness or task-success benchmark.

*Updated October 8, 2026. Research in progress.*

## Real-robot demonstrations
<span class="anchor" id="demos"></span>

**Manual interaction during G1 motion replay.** The videos show standing, walking, and a door-opening motion from the residual training set, plus a **backward-walking reference excluded from residual-policy training** that also exhibits yielding. This is a preliminary qualitative observation; broader generalization evaluation is ongoing.

<div class="softsonic-demos">
  <figure class="softsonic-demo">
    <figcaption><strong>Standing</strong><span class="softsonic-demo-tag trained">Trained motion</span></figcaption>
    <video controls muted playsinline preload="none" poster="{{ '/assets/images/softsonic/stand-trained.jpg' | relative_url }}" aria-label="Standing with manual interaction">
      <source src="{{ '/assets/videos/softsonic/stand-trained.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support embedded video. <a href="{{ '/assets/videos/softsonic/stand-trained.mp4' | relative_url }}">Open the video</a>.
    </video>
    <a class="softsonic-demo-link" href="{{ '/assets/videos/softsonic/stand-trained.mp4' | relative_url }}">Open video</a>
  </figure>
  <figure class="softsonic-demo">
    <figcaption><strong>Walking</strong><span class="softsonic-demo-tag trained">Trained motion</span></figcaption>
    <video controls muted playsinline preload="none" poster="{{ '/assets/images/softsonic/walking-trained.jpg' | relative_url }}" aria-label="Walking with manual interaction">
      <source src="{{ '/assets/videos/softsonic/walking-trained.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support embedded video. <a href="{{ '/assets/videos/softsonic/walking-trained.mp4' | relative_url }}">Open the video</a>.
    </video>
    <a class="softsonic-demo-link" href="{{ '/assets/videos/softsonic/walking-trained.mp4' | relative_url }}">Open video</a>
  </figure>
  <figure class="softsonic-demo">
    <figcaption><strong>Door-opening motion replay</strong><span class="softsonic-demo-tag trained">Trained motion</span></figcaption>
    <video controls muted playsinline preload="none" poster="{{ '/assets/images/softsonic/door-motion-trained.jpg' | relative_url }}" aria-label="Door-opening motion replay with manual interaction">
      <source src="{{ '/assets/videos/softsonic/door-motion-trained.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support embedded video. <a href="{{ '/assets/videos/softsonic/door-motion-trained.mp4' | relative_url }}">Open the video</a>.
    </video>
    <a class="softsonic-demo-link" href="{{ '/assets/videos/softsonic/door-motion-trained.mp4' | relative_url }}">Open video</a>
  </figure>
  <figure class="softsonic-demo">
    <figcaption><strong>Backward walking</strong><span class="softsonic-demo-tag unseen">Not in residual training</span></figcaption>
    <video controls muted playsinline preload="none" poster="{{ '/assets/images/softsonic/backward-walking-unseen.jpg' | relative_url }}" aria-label="Backward walking with manual interaction">
      <source src="{{ '/assets/videos/softsonic/backward-walking-unseen.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support embedded video. <a href="{{ '/assets/videos/softsonic/backward-walking-unseen.mp4' | relative_url }}">Open the video</a>.
    </video>
    <a class="softsonic-demo-link" href="{{ '/assets/videos/softsonic/backward-walking-unseen.mp4' | relative_url }}">Open video</a>
  </figure>
</div>

<small>Recorded with an overhead safety harness and manual perturbations. Training labels refer only to the residual policy’s training set, not to the frozen SONIC models’ pretraining data. These clips demonstrate observed behavior, rather than a measured stiffness or task-success benchmark.</small>

# Experience
<span class='anchor' id='experience'></span>

## Context-Grounded Robot Agent for Industrial Patrol
**Lenovo Robotics Research Institute (Shanghai), Solution & Development Center**<br>
*Research Intern, July – December 2025*

- Developed a robot agent prototype that combines visual observations with location/time-specific rules and action protocols to support traceable industrial-patrol decisions.
- Collected and organized **200+ real-world video clips** using a DEEPRobotics X30 quadruped; built structured annotations and a VLM evaluation workflow comparing QwenVL and GLM-family models.
- Designed hierarchical context retrieval and drafted **CE4Patrol**, a manuscript on multi-layer context reasoning for industrial anomaly inspection.

## VLA Inference for Retail Mobile Manipulation
*Technical Project, March – April 2026*

Reproduced a **RoboBenchMart** VLA inference pipeline in ManiSkill, including asset preparation, scene generation, model serving, and evaluation-client integration for retail pick-and-place and open/close tasks.

# Manuscripts
<span class='anchor' id='publications'></span>

**CE4Patrol: Multi-Layer Context Reasoning for Industrial Anomaly Inspection**<br>
Yi Gao, et al. · *Manuscript*
