# Physics
 Feynman-physics

这是对热力学的一个小结，不过就结果而言，仅包含一些公式，略去了其推到和证明过程，以期可以在不久的考试中用到

不过，虽说仅仅是公式的陈列，依然有先来后到之分，按照一般的逻辑顺序，我们先从气体动理论开始

为了描述气体的状态，如同描述一个物体在空间中的位置一样，我们给定三个参数：压强（ $p$ ），温度（ $T$ )，和体积（ $V$ )来刻画气体的状态，我们之所以选取这三个参数来表征气体，是因为我们可以推导出理想气体方程（严格意义上来说，上面的描述是本末倒置的，不过这仅仅是为了方便说明而已）

理想气体方程：
$$
pV=nRT
$$
其中 $n$ 指物质的量

上面的式子表明了气体可以对外做的功（内能，或者也可以说是理想气体（一团理想的原子（分子团））内部所蕴含的能量）大小与该理想气体所处的温度大小（一种宏观上的状态，通俗的来说，我们可以将这种状态描述成“冷”或者“热”，如果要具体量化，在物理学上使用的是开尔文温标 $k$）成正比

而参数 $R$ 则指的是普适气体常量，在国际单位制下是 $8.31J/(mol \cdot K)$ 

有了上面的理想气体方程，我们可以计算一些初步的参数

例如在已知初始状态的压强和温度的情况下，可以借此计算出气体的体积
$$
V=\frac{nRT}{p}
$$
接着假如发生了一些变化（比如温度变化或者气体泄漏，不过一般来说两者同时发生，只是参变量和自变量的区别），假设容器的体积没有变化，那么我们假设压强减小（或者增加，这无伤大雅）到了 $p'$，温度降到（或者增加到） $T'$，那么接下来我们可以计算容器中到底发生了什么变化，以计算泄露气体的量为例

