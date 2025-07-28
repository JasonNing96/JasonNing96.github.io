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
* **Joint-Ph.D in Computer Science and Communication Technology** (May 2024 - Present)
  * A*STAR Institute for Infocomm Research (I2R), Singapore
  * Supervisor: Prof. Sumei Sun (Fellow of The Academy of Engineering, Singapore)

* **Ph.D in Traffic Control and Transport Engineering** (Sep 2021 - Present)
  * Dalian Maritime University, China
  * Supervisor: Prof. Tingting Yang (Pengcheng Laboratory)

* **M.S. in Electrical and Electronic Information Technology** (Sep 2018 - Jan 2021)
  * Minnesota State University, USA
  * Supervisors: Prof. JianWu Zeng, Prof. Vincent Winstead

* **B.S. in Electrical Engineering and Automation** (Sep 2014 - Jun 2018)
  * Guangxi University, China

Research Experience
======

* **May 2024 - Present: Joint-Ph.D Research Supervisor: Prof. Sumei Sun**
  * A*STAR Institute for Infocomm Research (I2R), Singapore
  * **LLM Edge Distributed Inference Algorithm (EdgePrompt)**: Designed distributed KV-Cache inference framework for wireless networks; implemented KV routing and consistency management, sharding and streaming strategies, reducing end-to-end latency and improving throughput in bandwidth-constrained scenarios.
  * **Distributed Split Speculative Decoding (DSSD)**: Combined speculative decoding with edge-cloud collaboration, innovatively designed network uplink/downlink logic, achieving at least 2X model acceleration. Funded by Huawei to attend 42nd ICML Machine Learning Conference.
  * **Hybrid Hierarchical Offloading Algorithm Design**: Targeting decoder-based generative models, constructed UE→Edge→Cloud layered offloading with memory/bandwidth constraints scheduling; used reinforcement learning for task granularity and routing, balancing QoS, energy consumption and cost.
  * **UAV-Assisted LLM Edge Inference**: In emergency/communication-limited weak coverage scenarios, combined UAV relay with DSSD strategies for link adaptation and task partitioning, improving edge user service quality and flexibility.

* **March 2023 - July 2024: National Key R&D Program "6G General AI Intelligence"**
  * Pengcheng Laboratory, Supervisor: Prof. Tingting Yang, Shenzhen, China
  * **National Key R&D Program Core Research**: Researched large model architecture deployment and protocol design in communication network problems. Focused on integrated communication-computation interfaces and network large model capabilities and deployment.
  * **IMTM2030 Report Co-authoring**: Collaborated with Huawei and other enterprises to write sections of the IMTM2030 Report, providing insights into future technology trends.
  * **Reliable Distributed Learning**: Two-Stage Coded Distributed Learning (Two-Stage Coded DL) and Byzantine-robust federated learning, targeting edge training/resource heterogeneity and failure tolerance.
  * **Edge-Cloud Collaborative Hardware Architecture Design**: Built communication and computation integrated platform based on KubeEdge/Kube-Wireless, implementing edge-cloud collaborative orchestration; designed bandwidth/memory/energy-aware scheduling strategies supporting inference concurrency, KV migration and consistency control. Recognized as "Top 10 Communication Advances of 2023".

* **March 2022 - February 2023: Huawei 2012 Wireless Technology Lab (Collaborating Supervisor: Lu Jianming, Huawei Fellow)**
  * **Communication Theory and 3GPP Standards**: Tracked communication theory and 3GPP standard development, researched application paths of machine learning/deep learning in wireless networks.
  * **National Key R&D Program Network4AI**: Participated in Network4AI project, focusing on communication resource scheduling and intelligent orchestration algorithm design and verification.
  * **Huawei KubeEdge Open Source Community**: Co-founded Huawei KubeEdge open source community, initiated and promoted Kube-Wireless Group for wireless scenario container networks.
  * **Container Edge Network and Management Tools**: Researched containerized edge networks and management tools, explored resource orchestration and observability systems integrating with 5G networks.

Work Experience
======

* **June 2021 - September 2021: CloudBu Innovation Lab**
  * Huawei Cloud Computing Technology Co Ltd, Shenzhen, China
  * Responsible for Kubernetes operations and maintenance and log system maintenance, implemented Edge-Mesh plugin using Golang.
  * Managed KubeEdge community: collected user requirements and submitted feature suggestions.
  * Led wireless working group to explore new scenarios, researched wireless network dynamic topology.

