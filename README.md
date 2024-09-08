# SLAM and Path Planning for Outdoor Environments

This project was conducted as part of the 2022 Spring K-SW Square Program under Ministry of Science and ICT. It was carried out over 4 months by 4 students at Purdue University,USA. 

The [paper](https://ieeexplore.ieee.org/abstract/document/10023601) containing the project's results was accepted as a Regular Paper (8 pages) at the 2022 IEEE IRC CHARMS Workshop.

## Result Videos

### GPS-Mobile SLAM

<img width="1342" alt="Screenshot 2022-11-18 at 8 35 31 PM" src="https://user-images.githubusercontent.com/52185595/202696546-9d7a9dca-521f-4655-96ab-c5f99b1c348e.png">
[https://youtu.be/2mR5yEIUdMo](https://youtu.be/2mR5yEIUdMo)

### Demo Vehicle Production

![ezgif com-gif-maker](https://user-images.githubusercontent.com/52185595/202697340-7128bf4b-9954-4d7c-93c7-afd1b425d2e2.gif)


### Path Planning

<img src="%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Screenshot_2022-11-13_at_2.08.53_PM.png"  width="600" height="450"/>


## Summary

💡 This project focuses on SLAM and Path Planning in outdoor environments. The key part of the project was developing algorithms that account for the characteristics of "outdoor" environments. By adding GPS data to every phase of ORB-SLAM2 using a monocular camera, we achieved several benefits. For Path Planning, we incorporated the concept of "road stability" into the algorithm, improving the system by assigning greater weight to GPS data on stable roads to find optimal routes.

## Project Motivation

Purdue University, where we stayed, is located in Indiana, a region with many farms, which increased our interest in crop cultivation and farming technology.

<img width="283" alt="Screenshot 2022-11-13 at 3 00 18 PM" src="https://user-images.githubusercontent.com/52185595/201508149-f99eb777-49cc-400e-84ab-fc1f0fe01a60.png">

Farms in Indiana

There is a significant need for autonomous driving technology due to the large area of operations and the frequent need to transport materials and equipment.

Global path generation for autonomous driving requires maps. In outdoor environments, satellite maps using GPS are mainly used. On th other hand, for indoor environments, SLAM technology is used to map the internal structure in detail.

<img width="300" alt="Screenshot 2022-11-13 at 3 01 53 PM" src="https://user-images.githubusercontent.com/52185595/201508193-6d0f023d-486c-4c80-9ee9-c5a9f489de74.png">

GPS Satellite Map

![Point Cloud of the ORB-SLAM ](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/img7.jpg)

However, farms can be described as environments that are **outdoor but have indoor characteristics.**" This is because, while they cover a large area, information that GPS cannot capture (like tree trunks, branches, slopes, mud, etc.) significantly affects driving.

![IMG_0772.jpg](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/IMG_0772.jpg)

In environments with large tree branches, detailed mapping using SLAM is necessary, as GPS alone is insufficient. 

## Project Objective

💡 The creation of an outdoor SLAM and Path Planning algorithm for situations where GPS information alone is not sufficient.

## Project Progress

### Outdoor Environment Characteristics

Compared to indoor environments, outdoor environments have the following characteristics:
1) There are no traffic rules or lanes.
2) A criterion for determining obstacles is needed.
3) The environment constantly changes.

Considering these characteristics, we developed the system in three stages.

Detailed descriptions of the improvements to each algorithm can be found on the following pages:

[SLAM Algorithm Description](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/SLAM%20%E1%84%8B%E1%85%A1%E1%86%AF%E1%84%80%E1%85%A9%E1%84%85%E1%85%B5%E1%84%8C%E1%85%B3%E1%86%B7%20%E1%84%89%E1%85%A5%E1%86%AF%E1%84%86%E1%85%A7%E1%86%BC%20387384e4a12f409893cbe791838ca726.md)

[Path Planning Algorithm Description](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Path%20Planning%20%E1%84%8B%E1%85%A1%E1%86%AF%E1%84%80%E1%85%A9%E1%84%85%E1%85%B5%E1%84%8C%E1%85%B3%E1%86%B7%20%E1%84%89%E1%85%A5%E1%86%AF%E1%84%86%E1%85%A7%E1%86%BC%2009c37cd8bef1442ea143c8cd6c6a6de7.md)

