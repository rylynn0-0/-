# Introduction to Computer System Organization
## SZU Review
## Chapter8

# General

## 输入/输出设备

1. 基本原理:
    
    编址方式: 内存映射、独立编址

    传输时序控制: 同步、异步

    **轮询与中断**

2. LC-3 Keyboard and Display 的实现 **(Ban IN,OUT)**

    (1). KBSR/KBDR 轮询的代码原理

    (2). DSR/DDR 代码原理

    (3). 中断的工作原理 **(Concept)**

        中断通知

        中断响应:保存现场(硬件上多个状态机实现)

        中断号 --> 定位入口地址

        中断返回:  RET
    
    (4). 中断程序格式


   

## 输入与输出 (Variety)

1. 利用Register中的值进行计算

2. 将data从Memory装载到Register

3. 将data从Register存储到Memory

(I/O)

**Question:**

1. 内存中的数据是从哪里来的？

2. 人使用的数据是怎样通过计算机系统传出去的？

Answer: 外部设备(外设:e.g. 键盘，显示器)

## Rate:

**(How fast can the data transform.)**

keyboard:   100 bytes/sec

U 盘    :   30 - 40 MB/s  (2.0 480 mbps) 5GB/s - 10GB/s (3.1 gen1/gen2)

Internet:   1 MB/s - 1 GB/s - 10 GB/s **Obvious Difference (Variety)**

慢速的外部设备如何接到快速的总线上?

solu: 和CPU 内部总线连接

## 输入/输出控制器:

**(与外部设备直接相连)**

### Function:

1. 格式转换(统一转换为寄存器接口格式的数据)

2. 缓存(不是来一个传一个,而是等达到一定数目一起传)(fit rate!)

#### comment:先缓存数据再等待处理器读取
<img src=".\外部设备与CPU总线 .png" alt="外部设备与CPU总线" width="2000" style="float" />

①. CPU 告诉我们设备做什么---Write (控制寄存器)
    
   CPU check if tasks 've done --- Read (状态寄存器)

e.g. check the state of extern equipment:显示器是否空闲

②. CPU通过数据寄存器从设备 read/write 数据

③. 执行实际操作(e.g. 输出像素带屏幕的字符流)