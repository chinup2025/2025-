## 行列式 （determinant）
### 1. 定义 （3 个）
#### 1. 第一定义 （本质定义）
##### 引入
###### 1. ==二阶行列式 ：以这两个向量为邻边的平行四边形的面积==

![[Pasted image 20240510165502.png]]
  **2 阶行列式是由两个 2 维向量组成的，其（运算规则的）结果为以这两个向量为邻边的平行四边形的面积．**
  $$
\begin{aligned}
S_{\square O A B C} & =l \cdot m \cdot \sin (\beta-\alpha) \\
& =l \cdot m(\sin \beta \cos \alpha-\cos \beta \sin \alpha) \\
& =l \cos \alpha \cdot m \sin \beta-l \sin \alpha \cdot m \cos \beta \\
& =a_{11} a_{22}-a_{12} a_{21}, \\
\left|\begin{array}{ll}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{array}\right| & =a_{11} a_{22}-a_{12} a_{21}=S_{\square O A B C} .
\end{aligned}
$$
###### 2. ==三阶行列式 ：以这两个向量为邻边的平行六面体的体积==
 ![[Pasted image 20240510165753.png]]
此处可以联想 [[高等数学#曲面曲线积分]]中三个向量共面，其组成的 3* 3行列式等于 0
#####  ==第一定义 : **$n$ 个向量为邻边的 $n$ 维图形的体积====
$n(n \geqslant 3)$ 阶行列式是由 $n$ 个 $n$ 维向量 $\alpha_1=\left[a_{11}, a_{12}, \cdots, a_{1 n}\right], a_2=\left[a_{21}, a_{22}, \cdots, a_{2 n}\right], \cdots, \alpha_n=$ $\left[a_{n 1}, a_{n 2}, \cdots, a_{n n}\right]$ 组成的, 其 (运算规则的) 结果为以这 **$n$ 个向量为邻边的 $n$ 维图形的体积**.
 $$
D_{n} = \begin{vmatrix}
a_{11} & \dots & a_{1n} \\
\vdots & &\vdots \\
a_{n1} & \dots & a_{nn}
\end{vmatrix}
$$

#### 2. 逆序数法定义（第二种定义）

n 阶行列式 
$$
\begin{vmatrix}
a_{11}&a_{12}&\dots &a_{1n} \\
 a_{21}&a_{22}&\dots &a_{2n} \\ 
\vdots & \vdots & &\vdots \\
a_{n1}&a_{n2}&\dots &a_{nn}
\end{vmatrix} = \sum _{j_{1}j_{2}\dots j_{n}}(-1)^{\tau (j_{1}j_{2}\dots j_{n})}a_{1j_{1}}a_{2j_{1}}\dots a_{nj_{1}}
$$
其中 $\tau (j_{1}j_{2}\dots j_{n})$ 是**逆序数**，即从左到右依次取定第一个数，其后面的数比之小的个数之和
**注意**：计算行列式的逆序数时，前提是第一个下标从 1 到 n 顺序增大

#### 3. 余子式 （第三种定义）
$$
M_{i j}=\left|\begin{array}{cccccc}
a_{11} & \cdots & a_{1, j-1} & a_{1, j+1} & \cdots & a_{1 n} \\
\vdots & & \vdots & \vdots & & \vdots \\
a_{i-1,1} & \cdots & a_{i-1, j-1} & a_{i-1, j+1} & \cdots & a_{i-1, n} \\
a_{i+1,1} & \cdots & a_{i+1, j-1} & a_{i+1, j+1} & \cdots & a_{i+1, n} \\
\vdots & & \vdots & \vdots & & \vdots \\
a_{n 1} & \cdots & a_{n, j-1} & a_{n, j+1} & \cdots & a_{n n}
\end{array}\right| .
$$
行列式 = $\Sigma_{行或列}$ 某行某列元素 *  其所在行所在列的代数余子式
定义 $M_{ij}$ 为 $a_{ij}$ 的余子式
$A_{ij}$ 为 $a_{ij}$ 的代数余子式
$$A_{ij} = (-1)^{(i+j)}M_{ij}$$ 
##### **按行按列展开**
行列式等于行列式的**某行（列）元素分别乘其相应的代数余子式后再求和**，即
$$
|A|=\left\{\begin{array}{l}
a_{i 1} A_{i 1}+a_{i 2} A_{i 2}+\cdots+a_{i n} A_{i n}=\sum_{j=1}^n a_{i j} A_{i j}(i=1,2, \cdots, n), \\
a_{1 j} A_{1 j}+a_{2 j} A_{2 j}+\cdots+a_{n j} A_{w j}=\sum_{i=1}^n a_{i j} A_{i j}(j=1,2, \cdots, n) .
\end{array}\right.
$$

### 2. 性质 （7 个）
#### 性质 1:  行列互换，其值不变，即 $|\boldsymbol{A}|=\left|\boldsymbol{A}^{\mathrm{T}}\right|$

**表示==行列式中，行列地位等价**==

#### 性质 2:  若行列式中某行（列）元素全为零，则行列式为零 [[#**按行按列展开**]]

#### 性质 3 ：若行列式中某行 (外) 元素有公因子 $k(k \neq 0)$, 则 $k$ 可提到行列式外面, 即
$$
\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
\vdots & \vdots & & \vdots \\
k a_{i 1} & k a_{i 2} & \cdots & k a_{i n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right|=k\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
\vdots & \vdots & & \vdots \\
a_{i 1} & a_{i 2} & \cdots & a_{i n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right| .
$$

**注意：** 此处与[[矩阵性质]]不同 
$$
|c \boldsymbol{A}|=c^n|\boldsymbol{A}|
$$

#### 性质 4：行列式中某行（列）元素均是两个数之和，则可拆成两个行列式之和
$$
\left|\boldsymbol{\alpha}, \boldsymbol{\beta}_1+\boldsymbol{\beta}_2, \boldsymbol{\gamma}\right|=\left|\boldsymbol{\alpha}, \boldsymbol{\beta}_1, \boldsymbol{\gamma}\right|+\left|\boldsymbol{\alpha}, \boldsymbol{\beta}_2, \boldsymbol{\gamma}\right| 
$$
即 
$$
\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
\vdots & \vdots & & \vdots \\
a_{i 1}+b_{i 1} & a_{i 2}+b_{i 2} & \cdots & a_{i n}+b_{i n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right|=\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
\vdots & \vdots & & \vdots \\
a_{i 1} & a_{i 2} & \cdots & a_{i n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right|+\left|\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 n} \\
\vdots & \vdots & & \vdots \\
b_{i 1} & b_{i 2} & \cdots & b_{i n} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n n}
\end{array}\right| .
$$
#### 性质 5：行列式中两行（列）互换，行列式变号
#### 性质 6：行列式中的两行（列）元素相等或对应成比例，则行列式为 0
#### 性质 7：行列式中某行（列） 的 K 倍加到另一行（列），行列式不变
### 3. 重要行列式
#### 1. 上下三角行列式 (主对角线元素之积)

$\left|\begin{array}{cccc}a_{11} & a_{12} & \cdots & a_{1 n} \\ 0 & a_{22} & \cdots & a_{2 n} \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \cdots & a_{n n}\end{array}\right|=\left|\begin{array}{cccc}a_{11} & 0 & \cdots & 0 \\ a_{21} & a_{22} & \cdots & 0 \\ \vdots & \vdots & & \vdots \\ a_{n 1} & a_{n 2} & \cdots & a_{n n}\end{array}\right|=\left|\begin{array}{cccc}a_{11} & 0 & \cdots & 0 \\ 0 & a_{22} & \cdots & 0 \\ \vdots & \vdots & & \vdots \\ 0 & 0 & \cdots & a_{n n}\end{array}\right|=\prod_{i=1}^n a_{i i}$.
#### 2. 副对角线行列式 （$(-1)^{\sum^{n-1}_{i=1}i}$ 副对角线元素之积）
$\left|\begin{array}{cccc}a_{11} & \cdots & a_{1, n-1} & a_{1 n} \\ a_{21} & \cdots & a_{2, n-1} & 0 \\ \vdots & & \vdots & \vdots \\ a_{n 1} & \cdots & 0 & 0\end{array}\right|=\left|\begin{array}{cccc}0 & \cdots & 0 & a_{1 n} \\ 0 & \cdots & a_{2, n-1} & a_{2 n} \\ \vdots & & \vdots & \vdots \\ a_{n 1} & \cdots & a_{n, n-1} & a_{n n}\end{array}\right|=\left|\begin{array}{cccc}0 & \cdots & 0 & a_{1 n} \\ 0 & \cdots & a_{2, n-1} & 0 \\ \vdots & & \vdots & \vdots \\ a_{n 1} & \cdots & 0 & 0\end{array}\right|=(-1)^{\frac{n(n-1)}{2}} a_{1 n} a_{2, n-1} \cdots a_{n 1}$
**需要计算逆序数：** 

$\tau(n,(n-1), \cdots 1)={n-1+(n-2)}+\dots{+1}$

#### 3. 拉普拉斯展开式

设 $\boldsymbol{A}$ 为 $m$ 阶矩阵, $\boldsymbol{B}$ 为 $n$ 阶矩阵, 则
$$
\begin{gathered}
\left|\begin{array}{ll}
\boldsymbol{A} & \boldsymbol{O} \\
\boldsymbol{O} & \boldsymbol{B}
\end{array}\right|=\left|\begin{array}{ll}
\boldsymbol{A} & \boldsymbol{C} \\
\boldsymbol{O} & \boldsymbol{B}
\end{array}\right|=\left|\begin{array}{ll}
\boldsymbol{A} & \boldsymbol{O} \\
\boldsymbol{C} & \boldsymbol{B}
\end{array}\right|=|\boldsymbol{A}||\boldsymbol{B}|, \\
\left|\begin{array}{ll}
\boldsymbol{O} & \boldsymbol{A} \\
\boldsymbol{B} & \boldsymbol{O}
\end{array}\right|=\left|\begin{array}{ll}
\boldsymbol{C} & \boldsymbol{A} \\
\boldsymbol{B} & \boldsymbol{O}
\end{array}\right|=\left|\begin{array}{ll}
\boldsymbol{O} & \boldsymbol{A} \\
\boldsymbol{B} & \boldsymbol{C}
\end{array}\right|=(-1)^{m n}|\boldsymbol{A}||\boldsymbol{B}| .
\end{gathered}
$$
式 1，类似于主对角线行列式，上(下) 三角行列式
式 1，类似于副对角线行列式，$mn$ 代表副对角线换成主对角线的次数

#### 4. 范德蒙德行列式（记为 $V$）
$$ V_{n} = \left|\begin{array}{cccc}1 & 1 & \cdots & 1 \\ x_1 & x_2 & \cdots & x_n \\ x_1^2 & x_2^2 & \cdots & x_n^2 \\ \vdots & \vdots & & \vdots \\ x_1^{n-1} & x_2^{n-1} & \cdots & x_n^{n-1}\end{array}\right|=\prod_{1\leq i<j \leq n}\left(x_j-x_i\right)$$
 ##### **注意**
 $1$ 看成 $x^0$,  从 $x^0$ 到 $x^{n-1}$,  n * n 维矩阵
 第二行元素，大的-小的，遍历每一个元素，连乘之
 **Example：** 三阶范德蒙德行列式 
 $$
V_{3} = \begin{vmatrix}
1& 1&1 \\
x_{1} & x_{2} & x_{3} \\
x_{1}^2 & x_{2}^2 & x_{3}^2 
\end{vmatrix} = (x_{3}-x_{2})(x_{2}-x_{1})
$$
### 4. 计算
![[Pasted image 20240510180701.png]]
