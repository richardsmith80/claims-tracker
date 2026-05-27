<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Claims Tracker — Mann-Grandstaff VAMC FY2026</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=DM+Mono:wght@400;500&display=swap');
  :root{--navy:#0f2444;--navy2:#1a3560;--teal:#1a7fa8;--teal2:#22a8db;--gold:#c9922a;--green:#1a7a4a;--green-bg:#e8f7ee;--red:#c0392b;--red-bg:#fdecea;--amber:#d97706;--amber-bg:#fef3c7;--bg:#f0f4f9;--card:#fff;--border:#dde3ed;--text:#1a2640;--muted:#6b7a99;--stripe:#f7f9fc;}
  *{box-sizing:border-box;margin:0;padding:0;}
  body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);font-size:13px;}
  .header{background:linear-gradient(135deg,var(--navy),var(--navy2));padding:14px 24px;display:flex;align-items:center;justify-content:space-between;box-shadow:0 2px 12px rgba(0,0,0,.25);position:sticky;top:0;z-index:100;}
  .header-left h1{font-size:15px;font-weight:700;color:#fff;letter-spacing:.02em;}
  .header-left p{font-size:11px;color:rgba(255,255,255,.55);margin-top:1px;font-family:'DM Mono',monospace;}
  .header-right{font-size:11px;color:rgba(255,255,255,.5);font-family:'DM Mono',monospace;}
  .tabbar{background:var(--navy);display:flex;gap:2px;padding:0 24px;border-bottom:2px solid var(--teal);overflow-x:auto;}
  .tab{padding:9px 18px;font-size:12px;font-weight:600;color:rgba(255,255,255,.5);cursor:pointer;border-bottom:3px solid transparent;margin-bottom:-2px;transition:all .15s;white-space:nowrap;}
  .tab:hover{color:rgba(255,255,255,.85);}
  .tab.active{color:var(--teal2);border-bottom-color:var(--teal2);}
  .month-bar{background:var(--card);border-bottom:1px solid var(--border);padding:8px 24px;display:flex;gap:6px;align-items:center;overflow-x:auto;}
  .month-bar label{font-size:11px;font-weight:600;color:var(--muted);margin-right:4px;white-space:nowrap;}
  .mbtn{padding:5px 14px;border-radius:20px;font-size:11px;font-weight:600;border:1.5px solid var(--border);background:transparent;color:var(--muted);cursor:pointer;transition:all .15s;white-space:nowrap;}
  .mbtn:hover{border-color:var(--teal);color:var(--teal);}
  .mbtn.active{background:var(--teal);border-color:var(--teal);color:#fff;}
  .mbtn.ytd{background:var(--navy);border-color:var(--navy);color:#fff;}
  .mbtn.ytd.active{background:var(--gold);border-color:var(--gold);}
  .content{padding:16px 24px;max-width:1400px;margin:0 auto;}
  .stat-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:10px;margin-bottom:16px;}
  .stat-card{background:var(--card);border:1px solid var(--border);border-radius:10px;padding:12px 16px;position:relative;overflow:hidden;}
  .stat-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--teal);}
  .stat-card.gold::before{background:var(--gold);}
  .stat-card.green::before{background:var(--green);}
  .stat-card.navy::before{background:var(--navy);}
  .stat-label{font-size:10px;font-weight:600;color:var(--muted);text-transform:uppercase;letter-spacing:.06em;}
  .stat-val{font-size:26px;font-weight:700;color:var(--navy);line-height:1.1;margin:4px 0 2px;font-family:'DM Mono',monospace;}
  .stat-sub{font-size:10px;color:var(--muted);}
  .card{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;margin-bottom:16px;}
  .card-title{padding:10px 16px;font-size:12px;font-weight:700;color:var(--navy);border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;gap:8px;background:var(--stripe);}
  table{width:100%;border-collapse:collapse;}
  th{padding:8px 12px;text-align:center;font-size:10px;font-weight:700;color:#fff;background:var(--navy);text-transform:uppercase;letter-spacing:.05em;white-space:nowrap;}
  th.left{text-align:left;}
  td{padding:7px 12px;text-align:center;border-bottom:1px solid var(--border);font-size:12px;color:var(--text);}
  td.left{text-align:left;font-weight:600;}
  tr:last-child td{border-bottom:none;}
  tr:nth-child(even) td{background:var(--stripe);}
  tr.total-row td{background:var(--navy)!important;color:#fff!important;font-weight:700;}
  .num{font-family:'DM Mono',monospace;}
  .dash{color:var(--border);}
  .badge-met{background:var(--green-bg);color:var(--green);padding:2px 8px;border-radius:12px;font-size:11px;font-weight:700;white-space:nowrap;}
  .badge-miss{background:var(--red-bg);color:var(--red);padding:2px 8px;border-radius:12px;font-size:11px;font-weight:700;white-space:nowrap;}
  .badge-warn{background:var(--amber-bg);color:var(--amber);padding:2px 8px;border-radius:12px;font-size:11px;font-weight:700;white-space:nowrap;}
  .badge-ref{background:#f0f4f9;color:var(--muted);padding:2px 8px;border-radius:12px;font-size:11px;}
  .medal{font-size:16px;}
  .perf-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
  .perf-card{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;}
  .perf-head{padding:10px 14px;background:var(--navy);color:#fff;font-weight:700;font-size:13px;display:flex;justify-content:space-between;align-items:center;}
  .perf-body{padding:12px 14px;display:grid;grid-template-columns:1fr 1fr;gap:10px;}
  .perf-section h4{font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.07em;color:var(--muted);margin-bottom:6px;}
  .perf-section ul{padding-left:14px;}
  .perf-section li{font-size:11px;line-height:1.7;color:var(--text);}
  .perf-stats{display:flex;gap:8px;padding:8px 14px;background:var(--stripe);border-top:1px solid var(--border);flex-wrap:wrap;}
  .ps{text-align:center;min-width:70px;}
  .ps-val{font-size:16px;font-weight:700;color:var(--navy);font-family:'DM Mono',monospace;}
  .ps-lbl{font-size:9px;color:var(--muted);font-weight:600;}
  .panel{display:none;}
  .panel.active{display:block;}
  .prog-bar{height:6px;background:var(--border);border-radius:3px;overflow:hidden;margin-top:4px;}
  .prog-fill{height:100%;border-radius:3px;background:var(--teal);transition:width .4s;}
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
  <div class="tab active" onclick="switchTab('summary',this)">📊 Summary</div>
  <div class="tab" onclick="switchTab('weekly',this)">📅 Weekly Detail</div>
  <div class="tab" onclick="switchTab('leaderboard',this)">🏆 Leaderboard</div>
  <div class="tab" onclick="switchTab('threshold',this)">⚠️ 75% Threshold</div>
  <div class="tab" onclick="switchTab('trips',this)">🚐 Trips Scheduled</div>
  <div class="tab" onclick="switchTab('notes',this)">📝 Performance Notes</div>

</div>
<div class="month-bar">
  <label>MONTH:</label>
  <button class="mbtn" onclick="setMonth('Oct 2025',this)">Oct 2025</button>
  <button class="mbtn" onclick="setMonth('Nov 2025',this)">Nov 2025</button>
  <button class="mbtn" onclick="setMonth('Dec 2025',this)">Dec 2025</button>
  <button class="mbtn" onclick="setMonth('Jan 2026',this)">Jan 2026</button>
  <button class="mbtn" onclick="setMonth('Feb 2026',this)">Feb 2026</button>
  <button class="mbtn" onclick="setMonth('Mar 2026',this)">Mar 2026</button>
  <button class="mbtn" onclick="setMonth('Apr 2026',this)">Apr 2026</button>
  <button class="mbtn active" onclick="setMonth('May 2026',this)">May 2026</button>
  <button class="mbtn ytd" onclick="setMonth('YTD',this)">YTD</button>
</div>
<div class="content">
  <div id="panel-summary" class="panel active"></div>
  <div id="panel-weekly" class="panel"></div>
  <div id="panel-leaderboard" class="panel"></div>
  <div id="panel-threshold" class="panel"></div>
  <div id="panel-trips" class="panel"></div>
  <div id="panel-notes" class="panel"></div>

</div>
<script>
const CORE=["Thomas Banks","Tony Vaughn","Trent Crabtree","Richard Smith","Kelly Young","Alyson Atwater","Dakota Hackworth","Stephanie Sgambati"];
const MONTHS=["Oct 2025","Nov 2025","Dec 2025","Jan 2026","Feb 2026","Mar 2026","Apr 2026","May 2026"];
const AVG_START_MONTH="Feb 2026";
const STD_DAYS={"Feb 2026":19,"Mar 2026":21,"Apr 2026":22,"May 2026":21};
const THRESHOLD=0.75;
const CURRENT_MONTH="May 2026";
const TRACK_MONTHS=["Feb 2026","Mar 2026","Apr 2026","May 2026"];
const BASELINE_MONTH={"Thomas Banks":"Feb 2026","Tony Vaughn":"Feb 2026","Trent Crabtree":"Feb 2026","Richard Smith":"Feb 2026","Kelly Young":"Feb 2026","Alyson Atwater":"Feb 2026","Dakota Hackworth":"Mar 2026","Stephanie Sgambati":"May 2026"};

const ACTIVE_DAYS={
  "Thomas Banks":    {"Feb 2026":19,"Mar 2026":19,"Apr 2026":20,"May 2026":18},
  "Tony Vaughn":     {"Feb 2026":18,"Mar 2026":20,"Apr 2026":18,"May 2026":15},
  "Trent Crabtree":  {"Feb 2026":18,"Mar 2026":20,"Apr 2026":18,"May 2026":16},
  "Richard Smith":   {"Feb 2026":17,"Mar 2026":17,"Apr 2026":17,"May 2026":14},
  "Kelly Young":     {"Feb 2026":12,"Mar 2026":15,"Apr 2026":8, "May 2026":10},
  "Alyson Atwater":  {"Feb 2026":6, "Mar 2026":0, "Apr 2026":0, "May 2026":0},
  "Dakota Hackworth":{"Feb 2026":0, "Mar 2026":10,"Apr 2026":20,"May 2026":17},
  "Stephanie Sgambati":{"Feb 2026":0,"Mar 2026":0,"Apr 2026":0,"May 2026":5}
};

const DATA={
  "Oct 2025":{weeks:["Oct 5-11","Oct 12-18","Oct 19-25","Oct 26-Nov1"],wd:[5,4,5,5],modified:{"Thomas Banks":[0,0,0,0],"Tony Vaughn":[13,45,114,9],"Trent Crabtree":[161,88,148,36],"Richard Smith":[7,22,28,164],"Kelly Young":[284,82,405,164],"Alyson Atwater":[0,0,0,0],"Dakota Hackworth":[0,0,0,0],"Stephanie Sgambati":[0,0,0,0]},others_m:[5,5,149,0]},
  "Nov 2025":{weeks:["Nov 2-8","Nov 9-15","Nov 16-22","Nov 23-29"],wd:[5,4,5,4],modified:{"Thomas Banks":[0,0,0,0],"Tony Vaughn":[44,12,67,103],"Trent Crabtree":[89,75,51,15],"Richard Smith":[2,0,0,0],"Kelly Young":[109,8,28,2],"Alyson Atwater":[0,0,23,0],"Dakota Hackworth":[0,0,0,0],"Stephanie Sgambati":[0,0,0,0]},others_m:[1,16,82,18]},
  "Dec 2025":{weeks:["Dec 7-13","Dec 14-20","Dec 21-27"],wd:[5,5,4],modified:{"Thomas Banks":[0,0,0],"Tony Vaughn":[216,56,131],"Trent Crabtree":[111,65,23],"Richard Smith":[2,0,29],"Kelly Young":[0,0,0],"Alyson Atwater":[0,0,0],"Dakota Hackworth":[0,0,0],"Stephanie Sgambati":[0,0,0]},others_m:[27,43,6]},
  "Jan 2026":{weeks:["Jan 1-3","Jan 4-10","Jan 11-17","Jan 18-24","Jan 25-31"],wd:[4,5,5,4,5],modified:{"Thomas Banks":[0,0,0,0,151],"Tony Vaughn":[414,300,338,242,43],"Trent Crabtree":[71,104,105,37,149],"Richard Smith":[9,17,162,18,98],"Kelly Young":[2,2,2,1,96],"Alyson Atwater":[0,0,0,0,0],"Dakota Hackworth":[0,0,0,0,0],"Stephanie Sgambati":[0,0,0,0,0]},others_m:[10,32,44,4,2]},
  "Feb 2026":{weeks:["Feb 1-7","Feb 8-14","Feb 15-21","Feb 22-28"],wd:[5,5,4,5],modified:{"Thomas Banks":[221,147,197,66],"Tony Vaughn":[154,242,211,127],"Trent Crabtree":[184,417,72,161],"Richard Smith":[31,183,9,27],"Kelly Young":[45,5,5,6],"Alyson Atwater":[34,2,0,0],"Dakota Hackworth":[0,0,0,0],"Stephanie Sgambati":[0,0,0,0]},others_m:[4,10,43,49]},
  "Mar 2026":{weeks:["Mar 1-6","Mar 8-14","Mar 15-21","Mar 22-28","Mar 29-31"],wd:[5,5,5,5,3],modified:{"Thomas Banks":[144,244,223,342,41],"Tony Vaughn":[227,138,257,121,51],"Trent Crabtree":[115,235,130,194,88],"Richard Smith":[44,35,17,25,8],"Kelly Young":[20,100,107,75,0],"Alyson Atwater":[0,0,0,0,0],"Dakota Hackworth":[0,0,170,105,50],"Stephanie Sgambati":[0,0,0,0,0]},others_m:[52,67,90,84,0]},
  "Apr 2026":{weeks:["Apr 1-4","Apr 5-11","Apr 12-18","Apr 19-24","Apr 28-30"],wd:[4,5,5,5,3],modified:{"Thomas Banks":[93,123,137,163,102],"Tony Vaughn":[118,124,169,144,123],"Trent Crabtree":[91,281,209,287,115],"Richard Smith":[6,49,49,20,0],"Kelly Young":[1,13,1,1,0],"Alyson Atwater":[0,0,0,0,0],"Dakota Hackworth":[113,174,294,186,155],"Stephanie Sgambati":[0,0,0,0,0]},others_m:[0,35,43,5,0]},
  "May 2026":{weeks:["May 1-2","May 4-9","May 10-16","May 17-23"],wd:[2,5,5,5],modified:{"Thomas Banks":[50,712,194,474],"Tony Vaughn":[64,121,116,100],"Trent Crabtree":[99,323,114,306],"Richard Smith":[0,22,48,48],"Kelly Young":[5,4,8,4],"Alyson Atwater":[0,0,0,0],"Dakota Hackworth":[89,139,195,175],"Stephanie Sgambati":[0,0,2,1]},others_m:[16,31,47,3]}
};

// ── TRIPS ─────────────────────────────────────────────────────────
const TRIPS_STAFF=["Richard Smith","Dakota Hackworth","Tony Vaughn","Kelly Young","Trent Crabtree","Thomas Banks"];
const TRIPS_MONTHS=["Nov 2025","Dec 2025","Jan 2026","Feb 2026","Mar 2026","Apr 2026","May 2026","Jun 2026"];
const TRIPS_MONTHLY={
  "Nov 2025":{"Richard Smith":63,"Dakota Hackworth":0, "Tony Vaughn":0, "Kelly Young":0, "Trent Crabtree":0,"Thomas Banks":0},
  "Dec 2025":{"Richard Smith":58,"Dakota Hackworth":0, "Tony Vaughn":0, "Kelly Young":0, "Trent Crabtree":0,"Thomas Banks":0},
  "Jan 2026":{"Richard Smith":67,"Dakota Hackworth":0, "Tony Vaughn":0, "Kelly Young":25,"Trent Crabtree":0,"Thomas Banks":0},
  "Feb 2026":{"Richard Smith":45,"Dakota Hackworth":0, "Tony Vaughn":12,"Kelly Young":0, "Trent Crabtree":4,"Thomas Banks":0},
  "Mar 2026":{"Richard Smith":175,"Dakota Hackworth":98,"Tony Vaughn":20,"Kelly Young":0,"Trent Crabtree":4,"Thomas Banks":0},
  "Apr 2026":{"Richard Smith":130,"Dakota Hackworth":112,"Tony Vaughn":30,"Kelly Young":0,"Trent Crabtree":2,"Thomas Banks":0},
  "May 2026":{"Richard Smith":15,"Dakota Hackworth":81,"Tony Vaughn":18,"Kelly Young":0,"Trent Crabtree":1,"Thomas Banks":0},
  "Jun 2026":{"Richard Smith":0, "Dakota Hackworth":17,"Tony Vaughn":0, "Kelly Young":0, "Trent Crabtree":0,"Thomas Banks":0}
};

const PERF_NOTES={
  "Thomas Banks":{strengths:["YTD leader in claims created. Took ownership of paper backlog from Jan 2026.","Strong Q2 FY2026 — 631 modified in Feb, 994 in Mar.","Works across all three primary workflows: paper claims creation, CITC, and Manual Review."],development:["Two documented entry errors this quarter — both self-reported immediately and corrected prior to payment processing. No financial impact.","Month-to-month variance (376 claim spread) partially explained by window rotation and calendar factors."],goals:["Target 50+ avg/day. Reduce variance — floor of 650 modified any single month. Continue cross-workflow flexibility."],q3goals:["Target ≥950 modified per month.","Maintain daily avg of 45+ claims on active days.","Meet 75% threshold every month.","No recurrence of wrong-Veteran entry errors."]},
  "Tony Vaughn":{strengths:["Primary CITC claims processor. Deep expertise in complex community claim verification.","Consistent output across FY2026. Jan 2026 — 1,337 modified, highest single-month on team.","Met 75% threshold both evaluated months."],development:["Month-to-month variance (493 claim spread) — consistency on processing weeks is primary development area.","May 2026 is still in progress; currently on Window Group duty."],goals:["Maintain avg/day ≥35. Sustain 75% threshold. Establish weekly floor of 100+ on processing weeks."],q3goals:["Target ≥650 modified per month.","Maintain daily avg of 40+ claims.","Meet 75% threshold all 3 months of Q3.","Establish reliable processing-week floor."]},
  "Trent Crabtree":{strengths:["Primary Manual Review claims processor — highest-complexity queue on team.","Apr 2026 — 983 modified, highest single month on team for Q2.","Daily avg of 42.9 approaching Exceptional standard of 45/day."],development:["Largest variance on team (447 claim spread). Window rotation explains some dips but processing-week consistency needs improvement.","May 2026 still in progress."],goals:["Establish weekly minimum floor. Target 75% threshold every month. Reduce variance."],q3goals:["Target ≥850 modified per month.","Maintain daily avg of 45+ claims.","First quarter with perfect 3/3 threshold pass rate.","No week below 150 claims when fully active."]},
  "Richard Smith":{strengths:["Supervisor/lead role — volume reflects dual processing and supervisory responsibilities.","Strong Jan 2026 (304 modified) demonstrating processing capability.","Consistent presence across multiple months."],development:["Declining trend (250→129→124→70) requires focused attention and discussion.","Missed 75% threshold both evaluated months."],goals:["Target ≥150 modified per month. Document supervisory hours separately. Meet 75% threshold at least 2 of 3 months in Q3."],q3goals:["Reverse declining trend — 150+ modified per month minimum.","Maintain daily avg of 10+ on active days.","Meet 75% threshold at least 2 of 3 months.","Document supervisory contributions formally."]},
  "Kelly Young":{strengths:["935 modified in Oct 2025 — exceptional Q1 performance.","Strong Mar 2026 reengagement (302 modified).","High-capacity processor when fully active."],development:["Extreme inconsistency — Mar (302) vs Apr (16). Only 1 of 2 months met 75% threshold.","Consistency is the core development area — capacity is demonstrated."],goals:["No zero-output weeks. Full-month consistency every month. Document any absences."],q3goals:["Target ≥150 modified every month of Q3.","Meet 75% threshold all 3 months.","No near-zero months — document any month below 50."]},
  "Alyson Atwater":{strengths:["Active contributor Oct–Feb. Solid productivity in Nov 2025.","Cross-trained on both created and modified workflows."],development:["No recorded activity from Mar 2026 onward — status must be confirmed with supervisor."],goals:["Confirm role and assignment. Re-establish targets if active. Provide explanation for activity gaps."],q3goals:["Confirm employment status before Q3 begins.","If active: target ≥50 modified per month as re-entry baseline.","If active: no zero-output weeks.","Written explanation for Mar–May absence."]},
  "Dakota Hackworth":{strengths:["Primary paper claims creator and ride scheduler. 1,670 claims YTD and 291 trips scheduled.","Apr 2026 — 922 modified, highest on team for Q2. 184% growth Mar→Apr.","Dual-workflow contributor from first week of employment."],development:["Weekly floor not yet established — variance between weeks is the primary development area.","May 2026 in progress; currently on Window Group duty."],goals:["Sustain 300+ modified monthly. Meet 75% threshold every month. Establish weekly floor."],q3goals:["Target ≥600 modified per month.","Maintain daily avg of 40+ claims.","Meet 75% threshold all 3 months.","Weekly floor of 125+ claims when fully active."]},
  "Stephanie Sgambati":{strengths:["New team member — early contributions show engagement.","Active from first tracked week in May 2026."],development:["Insufficient data — first full month will establish baseline.","Focus on consistency and building volume."],goals:["Establish baseline avg/day. Build consistent weekly output. Target 75% threshold from first full month."],q3goals:["Complete first full month (Jun 2026) to establish baseline.","Target ≥50 modified in Jun 2026.","Maintain daily avg of 5+ on active days.","Meet 75% threshold from Jul 2026 onward."]}
};

function modTotal(mo,name){return(DATA[mo]?.modified[name]||[]).reduce((a,b)=>a+b,0);}
function ytdTotal(name){return MONTHS.reduce((s,m)=>s+modTotal(m,name),0);}
function activeWeeks(mo,name){return(DATA[mo]?.modified[name]||[]).filter(v=>v>0).length;}
function getActiveDays(mo,name){const ad=ACTIVE_DAYS[name]?.[mo];if(ad!==undefined)return ad;const v=DATA[mo]?.modified[name]||[],w=DATA[mo]?.wd||[];return v.reduce((s,x,i)=>s+(x>0?w[i]:0),0);}
function avgDay(mo,name){const t=modTotal(mo,name);if(!t)return"—";const ad=getActiveDays(mo,name);return ad>0?(t/ad).toFixed(1):"—";}
function ytdAvgDay(name){let c=0,d=0;MONTHS.forEach(mo=>{if(MONTHS.indexOf(mo)<MONTHS.indexOf(AVG_START_MONTH))return;const t=modTotal(mo,name);if(!t)return;const ad=getActiveDays(mo,name);if(ad>0){c+=t;d+=ad;}});return d>0?(c/d).toFixed(1):"—";}
function proRatedTarget(baseVal,baseMo,mo,name){const stdBase=STD_DAYS[baseMo]||21;const ad=getActiveDays(mo,name);const stdMo=STD_DAYS[mo]||21;return Math.round((baseVal/stdBase)*(ad>0?ad:stdMo)*THRESHOLD);}
function tripsTotal(name){return TRIPS_MONTHS.reduce((s,m)=>s+(TRIPS_MONTHLY[m]?.[name]||0),0);}
function tripsMoTotal(mo){return TRIPS_STAFF.reduce((s,n)=>s+(TRIPS_MONTHLY[mo]?.[n]||0),0);}
function fmt(n){return(n>0)?n.toLocaleString():'<span class="dash">—</span>';}
function pct(a,b){return b>0?Math.round(a/b*100):0;}

let currentMonth="May 2026",currentTab="summary";
function switchTab(tab,el){currentTab=tab;document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));el.classList.add('active');document.querySelectorAll('.panel').forEach(p=>p.classList.remove('active'));document.getElementById('panel-'+tab).classList.add('active');renderPanel(tab);}
function setMonth(mo,el){currentMonth=mo;document.querySelectorAll('.mbtn').forEach(b=>b.classList.remove('active'));el.classList.add('active');renderPanel(currentTab);}
function renderPanel(tab){
  if(tab==='summary')renderSummary();
  if(tab==='weekly')renderWeekly();
  if(tab==='leaderboard')renderLeaderboard();
  if(tab==='threshold')renderThreshold();
  if(tab==='trips')renderTrips();
  if(tab==='notes')renderNotes();

}

function renderSummary(){
  const isYTD=currentMonth==='YTD',months=isYTD?MONTHS:[currentMonth],label=isYTD?'YTD FY2026':currentMonth;
  const grandTotal=CORE.reduce((s,n)=>s+(isYTD?ytdTotal(n):modTotal(currentMonth,n)),0);
  const top=CORE.reduce((b,n)=>(isYTD?ytdTotal(n):modTotal(currentMonth,n))>(isYTD?ytdTotal(b):modTotal(currentMonth,b))?n:b,CORE[0]);
  const otherTotal=months.reduce((s,m)=>s+DATA[m].others_m.reduce((a,b)=>a+b,0),0);
  const teamTotal=grandTotal+otherTotal;
  const moCols=isYTD?MONTHS.map(m=>`<th>${m}</th>`).join(''):'';
  const rows=CORE.map(n=>{const t=isYTD?ytdTotal(n):modTotal(currentMonth,n),avg=isYTD?ytdAvgDay(n):avgDay(currentMonth,n);return`<tr><td class="left">${n}</td><td class="num">${fmt(t)}</td><td class="num">${avg}</td>${isYTD?MONTHS.map(m=>`<td class="num">${fmt(modTotal(m,n))}</td>`).join(''):''}</tr>`;}).join('');
  document.getElementById('panel-summary').innerHTML=`<div class="stat-row"><div class="stat-card"><div class="stat-label">Team Total (${label})</div><div class="stat-val num">${teamTotal.toLocaleString()}</div><div class="stat-sub">All staff combined</div></div><div class="stat-card gold"><div class="stat-label">Core Staff Total</div><div class="stat-val num">${grandTotal.toLocaleString()}</div><div class="stat-sub">${CORE.length} tracked employees</div></div><div class="stat-card green"><div class="stat-label">Top Producer</div><div class="stat-val" style="font-size:16px;padding-top:4px">${top.split(' ')[0]}</div><div class="stat-sub">${(isYTD?ytdTotal(top):modTotal(currentMonth,top)).toLocaleString()} claims</div></div><div class="stat-card navy"><div class="stat-label">Other Staff</div><div class="stat-val num">${otherTotal.toLocaleString()}</div><div class="stat-sub">Non-core contributors</div></div></div>
  <div class="card"><div class="card-title">📋 Claims Modified — ${label}</div><table><thead><tr><th class="left">Staff Member</th><th>Total</th><th>Avg/Day</th>${moCols}</tr></thead><tbody>${rows}<tr class="total-row"><td class="left">GRAND TOTAL (incl. other staff)</td><td class="num">${teamTotal.toLocaleString()}</td><td>—</td>${isYTD?MONTHS.map(m=>`<td class="num">${(CORE.reduce((s,n)=>s+modTotal(m,n),0)+DATA[m].others_m.reduce((a,b)=>a+b,0)).toLocaleString()}</td>`).join(''):''}</tr></tbody></table></div>`;
}

function renderWeekly(){
  const isYTD=currentMonth==='YTD',months=isYTD?MONTHS:[currentMonth];
  let html='';
  months.forEach(mo=>{const d=DATA[mo];html+=`<div class="card" style="margin-bottom:16px"><div class="card-title">📅 ${mo} — Weekly Breakdown</div><table><thead><tr><th class="left">Staff Member</th>${d.weeks.map(w=>`<th>${w}</th>`).join('')}<th>Total</th><th>Avg/Day</th></tr></thead><tbody>${CORE.map(n=>{const vals=d.modified[n]||[],t=vals.reduce((a,b)=>a+b,0);return`<tr><td class="left">${n}</td>${vals.map(v=>`<td class="num">${fmt(v)}</td>`).join('')}<td class="num" style="font-weight:700;color:var(--navy)">${fmt(t)}</td><td class="num">${avgDay(mo,n)}</td></tr>`;}).join('')}<tr><td class="left" style="color:var(--muted);font-style:italic">Other Staff</td>${d.others_m.map(v=>`<td class="num" style="color:var(--muted)">${fmt(v)}</td>`).join('')}<td class="num" style="color:var(--muted)">${fmt(d.others_m.reduce((a,b)=>a+b,0))}</td><td>—</td></tr><tr class="total-row"><td class="left">Grand Total</td>${d.weeks.map((_,wi)=>`<td class="num">${(CORE.reduce((s,n)=>s+(d.modified[n]?.[wi]||0),0)+d.others_m[wi]).toLocaleString()}</td>`).join('')}<td class="num">${(CORE.reduce((s,n)=>s+modTotal(mo,n),0)+d.others_m.reduce((a,b)=>a+b,0)).toLocaleString()}</td><td>—</td></tr></tbody></table></div>`;});
  document.getElementById('panel-weekly').innerHTML=html;
}

function renderLeaderboard(){
  const isYTD=currentMonth==='YTD',medals=['🥇','🥈','🥉'];
  const sorted=[...CORE].map(n=>({name:n,total:isYTD?ytdTotal(n):modTotal(currentMonth,n),avg:isYTD?ytdAvgDay(n):avgDay(currentMonth,n)})).sort((a,b)=>b.total-a.total);
  const rows=sorted.map((e,i)=>`<tr><td><span class="medal">${medals[i]||i+1}</span></td><td class="left">${e.name}</td><td class="num" style="font-weight:700;font-size:15px;color:var(--navy)">${e.total>0?e.total.toLocaleString():'<span class="dash">—</span>'}</td><td class="num">${e.avg}</td><td style="width:180px"><div class="prog-bar"><div class="prog-fill" style="width:${pct(e.total,sorted[0].total)}%"></div></div></td>${MONTHS.map(m=>`<td class="num">${fmt(modTotal(m,e.name))}</td>`).join('')}</tr>`).join('');
  document.getElementById('panel-leaderboard').innerHTML=`<div class="card"><div class="card-title">🏆 ${isYTD?'YTD':'Monthly'} Leaderboard — ${currentMonth}</div><table><thead><tr><th style="width:40px">#</th><th class="left">Staff Member</th><th>Total</th><th>Avg/Day</th><th>Relative</th>${MONTHS.map(m=>`<th>${m}</th>`).join('')}</tr></thead><tbody>${rows}</tbody></table></div>`;
}

function renderThreshold(){
  const rows=CORE.map((name,ri)=>{
    const baseMo=BASELINE_MONTH[name]||"Feb 2026",baseVal=modTotal(baseMo,name),stdBase=STD_DAYS[baseMo]||21,dailyRate=baseVal>0?(baseVal/stdBase).toFixed(1):"—";
    let cells='',met=0,total=0;
    TRACK_MONTHS.forEach(mo=>{
      const t=modTotal(mo,name),isPartial=mo===CURRENT_MONTH,isBaseline=mo===baseMo,isPreHire=TRACK_MONTHS.indexOf(mo)<TRACK_MONTHS.indexOf(baseMo);
      const ad=getActiveDays(mo,name),stdMo=STD_DAYS[mo]||21,onLeave=ad>0&&ad<stdMo;
      const needed=baseVal>0?Math.round((baseVal/stdBase)*(ad>0?ad:stdMo)*THRESHOLD):0;
      if(isPreHire){cells+=`<td><span class="badge-ref" style="font-size:10px">Pre-hire</span></td>`;return;}
      if(isBaseline){cells+=`<td class="num"><strong>${t>0?t.toLocaleString():'—'}</strong><br><span style="font-size:9px;color:var(--muted)">baseline · ${stdBase}d · ${dailyRate}/day</span></td>`;return;}
      if(!baseVal){cells+=`<td><span class="badge-ref">—</span></td>`;return;}
      const pass=t>=needed;
      if(!isPartial){total++;if(pass)met++;}
      const leaveNote=onLeave?`<br><span style="font-size:9px;color:var(--amber)">📅 ${ad}/${stdMo} days</span>`:`<br><span style="font-size:9px;color:var(--muted)">${ad}/${stdMo} days</span>`;
      cells+=`<td><span class="${pass?'badge-met':isPartial?'badge-warn':'badge-miss'}">${pass?'✅':isPartial?'⏳':'❌'} ${t.toLocaleString()}</span><br><span style="font-size:9px;color:var(--${pass?'green':isPartial?'amber':'red'})">need ≥${needed}${isPartial?' (partial)':''}</span>${leaveNote}</td>`;
    });
    const rate=total>0?Math.round(met/total*100):null;
    const rateBadge=rate===null?'<span class="badge-ref">—</span>':rate===100?`<span class="badge-met">${rate}%</span>`:rate>=75?`<span class="badge-warn">${rate}%</span>`:`<span class="badge-miss">${rate}%</span>`;
    return`<tr><td class="left">${name}<br><span style="font-size:10px;color:var(--muted);font-weight:400">baseline: ${baseMo} = ${baseVal.toLocaleString()} · ${dailyRate} claims/day</span></td>${cells}<td class="num" style="font-weight:700">${total>0?`${met}/${total}`:'—'}</td><td>${rateBadge}</td></tr>`;
  }).join('');
  document.getElementById('panel-threshold').innerHTML=`<div class="card" style="margin-bottom:12px"><div class="card-title">ℹ️ How This Works</div><div style="padding:10px 16px;font-size:12px;color:var(--muted);line-height:1.7">Fixed baseline per employee (first full month). Daily rate × days actually worked × 75% = monthly target. Leave days auto-detected and pro-rated. <span style="color:var(--amber)">📅 = fewer than standard days worked.</span> <strong>⏳ ${CURRENT_MONTH} excluded until month closes.</strong></div></div>
  <div class="card"><div class="card-title">⚠️ 75% Pro-Rated Fixed Baseline Threshold — Feb 2026 onward</div><div style="overflow-x:auto"><table><thead><tr><th class="left">Staff Member</th>${TRACK_MONTHS.map(m=>`<th>${m}${m===CURRENT_MONTH?' ⏳':''}</th>`).join('')}<th>Months Met</th><th>Pass Rate</th></tr></thead><tbody>${rows}<tr class="total-row"><td class="left">Team Total</td>${TRACK_MONTHS.map(m=>`<td class="num">${CORE.reduce((s,n)=>s+modTotal(m,n),0).toLocaleString()}</td>`).join('')}<td>—</td><td>—</td></tr></tbody></table></div></div>`;
}

function renderTrips(){
  const grandTotal=TRIPS_STAFF.reduce((s,n)=>s+tripsTotal(n),0);
  const topName=TRIPS_STAFF.reduce((b,n)=>tripsTotal(n)>tripsTotal(b)?n:b,TRIPS_STAFF[0]);
  const sorted=[...TRIPS_STAFF].sort((a,b)=>tripsTotal(b)-tripsTotal(a));
  const rows=sorted.map((name,ri)=>{
    const moVals=TRIPS_MONTHS.map(m=>TRIPS_MONTHLY[m]?.[name]||0);
    const total=tripsTotal(name);
    return`<tr style="background:${ri%2===0?'var(--stripe)':'#fff'}"><td class="left">${name}</td>${moVals.map(v=>`<td class="num">${v>0?v.toLocaleString():'<span class="dash">—</span>'}</td>`).join('')}<td class="num" style="font-weight:700;color:var(--navy)">${total>0?total.toLocaleString():'<span class="dash">—</span>'}</td></tr>`;
  }).join('');
  const teamRow=`<tr class="total-row"><td class="left">Team Total</td>${TRIPS_MONTHS.map(m=>{const t=tripsMoTotal(m);return`<td class="num">${t>0?t.toLocaleString():'—'}</td>`;}).join('')}<td class="num">${grandTotal.toLocaleString()}</td></tr>`;
  document.getElementById('panel-trips').innerHTML=`
    <div class="stat-row">
      <div class="stat-card"><div class="stat-label">Total Trips Scheduled</div><div class="stat-val num">${grandTotal.toLocaleString()}</div><div class="stat-sub">Nov 2025 – Jun 2026</div></div>
      <div class="stat-card gold"><div class="stat-label">Top Scheduler</div><div class="stat-val" style="font-size:16px;padding-top:4px">${topName.split(' ')[0]}</div><div class="stat-sub">${tripsTotal(topName).toLocaleString()} trips</div></div>
      <div class="stat-card green"><div class="stat-label">Staff Contributing</div><div class="stat-val num">${TRIPS_STAFF.filter(n=>tripsTotal(n)>0).length}</div><div class="stat-sub">of ${TRIPS_STAFF.length} tracked</div></div>
      <div class="stat-card navy"><div class="stat-label">May 2026 (partial)</div><div class="stat-val num">${tripsMoTotal('May 2026')}</div><div class="stat-sub">Month in progress</div></div>
    </div>
    <div class="card"><div class="card-title">🚐 Trips Scheduled by Staff — Nov 2025 through Jun 2026</div>
      <div style="overflow-x:auto"><table>
        <thead><tr><th class="left">Staff Member</th>${TRIPS_MONTHS.map(m=>`<th>${m}</th>`).join('')}<th>YTD Total</th></tr></thead>
        <tbody>${rows}${teamRow}</tbody>
      </table></div>
    </div>
    <div class="card"><div class="card-title">ℹ️ About Trips Data</div>
      <div style="padding:10px 16px;font-size:12px;color:var(--muted);line-height:1.7">Trips include VetRide coordination and Community transportation authorizations. Data covers Nov 2025 through present. May and Jun 2026 are partial months.</div>
    </div>`;
}

function renderNotes(){
  const html=`<div class="perf-grid">${CORE.map(name=>{
    const ytd=ytdTotal(name),avg=ytdAvgDay(name);
    const notes=PERF_NOTES[name]||{strengths:["Active contributor."],development:["Continue monitoring."],goals:["Maintain current pace."],q3goals:["Maintain current pace."]};
    const bestMo=MONTHS.reduce((b,m)=>modTotal(m,name)>modTotal(b,name)?m:b,MONTHS[0]);
    const baseMo=BASELINE_MONTH[name]||"Feb 2026",baseVal=modTotal(baseMo,name),stdBase=STD_DAYS[baseMo]||21,dailyRate=baseVal>0?(baseVal/stdBase).toFixed(1):"—";
    let threshMet=0,threshTotal=0;
    TRACK_MONTHS.forEach(mo=>{
      if(mo===baseMo||mo===CURRENT_MONTH||TRACK_MONTHS.indexOf(mo)<TRACK_MONTHS.indexOf(baseMo)||!baseVal)return;
      const t=modTotal(mo,name),ad=getActiveDays(mo,name),stdMo=STD_DAYS[mo]||21;
      const needed=Math.round((baseVal/stdBase)*(ad>0?ad:stdMo)*THRESHOLD);
      threshTotal++;if(t>=needed)threshMet++;
    });
    return`<div class="perf-card"><div class="perf-head"><span>${name}</span><span style="font-size:11px;font-weight:400;opacity:.7">YTD: ${ytd.toLocaleString()} claims</span></div>
      <div class="perf-stats">
        <div class="ps"><div class="ps-val">${ytd.toLocaleString()}</div><div class="ps-lbl">YTD Total</div></div>
        <div class="ps"><div class="ps-val">${avg}</div><div class="ps-lbl">Avg/Day</div></div>
        <div class="ps"><div class="ps-val" style="font-size:13px">${bestMo.split(' ')[0]}</div><div class="ps-lbl">Best Month</div></div>
        <div class="ps"><div class="ps-val">${modTotal(bestMo,name).toLocaleString()}</div><div class="ps-lbl">Best Mo Total</div></div>
        <div class="ps"><div class="ps-val">${dailyRate}</div><div class="ps-lbl">Base Rate/Day</div></div>
        <div class="ps"><div class="ps-val">${threshTotal>0?threshMet+'/'+threshTotal:'—'}</div><div class="ps-lbl">75% Met</div></div>
      </div>
      <div class="perf-body">
        <div class="perf-section"><h4>✅ Strengths</h4><ul>${notes.strengths.map(s=>`<li>${s}</li>`).join('')}</ul></div>
        <div class="perf-section"><h4>⚠️ Development Areas</h4><ul>${notes.development.map(s=>`<li>${s}</li>`).join('')}</ul></div>
        <div class="perf-section" style="grid-column:1/-1"><h4>🎯 Current Goals</h4><ul>${notes.goals.map(s=>`<li>${s}</li>`).join('')}</ul></div>
        <div class="perf-section" style="grid-column:1/-1;background:#f0f4f9;border-radius:8px;padding:10px;margin-top:4px"><h4 style="color:var(--navy)">📅 Q3 2026 Goals (Jun–Aug)</h4><ul>${(notes.q3goals||[]).map(s=>`<li>${s}</li>`).join('')}</ul></div>
      </div></div>`;
  }).join('')}</div>`;
  document.getElementById('panel-notes').innerHTML=html;
}



renderSummary();
</script>
</body>
</html>
