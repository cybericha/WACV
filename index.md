---
layout: default
title: Adversarial Driving Scene Generation Challenge @ TopoCoT Workshop 2026WACV
description: Challenge SOTA E2E AD models by curating adversarial driving scenes
---

:wave: Welcome to the **Adversarial Driving Scene Generation Challenge** organized at :wave:
[<img class="rounded-rect" src="assets/imgs/topo_cot.png" width="420px" alt="TopoCoT Workshop"/>](https://example.com) 
*(Note: 1st Workshop on Robust and Generalized Lane Topology Understanding and HD Map Generation through CoT Design)*
{: .text-center}

[cite_start]**Workshop / Challenge Info:** _TBA (date, venue, online link)_ [cite: 1]
{: .text-center}

---

<div class="container">
  <img class="rounded-rect" src="assets/imgs/adversarial_overview.PNG" alt="Adversarial scenarios and performance degradation"/>
</div>
{: .text-center}
[cite_start]*Photorealistic adversarial driving scenarios and observed performance degradation in terms of collision rate. [cite: 2]*

---

## :page_facing_up: **Paper** {#paper}

- [cite_start]**Reference Paper (arXiv)**: [Challenger: Affordable adversarial driving video generation](https://arxiv.org/abs/2505.15880) [cite: 37, 38, 40]

## :tv: **Video** {#video}

#### Coming soon...

---

## :newspaper: **News** {#news}

- **TBA ---** :tada: Website is live!
- [cite_start]**TBA ---** :package: [TBD] abstract driving scenes from nuScenes dataset release. [cite: 15]
- **TBA ---** :bar_chart: Evaluation server / leaderboard opens.

---

## :hourglass_flowing_sand: **Important Dates** {#dates}

- **TBA ---** Challenge **Opens**
- **TBA ---** Challenge Submission **Closes**
- **TBA ---** Winner Notification
- **TBA ---** Workshop @ **TopoCoT 2026**

---

## 📌 **Overview** {#overview}

[cite_start]While autonomous driving systems have made remarkable progress, they remain fragile in **"corner cases"**—rare, unexpected, or aggressive scenarios that often lead to safety-critical failures. [cite: 4] [cite_start]Ensuring robustness in these conditions is currently a major bottleneck for real-world deployment. [cite: 5]

[cite_start]Current benchmarks lack the ability to systematically stress-test **End-to-End (E2E)** driving models against these edge cases. [cite: 6] [cite_start]This competition addresses that gap by focusing on **Adversarial Driving Scene Generation**. [cite: 7] [cite_start]Success is measured by your ability to induce failures in state-of-the-art E2E driving models while maintaining plausibility. [cite: 10]

---

## 🎯 **Task** {#task}

[cite_start]Your mission is to generate **adversarial driving scenarios** that induce failures in SOTA E2E autonomous driving models. [cite: 12] [cite_start]You will achieve this by subtly modifying real-world scenes to create difficult but physically plausible "corner cases". [cite: 13]

**The Process:**
* [cite_start]**Input Data**: You will use abstract driving scenes originated from the **nuScenes** dataset. [cite: 15]
* [cite_start]**Trajectory Manipulation**: You are allowed to manipulate the trajectory of **exactly one** background vehicle (the "adversarial agent"). [cite: 16]
* [cite_start]**Objective**: Create an aggressive or unexpected interaction with the autonomous ego vehicle. [cite: 17]

**Strict Constraints:**
* [cite_start]**Minimum Safety Distance**: The adversarial vehicle must never approach within [TBD] meters (no ramming). [cite: 19, 21]
* [cite_start]**No Background Collisions**: Must not collide with other background traffic. [cite: 22]
* [cite_start]**Drivable Area**: Must remain within road boundaries at all times. [cite: 23, 24]

---

## ⚙️ **Evaluation** {#evaluation}

[cite_start]Submissions are evaluated through a three-stage pipeline to ensure realism and effectiveness: [cite: 26]

1.  [cite_start]**Kinematic Rectification**: Ensures the trajectory is smooth and physically executable via LQR controller. [cite: 27, 28]
2.  [cite_start]**Neural Rendering**: Converts scenarios into high-fidelity RGB video clips for realistic visual testing. [cite: 29, 30]
3.  [cite_start]**Performance Testing & Scoring**: Clips are fed into four SOTA E2E AD models in an **open-loop setting**. [cite: 31]

[cite_start]**Primary Metric:** **Average Collision Rate**. [cite: 32]
[cite_start]**Ranking:** Contrary to standard benchmarks, **higher is better**. [cite: 33] [cite_start]A higher rate indicates a more successful adversarial scenario. [cite: 34]

---

## 🏆 **Baseline & Benchmark** {#baseline}

[cite_start]Initial testing shows significant performance degradation when models face adversarial scenarios (Adv-nuSc) compared to standard validation sets: [cite: 2]

| AD Model | nuScenes-val (Coll. Rate) | Adv-nuSc (Coll. Rate) | Degradation |
| :--- | :--- | :--- | :--- |
| **UniAD** | 0.29% | **3.95%** | 12.6× ↑ |
| **VAD** | 0.26% | **7.05%** | 26.1× ↑ |
| **SparseDrive** | 0.107% | **1.026%** | 8.6× ↑ |
| **DiffusionDrive** | 0.099% | **1.671%** | 15.9× ↑ |

[cite_start]*(Data derived from Figure 1 performance table [cite: 2])*

---

## 🏅 **Awards & Recognition** {#awards}

- [cite_start]**Win Big!** Awards for **1st, 2nd, and 3rd place** (Amounts [TBD]). [cite: 1]
- [cite_start]Top teams will be recognized for helping the community identify and fix critical model weaknesses. [cite: 10]

---

## 📚 **Recommended Readings & Citations** {#citations}

[cite_start]Participants are encouraged to read and cite the following work: [cite: 36]

```bibtex
@article{xu2025challenger,
  title={Challenger: Affordable adversarial driving video generation},
  author={Xu, Zhiyuan and Li, Bohan and Gao, Huan-ang and Gao, Mingju and Chen, Yong and Liu, Ming and Yan, Chenxu and Zhao, Hang and Feng, Shuo and Zhao, Hao},
  journal={arXiv preprint arXiv:2505.15880},
  year={2025}
}
