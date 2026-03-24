---
title: 作品集
layout: page
---

<style>
/* ── portfolio grid ── */
.pf-intro {
  font-size: 0.95rem;
  color: var(--text-muted);
  margin-bottom: 2rem;
  line-height: 1.7;
}

.pf-grid {
  display: grid;
  gap: 1.25rem;
}

.pf-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 1.5rem 1.75rem;
  transition: border-color 0.2s, box-shadow 0.2s;
  position: relative;
}
.pf-card:hover {
  border-color: var(--link);
  box-shadow: 0 4px 24px rgba(0,0,0,0.3);
}

.pf-card-head {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  margin-bottom: 0.75rem;
}

.pf-card-icon {
  font-size: 1.3rem;
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(0, 230, 118, 0.08);
  border-radius: var(--radius);
  flex-shrink: 0;
}

.pf-card-title {
  font-family: var(--font-mono);
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--text);
}
.pf-card-title a {
  color: var(--text);
  text-decoration: none;
}
.pf-card-title a:hover {
  color: var(--link);
  text-decoration: none;
}

.pf-card-fork {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  color: var(--text-muted);
  background: rgba(110, 118, 129, 0.12);
  padding: 0.1rem 0.45rem;
  border-radius: 4px;
  margin-left: 0.3rem;
}

.pf-card-desc {
  font-size: 0.9rem;
  color: var(--text-muted);
  line-height: 1.65;
  margin-bottom: 1rem;
}

.pf-card-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin-bottom: 1rem;
}

.pf-tag {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  color: var(--accent);
  border: 1px solid rgba(0, 230, 118, 0.25);
  background: rgba(0, 230, 118, 0.06);
  padding: 0.12rem 0.55rem;
  border-radius: 20px;
}

.pf-tag--lang {
  color: var(--link);
  border-color: rgba(88, 166, 255, 0.3);
  background: rgba(88, 166, 255, 0.08);
}

.pf-card-footer {
  display: flex;
  align-items: center;
  gap: 1rem;
  font-family: var(--font-mono);
  font-size: 0.78rem;
  color: var(--text-muted);
}

.pf-card-footer a {
  color: var(--link);
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
}
.pf-card-footer a:hover {
  text-decoration: underline;
}

.pf-card-footer svg {
  width: 14px;
  height: 14px;
  fill: currentColor;
}

/* ── upstream badge ── */
.pf-upstream {
  font-size: 0.78rem;
  color: var(--text-muted);
  margin-top: 0.5rem;
}
.pf-upstream a {
  color: var(--link);
}

@media (max-width: 640px) {
  .pf-card { padding: 1.2rem 1rem; }
}
</style>

# 作品集

<p class="pf-intro">
  以下是我参与开发和贡献的核心项目，涵盖数据库内核、查询优化器、性能基准测试等方向。
</p>

<div class="pf-grid">

<!-- QuantWise (ccode) -->
<div class="pf-card">
  <div class="pf-card-head">
    <div class="pf-card-icon">⚡</div>
    <span class="pf-card-title"><a href="https://github.com/quantumiodb/quantwise">QuantWise</a></span>
  </div>
  <div class="pf-card-desc">
    Agentic Coding & Trading 终端智能工具 — 基于 Claude 构建，集编码助手与交易分析于一体。支持代码理解/生成/调试、Git 操作、交互式数据库调试，内置 30+ 交易分析 Skills（股票分析、CANSLIM 选股、VCP 形态筛选、期权策略、机构资金流向追踪等），并提供 Bash、浏览器控制、PostgreSQL 交互等内置工具。
  </div>
  <div class="pf-card-tags">
    <span class="pf-tag--lang pf-tag">Python</span>
    <span class="pf-tag--lang pf-tag">Swift</span>
    <span class="pf-tag--lang pf-tag">JavaScript</span>
    <span class="pf-tag">Agentic AI</span>
    <span class="pf-tag">Claude Code</span>
    <span class="pf-tag">FinTech</span>
    <span class="pf-tag">Skills</span>
    <span class="pf-tag">CLI</span>
  </div>
  <div class="pf-card-footer">
    <a href="https://github.com/quantumiodb/quantwise">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      查看源码
    </a>
    <a href="https://quantumio.com.cn/">
      🌐 官网
    </a>
  </div>
</div>

