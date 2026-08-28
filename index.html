<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>HabitFlow — Fieldbook</title>
<meta name="description" content="A personal habit ledger and day-by-day memory journal.">

<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#3f6146">
<link rel="icon" type="image/png" sizes="192x192" href="icon-192.png">
<link rel="icon" href="favicon.ico">

<!-- iOS home-screen support (iOS ignores the manifest for install behavior) -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="HabitFlow">
<link rel="apple-touch-icon" href="apple-touch-icon.png">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,600;9..144,700;9..144,900&family=Public+Sans:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#f2ecdd;
    --paper-deep:#eae2cc;
    --card:#fbf7ec;
    --line:#d9cfb2;
    --ink:#242a1f;
    --ink-soft:#5c6152;
    --moss:#3f6146;
    --moss-deep:#2c4632;
    --moss-wash:#e4ead9;
    --clay:#a8492c;
    --clay-deep:#832f19;
    --clay-wash:#f4dfd0;
    --gold:#b4842c;
    --gold-wash:#f1e3c2;
    --shadow: 0 18px 34px rgba(36,42,31,0.14);
  }
  *{box-sizing:border-box;}
  html,body{margin:0;padding:0;}
  body{
    background:var(--paper);
    color:var(--ink);
    font-family:"Public Sans", sans-serif;
    background-image:
      radial-gradient(circle at 1px 1px, rgba(36,42,31,0.06) 1px, transparent 0);
    background-size: 16px 16px;
  }
  h1,h2,h3{
    font-family:"Fraunces", serif;
    margin:0;
  }
  button{font-family:inherit;border:0;background:none;cursor:pointer;color:inherit;}
  input,textarea,select{font-family:inherit;font-size:0.92rem;color:var(--ink);}
  .mono{font-family:"IBM Plex Mono", monospace; letter-spacing:0.02em;}

  .shell{
    max-width:460px;
    margin:0 auto;
    min-height:100vh;
    background:var(--paper);
    display:flex;
    flex-direction:column;
    box-shadow:0 0 0 1px rgba(36,42,31,0.06);
  }

  /* ---------- top bar ---------- */
  .topbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:16px 20px;
    border-bottom:1px solid var(--line);
    position:sticky;
    top:0;
    z-index:20;
    background:rgba(242,236,221,0.94);
    backdrop-filter:blur(10px);
  }
  .brand{display:flex;align-items:center;gap:10px;}
  .brand-mark{
    width:34px;height:34px;border-radius:8px;
    background:var(--moss);
    color:var(--paper);
    display:grid;place-items:center;
    font-family:"Fraunces",serif;font-weight:700;font-size:0.95rem;
    transform:rotate(-4deg);
  }
  .brand span{font-family:"Fraunces",serif;font-weight:700;font-size:1.08rem;letter-spacing:-0.01em;}
  .streak-tag{
    display:flex;align-items:center;gap:6px;
    padding:6px 10px;
    border:1px solid var(--line);
    border-radius:999px;
    font-size:0.7rem;
    font-weight:700;
    color:var(--clay-deep);
    background:var(--clay-wash);
  }
  .topbar-right{display:flex;align-items:center;gap:8px;}
  .lang-select{
    border:1px solid var(--line);
    border-radius:999px;
    padding:6px 8px;
    font-size:0.72rem;
    font-weight:700;
    color:var(--ink-soft);
    background:var(--card);
  }
  .lang-select:hover{border-color:var(--moss);color:var(--moss);}

  /* ---------- views ---------- */
  main{flex:1;padding-bottom:92px;overflow-x:hidden;}
  .view{display:none;}
  .view.active{display:block;}

  /* ---------- cover / hero ---------- */
  .cover{
    position:relative;
    padding:26px 22px 34px;
    color:var(--paper);
    background:linear-gradient(150deg, var(--moss) 0%, var(--moss-deep) 100%);
    overflow:hidden;
  }
  .cover.cover-clay{ background:linear-gradient(150deg, var(--clay) 0%, var(--clay-deep) 100%); }
  .cover.cover-ink{ background:linear-gradient(150deg, #2f362a 0%, #1b2018 100%); }
  .cover-eyebrow{
    font-family:"IBM Plex Mono",monospace;
    font-size:0.68rem;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:rgba(242,236,221,0.7);
    margin-bottom:8px;
  }
  .cover h1{font-size:1.7rem;font-weight:700;line-height:1.1;letter-spacing:-0.01em;margin-bottom:6px;}
  .name-edit{
    font-family:inherit;font-size:inherit;font-weight:inherit;color:inherit;
    background:none;border:0;border-bottom:1.5px dashed rgba(242,236,221,0.5);
    padding:0 1px;cursor:pointer;
  }
  .name-edit:hover{border-bottom-color:rgba(242,236,221,0.9);}
  .cover p.lede{color:rgba(242,236,221,0.72);font-size:0.84rem;line-height:1.5;max-width:78%;}
  .deckle{display:block;width:100%;height:16px;position:relative;top:1px;}

  .stamp-corner{
    position:absolute;
    top:20px;right:20px;
    width:78px;height:78px;
    border-radius:50%;
    border:2px solid rgba(242,236,221,0.55);
    display:grid;place-items:center;
    text-align:center;
    transform:rotate(9deg);
    clip-path: polygon(50% 0%, 61% 4%, 72% 2%, 80% 10%, 92% 12%, 96% 22%, 100% 32%,
      97% 43%, 100% 54%, 94% 63%, 96% 74%, 87% 80%, 82% 90%, 71% 90%, 62% 98%,
      50% 94%, 38% 98%, 29% 90%, 18% 90%, 13% 80%, 4% 74%, 6% 63%, 0% 54%,
      3% 43%, 0% 32%, 4% 22%, 8% 12%, 20% 10%, 28% 2%, 39% 4%);
  }
  .stamp-corner strong{display:block;font-family:"Fraunces",serif;font-size:1.05rem;font-weight:700;color:#fff;}
  .stamp-corner span{display:block;font-family:"IBM Plex Mono",monospace;font-size:0.55rem;letter-spacing:0.08em;text-transform:uppercase;color:rgba(255,255,255,0.75);}

  /* ---------- ledger cards ---------- */
  .ledger-card{
    margin:16px 18px 0;
    background:var(--card);
    border:1px solid var(--line);
    border-radius:4px;
    padding:18px;
    box-shadow:0 1px 0 var(--line);
  }
  .ledger-head{
    display:flex;align-items:baseline;justify-content:space-between;
    gap:10px;margin-bottom:14px;
    border-bottom:1px dashed var(--line);
    padding-bottom:10px;
  }
  .ledger-head h2{font-size:1.02rem;font-weight:700;}
  .ledger-head .count{font-family:"IBM Plex Mono",monospace;font-size:0.72rem;color:var(--ink-soft);}

  .chip-group{display:flex;gap:6px;flex-wrap:wrap;}
  .chip{
    padding:5px 11px;border:1px solid var(--line);border-radius:999px;
    font-size:0.68rem;font-weight:700;color:var(--ink-soft);background:var(--paper);
  }
  .chip.active{background:var(--moss);border-color:var(--moss);color:var(--paper);}

  .entry-row-form{display:flex;gap:8px;}
  .entry-row-form input{
    flex:1;border:0;border-bottom:1.5px solid var(--line);
    padding:9px 2px;background:transparent;outline:none;
  }
  .entry-row-form input:focus{border-color:var(--moss);}
  .entry-row-form button{
    padding:9px 16px;border-radius:4px;background:var(--ink);color:var(--paper);
    font-weight:700;font-size:0.8rem;
  }

  /* ---------- ledger rows (habits) ---------- */
  .ledger-list{display:flex;flex-direction:column;}
  .ledger-row{
    display:flex;align-items:center;gap:12px;
    padding:12px 0;
    border-bottom:1px dotted var(--line);
  }
  .ledger-row:last-child{border-bottom:0;}

  .stamp-toggle{
    flex:0 0 auto;width:38px;height:38px;border-radius:50%;
    border:1.5px solid var(--line);
    display:grid;place-items:center;
    color:transparent;
    transition:transform .15s ease;
  }
  .stamp-toggle:active{transform:scale(0.9);}
  .stamp-toggle.done{
    border:none;
    background:var(--moss);
    color:var(--paper);
    transform:rotate(-8deg);
    clip-path: polygon(50% 2%, 63% 6%, 76% 3%, 85% 13%, 96% 17%, 98% 29%,
      100% 40%, 95% 50%, 100% 61%, 96% 72%, 87% 79%, 82% 90%, 70% 89%,
      60% 98%, 50% 92%, 40% 98%, 30% 89%, 18% 90%, 13% 79%, 4% 72%,
      0% 61%, 5% 50%, 0% 40%, 2% 29%, 4% 17%, 15% 13%, 24% 3%, 37% 6%);
  }
  .stamp-toggle.done::after{content:"✓";font-size:1rem;font-weight:800;}

  .ledger-row-main{flex:1;display:flex;align-items:baseline;gap:8px;min-width:0;}
  .ledger-name{font-weight:600;font-size:0.9rem;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;}
  .ledger-row.is-done .ledger-name{color:var(--ink-soft);}
  .ledger-leader{flex:1;border-bottom:1px dotted var(--line);height:0;transform:translateY(-4px);min-width:16px;}
  .ledger-streak{
    flex:0 0 auto;font-family:"IBM Plex Mono",monospace;font-size:0.7rem;font-weight:600;
    color:var(--clay-deep);white-space:nowrap;
  }

  .ledger-row-actions{flex:0 0 auto;display:flex;align-items:center;gap:2px;}
  .row-icon-btn{
    width:26px;height:26px;border-radius:6px;
    display:grid;place-items:center;
    color:var(--ink-soft);font-size:0.7rem;
    border:1px solid transparent;
  }
  .row-icon-btn:hover{background:var(--paper);border-color:var(--line);}
  .row-icon-btn:disabled{opacity:0.25;cursor:default;}
  .row-icon-btn:disabled:hover{background:none;border-color:transparent;}
  .row-icon-btn.danger{color:var(--clay-deep);}
  .row-icon-btn.danger:hover{background:var(--clay-wash);border-color:var(--clay);}

  .ghost-link{font-size:0.72rem;font-weight:700;color:var(--ink-soft);text-decoration:underline;text-underline-offset:3px;}
  .empty-note{padding:16px 4px;color:var(--ink-soft);font-size:0.82rem;font-style:italic;}

  .backup-card{margin-bottom:24px;}
  .backup-note{font-size:0.78rem;color:var(--ink-soft);line-height:1.5;margin-bottom:14px;}
  .backup-actions{display:flex;gap:8px;flex-wrap:wrap;}
  .ghost-button-wide{
    flex:1;min-width:140px;text-align:center;
    padding:10px 12px;border:1px solid var(--line);border-radius:4px;
    font-size:0.76rem;font-weight:700;color:var(--ink-soft);cursor:pointer;
  }
  .ghost-button-wide:hover{border-color:var(--moss);color:var(--moss);}

  /* ---------- calendar / journal page ---------- */
  .notebook{
    background-image: repeating-linear-gradient(var(--card) 0px, var(--card) 27px, var(--line) 28px);
    border:1px solid var(--line);
    border-radius:3px;
    padding:14px 14px 14px 18px;
    border-left:3px solid var(--clay);
    width:100%;
    min-height:150px;
    resize:vertical;
    outline:none;
    line-height:28px;
    font-size:0.9rem;
  }
  .field{margin-bottom:14px;}
  .field label{
    display:block;margin-bottom:6px;font-size:0.68rem;font-weight:700;
    text-transform:uppercase;letter-spacing:0.08em;color:var(--ink-soft);
  }
  .field input[type="date"]{
    border:1px solid var(--line);border-radius:4px;padding:9px 10px;background:var(--paper);width:100%;
  }
  .file-tab{
    display:inline-flex;align-items:center;gap:8px;
    padding:9px 14px;border:1px dashed var(--line);border-radius:4px;
    font-size:0.78rem;font-weight:700;color:var(--ink-soft);cursor:pointer;
  }
  .file-tab:hover{border-color:var(--moss);color:var(--moss);}

  .polaroid{
    margin-top:16px;background:#fff;padding:10px 10px 34px;
    border:1px solid var(--line);border-radius:2px;
    box-shadow:var(--shadow);
    transform:rotate(-1.4deg);
    max-width:220px;
  }
  .polaroid img,.polaroid video,.polaroid .no-photo{
    display:block;width:100%;height:150px;object-fit:cover;background:var(--moss-wash);
  }
  .polaroid .no-photo{display:grid;place-items:center;color:var(--ink-soft);font-size:0.72rem;}
  .media-actions{
    display:flex;gap:8px;margin-top:10px;
  }
  .media-action{
    flex:1;padding:8px 10px;border:1px solid var(--line);border-radius:4px;
    font-size:0.72rem;font-weight:700;color:var(--ink-soft);background:var(--paper);
  }
  .media-action:hover{border-color:var(--moss);color:var(--moss);}
  .media-action.danger{color:var(--clay-deep);}
  .media-action.danger:hover{border-color:var(--clay);background:var(--clay-wash);}
  .polaroid figcaption{
    margin-top:8px;font-family:"Fraunces",serif;font-style:italic;font-size:0.78rem;color:var(--ink-soft);
    text-align:center;
  }

  .primary-button{
    width:100%;margin-top:14px;padding:13px;border-radius:4px;
    background:var(--clay);color:#fff;font-weight:700;font-size:0.86rem;
    transition:transform .1s ease;
  }
  .primary-button:active{transform:scale(0.98);}

  /* ---------- month calendar ---------- */
  .calendar-nav{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px;}
  .calendar-nav button{
    width:30px;height:30px;border-radius:50%;border:1px solid var(--line);
    display:grid;place-items:center;font-size:0.9rem;color:var(--ink-soft);
  }
  .calendar-nav button:hover{border-color:var(--moss);color:var(--moss);}
  .calendar-nav h3{font-family:"Fraunces",serif;font-size:0.98rem;font-weight:700;}
  .calendar-weekdays,.calendar-grid{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;}
  .calendar-weekdays span{
    text-align:center;font-size:0.6rem;font-weight:700;color:var(--ink-soft);
    text-transform:uppercase;letter-spacing:0.04em;padding-bottom:6px;
  }
  .calendar-day{
    position:relative;aspect-ratio:1;display:flex;align-items:center;justify-content:center;
    border-radius:4px;border:1px solid transparent;
    font-family:"IBM Plex Mono",monospace;font-size:0.76rem;color:var(--ink);
    background:transparent;
  }
  .calendar-day.pad{visibility:hidden;}
  .calendar-day:hover{border-color:var(--line);}
  .calendar-day.today{font-weight:700;color:var(--clay-deep);}
  .calendar-day.selected{background:var(--moss);color:var(--paper);font-weight:700;}
  .calendar-day .entry-dot{
    position:absolute;bottom:4px;left:50%;transform:translateX(-50%);
    width:5px;height:5px;border-radius:50%;background:var(--clay);
  }
  .calendar-day.selected .entry-dot{background:var(--paper);}
  .calendar-day .media-dot{background:var(--gold);}

  /* ---------- bottom nav ---------- */
  .bottom-nav{
    position:fixed;left:50%;transform:translateX(-50%);bottom:0;
    width:100%;max-width:460px;
    display:grid;grid-template-columns:repeat(2,1fr);
    background:var(--card);border-top:1px solid var(--line);
    padding:8px;z-index:30;
  }
  .nav-btn{
    display:flex;flex-direction:column;align-items:center;gap:3px;
    padding:8px 4px;border-radius:4px;font-size:0.66rem;font-weight:700;color:var(--ink-soft);
  }
  .nav-btn .dot{width:5px;height:5px;border-radius:50%;background:transparent;}
  .nav-btn.active{color:var(--moss-deep);}
  .nav-btn.active .dot{background:var(--clay);}

  @media (min-width:520px){
    .shell{margin:20px auto;border-radius:10px;overflow:hidden;box-shadow:var(--shadow);min-height:calc(100vh - 40px);}
    .bottom-nav{border-radius:0 0 10px 10px;}
  }
</style>
</head>
<body>
<div class="shell">

  <header class="topbar">
    <div class="brand">
      <div class="brand-mark">Hf</div>
      <span>HabitFlow</span>
    </div>
    <div class="streak-tag">🔥 <span id="top-streak-pill">0 day streak</span></div>
  </header>

  <main>

    <!-- HOME -->
    <section class="view active" data-view="home">
      <section class="cover">
        <p class="cover-eyebrow" id="cover-date">TODAY</p>
        <h1 id="hero-title"><span id="home-greeting">Good morning,</span> <button type="button" id="edit-name-btn" class="name-edit">there</button></h1>
        <p class="lede" id="home-lede">Every small entry adds up to something worth keeping.</p>
        <div class="stamp-corner"><div><strong id="ring-count">0/0</strong><span id="home-done-label">done</span></div></div>
        <svg class="deckle" viewBox="0 0 480 26" preserveAspectRatio="none"><path d="M0,26 L0,0 L20.0,14 L40.0,0 L60.0,14 L80.0,0 L100.0,14 L120.0,0 L140.0,14 L160.0,0 L180.0,14 L200.0,0 L220.0,14 L240.0,0 L260.0,14 L280.0,0 L300.0,14 L320.0,0 L340.0,14 L360.0,0 L380.0,14 L400.0,0 L420.0,14 L440.0,0 L460.0,14 L480.0,0 L480,26 Z" fill="var(--paper)"/></svg>
      </section>

      <section class="ledger-card">
        <div class="ledger-head"><h2 id="entry-heading">New entry</h2></div>
        <form id="habit-form" class="entry-row-form">
          <input id="habit-input" type="text" placeholder="A habit worth keeping..." autocomplete="off">
          <button type="submit" id="add-habit-button">Add</button>
        </form>
      </section>

      <section class="ledger-card">
        <div class="ledger-head">
          <h2 id="ledger-heading">Today's ledger</h2>
          <button class="ghost-link" id="reset-today-button" type="button">reset</button>
        </div>
        <div class="chip-group" id="habit-filters">
          <button class="chip active" data-habit-filter="all">All</button>
          <button class="chip" data-habit-filter="active">Active</button>
          <button class="chip" data-habit-filter="done">Done</button>
        </div>
        <div id="habit-list" class="ledger-list" style="margin-top:12px;"></div>
      </section>

      <section class="ledger-card backup-card">
        <div class="ledger-head"><h2>Backup</h2></div>
        <p class="backup-note">Everything here lives only on this device. Export a backup now and then so nothing gets lost if you clear your browser or switch phones.</p>
        <div class="backup-actions">
          <button type="button" id="export-button" class="ghost-button-wide">⬇ Export backup</button>
          <label class="ghost-button-wide" for="import-input">⬆ Import backup</label>
          <input id="import-input" type="file" accept="application/json" hidden>
        </div>
      </section>
    </section>

    <!-- CALENDAR -->
    <section class="view" data-view="calendar">
      <section class="cover cover-clay">
        <p class="cover-eyebrow" id="cal-eyebrow">MEMORY LANE</p>
        <h1 id="cal-title-text">Field notes</h1>
        <p class="lede" id="cal-lede"><span id="memory-count">0</span> pages written so far</p>
        <svg class="deckle" viewBox="0 0 480 26" preserveAspectRatio="none"><path d="M0,26 L0,0 L20.0,14 L40.0,0 L60.0,14 L80.0,0 L100.0,14 L120.0,0 L140.0,14 L160.0,0 L180.0,14 L200.0,0 L220.0,14 L240.0,0 L260.0,14 L280.0,0 L300.0,14 L320.0,0 L340.0,14 L360.0,0 L380.0,14 L400.0,0 L420.0,14 L440.0,0 L460.0,14 L480.0,0 L480,26 Z" fill="var(--paper)"/></svg>
      </section>

      <section class="ledger-card">
        <div class="calendar-nav">
          <button type="button" id="cal-prev">‹</button>
          <h3 id="cal-month-label">Month Year</h3>
          <button type="button" id="cal-next">›</button>
        </div>
        <div class="calendar-weekdays" id="calendar-weekdays"></div>
        <div id="calendar-grid" class="calendar-grid"></div>
      </section>

      <section class="ledger-card">
        <div class="field">
          <label for="memory-date" id="cal-selected-day-label">Selected day</label>
          <input id="memory-date" type="date">
        </div>
        <div class="field">
          <label for="memory-text" id="cal-entry-label">Entry</label>
          <textarea id="memory-text" class="notebook" placeholder="Write wins, lessons, or anything worth remembering..."></textarea>
        </div>
        <div class="field">
          <label id="cal-attach-label">Attach a photo or video</label>
          <label class="file-tab" for="memory-photo" id="cal-file-tab">📎 choose a photo or video</label>
          <input id="memory-photo" type="file" accept="image/*,video/*" hidden>
          <div class="media-actions">
            <button id="remove-memory-media-button" class="media-action danger" type="button" style="display:none;">✕ Remove media</button>
          </div>
        </div>
        <button id="save-memory-button" class="primary-button" type="button">Pin to this page</button>
        <figure class="polaroid" id="memory-preview" style="display:none;">
          <div class="no-photo">no photo or video attached</div>
          <figcaption>—</figcaption>
        </figure>
      </section>
    </section>

  </main>

  <nav class="bottom-nav">
    <button class="nav-btn active" data-view="home"><span class="dot"></span><span class="label" id="nav-label-home">Home</span></button>
    <button class="nav-btn" data-view="calendar"><span class="dot"></span><span class="label" id="nav-label-calendar">Field notes</span></button>
  </nav>
</div>

<script>
const $ = (id) => document.getElementById(id);

const habitForm = $("habit-form");
const habitInput = $("habit-input");
const habitList = $("habit-list");
const resetTodayButton = $("reset-today-button");
const habitFilterButtons = document.querySelectorAll("[data-habit-filter]");
const exportButton = $("export-button");
const importInput = $("import-input");

const memoryDate = $("memory-date");
const memoryText = $("memory-text");
const memoryPhoto = $("memory-photo");
const memoryPreview = $("memory-preview");
const removeMemoryMediaButton = $("remove-memory-media-button");
const saveMemoryButton = $("save-memory-button");
const memoryCount = $("memory-count");
const calGrid = $("calendar-grid");
const calMonthLabel = $("cal-month-label");
const calPrev = $("cal-prev");
const calNext = $("cal-next");

const MAX_DAY_MEDIA_BYTES = 15 * 1024 * 1024;
let draftDayMedia = null; // { dataUrl, type } pending for the selected day
let mediaMarkedForDeletion = false;
let calViewYear, calViewMonth; // 0-indexed month for the grid currently shown

const heroTitle = $("hero-title");
const homeGreeting = $("home-greeting");
const editNameBtn = $("edit-name-btn");
const coverDate = $("cover-date");
const ringCount = $("ring-count");
const topStreakPill = $("top-streak-pill");

let currentHabitFilter = "all";


const todayISO = new Date().toISOString().slice(0, 10);
const yesterdayISO = (() => {
  const d = new Date();
  d.setDate(d.getDate() - 1);
  return d.toISOString().slice(0, 10);
})();
memoryDate.value = todayISO;
coverDate.textContent = new Date().toLocaleDateString(undefined, { weekday: "long", month: "long", day: "numeric" }).toUpperCase();

const todayObj = new Date();
calViewYear = todayObj.getFullYear();
calViewMonth = todayObj.getMonth();

let appData = loadData();
normalizeHabitsForToday();

function loadData() {
  const saved = localStorage.getItem("habitflow-fieldbook-data");

  if (saved) {
    try {
      const parsed = JSON.parse(saved);
      if (
        parsed &&
        Array.isArray(parsed.habits) &&
        parsed.memories &&
        typeof parsed.memories === "object"
      ) {
        return parsed;
      }
    } catch (e) {
      console.warn("HabitFlow data could not be read; starting with empty defaults.", e);
    }
  }

  return {
    userName: null,
    habits: [
      { name: "Drink water", streak: 0, lastCompletedDate: null },
      { name: "Study JavaScript", streak: 0, lastCompletedDate: null }
    ],
    memories: {}
  };
}

function saveData() {
  const serialized = JSON.stringify(appData);
  localStorage.setItem("habitflow-fieldbook-data", serialized);
}

function escapeHtml(text) {
  const div = document.createElement("div");
  div.textContent = text;
  return div.innerHTML;
}

function renderApp() {
  renderGreeting();
  renderHabits();
  renderMemory();
  renderSummary();
}

function renderGreeting() {
  const hour = new Date().getHours();
  const timeLabel = hour < 12 ? "Good morning," : hour < 18 ? "Good afternoon," : "Good evening,";
  homeGreeting.textContent = timeLabel;
  editNameBtn.textContent = appData.userName || "there";
}

function renderSummary() {
  const done = appData.habits.filter(isDoneToday);
  const top = getTopHabit();

  ringCount.textContent = done.length + "/" + appData.habits.length;
  topStreakPill.textContent = (top ? top.streak : 0) + " day streak";
  memoryCount.textContent = Object.keys(appData.memories).length;
}

function renderHabits() {
  habitList.innerHTML = "";
  const visible = appData.habits.filter(h => {
    const done = isDoneToday(h);
    if (currentHabitFilter === "done") return done;
    if (currentHabitFilter === "active") return !done;
    return true;
  });

  if (appData.habits.length === 0) {
    habitList.innerHTML = "<p class='empty-note'>No habits yet — add your first entry above.</p>";
    return;
  }
  if (visible.length === 0) {
    habitList.innerHTML = "<p class='empty-note'>Nothing here for this filter.</p>";
    return;
  }

  visible.forEach(habit => {
    const index = appData.habits.indexOf(habit);
    const isFirst = index === 0;
    const isLast = index === appData.habits.length - 1;
    const done = isDoneToday(habit);
    const row = document.createElement("div");
    row.className = "ledger-row" + (done ? " is-done" : "");
    row.innerHTML =
      "<button class='stamp-toggle" + (done ? " done" : "") + "' data-index='" + index + "'" + (done ? " disabled" : "") + "></button>" +
      "<div class='ledger-row-main'>" +
        "<span class='ledger-name'>" + escapeHtml(habit.name) + "</span>" +
        "<span class='ledger-leader'></span>" +
        "<span class='ledger-streak mono'>" + habit.streak + "D</span>" +
      "</div>" +
      "<div class='ledger-row-actions'>" +
        "<button class='row-icon-btn' data-action='up' data-index='" + index + "'" + (isFirst ? " disabled" : "") + " aria-label='Move up'>▲</button>" +
        "<button class='row-icon-btn' data-action='down' data-index='" + index + "'" + (isLast ? " disabled" : "") + " aria-label='Move down'>▼</button>" +
        "<button class='row-icon-btn danger' data-action='delete' data-index='" + index + "' aria-label='Delete habit'>✕</button>" +
      "</div>";
    habitList.appendChild(row);
  });
}

function getTopHabit() {
  return appData.habits.reduce((best, h) => (!best || h.streak > best.streak) ? h : best, null);
}

function addHabit(event) {
  event.preventDefault();
  const name = habitInput.value.trim();
  if (!name) return;
  appData.habits.push({ name, streak: 0, lastCompletedDate: null });
  habitInput.value = "";
  saveData();
  renderApp();
}

function isDoneToday(habit) {
  return habit.lastCompletedDate === todayISO;
}

function markHabitDone(index) {
  const habit = appData.habits[index];
  if (!habit || isDoneToday(habit)) return;
  // continue the streak only if the last completion was exactly yesterday, otherwise start fresh
  habit.streak = (habit.lastCompletedDate === yesterdayISO) ? habit.streak + 1 : 1;
  habit.lastCompletedDate = todayISO;
  saveData();
  renderApp();
}

function moveHabit(index, direction) {
  const newIndex = index + direction;
  if (newIndex < 0 || newIndex >= appData.habits.length) return;
  const temp = appData.habits[index];
  appData.habits[index] = appData.habits[newIndex];
  appData.habits[newIndex] = temp;
  saveData();
  renderHabits();
}

function deleteHabit(index) {
  const habit = appData.habits[index];
  if (!habit) return;
  const ok = confirm("Delete \"" + habit.name + "\"? This can't be undone.");
  if (!ok) return;
  appData.habits.splice(index, 1);
  saveData();
  renderApp();
}

function resetToday() {
  appData.habits.forEach(h => {
    if (isDoneToday(h)) {
      // undo today's tap: if the streak was a continuation, step it back one day;
      // if it was a fresh start today, this correctly zeroes it out
      h.streak = Math.max(0, h.streak - 1);
      h.lastCompletedDate = h.streak > 0 ? yesterdayISO : null;
    }
  });
  saveData();
  renderApp();
}

// Runs once per load: rolls "done today" back to "not done" automatically once the
// calendar date changes, and breaks any streak where a full day was missed entirely.
function normalizeHabitsForToday() {
  let changed = false;

  if (!appData.memories || typeof appData.memories !== "object" || Array.isArray(appData.memories)) {
    appData.memories = {};
    changed = true;
  }

  appData.habits.forEach(h => {
    // migrate pre-refactor data that stored an explicit completedToday flag
    if (typeof h.completedToday === "boolean") {
      if (h.completedToday && !h.lastCompletedDate) h.lastCompletedDate = todayISO;
      delete h.completedToday;
      changed = true;
    }
    if (h.lastCompletedDate && h.lastCompletedDate !== todayISO && h.lastCompletedDate !== yesterdayISO) {
      if (h.streak !== 0) changed = true;
      h.streak = 0;
    }
  });
  if (changed) saveData();
}

function exportBackup() {
  const blob = new Blob([JSON.stringify(appData, null, 2)], { type: "application/json" });
  const url = URL.createObjectURL(blob);
  const a = document.createElement("a");
  a.href = url;
  a.download = "habitflow-backup-" + todayISO + ".json";
  document.body.appendChild(a);
  a.click();
  a.remove();
  URL.revokeObjectURL(url);
}

function importBackup(event) {
  const file = event.target.files[0];
  if (!file) return;

  const reader = new FileReader();
  reader.onload = () => {
    let parsed;
    try {
      parsed = JSON.parse(reader.result);
    } catch (e) {
      alert("That file doesn't look like a valid HabitFlow backup.");
      importInput.value = "";
      return;
    }
    if (!parsed || !Array.isArray(parsed.habits) || typeof parsed.memories !== "object") {
      alert("That file doesn't look like a valid HabitFlow backup.");
      importInput.value = "";
      return;
    }
    const ok = confirm("This replaces everything currently in the app with the backup file. Continue?");
    if (!ok) { importInput.value = ""; return; }

    appData = parsed;
    normalizeHabitsForToday();
    saveData();
    renderApp();
    renderCalendar();
    importInput.value = "";
  };
  reader.readAsText(file);
}

function readFileAsDataUrl(file) {
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.addEventListener("load", () => resolve(reader.result));
    reader.addEventListener("error", () => reject(reader.error));
    reader.readAsDataURL(file);
  });
}

function renderMemory() {
  const memory = appData.memories[memoryDate.value];

  // Changing days starts a fresh draft for that day.
  memoryPhoto.value = "";
  draftDayMedia = null;
  mediaMarkedForDeletion = false;

  if (!memory) {
    memoryText.value = "";
    renderMemoryPreview(null);
    renderCalendar();
    return;
  }

  memoryText.value = memory.text || "";
  renderMemoryPreview(memory);
  renderCalendar();
}

function renderMemoryPreview(memory) {
  memoryPreview.style.display = "block";

  let mediaData = "";
  let mediaType = "";

  if (draftDayMedia) {
    mediaData = draftDayMedia.dataUrl;
    mediaType = draftDayMedia.type;
  } else if (!mediaMarkedForDeletion && memory) {
    mediaData = memory.mediaData || memory.photoData || "";
    mediaType = memory.mediaType || (memory.photoData ? "image" : "");
  }

  if (mediaData) {
    const mediaElement = mediaType === "video"
      ? "<video src='" + mediaData + "' controls playsinline preload='metadata'></video>"
      : "<img src='" + mediaData + "' alt='Memory media'>";

    const fileLabel = draftDayMedia
      ? "<figcaption>New media selected</figcaption>"
      : "<figcaption>" + escapeHtml((memory && memory.text) || "—") + "</figcaption>";

    memoryPreview.innerHTML = mediaElement + fileLabel;
    removeMemoryMediaButton.style.display = "block";
  } else {
    memoryPreview.innerHTML =
      "<div class='no-photo'>no photo or video attached</div>" +
      "<figcaption>" + escapeHtml((memory && memory.text) || "—") + "</figcaption>";
    removeMemoryMediaButton.style.display = "none";
  }
}

function readFileAsDataUrl(file) {
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.addEventListener("load", () => resolve(reader.result));
    reader.addEventListener("error", () => reject(reader.error));
    reader.readAsDataURL(file);
  });
}