容器中剩余气体的物质的量为
$$
n'=\frac{p'V}{RT'}=\frac{p'\frac {nRT}{p}}{RT'}
$$
接着是理想气体分子的动能，我们为什么要讨论动能？是因为我们知道，温度越高，气体分子运动的速度也就越快；反之也一样，那么我们不难联想到，温度或许与气体分子的运动存在某种联系。比如，温度是否就是这种运动的宏观表现？另外，我们在这里也做出了一些前提假设，不过此处略去不表。

可以计算得到，分子在三个方向（笛卡尔坐标系的三个轴向）上的平均速度分量大小都相等，也就是说
$$
\bar{v^2_x}=\bar{v^2_y}=\bar{v^2_z}=\frac13\bar{v^2}
$$
不难推导得到，基于上面的假设，如果记理想气体分子的平均动能为 $\bar{\epsilon_k}$ ，那么有总压强
$$
p=\frac23n(\frac12m_0\bar{v^2})=\frac23n\bar{\epsilon_k}
$$
要注意的是，我们是通过统计学方式推导出上述式子的，因此其并不是一个力学规律

另外，假如我们记单位体积中所包含的分子数目为 $n=\frac NV$,为了计算物质的量，我们还要除以阿伏伽德罗常数 $N_A$ ，因此我们得到
$$
p=nkT
$$
式中的 $k$ 为玻尔兹曼常数

联立两式可以得到
$$
\bar{\epsilon_k}=\frac32kT
$$
因此反过来，我们可以通过温度来计算气体分子的平均速率
$$
v_{rms}=\sqrt{\bar{v^2}}=\sqrt{\frac{3kT}{m_0}}=\sqrt{\frac{3RT}{M}}
$$
此外我们给出自由度的概念，自由度指的是分子可能进行的运动，假如气体仅由单原子构成，忽略转动，那么其运动的方向，总的来讲都可以拆分到三个轴向方向上，因此其自由度为3，而双原子分子的自由度为5，三原子以上的自由度为6，我们认为一个自由度会赋给这些理性气体分子每个 $\frac12kT$ 的平均动能，假设理想气体分子的自由度为 $i$ ，分子个数为 $N$ ，那么该系统的内能即为
$$
E_0=N(\frac i2kT)
$$
特别的，如果 $N=N_A$ ,那么
$$
E_0=N_A(\frac i2kT)=\frac i2RT
$$
 接着是热力学，首先是热力学第零定律：

**如果两个物体都与确定状态的第三物体处于热平衡，则该两个物体彼此处于热平衡**

我们记气体在膨胀时，通过推挤活塞对外界做的功的大小为 $dA$ （这是一小段位移内作的功）
$$
dA=Fdl=F\frac{dV}{s}=pdV
$$
由此我们引出热力学第一定律：

假设在一个系统中，初始平衡状态的内能为 $E_1$ ,终末平衡状态系统的内能为 $E_2$ ，假设该过程中系统还对外做功（或者外界对其做功）了 $A$ ，那么根据能量守恒定律，系统吸收（或者放出）的热量大小为
$$
Q=E_2-E_1+A
$$
其中系统的内能可根据上面的自由度理论计算得出

而假如气体在这个过程中发生了体积变化，那么联立上面两式，我们得到
$$
Q=E_2-E_1+\int^{V_2}_{V_1}pdV
$$
而压强与体积的关系可以从理想气体方程中得到，是一反比关系

借此我们可以推导出气体在进行等体过程和等压过程中发生的热量变化

**等体过程**中，体积未发生变化，因此气体从外界吸收（或放出）的热量即为其内能变化
$$
Q_V=E_2-E_1
$$
如果将其表征为与温度的关系（也就是每升高1k，系统放出了（或吸收）多少能量），那么我们首先将内能表征为与温度有关的形式
$$
E_0=N_A(\frac i2kT)=\frac i2RT
$$
换言之，每摩尔气体分子的内能变化为
$$
\Delta E=\frac i2R\Delta T
$$
因此，其比值为
$$
\frac i2R
$$
定义为摩尔定容热容（$C_{V,m}$）

接下来是**等压过程**，设初始压强为 $p$ ，同样以温度 $T$ 为自变量，可以得到
$$
dA=pdV=nRdT
$$
因此系统变化的热量为
$$
dQ_p=dE+nRdT
$$
而 $A=\int^{V_2}_{V_1}pdV=p(V_2-V_1)$

将体积用理想气体定律中的温度代替，因此有
$$
Q_p=E_2-E_1+nR(T_2-T_1)
$$
因此所谓的摩尔定压热容为
$$
C_{p,m}=\frac{i+2}2R
$$

定义比热容比为
$$
\gamma=\frac{C_p}{C_V}=\frac{i+2}{i}
$$
![image-20210629111021041](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629111021041.png)

此外，还有**等温过程**，该过程中气体分子的内能不变，仅做功，即
$$
Q_T=A
$$
而等温过程中，有 $p_1V_1=p_2V_2$ （即该过程中存在一个常量，我们可以通过将初始状态（或者已知的某状态）得到的常数除以变量 $V$ 来得到压强），因此
$$
A=\int^{V_2}_{V_1}pdV=\int^{V_2}_{V_1}\frac{p_1V_1}{V}dV=p_1V_1ln\frac{V_2}{V_1}
$$
**从上面的计算中我们也能总结出一些规律，即理想气体的内能大小仅仅取决于其温度大小，假如系统前后温度不变，那么单位摩尔浓度（分子的量/单位体积，等等）理想气体所包含的内能大小是不变的（这个不变并不是指的是系统在整个过程中没有发生任何变化，整个过程中可能气体吸热增加内能然后将内能放出用于做功，但这两者数量上相等）。而气体所作的功的大小则直接相关于体积，假如体积有变化，那么气体一定做功。**

绝热过程：该过程同样有功能变化，但不同的是，内能变化即为做功量

其相互关系式为

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629112619312.png" alt="image-20210629112619312" style="zoom:67%;" />

解题时，首先写出容器内部体积如何变化（变or不变），压强变化，以及能量的变化（各个参数是如何改变的），接着判断系统是否与外界发生了能量交换（借由体积是否改变和容器是否绝热来判断）

![image-20210629113518643](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629113518643.png)

![image-20210629113528315](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629113528315.png)

![image-20210629113543367](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629113543367.png)

![image-20210629114103824](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629114103824.png)

![image-20210629114127184](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629114127184.png)

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629114148997.png" alt="image-20210629114148997" style="zoom:80%;" />

![image-20210629114239402](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629114239402.png)

借由上面的几个过程，我们可以借此将内能转化为机械能，这就是循环

简单地说，循环就是**气体吸热→内能增加→压强上升→对外做功→内能下降（气体放热）→吸收能量（气体吸热）**这一过程，但我们有许多方法可以让气体的内能增加，是采用等体，等温还是绝热，等压，这都会带来不同的吸热效率

**卡诺循环**是在两个**温度恒定**的热源（一个高温热源，一个低温热源）之间工作的循环过程，在整个循环中，工作物**只和**高温热源或低温热源**交换能量**，没有散热漏气等因素存在.现在，我们来研究由平衡过程组成的卡诺循环因为是平衡过程，所以在工作物与温度为$T_1$的高温热源接触的过程中，基本上没有温度差，亦即工作物与高温热源接触而吸热的过程是一个温度为$T_1$的**等温膨胀**过程。同样，与温度为$T_2$的低温热源接触而放热的过程是一个温度为$T_2$的等温压缩过程，因为工作物**只与两个热源交换能量**，所以，当工作物脱离两热源时所进行的过程，必然是绝热的平衡过程。因此，卡诺循环是由**两个平衡的等温过程和两个平衡的绝热过程组成的.**。

![image-20210629134614180](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629134614180.png)

如图44-5所示，假设有一个盛有气体的汽缸，汽缸上带有一个无摩擦的活塞。气体不一定必须是理想气体，甚至液体也不一定必须能汽化，但是为了确定起见，我们认为这是一种理想气体。假设我们还有两个很大的热垫T1和T2（具有确定温度T1和T2的很大的东西）。假定现在的情况是T1高于T2。我们先加热气体同时让它膨胀，这时它与热垫T1接触。在这样做的时候，一旦**热量流入气体**，活塞就非常**缓慢地被顶出**，我们确信气体的温度永远不会远离T。假定活塞被**顶得太快**，气体的温度就会比T1低许多，于是过程就**不完全是可逆的**，但若活塞被顶得**足够慢**，气体的温度就**永远不会远离T1。**

![image-20210629134325411](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629134325411.png)

如果我们缓慢地把活塞推回来，气体温度只比T1高一个无限小量，热量将传回给热垫。我们看到，这样一种进行得足够缓慢的等温（温度不变）膨胀是可逆过程

因此上图中的图线（1）和（3）告诉了我们在等温情况下压强与体积之间的变化，具体来说，其遵循理想气体定律
$$
pV=NkT_!
$$
完成了等温膨胀而停止在b点后，我们将汽缸从热库拿开，并让它继续膨胀。这时我们**不让任何热量进入**汽缸，同时仍让气体缓慢地膨胀，再假设没有任何摩擦力，因此没有任何理由说这个过程不可逆。气体继续膨胀时，因为再没有任何热量进入汽缸，所以气体温度将下降。因而这是一次绝热膨胀，遵循
$$
PV^{\gamma}=C
$$
当期温度下降到T2时，因而如果我们把它放在温度为T2的热垫上，将**不会出现不可逆的变化**。现在在气体与温度为T2的热库接触的情况下，沿着记为（3）的曲线缓慢地**压缩气体**（图44-5，第二步）。

因为汽缸与热库接触，它的温度不会升高，但是**热量$Q_2$要在温度为$T_2$时从汽缸流入热库**。在沿曲线（3）等温地压缩气体至d点后，我们把汽缸从温度为$T_2$的热垫上拿开，并继续压缩气体，同时不让任何热量流出。于是气体的温度将上升，压强将沿记为（4）的曲线变化。

如果妥善地实现每一步骤，我们可以回到温度为Tl的起点a处，并且重复这一个循环。在图44-6上可以看到，我们已经使气体作一个完整的循环，在这一循环中，我们**在温度T1处加进了热量$Q_1$，而在温度$T_2$处取走了热量$Q_2$**。现在，要点在于这个循环是**可逆**的，因而我们能够把所有的步骤用另外反过来的方式表示。我们可以反向循环而不是正向循环：让气体从温度为$T_1$的a点出发，沿曲线（4）膨胀，膨胀到温度$T_2$后再吸收热量$Q_2$，等等，使循环反向进行。**如果我们沿这个方向作一个循环，我们必须对气体做功；而如果我们沿相反的方向循环，气体必定对我们做功。**

对于理想气体来说**，每个分子具有一个只取决于温度的能量**，而且因为a点和b点的温度和分子数相同，内能也就相同。气体在膨胀过程中所做的总功

![image-20210629140558715](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629140558715.png)

等于由热库取出的能量$Q_1$。在膨胀过程中，$pV=NT_1$，或

![image-20210629140614352](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629140614352.png)

于是

![image-20210629140710017](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629140710017.png)

即

![image-20210629140731392](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629140731392.png)

这就是从T1热库取得的热量。同样，对于在T2温度下的压缩来说[图44-6曲线（3）]，释放给T2热库的热量是

![image-20210629140746849](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629140746849.png)

不难得到

![image-20210629142101338](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629142101338.png)

而

![image-20210629142123501](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629142123501.png)

因此

![image-20210629142138059](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629142138059.png)

这个公式指出了热机的效率——从那么多的热量中得到了多少功。热机的效率等于热机在其中工作的两个温度之差除以较高的温度

![image-20210629142148408](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629142148408.png)

质量、温度或动能等物理量完全由指定其大小的单个实数决定。 这些称为标量，或简称为标量。 与此相反，称为向量或向量的其他实体同时具有大小和方向。 作为例子，我们提到了速度、力和位移。我们将对运动问题感兴趣，这要求我们使用矢量演算。 当向量和微积分被允许相互作用时，结果是一门强大而高效的数学学科，用于研究几何和物理的多维问题。 这种向量微积分——通常称为向量分析——是微积分高级课程的主要课题之一。 在本章中，我们只能介绍该主题并讨论一些经典应用，最终处理开普勒行星运动定律和牛顿万有引力定律

假如我们对位矢有关时间求导，那么我们得到

![image-20210629144653711](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629144653711.png)

几个熟悉的微分规则现在可以扩展到向量函数。其中最重要的一个是：如果一个向量函数乘以一个标量函数，并且如果两者都可以微分，那么它们的乘积可以根据链式法则来进行微分

![image-20210629144751666](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629144751666.png)

下图展示了上式的几何意义（平面上的）

![image-20210629144841887](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629144841887.png)

模长则是

![image-20210629144934966](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629144934966.png)

该标量被定义为速率，请注意其与速度之间的区别——速率没有方向

![image-20210629145014880](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145014880.png)

正如我们移动点的速度 v 是其位置的变化率，加速度 a 是其速度的变化率，

![image-20210629145045773](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145045773.png)

因此，我们目前的速度和加速度概念是我们早期对一维运动研究的这些概念的更有限版本的直接扩展。如果移动点 P 是移动物理对象的位置，因此可以认为是质量为 m 的粒子在外加力 F 的作用下移动，则牛顿第二运动定律指出

![image-20210629145152287](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145152287.png)

现在很明显，时间 t 是研究点 P 沿曲线路径运动的基本重要参数。 另一个重要参数是弧长 s，沿曲线从固定点 Po 到 P 测量，如图 17.40 所示。 我们现在将 R 视为 s 的函数并检查导数 $dR/ds$ 的含义。 如果当 s 变为 $s + \Delta s$ 时 P 沿着曲线移动到 Q，则

![image-20210629145325122](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145325122.png)

![image-20210629145334819](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145334819.png)

取微分，我们定义向量 $T$ 为指向运动方向的单位向量

![image-20210629145527928](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145527928.png)

作为我们在第 17 .6 节中推导出的一般加速度公式的第一步，我们现在必须分析 T 对 s 的导数，这要求我们检查曲线“曲率”的纯几何概念。如果我们参考我们对曲率概念的直觉感受，我们大多数人都会同意直线根本不弯曲； 也就是说，它的曲率为零。此外，圆在每个点的曲率都相同，小圆的曲率大于大圆的曲率，如图 1 7.42 所示。 在像右边这样的不均匀曲线的情况下，曲线相对直的地方曲率应该更小，曲线弯曲得更陡峭的地方曲率应该更大。

这些观点基于这样一种观点，即一点的曲率应该测量曲线的方向相对于沿曲线的距离在该点变化的速度。 由于方向由从 x 轴到切线的角度 <f> 指定（图 17.41），我们将此角度视为弧长 s 的函数，并将曲率 k 定义为 $\varphi$ ,关于 s 的变化快慢，

![image-20210629145902834](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629145902834.png)

考虑一个移动的粒子，它在时间 t 的位置由参数方程 x = x(t) 和 y = y(t) 给出。 该粒子的位置向量为 $R = x\vec{i} + y\vec{j}$，其速度和加速度为

![image-20210629150256615](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629150256615.png)

不幸的是，这些向量的 i 和 j 分量没有物理意义，因为它们依赖于坐标系，坐标系的选择是任意的； 它不是由运动本身的内在性质决定的。 然而，我们在 17.4 中看到，速度也可以写成

![image-20210629150448332](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629150448332.png)

或者

![image-20210629150529766](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629150529766.png)

为了获得类似的加速度表达式，我们对上式对 t 进行微分，

![image-20210629150826369](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629150826369.png)

![image-20210629151023764](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629151023764.png)

![image-20210629151728228](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629151728228.png)

![image-20210629152149280](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629152149280.png)

二维空间中的转动

质心定理：存在一个在数学上可以定义的平均位置，使其运动轨迹可以被表示为该点的运动轨迹

证明，每个粒子都由大量的粒子构成，对于每一个粒子，作用在其上的力可以表示成
$$
\vec{F_i}=\frac{m_id^2\vec{r_i}}{dt^2}
$$
加入我们忽略相对论效应，可以认为每个粒子的质量都是常量，那么
$$
\vec{F_i}=\frac{d^2m_i\vec{r_i}}{dt^2}
$$
根据牛顿第三定律，当我们把这些力加起来时，我们可以得到作用在这个物体上的力，换言之
$$
F=\Sigma F_i=\Sigma\frac{d^2m_i\vec{r_i}}{dt^2}
$$
设 $M$ 为物体的总质量，并令 $\vec{R}=\Sigma\frac{m_i\vec{r_i}}{M}$ ，则
$$
F=\frac{d^2(MR)}{dt^2}=\frac{Md^2R}{dt^2}
$$
这就是说物体所受的合外力等于物体的总质量与其上某一点处的加速度的积分，换言之，该点即为质心

研究曲线运动时，我们可以类比与在直线运动（一维质点系）中的加速度，线速度等参数，以角速度和角加速度来刻画曲线运动的物体，对于一个正在转动的圆盘而言，其上某一点的线速度为
$$
v=\omega R=\frac{d\theta}{dt}R
$$
因此其加速度为
$$
a=\frac{d\omega}{dt}R=\frac{d^2\theta}{dt^2}R
$$
我们知道，进行直线运动的物体存在动能，那么转动的物体是否也有动能？我们在这个转动的圆盘上取一小块区域，质量为 $m_i$ ，对于这块区域而言，其动能为
$$
E_k=\frac12mv^2=\frac12m_i\omega^2R_i^2
$$
因此整个圆盘的动能为其累加之和
$$
\frac12{\omega^2}\Sigma m_iR_i^2
$$
假如我们令 $\Sigma m_iR_i^2=I$ ，就有
$$
E_k=\frac12I\omega^2
$$
因此我们看到这个 $I$ 对应了一维运动中的参数质量，被命名为转动惯量

事实上计算转动惯量的问题是一个二重/三重积分问题，当 $i\rightarrow\infin$ 时，该式子等于
$$
\int\int_{D}=\rho
$$
不过我们在这里还是列出了一些常见刚体的转动惯量

**细圆环 薄圆柱环**
　　 细圆环和薄圆柱环的所有质量与转轴的距离都为 ![[公式]](https://www.zhihu.com/equation?tex=R)，可以看成许多质点的叠加，每个质点转惯量为 ![[公式]](https://www.zhihu.com/equation?tex=m_i+R%5E2)，所以

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Csum_i+m_i+R%5E2+%3D+M+R%5E2%5Cqquad+%281%29)

**细棒（端点轴）**
　　 细棒的线密度为 ![[公式]](https://www.zhihu.com/equation?tex=%5Clambda++%3D+M%2FL)，如果划分成长度为 ![[公式]](https://www.zhihu.com/equation?tex=%5CDelta+r) 的小段，第 ![[公式]](https://www.zhihu.com/equation?tex=i) 段距离转轴 ![[公式]](https://www.zhihu.com/equation?tex=r_i)，有

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Clim_%7B%5CDelta+r+%5Cto+0%7D%5Csum_i+%5Clambda%5CDelta+r+%5Ccdot+r_i%5E2+%3D++%5Cint_0%5EL+%5Clambda+r%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D++%3D+%5Cfrac%7B1%7D%7B3%7D%5Clambda+L%5E3+%3D+%5Cfrac%7B1%7D%7B3%7DM+L%5E2%5Cqquad+%282%29)

**细棒（中心轴）**
　　 细棒（中心轴）可以看做两个等质量的细棒（端点轴），质量都为 ![[公式]](https://www.zhihu.com/equation?tex=M_1)，每个具有转动惯量（[式 2 ](https://link.zhihu.com/?target=https%3A//wuli.wiki/changed/ExMI.html%23eq2)）![[公式]](https://www.zhihu.com/equation?tex=M_1+R%5E2%2F3)，乘以二得总转动惯量为

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cfrac%7B1%7D%7B3%7D+MR%5E2+%3D+%5Cfrac%7B1%7D%7B12%7DML%5E2%5Cqquad+%283%29)

**薄长方体（共面轴）**
　　 薄长方体（共面轴）可以看成许多细棒（中心轴）组成，所以转动惯量的系数仍然为

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cfrac%7B1%7D%7B3%7D+MR%5E2+%3D+%5Cfrac%7B1%7D%7B12%7DML%5E2%5Cqquad+%284%29)

