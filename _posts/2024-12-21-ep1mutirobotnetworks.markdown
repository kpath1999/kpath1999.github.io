---
layout: post
comments: true
title: "#1 - Sandilya Sai Garimella: Multi-Robot Networks"
excerpt: "Sandilya's work focuses on multi-robot networks and contact perception using graph neural networks. His research aims to improve how robots coordinate and understand their environment, potentially leading to more versatile and capable robotic systems."
date: 2024-12-21 10:30:00
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

In this episode, we delve into multi-robot networks, exploring how robots coordinate to tackle complex tasks. This area is being researched by Sandilya Sai Garimella, as part of Professor Lu Gan’s lab.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LEN20XZSVOw?si=Mu2VlrZhFuKpyzq8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Inspiration from nature.** Multi-agent systems are all around us. You’ll see this behavior in ants and bees. A striking example is a school of fish evading predators. Hundreds of fish coordinate effortlessly to escape dolphins. So much so that dolphins come up with a separate strategy as a multi-agent system to catch their prey. Individual fish do not coordinate with every other fish in the school. Rather, they focus on their nearest neighbors. In nerd-speak, this is called a disconnected graph. This structure is more efficient because communicating with every other fish would be expensive and time-consuming. Therein lies the tradeoff between optimality and real-time responsiveness. In the research that Sandilya works on, these systems of collaboration are called decentralized multi-agent networks, where each agent does not necessarily communicate with every other agent. You are focused on your neighborhood, and through each robot working with its own neighborhood, you achieve coordination that is comparable to that if it were fully centralized.

**Centralization vs decentralization.** In a centralized network, all robots are fully connected and receive information from every other robot in the system. Decentralized networks, on the other hand, involve robots that do not coordinate with every other robot. Centralization, it turns out, has better optimality guarantees. This means that, in a map exploration setting, with every robot knowing every other robot’s actions, there is a better guarantee of covering the whole area by a certain amount of time. But the reason you want to move away from centralization is due to its real-time performance shortcomings. In such a system, robots need to transmit rich sensor data (e.g., RGB depth, LIDAR, 3D points) to all other robots (peer-to-peer) or a central base station. This can introduce substantial delays due to bandwidth limitations. If using a central base station, it would need to be extremely powerful to process and distribute data from all robots effectively. Such a system is also vulnerable to attacks. If an adversary compromises the base station, the entire fleet of robots could be grounded. That’s why it’s better to decentralize. They’re more resilient – if one robot fails, the others can continue to function.

**Critical point.** Imagine you and a friend are exploring a room, each with a flashlight. You’d naturally want to spread out to cover more ground. Now, add more friends with flashlights. At first, each new explorer helps cover more area. But eventually, you reach a point where adding more explorers doesn’t really help – they’re just getting in each other’s way. That’s the critical point - where the benefits of having more robots (or flashlight-wielding friends) start to level off. Or, as economists call it, diminishing returns. As you add more robots, each new one contributes less to the overall mission. There’s a sweet spot where you have just enough robots to do the job efficiently.

**Neighbor selection.** Imagine a swarm of drones exploring a vast area. There may be cases where a drone may need to know what’s happening on the other end of the map. The algorithm does not ignore this need completely. As drones zip around, they naturally come into range of different neighbors. Much like mingling at a party, you move around, chat with different groups, and gather information. This way, important information from far-away drones can still spread through the network, but without overwhelming everyone with constant chatter. The key, again, is finding a sweet spot: enough communication to be effective, but not so much that there’s information overload.

**Sim-to-Real Gap.** Sandilya and his team did their best to narrow this difference by mimicking real-world challenges such as communication delays and signal attenuation. The gap between simulation and reality remains wide. Below are a few considerations from the real-world worth making:

