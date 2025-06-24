# Introduction to Computer System Organization
## SZU Review
## Chapter4

## Model

1. 冯-诺依曼模型

    部件级原理

    内存:MAR/MDR

    寄存器(Register) --> 运算器(ALU)

    控制器(Control Unit):

    1. PC:
   
        自加性 (保证程序顺序执行)
   
        可改写性 (当遇到BR分支指令时执行对应条件下的分支跳转)
   
    2. IR: 转存

2. 指令的3种类型

   (a). 计算型指令(ADD,AND,NOT)

   (b). 数据搬移型指令(LD,ST,LDR,LDI,STR,STI,LEA)

   (c).控制型指令(JMP,BR)

3. 指令执行的步骤(Process)
   
   取指令 --> 译码 --> 地址计算(仅针对数据搬移型指令) --> 取操作数 --> Execute(执行:特指运算)(故只有运算型指令有这一步) --> 写回 (Not all the steps are necessary.)

   e.g. 

    ADD 指令 (无地址计算)
        
    LD 指令 (无执行(计算))