**薄圆盘 圆柱**
　　 薄圆盘可以看做许多宽度为 ![[公式]](https://www.zhihu.com/equation?tex=%5CDelta+r) 的细圆环组成**[1](https://link.zhihu.com/?target=https%3A//wuli.wiki/changed/ExMI.html%23note1)**，质量面密度为 ![[公式]](https://www.zhihu.com/equation?tex=%5Csigma++%3D+M%2F%28%5Cpi+R%5E2%29)，第 ![[公式]](https://www.zhihu.com/equation?tex=i) 个圆环的半径为 ![[公式]](https://www.zhihu.com/equation?tex=r_i)，面积为 ![[公式]](https://www.zhihu.com/equation?tex=2%5Cpi+r_i+%5CDelta+%7Br%7D)，总转动惯量为

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cint_0%5ER+r%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Bm%7D+++%3D+%5Cint_0%5ER+%5Csigma++%5Ccdot+2%5Cpi+r++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D+++%5C%2C%5Cmathrm%7Bd%7D%7Br%5E2%7D+++%3D+2%5Cpi+%5Csigma+%5Cint_0%5ER+r%5E3++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D%5Cqquad+%285%29)

也可以在极坐标极坐标中直接根据定义写出积分
![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cint+%7Br%5E2%7D%5Csigma++%5C%2C%5Cmathrm%7Bd%7D%7Bs%7D+++%3D+%5Cint_0%5E%7B2%5Cpi+%7D+%5Cint_0%5ER+%5Csigma+r%5E2+%5Ccdot+r++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+++%3D+2%5Cpi+%5Csigma+%5Cint_0%5ER+r%5E3++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D+++%3D+%5Cfrac12%5Csigma+%5Cpi+R%5E2+R%5E2+%3D+%5Cfrac12+M+R%5E2%5Cqquad+%286%29)

