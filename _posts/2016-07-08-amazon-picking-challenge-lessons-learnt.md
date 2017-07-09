---
layout: page
title: Lessons Learned - Amazon Picking Challenge 2016
author: Feroze Naina
---

These lessons are derived from working towards the Amazon Picking Challenge (APC) between September 2015 and June 2016. I had an opportunity to interact with other teams during the final competition at RoboCup, Leipzig, Germany.

Our system consisted of modules for perception, grasping and motion planning tied together using ROS and smash state controller. I think our strength was in the simplicity of system.

**Software Codebase**

Should have sat down and written a list of software rules. 
Code reviews
not abusing ros - we used it everywhere
more wellthough out architecture, naming conventions
Lesser ros. More cpp. 
Code freeze 1 month before
UBonn - Nimbro team had nice software. They had some superb rqt plugins which would have made testing a lot easier. Lot of prior robocup soccer experience

**Testing**

Better testing architecture. Like really solid. Break down into smaller components. Decide interface. Test independently.
integration would have been awesome

In our case we had a perception,  planning and grasping. Should have built enough infra code for testing:
trajectory

introspection tool

Better state machine. 

**Motion Planning**
better caching infra, better planning speed

focus on score before hand - read into competition rule. Better to get 8 than all and fail.

// add stuff from notes

no team used in bin collision checking. Convex hull for detecting collisions. faster

**Robots & Actuators**

Early on, we made a decision to switch from the PR2 (which was already available to us) to a UR5. The PR2 had a moving base and a telescopic spine - these would have made planning more complex and slower. Universal Robots loaned us a UR5.

The UR5 was an amazing robot - it had tight ROS integration and was force compliant. We were up and running in no time. 

However, with the UR5, we had reachability issues - We could not easily plan paths to the corners of all the shelf bins as our end-effector greatly limited workspace. At the competition, we were the only team using the UR5. Many of the other teams had a UR10 robot with a linearly actuated arm - resulting in a much larger workspace, better reachability and easier planning. Next time, UR10 with a linearly actuated arm would be the way to go!

**End effector**

Due to the task, items and grasping complexity, most APC teams prefer to use suction grasping end-effectors. This obviates the need for accurate perception and force-closure for finger grasping.

The MIT team's end-effector was unique and large - it had grasping arms and suction. The Delft teams' was more elegant - suction and a clamp. These would have enabled them to grasp even the 3lb dumbbell and black mesh pencil cup.

Should not have finalized and put the end-effector design on hold. We saw a lot of teams having smaller suction cups. Better suction system. 

We used pretty basic electronics - Arduino, AC relays, pressure sensors and a linear actuator.

**Perception**

The top teams had a lighting setup mounted inside their workspace. This allows them better control for using CNNs for item identification. It would also allow them to transform the perception data to match lighting conditions of their training data set.

We were probably the only team using the bulky Kinect 2. Most teams used a smaller Creative Auto or Intel Realsense 3D sensors. A smaller sensor mounted on our arm would have allowed us to mount multiple sensors, giving better recongition. Would have also made in-bin planning much easier.

A huge drawback was that Kinect2 used time of flight technology compared to the other Structured Light sensors. // put links. The Halogens lamps mounted on the ceiling emitted IR radiation which interfered with our sensors and they had to be removed.
Most teams used creative. Halogen Lamps

multiple images - We should have taken multiple images of the items in the bin, giving us better recognition.

**Other Lessons**

<!--Focus on one thing for best results. In my second semester, I took up additional projects,research and actively partipated in cultural events. veered far too much in the other direction.-->

Better planning for transportation - If anything goes wrong, it will cause stress and in our hurry, we would overloop some other important factor. Me forgetting about transformer is a good example. 

Teams - this is the first time I'm working in a 5-person team for extended periods of time.

Balancing coursework, research and projects is pretty hard. I could really improve my time management. 

packing - send things before. more thought.  Things which will not work

worked with awesome team. Learnt a bit of mech and factors that go into designing things. Prototyping. programming funda.

Engineering workflow - I realized that the MRSD project course was structured very similar to the workflow in an actual company.
