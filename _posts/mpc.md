
# Table of Contents

1.  [MPC 协议](#org241eec2)
2.  [2pc 和 mpc 的不同点](#org1f2fc1d)
3.  [姚老板论文：混淆电路 + 不经意传输可以构建mpc](#orgd87f234)
4.  [只需要不经意传输原语，就可以构建MPC](#org37a4597)
5.  [在标准模型下，不可能构建UC安全的mpc协议](#orgb2340db)
6.  [在crs模型下，可以构建UC安全的mpc协议](#orgd8ee909)
7.  [构建UC安全的2pc的方法](#org17d59a7)
    1.  [构建F<sub>mcom</sub>](#orge953f5b)
    2.  [构建F<sub>ot</sub>](#org23e2293)
    3.  [基于F<sub>mcom和F</sub><sub>ot构建F</sub><sub>zk</sub>](#org8629920)
    4.  [基于F<sub>zk</sub> 构建F<sub>cp</sub>](#org3f6cdef)
    5.  [基于F<sub>CP</sub> 和 GMW compiler构建2pc](#orgb603cbc)
8.  [基于TEE如何构建MPC协议](#org14eea9f)


<a id="org241eec2"></a>

# MPC 协议


<a id="org1f2fc1d"></a>

# 2pc 和 mpc 的不同点

mpc依赖于假设系统中超过半数节点不作恶的假设。2pc不能依赖这种假设，因为只有俩节点。


<a id="orgd87f234"></a>

# 姚老板论文：混淆电路 + 不经意传输可以构建mpc


<a id="org37a4597"></a>

# 只需要不经意传输原语，就可以构建MPC


<a id="orgb2340db"></a>

# 在标准模型下，不可能构建UC安全的mpc协议


<a id="orgd8ee909"></a>

# 在crs模型下，可以构建UC安全的mpc协议


<a id="org17d59a7"></a>

# 构建UC安全的2pc的方法


<a id="orge953f5b"></a>

## 构建F<sub>mcom</sub>


<a id="org23e2293"></a>

## 构建F<sub>ot</sub>


<a id="org8629920"></a>

## 基于F<sub>mcom和F</sub><sub>ot构建F</sub><sub>zk</sub>


<a id="org3f6cdef"></a>

## 基于F<sub>zk</sub> 构建F<sub>cp</sub>


<a id="orgb603cbc"></a>

## 基于F<sub>CP</sub> 和 GMW compiler构建2pc


<a id="org14eea9f"></a>

# 基于TEE如何构建MPC协议

