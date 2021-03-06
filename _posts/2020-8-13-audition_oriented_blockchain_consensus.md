---
layout: post
title:  "向监管开放的联盟链共识算法"
date:   2020-8-13 12:20:01
categories: thoughts
tags: consensus blockchain audition
---

* content
{:toc}

---
# Table of Contents

1.  [相关工作，现阶段方案](#org9007d1f)
2.  [缺点](#org77a686e)
3.  [解决方法](#orge745d6b)
4.  [基于TEE的共识算法](#orgf88af43)

向监管开放的联盟链共识算法


<a id="org9007d1f"></a>

# 相关工作，现阶段方案

目前，监管部门为了对某一条联盟链进行监管，通常做法是参与该条链中，作为其中一个参与方，部署一个节点。监管部分管理的这个节点与链上其他参与方的节点一样，运行相同的代码。

或者，监管部门不用直接管理该条链上的一个节点，只要求某条链上某个参与方实时的把他的最新区块转发给监管链。这种方案比第一种情况更不稳定，优点是成本更低。


<a id="org77a686e"></a>

# 缺点

但是，这种方案非常不安全。因为联盟链的共识算法通常使用raft或者pbft算法。这意味着作恶节点如果超过1/2(raft),或者2/3（pbft）就可以伪造一条分叉链。而且作恶节点可以操控任意一个诚实节点的账本。

对应于目前监管链的场景，如果链上有超过超过1/2 或者 2/3的节点不愿意让监管部门看到真实的账本信息，即可通过统一修改各自的区块链节点源代码，执行拜占庭攻击，让监管部门的节点只能看到一个分叉链。这样，就能对监管部门隐藏真实账本信息。

这种攻击的可行性，是因为当前主流区块链采用pbft算法，只能容纳1/3作恶节点。如果监管部门想要确保不会被其他参与者联合欺骗，那么必须在链上拥有超过2/3的节点。这就等价于监管部分帮助链上各个参与方达成共识，成本过高，超出了监管的目标。


<a id="orge745d6b"></a>

# 解决方法

TEE技术可以使恶意节点无法偏离共识协议，即无法修改自己的控制的节点上的共识算法源码。通过把raft协议放到TEE中，可以使得恶意节点无法作恶，不能欺骗监管部分。

只有在一种情况下，可以欺骗监管部们。必须除监管部门外的所有节点合谋，另外部署一条链，用于非法目的。给监管部分看的则是一条专门设计的不包括非法信息的链。对于作恶者来说，这种欺骗的成本过高，而且还能被其他手段检测到。监管部门可以通过现实世界中其他手段，比如监控这些参与方所拥有的服务器，来检测到这种欺骗行为。


<a id="orgf88af43"></a>

# 基于TEE的共识算法

略