圆柱可看做由许多相同的薄圆盘组成，转动惯量系数相同．

**薄球壳**
　　 球壳可以看做由许多细圆环组成，质量面密度为 ![[公式]](https://www.zhihu.com/equation?tex=%5Csigma++%3D+M%2F%284%5Cpi+R%5E2%29)，球坐标中，令第 ![[公式]](https://www.zhihu.com/equation?tex=i) 个圆环对应的极角为 ![[公式]](https://www.zhihu.com/equation?tex=%5Ctheta)，宽度为 ![[公式]](https://www.zhihu.com/equation?tex=R++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D)，面积为 ![[公式]](https://www.zhihu.com/equation?tex=%5C%2C%5Cmathrm%7Bd%7D%7Bs_i%7D++%3D+2%5Cpi+R%5Csin%5Ctheta+%5Ccdot+R++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D)，半径为 ![[公式]](https://www.zhihu.com/equation?tex=r_%7B%5Cbot%7D+%3D+R%5Csin%5Ctheta)，总转动惯量为

![[公式]](https://www.zhihu.com/equation?tex=%5Cbegin%7Baligned%7D+I+%26%3D+%5Cint_0%5E%5Cpi+r_%5Cbot%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Bm%7D+++%3D+%5Cint+R%5E2+%5Csin%5E2+%5Ctheta+%5Ccdot+%5Csigma++%5Ccdot+2%5Cpi+R%5Csin%5Ctheta+%5Ccdot+R++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D++%5C%5C+%26%3D+2%5Cpi+%5Csigma+R%5E4+%5Cint+%5Csin%5E3+%5Ctheta_i++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+++%3D+2%5Cpi+%5Csigma+R%5E4+%5Cint_0%5E%5Cpi+%5Csin%5E3+%5Ctheta++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+%5Cend%7Baligned%7D%5Cqquad+%287%29)

也可以在球坐标中直接写出球面积分
![[公式]](https://www.zhihu.com/equation?tex=%5Cbegin%7Baligned%7D+I+%26%3D+%5Cint+r%5E2+%5Csigma++%5C%2C%5Cmathrm%7Bd%7D%7Bs%7D+++%3D+%5Cint_0%5E%7B2%5Cpi%7D+%5Cint_0%5E%5Cpi++%28R%5Csin+%5Ctheta%29%5E2+%5Csigma+R%5E2%5Csin+%5Ctheta++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+++%5C%2C%5Cmathrm%7Bd%7D%7B%5Cphi%7D++++%3D+2%5Cpi+%5Csigma+R%5E4+%5Cint_0%5E%5Cpi++%5Csin%5E3+%5Ctheta++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+%5C%5C+%26%3D+2%5Cpi+%5Csigma+R%5E4%5Cint_%7B-1%7D%5E1+%281+-+%5Ccos%5E2+%5Ctheta+%29++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ccos+%5Ctheta%7D+++%3D+%5Cfrac23+%28%5Csigma+4%5Cpi+R%5E2%29+R%5E2+%3D+%5Cfrac23+M+R%5E2+%5Cend%7Baligned%7D%5Cqquad+%288%29)

其中对 ![[公式]](https://www.zhihu.com/equation?tex=%5Ctheta) 的积分使用了换元积分法


**球体**
　　 球体可以看做由许多薄球壳组成，体密度为 ![[公式]](https://www.zhihu.com/equation?tex=%5Crho++%3D+M%2F%284%5Cpi+R%5E3%2F3%29)，令第 ![[公式]](https://www.zhihu.com/equation?tex=i) 个球壳半径为 ![[公式]](https://www.zhihu.com/equation?tex=r)，厚度为 ![[公式]](https://www.zhihu.com/equation?tex=%5C%2C%5Cmathrm%7Bd%7D%7Br%7D)，体积为 ![[公式]](https://www.zhihu.com/equation?tex=4%5Cpi+r%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D)，总转动惯量为

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cint_0%5ER+%5Cfrac23+r%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Bm%7D+++%3D+%5Cfrac23+%5Crho+%5Cint_0%5ER+r%5E2++%5C%2C%5Cmathrm%7Bd%7D%7BV%7D+++%3D+%5Cfrac%7B2M%7D%7BR%5E3%7D+%5Cint_0%5ER+r%5E4++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D++%3D+%5Cfrac%7B2%7D%7B5%7D+M+R%5E2%5Cqquad+%289%29)

也可以在球坐标中直接体积分
![[公式]](https://www.zhihu.com/equation?tex=%5Cbegin%7Baligned%7D+I+%26%3D+%5Cint+%28r%5Csin+%5Ctheta+%29%5E2++%5C%2C%5Cmathrm%7Bd%7D%7Bm%7D+++%3D+%5Cint_0%5E%7B2%5Cpi+%7D+%5Cint_0%5E%5Cpi++%5Cint_0%5ER+%28r%5Csin+%5Ctheta+%29%5E2%5Csigma+r%5E2+%5Csin+%5Ctheta++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D++%5C%2C%5Cmathrm%7Bd%7D%7B%5Cphi%7D+%5C%5C+%26%3D+%5Cfrac%7B3M%7D%7B2R%5E3%7D%5Cint_0%5E%5Cpi++%5Csin%5E3%5Ctheta+++%5C%2C%5Cmathrm%7Bd%7D%7B%5Ctheta%7D+++%5Cint_0%5ER+r%5E4++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D+++%3D%5Cfrac%7B2M%7D%7BR%5E3%7D%5Cint_0%5ER+r%5E4++%5C%2C%5Cmathrm%7Bd%7D%7Br%7D++%3D+%5Cfrac%7B2%7D%7B5%7D+M+R%5E2+%5Cend%7Baligned%7D%5Cqquad+%2810%29)

其中对 ![[公式]](https://www.zhihu.com/equation?tex=%5Ctheta) 的积分使用了换元积分法．


**薄长方体（垂直轴）**
　　 由 “薄长方体（共面轴）” 可知两个共面方向的转动惯量分别为（[式 4 ](https://link.zhihu.com/?target=https%3A//wuli.wiki/changed/ExMI.html%23eq4)）![[公式]](https://www.zhihu.com/equation?tex=MR_1%5E2%2F3) 和 ![[公式]](https://www.zhihu.com/equation?tex=MR_2%5E2%2F3)，使用垂直轴定理[式 3 ](https://link.zhihu.com/?target=https%3A//wuli.wiki/changed/MIthm.html%23eq3)可得关于垂直轴的转动惯量为二者之和

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cfrac13+M%28R_1%5E2+%2B+R_2%5E2%29+%3D+%5Cfrac%7B1%7D%7B12%7D+M%28L_1%5E2+%2B+L_2%5E2%29%5Cqquad+%2811%29)

其中 ![[公式]](https://www.zhihu.com/equation?tex=L_1+%3D+2R_1)，![[公式]](https://www.zhihu.com/equation?tex=L_2+%3D+2R_2) 分别是两条边长．

**长方体**
　　 另外由于长方体可以看作许多薄片延轴方向叠加，其转动惯量公式也相同

![[公式]](https://www.zhihu.com/equation?tex=I+%3D+%5Cfrac13+M%28R_1%5E2+%2B+R_2%5E2%29+%3D+%5Cfrac%7B1%7D%7B12%7D+M%28L_1%5E2+%2B+L_2%5E2%29%5Cqquad+%2812%29)

其中 ![[公式]](https://www.zhihu.com/equation?tex=L_1+%3D+2R_1)，![[公式]](https://www.zhihu.com/equation?tex=L_2+%3D+2R_2) 分别是长方体垂直于转轴的两条边长．

不难从上面的式子中看出，对于同一个物体，其转动惯量并不是恒定的，其大小取决于转轴的位置，对于这种问题，有

**平行轴定理**

假设存在一个**质量分布均匀**的转动圆盘

<img src="C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629162150749.png" alt="image-20210629162150749" style="zoom:67%;" />



原先其转轴穿过其质心 $o$ ，现在我们更换一根性的转轴 $l'$ ，并设两根转轴之间的距离为 $d$ ，那么有
$$
I_{l'}=I_l+md^2
$$
**垂直轴定理**

![image-20210629162916619](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629162916619.png)



该定理的应用对象是十分薄的，可以被视作是平面的物体，有
$$
I_z=I_x+I_y
$$
我们可以通过相同的方法求出角动量

我们在旋转的刚体上取一点 $Q$ ，并取 $Q$ 到该刚体的质心的矢径 $\vec{R}$ ，设其设其质心的动量大小为 $\vec{P}=m\vec{v}$

我们定义质心相对于点 $Q$ 的角动量 $\vec{L_Q}$ 为
$$
\vec{L_Q}=\vec{r_Q}\times\vec{p}![image-20210629184117620]
$$
根据外积 的定义，我们可以得到外积的模长大小为
$$
|\vec{L_Q}|=mvr_qsin\theta
$$
![image-20210629184722468](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210629184722468.png)

而如果我们改换参考点 $Q$ 的位置，那么其对应的角动量大小也会发生改变，具体而言，假如我们取一个在动量所在直线延长线上的参考点，那么该刚体相对于此点的角动量大小即为0

现在我们对角动量的大小求导
$$
\frac{d\vec{L}}{dt}=\frac{d\vec{r_Q}}{dt}\times\vec{p}+\vec{r_Q}\frac{d\vec{p}}{dt}
$$
从而
$$
\frac{d\vec{L}}{dt}=\vec{r_Q}\times\vec{F}
$$
我们称职这个量为“力矩”以用来对应力这一概念

 角动量守恒可以与动量守恒一起应用

![image-20210630155903360](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210630155903360.png)

第一阶段我们通过能量守恒计算出了下落时细棒的角速度大小，借此我们可以计算出角动量大小

而碰撞前后外力矩为0，应用动量守恒，有

![image-20210630160103617](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20210630160103617.png)

































































































​                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             

