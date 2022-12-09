Distance Transforms of
Sampled Functions

欧几里得符号距离场（ESDF）可以很方便的对障碍物进行距离和梯度信息的查询，对空中机器人的在线运动规划具有重要意义。如何快速地生成ESDF地图是进行实时运动规划的重点

Voxblox [24] and FIESTA [25] are novel tools for volumetric
ESDF mapping.

Collision-free
mpc for legged robots in static and dynamic scenes,

FIESTA,速度快
我们在速度、精度上都是5-10倍的提升。
Fiesta: Fast incremental euclidean distance fields for online motion planning of aerial robots

[https://github.com/fzi-forschungszentrum-informatik/gpu-voxels](https://github.com/fzi-forschungszentrum-informatik/gpu-voxels)

在四足机器人运动中，SDF需要留意的是：

* Computation time for constructing
* Querying SDF time
* SDF是用的什么形式的地图：voxel map / elevation map

为什么要把机器人各个部分近似成球体，因为方便查询球体中心到障碍物的距离，查询的点少，高效，算力小。

## SDF from Elevation map

### Method

* elevation_mapping_cupy
* GEM

### Paper

* Perceptive Locomotion through Nonlinear Model Predictive Control
  * SDF update frequency 20Hz
  * SDF 是从高度值算来的，把机器人近似成一个bounding box
  * MPC中的约束形式：![1670517883236](image/SDF/1670517883236.png)
*

## SDF in trajectory planning

* 2013_CHOMP_Covariant Hamiltonian optimization for motion planning
* 这篇