## 单狗

### 事情

#### 导航

全局路径规划  in: 点云  out: 全局路径（road点）

局部轨迹规划   in :全局路径参考点 ref out : 一段时间内or一段距离内 COM pose（x y z r p y ）

落足点规划

MPC足端轨迹规划

#### 全局规划

3D全局ESDF ，RRT*搜索满足质心不碰撞、足端一定碰撞的全局路径

全局地图：加载的

局部轨迹规划
考虑两个问题：
1.地图表现形式
elevation map :不行 没有code ，不好接
点云数据更新ESDF map：
方法：
FISTA
