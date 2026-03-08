---
title: GitHub 贡献
layout: page
---

<style>
.stat-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin: 16px 0 24px;
}
.stat-card {
  background: #f6f8fa;
  border: 1px solid #e1e4e8;
  border-radius: 6px;
  padding: 16px 20px;
  min-width: 130px;
  text-align: center;
}
.stat-card .num {
  font-size: 2em;
  font-weight: bold;
  color: #0366d6;
  display: block;
}
.stat-card .label {
  font-size: 0.85em;
  color: #586069;
}
.contrib-table table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.9em;
}
.contrib-table th {
  background: #f6f8fa;
  border: 1px solid #e1e4e8;
  padding: 8px 10px;
  text-align: left;
}
.contrib-table td {
  border: 1px solid #e1e4e8;
  padding: 7px 10px;
  vertical-align: top;
}
.contrib-table tr:hover td {
  background: #f6f8fa;
}
.tag {
  display: inline-block;
  background: #0366d6;
  color: #fff;
  border-radius: 10px;
  padding: 1px 8px;
  font-size: 0.78em;
  margin-right: 4px;
}
.tag.green { background: #28a745; }
.tag.gray  { background: #586069; }
</style>

---

## 贡献统计

<div class="stat-grid">
  <div class="stat-card"><span class="num">145</span><span class="label">合并 PR 总数</span></div>
  <div class="stat-card"><span class="num">106</span><span class="label">PR Review</span></div>
  <div class="stat-card"><span class="num">98</span><span class="label">Commits（近期）</span></div>
  <div class="stat-card"><span class="num">11</span><span class="label">Issues</span></div>
  <div class="stat-card"><span class="num">4395⭐</span><span class="label">deep-into-node</span></div>
</div>

---

## 开源贡献

### [apache/cloudberry](https://github.com/apache/cloudberry) — Apache PPMC 成员

主力贡献仓库，贡献方向覆盖优化器、存储引擎、工具链、CI/CD。

<div class="contrib-table">

| PR | 类别 | 描述 |
|----|------|------|
| [#1573](https://github.com/apache/cloudberry/pull/1573) | <span class="tag">ORCA</span> | Fix window function cost model producing zero local cost when no ORDER BY |
| [#1543](https://github.com/apache/cloudberry/pull/1543) | <span class="tag">ORCA</span> | Optimize CDatumSortedSet by checking IsSorted before sorting |
| [#1533](https://github.com/apache/cloudberry/pull/1533) | <span class="tag">ORCA</span> | Fix memory leak in CWindowOids by adding destructor |
| [#1519](https://github.com/apache/cloudberry/pull/1519) | <span class="tag">ORCA</span> | Validate hash function existence in IsOpHashJoinable |
| [#1512](https://github.com/apache/cloudberry/pull/1512) | <span class="tag">ORCA</span> | Fix assertion failure for dynamic table scan rewindability |
| [#1409](https://github.com/apache/cloudberry/pull/1409) | <span class="tag">ORCA</span> | Skip MVCC system columns for standalone AO tables |
| [#1392](https://github.com/apache/cloudberry/pull/1392) | <span class="tag">ORCA</span> | Fix segmentation fault when appending group statistics |
| [#1360](https://github.com/apache/cloudberry/pull/1360) | <span class="tag">ORCA</span> | Prevent crashes with extension prosupport functions in NULL rtable queries |
| [#1319](https://github.com/apache/cloudberry/pull/1319) | <span class="tag">ORCA</span> | Reject functions with prosupport in DXL translation |
| [#1241](https://github.com/apache/cloudberry/pull/1241) | <span class="tag green">存储</span> | Fast ANALYZE for append-optimized tables |
| [#1025](https://github.com/apache/cloudberry/pull/1025) | <span class="tag green">存储</span> | Improve appendonly_getnextslot to optimize tuple retrieval |
| [#1010](https://github.com/apache/cloudberry/pull/1010) | <span class="tag green">存储</span> | Optimize AOCS scan performance by introducing specialized no-qual path |
| [#1170](https://github.com/apache/cloudberry/pull/1170) | <span class="tag gray">工具</span> | gpfdist add --compress-level option |
| [#1225](https://github.com/apache/cloudberry/pull/1225) | <span class="tag gray">工具</span> | gpfdist: use event_base with libevent 2.0+ to avoid thread-unsafe event_init |
| [#1016](https://github.com/apache/cloudberry/pull/1016) | <span class="tag gray">CI/CD</span> | Upload Cloudberry debuginfo RPM build artifacts |
| [#280](https://github.com/apache/cloudberry/pull/280) | <span class="tag green">特性</span> | Incremental view maintenance（增量物化视图）|
| [#647](https://github.com/apache/cloudberry/pull/647) | <span class="tag green">特性</span> | Refactor parallel scan node and framework |

</div>

> 另有约 40 个 Cherry-pick / backport 系列 PR，将 PostgreSQL 上游修复合并入 Cloudberry 主线。

---

### 其他开源项目

<div class="contrib-table">

| 仓库 | PR | 描述 |
|------|----|------|
| [dbeaver/dbeaver](https://github.com/dbeaver/dbeaver/pull/37590) | #37590 | Fix version extraction for Cloudberry and Apache Cloudberry |
| [citusdata/pg_cron](https://github.com/citusdata/pg_cron/pull/395) | #395 | Fix type mismatch in dsm_attach() argument by using DatumGetUInt32() |
| [cloudberry-contrib/plcontainer](https://github.com/cloudberry-contrib/plcontainer) | #1/#2/#6 | 适配 Cloudberry 主线、修复 libcurl 链接、升级 json-c |
| [apache/cloudberry-devops-release](https://github.com/apache/cloudberry-devops-release/pull/12) | #12 | Add debuginfo package support |

</div>

---

## 个人代表项目

<div class="contrib-table">

| 仓库 | Stars | 描述 |
|------|-------|------|
| [deep-into-node](https://github.com/yjhjstz/deep-into-node) | ⭐ 4395 | 《深入理解 Node.js：核心思想与源码分析》开源书，618 forks |
| [mempool](https://github.com/yjhjstz/mempool) | ⭐ 4 | nginx-like 内存池实现（C） |
| [pandorabox](https://github.com/yjhjstz/pandorabox) | ⭐ 9 | 路由器固件 |
| [postgres-xl-docker](https://github.com/yjhjstz/postgres-xl-docker) | — | 分布式图数据库 POC，支持 OpenCypher、向量、地理融合查询 |
| [libuv](https://github.com/yjhjstz/libuv) | ⭐ 2 | 异步 I/O 库 |

</div>

---

<small>数据来源：GitHub API，最后更新 2026-03</small>
