---
layout: post
comments: true
title: "#3 - Maithili Patel: Proactive Robot Assistance"
excerpt: "Maithili's research addresses the longitudinal proactive assistance problem - understanding user routines and preferences, anticipating assistive opportunities over an extended period of time. In this conversation, she addresses the importance of user-friendly interactions, proactivity, and personalization in robotic systems."
date: 2025-02-15 13:30:00
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

In this conversation, Maithili addresses the importance of user-friendly interactions, proactivity, and personalization in robotic systems. She emphasizes the need for robots to understand human routines while respecting user agency and preferences. The conversation also touches on emotional recognition, the significance of datasets like HOMER, and the challenges of deploying robots in real-world settings, particularly in multi-user environments. Patel warns against the potential for robots to replace human relationships, advocating for their role as facilitators of social connections.

<iframe 
    style="border-radius:12px" 
    src="https://open.spotify.com/embed/episode/1Uskgoce9xVJHuYCVSaM0y/video?utm_source=generator" 
    width="790" 
    height="100" 
    frameBorder="0" 
    allowfullscreen="" 
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
    loading="lazy">
</iframe>

**The inspiration behind Rosie the Robot.** Rosie the Robot from The Jetsons represents a vision of natural human-robot interaction that still inspires roboticists today. As Maithili notes, Rosie demonstrated an ability to interact with humans in a non-robotic way, emphasizing that humans shouldn't have to adapt to robots. While modern robots have evolved to understand natural language commands, Maithili's work aims to make interactions even more seamless, moving beyond the need for explicit programming or overly detailed instructions.

**Proactivity and personalization in robotics.** Proactivity and personalization are two key components in creating user-friendly robotic systems. Proactivity allows robots to anticipate routine tasks without constant commands, like preparing morning coffee. Personalization enables robots to learn and remember user preferences, such as how someone likes their eggs or coffee prepared. The goal is to reduce the burden of providing detailed instructions for every task while maintaining appropriate boundaries of automation.

**Understanding human routine and stochasticity.** Humans are creatures of routine, but with elements of unpredictability. Maithili's research shows that people often overestimate how chaotic their lives are. The challenge lies in creating robots that can recognize patterns while accounting for natural variations in human behavior. A successful proactive robot shouldn't aim for 100% prediction accuracy, as that would feel unsettling. Instead, it should understand both the patterns and the inherent randomness in human behavior.

**Agency and user preference in robotics.** The question of agency - who should perform which tasks - is crucial in human-robot interaction. Not every task should be automated, as people may prefer to do certain activities themselves. Maithili's research focuses on teaching robots to understand these boundaries through user feedback and explanations. For instance, if someone enjoys making coffee, the robot should learn to respect that preference and not intervene.

**Emotional recognition and nonverbal communication.** While affect recognition in robotics can identify basic emotions like happiness or sadness, understanding task-oriented emotional responses remains challenging. The field needs to develop more nuanced ways of interpreting human reactions in specific contexts, such as distinguishing between emotions during different activities or interactions.

**Spatio-Temporal Object Tracking (STOT).** STOT was developed to track object movements as indicators of human routines over extended periods. This approach was chosen because object tracking is more reliable than human activity recognition and easier for robots to observe. The system can predict object locations and movements, enabling robots to assist with tasks without needing to understand complex human behaviors.

**Advances with SLaTe-PRO.** SLaTe-PRO built upon STOT by incorporating activity recognition and making the system recurrent, allowing it to consider historical context rather than just current state. This advancement enabled the system to better understand and predict patterns in human behavior while maintaining the practical benefits of object-based tracking.

**Sparse user feedback and personalization.** The TAACo system was designed to learn user preferences with minimal interaction, using sparse feedback to understand boundaries and preferences. The system can generalize from limited feedback to understand broader patterns of what tasks users want robots to perform or avoid.

**The importance of explainability.** Explainability in robotics focuses on ensuring robots can justify their actions when asked. Rather than constantly explaining themselves, robots should maintain the ability to provide clear reasoning for their decisions when necessary. This becomes particularly important as robots become more autonomous and proactive in their assistance.

**Home vs. factory collaboration.** Human-robot collaboration in homes differs fundamentally from factory settings. While factory robotics focus on optimization and productivity, home robots must prioritize personal preferences and adapt to private space norms. The goal shifts from efficiency to meeting individual needs and respecting personal boundaries.

**Building robot-human relationships.** Robots should maintain a balanced relationship with humans, serving as functional agents while developing appropriate social interactions. The focus should be on helping facilitate human connections rather than replacing them, with robots acting as mediators rather than primary social companions.

**The HOMER dataset.** HOMER was created to enable research on proactive robotics by providing detailed, longitudinal data about human routines. The dataset combines crowdsourced information about daily activities with object-level details, creating realistic scenarios for training robots. This unique combination allows researchers to study both routine patterns and detailed interactions.

**Habitat-Sim connection.** While HOMER focuses on data generation, Habitat Simulator provides a complementary platform for testing robot-human interactions. The two systems work together, with HOMER providing the underlying data patterns that can be projected into various modalities within simulators like Habitat.

**Sim2Real gap.** The transition from simulation to reality presents challenges, particularly in maintaining perfect observability of object movements and human activities. Real-world deployment must account for imperfect perception and more natural, unpredictable human routines.

**Multi-user challenges.** While the current models don't fundamentally limit the number of users, testing in multi-user settings presents new challenges. The complexity increases with multiple users, requiring careful consideration of how predictions and mistakes might affect different individuals in the household.

**Addressing loneliness.** Proactive robot assistance can help address loneliness, particularly among elderly populations, but must be implemented carefully. Robots should facilitate human connections rather than replace them, serving as mediators that encourage real social interactions rather than becoming primary companions.

**Advice for AI researchers.** For aspiring AI researchers, Maithili emphasizes the importance of choosing research areas that genuinely interest them, given the rapidly changing landscape of AI technology. Success in a PhD program requires intrinsic motivation and finding the right advisor whose style matches yours.

> More of a visual learner? There's a YouTube video too. Click [here](https://www.youtube.com/watch?v=XFYgCRbc0Hc&t=1307s).

Maithili Patel is a Robotics PhD student in the Robot Autonomy and Interactive Learning (RAIL) lab, advised by Professor Sonia Chernova. The aim of her research is to address the longitudinal proactive assistance problem - understanding user routines and preferences, anticipating assistive opportunities over an extended period of time.