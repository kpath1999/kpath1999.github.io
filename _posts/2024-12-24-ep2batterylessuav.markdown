---
layout: post
comments: true
title: "#2 - Rishabh Goel: Batteryless UAVs"
excerpt: "Rishabh’s work focuses on batteryless technologies and embedded systems. His team recently built batteryless UAVs that flap like birds. He’s one of the key minds behind Protean, a platform that enables batteryless sensors to perform machine learning tasks amidst unpredictable energy conditions."
date: 2024-12-24 10:30:00
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

In this episode, we delve into battery-free technologies, from UAVs that fly like birds to sensors that perform machine learning tasks amidst unpredictable energy conditions. This area is being researched by Rishabh Goel, as part of Professor Alexander Adams’ lab. Rishabh has also ventured into healthcare innovation with phantom organs, most recently a phantom lung.

<iframe width="560" height="315" src="https://www.youtube.com/embed/fAKvoZkC-Zo?si=mujF2MrVSPqDxeSh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Choosing projects.** His approach to selecting projects is straightforward: he pursues ideas he finds interesting and enjoyable. It could also help him learn a new skill. While he generates numerous ideas, he focuses on those that are fun for him - some of which eventually prove successful. Sustainability is a driving force behind this. He’s particularly interested in building products that stand the test of time, and capture energy from the surrounding environment in meaningful ways. There is abundant energy in our environment that’s often overlooked. Additionally, relying on fossil fuels and batteries can have adverse environmental impacts. There is a genuine need for more solutions that harness ambient energy.

**Narrowing it down.** The project that perfectly embodies this approach is the battery-free UAV project. The initiative combines existing drone technologies with a batteryless system, pushing the limits of both flight capabilities and energy harvesting. The goal is to create a drone that can fly for as long as sunlight is available, enabling much longer missions. Such a technology could revolutionize several applications, including environmental monitoring, wildlife monitoring, volcano activity monitoring, and city air quality assessment.

**Challenges ahead.** Drones today primarily rely on lithium-ion batteries. This is the most energy-dense option, but it has a few drawbacks. They are heavy, degrade rapidly, and are toxic to the environment. Battery-free drones aim to address these issues by directly harvesting energy from the environment. Several factors get in the way of realizing this vision. Funding is the main problem, as securing resources for a novel research area is an uphill battle. Some other issues:

* Investigating suitable materials for drone construction and energy harvesting
* Balancing payload capacity with battery-free capabilities
* Lack of interdisciplinary expertise, no aerospace engineers on the team

The complexity of the project lies in its numerous interconnected variables and design constraints.

**Flapping wings.** They’re efficient, just like nature. The drone can switch between high-power flapping for lift and thrust, and low-power gliding to conserve energy. The flapping motion has two parts: a downward flap, where the wings move down, pushing air down and creating lift, and an upward flap, where the wings move up, which can create an unwanted downward force. Birds have clever ways to deal with this downward force. Their feathers form a solid surface on the down flap but let air through on the up flap. This reduces the downward force. Birds also adjust their wing angles to manage airflow during different parts of the flap. Their research team is trying to copy these bird techniques, but it’s challenging. Right now, their drone can fly, but it still creates too much downward force on the upward flap.

**Material selection.** This was the crucial step. The team needed to balance durability, weight, and energy generation capabilities. For the body, the choice was straightforward: they required a material strong enough to withstand crashes but light enough to fly reliably. Carbon fiber emerged as the clear winner due to its excellent strength-to-weight ratio. The wings presented a more complex challenge. Initially, the team considered constructing the wings from solar panels to maximize energy harvesting. However, this idea had a significant flaw: as the wings flapped, the angle of the solar panels relative to the sun constantly changed. This resulted in inconsistent energy production, causing inefficient flapping or even failure to complete a flap cycle. To address this issue, a "solar parachute" design was developed. Solar panels were mounted on top of the drone, like a small canopy. While this added some drag, it was far less problematic than the energy loss caused by constantly changing panel angles on the wings. For the wings themselves, a lightweight nylon-type fabric was chosen. This material is flexible enough to generate lift, light enough to minimize motor size, and durable enough to withstand a few crashes. Keeping the wings light was essential—heavier wings would require a larger motor, which would demand more energy, creating a cycle of increasing weight and power requirements.

**Energy management.** The team uses supercapacitors instead of traditional batteries. These are ‘high-capacity capacitors’ that serve a small energy buffer between the solar panels and the drone’s systems. They help maximize solar panel efficiency. Using a maximum power point tracker (MPPT), the drone can adjust its power draw to get the most energy from the solar panels. The supercapacitor helps stabilize this process. In addition to maximizing efficiency, it handles intermittent power. If there is a sudden drop in solar energy (say from cloud cover), the supercapacitor provides enough power to keep the drone stable until it can harvest more energy. However, supercapacitors are much less energy-dense than batteries, which creates challenges. To address this, the team developed an energy-aware flight controller. This system dynamically adjusts flight conditions based on harvested energy, changes throttle limits and motor speeds in real-time, predicts energy harvesting based on recent trends, and balances energy input and output to maintain flight. Unlike traditional drones that only worry about low battery levels when it’s time to land, this system constantly manages energy levels. It looks at the current energy being harvested, recent energy accumulation trends, and past energy consumption trends. Using this information, the controller predicts whether to lower or increase throttle, ensuring that energy input is always greater than or equal to energy output. When the supercapacitor has enough charge, the system can even push for higher performance. This dynamic approach allows the battery-free drone to adapt to changing energy conditions in real-time, making the most of its limited energy storage capacity.

