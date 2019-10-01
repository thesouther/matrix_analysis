<style>
.samps{
    border-width:1px;
    border-style:solid;
    border-color:gray;  
}
</style>
## 矩阵代数
---
#### 基本定义

&emsp;$\mathcal{R}$代表实数集，$\mathcal{C}$代表复数集；$\mathcal{R}^n$代表n个实数组成的元组的集合,$\mathcal{C}^n$代表n个实数组成的元组的集合；$\mathcal{R}^{m\times n}$代表实数矩阵、$\mathcal{C}^{m\times n}$代表复数矩阵。
&emsp;矩阵$\mathbf{A}=[a_{ij}]$ 与矩阵$\mathbf{B}_{b_{ij}}$相等，定义为矩阵$\mathbf{A}$与$\mathbf{B}$形式相同，并且对应元素相等；即$a_{ij}=b_{ij},\forall i,j$。  
&emsp;只有一列的数组（矩阵），叫做列向量；只有一行的数组（矩阵）叫行向量。

#### 矩阵基本运算
1. 矩阵加法
   &emsp;假设矩阵$A$和$B$是$m\times n$矩阵，定义矩阵加法$A+B$的和仍然是$m\times n$矩阵，且等于矩阵$A$和$B$对应元素相加，即
   <!-- <center> -->
   $${\left[ A+B\right]}_{ij} = \left[A \right]_{ij} + \left[ B \right]_{ij}, \ for\ \ each \ \ i \ \ and \ \ j.$$

   &emsp;矩阵$(-A)$称为矩阵加法的逆运算，代表$A$中的每个元素都取相反数，即<font color='red'>||  </font>$if \ A =[a_{ij}], \ then \ \ (-A)=\left[ -a_{ij} \right]$<font color='red'> ||</font>，这就使用加法定义了减法。对于两个形式相同的矩阵，定义减法$A-B=A+(-B)$，所以
   $$
   \left[A-B \right]_{ij} = \left[A\right]_{ij} - \left[B \right]_{ij}, \forall i,j.
   $$
-  加法定理：
   <span><div class="samps">对于$m\times n$ 矩阵$A,B,C$，以下定理成立：
   1.闭合率：$A+B$仍然是$m\times n$矩阵
   2.结合律：$(A+B)+C = A+(B+C)$
   3.交换律：$A+B=B+A$
   4.$A+0=A$
   5.$A+(-A)=0$</div></span>

-  数乘：$[\alpha A]_{ij}=\alpha [A]_{ij}$，及其定理：
   <span><div class="samps">对于$m\times n$ 矩阵$A,B$，以及标量$\alpha,\beta$， 以下定理成立：
   1.闭合率：$\alpha A$仍然是$m\times n$矩阵
   2.结合律：$(\alpha \beta)A = \alpha (\beta A)$
   3.分配律：$\alpha(A+B)=\alpha A + \alpha B$
   4.分配律：$(\alpha + \beta)A=\alpha A + \beta A$
   5.$1A=A$</div></span>
-  其他定义：转置、共轭转置
   <span><div class="samps">
   1. $(A^T) ^T=A$
   2. A的共轭矩阵：$\bar{A}=\left[ \bar{a}_{ij}\right]$
      A的共轭转置：$\bar{A}^T = \bar{A^T}$，用$A^*$表示，$\left[A^*\right]_{ij}=\bar{a}_{ji}$
      $$
      \left(
      \begin{matrix}
        1-4i & i & 2 \\
        3 & 2+i & 0
      \end{matrix}
      \right)^*=
      \left(
          \begin{matrix}
              1+4i & 3 \\
              -i & 2-i \\
              2 & 0
          \end{matrix}
      \right)
      $$
      $(A^*)^*=A$， 当A为实数矩阵，$A^*=A^T$，有时$A^*$称为A的伴随矩阵
   3.运算律：
   $$(A+B)^T = A^T + B^T, \ \ \ and \ \ \ (A+B)^*=A^*+B^* \newline
   (\alpha A)^T=\alpha A^T, \ \ and \ \ \ (\alpha A)^*=\alpha A^*
   $$</div></span>
-  对于方阵：对称阵、对角阵、反对称矩阵、埃尔米特矩阵、反埃尔米特矩阵

2. 矩阵乘法
  - 线性
  - 
3. 

#### LU分解
当我们可以保证高斯消去法只有第三种情况时，使用矩阵的乘法代替行初等变换，只有下三角矩阵
LU分解：L下三角矩阵，U上三角矩阵

当矩阵中只出现第三种初等行变换，不会出现第二种初等行变换  
并不是所有的非奇异矩阵都存才LU分解，例子[\[0,1],[1,1]]  
2.为什么不能出现第二种初等行变换？
`如果出现两行交换位置，连乘积中一定存在某个矩阵不是下三角矩阵，那么L就不能是下三角矩阵`

##### 二，但是某些矩阵使用高斯消去法时必须要交换两行才可以，这种方程是有解的，能不能利用LU呢？
`可以，我们可以在得LU之前先把所有的行交换操作做完。`

##### <font color='red'>3. 作业</font>
程序实现LU分解.
Exercises,4(看看)，x取遍所有向量形式  
          11，12