function handleMemoryFileChange() {
  const file = memoryPhoto.files[0];

  if (!file) return;

  if (!file.type.startsWith("image/") && !file.type.startsWith("video/")) {
    alert("Please choose an image or video file.");
    memoryPhoto.value = "";
    return;
  }

  if (file.size > MAX_DAY_MEDIA_BYTES) {
    alert("That file is too large — please choose something under 15MB.");
    memoryPhoto.value = "";
    return;
  }

  const mediaType = file.type.startsWith("video") ? "video" : "image";

  readFileAsDataUrl(file).then(dataUrl => {
    draftDayMedia = {
      dataUrl: dataUrl,
      type: mediaType,
      name: file.name
    };
    mediaMarkedForDeletion = false;

    // Preview immediately, before saving.
    renderMemoryPreview(appData.memories[memoryDate.value] || null);
  }).catch(() => {
    alert("Couldn't read that file.");
    memoryPhoto.value = "";
    draftDayMedia = null;
    renderMemoryPreview(appData.memories[memoryDate.value] || null);
  });
}

function removeMemoryMedia() {
  draftDayMedia = null;
  mediaMarkedForDeletion = true;
  memoryPhoto.value = "";

  const memory = appData.memories[memoryDate.value] || null;
  renderMemoryPreview(memory);
}

