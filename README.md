# SPEC 2006 Memory Access Pattern Analysis

# 0. 总体方法论
1. 用Gem5跑一遍spec 2006 benchmark中所有的checkpoint(这里为了简单，只做了权重最高的ckpt的分析)，按照[gem5 trace](https://github.com/miaochenlu/Gem5_tutorials/blob/main/mem_trace.md)方法收集L1 miss trace
2. 绘制全局miss图，查看整体pattern
3. 找到miss最多的pc, 到汇编进行对应，再找到对应的spec源码，分析pattern

(也可以用linux perf去分析热点函数)

# 1. INT

* [462.libquantum](https://swevaw4b4lv.feishu.cn/docx/A8SodO5wzofOZyxBvdscdAEBnnh?from=from_copylink)
* [471.omnetpp](https://swevaw4b4lv.feishu.cn/docx/GfqKdfcivo0eElxQ2Dzc1HESn5c?from=from_copylink)

# 2. FP

* [433.milc](https://swevaw4b4lv.feishu.cn/docx/PstFdClK6oxlrCxv6R2ckhCDnsh?from=from_copylink)