## Results

### SLAM

<img width="391" alt="Screenshot 2022-11-13 at 12 56 52 PM" src="https://user-images.githubusercontent.com/52185595/201508261-72a5168e-2b1a-4791-b583-41c574d1d722.png">
<img width="393" alt="Screenshot 2022-11-13 at 12 57 31 PM" src="https://user-images.githubusercontent.com/52185595/201508264-58273c8d-5db5-4c28-8593-59a52075fe0c.png">

In Table 1, you can see that the number of Keyframes and Map Points extracted by our GPS Mobile SLAM is significantly lower than that of traditional ORB SLAM.

### Optimization Stage

![Screenshot 2022-11-13 at 1.08.19 PM.png](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Screenshot_2022-11-13_at_1.08.19_PM.png)


### Results

The map generated by the traditional ORB SLAM:

![Untitled](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Untitled.png)

The map generated by our algorithm:

![Untitled](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Untitled%201.png)

### After Algorithm Improvements

By adding GPS data to these three processes, we achieved the following benefits:

1. **Reduced Time Complexity by avoiding unnecessary computations**  
   In outdoor driving, it is common for vehicles not to move as intended (e.g., due to mud causing the wheels to slip). We used GPS data to calculate the vehicle’s movement distance and, if the movement was insignificant, we avoided the Tracking process. Additionally, meaningless Keyframes can degrade the map’s accuracy, so we ensured that Keyframes were not added to the map if the distance between a candidate Keyframe and an existing Keyframe was below a certain threshold. This improved map accuracy and reduced computations.

2. **Improved accuracy in Covisibility Graph creation**  
   When a new Keyframe is added, the Covisibility Graph of other Keyframes sharing the same map is updated. This graph allows the system to estimate the vehicle's pose without comparing every Keyframe. Features in the frames are typically used to estimate the correlation between Keyframes. However, since outdoor environments (especially forest terrains) make it difficult to extract features, we added GPS data to improve the comparison process by comparing the distances between Keyframes.

3. **Improved Relocalization accuracy**  
   If the vehicle fails to execute the Tracking process correctly, the system must estimate the current position using previous data. In this process, the Keyframe Database uses BOW (Bag of Words) to find Keyframes with high similarity to the current frame. However, this process consumes significant computing power and time. Additionally, using only the Keyframe Database is not highly reliable. We incorporated GPS data into this process by excluding distant Keyframes from the calculation and only computing Keyframes with GPS data similar to the current location. This reduced time complexity and improved decision reliability.

### Path Planning

![Screenshot 2022-11-13 at 1.22.22 PM.png](%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8B%E1%85%AC%20%E1%84%92%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A7%E1%86%BC%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B1%E1%84%92%E1%85%A1%E1%86%AB%20SLAM%20%E1%84%86%E1%85%B5%E1%86%BE%20Path%20Planning%20f27a9fcb14274713939a75f7e556ce16/Screenshot_2022-11-13_at_1.22.22_PM.png)

The original BIT* algorithm finds the shortest path regardless of the gray area (unstable roads), but our improved algorithm focuses on finding paths primarily through the white area (stable roads).

<img width="416" alt="Screenshot 2022-11-13 at 1 25 08 PM" src="https://user-images.githubusercontent.com/52185595/201508275-d8b5cf96-8deb-4510-a3b9-94a9d2c8f5f9.png">
<img width="530" alt="Screenshot 2022-11-13 at 1 25 04 PM" src="https://user-images.githubusercontent.com/52185595/201508277-fc59c870-2b15-4559-952d-77e3843f81f4.png">

The distance from surrounding obstacles is also measured to be greater than in the existing algorithm.

Additionally, the reduced number of samples allowed for decreased algorithm time complexity.

## Developers 👥

<img width="400" alt="Screenshot 2022-11-13 at 12 56 52 PM" src="https://user-images.githubusercontent.com/52185595/201508998-4a209b03-0420-4616-b48e-6563fb99a18c.jpg">

Seongil Heo `tjddlf101@hufs.ac.kr`

Jueun Moon `cindy4741@khu.ac.kr`

Jiwoong (Gio) Choi `jiwung22@gmail.com`

Jiweon Park `overflow21@khu.ac.kr`