function validateMemoryMedia(dataUrl, mediaType) {
  if (!dataUrl) return true;
  if (typeof dataUrl !== "string") return false;

  const expectedPrefix = mediaType === "video" ? "data:video/" : "data:image/";
  return dataUrl.startsWith(expectedPrefix);
}

async function saveMemory() {
  const selectedDate = memoryDate.value;
  if (!selectedDate) {
    alert("Please choose a date.");
    return;
  }

  const old = appData.memories[selectedDate];

  let mediaData = old ? (old.mediaData || old.photoData || "") : "";
  let mediaType = old ? (old.mediaType || (old.photoData ? "image" : "")) : "";

  if (mediaMarkedForDeletion) {
    mediaData = "";
    mediaType = "";
  } else if (draftDayMedia) {
    mediaData = draftDayMedia.dataUrl;
    mediaType = draftDayMedia.type;

    if (!validateMemoryMedia(mediaData, mediaType)) {
      alert("The selected media could not be prepared correctly.");
      return;
    }
  }

  const text = memoryText.value.trim();

  // If the user removed both text and media, remove the memory entirely.
  if (!text && !mediaData) {
    if (appData.memories[selectedDate]) {
      delete appData.memories[selectedDate];
    }

    try {
      saveData();
    } catch (e) {
      alert("Couldn't save the change. Your existing data was left untouched.");
      return;
    }

    memoryPhoto.value = "";
    draftDayMedia = null;
    mediaMarkedForDeletion = false;
    renderApp();
    return;
  }

  const previous = appData.memories[selectedDate];
  appData.memories[selectedDate] = {
    text: text,
    mediaData: mediaData,
    mediaType: mediaType
  };

  try {
    saveData();
  } catch (e) {
    // Roll back in-memory state if localStorage is full/unavailable.
    if (previous) {
      appData.memories[selectedDate] = previous;
    } else {
      delete appData.memories[selectedDate];
    }

    alert("Couldn't save — your browser's local storage may be full. Try a smaller photo or video (under 15MB).");
    return;
  }

  memoryPhoto.value = "";
  draftDayMedia = null;
  mediaMarkedForDeletion = false;
  renderApp();
}

