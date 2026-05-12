# Build the interactive HTML dashboard
# All data embedded, single file, no dependencies except CDN Chart.js

HTML = r'''<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Claims Tracker — Mann-Grandstaff VAMC FY2026</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap');

  :root {
    --navy: #0f2444;
    --navy2: #1a3560;
    --teal: #1a7fa8;
    --teal2: #22a8db;
    --gold: #c9922a;
    --gold2: #f0b53f;
    --green: #1a7a4a;
    --green-bg: #e8f7ee;
    --red: #c0392b;
    --red-bg: #fdecea;
    --amber: #d97706;
    --amber-bg: #fef3c7;
    --bg: #f0f4f9;
    --card: #ffffff;
    --border: #dde3ed;
    --text: #1a2640;
    --muted: #6b7a99;
    --stripe: #f7f9fc;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--text); font-size: 13px; }

  /* ── HEADER ── */
  .header {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy2) 100%);
    padding: 14px 24px;
    display: flex; align-items: center; justify-content: space-between;
    box-shadow: 0 2px 12px rgba(0,0,0,0.25);
    position: sticky; top: 0; z-index: 100;
  }
  .header-left h1 { font-size: 15px; font-weight: 700; color: #fff; letter-spacing: 0.02em; }
  .header-left p  { font-size: 11px; color: rgba(255,255,255,0.55); margin-top: 1px; font-family: 'DM Mono', monospace; }
  .header-right { font-size: 11px; color: rgba(255,255,255,0.5); font-family: 'DM Mono', monospace; }

  /* ── TAB BAR ── */
  .tabbar {
    background: var(--navy);
    display: flex; gap: 2px; padding: 0 24px;
    border-bottom: 2px solid var(--teal);
  }
  .tab {
    padding: 9px 18px; font-size: 12px; font-weight: 600; color: rgba(255,255,255,0.5);
    cursor: pointer; border-bottom: 3px solid transparent; margin-bottom: -2px;
    transition: all 0.15s; letter-spacing: 0.03em; white-space: nowrap;
  }
  .tab:hover { color: rgba(255,255,255,0.85); }
  .tab.active { color: var(--teal2); border-bottom-color: var(--teal2); }

  /* ── MONTH PICKER ── */
  .month-bar {
    background: var(--card); border-bottom: 1px solid var(--border);
    padding: 8px 24px; display: flex; gap: 6px; align-items: center;
    overflow-x: auto;
  }
  .month-bar label { font-size: 11px; font-weight: 600; color: var(--muted); margin-right: 4px; white-space: nowrap; }
  .mbtn {
    padding: 5px 14px; border-radius: 20px; font-size: 11px; font-weight: 600;
    border: 1.5px solid var(--border); background: transparent; color: var(--muted);
    cursor: pointer; transition: all 0.15s; white-space: nowrap;
  }
  .mbtn:hover { border-color: var(--teal); color: var(--teal); }
  .mbtn.active { background: var(--teal); border-color: var(--teal); color: #fff; }
  .mbtn.ytd { background: var(--navy); border-color: var(--navy); color: #fff; }
  .mbtn.ytd.active { background: var(--gold); border-color: var(--gold); }

  /* ── MAIN CONTENT ── */
  .content { padding: 16px 24px; max-width: 1400px; margin: 0 auto; }

  /* ── STAT CARDS ── */
  .stat-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 10px; margin-bottom: 16px; }
  .stat-card {
    background: var(--card); border: 1px solid var(--border); border-radius: 10px;
    padding: 12px 16px; position: relative; overflow: hidden;
  }
  .stat-card::before { content:''; position:absolute; top:0; left:0; right:0; height:3px; background: var(--teal); }
  .stat-card.gold::before { background: var(--gold); }
  .stat-card.green::before { background: var(--green); }
  .stat-card.navy::before { background: var(--navy); }
  .stat-label { font-size: 10px; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; }
  .stat-val { font-size: 26px; font-weight: 700; color: var(--navy); line-height: 1.1; margin: 4px 0 2px; font-family: 'DM Mono', monospace; }
  .stat-sub { font-size: 10px; color: var(--muted); }

  /* ── TABLES ── */
  .card { background: var(--card); border: 1px solid var(--border); border-radius: 10px; overflow: hidden; margin-bottom: 16px; }
  .card-title { padding: 10px 16px; font-size: 12px; font-weight: 700; color: var(--navy); border-bottom: 1px solid var(--border); display: flex; align-items: center; gap: 8px; background: var(--stripe); }
  table { width: 100%; border-collapse: collapse; }
  th { padding: 8px 12px; text-align: center; font-size: 10px; font-weight: 700; color: #fff; background: var(--navy); text-transform: uppercase; letter-spacing: 0.05em; white-space: nowrap; }
  th.left { text-align: left; }
  td { padding: 7px 12px; text-align: center; border-bottom: 1px solid var(--border); font-size: 12px; color: var(--text); }
  td.left { text-align: left; font-weight: 600; }
  tr:last-child td { border-bottom: none; }
  tr:nth-child(even) td { background: var(--stripe); }
  tr.total-row td { background: var(--navy) !important; color: #fff !important; font-weight: 700; }
  .num { font-family: 'DM Mono', monospace; }
  .dash { color: var(--border); }

  /* ── BADGES ── */
  .badge-met  { background: var(--green-bg); color: var(--green); padding: 2px 8px; border-radius: 12px; font-size: 11px; font-weight: 700; white-space: nowrap; }
  .badge-miss { background: var(--red-bg);   color: var(--red);   padding: 2px 8px; border-radius: 12px; font-size: 11px; font-weight: 700; white-space: nowrap; }
  .badge-warn { background: var(--amber-bg); color: var(--amber); padding: 2px 8px; border-radius: 12px; font-size: 11px; font-weight: 700; white-space: nowrap; }
  .badge-ref  { background: #f0f4f9; color: var(--muted); padding: 2px 8px; border-radius: 12px; font-size: 11px; }

  /* ── MEDAL ── */
  .medal { font-size: 16px; }

  /* ── PERF NOTES ── */
  .perf-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .perf-card { background: var(--card); border: 1px solid var(--border); border-radius: 10px; overflow: hidden; }
  .perf-head { padding: 10px 14px; background: var(--navy); color: #fff; font-weight: 700; font-size: 13px; display:flex; justify-content:space-between; align-items:center; }
  .perf-body { padding: 12px 14px; display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .perf-section h4 { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.07em; color: var(--muted); margin-bottom: 6px; }
  .perf-section p  { font-size: 11px; line-height: 1.6; color: var(--text); }
  .perf-section ul { padding-left: 14px; }
  .perf-section li { font-size: 11px; line-height: 1.7; color: var(--text); }
  .perf-stats { display:flex; gap:12px; padding: 8px 14px; background: var(--stripe); border-top: 1px solid var(--border); }
  .ps { text-align:center; }
  .ps-val { font-size:18px; font-weight:700; color:var(--navy); font-family:'DM Mono',monospace; }
  .ps-lbl { font-size:10px; color:var(--muted); font-weight:600; }

  /* ── CHART CONTAINER ── */
  .chart-wrap { padding: 16px; }
  .charts-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }

  /* ── HIDDEN ── */
  .panel { display: none; }
  .panel.active { display: block; }

  /* ── PROGRESS BAR ── */
  .prog-bar { height: 6px; background: var(--border); border-radius: 3px; overflow: hidden; margin-top: 4px; }
  .prog-fill { height: 100%; border-radius: 3px; background: var(--teal); transition: width 0.4s; }
</style>
</head>
<body>

<div class="header">
  <div class="header-left">
    <h1>Claims Processing Tracker — Mann-Grandstaff VAMC</h1>
    <p>FY2026 &nbsp;·&nbsp; Oct 2025 – Present &nbsp;·&nbsp; Last Modified: Claims data</p>
  </div>
  <div class="header-right">Mann-Grandstaff Dept of Veterans Affairs Medical Center</div>
</div>

<div class="tabbar">
  <div class="tab active" onclick="switchTab('summary')">📊 Summary</div>
  <div class="tab" onclick="switchTab('weekly')">📅 Weekly Detail</div>
  <div class="tab" onclick="switchTab('leaderboard')">🏆 Leaderboard</div>
  <div class="tab" onclick="switchTab('threshold')">⚠️ 90% Threshold</div>
  <div class="tab" onclick="switchTab('charts')">📈 Charts</div>
  <div class="tab" onclick="switchTab('notes')">📝 Performance Notes</div>
</div>

<div class="month-bar">
  <label>MONTH:</label>
  <button class="mbtn" onclick="setMonth('Oct 2025')">Oct 2025</button>
  <button class="mbtn" onclick="setMonth('Nov 2025')">Nov 2025</button>
  <button class="mbtn" onclick="setMonth('Dec 2025')">Dec 2025</button>
  <button class="mbtn" onclick="setMonth('Jan 2026')">Jan 2026</button>
  <button class="mbtn" onclick="setMonth('Feb 2026')">Feb 2026</button>
  <button class="mbtn" onclick="setMonth('Mar 2026')">Mar 2026</button>
  <button class="mbtn" onclick="setMonth('Apr 2026')">Apr 2026</button>
  <button class="mbtn active" onclick="setMonth('May 2026')">May 2026</button>
  <button class="mbtn ytd active-ytd" onclick="setMonth('YTD')">YTD</button>
</div>

<div class="content">
  <div id="panel-summary"    class="panel active"></div>
  <div id="panel-weekly"     class="panel"></div>
  <div id="panel-leaderboard" class="panel"></div>
  <div id="panel-threshold"  class="panel"></div>
  <div id="panel-charts"     class="panel"></div>
  <div id="panel-notes"      class="panel"></div>
</div>

<script>
// ════════════════════════════════════════════════════════════
// DATA
// ════════════════════════════════════════════════════════════
const CORE = ["Thomas Banks","Tony Vaughn","Trent Crabtree","Richard Smith","Kelly Young","Alyson Atwater","Dakota Hackworth"];
const MONTHS = ["Oct 2025","Nov 2025","Dec 2025","Jan 2026","Feb 2026","Mar 2026","Apr 2026","May 2026"];

const DATA = {
  "Oct 2025": {
    weeks: ["Oct 5-11","Oct 12-18","Oct 19-25","Oct 26-Nov1"],
    wd:    [5,4,5,5],
    modified: {
      "Thomas Banks":     [0,0,0,0],
      "Tony Vaughn":      [13,45,114,9],
      "Trent Crabtree":   [161,88,148,36],
      "Richard Smith":    [7,22,28,164],
      "Kelly Young":      [284,82,405,164],
      "Alyson Atwater":   [0,0,0,0],
      "Dakota Hackworth": [0,0,0,0],
    }, others_m:[5,5,149,0]
  },
  "Nov 2025": {
    weeks: ["Nov 2-8","Nov 9-15","Nov 16-22","Nov 23-29"],
    wd:    [5,4,5,4],
    modified: {
      "Thomas Banks":     [0,0,0,0],
      "Tony Vaughn":      [44,12,67,103],
      "Trent Crabtree":   [89,75,51,15],
      "Richard Smith":    [2,0,0,0],
      "Kelly Young":      [109,8,28,2],
      "Alyson Atwater":   [0,0,23,0],
      "Dakota Hackworth": [0,0,0,0],
    }, others_m:[1,16,82,18]
  },
  "Dec 2025": {
    weeks: ["Dec 7-13","Dec 14-20","Dec 21-27"],
    wd:    [5,5,4],
    modified: {
      "Thomas Banks":     [0,0,0],
      "Tony Vaughn":      [216,56,131],
      "Trent Crabtree":   [111,65,23],
      "Richard Smith":    [2,0,29],
      "Kelly Young":      [0,0,0],
      "Alyson Atwater":   [0,0,0],
      "Dakota Hackworth": [0,0,0],
    }, others_m:[27,43,6]
  },
  "Jan 2026": {
    weeks: ["Jan 1-3","Jan 4-10","Jan 11-17","Jan 18-24","Jan 25-31"],
    wd:    [4,5,5,4,5],
    modified: {
      "Thomas Banks":     [0,0,0,0,151],
      "Tony Vaughn":      [414,300,338,242,43],
      "Trent Crabtree":   [71,104,105,37,149],
      "Richard Smith":    [9,17,162,18,98],
      "Kelly Young":      [2,2,2,1,96],
      "Alyson Atwater":   [0,0,0,0,0],
      "Dakota Hackworth": [0,0,0,0,0],
    }, others_m:[10,32,44,4,2]
  },
  "Feb 2026": {
    weeks: ["Feb 1-7","Feb 8-14","Feb 15-21","Feb 22-28"],
    wd:    [5,5,4,5],
    modified: {
      "Thomas Banks":     [221,147,197,66],
      "Tony Vaughn":      [154,242,211,127],
      "Trent Crabtree":   [184,417,72,161],
      "Richard Smith":    [31,183,9,27],
      "Kelly Young":      [45,5,5,6],
      "Alyson Atwater":   [34,2,0,0],
      "Dakota Hackworth": [0,0,0,0],
    }, others_m:[4,10,43,49]
  },
  "Mar 2026": {
    weeks: ["Mar 1-6","Mar 8-14","Mar 15-21","Mar 22-28","Mar 29-31"],
    wd:    [5,5,5,5,3],
    modified: {
      "Thomas Banks":     [144,244,223,342,41],
      "Tony Vaughn":      [227,138,257,121,51],
      "Trent Crabtree":   [115,235,130,194,88],
      "Richard Smith":    [44,35,17,25,8],
      "Kelly Young":      [20,100,107,75,0],
      "Alyson Atwater":   [0,0,0,0,0],
      "Dakota Hackworth": [0,0,170,105,50],
    }, others_m:[52,67,90,84,0]
  },
  "Apr 2026": {
    weeks: ["Apr 1-4","Apr 5-11","Apr 12-18","Apr 19-24","Apr 28-30"],
    wd:    [4,5,5,5,3],
    modified: {
      "Thomas Banks":     [93,123,137,163,102],
      "Tony Vaughn":      [118,124,169,144,123],
      "Trent Crabtree":   [91,281,209,287,115],
      "Richard Smith":    [6,49,49,20,0],
      "Kelly Young":      [1,13,1,1,0],
      "Alyson Atwater":   [0,0,0,0,0],
      "Dakota Hackworth": [113,174,294,186,155],
    }, others_m:[0,35,43,5,0]
  },
  "May 2026": {
    weeks: ["May 1-2","May 4-9"],
    wd:    [2,5],
    modified: {
      "Thomas Banks":     [50,712],
      "Tony Vaughn":      [64,121],
      "Trent Crabtree":   [99,323],
      "Richard Smith":    [0,22],
      "Kelly Young":      [5,4],
      "Alyson Atwater":   [0,0],
      "Dakota Hackworth": [89,139],
    }, others_m:[16,31]
  }
};

const PERF_NOTES = {
  "Thomas Banks": {
    strengths: ["YTD leader in claims created (paper queue). Took ownership of paper backlog from Jan 2026.", "Consistent daily producer — strong FY2026 Q2 performance with 631 modified in Feb and 953 in Mar.", "Primary driver of paper backlog reduction across the team."],
    development: ["Claims Modified volume lower in Q1 — opportunity to build more balanced processing profile.", "Ensure throughput maintained as paper backlog decreases and work type shifts."],
    goals: ["Target 50+ avg/day for Apr 2026. Begin cross-training on modified workflow. Maintain paper queue leadership through backlog clearance."]
  },
  "Tony Vaughn": {
    strengths: ["Highest community claims volume on team. Strong ownership of complex ongoing modifications.", "Consistent daily output across FY2026. Clear leader in Q1 FY2026 (Oct-Dec 2025).", "1,337 modified in Jan 2026 — exceptional single-month performance."],
    development: ["Week-over-week consistency shows dips at month-end — warrants monitoring.", "March volume lower vs Feb — review workload distribution and case pipeline."],
    goals: ["Maintain avg/day at or above 35. Sustain 90% monthly threshold pass rate. Target consistent volume across all 4 weeks of each month."]
  },
  "Trent Crabtree": {
    strengths: ["Highest Claims Modified ceiling on team. Deep expertise in modification workflow and complex claims.", "Outstanding Feb 2026 performance — 834 modified, highest single-month on the team.", "Strong Q2 FY2026 contributor. 674 modified in Mar 2026."],
    development: ["Significant week-to-week volume variation — standout weeks alongside sharp dips.", "Pacing and consistent throughput are primary development areas. Reduce threshold misses."],
    goals: ["Establish weekly minimum floor. Target 90% monthly threshold met every month. Reduce variance between best and lowest weeks."]
  },
  "Richard Smith": {
    strengths: ["Supervisor/lead role — volume reflects dual processing and supervisory responsibilities.", "Strong Jan 2026 performance (304 modified) demonstrating processing capability.", "Consistent presence in data across multiple months — reliable team anchor."],
    development: ["Lower raw volume reflects supervisory duties. Document supervisory contributions separately for full performance picture.", "Establish clear processing targets that account for supervisory time allocation."],
    goals: ["Define monthly processing targets accounting for supervisory hours. Document team oversight contributions for review period. Maintain active processing role."]
  },
  "Kelly Young": {
    strengths: ["Exceptional Q1 FY2026 performance — 935 modified in Oct 2025 alone.", "Strong reengagement in Feb-Mar 2026 showing renewed consistency.", "High-capacity processor when fully active — demonstrated ceiling is among the team's best."],
    development: ["Activity gaps across several months (Nov, Dec, Jan minimal output) need documentation.", "Consistency between months is the primary development area — capacity is not the issue."],
    goals: ["Maintain consistent weekly activity — no zero-output weeks. Build toward full-month consistency every month. Document any absences or reduced-duty periods."]
  },
  "Alyson Atwater": {
    strengths: ["Active contributor in Oct-Feb period. Showed solid productivity in Nov 2025.", "Cross-trained on both created and modified workflows."],
    development: ["No recorded activity from Mar 2026 onward — status should be confirmed with supervisor.", "Earlier months show capacity that has not been sustained through Q2 FY2026."],
    goals: ["Confirm current role and assignment status. If active, re-establish processing targets and weekly minimums. Provide explanation for activity gaps."]
  },
  "Dakota Hackworth": {
    strengths: ["Strong entry into tracked processing — 275 modified in first partial month (Mar 15-28).", "Immediate contributor to paper/created queue. High-capacity first two weeks.", "Ramp-up trajectory suggests strong performance ahead."],
    development: ["Insufficient data for full development analysis — first full month (Apr 2026) will establish baseline.", "90% threshold tracking begins Apr 2026. Focus on consistency from the start."],
    goals: ["Complete first full tracked month (Apr 2026). Establish baseline avg/day. Target 90% monthly threshold from first full month. Aim for 300+ modified in first full month."]
  }
};

// ════════════════════════════════════════════════════════════
// HELPERS
// ════════════════════════════════════════════════════════════
let currentMonth = "Mar 2026";
let currentTab   = "summary";
let chartInstances = {};

function modTotal(mo, name) {
  return (DATA[mo]?.modified[name] || []).reduce((a,b)=>a+b,0);
}
function ytdTotal(name) {
  return MONTHS.reduce((s,m)=>s+modTotal(m,name),0);
}
function activeDays(mo, name) {
  const v=DATA[mo]?.modified[name]||[], w=DATA[mo]?.wd||[];
  return v.reduce((s,x,i)=>s+(x>0?w[i]:0),0);
}
function ytdActiveDays(name) {
  return MONTHS.reduce((s,m)=>s+activeDays(m,name),0);
}
function avgDay(mo, name) {
  const ad=activeDays(mo,name), t=modTotal(mo,name);
  return ad>0 ? (t/ad).toFixed(1) : "—";
}

// Avg/day: exact day counts from daily columns in source images where known.
// Unknown weeks default to 5 days if output > 0.
// Exact days worked from daily image columns — zero means day off.
// Mar 8-14: Tony=4. Mar 29-31: Thomas=1,Tony=1,Trent=2,Dakota=2.
// Apr 1-4: Thomas=4,Tony=3,Trent=3,Dakota=3. Apr 5-11: Thomas=4,Tony=3,Trent=5,Dakota=5.
// Apr 12-18: Thomas=5,Tony=5,Trent=5,Dakota=5. Apr 19-24: Thomas=5,Tony=3,Trent=5,Dakota=5.
// Apr 28-30: Thomas=3,Tony=3,Trent=3,Dakota=3. May 1-2: Thomas=2,Tony=2,Trent=2,Dakota=2.
// May 4-9: Thomas=5,Tony=5,Trent=5,Dakota=5.
const FIXED_AVG = {
  "Thomas Banks":   { total: 3005, days: 69, label: "Feb 1–May 9" },
  "Tony Vaughn":    { total: 2391, days: 64, label: "Feb 1–May 9" },
  "Trent Crabtree": { total: 3001, days: 70, label: "Feb 1–May 9" },
  "Dakota Hackworth":{ total: 1475, days: 40, label: "Mar 15–May 9" },
};
function activeWeeks(mo, name) {
  return (DATA[mo]?.modified[name]||[]).filter(v=>v>0).length;
}
function ytdActiveWeeks(name) {
  return MONTHS.reduce((s,m)=>s+activeWeeks(m,name),0);
}
function perfAvgDay(name) {
  if (FIXED_AVG[name]) return (FIXED_AVG[name].total / FIXED_AVG[name].days).toFixed(1);
  const wks=ytdActiveWeeks(name), t=ytdTotal(name);
  return wks>0 ? (t/(wks*5)).toFixed(1) : "—";
}
function perfAvgLabel(name) {
  return FIXED_AVG[name] ? `since ${FIXED_AVG[name].label}` : "active weeks × 5 days";
}
function ytdAvgDay(name) {
  const wks=ytdActiveWeeks(name), t=ytdTotal(name);
  return wks>0 ? (t/(wks*5)).toFixed(1) : "—";
}
function avgDay(mo, name) {
  const wks=activeWeeks(mo,name), t=modTotal(mo,name);
  return wks>0 ? (t/(wks*5)).toFixed(1) : "—";
}
function fmt(n) { return n>0 ? n.toLocaleString() : '<span class="dash">—</span>'; }
function pct(a,b) { return b>0 ? Math.round(a/b*100) : 0; }

// ════════════════════════════════════════════════════════════
// NAVIGATION
// ════════════════════════════════════════════════════════════
function switchTab(tab) {
  currentTab = tab;
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
  event.target.classList.add('active');
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));
  document.getElementById('panel-'+tab).classList.add('active');
  renderPanel(tab);
}

function setMonth(mo) {
  currentMonth = mo;
  document.querySelectorAll('.mbtn').forEach(b=>b.classList.remove('active'));
  event.target.classList.add('active');
  renderPanel(currentTab);
}

// ════════════════════════════════════════════════════════════
// RENDERERS
// ════════════════════════════════════════════════════════════
function renderPanel(tab) {
  if (tab==='summary')    renderSummary();
  if (tab==='weekly')     renderWeekly();
  if (tab==='leaderboard') renderLeaderboard();
  if (tab==='threshold')  renderThreshold();
  if (tab==='charts')     renderCharts();
  if (tab==='notes')      renderNotes();
}

// ── SUMMARY ──────────────────────────────────────────────────
function renderSummary() {
  const isYTD = currentMonth==='YTD';
  const months = isYTD ? MONTHS : [currentMonth];
  const label = isYTD ? 'YTD FY2026' : currentMonth;

  let grandTotal=0, grandDays=0;
  CORE.forEach(n=>{ grandTotal+=isYTD?ytdTotal(n):modTotal(currentMonth,n); grandDays+=isYTD?ytdActiveDays(n):activeDays(currentMonth,n); });

  const topProducer = CORE.reduce((best,n)=>{
    const t=isYTD?ytdTotal(n):modTotal(currentMonth,n);
    return t>(isYTD?ytdTotal(best):modTotal(currentMonth,best))?n:best;
  }, CORE[0]);

  const otherTotal = months.reduce((s,m)=>s+DATA[m].others_m.reduce((a,b)=>a+b,0),0);
  const teamTotal = grandTotal + otherTotal;

  let rows = CORE.map(n=>{
    const t = isYTD?ytdTotal(n):modTotal(currentMonth,n);
    const avg = isYTD?ytdAvgDay(n):avgDay(currentMonth,n);
    return `<tr>
      <td class="left">${n}</td>
      <td class="num">${fmt(t)}</td>
      <td class="num">${avg!=="—"?avg:"—"}</td>
      ${months.map(m=>`<td class="num">${fmt(modTotal(m,n))}</td>`).join('')}
    </tr>`;
  }).join('');

  const moCols = isYTD ? MONTHS.map(m=>`<th>${m}</th>`).join('') : '';

  document.getElementById('panel-summary').innerHTML = `
    <div class="stat-row">
      <div class="stat-card"><div class="stat-label">Team Total (${label})</div><div class="stat-val num">${teamTotal.toLocaleString()}</div><div class="stat-sub">All staff combined</div></div>
      <div class="stat-card gold"><div class="stat-label">Core Staff Total</div><div class="stat-val num">${grandTotal.toLocaleString()}</div><div class="stat-sub">${CORE.length} tracked employees</div></div>
      <div class="stat-card green"><div class="stat-label">Top Producer</div><div class="stat-val" style="font-size:16px;padding-top:4px">${topProducer.split(' ')[0]}</div><div class="stat-sub">${isYTD?ytdTotal(topProducer).toLocaleString():modTotal(currentMonth,topProducer).toLocaleString()} claims</div></div>
      <div class="stat-card navy"><div class="stat-label">Other Staff</div><div class="stat-val num">${otherTotal.toLocaleString()}</div><div class="stat-sub">Non-core contributors</div></div>
    </div>
    <div class="card">
      <div class="card-title">📋 Claims Modified — ${label}</div>
      <table>
        <thead><tr><th class="left">Staff Member</th><th>Total</th><th>Avg/Day</th>${moCols}</tr></thead>
        <tbody>
          ${rows}
          <tr class="total-row"><td class="left">GRAND TOTAL (incl. other staff)</td><td class="num">${teamTotal.toLocaleString()}</td><td>—</td>${isYTD?MONTHS.map(m=>`<td class="num">${(CORE.reduce((s,n)=>s+modTotal(m,n),0)+DATA[m].others_m.reduce((a,b)=>a+b,0)).toLocaleString()}</td>`).join(''):''}</tr>
        </tbody>
      </table>
    </div>`;
}

// ── WEEKLY DETAIL ─────────────────────────────────────────────
function renderWeekly() {
  const isYTD = currentMonth==='YTD';
  const months = isYTD ? MONTHS : [currentMonth];
  let html = '';

  months.forEach(mo => {
    const d = DATA[mo];
    html += `<div class="card" style="margin-bottom:16px">
      <div class="card-title">📅 ${mo} — Weekly Breakdown</div>
      <table>
        <thead><tr><th class="left">Staff Member</th>${d.weeks.map(w=>`<th>${w}</th>`).join('')}<th>Total</th><th>Avg/Day</th></tr></thead>
        <tbody>
          ${CORE.map((n,ri) => {
            const vals = d.modified[n]||[];
            const t = vals.reduce((a,b)=>a+b,0);
            return `<tr><td class="left">${n}</td>${vals.map(v=>`<td class="num">${fmt(v)}</td>`).join('')}<td class="num" style="font-weight:700;color:var(--navy)">${fmt(t)}</td><td class="num">${avgDay(mo,n)}</td></tr>`;
          }).join('')}
          <tr><td class="left" style="color:var(--muted);font-style:italic">Other Staff</td>${d.others_m.map(v=>`<td class="num" style="color:var(--muted)">${fmt(v)}</td>`).join('')}<td class="num" style="color:var(--muted)">${fmt(d.others_m.reduce((a,b)=>a+b,0))}</td><td>—</td></tr>
          <tr class="total-row"><td class="left">Grand Total</td>${d.weeks.map((_,wi)=>`<td class="num">${(CORE.reduce((s,n)=>s+(d.modified[n]?.[wi]||0),0)+d.others_m[wi]).toLocaleString()}</td>`).join('')}<td class="num">${(CORE.reduce((s,n)=>s+modTotal(mo,n),0)+d.others_m.reduce((a,b)=>a+b,0)).toLocaleString()}</td><td>—</td></tr>
        </tbody>
      </table>
    </div>`;
  });
  document.getElementById('panel-weekly').innerHTML = html;
}

// ── LEADERBOARD ───────────────────────────────────────────────
function renderLeaderboard() {
  const isYTD = currentMonth==='YTD';
  const medals = ['🥇','🥈','🥉'];

  const sorted = [...CORE]
    .map(n=>({ name:n, total:isYTD?ytdTotal(n):modTotal(currentMonth,n), avg:isYTD?ytdAvgDay(n):avgDay(currentMonth,n) }))
    .sort((a,b)=>b.total-a.total);

  const rows = sorted.map((e,i)=>`<tr>
    <td><span class="medal">${medals[i]||i+1}</span></td>
    <td class="left">${e.name}</td>
    <td class="num" style="font-weight:700;font-size:15px;color:var(--navy)">${e.total>0?e.total.toLocaleString():'<span class="dash">—</span>'}</td>
    <td class="num">${e.avg}</td>
    <td style="width:180px">
      <div class="prog-bar"><div class="prog-fill" style="width:${pct(e.total,sorted[0].total)}%"></div></div>
    </td>
    ${MONTHS.map(m=>`<td class="num">${fmt(modTotal(m,e.name))}</td>`).join('')}
  </tr>`).join('');

  document.getElementById('panel-leaderboard').innerHTML = `
    <div class="card">
      <div class="card-title">🏆 ${isYTD?'YTD':'Monthly'} Leaderboard — ${currentMonth}</div>
      <table>
        <thead><tr><th style="width:40px">#</th><th class="left">Staff Member</th><th>Total</th><th>Avg/Day</th><th>Relative</th>${MONTHS.map(m=>`<th>${m}</th>`).join('')}</tr></thead>
        <tbody>${rows}</tbody>
      </table>
    </div>`;
}

// ── 90% THRESHOLD (BI-WEEKLY) ────────────────────────────────
function renderThreshold() {
  // Build a flat list of bi-weekly periods across all months, Feb 2026 onward
  // Each period = sum of 2 consecutive weeks within a month
  // Baseline = last bi-weekly period of Jan 2026 (weeks 4+5: Jan 18-31)

  // All tracked periods in order: [label, month, weekIndexes[]]
  const periods = [
    // Jan baseline (last 2 weeks — reference only, not evaluated)
    { label:"Jan 18-31",  mo:"Jan 2026", wks:[3,4], baseline:true },
    // Feb periods
    { label:"Feb 1-14",   mo:"Feb 2026", wks:[0,1] },
    { label:"Feb 15-28",  mo:"Feb 2026", wks:[2,3] },
    // Mar periods
    { label:"Mar 1-14",   mo:"Mar 2026", wks:[0,1] },
    { label:"Mar 15-28",  mo:"Mar 2026", wks:[2,3] },
  ];

  function periodTotal(p, name) {
    return p.wks.reduce((s,wi) => s + (DATA[p.mo].modified[name]?.[wi] || 0), 0);
  }

  const trackPeriods = periods.filter(p=>!p.baseline);

  let html = `
    <div class="card" style="margin-bottom:12px">
      <div class="card-title">ℹ️ How This Works</div>
      <div style="padding:10px 16px;font-size:12px;color:var(--muted);line-height:1.7">
        Weeks are combined into <strong>2-week periods</strong>. Each period is compared to the prior 2-week period.
        <strong>90% or more</strong> of the prior period's output = ✅ Met. Below 90% = ❌ showing exact claims short.
        <strong>Jan 18–31 is the baseline</strong> (not evaluated). Policy effective Feb 2026.
        <br><span style="color:var(--teal);font-weight:600">Tip: To hit 90%, each person just needs to stay within ~10% of their own previous output — attainable even in shorter weeks.</span>
      </div>
    </div>
    <div class="card">
      <div class="card-title">⚠️ Bi-Weekly 90% Threshold — Feb 2026 onward</div>
      <table>
        <thead>
          <tr>
            <th class="left">Staff Member</th>
            <th>Jan 18-31<br><span style="font-weight:400;font-size:9px">(baseline)</span></th>
            ${trackPeriods.map(p=>`<th>${p.label}</th>`).join('')}
            <th>Periods Met</th>
            <th>Pass Rate</th>
          </tr>
        </thead>
        <tbody>
          ${CORE.map(name => {
            const baseline = periods[0];
            let prev = periodTotal(baseline, name);
            let met=0, total=0;

            const cells = trackPeriods.map(p => {
              const cur = periodTotal(p, name);
              // If no baseline yet, use this as first reference
              if (prev === 0) {
                prev = cur;
                return `<td><span class="badge-ref">${cur>0?cur:'—'}<br><span style="font-size:9px">est. baseline</span></span></td>`;
              }
              total++;
              const needed = Math.round(prev * 0.9);
              const short  = needed - cur;
              const ratio  = cur / prev;
              prev = cur;
              if (ratio >= 0.9) {
                met++;
                return `<td><span class="badge-met">✅ ${cur.toLocaleString()}</span><br><span style="font-size:9px;color:var(--green)">needed ${needed}</span></td>`;
              } else {
                return `<td><span class="badge-miss">❌ ${cur.toLocaleString()}</span><br><span style="font-size:9px;color:var(--red)">short by ${short}</span></td>`;
              }
            });

            const rate = total>0 ? Math.round(met/total*100) : null;
            const rateBadge = rate===null
              ? '<span class="badge-ref">—</span>'
              : rate===100 ? `<span class="badge-met">${rate}%</span>`
              : rate>=50   ? `<span class="badge-warn">${rate}%</span>`
              :               `<span class="badge-miss">${rate}%</span>`;

            const baseVal = periodTotal(baseline, name);
            return `<tr>
              <td class="left">${name}</td>
              <td class="num">${baseVal>0?baseVal:'<span class="badge-ref">No data</span>'}</td>
              ${cells.join('')}
              <td class="num" style="font-weight:700">${total>0?`${met}/${total}`:'—'}</td>
              <td>${rateBadge}</td>
            </tr>`;
          }).join('')}
          <tr class="total-row">
            <td class="left">Team Total</td>
            <td class="num">${periodTotal(periods[0], 'ALL')|| CORE.reduce((s,n)=>s+periodTotal(periods[0],n),0)}</td>
            ${trackPeriods.map(p=>`<td class="num">${CORE.reduce((s,n)=>s+periodTotal(p,n),0).toLocaleString()}</td>`).join('')}
            <td>—</td><td>—</td>
          </tr>
        </tbody>
      </table>
    </div>`;

  document.getElementById('panel-threshold').innerHTML = html;
}

// ── CHARTS ────────────────────────────────────────────────────
function renderCharts() {
  // Destroy existing
  Object.values(chartInstances).forEach(c=>c.destroy());
  chartInstances = {};

  const colors = ['#1a7fa8','#c9922a','#2e7d32','#7b1fa2','#d32f2f','#0288d1','#558b2f'];

  document.getElementById('panel-charts').innerHTML = `
    <div class="charts-grid">
      <div class="card"><div class="card-title">📊 Monthly Claims by Staff Member</div><div class="chart-wrap" style="height:280px"><canvas id="chart-monthly"></canvas></div></div>
      <div class="card"><div class="card-title">📈 Month-over-Month Trend (Core Staff)</div><div class="chart-wrap" style="height:280px"><canvas id="chart-trend"></canvas></div></div>
    </div>
    <div class="card"><div class="card-title">📉 Team Weekly Volume — Mar 2026</div><div class="chart-wrap" style="height:220px"><canvas id="chart-weekly"></canvas></div></div>`;

  // Monthly bar
  setTimeout(()=>{
    const activeNames = CORE.filter(n=>ytdTotal(n)>0);
    chartInstances.monthly = new Chart(document.getElementById('chart-monthly'), {
      type:'bar',
      data:{
        labels: MONTHS,
        datasets: activeNames.map((n,i)=>({
          label:n, backgroundColor:colors[i]+'cc',
          data: MONTHS.map(m=>modTotal(m,n))
        }))
      },
      options:{ responsive:true, maintainAspectRatio:false, plugins:{legend:{labels:{font:{size:10}}}},
        scales:{ x:{ticks:{font:{size:10}}}, y:{ticks:{font:{size:10}}} } }
    });

    // Trend line
    chartInstances.trend = new Chart(document.getElementById('chart-trend'), {
      type:'line',
      data:{
        labels: MONTHS,
        datasets: activeNames.map((n,i)=>({
          label:n, borderColor:colors[i], backgroundColor:colors[i]+'22',
          data: MONTHS.map(m=>modTotal(m,n)), tension:0.3, pointRadius:4
        }))
      },
      options:{ responsive:true, maintainAspectRatio:false, plugins:{legend:{labels:{font:{size:10}}}},
        scales:{ x:{ticks:{font:{size:10}}}, y:{ticks:{font:{size:10}}} } }
    });

    // Weekly bar (Mar 2026)
    const marData = DATA["Mar 2026"];
    const activeNamesMar = CORE.filter(n=>modTotal("Mar 2026",n)>0);
    chartInstances.weekly = new Chart(document.getElementById('chart-weekly'), {
      type:'bar',
      data:{
        labels: marData.weeks,
        datasets: activeNamesMar.map((n,i)=>({
          label:n, backgroundColor:colors[i]+'cc',
          data: marData.modified[n]
        }))
      },
      options:{ responsive:true, maintainAspectRatio:false, plugins:{legend:{labels:{font:{size:10}}}},
        scales:{ x:{stacked:true,ticks:{font:{size:10}}}, y:{stacked:true,ticks:{font:{size:10}}} } }
    });
  }, 50);
}

// ── PERFORMANCE NOTES ─────────────────────────────────────────
function renderNotes() {
  const html = `
    <div class="perf-grid">
      ${CORE.map(name => {
        const ytd = ytdTotal(name);
        const avg = perfAvgDay(name);
        const notes = PERF_NOTES[name];
        const bestMo = MONTHS.reduce((b,m)=>modTotal(m,name)>modTotal(b,name)?m:b, MONTHS[0]);
        return `
        <div class="perf-card">
          <div class="perf-head">
            <span>${name}</span>
            <span style="font-size:11px;font-weight:400;opacity:0.7">YTD: ${ytd.toLocaleString()} claims</span>
          </div>
          <div class="perf-stats">
            <div class="ps"><div class="ps-val">${ytd.toLocaleString()}</div><div class="ps-lbl">YTD Total</div></div>
            <div class="ps"><div class="ps-val">${avg}</div><div class="ps-lbl">Avg/Day</div></div>
            <div class="ps"><div class="ps-val" style="font-size:13px">${bestMo}</div><div class="ps-lbl">Best Month</div></div>
            <div class="ps"><div class="ps-val">${modTotal(bestMo,name).toLocaleString()}</div><div class="ps-lbl">Best Month Total</div></div>
          </div>
          <div class="perf-body">
            <div class="perf-section">
              <h4>✅ Strengths</h4>
              <ul>${notes.strengths.map(s=>`<li>${s}</li>`).join('')}</ul>
            </div>
            <div class="perf-section">
              <h4>⚠️ Development Areas</h4>
              <ul>${notes.development.map(s=>`<li>${s}</li>`).join('')}</ul>
            </div>
            <div class="perf-section" style="grid-column:1/-1">
              <h4>🎯 Goals / Next Steps</h4>
              <ul>${notes.goals.map(s=>`<li>${s}</li>`).join('')}</ul>
            </div>
          </div>
        </div>`;
      }).join('')}
    </div>`;
  document.getElementById('panel-notes').innerHTML = html;
}

// ── INIT ──────────────────────────────────────────────────────
renderSummary();
</script>
</body>
</html>'''

with open("/mnt/user-data/outputs/ClaimsTracker_FY2026.html", "w") as f:
    f.write(HTML)
print("Done")