* **July 2020 - May 2021: Wireless Tech Lab**
  * Huawei 2012 Wireless Technology Lab, Shenzhen, China
  * Participated in 3GPP standards and AI optimization related work, Network4AI container network projects.
  * Developed SLAM algorithm prototypes, promoted intelligent perception and positioning research.
  * Coordinated project progress and requirements, wrote technical documents and conducted cross-team communication.

Skills
======
* **Model & Systems**: LLM Serving (vLLM/TGI/TensorRT-LLM), KV-Cache Management, Speculative Decoding, Prompt/Cache Routing, Streaming Inference
* **Platforms & Engineering**: Kubernetes, KubeEdge, Docker, CI/CD, Linux, Grafana
* **Algorithms & Optimization**: Distributed & Federated Learning (Byzantine-robust), RL for Offloading, Convex Optimization/Gurobi, PyTorch
* **Languages & Collaboration**: Python, Golang, Shell; Cross-team collaboration and project management (National Key R&D applications, open source community promotion, delivery)

Languages
======
* **Chinese** (Native)
* **English** (Fluent, TOEFL 96)
* **Japanese** (Beginner)
* **Cantonese** (Fluent)

Selected Publications
======
## Journal Papers

**Jiahong Ning**, Aiming Li, Ning Huang, Tingting Yang, Gary Lee, Sumei Sun, "MARHLO: Multi-Agent RL-Based Hybrid Offloading for Maritime MEC Network", *IEEE Transactions on Network Science and Engineering (TNSE)*, Under Review, 2025.

**Jiahong Ning**, Tingting Yang, Yongyi Su, "SkyDSSD: A UAV-Assisted Distributed Split Speculative Decoding Framework for Edge Inference", *IEEE Transactions on Cognitive Communications and Networking (TCCN)*, Under Review, 2025.

**Jiahong Ning**, Ce Zheng, Tingting Yang, "DeAOff: Dependence-Aware Offloading of Decoder-Based Generative Models for Edge Computing", *IEEE China Communications (ChinaCom)*, 2025, Accept.

Tingting Yang, Ping Feng, Qixin Guo, Jindi Zhang, Xiufeng Zhang, **Jiahong Ning**, Xinghan Wang, Zhongyang Mao, "AutoHMA-LLM: Efficient Task Coordination and Execution in Heterogeneous Multi-Agent Systems Using Hybrid Large Language Models", *IEEE Transactions on Cognitive Communications and Networking* **11**(2): 987--998, 2025.

## Conference Papers

**Jiahong Ning**, Ce Zheng, Tingting Yang, "DSSD: Efficient Edge-Device Deployment and Collaborative Inference via Distributed Split Speculative Decoding", *In The 42nd International Conference on Machine Learning (ICML)*, 2025, Accept.

**Jiahong Ning**, Pengyan Zhu, Ce Zheng, Gary Lee, Sumei Sun, Tingting Yang, "EdgePrompt: A Distributed Key-Value Inference Framework for LLMs in 6G Networks", *In 2025 IEEE International Conference on Computer Communications (INFOCOM)*, London, UK, 2025, Accept.

Patents and Industry Contributions
======
* **5 Chinese Patents** filed/granted in distributed learning, speculative decoding, and edge computing optimization
* **Multiple Industry White Papers** for 6GANA (6G Alliance of Network AI) on native AI technical requirements, network architecture, and distributed learning
* **Contributing Author** to "2024 10.0A GPT and Communication White Paper" and IMTM2030 Report

Honors and Awards
======
* **"Top 10 Technological Advances in Communication 2023"** - China Institute of Communications, for collaborative optimization of network architecture, protocols and experimental platform through communication and computing
* **ICML 2025 Travel Grant** - Huawei sponsored attendance at 42nd International Conference on Machine Learning
* **National Key R&D Program Participation** - Core contributor to "6G General AI Intelligence" project

Service and Leadership
======
* **Co-founder** of Huawei KubeEdge open source community and Kube-Wireless working group
* **Project Leadership** experience in National Key R&D Program applications and management
* **Cross-team Collaboration** coordinator between academia and industry (A*STAR, Pengcheng Lab, Huawei)
* **Technical Community Contributions** to KubeEdge, Kubernetes, and wireless edge computing ecosystems

{% comment %}
Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endcomment %}