function renderCalendar() {
  const first = new Date(calViewYear, calViewMonth, 1);
  const daysInMonth = new Date(calViewYear, calViewMonth + 1, 0).getDate();
  const startWeekday = first.getDay();
  const todayStr = new Date().toISOString().slice(0, 10);

  calMonthLabel.textContent = first.toLocaleDateString(undefined, { month: "long", year: "numeric" });
  calGrid.innerHTML = "";

  for (let i = 0; i < startWeekday; i++) {
    const pad = document.createElement("div");
    pad.className = "calendar-day pad";
    calGrid.appendChild(pad);
  }

  for (let d = 1; d <= daysInMonth; d++) {
    const dateObj = new Date(calViewYear, calViewMonth, d);
    const iso = dateObj.getFullYear() + "-" + String(dateObj.getMonth() + 1).padStart(2, "0") + "-" + String(d).padStart(2, "0");
    const cell = document.createElement("button");
    cell.type = "button";
    cell.className = "calendar-day";
    if (iso === todayStr) cell.classList.add("today");
    if (iso === memoryDate.value) cell.classList.add("selected");

    const memory = appData.memories[iso];
    let dotHtml = "";
    if (memory && memory.text) {
      const hasMedia = memory.mediaData || memory.photoData;
      dotHtml = "<span class='entry-dot" + (hasMedia ? " media-dot" : "") + "'></span>";
    }

    cell.innerHTML = d + dotHtml;
    cell.addEventListener("click", () => {
      memoryDate.value = iso;
      renderMemory();
    });
    calGrid.appendChild(cell);
  }
}

