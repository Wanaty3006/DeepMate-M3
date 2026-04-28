<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DeepMate M3 — Consultation QA</title>
<link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--bg:#08080f;--bg2:#0f0f1a;--bg3:#14141f;--t1:#fff;--t2:rgba(255,255,255,.65);--t3:rgba(255,255,255,.35);--teal:#5DCAA5;--purple:#7F77DD;--red:#E24B4A;--amber:#EF9F27;--blue:#378ADD;--border:rgba(255,255,255,.08)}
html,body{min-height:100%;background:var(--bg);color:var(--t1);font-family:'Prompt',system-ui,sans-serif}
.wrap{max-width:900px;margin:0 auto;padding:28px 24px 60px}
/* Header */
.hdr{display:flex;align-items:center;gap:10px;margin-bottom:24px}
.hdr-dot{width:10px;height:10px;border-radius:50%;background:var(--amber)}
.hdr-title{font-size:17px;font-weight:500}
.badge{font-size:10px;background:rgba(239,159,39,.15);color:var(--amber);padding:3px 9px;border-radius:10px;border:0.5px solid rgba(239,159,39,.3)}
/* Tabs */
.tabs{display:flex;gap:2px;margin-bottom:22px;background:rgba(255,255,255,.04);padding:3px;border-radius:10px;width:fit-content}
.tab{padding:7px 16px;border-radius:7px;border:none;background:transparent;color:rgba(255,255,255,.4);font-size:12px;cursor:pointer;font-family:inherit;font-weight:400;transition:all .15s}
.tab.active{background:rgba(255,255,255,.12);color:#fff;font-weight:500}
.tab:disabled{opacity:.3;cursor:default}
/* Step bar */
.stepbar{display:flex;align-items:center;margin-bottom:24px}
.step-item{display:flex;flex-direction:column;align-items:center;gap:3px}
.step-circle{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:600;transition:all .3s}
.step-circle.done{background:var(--teal);color:#000}
.step-circle.active{background:var(--amber);color:#000}
.step-circle.pending{background:rgba(255,255,255,.07);color:rgba(255,255,255,.3)}
.step-label{font-size:9px;white-space:nowrap}
.step-label.active{color:var(--amber)}
.step-label.done{color:var(--teal)}
.step-label.pending{color:rgba(255,255,255,.25)}
.step-line{flex:1;height:1.5px;margin:0 4px;margin-bottom:14px;transition:background .3s}
/* Cards */
.card{background:var(--bg2);border:0.5px solid var(--border);border-radius:12px;padding:16px 18px;margin-bottom:12px}
.card.active-step{border-color:rgba(239,159,39,.35)}
.card.done-step{border-color:rgba(93,202,165,.2);opacity:.7}
.card-title{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.14em;margin-bottom:12px}
/* Form */
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:10px}
.field label{display:block;font-size:10px;color:var(--t3);margin-bottom:4px}
.field input,.field select{width:100%;background:rgba(255,255,255,.04);border:0.5px solid rgba(255,255,255,.1);border-radius:8px;padding:8px 11px;color:var(--t1);font-size:13px;font-family:inherit;outline:none;color-scheme:dark}
.field input:focus,.field select:focus{border-color:rgba(239,159,39,.4)}
.key-row{display:flex;align-items:center;gap:6px;margin-bottom:3px}
.key-toggle{background:none;border:none;font-size:10px;color:rgba(255,255,255,.3);cursor:pointer;font-family:inherit}
.hint{font-size:10px;color:rgba(255,255,255,.2);margin-top:3px;line-height:1.5}
.hint a{color:rgba(55,138,221,.7)}
/* Upload zone */
.upload-zone{border:1.5px dashed rgba(255,255,255,.12);border-radius:10px;padding:32px;text-align:center;cursor:pointer;transition:all .2s}
.upload-zone:hover{border-color:rgba(255,255,255,.25);background:rgba(255,255,255,.02)}
.upload-zone.has-file{border-color:var(--teal);background:rgba(93,202,165,.04)}
.upload-icon{font-size:36px;opacity:.35;margin-bottom:10px}
.upload-name{font-size:13px;font-weight:500;color:var(--teal);margin-bottom:3px}
.upload-size{font-size:11px;color:var(--t3)}
.upload-hint{font-size:11px;color:rgba(255,255,255,.3);margin-top:4px}
/* Buttons */
.btn{border:0.5px solid var(--border);border-radius:8px;padding:9px 20px;font-size:13px;font-family:inherit;cursor:pointer;transition:all .15s;color:var(--t2);background:transparent}
.btn:hover{background:rgba(255,255,255,.06)}
.btn-primary{background:var(--amber)!important;color:#000!important;border-color:var(--amber)!important;font-weight:700}
.btn-teal{background:var(--teal)!important;color:#000!important;border-color:var(--teal)!important;font-weight:700}
.btn:disabled{opacity:.4;cursor:not-allowed}
.btn-row{display:flex;gap:8px;align-items:center;margin-top:12px;flex-wrap:wrap}
.divider{display:flex;align-items:center;gap:8px;margin:10px 0}
.divider-line{flex:1;height:0.5px;background:rgba(255,255,255,.07)}
.divider-text{font-size:11px;color:rgba(255,255,255,.2)}
/* Transcript */
textarea{width:100%;min-height:160px;background:rgba(255,255,255,.03);border:0.5px solid rgba(255,255,255,.08);border-radius:8px;padding:12px;color:rgba(255,255,255,.8);font-size:13px;font-family:inherit;resize:vertical;outline:none;line-height:1.75}
textarea:focus{border-color:rgba(239,159,39,.3)}
/* Progress */
.progress-box{display:flex;align-items:center;gap:10px;padding:13px 16px;background:rgba(239,159,39,.07);border-radius:8px}
.spinner{width:16px;height:16px;border:2px solid rgba(239,159,39,.25);border-top-color:var(--amber);border-radius:50%;animation:spin .8s linear infinite;flex-shrink:0}
@keyframes spin{to{transform:rotate(360deg)}}
/* Error */
.error-box{background:rgba(226,75,74,.1);border:0.5px solid rgba(226,75,74,.3);border-radius:8px;padding:10px 14px;font-size:12px;color:#f09595;margin-top:10px;line-height:1.6}
/* Result */
.result-hero{display:grid;grid-template-columns:auto 1fr;gap:18px;padding:18px 20px;border-radius:14px;margin-bottom:14px}
.gauge-wrap{text-align:center}
.hero-info{display:flex;flex-direction:column;justify-content:center;gap:8px}
.zone-label{font-size:18px;font-weight:600}
.zone-action{font-size:12px;color:var(--t2);background:rgba(0,0,0,.25);padding:8px 13px;border-radius:8px;line-height:1.6}
.red-flags{display:flex;gap:5px;flex-wrap:wrap}
.red-flag-tag{font-size:11px;background:rgba(226,75,74,.15);color:#f09595;padding:2px 8px;border-radius:8px;border:0.5px solid rgba(226,75,74,.25)}
.score-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:12px}
.score-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:12px;padding:14px 16px}
.score-card-title{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.12em;margin-bottom:12px}
.score-row{margin-bottom:10px}
.score-row-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:4px}
.score-row-label{font-size:12px;color:var(--t2);display:flex;align-items:center;gap:5px}
.score-row-val{font-size:13px;font-weight:600}
.score-bar{height:4px;background:rgba(255,255,255,.06);border-radius:2px;overflow:hidden;margin-bottom:2px}
.score-bar-fill{height:100%;border-radius:2px;transition:width .5s}
.score-note{font-size:10px;color:rgba(255,255,255,.28);line-height:1.4}
.weight-badge{font-size:9px;color:rgba(255,255,255,.2);background:rgba(255,255,255,.05);padding:1px 5px;border-radius:3px}
.two-col{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:12px}
.insight-box{border-radius:10px;padding:13px 15px}
.insight-title{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.1em;margin-bottom:8px}
.insight-item{font-size:12px;color:var(--t2);padding-left:9px;margin-bottom:5px;line-height:1.5;border-left:2px solid transparent}
.coaching-box{border-radius:10px;padding:13px 15px;margin-bottom:14px}
.coaching-title{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.1em;margin-bottom:5px}
.coaching-text{font-size:13px;color:var(--t2);line-height:1.65}
/* Formula */
.formula-box{background:rgba(127,119,221,.07);border-radius:7px;padding:8px 11px;font-size:11px;color:rgba(255,255,255,.4);margin-top:10px}
/* Overview */
.stat-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:16px}
.stat-box{border-radius:10px;padding:13px;text-align:center;background:rgba(255,255,255,.03);border:0.5px solid rgba(255,255,255,.07)}
.stat-num{font-size:28px;font-weight:400;margin-bottom:3px}
.stat-lbl{font-size:11px;color:var(--t3)}
.perf-row{display:flex;align-items:center;gap:10px;margin-bottom:9px}
.perf-name{width:55px;font-size:12px;font-weight:500;color:var(--t2);flex-shrink:0}
.perf-bar-wrap{flex:1;height:7px;background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden}
.perf-bar-fill{height:100%;border-radius:3px;transition:width .5s}
.perf-score{width:34px;font-size:13px;font-weight:600;text-align:right;flex-shrink:0}
.perf-icon{font-size:14px;flex-shrink:0}
.perf-cnt{width:30px;font-size:10px;color:rgba(255,255,255,.25);text-align:right;flex-shrink:0}
.action-box{border-radius:10px;padding:13px 15px}
/* History */
.hist-item{display:flex;align-items:center;gap:10px;padding:9px 13px;background:rgba(255,255,255,.03);border:0.5px solid rgba(255,255,255,.07);border-radius:9px;cursor:pointer;margin-bottom:5px;transition:background .15s}
.hist-item:hover{background:rgba(255,255,255,.06)}
.hist-icon{font-size:16px}
.hist-info{flex:1;min-width:0}
.hist-name{font-size:12px;font-weight:500;color:var(--t2);overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.hist-meta{font-size:10px;color:var(--t3)}
.hist-score{text-align:right;flex-shrink:0}
.hist-score-num{font-size:14px;font-weight:600}
.hist-score-lbl{font-size:9px}
</style>
</head>
<body>
<div class="wrap">

  <!-- Header -->
  <div class="hdr">
    <div class="hdr-dot"></div>
    <div class="hdr-title">DeepMate · M3 Consultation QA</div>
    <div class="badge">LIC · Audio Input</div>
    <div style="margin-left:auto;font-size:11px;color:var(--t3)" id="case-count"></div>
  </div>

  <!-- Tabs -->
  <div class="tabs">
    <button class="tab active" id="tab-analyze" onclick="switchTab('analyze')">🎙 วิเคราะห์</button>
    <button class="tab" id="tab-result" onclick="switchTab('result')" disabled>📊 ผลลัพธ์</button>
    <button class="tab" id="tab-overview" onclick="switchTab('overview')" disabled>🗂 ภาพรวม</button>
    <button class="tab" id="tab-history" onclick="switchTab('history')" disabled>🕐 ประวัติ</button>
  </div>

  <div id="pane-analyze">
    <!-- Step bar -->
    <div class="stepbar" id="stepbar"></div>

    <!-- STEP 1 -->
    <div class="card active-step" id="card-step1">
      <div class="card-title" style="color:var(--amber)">Step 1 · ตั้งค่า</div>
      <div class="form-row">
        <div class="field">
          <label>Consultant</label>
          <select id="consultant">
            <option>น้ำ</option><option>กิต</option><option>นัท</option>
            <option>เพิร์ล</option><option>วิว</option><option>อื่นๆ</option>
          </select>
        </div>
        <div class="field">
          <label>วันที่</label>
          <input type="date" id="date-input">
        </div>
      </div>
      <div class="field" style="margin-bottom:10px">
        <div class="key-row">
          <label style="margin:0">AssemblyAI API Key</label>
          <button class="key-toggle" onclick="toggleKey('aai-key','toggle-aai')" id="toggle-aai">แสดง</button>
        </div>
        <input type="password" id="aai-key" placeholder="xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" style="font-family:monospace">
        <div class="hint">รับฟรีที่ <a href="https://www.assemblyai.com" target="_blank">assemblyai.com</a> → Dashboard → API Key</div>
      </div>
      <div class="field" style="margin-bottom:0">
        <div class="key-row">
          <label style="margin:0">Anthropic API Key</label>
          <button class="key-toggle" onclick="toggleKey('ant-key','toggle-ant')" id="toggle-ant">แสดง</button>
        </div>
        <input type="password" id="ant-key" placeholder="sk-ant-api03-xxxxxxxxxxxx" style="font-family:monospace">
        <div class="hint">รับที่ <a href="https://console.anthropic.com" target="_blank">console.anthropic.com</a> → API Keys</div>
      </div>
      <div id="step1-error" class="error-box" style="display:none;margin-top:10px"></div>
      <div class="btn-row">
        <button class="btn btn-primary" onclick="goStep(2)">ถัดไป →</button>
      </div>
    </div>

    <!-- STEP 2 -->
    <div class="card" id="card-step2" style="display:none">
      <div class="card-title" id="s2-title" style="color:var(--amber)">Step 2 · อัปโหลดไฟล์เสียง</div>
      <div class="upload-zone" id="upload-zone" onclick="document.getElementById('file-input').click()">
        <input type="file" id="file-input" accept=".mp3,.mp4,.m4a,.wav,.webm,.ogg,.aac" style="display:none" onchange="onFileSelect(this)">
        <div id="upload-content">
          <div class="upload-icon">🎵</div>
          <div style="font-size:13px;color:rgba(255,255,255,.5);margin-bottom:4px">คลิกเพื่อเลือกไฟล์เสียง</div>
          <div class="upload-hint">รองรับ: MP3 · MP4 · M4A · WAV · WebM · AAC</div>
        </div>
      </div>
      <div class="btn-row" id="s2-btns" style="display:none">
        <button class="btn btn-primary" onclick="goStep(3)">ถัดไป →</button>
        <button class="btn" onclick="document.getElementById('file-input').click()">เปลี่ยนไฟล์</button>
      </div>
    </div>

    <!-- STEP 3 -->
    <div class="card" id="card-step3" style="display:none">
      <div class="card-title" id="s3-title" style="color:var(--amber)">Step 3 · ถอดเสียงภาษาไทย</div>
      <div style="display:flex;gap:8px;padding:10px 13px;background:rgba(55,138,221,.07);border:0.5px solid rgba(55,138,221,.2);border-radius:8px;font-size:12px;color:rgba(55,138,221,.9);line-height:1.6;margin-bottom:12px">
        <span>ℹ️</span><span>ใช้ AssemblyAI ถอดเสียงภาษาไทย + อังกฤษ · ไฟล์ขนาดใหญ่อาจใช้เวลา 1-3 นาที</span>
      </div>
      <div id="transcribe-progress" style="display:none" class="progress-box">
        <div class="spinner"></div>
        <span id="transcribe-msg" style="font-size:12px;color:var(--amber)"></span>
      </div>
      <div id="s3-btns">
        <div class="btn-row">
          <button class="btn btn-primary" onclick="startTranscribe()">🎙 เริ่มถอดเสียงอัตโนมัติ</button>
        </div>
        <div class="divider"><div class="divider-line"></div><div class="divider-text">หรือถ้าถอดไม่ได้</div><div class="divider-line"></div></div>
        <button class="btn" onclick="goStep(4)" style="font-size:12px">✏️ วาง Transcript เองในขั้นตอนถัดไป</button>
      </div>
      <div id="s3-error" class="error-box" style="display:none"></div>
    </div>

    <!-- STEP 4 -->
    <div class="card" id="card-step4" style="display:none">
      <div class="card-title" id="s4-title" style="color:var(--amber)">Step 4 · ตรวจสอบ Transcript</div>
      <div style="font-size:11px;color:var(--t3);margin-bottom:6px">แก้ไขได้ถ้าถอดผิด — AI จะใช้ข้อความนี้วิเคราะห์ <span id="word-count"></span></div>
      <textarea id="transcript-box" oninput="updateWordCount()" placeholder="วาง Transcript ที่นี่..."></textarea>
      <div class="btn-row">
        <button class="btn btn-primary" onclick="goStep(5)">ถัดไป →</button>
      </div>
    </div>

    <!-- STEP 5 -->
    <div class="card" id="card-step5" style="display:none">
      <div class="card-title" style="color:var(--amber)">Step 5 · วิเคราะห์ด้วย AI</div>
      <div id="analyze-progress" style="display:none" class="progress-box">
        <div class="spinner"></div>
        <span style="font-size:12px;color:var(--amber)">กำลังวิเคราะห์ด้วย Claude...</span>
      </div>
      <div id="analyze-error" class="error-box" style="display:none"></div>
      <div class="btn-row">
        <button class="btn btn-primary" id="analyze-btn" onclick="runAnalyze()">🔍 วิเคราะห์ Consultation</button>
        <button class="btn" onclick="resetAll()">↺ เริ่มใหม่</button>
      </div>
    </div>
  </div>

  <div id="pane-result" style="display:none"></div>
  <div id="pane-overview" style="display:none"></div>
  <div id="pane-history" style="display:none"></div>
</div>

<script>
// ── State ──────────────────────────────────────────────────────
var state = {
  step: 1,
  audioFile: null,
  transcript: '',
  lastResult: null,
  lastConsultant: '',
  lastDate: '',
  history: [],
};

// ── Init ───────────────────────────────────────────────────────
document.getElementById('date-input').value = new Date().toISOString().slice(0,10);
renderStepBar();

// ── Step bar ───────────────────────────────────────────────────
var STEP_LABELS = ['ตั้งค่า','อัปโหลด','ถอดเสียง','ตรวจสอบ','วิเคราะห์'];
function renderStepBar() {
  var sb = document.getElementById('stepbar'), html = '';
  for (var i = 1; i <= 5; i++) {
    var cls = state.step > i ? 'done' : state.step === i ? 'active' : 'pending';
    var icon = state.step > i ? '✓' : i;
    html += '<div class="step-item"><div class="step-circle '+cls+'">'+icon+'</div><div class="step-label '+cls+'">'+STEP_LABELS[i-1]+'</div></div>';
    if (i < 5) html += '<div class="step-line" style="background:'+(state.step > i ? 'var(--teal)' : 'rgba(255,255,255,.07)')+'"></div>';
  }
  sb.innerHTML = html;
}

// ── Navigation ─────────────────────────────────────────────────
function goStep(n) {
  var errBox = document.getElementById('step1-error');
  if (errBox) errBox.style.display = 'none';

  if (n === 2) {
    var antVal = document.getElementById('ant-key').value.trim();
    var aaiVal = document.getElementById('aai-key').value.trim();
    if (!antVal && !aaiVal) {
      errBox.style.display = 'block';
      errBox.textContent = '⚠️ กรุณากรอก API Key ทั้ง 2 ช่องครับ';
      return;
    }
    if (!antVal) {
      errBox.style.display = 'block';
      errBox.textContent = '⚠️ กรุณากรอก Anthropic API Key ครับ';
      return;
    }
    if (!aaiVal) {
      errBox.style.display = 'block';
      errBox.textContent = '⚠️ กรุณากรอก AssemblyAI API Key ครับ';
      return;
    }
  }
  if (n === 4 && !document.getElementById('transcript-box').value.trim()) {
    // ok - user will paste
  }
  state.step = n;
  renderStepBar();
  // Show/hide cards
  [1,2,3,4,5].forEach(function(i) {
    var c = document.getElementById('card-step'+i);
    c.style.display = i <= n ? 'block' : 'none';
    c.className = 'card ' + (i === n ? 'active-step' : i < n ? 'done-step' : '');
  });
  // Update titles
  var titles = {2:'s2-title',3:'s3-title',4:'s4-title'};
  Object.keys(titles).forEach(function(k) {
    var el = document.getElementById(titles[k]);
    if (el) el.style.color = state.step === parseInt(k) ? 'var(--amber)' : 'rgba(255,255,255,.4)';
  });
}

// ── Key toggle ─────────────────────────────────────────────────
function toggleKey(inputId, btnId) {
  var inp = document.getElementById(inputId);
  var btn = document.getElementById(btnId);
  if (inp.type === 'password') { inp.type = 'text'; btn.textContent = 'ซ่อน'; }
  else { inp.type = 'password'; btn.textContent = 'แสดง'; }
}

// ── File select ────────────────────────────────────────────────
function onFileSelect(input) {
  var f = input.files[0]; if (!f) return;
  state.audioFile = f;
  var zone = document.getElementById('upload-zone');
  zone.className = 'upload-zone has-file';
  document.getElementById('upload-content').innerHTML =
    '<div style="font-size:32px;margin-bottom:8px">🎙</div>' +
    '<div class="upload-name">'+f.name+'</div>' +
    '<div class="upload-size">'+(f.size/1024/1024).toFixed(2)+' MB</div>';
  document.getElementById('s2-btns').style.display = 'flex';
}

// ── Transcribe ─────────────────────────────────────────────────
function startTranscribe() {
  var aaiKey = document.getElementById('aai-key').value.trim();
  if (!aaiKey) { showS3Error('กรุณากรอก AssemblyAI API Key ใน Step 1'); return; }
  if (!state.audioFile) { showS3Error('ยังไม่ได้เลือกไฟล์เสียง'); return; }

  document.getElementById('s3-btns').style.display = 'none';
  document.getElementById('transcribe-progress').style.display = 'flex';
  document.getElementById('s3-error').style.display = 'none';

  var msg = document.getElementById('transcribe-msg');

  // Read file as ArrayBuffer
  msg.textContent = 'กำลังเตรียมไฟล์เสียง...';
  var reader = new FileReader();
  reader.onload = function(e) {
    var buf = e.target.result;
    msg.textContent = 'กำลังอัปโหลดไฟล์ไปยัง AssemblyAI...';
    fetch('https://api.assemblyai.com/v2/upload', {
      method: 'POST',
      headers: { 'authorization': aaiKey },
      body: buf
    })
    .then(function(r) {
      if (r.status === 401) throw new Error('API Key ไม่ถูกต้อง');
      if (!r.ok) throw new Error('Upload ไม่สำเร็จ HTTP ' + r.status);
      return r.json();
    })
    .then(function(d) {
      msg.textContent = 'กำลังส่งคำขอถอดเสียงภาษาไทย...';
      return fetch('https://api.assemblyai.com/v2/transcript', {
        method: 'POST',
        headers: { 'authorization': aaiKey, 'content-type': 'application/json' },
        body: JSON.stringify({ audio_url: d.upload_url, language_code: 'th', speech_model: 'nano' })
      });
    })
    .then(function(r) {
      if (!r.ok) throw new Error('ส่งคำขอถอดเสียงไม่สำเร็จ');
      return r.json();
    })
    .then(function(d) {
      return pollTranscript(aaiKey, d.id, 0, msg);
    })
    .then(function(text) {
      document.getElementById('transcript-box').value = text;
      updateWordCount();
      document.getElementById('transcribe-progress').style.display = 'none';
      document.getElementById('s3-btns').style.display = 'block';
      goStep(4);
    })
    .catch(function(err) {
      document.getElementById('transcribe-progress').style.display = 'none';
      document.getElementById('s3-btns').style.display = 'block';
      showS3Error(err.message);
    });
  };
  reader.onerror = function() { showS3Error('อ่านไฟล์ไม่ได้ ลองเลือกใหม่'); };
  reader.readAsArrayBuffer(state.audioFile);
}

function pollTranscript(key, id, attempts, msg) {
  if (attempts > 80) return Promise.reject(new Error('หมดเวลา — ไฟล์อาจยาวเกินไป'));
  return new Promise(function(res) { setTimeout(res, 3000); })
    .then(function() {
      msg.textContent = 'กำลังถอดเสียง... ' + ((attempts+1)*3) + 's';
      return fetch('https://api.assemblyai.com/v2/transcript/' + id, {
        headers: { 'authorization': key }
      }).then(function(r) { return r.json(); });
    })
    .then(function(d) {
      if (d.status === 'completed') return d.text || '';
      if (d.status === 'error') throw new Error('ถอดเสียงไม่สำเร็จ: ' + d.error);
      return pollTranscript(key, id, attempts + 1, msg);
    });
}

function showS3Error(msg) {
  var el = document.getElementById('s3-error');
  el.style.display = 'block';
  el.textContent = '⚠️ ' + msg;
}

function updateWordCount() {
  var t = document.getElementById('transcript-box').value;
  var n = t.split(/\s+/).filter(Boolean).length;
  document.getElementById('word-count').textContent = n ? '· ' + n + ' คำ' : '';
}

// ── Analyze ────────────────────────────────────────────────────
var SYSTEM_PROMPT = 'คุณคือผู้เชี่ยวชาญประเมินคุณภาพการให้คำปรึกษาด้านการศึกษา (Consultation QA) ของ LIC\n' +
'บริบท: Consultant ให้คำปรึกษาแนะนำเตรียมสอบ/วางแผนการเรียน กับนักเรียนและผู้ปกครอง 1:1 ระยะ 15-30 นาที\n' +
'หมายเหตุ: Transcript ถอดจากเสียงภาษาไทยและอาจมีภาษาอังกฤษปน อาจมีคำผิดบ้าง ให้พิจารณาจากบริบท\n\n' +
'มาตรฐาน 5 ขั้นตอน Protocol:\n' +
'1. Opening (10%): ทักทาย แนะนำตัว เปิดโอกาสให้พูดก่อน\n' +
'2. Needs Assessment (25%): ถามเป้าหมาย สถานการณ์ ปัญหา\n' +
'3. Information & Analysis (30%): ให้ข้อมูลถูกต้อง สนามสอบ ปฏิทิน หลักสูตร\n' +
'4. Action Plan (25%): วางแผนชัด เป็นรูปธรรม Personalized\n' +
'5. Closing (10%): สรุป ถามข้อสงสัย นัดติดตาม\n\n' +
'ประเมิน 2 มิติ: Academic (70%) + Emotional Intelligence (30%)\n' +
'Red Flags: ข้อมูลผิด / ไม่มี Action Plan / Consultant พูดฝ่ายเดียว / Session สั้นผิดปกติ\n\n' +
'ส่งคืน JSON เท่านั้น ไม่มีข้อความอื่น:\n' +
'{"protocol":{"opening":{"score":0-100,"found":true/false,"note":""},"needs":{"score":0-100,"found":true/false,"note":""},"info":{"score":0-100,"found":true/false,"note":""},"plan":{"score":0-100,"found":true/false,"note":""},"closing":{"score":0-100,"found":true/false,"note":""}},"academic_score":0-100,"emotional":{"empathy":{"score":0-100,"note":""},"clarity":{"score":0-100,"note":""},"confidence":{"score":0-100,"note":""}},"emotional_score":0-100,"overall_score":0-100,"red_flags":[],"strengths":[],"improvements":[],"coaching_focus":""}';

function runAnalyze() {
  var tx = document.getElementById('transcript-box').value.trim();
  var antKey = document.getElementById('ant-key').value.trim();
  if (!tx) { document.getElementById('analyze-error').style.display='block'; document.getElementById('analyze-error').textContent='⚠️ ไม่มี Transcript'; return; }
  if (!antKey) { document.getElementById('analyze-error').style.display='block'; document.getElementById('analyze-error').textContent='⚠️ กรุณากรอก Anthropic API Key'; return; }

  document.getElementById('analyze-btn').disabled = true;
  document.getElementById('analyze-progress').style.display = 'flex';
  document.getElementById('analyze-error').style.display = 'none';

  fetch('https://api.anthropic.com/v1/messages', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      model: 'claude-sonnet-4-20250514',
      max_tokens: 2000,
      system: SYSTEM_PROMPT,
      messages: [{ role: 'user', content: 'วิเคราะห์ Consultation Transcript นี้:\n\n' + tx }]
    })
  })
  .then(function(r) { return r.json(); })
  .then(function(data) {
    var txt = data.content[0].text.trim();
    var m = txt.match(/\{[\s\S]*\}/);
    if (!m) throw new Error('Parse ผิดพลาด');
    var parsed = JSON.parse(m[0].replace(/\\(?!["\\/bfnrtu])/g,'\\\\').replace(/[\u0000-\u001F]+/g,' '));
    state.lastResult = parsed;
    state.lastConsultant = document.getElementById('consultant').value;
    state.lastDate = document.getElementById('date-input').value;
    state.history.unshift({ consultant: state.lastConsultant, date: state.lastDate, filename: state.audioFile ? state.audioFile.name : 'manual', result: parsed });
    if (state.history.length > 30) state.history.pop();
    updateCaseCount();
    document.getElementById('analyze-progress').style.display = 'none';
    document.getElementById('analyze-btn').disabled = false;
    renderResult(parsed, state.lastConsultant, state.lastDate);
    switchTab('result');
  })
  .catch(function(err) {
    document.getElementById('analyze-progress').style.display = 'none';
    document.getElementById('analyze-btn').disabled = false;
    document.getElementById('analyze-error').style.display = 'block';
    document.getElementById('analyze-error').textContent = '⚠️ ' + err.message;
  });
}

// ── Reset ──────────────────────────────────────────────────────
function resetAll() {
  state.step = 1; state.audioFile = null; state.transcript = '';
  document.getElementById('transcript-box').value = '';
  document.getElementById('word-count').textContent = '';
  var uc = document.getElementById('upload-content');
  uc.innerHTML = '<div class="upload-icon">🎵</div><div style="font-size:13px;color:rgba(255,255,255,.5);margin-bottom:4px">คลิกเพื่อเลือกไฟล์เสียง</div><div class="upload-hint">รองรับ: MP3 · MP4 · M4A · WAV · WebM · AAC</div>';
  document.getElementById('upload-zone').className = 'upload-zone';
  document.getElementById('s2-btns').style.display = 'none';
  document.getElementById('s3-error').style.display = 'none';
  [2,3,4,5].forEach(function(i){ var c=document.getElementById('card-step'+i); c.style.display='none'; });
  document.getElementById('card-step1').className = 'card active-step';
  document.getElementById('card-step1').style.display = 'block';
  renderStepBar();
  switchTab('analyze');
}

// ── Helpers ────────────────────────────────────────────────────
function zoneOf(s) {
  return s>=90 ? {label:'Excellent',color:'#22c55e',bg:'rgba(34,197,94,.1)',action:'ยกย่อง / ใช้เป็น Best Practice'}
       : s>=75 ? {label:'Pass',color:'#5DCAA5',bg:'rgba(93,202,165,.08)',action:'ผ่านมาตรฐาน'}
       : s>=60 ? {label:'Warning',color:'#EF9F27',bg:'rgba(239,159,39,.08)',action:'Coach ภายใน 3 วัน'}
       :          {label:'Critical',color:'#E24B4A',bg:'rgba(226,75,74,.08)',action:'Supervisor ดำเนินการทันที'};
}
function zoneIcon(s){ return s>=75?'🟢':s>=60?'🟡':'🔴'; }

function scoreBarColor(s) { return zoneOf(s).color; }

function gaugeHTML(score, size) {
  var z=zoneOf(score), r=size/2-8, circ=Math.PI*r, dash=(score/100)*circ;
  return '<svg width="'+size+'" height="'+(size/2+14)+'" viewBox="0 0 '+size+' '+(size/2+14)+'">'
    +'<path d="M8,'+size/2+' A'+r+','+r+' 0 0,1 '+(size-8)+','+size/2+'" fill="none" stroke="rgba(255,255,255,.07)" stroke-width="7" stroke-linecap="round"/>'
    +'<path d="M8,'+size/2+' A'+r+','+r+' 0 0,1 '+(size-8)+','+size/2+'" fill="none" stroke="'+z.color+'" stroke-width="7" stroke-linecap="round" stroke-dasharray="'+dash.toFixed(2)+' '+circ.toFixed(2)+'"/>'
    +'<text x="'+size/2+'" y="'+(size/2+2)+'" text-anchor="middle" fill="'+z.color+'" font-size="'+(size*.2)+'" font-weight="600" font-family="system-ui">'+score+'</text>'
    +'<text x="'+size/2+'" y="'+(size/2+14)+'" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="'+(size*.1)+'" font-family="system-ui">'+z.label+'</text>'
    +'</svg>';
}

function updateCaseCount() {
  document.getElementById('case-count').textContent = state.history.length + ' เคส';
  ['tab-result','tab-overview','tab-history'].forEach(function(id){ document.getElementById(id).disabled = !state.history.length; });
  document.getElementById('tab-result').disabled = !state.lastResult;
}

// ── Render Result ──────────────────────────────────────────────
var PROTOCOL_STEPS = [
  {id:'opening',label:'Opening',weight:10},
  {id:'needs',label:'Needs Assessment',weight:25},
  {id:'info',label:'Information',weight:30},
  {id:'plan',label:'Action Plan',weight:25},
  {id:'closing',label:'Closing',weight:10},
];

function renderResult(r, consultant, date) {
  var z = zoneOf(r.overall_score);
  var flags = (r.red_flags||[]).map(function(f){ return '<div class="red-flag-tag">🚩 '+f+'</div>'; }).join('');
  var protocol_rows = PROTOCOL_STEPS.map(function(step){
    var s = r.protocol && r.protocol[step.id];
    if (!s) return '';
    var c = scoreBarColor(s.score);
    return '<div class="score-row">'
      +'<div class="score-row-head"><div class="score-row-label"><span>'+(s.found?'✓':'✗')+'</span>'+step.label+'<span class="weight-badge">×'+step.weight+'%</span></div><div class="score-row-val" style="color:'+c+'">'+s.score+'</div></div>'
      +'<div class="score-bar"><div class="score-bar-fill" style="width:'+s.score+'%;background:'+c+'"></div></div>'
      +(s.note?'<div class="score-note">'+s.note+'</div>':'')
      +'</div>';
  }).join('');
  var emo_rows = r.emotional ? Object.entries(r.emotional).map(function(e){
    var k=e[0], v=e[1], c=scoreBarColor(v.score);
    return '<div class="score-row">'
      +'<div class="score-row-head"><div class="score-row-label" style="text-transform:capitalize">'+k+'</div><div class="score-row-val" style="color:'+c+'">'+v.score+'</div></div>'
      +'<div class="score-bar"><div class="score-bar-fill" style="width:'+v.score+'%;background:'+c+'"></div></div>'
      +(v.note?'<div class="score-note">'+v.note+'</div>':'')
      +'</div>';
  }).join('') : '';
  var strengths = (r.strengths||[]).map(function(s){ return '<div class="insight-item" style="border-left-color:#5DCAA5">'+s+'</div>'; }).join('');
  var improv = (r.improvements||[]).map(function(s){ return '<div class="insight-item" style="border-left-color:#EF9F27">'+s+'</div>'; }).join('');

  var html = '<div class="result-hero" style="background:'+z.bg+';border:0.5px solid '+z.color+'40">'
    +'<div class="gauge-wrap">'+gaugeHTML(r.overall_score, 110)+'</div>'
    +'<div class="hero-info">'
    +'<div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap"><span style="font-size:18px">'+zoneIcon(r.overall_score)+'</span><span class="zone-label" style="color:'+z.color+'">'+z.label+'</span><span style="font-size:11px;color:var(--t3)">· '+consultant+' · '+date+'</span></div>'
    +'<div class="zone-action"><strong style="color:'+z.color+'">Action: </strong>'+z.action+'</div>'
    +(flags?'<div class="red-flags">'+flags+'</div>':'')
    +'</div></div>'
    +'<div class="score-grid">'
    +'<div class="score-card"><div class="score-card-title" style="color:#5DCAA5">Academic Quality · '+r.academic_score+'</div>'+protocol_rows+'</div>'
    +'<div class="score-card"><div class="score-card-title" style="color:#7F77DD">Emotional Intelligence · '+r.emotional_score+'</div>'+emo_rows+'<div class="formula-box">'+r.academic_score+'×70% + '+r.emotional_score+'×30% = <strong style="color:#fff">'+r.overall_score+'</strong></div></div>'
    +'</div>'
    +'<div class="two-col">'
    +'<div class="insight-box" style="background:rgba(93,202,165,.06);border:0.5px solid rgba(93,202,165,.18)"><div class="insight-title" style="color:#5DCAA5">✓ จุดเด่น</div>'+strengths+'</div>'
    +'<div class="insight-box" style="background:rgba(239,159,39,.06);border:0.5px solid rgba(239,159,39,.18)"><div class="insight-title" style="color:#EF9F27">⚡ ควรพัฒนา</div>'+improv+'</div>'
    +'</div>'
    +(r.coaching_focus?'<div class="coaching-box" style="background:rgba(55,138,221,.07);border:0.5px solid rgba(55,138,221,.2)"><div class="coaching-title" style="color:#378ADD">🎯 Coaching Focus</div><div class="coaching-text">'+r.coaching_focus+'</div></div>':'')
    +'<div style="display:flex;gap:8px;flex-wrap:wrap">'
    +'<button class="btn" onclick="resetAll()">+ เคสใหม่</button>'
    +(state.history.length>1?'<button class="btn btn-teal" onclick="switchTab(\'overview\')">ดูภาพรวม →</button>':'')
    +'</div>';

  document.getElementById('pane-result').innerHTML = html;
}

// ── Render Overview ────────────────────────────────────────────
function renderOverview() {
  var h = state.history;
  var total = h.length;
  var green = h.filter(function(x){ return x.result.overall_score >= 75; }).length;
  var yellow = h.filter(function(x){ return x.result.overall_score >= 60 && x.result.overall_score < 75; }).length;
  var red = h.filter(function(x){ return x.result.overall_score < 60; }).length;
  var byC = {};
  h.forEach(function(x){
    if (!byC[x.consultant]) byC[x.consultant] = [];
    byC[x.consultant].push(x.result.overall_score);
  });
  var perfRows = Object.entries(byC).map(function(e){
    var name=e[0], scores=e[1];
    var avg = Math.round(scores.reduce(function(a,b){return a+b;},0)/scores.length);
    var z = zoneOf(avg);
    return '<div class="perf-row"><div class="perf-name">'+name+'</div>'
      +'<div class="perf-bar-wrap"><div class="perf-bar-fill" style="width:'+avg+'%;background:'+z.color+'"></div></div>'
      +'<div class="perf-score" style="color:'+z.color+'">'+avg+'</div>'
      +'<div class="perf-icon">'+zoneIcon(avg)+'</div>'
      +'<div class="perf-cnt">'+scores.length+'เคส</div></div>';
  }).join('');

  var actionHtml = red > 0 ? '<div style="font-size:13px;color:var(--t2);margin-bottom:4px">🔴 '+red+' เคส → Supervisor ดำเนินการทันที</div>' : '';
  actionHtml += yellow > 0 ? '<div style="font-size:13px;color:var(--t2)">🟡 '+yellow+' เคส → Coach ภายใน 3 วัน</div>' : '';
  if (!red && !yellow) actionHtml = '<div style="font-size:13px;color:#5DCAA5">✓ ทุกเคสผ่านมาตรฐาน</div>';

  document.getElementById('pane-overview').innerHTML =
    '<div style="font-size:15px;font-weight:500;margin-bottom:3px">Overview Report</div>'
    +'<div style="font-size:11px;color:var(--t3);margin-bottom:14px">ภาพรวม · '+total+' เคส</div>'
    +'<div class="stat-grid">'
    +[{l:'ทั้งหมด',v:total,c:'#fff'},{l:'🟢 ผ่าน',v:green,c:'#5DCAA5'},{l:'🟡 Coach',v:yellow,c:'#EF9F27'},{l:'🔴 Critical',v:red,c:'#E24B4A'}].map(function(s){
      return '<div class="stat-box"><div class="stat-num" style="color:'+s.c+'">'+s.v+'</div><div class="stat-lbl">'+s.l+'</div></div>';
    }).join('')+'</div>'
    +'<div class="card" style="margin-bottom:12px"><div class="card-title" style="color:var(--t3)">Performance รายบุคคล</div>'+perfRows+'</div>'
    +'<div class="action-box" style="background:rgba(226,75,74,.06);border:0.5px solid rgba(226,75,74,.18)"><div style="font-size:10px;font-weight:600;color:#E24B4A;text-transform:uppercase;letter-spacing:.1em;margin-bottom:7px">🚨 Action Required</div>'+actionHtml+'</div>';
}

// ── Render History ─────────────────────────────────────────────
function renderHistory() {
  var html = '<div style="font-size:15px;font-weight:500;margin-bottom:3px">ประวัติการวิเคราะห์</div>'
    +'<div style="font-size:11px;color:var(--t3);margin-bottom:14px">'+state.history.length+' เคส · คลิกเพื่อดูผลลัพธ์</div>';
  state.history.forEach(function(item, idx) {
    var z = zoneOf(item.result.overall_score);
    var flags = item.result.red_flags||[];
    html += '<div class="hist-item" onclick="viewHistory('+idx+')">'
      +'<div class="hist-icon">'+zoneIcon(item.result.overall_score)+'</div>'
      +'<div class="hist-info"><div class="hist-name">'+item.consultant+' · '+item.date+'</div>'
      +'<div class="hist-meta">'+item.filename+(flags.length?' · ⚠ '+flags.length+' red flag':' · ไม่มี red flag')+'</div></div>'
      +'<div class="hist-score"><div class="hist-score-num" style="color:'+z.color+'">'+item.result.overall_score+'</div>'
      +'<div class="hist-score-lbl" style="color:'+z.color+'">'+z.label+'</div></div></div>';
  });
  document.getElementById('pane-history').innerHTML = html;
}

function viewHistory(idx) {
  var item = state.history[idx];
  state.lastResult = item.result;
  state.lastConsultant = item.consultant;
  state.lastDate = item.date;
  renderResult(item.result, item.consultant, item.date);
  switchTab('result');
}

// ── Tab switching ──────────────────────────────────────────────
function switchTab(id) {
  ['analyze','result','overview','history'].forEach(function(t) {
    document.getElementById('pane-'+t).style.display = t===id?'block':'none';
    var btn = document.getElementById('tab-'+t);
    if (btn) btn.className = 'tab' + (t===id?' active':'');
  });
  if (id === 'overview') renderOverview();
  if (id === 'history') renderHistory();
}
</script>
</body>
</html>
