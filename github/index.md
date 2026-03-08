---
title: GitHub 贡献
layout: page
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
/* ── reset within content ── */
.gh-wrap * { box-sizing: border-box; }
.gh-wrap a { text-decoration: none; }

/* ── fonts ── */
.gh-wrap { font-family: 'DM Sans', sans-serif; }
.mono     { font-family: 'JetBrains Mono', monospace; }

/* ── hero ── */
.gh-hero {
  background: #0d1117;
  border-radius: 12px;
  padding: 40px 36px 32px;
  margin: 8px 0 28px;
  position: relative;
  overflow: hidden;
}
.gh-hero::before {
  content: '';
  position: absolute;
  top: -60px; right: -60px;
  width: 260px; height: 260px;
  background: radial-gradient(circle, rgba(0,210,110,.18) 0%, transparent 70%);
  pointer-events: none;
}
.gh-hero-title {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 3px;
  color: #00e676;
  text-transform: uppercase;
  margin-bottom: 6px;
}
.gh-hero-name {
  font-family: 'DM Sans', sans-serif;
  font-size: 26px;
  font-weight: 600;
  color: #e6edf3;
  margin-bottom: 20px;
}
.gh-hero-name a {
  color: #58a6ff;
  font-family: 'JetBrains Mono', monospace;
  font-size: 15px;
  font-weight: 400;
}
.gh-hero-name a:hover { color: #79c0ff; }

/* ── stat cards ── */
.gh-stats {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 12px;
}
@media (max-width: 720px) {
  .gh-stats { grid-template-columns: repeat(3, 1fr); }
}
.stat-card {
  background: #161b22;
  border: 1px solid #21262d;
  border-radius: 8px;
  padding: 16px 12px 14px;
  text-align: center;
  transition: border-color .2s, transform .2s;
}
.stat-card:hover {
  border-color: #00e676;
  transform: translateY(-2px);
}
.stat-num {
  font-family: 'JetBrains Mono', monospace;
  font-size: 28px;
  font-weight: 700;
  color: #00e676;
  display: block;
  line-height: 1;
  margin-bottom: 6px;
}
.stat-num.blue  { color: #58a6ff; }
.stat-num.amber { color: #e3b341; }
.stat-num.pink  { color: #f778ba; }
.stat-label {
  font-size: 11px;
  color: #8b949e;
  text-transform: uppercase;
  letter-spacing: 1px;
}

/* ── section header ── */
.gh-section-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 32px 0 16px;
}
.gh-section-header h2 {
  font-family: 'DM Sans', sans-serif !important;
  font-size: 17px !important;
  font-weight: 600 !important;
  color: #1f2328 !important;
  margin: 0 !important;
  padding: 0 !important;
}
.gh-dot {
  width: 8px; height: 8px;
  border-radius: 50%;
  background: #00e676;
  flex-shrink: 0;
}
.gh-count {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  background: #eaf5ec;
  color: #1a7f37;
  border-radius: 20px;
  padding: 2px 8px;
  font-weight: 600;
}

/* ── filter tabs ── */
.gh-filters {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
  margin-bottom: 14px;
}
.gh-filter-btn {
  font-family: 'DM Sans', sans-serif;
  font-size: 12px;
  font-weight: 500;
  padding: 4px 12px;
  border-radius: 20px;
  border: 1px solid #d0d7de;
  background: #fff;
  color: #57606a;
  cursor: pointer;
  transition: all .15s;
}
.gh-filter-btn:hover,
.gh-filter-btn.active {
  background: #0d1117;
  color: #fff;
  border-color: #0d1117;
}
.gh-filter-btn.active[data-filter="orca"]   { background: #7c3aed; border-color: #7c3aed; }
.gh-filter-btn.active[data-filter="storage"]{ background: #0969da; border-color: #0969da; }
.gh-filter-btn.active[data-filter="tool"]   { background: #bf8700; border-color: #bf8700; }
.gh-filter-btn.active[data-filter="fix"]    { background: #cf222e; border-color: #cf222e; }
.gh-filter-btn.active[data-filter="feature"]{ background: #1a7f37; border-color: #1a7f37; }

/* ── PR list ── */
.gh-pr-list {
  border: 1px solid #d0d7de;
  border-radius: 8px;
  overflow: hidden;
}
.gh-pr-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 12px 16px;
  border-bottom: 1px solid #f3f4f6;
  transition: background .12s;
}
.gh-pr-item:last-child { border-bottom: none; }
.gh-pr-item:hover { background: #f6f8fa; }
.gh-pr-item[data-hide="true"] { display: none; }

.pr-icon {
  flex-shrink: 0;
  margin-top: 2px;
  color: #8250df;
}
.pr-body { flex: 1; min-width: 0; }
.pr-title {
  font-size: 13.5px;
  font-weight: 500;
  color: #1f2328;
  line-height: 1.4;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.pr-title a { color: #1f2328; }
.pr-title a:hover { color: #0969da; }
.pr-meta {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-top: 4px;
  flex-wrap: wrap;
}
.pr-repo {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  color: #57606a;
}
.pr-date {
  font-size: 11px;
  color: #8c959f;
  font-family: 'JetBrains Mono', monospace;
}

/* ── badge ── */
.badge {
  font-size: 10px;
  font-weight: 600;
  font-family: 'DM Sans', sans-serif;
  padding: 1px 7px;
  border-radius: 20px;
  text-transform: uppercase;
  letter-spacing: .4px;
  flex-shrink: 0;
}
.badge-orca    { background: #f3e8ff; color: #6f42c1; }
.badge-storage { background: #dbeafe; color: #0550ae; }
.badge-tool    { background: #fff3cd; color: #9a6700; }
.badge-fix     { background: #ffd8d3; color: #82071e; }
.badge-feature { background: #d1f7dc; color: #116329; }
.badge-ci      { background: #e8eaed; color: #424a53; }
.badge-other   { background: #e8eaed; color: #424a53; }

/* ── other repos table ── */
.gh-other-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 13.5px;
  border: 1px solid #d0d7de;
  border-radius: 8px;
  overflow: hidden;
}
.gh-other-table th {
  background: #f6f8fa;
  border-bottom: 1px solid #d0d7de;
  padding: 9px 14px;
  text-align: left;
  font-size: 12px;
  font-weight: 600;
  color: #57606a;
  text-transform: uppercase;
  letter-spacing: .6px;
}
.gh-other-table td {
  padding: 10px 14px;
  border-bottom: 1px solid #f3f4f6;
  color: #1f2328;
  vertical-align: top;
}
.gh-other-table tr:last-child td { border-bottom: none; }
.gh-other-table tr:hover td { background: #f6f8fa; }
.gh-other-table a { color: #0969da; font-weight: 500; }
.gh-other-table a:hover { text-decoration: underline; }

/* ── personal repos ── */
.gh-repo-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-top: 4px;
}
@media (max-width: 600px) {
  .gh-repo-grid { grid-template-columns: 1fr; }
}
.repo-card {
  border: 1px solid #d0d7de;
  border-radius: 8px;
  padding: 16px;
  transition: border-color .2s, box-shadow .2s;
  background: #fff;
}
.repo-card:hover {
  border-color: #0969da;
  box-shadow: 0 2px 12px rgba(9,105,218,.1);
}
.repo-card-name {
  font-weight: 600;
  color: #0969da;
  font-size: 14px;
  margin-bottom: 5px;
}
.repo-card-name a { color: inherit; }
.repo-card-name a:hover { text-decoration: underline; }
.repo-card-desc {
  font-size: 12.5px;
  color: #57606a;
  line-height: 1.5;
  margin-bottom: 10px;
}
.repo-card-footer {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 12px;
  color: #57606a;
}
.repo-lang-dot {
  width: 10px; height: 10px;
  border-radius: 50%;
  display: inline-block;
  margin-right: 3px;
}
.lang-c      { background: #555; }
.lang-cpp    { background: #f34b7d; }
.lang-js     { background: #f1e05a; }
.lang-python { background: #3572A5; }
.star-count { display: flex; align-items: center; gap: 3px; }

/* ── footer note ── */
.gh-footer-note {
  text-align: center;
  color: #8c959f;
  font-size: 12px;
  font-family: 'JetBrains Mono', monospace;
  margin-top: 32px;
  padding-top: 20px;
  border-top: 1px dashed #d0d7de;
}
</style>

<div class="gh-wrap">

<!-- ══ HERO ══ -->
<div class="gh-hero">
  <div class="gh-hero-title">// open source</div>
  <div class="gh-hero-name">
    Jianghua Yang &nbsp;
    <a href="https://github.com/yjhjstz" target="_blank">@yjhjstz</a>
  </div>
  <div class="gh-stats">
    <div class="stat-card">
      <span class="stat-num" data-target="145">0</span>
      <span class="stat-label">合并 PR</span>
    </div>
    <div class="stat-card">
      <span class="stat-num blue" data-target="106">0</span>
      <span class="stat-label">PR Review</span>
    </div>
    <div class="stat-card">
      <span class="stat-num" data-target="98">0</span>
      <span class="stat-label">Commits</span>
    </div>
    <div class="stat-card">
      <span class="stat-num amber" data-target="11">0</span>
      <span class="stat-label">Issues</span>
    </div>
    <div class="stat-card">
      <span class="stat-num pink" data-target="4395">0</span>
      <span class="stat-label">⭐ deep-into-node</span>
    </div>
  </div>
</div>

<!-- ══ CLOUDBERRY PRs ══ -->
<div class="gh-section-header">
  <div class="gh-dot"></div>
  <h2>apache/cloudberry</h2>
  <span class="gh-count">100+ PRs</span>
</div>

<div class="gh-filters">
  <button class="gh-filter-btn active" data-filter="all">全部</button>
  <button class="gh-filter-btn" data-filter="orca">ORCA</button>
  <button class="gh-filter-btn" data-filter="storage">存储</button>
  <button class="gh-filter-btn" data-filter="feature">特性</button>
  <button class="gh-filter-btn" data-filter="fix">修复</button>
  <button class="gh-filter-btn" data-filter="tool">工具</button>
  <button class="gh-filter-btn" data-filter="ci">CI/CD</button>
</div>

<div class="gh-pr-list">

  <div class="gh-pr-item" data-cat="orca">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#8250df"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1573" target="_blank">ORCA: Fix window function cost model producing zero local cost when no ORDER BY</a></div>
      <div class="pr-meta"><span class="badge badge-orca">ORCA</span><span class="pr-repo">apache/cloudberry #1573</span><span class="pr-date">2026-02</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="orca">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#8250df"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1543" target="_blank">ORCA: Optimize CDatumSortedSet by checking IsSorted before sorting</a></div>
      <div class="pr-meta"><span class="badge badge-orca">ORCA</span><span class="pr-repo">apache/cloudberry #1543</span><span class="pr-date">2026-01</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="orca">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#8250df"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1533" target="_blank">ORCA: Fix memory leak in CWindowOids by adding destructor</a></div>
      <div class="pr-meta"><span class="badge badge-orca">ORCA</span><span class="pr-repo">apache/cloudberry #1533</span><span class="pr-date">2026-01</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="orca">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#8250df"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1392" target="_blank">ORCA: Fix segmentation fault when appending group statistics</a></div>
      <div class="pr-meta"><span class="badge badge-orca">ORCA</span><span class="pr-repo">apache/cloudberry #1392</span><span class="pr-date">2025-10</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="orca">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#8250df"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1360" target="_blank">ORCA: Prevent crashes with extension prosupport functions in NULL rtable queries</a></div>
      <div class="pr-meta"><span class="badge badge-orca">ORCA</span><span class="pr-repo">apache/cloudberry #1360</span><span class="pr-date">2025-09</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="storage">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#0969da"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1241" target="_blank">Fast analyze: implement fast ANALYZE for append-optimized tables</a></div>
      <div class="pr-meta"><span class="badge badge-storage">存储</span><span class="pr-repo">apache/cloudberry #1241</span><span class="pr-date">2025-08</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="storage">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#0969da"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1010" target="_blank">Optimize AOCS scan performance by introducing specialized no-qual path</a></div>
      <div class="pr-meta"><span class="badge badge-storage">存储</span><span class="pr-repo">apache/cloudberry #1010</span><span class="pr-date">2025-03</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="storage">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#0969da"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1025" target="_blank">Improve appendonly_getnextslot to optimize tuple retrieval</a></div>
      <div class="pr-meta"><span class="badge badge-storage">存储</span><span class="pr-repo">apache/cloudberry #1025</span><span class="pr-date">2025-03</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="feature">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#1a7f37"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/280" target="_blank">Incremental view maintenance（增量物化视图）</a></div>
      <div class="pr-meta"><span class="badge badge-feature">特性</span><span class="pr-repo">apache/cloudberry #280</span><span class="pr-date">2023-12</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="feature">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#1a7f37"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/647" target="_blank">Refactor parallel scan node and framework</a></div>
      <div class="pr-meta"><span class="badge badge-feature">特性</span><span class="pr-repo">apache/cloudberry #647</span><span class="pr-date">2024-10</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="tool">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#9a6700"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1170" target="_blank">gpfdist: add --compress-level option</a></div>
      <div class="pr-meta"><span class="badge badge-tool">工具</span><span class="pr-repo">apache/cloudberry #1170</span><span class="pr-date">2025-06</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="tool">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#9a6700"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1225" target="_blank">gpfdist: use event_base with libevent 2.0+ to avoid thread-unsafe event_init</a></div>
      <div class="pr-meta"><span class="badge badge-tool">工具</span><span class="pr-repo">apache/cloudberry #1225</span><span class="pr-date">2025-07</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="fix">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#cf222e"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1159" target="_blank">Fix use-after-free of viewQuery in ExecRefreshMatView</a></div>
      <div class="pr-meta"><span class="badge badge-fix">修复</span><span class="pr-repo">apache/cloudberry #1159</span><span class="pr-date">2025-06</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="fix">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#cf222e"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1196" target="_blank">Fix unable to map dynamic shared memory segment</a></div>
      <div class="pr-meta"><span class="badge badge-fix">修复</span><span class="pr-repo">apache/cloudberry #1196</span><span class="pr-date">2025-07</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="fix">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#cf222e"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1294" target="_blank">Fix: ERROR: too many sample rows received from gp_acquire_sample_rows</a></div>
      <div class="pr-meta"><span class="badge badge-fix">修复</span><span class="pr-repo">apache/cloudberry #1294</span><span class="pr-date">2025-08</span></div>
    </div>
  </div>

  <div class="gh-pr-item" data-cat="ci">
    <svg class="pr-icon" width="16" height="16" viewBox="0 0 16 16" fill="#57606a"><path d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5a1 1 0 01-1 1H4a1 1 0 01-1-1v-5a1 1 0 011-1h1V2.5H4a2.5 2.5 0 00-2.5 2.5v5A2.5 2.5 0 004 12.5h7a2.5 2.5 0 002.5-2.5v-5A2.5 2.5 0 0011 2.5z"/></svg>
    <div class="pr-body">
      <div class="pr-title"><a href="https://github.com/apache/cloudberry/pull/1016" target="_blank">CI: upload Cloudberry debuginfo RPM build artifacts</a></div>
      <div class="pr-meta"><span class="badge badge-ci">CI/CD</span><span class="pr-repo">apache/cloudberry #1016</span><span class="pr-date">2025-04</span></div>
    </div>
  </div>

</div>

<!-- ══ OTHER REPOS ══ -->
<div class="gh-section-header">
  <div class="gh-dot" style="background:#0969da"></div>
  <h2>其他开源贡献</h2>
</div>

<table class="gh-other-table">
  <thead>
    <tr><th>仓库</th><th>PR</th><th>描述</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://github.com/dbeaver/dbeaver/pull/37590" target="_blank">dbeaver/dbeaver</a></td>
      <td><span class="mono" style="font-size:12px">#37590</span></td>
      <td>Fix version extraction for Cloudberry and Apache Cloudberry</td>
    </tr>
    <tr>
      <td><a href="https://github.com/citusdata/pg_cron/pull/395" target="_blank">citusdata/pg_cron</a></td>
      <td><span class="mono" style="font-size:12px">#395</span></td>
      <td>Fix type mismatch in dsm_attach() argument by using DatumGetUInt32()</td>
    </tr>
    <tr>
      <td><a href="https://github.com/cloudberry-contrib/plcontainer" target="_blank">cloudberry-contrib/plcontainer</a></td>
      <td><span class="mono" style="font-size:12px">#1 #2 #6</span></td>
      <td>适配 Cloudberry 主线、修复 libcurl 链接、升级 json-c</td>
    </tr>
    <tr>
      <td><a href="https://github.com/apache/cloudberry-devops-release/pull/12" target="_blank">apache/cloudberry-devops-release</a></td>
      <td><span class="mono" style="font-size:12px">#12</span></td>
      <td>Add debuginfo package build support</td>
    </tr>
  </tbody>
</table>

<!-- ══ PERSONAL PROJECTS ══ -->
<div class="gh-section-header">
  <div class="gh-dot" style="background:#e3b341"></div>
  <h2>个人代表项目</h2>
</div>

<div class="gh-repo-grid">
  <div class="repo-card">
    <div class="repo-card-name"><a href="https://github.com/yjhjstz/deep-into-node" target="_blank">deep-into-node</a></div>
    <div class="repo-card-desc">深入理解 Node.js：核心思想与源码分析。系统讲解事件循环、V8、libuv 等底层机制。</div>
    <div class="repo-card-footer">
      <span><span class="repo-lang-dot lang-js"></span>JavaScript</span>
      <span class="star-count">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="#e3b341"><path d="M8 .25a.75.75 0 01.673.418l1.882 3.815 4.21.612a.75.75 0 01.416 1.279l-3.046 2.97.719 4.192a.751.751 0 01-1.088.791L8 12.347l-3.766 1.98a.75.75 0 01-1.088-.79l.72-4.194L.818 6.374a.75.75 0 01.416-1.28l4.21-.611L7.327.668A.75.75 0 018 .25z"/></svg>
        4,395
      </span>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-card-name"><a href="https://github.com/yjhjstz/postgres-xl-docker" target="_blank">postgres-xl-docker</a></div>
    <div class="repo-card-desc">分布式图数据库 POC，基于 Postgres-XL，支持 OpenCypher 语法、向量与地理位置融合查询。</div>
    <div class="repo-card-footer">
      <span><span class="repo-lang-dot lang-python"></span>Python</span>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-card-name"><a href="https://github.com/yjhjstz/mempool" target="_blank">mempool</a></div>
    <div class="repo-card-desc">nginx-like 内存池实现，轻量高效的 C 语言内存管理组件。</div>
    <div class="repo-card-footer">
      <span><span class="repo-lang-dot lang-c"></span>C</span>
      <span class="star-count">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="#e3b341"><path d="M8 .25a.75.75 0 01.673.418l1.882 3.815 4.21.612a.75.75 0 01.416 1.279l-3.046 2.97.719 4.192a.751.751 0 01-1.088.791L8 12.347l-3.766 1.98a.75.75 0 01-1.088-.79l.72-4.194L.818 6.374a.75.75 0 01.416-1.28l4.21-.611L7.327.668A.75.75 0 018 .25z"/></svg>
        4
      </span>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-card-name"><a href="https://github.com/yjhjstz/pandorabox" target="_blank">pandorabox</a></div>
    <div class="repo-card-desc">路由器固件定制，适用于小型 MIPS 路由器设备。</div>
    <div class="repo-card-footer">
      <span><span class="repo-lang-dot lang-c"></span>C</span>
      <span class="star-count">
        <svg width="14" height="14" viewBox="0 0 16 16" fill="#e3b341"><path d="M8 .25a.75.75 0 01.673.418l1.882 3.815 4.21.612a.75.75 0 01.416 1.279l-3.046 2.97.719 4.192a.751.751 0 01-1.088.791L8 12.347l-3.766 1.98a.75.75 0 01-1.088-.79l.72-4.194L.818 6.374a.75.75 0 01.416-1.28l4.21-.611L7.327.668A.75.75 0 018 .25z"/></svg>
        9
      </span>
    </div>
  </div>
</div>

<div class="gh-footer-note">
  // data via GitHub API &nbsp;·&nbsp; last updated 2026-03
</div>

</div><!-- .gh-wrap -->

<script>
(function(){
  // ── count-up animation ──
  function countUp(el, target, duration) {
    var start = 0;
    var step = target / (duration / 16);
    var timer = setInterval(function(){
      start += step;
      if (start >= target) { start = target; clearInterval(timer); }
      el.textContent = Math.floor(start).toLocaleString();
    }, 16);
  }
  var nums = document.querySelectorAll('.stat-num[data-target]');
  var triggered = false;
  function maybeAnimate() {
    if (triggered) return;
    var hero = document.querySelector('.gh-hero');
    if (!hero) return;
    var rect = hero.getBoundingClientRect();
    if (rect.top < window.innerHeight) {
      triggered = true;
      nums.forEach(function(el){
        countUp(el, parseInt(el.dataset.target), 1000);
      });
    }
  }
  window.addEventListener('scroll', maybeAnimate, {passive:true});
  maybeAnimate();

  // ── filter tabs ──
  var btns = document.querySelectorAll('.gh-filter-btn');
  btns.forEach(function(btn){
    btn.addEventListener('click', function(){
      btns.forEach(function(b){ b.classList.remove('active'); });
      btn.classList.add('active');
      var f = btn.dataset.filter;
      document.querySelectorAll('.gh-pr-item').forEach(function(item){
        if (f === 'all' || item.dataset.cat === f) {
          item.setAttribute('data-hide', 'false');
          item.style.display = '';
        } else {
          item.setAttribute('data-hide', 'true');
          item.style.display = 'none';
        }
      });
    });
  });
})();
</script>
