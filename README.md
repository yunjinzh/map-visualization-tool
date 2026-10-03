@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

:root {
  font-family: 'Inter', sans-serif;
  color: #e5eefb;
  background: #09111f;
  line-height: 1.5;
  font-weight: 400;
  --bg: #09111f;
  --panel: rgba(15, 23, 42, 0.82);
  --panel-strong: rgba(15, 23, 42, 0.96);
  --border: rgba(148, 163, 184, 0.18);
  --text: #e2e8f0;
  --muted: #94a3b8;
  --blue: #4da3ff;
  --green: #38d39f;
  --orange: #f9b84f;
  --purple: #b88cff;
}

* {
  box-sizing: border-box;
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  min-width: 0;
  background: radial-gradient(circle at top, #122545 0%, var(--bg) 52%);
}

body {
  min-height: 100vh;
  color: var(--text);
}

button {
  font: inherit;
}

.page-shell {
  display: grid;
  grid-template-columns: 320px minmax(0, 1fr);
  min-height: 100vh;
  gap: 20px;
  padding: 24px;
}

.panel {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 20px;
  backdrop-filter: blur(6px);
  box-shadow: 0 18px 24px rgba(15, 23, 42, 0.22);
}

.sidebar {
  padding: 22px 18px;
  display: flex;
  flex-direction: column;
  gap: 22px;
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 8px 6px 16px;
}

.brand-icon {
  width: 42px;
  height: 42px;
  border-radius: 14px;
  display: grid;
  place-items: center;
  background: linear-gradient(135deg, var(--blue), var(--purple));
  font-weight: 800;
  color: white;
}

.eyebrow {
  margin: 0 0 4px;
  font-size: 11px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--muted);
}

.brand-block h1,
.topbar h2,
.detail-header h3,
.card-title-row h3 {
  margin: 0;
}

.filter-group {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.section-label {
  margin: 0;
  color: var(--muted);
  font-size: 12px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.filter-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.filter-button {
  border: 1px solid var(--border);
  background: rgba(148, 163, 184, 0.04);
  color: var(--text);
  border-radius: 10px;
  padding: 8px 12px;
  transition: all 0.2s ease;
  cursor: pointer;
}

.filter-button:hover,
.filter-button.active {
  background: rgba(77, 163, 255, 0.12);
  border-color: rgba(77, 163, 255, 0.55);
  color: white;
}

.stats-card {
  padding: 16px;
  background: rgba(148, 163, 184, 0.04);
  border: 1px solid var(--border);
  border-radius: 16px;
}

.stats-card.compact {
  padding: 14px 16px;
}

.stats-header {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 10px;
  color: var(--muted);
  font-size: 12px;
}

.stats-card strong {
  display: block;
  font-size: 28px;
  margin-bottom: 4px;
}

.stats-card small {
  color: var(--muted);
}

.mini-icon,
.metric-icon {
  display: grid;
  place-items: center;
  border-radius: 10px;
  color: white;
}

.mini-icon {
  width: 26px;
  height: 26px;
}

.metric-icon {
  width: 42px;
  height: 42px;
}

.mini-icon.blue,
.metric-icon.blue { background: rgba(77, 163, 255, 0.24); color: var(--blue); }
.mini-icon.purple { background: rgba(184, 140, 255, 0.2); color: var(--purple); }
.metric-icon.green { background: rgba(56, 211, 159, 0.18); color: var(--green); }
.metric-icon.orange { background: rgba(249, 184, 79, 0.18); color: var(--orange); }

.main-panel {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 22px 24px;
}

.topbar-meta {
  display: flex;
  align-items: center;
  gap: 12px;
}

.badge {
  display: inline-flex;
  align-items: center;
  height: 32px;
  padding: 0 12px;
  border-radius: 999px;
  background: rgba(56, 211, 159, 0.1);
  border: 1px solid rgba(56, 211, 159, 0.2);
  color: var(--green);
  font-size: 12px;
}

.badge.neutral {
  color: var(--muted);
  background: rgba(148, 163, 184, 0.06);
  border-color: rgba(148, 163, 184, 0.1);
}

.primary-button {
  border: none;
  border-radius: 10px;
  background: linear-gradient(135deg, var(--blue), #7ba8ff);
  color: white;
  padding: 10px 16px;
  cursor: pointer;
  font-weight: 600;
}

.metric-row {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.metric-card {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 18px 20px;
}

.metric-card p {
  margin: 0 0 4px;
  color: var(--muted);
  font-size: 12px;
}

.metric-card strong {
  font-size: 28px;
}

.content-grid {
  display: grid;
  grid-template-columns: minmax(0, 2fr) minmax(260px, 0.8fr);
  gap: 18px;
}

.map-panel,
.detail-panel,
.chart-card,
.list-card {
  padding: 16px;
}

.map-view {
  height: 520px;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid rgba(148, 163, 184, 0.12);
}

.detail-panel {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.detail-header {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  align-items: flex-start;
}

.status-tag {
  display: inline-flex;
  align-items: center;
  border-radius: 999px;
  padding: 7px 10px;
  font-size: 12px;
  border: 1px solid rgba(148, 163, 184, 0.18);
  white-space: nowrap;
}

.detail-metrics {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-top: 20px;
}

.detail-metrics div {
  padding: 12px 10px;
  border-radius: 12px;
  background: rgba(148, 163, 184, 0.04);
  border: 1px solid var(--border);
}

.detail-metrics small {
  display: block;
  color: var(--muted);
  margin-bottom: 6px;
}

.detail-copy {
  color: #dfeafc;
  margin-top: 20px;
  line-height: 1.7;
}

.legend-list {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 12px;
  margin-top: 22px;
  color: var(--muted);
}

.legend-list div {
  display: flex;
  align-items: center;
  gap: 8px;
}

.legend-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  display: inline-block;
}

.legend-dot.retail { background: var(--blue); }
.legend-dot.logistics { background: var(--green); }
.legend-dot.transit { background: var(--orange); }
.legend-dot.service { background: var(--purple); }

.bottom-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.3fr) minmax(260px, 0.7fr);
  gap: 18px;
}

.card-title-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 12px;
}

.site-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.site-item {
  cursor: pointer;
  border: 1px solid var(--border);
  border-radius: 14px;
  padding: 12px 14px;
  background: rgba(148, 163, 184, 0.03);
  transition: all 0.2s ease;
}

.site-item:hover,
.site-item.active {
  border-color: rgba(77, 163, 255, 0.4);
  background: rgba(77, 163, 255, 0.08);
}

.site-item__head,
.site-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
}

.site-meta {
  margin-top: 10px;
  color: var(--muted);
  font-size: 12px;
}

.site-name {
  font-weight: 600;
}

.site-badge {
  display: inline-flex;
  align-items: center;
  border-radius: 999px;
  padding: 5px 8px;
  font-size: 10px;
  font-weight: 600;
}

.popup-card {
  min-width: 150px;
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.popup-card strong {
  font-size: 15px;
}

.popup-card span,
.popup-card p,
.popup-card small {
  color: #475569;
}

@media (max-width: 1100px) {
  .page-shell {
    grid-template-columns: 1fr;
  }

  .sidebar {
    order: 2;
  }

  .main-panel {
    order: 1;
  }
}

@media (max-width: 760px) {
  .page-shell {
    padding: 16px;
  }

  .metric-row,
  .content-grid,
  .bottom-grid {
    grid-template-columns: 1fr;
  }

  .topbar {
    flex-direction: column;
    align-items: flex-start;
    gap: 12px;
  }

  .topbar-meta {
    width: 100%;
    justify-content: space-between;
  }
}