<!-- postgres (quantum-13.3) -->
<div class="pf-card">
  <div class="pf-card-head">
    <div class="pf-card-icon">🐘</div>
    <span class="pf-card-title"><a href="https://github.com/quantumiodb/postgres/tree/quantum-13.3">postgres</a></span>
    <span class="pf-card-fork">quantum-13.3</span>
  </div>
  <div class="pf-card-desc">
    基于 PostgreSQL 13.3 的向量检索增强版本 — 内置 HNSW（Hierarchical Navigable Small World）和 IVF（Inverted File Index）向量索引插件，为 PostgreSQL 提供原生高性能近似最近邻搜索能力，适用于 AI Embedding 检索、推荐系统等场景。
  </div>
  <div class="pf-card-tags">
    <span class="pf-tag--lang pf-tag">C</span>
    <span class="pf-tag--lang pf-tag">PLpgSQL</span>
    <span class="pf-tag--lang pf-tag">C++</span>
    <span class="pf-tag">HNSW</span>
    <span class="pf-tag">IVF</span>
    <span class="pf-tag">Vector Search</span>
    <span class="pf-tag">ANN</span>
  </div>
  <div class="pf-card-footer">
    <a href="https://github.com/quantumiodb/postgres/tree/quantum-13.3">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      查看源码
    </a>
    <span>private</span>
  </div>
</div>

<!-- Cloudberry -->
<div class="pf-card">
  <div class="pf-card-head">
    <div class="pf-card-icon">🫐</div>
    <span class="pf-card-title"><a href="https://github.com/quantumiodb/cloudberry">cloudberry</a></span>
    <span class="pf-card-fork">fork</span>
  </div>
  <div class="pf-card-desc">
    Apache Cloudberry (Incubating) — 先进且成熟的开源 MPP（大规模并行处理）数据库，Greenplum Database 的开源替代方案。参与分布式查询优化、并行执行引擎等核心模块开发。
  </div>
  <div class="pf-card-tags">
    <span class="pf-tag--lang pf-tag">C</span>
    <span class="pf-tag--lang pf-tag">C++</span>
    <span class="pf-tag--lang pf-tag">PLpgSQL</span>
    <span class="pf-tag--lang pf-tag">Python</span>
    <span class="pf-tag">MPP</span>
    <span class="pf-tag">Distributed</span>
    <span class="pf-tag">OLAP</span>
  </div>
  <div class="pf-card-footer">
    <a href="https://github.com/quantumiodb/cloudberry">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      查看源码
    </a>
  </div>
  <div class="pf-upstream">
    上游: <a href="https://github.com/apache/cloudberry">apache/cloudberry</a>
  </div>
</div>

<!-- xlgraph -->
<div class="pf-card">
  <div class="pf-card-head">
    <div class="pf-card-icon">🕸️</div>
    <span class="pf-card-title"><a href="https://github.com/quantumiodb/xlgraph">xlgraph</a></span>
  </div>
  <div class="pf-card-desc">
    基于 Postgres-XL v10.4 的分布式图数据库 — 在 Postgres-XL 分布式架构之上扩展图数据模型与图查询能力，支持大规模图存储与遍历，融合关系型与图数据库的优势，适用于社交网络、知识图谱、欺诈检测等场景。
  </div>
  <div class="pf-card-tags">
    <span class="pf-tag--lang pf-tag">C</span>
    <span class="pf-tag--lang pf-tag">PLpgSQL</span>
    <span class="pf-tag--lang pf-tag">Perl</span>
    <span class="pf-tag">Graph Database</span>
    <span class="pf-tag">Postgres-XL</span>
    <span class="pf-tag">Distributed</span>
  </div>
  <div class="pf-card-footer">
    <a href="https://github.com/quantumiodb/xlgraph">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      查看源码
    </a>
    <span>private</span>
  </div>
</div>

<!-- pg_tpch & pg_tpcds -->
<div class="pf-card">
  <div class="pf-card-head">
    <div class="pf-card-icon">📊</div>
    <span class="pf-card-title"><a href="https://github.com/quantumiodb/pg_tpch">pg_tpch</a> / <a href="https://github.com/quantumiodb/pg_tpcds">pg_tpcds</a></span>
    <span class="pf-card-fork">fork</span>
  </div>
  <div class="pf-card-desc">
    PostgreSQL TPC 性能基准测试扩展套件 — 即插即用的 Postgres 扩展，pg_tpch 内置 TPC-H 数据生成与查询模板，pg_tpcds 受 DuckDB 启发覆盖 TPC-DS 全部 99 条复杂查询，用于评估数据库 OLAP 查询性能、优化器效果与大规模决策支持能力。
  </div>
  <div class="pf-card-tags">
    <span class="pf-tag--lang pf-tag">C++</span>
    <span class="pf-tag--lang pf-tag">C</span>
    <span class="pf-tag--lang pf-tag">CMake</span>
    <span class="pf-tag">Benchmark</span>
    <span class="pf-tag">TPC-H</span>
    <span class="pf-tag">TPC-DS</span>
    <span class="pf-tag">Extension</span>
  </div>
  <div class="pf-card-footer">
    <a href="https://github.com/quantumiodb/pg_tpch">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      pg_tpch
    </a>
    <a href="https://github.com/quantumiodb/pg_tpcds">
      <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
      pg_tpcds
    </a>
  </div>
  <div class="pf-upstream">
    上游: <a href="https://github.com/askyx/pg_tpch">askyx/pg_tpch</a> · <a href="https://github.com/askyx/pg_tpcds">askyx/pg_tpcds</a>
  </div>
</div>

</div>
