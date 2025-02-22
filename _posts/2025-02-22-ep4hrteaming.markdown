---
layout: post
comments: true
title: "#4 - Batuhan Altundas: Human-Robot Teaming"
excerpt: "Batuhan's research focuses on developing intelligent scheduling systems that enable robots and humans to work together more effectively. He is the creator of HybridNet, a deep learning framework that helps robots understand and adapt to human learning patterns and performance variability in collaborative settings."
date: 2025-02-22 13:30:00
mathjax: false
---

<style>
.post-header h1 {
    font-size: 35px;
}
.post pre,
.post code {
    background-color: #fcfcfc;
    font-size: 13px;
}
.post blockquote {
    font-style: italic;
    background: #f9f9f9;
    border-left: 5px solid #ccc;
    margin: 1.5em 10px;
    padding: 0.5em 10px;
}
</style>

In this conversation, Batuhan discusses the evolving landscape of human-robot collaboration, emphasizing the importance of effective teamwork between humans and robots in various industries. He introduces HybridNet, a scheduling algorithm designed to optimize task allocation in heterogeneous teams, while addressing challenges such as scalability, trust, communication, and lifelong learning. The discussion highlights the adaptability of humans compared to robots and the necessity for human supervision in automated systems.

<iframe style="border-radius:12px" src="https://open.spotify.com/embed/episode/1Uskgoce9xVJHuYCVSaM0y/video?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>

**The state of human-robot collaboration.** Human-robot collaboration (HRC) is evolving beyond robots as mere tools to robots as teammates. Robots excel at precision and repetitive tasks, while humans bring adaptability and creativity. Collaborative robots (cobots) are increasingly deployed in homes, healthcare, and industries, such as during the Fukushima disaster, where robots handled hazardous tasks. The future of HRC lies in creating synergy between human adaptability and robotic precision, fostering teamwork rather than replacement.

**Human learning curves in robotics.** Humans improve task efficiency through repetition, a concept modeled in robotics research using learning curves. Studies like LEGO assembly tasks show how human performance accelerates with practice. Scheduling algorithms like HybridNet incorporate these learning patterns to balance immediate efficiency (via robots) with long-term human skill development. This approach ensures humans are neither overburdened nor underutilized during collaboration.

**HybridNet: a new scheduling algorithm.** HybridNet is an innovative scheduling framework combining graph neural networks (GNNs) and LSTM propagators. It models tasks, humans, and robots as nodes in a graph, enabling scalable task allocation for mixed teams. By leveraging GNNs for environment representation and LSTMs for sequential decision-making, HybridNet optimizes task assignments efficiently while accounting for human learning and stochasticity.

**Scalability challenges in human-robot teams.** Scalability remains a critical challenge in HRC. Traditional exact solvers cannot handle large-scale task allocation due to computational limits, while heuristics often lack accuracy. HybridNet addresses this by training on small-scale problems and deploying on larger ones, scaling up to 50 agents effectively. Future work aims to extend this capability to hundreds or thousands of agents.

**Trust and supervision in scheduling algorithms.** Trust between humans and scheduling algorithms is essential for effective collaboration. HybridNet allows human oversight, enabling modifications to schedules based on expertise or preferences. Transparency is key—explainable AI techniques can help users understand why specific decisions were made, fostering trust without compromising efficiency.

**Communication and coordination in teams.** Effective communication is crucial for human-robot teams, especially in dynamic settings like search-and-rescue missions. Graph-based representations enable adaptive communication networks that account for bandwidth limitations or agent range. Coordination strategies ensure smooth task execution even when full communication isn't feasible.

**Centralized vs. decentralized models.** Centralized models offer global optimization but struggle with scalability and single points of failure. Decentralized models are more robust and adaptable but may produce suboptimal solutions due to limited information sharing. A hybrid approach balancing centralized planning with decentralized execution could address these trade-offs effectively.

**Future directions in human-robot teaming.** The future of HRC lies in lifelong learning systems where robots continuously adapt through interaction with humans and environments. Challenges include avoiding local optima during learning and integrating trust-building mechanisms into algorithms. Research efforts aim to enhance scalability, transparency, and adaptability in human-robot teaming frameworks like HybridNet.

> More of a visual learner? There's a YouTube video too. Click [here](https://www.youtube.com/watch?v=D0TRBZBxqpc).

Batuhan Altundas is a PhD student in the School of Interactive Computing working in the CORE Robotics Lab under Professor Matthew Gombolay at Georgia Tech.