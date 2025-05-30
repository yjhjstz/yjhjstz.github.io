---
title: 关于
layout: page
comments: resume
---

---

#### 自我介绍

{{ site.about }}

> Linux 后端工程师，MongoDB,  Postgres , 机器学习

> Apache PMC 成员


---


### 个人信息
 - 本科/南京邮电大学, MCS@IIT 在读
 - 工作年限：14年
 - 邮箱：yjhjstz@163.com
 - Github: https://github.com/yjhjstz 
 - 期望职位：系统架构师，高级技术专家
 - 期望城市：杭州

---



## 工作经历
### 北京酷克数据 (2022/4 ~)
  - 开源数据库(https://github.com/apache/cloudberry), Apache PPMC 成员.
  - 2022 加入之初启动了 Cloudberry 数据库项目,  目标是先进的Massively Parallel Processing 数据库, 后开源进入Apache 社区.
    - 阶段1: 升级 gpdb 6.x内核到Postgresql 14.4;
    - 阶段2: 提升性能, 包括并行特性, Runtime filter, 增量物化视图, 异步物化视图;
    - 阶段3: 插件化实现存算分离的Cloud 版本: 包括稀疏索引,向量化等特性.

### 滴滴出行 (2018/3 ~ 2022/4)
---
### 滴滴出行-基础平台-机器学习云平台
- 负责 OLAP 数据库
   * 基于 Postgres 自研，提供亿级海量分布式相似检索服务方案
       - 支持高维度空间索引（HNSW，IVF），融合关系查询；
       - 支持内部人脸比对，安防项目，智能客服，智慧交通, NLP比对, 商品推荐落地。
   * 实现 PostgreSQL 副本集和分片集群容器化部署
     - 基于开源patroni与kubernetes集成，实现高可用的HA架构部署；
     - 基于开源 citus 开发实现企业版特性：包括扩容重新平衡分片，查看统计信息。

- 负责异构平台深度学习弹性推理的架构和开发实现，管理团队4人， 在滴滴云上输出。
  * 2018.3月初开始打造鲁班高性能弹性推理服务(DDL-Serving)，填补市面上多种深度学习模型部署的空白，提供了高可用，低延时的解决方案。目前支撑了300多个业务方，近千台GPU机器。机器使用数上是使用开源tensorflow-serving的1/2，节省了一半以上的成本并提高了稳定性。支撑2018年公司All in 安全的多个深度学习模型使用上线。以上DDL-Serving在2018年度申请专利2篇，受理2篇。

---

### 阿里巴巴 （ 2014/3 ~ 2017/7）

---

#### MongoDB 云服务
- 就职于阿里云-飞天八部-阿里云数据库团队
- MongoDB 内核核心开发, 涉及运维,多存储引擎（Wiredtiger, Rocksdb, Terarkdb）,多机房容灾, 副本集到Sharding版本演进等；
- [性能优化](http://mysql.taobao.org/monthly/2017/01/04/)，QPS 提升67%，Latency下降90%，解决官方版本在连接数上的资源消耗问题;
- 引入git和持续集成系统, 完成自动化构建测试，提升团队效率。

---

#### Node.js 云服务
- 负责 [alinode](https://www.aliyun.com/product/nodejs?spm=5176.19720258.J_8058803260.423.e9392c4az696dZ) 网站后台设计架构开发
- 通过高可用的 Agent 系统构建数据传输和控制链路，实现了云端监控，智能分析
- V8 虚拟机堆快照分析和 GC 在线分析服务
- 解决开源 Node.js 版本在性能，内存泄露，监控上的痛点
- 服务集团90%+的 node 应用，6000+实例部署，经历双11考验。

---



 
### 浙江大华 （ 2010年7月 ~ 2014年3月 ）

---
#### 职责

- Team Leader (5人)
- 存储产品线系统架构师

---

#### 存储系统开发
在Linux下从事文件系统的开发,实现视频文件的快速查找和并发写入等特性。

开发的用户态文件系统特性：
1、并发写入支持；
2、文件快速检索；
3、文件自动循环覆盖；
4、坏道处理机制。

---

#### NVR 存储产品
- 基于x64平台，最高可以接入128路前端IPC。性能在市场上处于领先地位；
- 负责系统模块化，公共组件设计，包括 Infra, Storage, Manager，并推进开发规范化，文档化；
- 负责解决、指导项目中遇到的技术难题、参与技术选型，制定大华三代网络通信协议；
- 拥有《NVR6000软件著作权》。

---


### 开源项目&个人项目
- 参与开源项目 Google V8,  libuv, MongoDB, Postgres 等。
- 个人分布式图数据库POC，基于 Postgres-XL 实现多模态数据存储查询，包括以下：
     - 补齐分布式图数据库的功能，实现*OpenCypher* 语法支持，多跳邻居查询，最短路径；
     - 关系，地理位置和向量，图关系融合查询 https://github.com/yjhjstz/postgres-xl-docker

---

### 技术文章
- 开源书：[深入理解Node.js：核心思想与源码分析]( https://yjhjstz.gitbooks.io/deep-into-node )
-  [Node.js相关技术博客](https://alinode.aliyun.com)
- [数据库相关博客](http://mysql.taobao.org/monthly/2017/01/)

---

### 外部演讲
 - 2015 MPD 工作坊——南京站：《基于node运行时的应用性能管理解决方案》
 - 2017 云栖大会深圳峰会--物联网大数据专场：《基于MongoDB与Node.js构建物联网系统》

---

### 专利
- 《基于V8一种内存可控的并行垃圾回收标记方法》 专利受理号为：cn 201610187840.2
- 《基于 Coredump 文件的一种定向分析内存的方法》 专利受理号为：cn 201710322576.3
- 《基于协程的自适应低延时成组提交技术》专利受理号：cn 2018113943420
- 《异构硬件平台弹性推理服务》 cn 2018115500268
- 《异步物化视图的中间结果存储和透明替换的方法》cn2025102460934
 
---

### 技能清单
以下均为我经常使用的技能, 排在前面表示更熟悉，主要技术领域在存储，虚拟机，Nosql。

- 开发语言：C/C++/Node.js/Java/Shell/Python
- 调试调优：gdb/oprofile/perf/hopper
- 数据库相关：Postgres/Greenplum/MongoDB
- 版本管理、持续集成：svn/git/jenkins/
- 开发平台：Linux/Mac/Arm


