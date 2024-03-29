#### spfa

---------

##### spfa算法是单源路最短路中限制最小的一种算法

只要图中没有负环，就可以使用spfa算法，而一般的最短路问题中都一定没有负环

-------

##### spfa 算法是 bellman-ford 算法的优化版

优化 bellman-ford 算法更新距离这一步

因为 bellman-ford 算法需要遍历所有的边，但实际上只有前驱的距离变小了，后继的距离才会变小，因此创建一个队列来存距离有变化的前驱，用这个前驱更新后继的距离

如果一个前驱的距离没有被更新过，他的后继的距离一定没有被更新

##### :star:一般使用spfa算法判断负环

思路与bellman-ford算法一样，利用抽屉原理

##### 算法思路：

1. 先把起点放到队列中
2. 当队列不空的时候，意味着有待更新的点
3. 弹出队头 t，用 t 来更新他的后继的点的距离
4. 把 t 的后继加入队列

<img src="https://raw.githubusercontent.com/DaoZuQieXing/Learn/main/img/算法基础课/算法基础课第三讲：搜索与图论/spfa算法思路.png" alt="system call" style="max-width: 70%">