// events
editNameBtn.addEventListener("click", () => {
  const input = prompt("What should we call you?", appData.userName || "");
  if (input === null) return; // cancelled
  appData.userName = input.trim() || null;
  saveData();
  renderGreeting();
});
habitForm.addEventListener("submit", addHabit);
resetTodayButton.addEventListener("click", resetToday);
habitList.addEventListener("click", e => {
  const stampBtn = e.target.closest(".stamp-toggle");
  if (stampBtn) {
    markHabitDone(Number(stampBtn.dataset.index));
    return;
  }

  const actionBtn = e.target.closest(".row-icon-btn");
  if (!actionBtn || actionBtn.disabled) return;
  const index = Number(actionBtn.dataset.index);
  const action = actionBtn.dataset.action;

  if (action === "up") moveHabit(index, -1);
  else if (action === "down") moveHabit(index, 1);
  else if (action === "delete") deleteHabit(index);
});
habitFilterButtons.forEach(btn => btn.addEventListener("click", () => {
  currentHabitFilter = btn.dataset.habitFilter;
  habitFilterButtons.forEach(b => b.classList.remove("active"));
  btn.classList.add("active");
  renderHabits();
}));

exportButton.addEventListener("click", exportBackup);
importInput.addEventListener("change", importBackup);

saveMemoryButton.addEventListener("click", saveMemory);
removeMemoryMediaButton.addEventListener("click", removeMemoryMedia);
memoryDate.addEventListener("change", renderMemory);
memoryPhoto.addEventListener("change", handleMemoryFileChange);
calPrev.addEventListener("click", () => {
  calViewMonth -= 1;
  if (calViewMonth < 0) { calViewMonth = 11; calViewYear -= 1; }
  renderCalendar();
});
calNext.addEventListener("click", () => {
  calViewMonth += 1;
  if (calViewMonth > 11) { calViewMonth = 0; calViewYear += 1; }
  renderCalendar();
});

// nav
document.querySelectorAll(".nav-btn").forEach(btn => {
  btn.addEventListener("click", () => {
    document.querySelectorAll(".nav-btn").forEach(b => b.classList.remove("active"));
    document.querySelectorAll(".view").forEach(v => v.classList.remove("active"));
    btn.classList.add("active");
    document.querySelector("[data-view='" + btn.dataset.view + "'].view").classList.add("active");
  });
});

renderApp();

if ("serviceWorker" in navigator) {
  window.addEventListener("load", () => {
    navigator.serviceWorker.register("sw.js").catch(() => {
      // offline support just won't be available this session — the app still works online
    });
  });
}
</script>
</body>
</html>
