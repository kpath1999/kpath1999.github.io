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

<iframe width="560" height="315" src="https://www.youtube.com/embed/D0TRBZBxqpc?si=nG1XIZMOAE91dx23" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**The state of human-robot collaboration.** Human-robot collaboration (HRC) leverages the complementary strengths of humans and robots. Humans excel at adaptability and improvisation, while robots handle repetitive, precise, or hazardous tasks. Real-world examples, such as the Fukushima nuclear disaster and nurse-patient scheduling, highlight how collaboration outperforms fully autonomous systems. A key motivation for HRC is integrating robots into human spaces, removing physical barriers like cages in manufacturing while addressing safety and operational concerns.

**Human learning curves in robotics.** Humans improve task efficiency through repetition, a concept modeled in robotics research using learning curves. Studies like LEGO assembly tasks demonstrate how human fluency evolves with practice. HybridNet incorporates these learning patterns into its scheduling algorithm, balancing immediate efficiency (via robots) with long-term human skill development. This approach is particularly relevant for seasonal jobs where workers must quickly gain expertise.

**HybridNet: a new scheduling algorithm.** HybridNet is a novel scheduling framework that combines graph neural networks (GNNs) for environment representation with an LSTM propagator for sequential decision-making. It addresses limitations of traditional methods like exact solvers (which lack scalability) and heuristics (which are suboptimal). By "dreaming" about future decisions rather than relying on real-time interaction, HybridNet generates faster and more efficient task-agent assignments, making it suitable for heterogeneous teams.

**Scalability challenges in human-robot teams.** Scalability remains a critical challenge in HRC due to the computational complexity of task allocation problems. HybridNet overcomes this by training on small-scale problems and deploying on larger ones, scaling up to 50 agents effectively. Traditional methods like exact solvers struggle with NP-hard problems at scale, while HybridNet's architecture allows for efficient scheduling without sacrificing adaptability.

**Trust and supervision in scheduling algorithms.** Trust between humans and scheduling algorithms is essential for effective collaboration. HybridNet supports human oversight by allowing modifications to schedules based on expertise or preferences. Transparency is key—explainable AI techniques can help users understand why specific decisions were made. This fosters trust without compromising efficiency and ensures that humans remain in control of critical decisions.

**Communication and coordination in teams.** Effective communication is crucial for human-robot teams, especially in dynamic settings like search-and-rescue missions. Graph-based representations enable adaptive communication networks that account for bandwidth limitations or agent range. These networks allow for both centralized communication models with full observation and decentralized models that adapt to real-world constraints.

**Centralized vs. decentralized models.** Centralized models offer global optimization but struggle with scalability and single points of failure. Decentralized models are more robust and adaptable but may produce suboptimal solutions due to limited information sharing. Hybrid approaches that balance centralized planning with decentralized execution could address these trade-offs effectively, especially in large-scale deployments like disaster response.

**Future directions in human-robot teaming.** The future of HRC lies in lifelong learning systems where robots continuously adapt through interaction with humans and environments. HybridNet supports online learning but faces challenges like avoiding local optima during training. Other frontiers include emotion-aware robots, democratized tools for collaboration, and integrating ethical considerations into task allocation to ensure both safety and human growth opportunities.

> On the go? There's an audio-only version too. Click [here](https://open.spotify.com/episode/66CQKWrURAYBrkyaYeaQlE?si=e1bd926410d54abc).

Batuhan Altundas is a PhD student in the School of Interactive Computing working in the CORE Robotics Lab under Professor Matthew Gombolay at Georgia Tech.