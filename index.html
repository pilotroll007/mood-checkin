<!doctype html>  
<html lang="es">  
<head>  
  <meta charset="utf-8" />  
  <meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover" />  
  <meta name="apple-mobile-web-app-capable" content="yes" />  
  <meta name="apple-mobile-web-app-status-bar-style" content="default" />  
  <meta name="theme-color" content="#ffffff" />  
  <title>Mood Check-in</title>  
  <style>  
    :root { --bg:#fff; --fg:#111; --muted:#666; --card:#f4f5f7; --line:#e7e7ea; --accent:#0a84ff; }  
    body { margin:0; font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial; background:var(--bg); color:var(--fg); }  
    .wrap { max-width:860px; margin:0 auto; padding:16px 16px 28px; }  
    h1 { font-size:20px; margin:6px 0 14px; }  
    .tabs { display:flex; gap:8px; margin:10px 0 14px; }  
    .tab { flex:1; padding:10px 12px; border:1px solid var(--line); border-radius:12px; background:#fff; cursor:pointer; }  
    .tab.active { border-color:var(--fg); }  
    .row { display:flex; gap:10px; flex-wrap:wrap; align-items:center; }  
    .seg { display:flex; border:1px solid var(--line); border-radius:12px; overflow:hidden; }  
    .seg button { padding:10px 12px; background:#fff; border:0; cursor:pointer; }  
    .seg button.active { background:var(--card); font-weight:600; }  
    .card { background:var(--card); border:1px solid var(--line); border-radius:16px; padding:14px; }  
    .faces { display:flex; gap:10px; }  
    .faceBtn { width:88px; padding:12px 10px; border-radius:14px; border:2px solid transparent; background:#fff; cursor:pointer; text-align:center; }  
    .faceBtn .emoji { font-size:38px; display:block; }  
    .faceBtn small { color:var(--muted); }  
    .faceBtn.active { border-color:var(--fg); }  
    .btn { width:100%; padding:12px 14px; border-radius:14px; border:1px solid var(--line); background:#fff; cursor:pointer; font-weight:600; }  
    .btn.primary { background:rgba(10,132,255,0.12); border-color:rgba(10,132,255,0.25); }  
    .muted { color:var(--muted); font-size:13px; }  
    .grid { display:grid; grid-template-columns:repeat(7,1fr); gap:6px; }  
    .dow { font-size:12px; color:var(--muted); text-align:center; }  
    .cell { height:30px; border-radius:8px; border:1px solid var(--line); background:#fff; display:flex; align-items:center; justify-content:center; font-size:12px; }  
    .cell.empty { border:none; background:transparent; }  
    .list { display:flex; flex-direction:column; gap:8px; }  
    .item { display:flex; justify-content:space-between; gap:10px; padding:10px 12px; border-radius:12px; background:#fff; border:1px solid var(--line); }  
    .tag { font-size:12px; color:var(--muted); }  
    canvas { width:100%; height:220px; background:#fff; border:1px solid var(--line); border-radius:14px; }  
    input[type="range"] { width:100%; }  
    .topbar { display:flex; justify-content:space-between; align-items:center; gap:10px; }  
    .miniBtn { padding:8px 10px; border-radius:12px; border:1px solid var(--line); background:#fff; cursor:pointer; }  
    .kpi { display:flex; gap:10px; flex-wrap:wrap; }  
    .pill { padding:8px 10px; border-radius:999px; border:1px solid var(--line); background:#fff; font-size:13px; }  
    a { color:var(--accent); }  
  </style>  
</head>  
<body>  
  <div class="wrap">  
    <div class="topbar">  
      <h1>🟦 Mood Check-in</h1>  
      <button class="miniBtn" id="exportBtn">Export</button>  
    </div>  
    <div class="muted">Mañana/Noche · Carita + nota 1–10 · Todo queda en tu iPhone (sin cuentas).</div>  
  
    <div class="tabs">  
      <button class="tab active" data-tab="checkin">Check-in</button>  
      <button class="tab" data-tab="stats">Stats</button>  
      <button class="tab" data-tab="help">Ayuda</button>  
    </div>  
  
    <!-- CHECKIN -->  
    <section id="tab-checkin">  
      <div class="card">  
        <div class="row" style="justify-content:space-between;">  
          <div class="seg" role="tablist" aria-label="Momento">  
            <button id="slotMorning" class="active">🌅 Mañana</button>  
            <button id="slotNight">🌙 Noche</button>  
          </div>  
          <div class="muted" id="todayLabel"></div>  
        </div>  
  
        <div style="height:12px"></div>  
  
        <div class="muted" style="margin-bottom:6px;">¿Cómo te sientes?</div>  
        <div class="faces">  
          <button class="faceBtn active" data-face="0"><span class="emoji">😞</span><small>Triste</small></button>  
          <button class="faceBtn" data-face="1"><span class="emoji">😐</span><small>Normal</small></button>  
          <button class="faceBtn" data-face="2"><span class="emoji">🙂</span><small>Bien</small></button>  
        </div>  
  
        <div style="height:14px"></div>  
  
        <div class="row" style="justify-content:space-between;">  
          <div class="muted">Nota</div>  
          <div class="pill" id="ratingPill">7 / 10</div>  
        </div>  
        <input id="rating" type="range" min="1" max="10" step="1" value="7" />  
  
        <div style="height:12px"></div>  
        <button class="btn primary" id="saveBtn">Guardar</button>  
        <div class="muted" id="saveHint" style="margin-top:10px;"></div>  
      </div>  
  
      <div style="height:14px"></div>  
  
      <div class="card">  
        <div class="row" style="justify-content:space-between;">  
          <div style="font-weight:600;">Últimos check-ins</div>  
          <button class="miniBtn" id="wipeBtn" title="Borra todo">Reset</button>  
        </div>  
        <div style="height:10px"></div>  
        <div class="list" id="recentList"></div>  
      </div>  
    </section>  
  
    <!-- STATS -->  
    <section id="tab-stats" style="display:none;">  
      <div class="card">  
        <div style="font-weight:600; margin-bottom:10px;">Media diaria (últimos 30 días)</div>  
        <canvas id="chart" width="800" height="220"></canvas>  
        <div class="muted" style="margin-top:8px;">La gráfica usa la media de la nota (1–10). Si hay mañana+noche, promedia.</div>  
      </div>  
  
      <div style="height:14px"></div>  
  
      <div class="card">  
        <div class="row" style="justify-content:space-between;">  
          <div style="font-weight:600;">Heatmap mensual</div>  
          <div class="row">  
            <button class="miniBtn" id="prevMonth">◀︎</button>  
            <div class="pill" id="monthTitle"></div>  
            <button class="miniBtn" id="nextMonth">▶︎</button>  
          </div>  
        </div>  
  
        <div style="height:10px"></div>  
        <div class="grid" id="dowRow"></div>  
        <div style="height:6px"></div>  
        <div class="grid" id="heatGrid"></div>  
  
        <div style="height:10px"></div>  
        <div class="muted">Color = intensidad según media 1–10. Sin datos = blanco.</div>  
      </div>  
  
      <div style="height:14px"></div>  
  
      <div class="card">  
        <div style="font-weight:600;">Resumen rápido</div>  
        <div style="height:10px"></div>  
        <div class="kpi" id="kpis"></div>  
      </div>  
    </section>  
  
    <!-- HELP -->  
    <section id="tab-help" style="display:none;">  
      <div class="card">  
        <div style="font-weight:600; margin-bottom:6px;">Instalación en iPhone (sin Mac)</div>  
        <ol>  
          <li>Abre esta web en <b>Safari</b> (no Chrome).</li>  
          <li>Botón <b>Compartir</b> → <b>Añadir a pantalla de inicio</b>.</li>  
          <li>Desde el icono se abre como “app”.</li>  
        </ol>  
        <div style="height:8px"></div>  
        <div style="font-weight:600; margin-bottom:6px;">Recordatorios a las 09:00 y 23:00</div>  
        <div class="muted">  
          Los hacemos con <b>Atajos</b> (Automatización personal) para que te salga una notificación y te abra la app.  
          Te dejo los pasos en el texto de abajo cuando publiques la web.  
        </div>  
      </div>  
    </section>  
  
    <div style="height:14px"></div>  
    <div class="muted">  
      Consejo: si Safari te recarga la app, no pasa nada: los datos están guardados en el dispositivo.  
    </div>  
  </div>  
  
<script>  
/* =========================  
   STORAGE (localStorage)  
========================= */  
const KEY = "mood_checkins_v1"; // { "<yyyy-mm-dd>": { morning:{face,rating,ts}, night:{...} } }  
  
function loadDB() {  
  try { return JSON.parse(localStorage.getItem(KEY) || "{}"); }  
  catch { return {}; }  
}  
function saveDB(db) {  
  localStorage.setItem(KEY, JSON.stringify(db));  
}  
function ymd(d) {  
  const yyyy = d.getFullYear();  
  const mm = String(d.getMonth()+1).padStart(2,"0");  
  const dd = String(d.getDate()).padStart(2,"0");  
  return `${yyyy}-${mm}-${dd}`;  
}  
function fmtDay(d) {  
  const opts = { day:"2-digit", month:"2-digit" };  
  return new Intl.DateTimeFormat("es-ES", opts).format(d);  
}  
function todayStart() { const d=new Date(); d.setHours(0,0,0,0); return d; }  
  
/* =========================  
   UI STATE  
========================= */  
let slot = "morning";     // morning/night  
let face = 0;             // 0/1/2  
let rating = 7;           // 1..10  
let monthAnchor = new Date();  
  
const tabs = document.querySelectorAll(".tab");  
const tabCheckin = document.getElementById("tab-checkin");  
const tabStats = document.getElementById("tab-stats");  
const tabHelp = document.getElementById("tab-help");  
  
function setTab(name) {  
  tabs.forEach(t => t.classList.toggle("active", t.dataset.tab === name));  
  tabCheckin.style.display = (name === "checkin") ? "" : "none";  
  tabStats.style.display   = (name === "stats")   ? "" : "none";  
  tabHelp.style.display    = (name === "help")    ? "" : "none";  
  if (name === "stats") { renderStats(); }  
}  
  
tabs.forEach(t => t.addEventListener("click", () => setTab(t.dataset.tab)));  
  
/* =========================  
   CHECKIN UI  
========================= */  
const slotMorning = document.getElementById("slotMorning");  
const slotNight   = document.getElementById("slotNight");  
const faceBtns    = document.querySelectorAll(".faceBtn");  
const ratingEl    = document.getElementById("rating");  
const ratingPill  = document.getElementById("ratingPill");  
const saveBtn     = document.getElementById("saveBtn");  
const saveHint    = document.getElementById("saveHint");  
const todayLabel  = document.getElementById("todayLabel");  
const recentList  = document.getElementById("recentList");  
const wipeBtn     = document.getElementById("wipeBtn");  
const exportBtn   = document.getElementById("exportBtn");  
  
function setSlot(newSlot) {  
  slot = newSlot;  
  slotMorning.classList.toggle("active", slot === "morning");  
  slotNight.classList.toggle("active", slot === "night");  
  loadExistingForToday();  
}  
  
slotMorning.addEventListener("click", () => setSlot("morning"));  
slotNight.addEventListener("click", () => setSlot("night"));  
  
faceBtns.forEach(btn => btn.addEventListener("click", () => {  
  face = Number(btn.dataset.face);  
  faceBtns.forEach(b => b.classList.toggle("active", Number(b.dataset.face) === face));  
}));  
  
ratingEl.addEventListener("input", (e) => {  
  rating = Number(e.target.value);  
  ratingPill.textContent = `${rating} / 10`;  
});  
  
function loadExistingForToday() {  
  const db = loadDB();  
  const k = ymd(todayStart());  
  const existing = db[k]?.[slot];  
  if (existing) {  
    face = existing.face;  
    rating = existing.rating;  
    faceBtns.forEach(b => b.classList.toggle("active", Number(b.dataset.face) === face));  
    ratingEl.value = rating;  
    ratingPill.textContent = `${rating} / 10`;  
    saveHint.textContent = "Ya había un check-in guardado. Puedes cambiarlo y guardar de nuevo.";  
  } else {  
    saveHint.textContent = "";  
    // no reseteo face para que no sea molesto; sí reseteo rating a un default razonable  
    rating = 7;  
    ratingEl.value = rating;  
    ratingPill.textContent = `${rating} / 10`;  
  }  
}  
  
saveBtn.addEventListener("click", () => {  
  const db = loadDB();  
  const k = ymd(todayStart());  
  db[k] = db[k] || {};  
  db[k][slot] = { face, rating, ts: Date.now() };  
  saveDB(db);  
  saveHint.textContent = "Guardado ✓";  
  renderRecent();  
});  
  
wipeBtn.addEventListener("click", () => {  
  if (!confirm("¿Seguro que quieres borrar todos los datos?")) return;  
  localStorage.removeItem(KEY);  
  saveHint.textContent = "Datos borrados.";  
  renderRecent();  
  renderStats();  
});  
  
exportBtn.addEventListener("click", () => {  
  const db = loadDB();  
  const blob = new Blob([JSON.stringify(db, null, 2)], {type:"application/json"});  
  const url = URL.createObjectURL(blob);  
  const a = document.createElement("a");  
  a.href = url;  
  a.download = "mood-checkins-export.json";  
  a.click();  
  URL.revokeObjectURL(url);  
});  
  
/* =========================  
   RECENT LIST  
========================= */  
const FACE_EMOJI = ["😞","😐","🙂"];  
const SLOT_EMOJI = { morning:"🌅", night:"🌙" };  
  
function renderRecent() {  
  const db = loadDB();  
  const keys = Object.keys(db).sort().reverse(); // newest first  
  const items = [];  
  
  for (const dayKey of keys) {  
    const dayObj = db[dayKey] || {};  
    for (const s of ["morning","night"]) {  
      if (!dayObj[s]) continue;  
      items.push({ dayKey, slot:s, ...dayObj[s] });  
    }  
  }  
  items.sort((a,b)=>b.ts-a.ts);  
  
  recentList.innerHTML = "";  
  (items.slice(0, 12)).forEach(it => {  
    const div = document.createElement("div");  
    div.className = "item";  
    const d = new Date(it.dayKey + "T00:00:00");  
    div.innerHTML = `  
      <div>  
        <div><b>${fmtDay(d)}</b> <span class="tag">${SLOT_EMOJI[it.slot]} ${it.slot==="morning"?"Mañana":"Noche"}</span></div>  
        <div class="muted">${FACE_EMOJI[it.face]} · ${it.rating}/10</div>  
      </div>  
      <button class="miniBtn">Editar</button>  
    `;  
    div.querySelector("button").addEventListener("click", () => {  
      setTab("checkin");  
      setSlot(it.slot);  
      // cargar exactamente ese día (por simplicidad, solo hoy editable “rápido”)  
      alert("Edición rápida está pensada para HOY.\nSi quieres editar días anteriores, te lo añado en 5 minutos.");  
    });  
    recentList.appendChild(div);  
  });  
  
  if (items.length === 0) {  
    recentList.innerHTML = `<div class="muted">Aún no hay datos. Haz tu primer check-in arriba.</div>`;  
  }  
}  
  
/* =========================  
   STATS  
========================= */  
const chart = document.getElementById("chart");  
const ctx = chart.getContext("2d");  
const dowRow = document.getElementById("dowRow");  
const heatGrid = document.getElementById("heatGrid");  
const monthTitle = document.getElementById("monthTitle");  
const prevMonth = document.getElementById("prevMonth");  
const nextMonth = document.getElementById("nextMonth");  
const kpis = document.getElementById("kpis");  
  
["L","M","X","J","V","S","D"].forEach(d => {  
  const el = document.createElement("div");  
  el.className = "dow";  
  el.textContent = d;  
  dowRow.appendChild(el);  
});  
  
prevMonth.addEventListener("click", ()=> { monthAnchor = addMonths(monthAnchor, -1); renderHeatmap(); });  
nextMonth.addEventListener("click", ()=> { monthAnchor = addMonths(monthAnchor, +1); renderHeatmap(); });  
  
function addMonths(d, delta) {  
  const nd = new Date(d);  
  nd.setMonth(nd.getMonth() + delta);  
  return nd;  
}  
  
function monthLabel(d) {  
  return new Intl.DateTimeFormat("es-ES", { month:"long", year:"numeric" }).format(d)  
    .replace(/^\w/, c=>c.toUpperCase());  
}  
  
function dailyAvgMap() {  
  // returns map dayKey -> avgRating (1..10)  
  const db = loadDB();  
  const out = {};  
  for (const dayKey of Object.keys(db)) {  
    const dayObj = db[dayKey] || {};  
    const vals = [];  
    if (dayObj.morning) vals.push(dayObj.morning.rating);  
    if (dayObj.night) vals.push(dayObj.night.rating);  
    if (vals.length) out[dayKey] = vals.reduce((a,b)=>a+b,0)/vals.length;  
  }  
  return out;  
}  
  
function renderChartLast30() {  
  const map = dailyAvgMap();  
  const end = todayStart();  
  const days = [];  
  for (let i=29; i>=0; i--) {  
    const d = new Date(end);  
    d.setDate(d.getDate() - i);  
    const key = ymd(d);  
    days.push({ d, key, avg: map[key] ?? null });  
  }  
  
  // draw  
  ctx.clearRect(0,0,chart.width,chart.height);  
  
  // padding + axes  
  const padL = 40, padR = 14, padT = 14, padB = 30;  
  const W = chart.width - padL - padR;  
  const H = chart.height - padT - padB;  
  
  // y scale 1..10  
  function y(v) { return padT + (10 - v) * (H / 9); }  
  function x(i) { return padL + (i * (W / (days.length-1))); }  
  
  // grid lines  
  ctx.strokeStyle = "#e7e7ea";  
  ctx.lineWidth = 1;  
  for (let v=1; v<=10; v+=1) {  
    const yy = y(v);  
    ctx.beginPath(); ctx.moveTo(padL, yy); ctx.lineTo(padL+W, yy); ctx.stroke();  
  }  
  
  // labels  
  ctx.fillStyle = "#666";  
  ctx.font = "12px -apple-system, Segoe UI, Arial";  
  [1,5,10].forEach(v=>{  
    ctx.fillText(String(v), 8, y(v)+4);  
  });  
  
  // line  
  ctx.strokeStyle = "#0a84ff";  
  ctx.lineWidth = 2;  
  ctx.beginPath();  
  let started = false;  
  days.forEach((p,i)=>{  
    if (p.avg == null) { started=false; return; }  
    const xx = x(i), yy = y(p.avg);  
    if (!started) { ctx.moveTo(xx,yy); started=true; }  
    else ctx.lineTo(xx,yy);  
  });  
  ctx.stroke();  
  
  // points  
  ctx.fillStyle = "#0a84ff";  
  days.forEach((p,i)=>{  
    if (p.avg == null) return;  
    const xx = x(i), yy = y(p.avg);  
    ctx.beginPath(); ctx.arc(xx,yy,3,0,Math.PI*2); ctx.fill();  
  });  
  
  // x labels (start/middle/end)  
  ctx.fillStyle = "#666";  
  const idxs = [0, Math.floor((days.length-1)/2), days.length-1];  
  idxs.forEach(i=>{  
    const p=days[i];  
    const label = fmtDay(p.d);  
    const xx = x(i) - 14;  
    ctx.fillText(label, Math.max(padL, xx), padT+H+22);  
  });  
}  
  
function heatColor(avg) {  
  if (avg == null) return "#ffffff";  
  // map 1..10 => alpha 0.15..0.85  
  const t = Math.min(1, Math.max(0, (avg-1)/9));  
  const a = 0.15 + 0.70*t;  
  // use accent blue with alpha on white background:  
  // approximate by mixing: color = (1-a)*white + a*blue(10,132,255)  
  const r = Math.round((1-a)*255 + a*10);  
  const g = Math.round((1-a)*255 + a*132);  
  const b = Math.round((1-a)*255 + a*255);  
  return `rgb(${r},${g},${b})`;  
}  
  
function renderHeatmap() {  
  const map = dailyAvgMap();  
  const cal = new Date(monthAnchor);  
  cal.setDate(1); cal.setHours(0,0,0,0);  
  
  const year = cal.getFullYear(), month = cal.getMonth();  
  const first = new Date(year, month, 1);  
  const last = new Date(year, month+1, 0);  
  const daysInMonth = last.getDate();  
  
  // weekday: JS 0=Sunday..6=Saturday. We want Monday first.  
  let weekday = first.getDay(); // 0..6  
  const mondayIndex = (weekday + 6) % 7; // Monday=0..Sunday=6  
  
  monthTitle.textContent = monthLabel(first);  
  
  heatGrid.innerHTML = "";  
  const totalCells = Math.ceil((mondayIndex + daysInMonth) / 7) * 7;  
  
  for (let i=0; i<totalCells; i++) {  
    const cell = document.createElement("div");  
  
    const dayNum = i - mondayIndex + 1;  
    if (dayNum < 1 || dayNum > daysInMonth) {  
      cell.className = "cell empty";  
      heatGrid.appendChild(cell);  
      continue;  
    }  
  
    const d = new Date(year, month, dayNum);  
    const key = ymd(d);  
    const avg = map[key] ?? null;  
    cell.className = "cell";  
    cell.textContent = String(dayNum);  
    cell.style.background = heatColor(avg);  
  
    // tap shows detail  
    cell.title = avg == null ? "Sin datos" : `Media: ${avg.toFixed(1)}/10`;  
    cell.addEventListener("click", () => {  
      const db = loadDB();  
      const obj = db[key] || {};  
      const m = obj.morning ? `${SLOT_EMOJI.morning} ${FACE_EMOJI[obj.morning.face]} ${obj.morning.rating}/10` : "🌅 —";  
      const n = obj.night   ? `${SLOT_EMOJI.night} ${FACE_EMOJI[obj.night.face]} ${obj.night.rating}/10` : "🌙 —";  
      alert(`${key}\n${m}\n${n}`);  
    });  
  
    heatGrid.appendChild(cell);  
  }  
}  
  
function renderKPIs() {  
  const db = loadDB();  
  const items = [];  
  for (const dayKey of Object.keys(db)) {  
    const o = db[dayKey] || {};  
    if (o.morning) items.push(o.morning);  
    if (o.night) items.push(o.night);  
  }  
  const count = items.length;  
  const avg = count ? (items.reduce((s,x)=>s+x.rating,0)/count) : null;  
  const faces = count ? items.reduce((acc,x)=>{acc[x.face]=(acc[x.face]||0)+1; return acc;},{}) : {};  
  
  kpis.innerHTML = "";  
  const pill = (text)=> {  
    const p = document.createElement("div");  
    p.className = "pill";  
    p.textContent = text;  
    return p;  
  };  
  
  kpis.appendChild(pill(`Check-ins: ${count}`));  
  kpis.appendChild(pill(`Media global: ${avg==null?"—":avg.toFixed(1)+"/10"}`));  
  kpis.appendChild(pill(`😞 ${faces[0]||0}`));  
  kpis.appendChild(pill(`😐 ${faces[1]||0}`));  
  kpis.appendChild(pill(`🙂 ${faces[2]||0}`));  
}  
  
function renderStats() {  
  renderChartLast30();  
  renderHeatmap();  
  renderKPIs();  
}  
  
/* =========================  
   INIT  
========================= */  
(function init() {  
  const d = new Date();  
  todayLabel.textContent = new Intl.DateTimeFormat("es-ES", { weekday:"long", day:"2-digit", month:"long" })  
    .format(d).replace(/^\w/, c=>c.toUpperCase());  
  
  monthAnchor = new Date();  
  renderRecent();  
  loadExistingForToday();  
})();  
</script>  
</body>  
</html>  
