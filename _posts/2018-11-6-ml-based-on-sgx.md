---
layout: post
title:  "基于SGX实现Machine learning"
date:   2018-11-06 12:20:01
categories: thoughts
tags: ML SGX
---

* content
{:toc}

---
## 问题：

### 很难同时保护隐私数据和私有算法。

如果想要同时保护隐私数据不被其他人获取，私有算法本身也不公开，那么必须使算法的计算结果也保存在平台上，不能流出，只能由最终用户来使用

### 无法使用GPU，intel sgx是基于intel的cpu

可能在很长时间内都很难实现GPU硬件层面的安全计算环境，这将是一个很大的限制。

### 目前无法使用分布式集群来计算

或许未来可以用sgx组成集群，实现类似hadoop之类的大数据处理框架。但hadoop依赖cft算法如parox/raft。因此要实现hadoop-sgx首先需要实现raft-sgx。

### 缺少库函数

但对每一个不同的应用，需要专门开发一套程序。或许我们可以尝试实现一些通用的库函数。从业务中提炼出一套通用的API接口，隐私数据读写接口，索引创建删除接口，MapReduce接口
