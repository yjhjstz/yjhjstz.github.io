---
title: 关于
layout: page
comments: resume
---

---

#### 自我介绍

{{ site.about }}

> Linux 后端工程师，MongoDB / Postgres 内核，机器学习基础设施

> Apache PPMC 成员 · AI Infra / RAG 检索引擎方向

---

### 个人信息
- 本科/南京邮电大学, MCS@IIT 在读
- 工作年限：14年
- 邮箱：yjhjstz@163.com
- Github: https://github.com/yjhjstz
- 期望职位：系统架构师 / 高级技术专家 / AI Infra 方向
- 期望城市：杭州

---

## AI / RAG 技术能力

长期围绕 **RAG（Retrieval Augmented Generation）** 检索底座建设，覆盖从向量索引内核到落地业务的全链路，是当下大模型应用最稀缺的"数据库 + 机器学习"复合背景工程师。

- **向量检索内核**：基于 Postgres 自研亿级分布式相似检索引擎，落地 **HNSW / IVF** 高维空间索引，支持 L2 / 内积 / 余弦等多种距离度量
- **混合查询（Hybrid Search）**：关系查询 + 向量检索的融合查询，对应 RAG 中"结构化过滤 + 语义召回"的核心诉求
- **Embedding 落地经验**：支撑过人脸比对、智能客服、NLP 语义匹配、商品推荐等业务的向量化召回链路
- **深度学习 / NLP 推理基础设施**：主导弹性推理服务（DDL-Serving），支撑 NLP、CV 类模型部署，300+ 业务方、近千台 GPU，机器使用数为开源 tensorflow-serving 的 1/2 —— GPU 调度与高可用部署经验可迁移到 LLM 推理场景

> 一句话：从 Embedding 存储、ANN 召回、混合检索到 NLP 推理服务，覆盖 RAG 检索增强链路的每一层。

---

## 工作经历

### 北京酷克数据 (2022/4 ~)
- 开源数据库(https://github.com/apache/cloudberry), Apache PPMC 成员.
- 2022 加入之初启动了 Cloudberry 数据库项目，目标是先进的 Massively Parallel Processing 数据库，后开源进入 Apache 社区.
  - 阶段1: 升级 gpdb 6.x 内核到 PostgreSQL 14.4;
  - 阶段2: 提升性能，包括并行特性、Runtime filter、增量物化视图、异步物化视图;
  - 阶段3: 插件化实现存算分离的 Cloud 版本：包括稀疏索引、向量化等特性.

### 滴滴出行 (2018/3 ~ 2022/4)

#### 滴滴出行-基础平台-机器学习云平台
- 负责 OLAP / 向量检索数据库（**RAG 检索底座**）
  - 基于 Postgres 自研，提供亿级海量分布式相似检索服务方案，等价于今天的 Vector Database
    - 支持高维度空间索引（**HNSW / IVF**），融合关系查询，对应 RAG 中的"过滤 + 语义召回"
    - 业务落地：人脸比对、安防、**智能客服**、智慧交通、**NLP 语义匹配**、商品推荐等向量化召回场景
  - 实现 PostgreSQL 副本集和分片集群容器化部署
    - 基于开源 patroni 与 kubernetes 集成，实现高可用的 HA 架构部署；
    - 基于开源 citus 开发实现企业版特性：包括扩容重新平衡分片，查看统计信息。
- 负责异构平台深度学习弹性推理的架构和开发实现，管理团队4人，在滴滴云上输出（**NLP / CV 推理基础设施**）。
  - 2018.3 月初开始打造鲁班高性能弹性推理服务(DDL-Serving)，填补市面上多种深度学习模型部署的空白，提供了高可用、低延时的解决方案。目前支撑了300多个业务方，近千台 GPU 机器。机器使用数上是使用开源 tensorflow-serving 的 1/2，节省了一半以上的成本并提高了稳定性。支撑2018年公司 All in 安全的多个深度学习模型使用上线。以上 DDL-Serving 在2018年度申请专利2篇，受理2篇。

---

### 阿里巴巴 （2014/3 ~ 2017/7）

#### MongoDB 云服务
- 就职于阿里云-飞天八部-阿里云数据库团队
- MongoDB 内核核心开发，涉及运维、多存储引擎（Wiredtiger, Rocksdb, Terarkdb）、多机房容灾、副本集到 Sharding 版本演进等；
- [性能优化](http://mysql.taobao.org/monthly/2017/01/04/)，QPS 提升67%，Latency 下降90%，解决官方版本在连接数上的资源消耗问题;
- 引入 git 和持续集成系统，完成自动化构建测试，提升团队效率。

#### Node.js 云服务
- 负责 [alinode](https://www.aliyun.com/product/nodejs?spm=5176.19720258.J_8058803260.423.e9392c4az696dZ) 网站后台设计架构开发
- 通过高可用的 Agent 系统构建数据传输和控制链路，实现了云端监控、智能分析
- V8 虚拟机堆快照分析和 GC 在线分析服务
- 解决开源 Node.js 版本在性能、内存泄露、监控上的痛点
- 服务集团90%+的 node 应用，6000+实例部署，经历双11考验。

---

### 浙江大华 （2010年7月 ~ 2014年3月）

#### 职责
- Team Leader (5人)
- 存储产品线系统架构师

#### 存储系统开发
在 Linux 下从事文件系统的开发，实现视频文件的快速查找和并发写入等特性。

开发的用户态文件系统特性：
- 并发写入支持；
- 文件快速检索；
- 文件自动循环覆盖；
- 坏道处理机制。

#### NVR 存储产品
- 基于 x64 平台，最高可以接入128路前端 IPC。性能在市场上处于领先地位；
- 负责系统模块化，公共组件设计，包括 Infra, Storage, Manager，并推进开发规范化、文档化；
- 负责解决、指导项目中遇到的技术难题、参与技术选型，制定大华三代网络通信协议；
- 拥有《NVR6000软件著作权》。

---

### 开源项目&个人项目
- 参与开源项目 MongoDB, Postgres 等。

---

### 技术文章
- 开源书：[深入理解Node.js：核心思想与源码分析](https://yjhjstz.gitbooks.io/deep-into-node)
- [Node.js相关技术博客](https://alinode.aliyun.com)
- [数据库相关博客](http://mysql.taobao.org/monthly/2017/01/)

---

### 专利
- 《基于V8一种内存可控的并行垃圾回收标记方法》 专利受理号为：cn 201610187840.2
- 《基于 Coredump 文件的一种定向分析内存的方法》 专利受理号为：cn 201710322576.3
- 《基于协程的自适应低延时成组提交技术》专利受理号：cn 2018113943420
- 《异构硬件平台弹性推理服务》 cn 2018115500268
- 《异步物化视图的中间结果存储和透明替换的方法》cn2025102460934

---

### 技能清单
以下均为我经常使用的技能，排在前面表示更熟悉，主要技术领域在 **数据库内核 / 向量检索 / AI Infra / NoSQL**。

- 开发工具：C/C++/Claude/Codex
- 调试调优：gdb/oprofile/perf/hopper
- 数据库内核：Postgres / Greenplum / MongoDB
- **AI / RAG**：向量索引（HNSW / IVF）、Embedding 召回、Hybrid Search、NLP 推理服务
- 版本管理、持续集成：svn/git/jenkins/
- 开发平台：Linux/Mac/Arm
