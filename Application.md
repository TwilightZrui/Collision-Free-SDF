2018-RAL-Safe Local Exploration for Replanning in Cluttered Unknown Environments for Microaerial Vehicles
voxblox
选择从TSDF更新ESDF，而不是从octomap更新ESDF：允许系统从传感器数据实时增量地构建任意大小的地图。

参考价值：
V. MAP REPRESENTATION AND UNKNOWN SPACE 对UNKNOWN SPACE格子的处理方法

2020-RAL-Perceptive Model Predictive Control for Continuous Mobile Manipulation voxblox
github: perceptive_mpc
collision avoidance in SLQ
用RBF soft constraint mechanism 避免 collisions
缓存机制：caching gradients of an ESDF, 加速地图查询效率，足够给MPC用（缓存后HZ多少?MPC freqency多少）
虽然底盘是移动机器人，但是底盘的优化变量是六维
