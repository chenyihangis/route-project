# 无人机路径规划
![](https://i.imgur.com/rK83I2I.jpg)
## 简介
   .....
## 目录
- [贪心算法](https://github.com/chenyihangis/route-project#greedy-algorithm)
- [蚁群算法](https://github.com/chenyihangis/route-project#ant-colont-algorithm)
- ...
- [进展](https://github.com/chenyihangis/route-project#project-progress)
## 贪心算法（greedy algorithm）
- 贪心算法的思想本质就是用局部解构造全局解，根据当前状态做出在当前看来最好的选择，即局部最优解选择，从而将所求问题简化为一个小规模的子问题
### 优点：
- 解题速度快，只需要一次遍历
- 时间复杂度和空间复杂度都是O(n)
- 解决无人机路线规划问题时，算法简单，容易实现
### 缺点：
- 得到的结果常常是局部最优解
- 贪心策略可以是每趟选择最短路径，每趟运输最多货物等，因此不同的贪心策略，决定所求得解的优劣
## 蚁群算法（ant colont algorithm）
- ...
- ...
- ...
## 进展
|问题描述 | 贪心|蚁群|粒子群|测试用例|
|-|-|-|-|-|
|250*250区域内，3个需求地，3个供应地；2辆车的载货量都是1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现1" target="-blank">代码实现</a>||<a href="https://github.com/chenyihangis/route-project/blob/master/粒子群/代码实现1" target="-blank">代码实现</a>|<a href="https://github.com/chenyihangis/route-project/blob/master/text1.md" target="-blank">测试用例</a>|
|5000*5000区域内，50个需求地，50个供应地；5辆车的载货量都是1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现2" target="-blank">代码实现</a>|<a href="https://github.com/chenyihangis/route-project/blob/master/蚁群算法/代码实现2" target="-blank">代码实现</a>||<a href="https://github.com/chenyihangis/route-project/blob/master/text2.md" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现3" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现4" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现5" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