* Sensor measurements from cameras and IMUs may not follow the assumed Gaussian distribution.
* Hardware requirements are also daunting. Equipping 45 drones with RGBD cameras, depth sensors, semantic segmentation capabilities, and rotating gimbals would be costly.
* Specialized radio hardware is required for vehicle-to-vehicle communication, much like the DARPA Subterranean Challenge.
* Extensive software development would be needed, likely using ROS1 or ROS2, to manage fleet takeoff, task execution, and landing procedures.
* There are safety factors too, including protocols for handling drone crashes or malfunctions.

**The two paths ahead for robots.** “Robots can evolve in one of two ways. They can become cheap, reliable, and moderately productive. Or they remain complex and expensive but be spectacularly productive.” To democratize access, we would need to be in the first group. Sandilya’s first paper was on a cost-effective, six-legged robot made from styrofoam, costing under $1,500 – a far cry from the $30,000 price tag of Boston Dynamics’ Spot. It could move in 2D and had basic sensors. The robot used its walking motion to pluck dandelions without extra mechanisms, balancing cost and effectiveness.

**Connection to nature.** As Sandilya points out, “nature does it really good”. It’s not over-engineered; it’s just right. Now, let’s talk about MIHGNN (Morphology Informed Heterogeneous Graph Neural Network). It’s not as complex as it sounds. Imagine a four-legged robot that can feel the ground beneath its feet. That’s contact perception. Each leg has sensors measuring forces, enabling it to predict future forces on the robot’s feet as it walks. This happens with the graph neural network – by creating a virtual map of the robot’s structure, with each sensor and motor as a point on this map, this ‘graph’ mirrors the robot’s body. The network is trained on all sorts of terrains – flat ground, slopes, rough patches, even stairs. It’s all about making robots more in tune with their environment. Currently, these legged robots struggle with adapting to unknown terrains. For instance, a robot trained on sand might be able to handle gravel due to similar slippage characteristics. However, it would likely fail in a forest with leaves.

**Computational challenges.** Following Moore’s law, both training and inference capabilities of GNNs will improve over time. However, a significant bottleneck remains - collecting real-life data from robots. This requires more researchers to have access to robots and a common platform for data encoding. GNNs have one key advantage compared to traditional dynamics models. While both require significant compute power, GNNs can provide faster real-time inference once trained. The trade-off is clear: GNNs require more time and data for training but offer faster inference.

**His journey.** Sandilya’s transition from mechanical engineering to robotics highlights the interdisciplinary nature of the field. He faced challenges transitioning to programming, moving from MATLAB to C++, but overcame them with mentorship and perseverance. Here’s some of his advice:

* View tools as problem-solving instruments rather than ideologies. This will allow for more flexible solutioning.
* Develop a strong mathematical foundation, particularly in linear algebra. Stress fundamental concepts before venturing into the deep end.

For him, the goal of robotics and AI isn’t to replace humans but to augment their capabilities. His greatest joy comes from seeing abstract ideas transform into functioning robots and simulations. He believes that significant advancements in robotics won’t always require revolutionary paradigm shifts. Instead, he finds motivation in the incremental, iterative nature of technological development.

> On the go? There's an audio-only version too. Click [here](https://open.spotify.com/embed/episode/0XHV07vqsajxBW9znfMz0P?utm_source=generator&t=0).

Sandilya Sai Garimella is a graduate researcher in the field of robotics and artificial intelligence here at Georgia Tech. He’s worked closely on one of the crucial challenges in legged robotics: contact perception. Using graph neural networks, he is helping the field reconsider how robots understand and interact with their environment. Imagine a world where robots can navigate in any terrain as effortlessly as animals do. Sandilya’s research could one day make this a reality. And the best part is… his work doesn’t not stop there. It extends to multi-robot networks, exploring how systems can coordinate efficiently to tackle complex tasks, such as drone surveillance. What sets Sandilya apart is his multidisciplinary approach. He’s not just developing algorithms from an ivory tower. He’s reimagining how robots can learn and adapt in real-world scenarios. Beyond his research, we’ll also touch on the practical challenges of implementing these cutting-edge technologies and what it means for the future of industries ranging from agriculture to urban planning.