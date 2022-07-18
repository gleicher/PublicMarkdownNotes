# Sensing Proposal Notes - mid-July

[![hackmd-github-sync-badge](https://hackmd.io/4l4HXXawSiuuRhGtNtGGiA/badge)](https://hackmd.io/4l4HXXawSiuuRhGtNtGGiA)


Sensing involves tradeoffs. A robot system designer must balance requirements such as  power, size, precision, resolution, robustness, cost, latency, and computation. WEIRD SENSORS is an emerging sensor design strategy that provides an intriguing new point in the tradeoff space: they provide benefits in terms of simplicity, and therefore power, size, cost, robustness, latency and computation needs, in trade for providing data in an non-standard format with WEIRD properties. For example, a sensor might provide a histogram of scene depth values (Sec), rather than a per-pixel depth map, or it might provide bounds on scene motion, rather than a more standard flow map (Sec). The benefit of these sensors for robotics applications is that they can provide extremely favorable properties. The problem of these sensors is that in order to use them, we must devise new approaches that make use of their unusual data types.

Robotics applications often require making extreme sensor tradeoffs. For example, small and robust depths sensors would allow creating an "active skin" around an arm or snake that would allow it to navigate in an unknown confined environment; low power and computation, but high speed sensors could help a micro-drone localize; or a very low latency motion detector could help a robot safely avoid dynamic obstacles in a dangerous scenario. WEIRD SENSORS offer the potential to enable new robotics applications, however, we first must develop methods that allow robots to make use of the WEIRD DATA they provide in order to address the core challenges of robotics.

In this project we will develop approaches that enable WEIRD SENSORS for robotics applications. We will use currently available sensors and common robotics problems to drive our exploration, devising not only specific solutions but also general tools that will generalize to future sensors and robotics needs. Our key idea is to make use of the DATA directly, rather than trying to convert it to a more standard representation. 

Project Strategy: New sensing modalities continue to appear. This includes new sensor types that will provide other kinds of WIERD DATA. Therefore, we need to develop a thorough understanding of WEIRD DATA SENSORS and how they may be used in robotics to appreciate the potential and tradeoffs these devices provide. We therefore seek to develop both solutions for current sensors, but also common strategies that may apply across sensing modalities. We seek to address both some current specific robotics needs, but also to develop common strategies that will apply in future cases where extreme sensing is necessary. In this project, we propose to explore a few initial examples using current sensors and applications and to use our results in these cases to develop more generalized approaches that will transfer to future problems and sensors. 

WEIRD SENSORS offer a great synergy with robotics. On one hand, they offer properies that are desirable in robot sensing, including low power, low computation and communication demands, small size, and low cost. Conversely, robotics can address some of the shortcomings of the approach by being able to move the sensors in known ways, to integrate multiple sensors, and to have flexibility in the required representations. 

Core capabilities/ideas:
- geometric calibration
- differential analysis
- differential representations
- signature matching
- fusing multiple sensors (super-res, better localization)
- robot "fear" (be conservative - stay away from bad things so they don't have all of a sudden)

## Existing sensors

Emphasis: we see common challenges across the class, these "existing examples" give us something to work with now. Attractive for robots, but the big payoff is knowing how to work with these sensors

1. Depth Histograms
2. Speckle (motion magnitude detection)
3. Spots (fast position estimation)
4. **others?**

Common properties:
1. ambiguity in some dimension in trade for details in another
2. **what else?**

## Core Questions:
1. How do we interpret the observations from WEIRD sensors?

    Inherrent ambiguity. But, it might be resolved through geometric reasoning or making multiple observations (which we can do because we have a robot). Or, we might be able to interpret things in useful ways despite the ambiguity (see #3) but only if we understand it.

2. How do we bring together observations from multiple sources?

    May have many WEIRD SENSORS (use as a distributed sensor), or some other sensor (high quality sensor giving a map). How do we use them together?

3. How can we act given incomplete information?

    Typical robotics approach is to build a detailed representation (map) of the environment. But this may be overkill. What do we really need? What can we do with the limited things that we can get?

## Robotics things:
- maps for planning
- depth checks for trajectory optimization
- real-time movement synthesis
- localization in a known map
- checking of a known map (is there something that seems out of place)
- exploration (incremental map construction)


- tele-operation - don't need a whole map, just need to be responsive (to user and obstacles)
- SPLAM - use what ever information we have to update the model (map and position), use to fill gaps in the model (if you know what is in half of a scene)
- affordance identification (can we identify things with certain signatures - flat surfaces, clear places on the floor to drive on, grasp points)

