# words

## Time-Optimal Planning for Quadrotor Waypoint Flight

polynomial 多项式

numerical optimization 数值优化

allocate 分配

resort to 采取

restore to 恢复到

capable 可行的 incapable 无法

simultaneous 同时

agile and maneuverable 敏捷与可操控性

continuous-time

discrete-time

quadrotor 四旋翼

state space representation 状态空间表示

differentially-flat

inherently 固有的

infinitesimal 无穷小

suboptimal 次优的

time-discretized 时间离散化

search and sampling-based 基于搜索和采样的

appoximation 近似  intracable 棘手的

system dynamics and input boundaries 系统动力学和输入边界

cost function 成本函数
complementary progress constraint 互补进度约束

intuitively 直观地讲

restricted to 受限于

maneuver 机动

specify 指定

aforementioned 前述的

traverse-dynamics 横向动力学

arc length 弧长

reference 参考

whereas 而

saturation  饱和

actuator 执行器

euler angle 欧拉角

refine 完善

feasible 可行的

take inspiration from 从...中获取灵感

non-convex 非凸 non-convexity 非凸性

interception 拦截

methodogy 方法论

respectively 分别

complement 补充 implement 实施

loss of generality 丧失一般性

fixed 固定的

coincide with  与...一致

decompose into 分解为

torque 扭矩

### planning time-optimal trajectories methods

+ Early works : **Using polynomial trajectory formulations**
+ Recently works : **Using numerical optimization , but require waypoints to be allocated as cost or constraints at specific discrete times ** 
+ This article propose : **propose a solution to the time allocation problem, by introducing a formulation of progress along the trajectory, which enable the simultaneous optimization of the time-allocation and the trajectory  **

### Two common approaches

+ continuous-time polynomials 
  + week-point :  These polynomials are inherently smooth and therefore cannot represent rapid state or input changes at reasonable order, They cannot exploit the full actuator potential
+ discrete-time state space representations
  + methods : 
    + search and sampling-based methods 
    + optimization-based methods
  + shortcoming :  when faced the multiple waypoints, the time spent between any two waypoints is unknown, so this is ineffective for time-optimal trajectory generation through multiple waypoints
+ This paper's approach : formulate a progress measure for each waypoint along the trajectory. And introduce a (Complementary Progress Constraint)CPC, this allows completion only in proximity to a waypoint.

  They formulate two factors which must complement each other

  + One factor : **the completion of a waypoint**
  + Another factor : **local proximity to a waypoint**


### methodology

+ **General trajectory Optimization**
  $$
  x^*=arg minL(x)
  $$

  $$
  subject\ to: g(x)=0\ and\ h(x) \leq 0
  $$

  + Multiple Shooting Method : 多重射击法

    Represent a dynamic system in the state space

    + system state(node) : x<sub>k</sub> 
    
    + actuation input : u<sub>k</sub>  
    
    + system evolution 
      $$
      \dot x = f_{dyn}(x,u)
      $$
    
      $$
      x_{k+1}-x_k-dt*f_{RK4}(x_k,u_k)=0
      $$

+ **Time-Optimal Trajectory Optimization**

  Optimizing for a time-optimal trajectory : **The only cost term** : overall trajectory time 
  $$
  L(x)=t_N
  $$
  

  + Passing Waypoints through Optimization

  + Progress Measure Variables

    To describe the progress throughout a track a measure that satisfy three requirements:

    + Start at a defined value
    + Reach a different value by the end of the trajectory
    + Only change when a waypoint is passed within a certain tolerance

  + Complementary Progress Constraints

  + Tolerance Relaxation

    Why this tolerance should be admitted?

    + It's impractical to force trajectory to pass exactly through a waypoint
    + negatively impacts the convergence behavior and time-optimality

    

  + Optimization Problem Summary

    

  + Quadrotor Dynamics

  

  

  

  
