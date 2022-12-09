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

## SDF from  Elevation map(2.5D)

### Package

* elevation_mapping_cupy
* GEM

### Paper

* Perceptive Locomotion through Nonlinear Model Predictive Control
  * SDF update frequency 20Hz
  * SDF 是从高度值算来的，把机器人近似成一个bounding box
  * MPC中的约束形式：![1670517883236](image/SDF/1670517883236.png)


## SDF from muti-elevation-map(3D)
### package
* elevation_map (RAW)
* 

### Paper
* Walking Posture Adaptation for Legged Robot Navigation in Confined Spaces
  * a robot-centric multi-elevation map
  * 2.5D elevation map存在的问题：elevation map是把障碍物中最高的一点记录下来，如果有墙，障碍物堆满， 不适用。
  * muti-elevation-map：会把overhanging obstacle remove，这样就会使地面的建图不会被悬挂的障碍物影响。缺点，不是ceiling ，把机器人当作了一个固定高度
  * 文章做法：扩展了ETH elevation map,用grid map库，把地面估计出来，当作地板，把地板层添加进map中的一个layer，把地图从2.5D扩展成3D，再算SDF
  * SDF是怎么用进轨迹优化问题中的:CHOMP

### Ref:
* 


## SDF in trajectory planning

* 2013_CHOMP_Covariant Hamiltonian optimization for motion planning
* 这篇
