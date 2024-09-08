# Path Planning Algorithm Explanation

This section determines **which path the vehicle should take** based on the map created in the previous SLAM stage using the Path Planning algorithm. We identified that a search-based algorithm, **BIT***, is suitable for our project, and we have improved upon it.

### Algorithm Improvement Method

Conventional pathfinding algorithms search for the route based on the shortest distance. However, in real-world driving, factors such as roads and obstacles in the driving environment must be considered. Since this research presents “outdoor” as the experimental environment, two factors below became even more critical, which were added to our Optimization Criteria.

1. **Clearance**
   This refers to the **distance from surrounding obstacles**. 
   First, we consider the size of the vehicle at the current state and determine if there are obstacles within a certain distance. Then, we quantify the number of obstacle and unknown space pixels in a certain range around the state to determine the Clearance Factor. 

2. **Stability**
   Stability was added to select a more stable route considering the rugged terrain of the outdoor environment. The stability of the path is measured in the SLAM stage, and this result is applied to the weights.

![Untitled](Path%20Planning%20%E1%84%8B%E1%85%A1%E1%86%AF%E1%84%80%E1%85%A9%E1%84%85%E1%85%B5%E1%84%8C%E1%85%B3%E1%86%B7%20%E1%84%89%E1%85%A5%E1%86%AF%E1%84%86%E1%85%A7%E1%86%BC%2009c37cd8bef1442ea143c8cd6c6a6de7/Untitled.png)
