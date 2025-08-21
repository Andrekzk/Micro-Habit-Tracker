<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Micro Habit Tracker</title>
<style>
  :root {
    --bg: #0f1221;
    --card: #141832;
    --surface: #1a1f3f;
    --surface-2: #212752;
    --text: #e9ecff;
    --muted: #9aa4d6;
    --accent: #6ee7cf; /* done */
    --warn: #ffd166;  /* skip */
    --danger: #ff6b6b;
    --focus: #8ab4ff;
    --shadow: 0 10px 30px rgba(0,0,0,.35);
  }
  @media (prefers-color-scheme: light) {
    :root {
      --bg: #f6f7fb;
      --card: #ffffff;
      --surface: #f0f2fb;
      --surface-2: #e7eaf7;
      --text: #0f1221;
      --muted: #5a638c;
      --accent: #14b8a6;
      --warn: #eab308;
      --danger: #ef4444;
      --focus: #2563eb;
    }
  }
  * { box-sizing: border-box; }
  html, body { height: 100%; }
  body {
    margin: 0;
    font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
    background: radial-gradient(1200px 600px at 10% -10%, rgba(110,231,207,.20), transparent 60%),
                radial-gradient(900px 500px at 110% 0%, rgba(99,102,241,.18), transparent 60%),
                var(--bg);
    color: var(--text);
  }
  header {
    padding: 24px 16px 12px;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 12px;
    align-items: center;
  }
  .brand {
    display: flex; gap: 12px; align-items: center;
  }
  .logo {
    width: 44px; height: 44px; border-radius: 12px;
    background: conic-gradient(from 210deg, #22d3ee, #34d399, #a78bfa, #fb7185, #22d3ee);
    filter: saturate(1.05) contrast(1.1);
    box-shadow: 0 8px 25px rgba(79,70,229,.35);
  }
  h1 { font-size: 20px; margin: 0; letter-spacing: .3px; }
  .tagline { margin: 2px 0 0; font-size: 13px; color: var(--muted); }

  .controls { display: flex; flex-wrap: wrap; gap: 8px; }
  button, .ghost {
    border: 0; border-radius: 12px; padding: 10px 12px; font-weight: 600;
    background: var(--surface); color: var(--text); cursor: pointer;
    box-shadow: 0 2px 0 rgba(0,0,0,.08) inset, 0 8px 18px rgba(0,0,0,.18);
    transition: transform .08s ease, filter .2s ease;
  }
  button:active { transform: translateY(1px) scale(.99); }
  button.primary { background: linear-gradient(180deg, #22c1c3, #1db2b3); color: #062a29; }
  button.warn { background: linear-gradient(180deg, #ffe08a, #f9c646); color: #3a2c00; }
  button.danger { background: linear-gradient(180deg, #ff9aa2, #ff6b6b); color: #32090b; }
  .ghost { background: transparent; color: var(--muted); }

  .app {
    padding: 8px 16px 28px;
    max-width: 1100px; margin: 0 auto;
  }
  .panel {
    background: var(--card);
    border: 1px solid rgba(255,255,255,.06);
    border-radius: 16px; padding: 14px; box-shadow: var(--shadow);
  }
  .row { display: flex; gap: 10px; align-items: center; flex-wrap: wrap; }
  .grow { flex: 1 1 200px; }
  input[type="text"], input[type="color"] {
    background: var(--surface); color: var(--text); border: 1px solid rgba(255,255,255,.08);
    padding: 10px 12px; border-radius: 12px; width: 100%; font-size: 14px;
    outline: none; box-shadow: 0 2px 0 rgba(0,0,0,.08) inset;
  }
  input[type="file"] { display: none; }
  label.file { cursor: pointer; }

  .meta { color: var(--muted); font-size: 12px; }

  .table { margin-top: 14px; overflow: auto; }
  table { width: 100%; border-collapse: collapse; min-width: 720px; }
  th, td { padding: 10px; text-align: left; border-bottom: 1px dotted rgba(255,255,255,.10); }
  th { font-size: 12px; color: var(--muted); font-weight: 700; letter-spacing: .06em; text-transform: uppercase; }
  tbody tr:hover { background: rgba(255,255,255,.03); }
  .nameCell { display:flex; align-items:center; gap:10px; }
  .swatch { width: 16px; height:16px; border-radius:4px; box-shadow: 0 0 0 2px rgba(0,0,0,.25) inset; }
  .rowActions { display:flex; gap:6px; }
  .iconBtn { background: var(--surface); padding: 6px 8px; border-radius: 10px; font-size: 13px; }

  .streak { font-weight: 800; }
  .hot { color: var(--accent); }

  .gridDays {
    display: grid;
    grid-auto-flow: column;
    grid-auto-columns: 20px;
    gap: 6px;
    align-items: center;
    overflow-x: auto; padding: 4px 0;
  }
  .day { width: 20px; height: 20px; border-radius: 6px; display: grid; place-items: center; font-size: 13px;
    background: var(--surface-2); color: var(--muted); user-select: none; cursor: pointer;
    border: 1px solid rgba(255,255,255,.06);
  }
  .day.done { background: var(--accent); color: #07312b; font-weight: 900; }
  .day.skip { background: var(--warn); color: #2e2300; font-weight: 900; }
  .day.today { outline: 2px solid var(--focus); }
  .dayLabel { font-size: 10px; color: var(--muted); text-align: center; margin-top: 6px; }

  .legend { display:flex; gap:10px; align-items:center; margin-top: 8px; color: var(--muted); font-size: 12px; }
  .pill { padding: 4px 8px; border-radius: 999px; background: var(--surface); border:1px solid rgba(255,255,255,.08); }

  .footer { margin-top: 16px; color: var(--muted); font-size: 12px; text-align: center; }

  @media (max-width: 780px) {
    header { grid-template-columns: 1fr; }
    .controls { justify-content: flex-start; }
    table { min-width: 640px; }
  }
</style>
</head>
<body>
  <header>
    <div class="brand">
      <div class="logo" aria-hidden="true"></div>
      <div>
        <h1>Micro Habit Tracker</h1>
        <p class="tagline">Small wins, every day. Keep your streaks burning. 🔥</p>
      </div>
    </div>
    <div class="controls">
      <button id="exportBtn" title="Export JSON">⬇️ Export</button>
      <label class="file ghost" title="Import JSON">
        ⬆️ Import
        <input id="importFile" type="file" accept="application/json" />
      </label>
    </div>
  </header>

  <main class="app">
    <section class="panel" aria-label="Add Habit">
      <div class="row">
        <input id="habitName" class="grow" type="text" placeholder="Add a habit (max 7)…" maxlength="40" />
        <input id="habitColor" type="color" value="#6ee7cf" title="Pick a color" />
        <button id="addHabit" class="primary">＋ Add</button>
      </div>
      <div class="row" style="margin-top:8px;">
        <span class="meta" id="todayMeta"></span>
        <span class="meta" style="margin-left:auto;">Tip: tap a day to toggle ◻ → ✓ → ⏭</span>
      </div>
    </section>

    <section class="panel table" aria-label="Habits Table">
      <table>
        <thead>
          <tr>
            <th style="width:260px;">Habit</th>
            <th>Streak</th>
            <th>7d %</th>
            <th>Last days</th>
            <th>Actions</th>
          </tr>
        </thead>
        <tbody id="habitBody"></tbody>
      </table>
      <div class="legend">
        <span class="pill">✓ done</span>
        <span class="pill">⏭ skip (doesn't break streak)</span>
        <span class="pill">◻ no entry</span>
      </div>
    </section>

    <p class="footer">Your data is stored locally in your browser. Export regularly if it matters to you.</p>
  </main>

<script>
(() => {
  const MAX_HABITS = 7;
  const DAYS_TO_SHOW = 21; // last N days
  const LS_KEY = 'microHabitDataV1';

  const els = {
    body: document.getElementById('habitBody'),
    name: document.getElementById('habitName'),
    color: document.getElementById('habitColor'),
    add: document.getElementById('addHabit'),
    todayMeta: document.getElementById('todayMeta'),
    exportBtn: document.getElementById('exportBtn'),
    importFile: document.getElementById('importFile'),
  };

  function fmtDate(d){
    const y = d.getFullYear();
    const m = String(d.getMonth()+1).padStart(2,'0');
    const day = String(d.getDate()).padStart(2,'0');
    return `${y}-${m}-${day}`;
  }
  function fromISO(s){
    const [y,m,d] = s.split('-').map(Number);
    return new Date(y, m-1, d);
  }
  function todayStr(){ return fmtDate(new Date()); }
  function daysBackArray(n){
    const arr=[]; const t=new Date();
    for(let i=n-1;i>=0;i--){ const d=new Date(t); d.setDate(t.getDate()-i); arr.push(fmtDate(d)); }
    return arr;
  }
  function dayLabel(iso){
    const d = fromISO(iso);
    return d.toLocaleDateString(undefined,{ weekday:'short', month:'short', day:'numeric'});
  }

  function load(){
    const raw = localStorage.getItem(LS_KEY);
    if(!raw){
      const demo = demoData();
      localStorage.setItem(LS_KEY, JSON.stringify(demo));
      return demo;
    }
    try{
      const obj = JSON.parse(raw);
      if(!obj.version) obj.version = 1;
      return obj;
    }catch(e){
      console.warn('Failed to parse data; resetting to demo.', e);
      const demo = demoData();
      localStorage.setItem(LS_KEY, JSON.stringify(demo));
      return demo;
    }
  }
  function save(){ localStorage.setItem(LS_KEY, JSON.stringify(state)); }

  function uid(){ return Math.random().toString(36).slice(2,9); }

  function demoData(){
    const base = { version:1, habits:[], settings:{ daysToShow: DAYS_TO_SHOW } };
    const days = daysBackArray(10);
    const patterns = [
      ['done','done','done','skip','','done','','done','done','done'],
      ['','done','','done','','skip','done','','done',''],
      ['done','','done','','done','done','','skip','done',''],
    ];
    const names = [
      {name:'Hydrate 2L', color:'#6ee7cf'},
      {name:'Stretch 10m', color:'#a78bfa'},
      {name:'Read 10 pages', color:'#60a5fa'},
    ];
    names.forEach((n,i)=>{
      const h = { id: uid(), name:n.name, color:n.color, history:{} };
      days.forEach((d,idx)=>{ const val = patterns[i][idx]||''; if(val) h.history[d]=val; });
      base.habits.push(h);
    });
    return base;
  }

  let state = load();

  function canAddMore(){ return state.habits.length < MAX_HABITS; }

  function addHabit(){
    const name = els.name.value.trim();
    if(!name) return;
    if(!canAddMore()){ alert(`Limit reached (max ${MAX_HABITS}). Delete one to add another.`); return; }
    const h = { id: uid(), name, color: els.color.value || '#6ee7cf', history:{} };
    state.habits.push(h); save(); els.name.value=''; render();
  }

  function editHabit(id){
    const h = state.habits.find(x=>x.id===id); if(!h) return;
    const newName = prompt('Rename habit:', h.name);
    if(newName && newName.trim()){ h.name = newName.trim(); save(); render(); }
  }
  function recolorHabit(id){
    const h = state.habits.find(x=>x.id===id); if(!h) return;
    const c = prompt('Set HEX color (e.g. #14b8a6):', h.color);
    if(c && /^#([0-9a-f]{3}|[0-9a-f]{6})$/i.test(c)){ h.color = c; save(); render(); }
  }
  function deleteHabit(id){
    const h = state.habits.find(x=>x.id===id); if(!h) return;
    if(confirm(`Delete “${h.name}”? This cannot be undone.`)){
      state.habits = state.habits.filter(x=>x.id!==id); save(); render();
    }
  }

  function toggleCell(id, date){
    const h = state.habits.find(x=>x.id===id); if(!h) return;
    const curr = h.history[date] || '';
    const next = curr==='' ? 'done' : (curr==='done' ? 'skip' : '');
    if(next==='') delete h.history[date]; else h.history[date]=next;
    save(); updateRow(id);
  }

  function setTodaySkip(id){ const d=todayStr(); const h=state.habits.find(x=>x.id===id); if(!h) return; h.history[d]='skip'; save(); updateRow(id); }
  function setTodayDone(id){ const d=todayStr(); const h=state.habits.find(x=>x.id===id); if(!h) return; h.history[d]='done'; save(); updateRow(id); }

  function computeStreak(habit){
    let streak=0; const start = new Date();
    for(let i=0;i<3650;i++){
      const d = new Date(start); d.setDate(start.getDate()-i);
      const key = fmtDate(d);
      const val = habit.history[key] || '';
      if(val==='skip') continue; // skip doesn't break or add
      if(val==='done') { streak++; } else { break; }
    }
    return streak;
  }

  function percent7d(habit){
    let done=0, total=0; const t=new Date();
    for(let i=0;i<7;i++){ const d=new Date(t); d.setDate(t.getDate()-i); const k=fmtDate(d); const v=habit.history[k]||''; if(v!=='skip') total++; if(v==='done') done++; }
    return total? Math.round((done/total)*100): 0;
  }

  function render(){
    els.todayMeta.textContent = `Today: ${dayLabel(todayStr())}`;
    els.add.disabled = !canAddMore();
    els.add.title = canAddMore()? 'Add habit' : `Limit reached (max ${MAX_HABITS})`;
    els.body.innerHTML = '';
    state.habits.forEach(h=>{
      els.body.appendChild(renderRow(h));
    });
  }

  function renderRow(h){
    const tr = document.createElement('tr'); tr.id = `row-${h.id}`;

    // Habit cell
    const nameTd = document.createElement('td'); nameTd.className = 'nameCell';
    const sw = document.createElement('span'); sw.className='swatch'; sw.style.background = h.color; nameTd.appendChild(sw);
    const name = document.createElement('span'); name.textContent = h.name; nameTd.appendChild(name);
    tr.appendChild(nameTd);

    // Streak
    const stTd = document.createElement('td'); stTd.innerHTML = `<span class="streak hot">🔥 ${computeStreak(h)}</span>`; tr.appendChild(stTd);

    // 7d %
    const pTd = document.createElement('td'); pTd.textContent = percent7d(h) + '%'; tr.appendChild(pTd);

    // Days grid
    const daysTd = document.createElement('td');
    const grid = document.createElement('div'); grid.className='gridDays';
    const days = daysBackArray(DAYS_TO_SHOW);
    days.forEach(d=>{
      const div = document.createElement('div');
      div.className='day';
      const v = h.history[d] || '';
      if(v==='done'){ div.classList.add('done'); div.textContent='✓'; }
      if(v==='skip'){ div.classList.add('skip'); div.textContent='⏭'; }
      if(d===todayStr()) div.classList.add('today');
      div.title = `${dayLabel(d)} — ${v||'no entry'}`;
      div.dataset.date = d; div.dataset.id = h.id;
      grid.appendChild(div);
    });
    daysTd.appendChild(grid); tr.appendChild(daysTd);

    // Actions
    const act = document.createElement('td'); act.className='rowActions';
    act.appendChild(iconButton('✓ Today', ()=>setTodayDone(h.id)));
    act.appendChild(iconButton('⏭ Skip', ()=>setTodaySkip(h.id)));
    act.appendChild(iconButton('✏️ Rename', ()=>editHabit(h.id)));
    act.appendChild(iconButton('🎨 Color', ()=>recolorHabit(h.id)));
    act.appendChild(iconButton('🗑️', ()=>deleteHabit(h.id), 'danger'));
    tr.appendChild(act);

    // delegate clicks for grid
    tr.addEventListener('click', (e)=>{
      const t = e.target;
      if(t.classList.contains('day')){
        toggleCell(h.id, t.dataset.date);
      }
    });

    return tr;
  }

  function updateRow(id){
    const idx = state.habits.findIndex(h=>h.id===id); if(idx<0) return;
    const trOld = document.getElementById(`row-${id}`);
    const trNew = renderRow(state.habits[idx]);
    trOld.replaceWith(trNew);
  }

  function iconButton(label, onClick, kind){
    const b = document.createElement('button'); b.className='iconBtn'+(kind? ' '+kind : ''); b.textContent = label; b.addEventListener('click', (e)=>{ e.stopPropagation(); onClick(); }); return b;
  }

  // Export / Import
  els.exportBtn.addEventListener('click', ()=>{
    const data = JSON.stringify(state, null, 2);
    const blob = new Blob([data], {type:'application/json'});
    const a = document.createElement('a');
    const date = todayStr().replaceAll('-','');
    a.href = URL.createObjectURL(blob);
    a.download = `micro_habits_${date}.json`;
    document.body.appendChild(a); a.click(); a.remove();
    setTimeout(()=>URL.revokeObjectURL(a.href), 2000);
  });

  els.importFile.addEventListener('change', (e)=>{
    const file = e.target.files && e.target.files[0]; if(!file) return;
    const reader = new FileReader();
    reader.onload = (ev)=>{
      try{
        const obj = JSON.parse(String(ev.target.result||'{}'));
        if(!obj || !Array.isArray(obj.habits)) throw new Error('Invalid file');
        state = { version: obj.version||1, habits: obj.habits, settings: obj.settings||{daysToShow:DAYS_TO_SHOW} };
        save(); render();
        alert('Import successful.');
      }catch(err){ alert('Import failed: '+ err.message); }
    };
    reader.readAsText(file);
    // reset file input to allow importing the same file again
    e.target.value = '';
  });

  // Add habit
  els.add.addEventListener('click', addHabit);
  els.name.addEventListener('keydown', (e)=>{ if(e.key==='Enter') addHabit(); });

  // init
  render();
})();
</script>
</body>
</html>