**A practical reality.** Battery-free UAVs have an exciting future, but several areas need to be worked on:

* Develop more UAVs with robust harvesting capabilities, reducing reliance on batteries.
* Address issues of extra weight, unreliable power supply, and sudden power loss risks.
* Create control systems that handle intermittent power and algorithms that account for energy uncertainty.
* Focus on fixed or flapping wing models that can glide or hover with minimal power.
* Boost research in long-duration, intervention-free flights.
* Develop better harvesting mechanisms, optimize storage and utilization.

**Battery-free inference.** Protean was a project led by Abu Bakar, a PhD student at Georgia Tech (now graduated). The idea behind this project was to create a prototyping platform to make research into battery-free computing more accessible, primarily for researchers or hobbyists trying to enter the field and learn more about it. Battery-free computing requires a lot of circuitry that isn’t necessary for traditional computing. For example, you need to be able to keep track of time even after losing power. In a battery-free computer, you can lose power, but you need to be able to tell how long it’s been since the last power outage. Most battery-free computing technologies use devices called timekeepers for this purpose. Battery-free computers typically rely on some sort of energy harvesting mechanism, such as solar panels, soil-powered harvesting, wind-powered harvesting, or thermal energy. You need an input that can accept energy from a harvester, which is quite different from a traditional power source. This often requires components like a Maximum Power Point Tracker (MPPT).

**Digging into thresholds.** When such a system turns on, it draws a sudden surge of current, causing a voltage drop that pushes the system below its operating threshold. This creates a cycle where the system cannot maintain enough voltage to function. This is where the thresholding mechanism comes in. It disconnects energy storage from the computational components until a safe voltage level is reached. This buffer protects against the initial current spike, ensuring the system can turn on and operate smoothly. Protean takes this a step further with a variable threshold. It’s an adjustable floodgate: for quick tasks, set a lower threshold, turn on sooner; for complex tasks, set a higher threshold, accumulate more energy, do more work.

**Modular design.** The team developed a modular system that allows users to snap on various peripherals. For example, to test facial recognition on a battery-free system, a camera module can be attached to the platform. Additional peripherals such as microphones, ADCs, or custom sensor boards can also be integrated. Power management is a key feature of the system. Users can dynamically control power to each sensor—whether external or internal to the board—using load switches. This enables an ultra-low-power state where virtually no components receive power. The modularity extends to the microcontroller itself, which can be replaced to support development on new platforms. The system utilizes a connector similar to M.2 SSDs, called Micromod from SparkFun. This design allows the platform to accommodate various microcontroller packages, enabling users to pair any microcontroller with any sensor to create a wide range of battery-free applications. To support battery-free computing, the board integrates essential components such as an energy harvester input, a variable threshold mechanism, timekeeping capabilities, and load switches for precise power control.

**Common theme.** There’s a red thread tying Protean with battery-free UAVs. Both rely on using energy intelligently and adapting to the environment. Once you go battery-free, you need to be much more careful with how you use energy because it becomes a very limited resource. With batteries, you don’t have to worry about energy until it’s time to replace the battery. The only energy conservation concern there is extending battery life. In day-to-day coding, you don’t worry about what happens if your code stops executing at a particular line. In battery-free systems, you must be more nuanced in how you design your hardware and write your code to work effectively.

**Phantom lungs.** The phantom lungs project originated from the PhD work of Dr. Alexander Adams. The team’s trying to monitor e-cigarette usage and record data on when a person vapes, as well as bodily signals such as heart rate or fidgeting. The goal is to predict and provide just-in-time interventions to stop people when they’re craving rather than after they have already smoked. Right now, the team’s trying to figure out which bio-signals are most closely linked to cravings and how to design such interventions to prevent smoking. Phantom organs lets researchers run tests without relying on human subjects. For instance, without a phantom lung, you would need to smoke dozens of e-cigarettes just to design and validate devices, adding significant variability and potential health risks. The phantom lung itself is pretty simple. It doesn’t breathe or use oxygen like a real lung. It works more like a plunger: compressing to push air out and relaxing to suck air in. That’s all we need to simulate how someone inhales from an e-cigarette.

**Moving forward.** There’s a lot happening right now. One big project is focused on a new way to harvest energy from impacts. On the vaping side, the team’s creating a device that snaps onto existing e-cigarettes and tracks when someone vapes, records the data, and sends it to an iPhone. Battery-free UAV work is ongoing and there are a few soft robotics projects keeping him busy as well.

> On the go? There's an audio-only version too. Click [here](https://open.spotify.com/embed/episode/4tQVp0l21cQIgZC3jIUfdR?utm_source=generator).

Rishabh's actively pushing the boundaries of engineering and sustainability. His work focuses on battery-free technologies and embedded systems. He’s one of the key minds behind Protean, a platform that enables battery-free sensors to perform advanced machine learning tasks while adapting to unpredictable energy conditions. He’s also explored the skies with his work on battery-free UAVs, inspired by bird flight. Imagine a drone powered entirely by solar energy, capable of ultra-long missions without the need for batteries. And if that’s not enough, Rishabh has also ventured into healthcare innovation with his work on phantom organs, like the phantom lung.