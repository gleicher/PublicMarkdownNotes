# Sensors V2

Robotics applications often require making tradeoffs in sensing. System needs for low power, size, weight, computation, robustness, latency and bandwidth may require tradeoffs in precision, accuracy, noise (NEED WORD FOR THESE PROPERTIES) and convenience of data representation. Statistically resolving sensors is an emerging sensor design strategy that can can be used to provide such tradeoffs: sensors provide statistical distributions of measurements, rather than specific details. Such sensors may be attractive for robotics applications where their SIMPLICITY is useful, if their non-standard and non-specific data can be used effectively.

In the project we will develop techniques that will allow statistically resolving sensors to be used in robotics applications. Our success will give robotics system designers new choices for sensors in situations where MINIMALNESS is important. For example, small and robust depths sensors would allow creating an "active skin" around an arm or snake that would allow it to navigate in an unknown confined environment; low power and computation, but high speed sensors could help a micro-drone localize; or a low latency motion detector could help a robot identify small defects in the environment. The core need is to develop approaches that allow the distribution data provided by these sensors to be used in applications that typically require unambiguous precision.

Our key idea is that when sensors are applied in robotics applications, we can exploit properties of robotics systems to circumvent some of the limitations of distribution resolving sensors. We will examine three general properties. 

1. A robot is able to **move the sensor**, often in known/controlled ways. By collecting measurements over time with motion, the observations may be improved and disambiguated.

2. A robot system is able to have **multiple sensors** and sources of information. A robot may use a collection of WEIRD sensors, couple these observations with data from other sensors or robots, or even prior knowledge of what is being sensed. Effectively using this information together can allow for WIERD DATA to be used despite its incompleteness and ambiguities.

3. A robot may be able to **act given imperfect data**. A robot may not need a complete detailed geometric model (the traditional representation constructed by sensing) in order to achieve its tasks.

We will develop these core capabilities by applying a currently available sensor, a depth histogram device, to a set of challenging robotics problems:

1. We will demonstrate how a "skin" of sensors placed over an arm can allow it to provide tele-manipulation that is responsive to both user control and the constraints of a dynamic environment. 

2. We will demonstrate how a robot can both localize itself in a known environment and detect subtle changes in that environment based on sensor observations.

3. We will demonstrate how a robot can plan motions in an unknown and dynamic environment using its sensors to create approximate maps as it progresses. 
4. 