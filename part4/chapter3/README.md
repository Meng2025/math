---
sort: 3
---
# 非线性系统

非线性才是工程里面的真实情况，前面都是线性定常系统，现在终于到了更广阔的领域了。非线性没有通用的、成熟的、统一的方法，线性定常是非线性的特例，前面分析的是在一定条件下近似的情况。

实际系统或多或少都会有非线性因素，哪怕电路也是。

典型的非线性如微分方程出现交叉项，或者出现正弦，或者加了个常数都会变成非线性，这是一种能用微分方程表述的。

还有另一种的非线性，比如一些典型的非线性特性。饱和、死区、间隙、继电特性等等。

三极管饱和失真、电机启动死区，齿轮间隙传动非线性，继电特性。这是静态的非线性，不是那种动起来微分方程的非线性。

[齿轮间隙非线性研究](https://kns.cnki.net/kcms/detail/detail.aspx?dbcode=CMFD&dbname=CMFD9904&filename=2004108801.nh&uniplatform=NZKPT&v=ldlTjca0Irgq5AsANSKMFaqIcolx7Kb%25mmd2B6MZ5YuYQHPK%25mmd2FUDLw6m4z7dC%25mmd2Fq1YqJx1o)


非线性系统运动的性质
- 不满足叠加原理：线性系统的理论不可用
- 稳定性问题：不仅与自身参数有关，与输入、初始条件有关，平衡点甚至不唯一。
- 自振运动：非线性系统特有的运动形式。自激振荡。
- 频率响应的复杂性：调频响应，倍频响应，分频响应，组合震荡。数学上混沌现象。

```tip
非线性最根本的一点，不满足叠加原理，所以数学上没有有效的工具，突破不容易，一旦突破不仅仅控制的问题，其他学科的问题也会有很大发展，因为数学是通用工具。

线性系统的稳定性和输入有关系，挺有意思。非线性不好讲广义的稳定性，这里要联系李雅普诺夫稳定性，从能量的角度理解一下。

自振很有意思，模拟电路里可以利用非线性，搞出信号发生器。

这和二阶系统零阻尼加阶跃的震动还不一样。指的是啥都不用，自己可以产生一个复制频率的运动，去掉扰动后还能回到这个幅值和频率。还有跳频响应啥的。这些都是长见识的东西，一开始不理解问题也不大。

混沌现象也挺好玩的，可以用电路模拟出来，后面做个仿真。

```


那么怎么分析呢？

- 小扰动线性化：经典。。工程到数学。

- 非线性系统研究方法
    - 相平面法
    - 描述函数法
    - 波波夫法
    - 反馈线性化方法
    - 微分几何方法

```note
都有局限性，但是基础都是数学。小扰动线性化是基于级数理论在稳定点舍去高阶作为近似，极限等价的思想。反馈线性在模拟电路里面全部都是，放大倍数几乎由反馈网络决定的条件，只不过叫做深度负反馈。

到现在，研究非线性还挺多，但都是针对一类的系统，没有通用的。
```

- 仿真方法
    - 全数字仿真
    - 半实物仿真

```note
仿真是个很重要的手段。半实物仿真比如飞机控制，飞机理论设计出来以后，要把控制器设计好，把实际的部件，传感器部件在地面上都做出来出来，用计算机模拟飞机特性，在地面把实际控制系统调好，然后上天，仿真模型和实际还有点差别，再优化一下参数。大概是这么个思路。

线性系统仿真也很常用。
```

这里主要去看两个方法，一个是直观的图解法，相平面。还有一个是充满了工程近似特色的描述函数法。

这里的非线性方法不是只能用于非线性系统，理想线性模型更可以使用。







