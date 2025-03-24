---
layout: post
comments: true
title: "#5 - Jeremy Collins: Causality, Consciousness & Video Learning in Robots"
excerpt: "Jeremy discusses the importance of data augmentation techniques like RoCoDA, video learning with AMPLIFY, and the challenges of generalization in robotics. He emphasizes the significance of causality, the long tail problem in robotic tasks, and the future of robotics in real-world applications."
date: 2025-03-23 19:30:00
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


In this conversation, Jeremy discusses innovative approaches to the data bottleneck in robotics through his work on RoCoDA (Robotic Counterfactual Data Augmentation) and AMPLIFY, which enable robots to learn from limited demonstrations and unlabeled video data. Jeremy explains how these methods leverage causal relationships and motion tracking to improve generalization across tasks. Beyond technical challenges, he reflects on what makes human cognition special, the "last domino" problem of deploying robots in real-world environments, and philosophical questions about consciousness, mortality, and suffering. Throughout the discussion, Jeremy shares insights on maintaining independent thinking in research and offers advice to aspiring researchers about balancing exploration with exploitation when developing their passions.

<iframe width="560" height="315" src="https://www.youtube.com/watch?v=yZ2Oe6pkZww" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**The marvel of human cognition.** The most beautiful fact about the universe is that humans can observe and understand themselves. This self-awareness represents something special that's challenging to replicate in robots. When discussing understanding, he defines it as approaching concepts from multiple angles and deriving them from first principles. Robots can understand to some extent, just as humans do, though both make mistakes. Jeremy challenges the notion that intelligence is merely statistics, arguing that while everything could be viewed statistically, causality can be modeled through conditional probabilities and counterfactuals—changing variables to observe outcome differences.

**Data augmentation with RoCoDA.** RoCoDA (Robotic Counterfactual Data Augmentation) addresses a key bottleneck in robotics: limited data. Typically, humans remotely control robots to collect training data, which is expensive and time-consuming. RoCoDA leverages symmetries in this data by identifying which environmental elements are relevant to tasks and which aren't. By randomly perturbing irrelevant objects (those that don't affect the correct action), they artificially expand the dataset. Unlike traditional data augmentation that modifies image properties, RoCoDA focuses on environmental interaction. Currently, humans specify task-relevant elements, but future versions aim to discover causal structures automatically through dynamics models that predict future states and identify what elements require attention.

**Video learning with AMPLIFY.** AMPLIFY, like RoCoDA, aims to alleviate the data bottleneck in robotics but uses a different approach. It relaxes the assumption that only direct robot-annotated data is useful by incorporating videos of humans or robots without action annotations and "off-task" data (robotics data without specified goals). AMPLIFY breaks down behavioral cloning into modules: a forward dynamics model predicting future observations based on language, and an inverse dynamics model predicting actions needed to cause predicted states. The system tracks keypoints (locations in video frames) through space using robust tracking algorithms that handle occlusion and camera movement. This approach enables task generalization—executing tasks without specific action annotations for them—which Jeremy considers the paper's most significant achievement.

**Being an independent thinker.** Jeremy credits his mechanical engineering background for helping him "go against the grain" in AI research. He observes that social media often creates intellectual monoculture, with researchers discussing the same papers and talking points simultaneously. To maintain independent thinking, he avoids recency bias by reading books from decades ago and listening to diverse podcasts. Jeremy emphasizes the importance of zooming out to recognize the broader history of ideas beyond the latest AI papers or Twitter discussions.

**Motivating questions.** Jeremy's primary motivation is making a positive impact on people's lives. He believes the next industrial revolution will involve AI and aims to create a future where everyone can live happy, long, fulfilling lives. Robotics appeals to him because it's an unsolved, challenging field that can give people more free time to pursue what they enjoy. He considers it tragic that many people don't enjoy their jobs, which constitute half their waking lives, and hopes selective automation can address this issue.

**Programming discomfort.** Jeremy believes suffering serves a purpose for both humans and robots. For humans, experiencing peaks and troughs leads to greater long-term happiness than optimizing for short-term pleasure. For robots, suffering could enhance robustness by helping them work around obstacles and avoid self-damage. He breaks down suffering into two components: frustration (barriers to goals) and physical threats (avoiding damage). Both are valuable qualities for robots to develop more robust planning capabilities.

**Mortality.** When discussing death, Jeremy admits he fears it and desires immortality. He challenges the notion that death gives life meaning, arguing that humans have finite context and prediction horizons regardless of lifespan. Even with infinite life, our limited ability to plan far ahead means our immediate actions wouldn't be affected by immortality. Similarly, concerns about experiencing everything and becoming bored are countered by our finite memory—we would forget experiences over time, allowing for renewed enjoyment.

**Consciousness.** Jeremy distinguishes between the "easy problem" of consciousness (self-awareness) and the "hard problem" (subjective experience). He references Wojciech Zaremba's view that intelligence is compression, and with sufficient compression, the compressor (mind) becomes one of the concepts being compressed, creating self-awareness. The harder problem involves qualia—subjective sensations like seeing red or tasting vanilla. Jeremy suggests consciousness might be merely a social concept, with no objective verification beyond one's vehement claims about their experiences.

**Advice for upcoming researchers.** For aspiring researchers, Jeremy recommends building habits with long-term goals in mind, absorbing as much information as possible, and following curiosity rather than forcing interest in trending topics. While he advocates following passion, he acknowledges that passion often develops through exploration. His own interest in AI grew from listening to podcasts and conducting research, not from an innate passion. Jeremy emphasizes the importance of balancing exploration (trying new things) with exploitation (pursuing known interests) and remaining open to discovering new passions through experience.

> On the go? There's an audio-only version too. Click [here](https://open.spotify.com/episode/4sIVw58lFg9UFVUxP3vvVu?si=3h7Y9UqxROu-6DU-XTg43g).

Jeremy Collins is a PhD student working at the intersection of deep learning and robotics, working under Professor Animesh Garg at Georgia Tech.