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
	在解决该类的小规模问题时，适合快速找出一个较好的局部最优解。
	随着规模逐渐扩大，得出来的解，偏差也会相应变大
### 优点：
- 解题速度极快，一次遍历就可以完成
- 具有更低的时间复杂度和空间复杂度
- 在解决无人机路线规划时，算法简单，容易理解
### 缺点：
- 得到的结果常常是局部最优解
- 依赖与之前作出的决定，从而导致可能会因此丢失了全局最优解
- 选择策略的判断，策略性质将直接决定算法的成败
## 蚁群算法（ant colont algorithm）
- ...
- ...
- ...
## 进展
|问题描述 | 贪心|蚁群|...|测试用例|
|-|-|-|-|-|
|5000*5000区域内，3个需求地，3个供应地；2辆车的载货量都是1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现1" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/text1.md" target="-blank">测试用例</a>|
|5000*5000区域内，50个需求地，50个供应地；5辆车的载货量都是1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现2" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/2" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现3" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现4" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
|5000*5000区域内，500个需求地，500个供应地；5辆车的载货量都大于1|<a href="https://github.com/chenyihangis/route-project/blob/master/贪心算法/代码实现5" target="-blank">代码实现</a>|||<a href="https://github.com/chenyihangis/route-project/blob/master/测试用例/3" target="-blank">测试用例</a>|
