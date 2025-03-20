### Multi-Robot Path Planning with IRRT*-RRMS and Right-of-Way Rule

This research introduces the Improved RRT* with Reduced Random Map Size (IRRT*-RRMS), combined with the Right-of-Way (RoW) Rule for efficient multi-robot path planning. The RoW Rule enhances local navigation by integrating a virtual obstacle shape, guiding robots to avoid unknown obstacles while prioritizing right-side paths for optimized collision-free motion.  

![multirobots](/assets/img/project-multirobots.gif)

#### Key Features  

- *Collision-Free Navigation:* Ensures safe multi-robot movement using the RoW Rule.  
- *Virtual Obstacle Integration:* Enhances obstacle avoidance in dynamic environments.  
- *Optimized Path Planning:* Post-processing with Bacterial Mutation and Node Deletion improves path efficiency.  
- *Real-Robot Implementation:* Validated through three scenarios—head-on navigation, static obstacle avoidance, and dynamic obstacle avoidance.

### Pseudo algorithm: Virtual Obstacles

```pseudo
Algorithm VirtualObstacleAdding()
1:  if Unknown Obstacle Detected then
2:      Wait for 5 seconds
3:      if Dynamic Unknown Obstacle then
4:          Continue Motion
5:      else
6:          Static Unknown Obstacle
7:          Subscribe a current position and orientation (xc, yc) and θ
8:          Determine a distance to an obstacle as r
9:          Create a Virtual Obstacle
10:         Add a virtual circle with radius R at (xc + r ⋅ cosθ, yc + r ⋅ sinθ)
11:         Add Virtual Line with Length of d
12:         Add Virtual Half-ring with Radius R 
            at (xc + r ⋅ cos(θ + π), yc + r ⋅ sin(θ + π))
13:         Do the new path planning
14:     end if
15:     Do the motion
16: end if
```

### Results

The proposed method successfully achieves *collision-free* multi-robot path planning with *optimal* path selection. It adapts efficiently to dynamic environments and was successfully tested on real mobile robots, proving its effectiveness in practical scenarios.

![multirobots](/assets/img/project-multirobots2.png)

*Case: Robot 1 local path solution after head-on situation with No Obstacles*

For more information, please read the scientific paper:

[🔗 Publication](https://dl.acm.org/doi/10.1145/3702468.3702470)

[back](./)
