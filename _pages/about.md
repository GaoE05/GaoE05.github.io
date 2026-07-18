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

我叫高翊，目前就读于西南财经大学-美国特拉华大学数据科学双学位项目，主修信息管理与信息系统，方向更偏向具身智能、机器人学习和 VLM/VLA 系统。

我希望把这份主页先搭成一个清爽、可靠、能持续更新的版本：先把简历里的经历和项目放上来，再慢慢补充论文、奖项和更完整的研究记录。

# Education
<span class='anchor' id='education'></span>

- **SWUFE-UD Data Science Institute (Dual-degree)**, 信息管理与信息系统, GPA 87.7/100, 2024.09 - 2028.06 (预计)
- **University of Delaware**, B.S. in Information Systems, 2024.09 - 2028.06 (预计)
- 主修课程：机器学习、Python 程序设计、数据结构、优化理论、数学校分析、高等代数、概率论与数理统计

# Skills
<span class='anchor' id='skills'></span>

- 编程语言：Python，熟悉模型训练与数据处理
- 深度学习：PyTorch，深度强化学习
- 模型理解：熟悉 π0、π0-FAST、π0.5、π*0.6 等系列模型与相关动作表示思路
- 机器人学习：了解连续动作生成、离散动作预测、动作序列压缩、环境泛化、错误累积等关键问题
- 工具平台：Git、Linux、Docker
- 英语能力：CET-4 632 分，CET-6 599 分，全国大学生英语竞赛二等奖

# Projects
<span class='anchor' id='projects'></span>

## 1. VLA/RL 机械臂抓取任务实践
2026.03 - 至今

- 基于 RoboBenchmark 跑通超场景 VLA 推理链路，完成 ManiSkill 仿真环境配置、资产下载、场景生成、模型服务启动与评测客户端联调。
- 复现并理解移动操作任务设置，覆盖 pick-and-place 与 open/close 两类任务，并尝试基于 π0.5 策略做微调与流程复现。
- 基于 MotrixLab 仿真平台与 PPO 算法做 Franka 机械臂抓取策略，梳理状态拼接、位置增量设计、稀疏奖励协同与行为可视化评估。

## 2. ACT 原理与实践
2026.02 - 2026.03

- 使用 PyTorch 构建并训练 VAE，完成 MNIST 手写数字重建可视化。
- 结合 VAE 与 Transformer 搭建 ACT 架构，理解 action chunking、attention 以及 proprioceptive data 与 state 的融合方式。
- 完整复现基于 ManiSkill 的 ACT policy 训练流程。

## 3. 基于 VLM 的机器狗工厂安防巡逻科研项目（投稿 WACV）
2025.09 - 2025.12

- 针对工业场景中“视觉正常但逻辑异常”的开放异常问题，分析传统 VLM 缺少上下文与时空逻辑盲区带来的痛点。
- 设计双模块架构：分层上下文构建与多源引导推理，通过 JSON 知识库、时空上下文和动作协议提升决策稳定性。
- 基于 QwenVL2.5 等模型做对比测试，整理 failure cases 并将实验结果撰写为科研论文。

# Internship
<span class='anchor' id='internship'></span>

- **联想上海研究院机器人实验室**, 2025.07 - 2025.09
- 搭建 VLM 自动化评估流程，使用 n8n 构建爬虫并自动采集图像，再调用 VLM 进行 XML 标注。
- 采集真实室内外场景数据，操作云深处 X30 机器狗，整理 200+ 视频片段。
- 设计上下文提示词，比较 QwenVL2.5、GLM4.1VL 等模型在异常检测任务上的表现，并输出对比报告。
- 调研主流 VLM 模型与智能驾驶方案，整理适合机器人任务的快慢双系统思路。

# Resume
<span class='anchor' id='resume'></span>

- [Download CV](/files/RESUME0605.pdf)
- [GitHub](https://github.com/GaoE05)
- [Email](mailto:3490352665@qq.com)
