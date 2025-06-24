# Introduction to Computer System Organization
## SZU Review
## Chapter3

## Digital logic
(1). 晶体管的工作原理:本质是一个开关

PMOS: 输出信号导出到1

NMOS: 输出信号导出到0

**comment**:

1. 互补特性
   
   PMOS管和NMOS管总是成对出现，因为2进制必须有2种状态。

   置 1 : PMOS 导通，NMOS断开;

   置 0 : PMOS 断开, NMOS导通.

2. 开关 --> Logical Gate(逻辑门)

    PMOS/NMOS --> AND、OR、NOT (与非，或非门)

    PMOS/NMOS 电路图 --> 真值表 --> 判断逻辑门的功能

3. Logical Gate --> Logical Circuit(逻辑电路)
   
   (1). 组合逻辑

   Question --> 真值表 (反应有限个输入对应的有限个输出) --> Logical Expression

   --> 电路 (真值表,逻辑表达式(在本课程中不作化简要求)). (Over)

   (2). 时序逻辑 = 组合逻辑 + 存储电路

   **存储电路的原理:**
  
   RS锁存器 --> D锁存器 (1 bit)

   基本单元(1 bit)

   **(Point)**

   **Register:**

    字(m bit)

    e.g. 在LC-3 中: m = 16 bit

    To realize: 16 × D 锁存器

    (m × 1 bit)

    **(Line)**

    **Memory:**

    2$^k$ × m bit 
    
    (k代表内存地址的长度)

    **(Plane)**

(2).  **other Points:**

   1. 内存的原理
   
   2. 内存的读写过程分析(电路图)

(3). 时序逻辑问题:

时序逻辑问题 --> 分析状态数量转换关系 --> **状态转换图 **(**Pay attention to the examples mentioned in the book**) --> 状态转换表 --> 时序逻辑电路

### comments:

1. PMOS/NMOS Circuit Analysis

2. 状态图与状态转换关系   
    