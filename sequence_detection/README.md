# 摩尔状态机序列检测器

## 目标

1. 设计“1101”序列检测的状态转换图。
2. 调用并转串输出模块，使用 Verilog HDL 语言的行为描述方式实现一个摩尔状态机，能检测一个 8 位的二进制数据中是否存在“1101”序列，如果检测到该序列则指定的 LED 灯亮。 
3. 综合、实现、生成 bit 流，下载到 Nexys4 开发板进行验证。

## 设计

### 原理

状态表与状态图是用来表示同步时序电路的输入、输出、现态、次态之间转移关系的两种常用工具。如果同步时序电路的输出只与现态有关而与输入无关，则称该电路为 Moore型电路。 

序列检测器在很多数字系统中都不可缺少，尤其是在通信系统当中。序列检测器的作用就是从一系列的码流中找出用户希望出现的序列，序列可长可短。比如在通信系统中，数据流帧头的检测就属于一个序列检测器。序列检测器的类型有很多种，有逐比特比较的，有逐字节比较的，也有其他的比较方式，实际应用中需要采用何种比较方式，主要是看序列的多少以及系统的延时要求。

### 状态图

![image-20210316223252658](https://frozenwhale.oss-cn-beijing.aliyuncs.com/img/image-20210316223252658.png)

## 实现

1. 序列检测模块（状态机实现）
2. 并转串模块
3. 按键消抖模块