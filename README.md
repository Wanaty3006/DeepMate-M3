<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>DeepMate M3 — Consultation QA</title>
<link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--bg:#08080f;--bg2:#0f0f1a;--bg3:#14141f;--t1:#fff;--t2:rgba(255,255,255,.65);--t3:rgba(255,255,255,.35);--teal:#5DCAA5;--amber:#EF9F27;--purple:#7F77DD;--red:#E24B4A;--blue:#378ADD;--border:rgba(255,255,255,.08)}
html,body{min-height:100%;background:var(--bg);color:var(--t1);font-family:'Prompt',system-ui,sans-serif}
.wrap{max-width:860px;margin:0 auto;padding:28px 22px 60px}
/* header */
.hdr{display:flex;align-items:center;gap:10px;margin-bottom:22px}
.badge{font-size:10px;background:rgba(239,159,39,.15);color:var(--amber);padding:3px 9px;border-radius:10px;border:.5px solid rgba(239,159,39,.3)}
/* tabs */
.tabs{display:flex;gap:2px;margin-bottom:22px;background:rgba(255,255,255,.04);padding:3px;border-radius:10px;width:fit-content}
.tab-btn{padding:7px 15px;border-radius:7px;border:none;background:transparent;color:rgba(255,255,255,.4);font-size:12px;cursor:pointer;font-family:inherit}
.tab-btn.on{background:rgba(255,255,255,.12);color:#fff;font-weight:500}
.tab-btn:disabled{opacity:.25;cursor:default}
/* stepbar */
.stepbar{display:flex;align-items:center;margin-bottom:20px;gap:0}
.sc{display:flex;flex-direction:column;align-items:center;gap:3px}
.sc-circle{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:600}
.sc-done{background:var(--teal);color:#000}
.sc-active{background:var(--amber);color:#000}
.sc-idle{background:rgba(255,255,255,.07);color:rgba(255,255,255,.3)}
.sc-lbl{font-size:9px;white-space:nowrap}
.sc-lbl.done{color:var(--teal)}.sc-lbl.active{color:var(--amber)}.sc-lbl.idle{color:rgba(255,255,255,.25)}
.sl{flex:1;height:1.5px;margin:0 4px;margin-bottom:14px}
/* card */
.card{background:var(--bg2);border:.5px solid var(--border);border-radius:12px;padding:16px 18px;margin-bottom:10px}
.card.hi{border-color:rgba(239,159,39,.35)}
.card.lo{border-color:rgba(93,202,165,.2);opacity:.75}
.ct{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.14em;margin-bottom:12px}
/* form */
.row2{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:10px}
.fl label{display:block;font-size:10px;color:var(--t3);margin-bottom:4px}
.fl input,.fl select{width:100%;background:rgba(255,255,255,.04);border:.5px solid rgba(255,255,255,.1);border-radius:8px;padding:8px 11px;color:var(--t1);font-size:13px;font-family:inherit;outline:none;color-scheme:dark}
.krow{display:flex;align-items:center;gap:6px;margin-bottom:4px}
.ktgl{background:none;border:none;font-size:10px;color:rgba(255,255,255,.3);cursor:pointer;font-family:inherit}
.hint{font-size:10px;color:rgba(255,255,255,.2);line-height:1.5;margin-top:3px}
.hint a{color:rgba(55,138,221,.7)}
/* upload */
.uz{border:1.5px dashed rgba(255,255,255,.12);border-radius:10px;padding:30px;text-align:center;cursor:pointer;transition:all .2s}
.uz:hover{border-color:rgba(255,255,255,.25)}
.uz.has{border-color:var(--teal);background:rgba(93,202,165,.04)}
/* buttons */
.btn{border:.5px solid var(--border);border-radius:8px;padding:9px 20px;font-size:13px;font-family:inherit;cursor:pointer;color:var(--t2);background:transparent;transition:all .15s}
.btn:hover{background:rgba(255,255,255,.06)}
.btn.pri{background:var(--amber);color:#000;border-color:var(--amber);font-weight:700}
.btn.teal{background:var(--teal);color:#000;border-color:var(--teal);font-weight:700}
.btn:disabled{opacity:.35;cursor:not-allowed}
.brow{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin-top:12px}
/* divider */
.div{display:flex;align-items:center;gap:8px;margin:10px 0}
.dl{flex:1;height:.5px;background:rgba(255,255,255,.07)}
.dt{font-size:11px;color:rgba(255,255,255,.25)}
/* tx */
textarea{width:100%;min-height:160px;background:rgba(255,255,255,.03);border:.5px solid rgba(255,255,255,.08);border-radius:8px;padding:12px;color:rgba(255,255,255,.8);font-size:13px;font-family:inherit;resize:vertical;outline:none;line-height:1.75}
/* progress */
.prog{display:flex;align-items:center;gap:10px;padding:12px 15px;background:rgba(239,159,39,.07);border-radius:8px;display:none}
@keyframes spin{to{transform:rotate(360deg)}}
.spin{width:15px;height:15px;border:2px solid rgba(239,159,39,.25);border-top-color:var(--amber);border-radius:50%;animation:spin .8s linear infinite;flex-shrink:0}
/* error */
.err{background:rgba(226,75,74,.1);border:.5px solid rgba(226,75,74,.3);border-radius:8px;padding:10px 14px;font-size:12px;color:#f09595;line-height:1.6;display:none;margin-top:8px}
/* info box */
.info{display:flex;gap:8px;padding:10px 13px;background:rgba(55,138,221,.07);border:.5px solid rgba(55,138,221,.2);border-radius:8px;font-size:12px;color:rgba(55,138,221,.9);line-height:1.6;margin-bottom:12px}
/* result */
.rhero{display:grid;grid-template-columns:auto 1fr;gap:18px;padding:16px 18px;border-radius:14px;margin-bottom:14px;align-items:center}
.sg2{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:12px}
.scard{background:var(--bg2);border:.5px solid var(--border);border-radius:12px;padding:13px 15px}
.srow{margin-bottom:9px}
.shead{display:flex;justify-content:space-between;align-items:center;margin-bottom:3px}
.sbar{height:4px;background:rgba(255,255,255,.06);border-radius:2px;overflow:hidden;margin-bottom:2px}
.sfill{height:100%;border-radius:2px}
.snote{font-size:10px;color:rgba(255,255,255,.28);line-height:1.4}
.wbadge{font-size:9px;color:rgba(255,255,255,.2);background:rgba(255,255,255,.05);padding:1px 5px;border-radius:3px}
.ins{border-radius:10px;padding:12px 14px}
.ins-t{font-size:10px;font-weight:600;text-transform:uppercase;letter-spacing:.1em;margin-bottom:7px}
.ins-i{font-size:12px;color:var(--t2);padding-left:9px;margin-bottom:5px;line-height:1.5;border-left:2px solid}
.fbox{background:rgba(127,119,221,.07);border-radius:7px;padding:8px 11px;font-size:11px;color:rgba(255,255,255,.4);margin-top:10px}
/* overview */
.sg4{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:14px}
.sbox{background:rgba(255,255,255,.03);border:.5px solid var(--border);border-radius:10px;padding:12px;text-align:center}
.sn{font-size:26px;font-weight:400;margin-bottom:3px}
.sl2{font-size:11px;color:var(--t3)}
/* history */
.hi-item{display:flex;align-items:center;gap:10px;padding:9px 13px;background:rgba(255,255,255,.03);border:.5px solid var(--border);border-radius:9px;cursor:pointer;margin-bottom:5px;transition:background .15s}
.hi-item:hover{background:rgba(255,255,255,.06)}
</style>
</head>
<body>
<div class="wrap">

  <div class="hdr">
    <div style="width:10px;height:10px;border-radius:50%;background:var(--amber)"></div>
    <span style="font-size:17px;font-weight:500">DeepMate · M3 Consultation QA</span>
    <span class="badge">LIC · Audio Input</span>
    <span id="case-lbl" style="margin-left:auto;font-size:11px;color:var(--t3)"></span>
  </div>

  <!-- JS check indicator (hidden once JS runs) -->
  <div id="no-js" style="background:rgba(226,75,74,.1);border:.5px solid rgba(226,75,74,.3);border-radius:8px;padding:10px 14px;font-size:12px;color:#f09595;margin-bottom:14px">
    ⏳ กำลังโหลด JavaScript...
  </div>

  <div class="tabs">
    <button class="tab-btn on" id="t-analyze">🎙 วิเคราะห์</button>
    <button class="tab-btn" id="t-result" disabled>📊 ผลลัพธ์</button>
    <button class="tab-btn" id="t-overview" disabled>🗂 ภาพรวม</button>
    <button class="tab-btn" id="t-history" disabled>🕐 ประวัติ</button>
  </div>

  <!-- ANALYZE PANE -->
  <div id="pane-analyze">
    <div class="stepbar" id="stepbar"></div>

    <!-- S1 -->
    <div class="card hi" id="cs1">
      <div class="ct" style="color:var(--amber)">Step 1 · ตั้งค่า</div>
      <div class="row2">
        <div class="fl">
          <label>Consultant</label>
          <select id="f-consultant">
            <option>น้ำ</option><option>กิต</option><option>นัท</option>
            <option>เพิร์ล</option><option>วิว</option><option>อื่นๆ</option>
          </select>
        </div>
        <div class="fl">
          <label>วันที่</label>
          <input type="date" id="f-date">
        </div>
      </div>
      <div class="fl" style="margin-bottom:10px">
        <div class="krow">
          <label style="margin:0;font-size:10px;color:var(--t3)">AssemblyAI API Key</label>
          <button class="ktgl" id="tgl-aai">แสดง</button>
        </div>
        <input type="password" id="f-aai" placeholder="xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" style="font-family:monospace;font-size:12px">
        <div class="hint">รับฟรีที่ <a href="https://www.assemblyai.com" target="_blank">assemblyai.com</a> → Dashboard → API Key</div>
      </div>
      <div class="fl">
        <div class="krow">
          <label style="margin:0;font-size:10px;color:var(--t3)">Anthropic API Key</label>
          <button class="ktgl" id="tgl-ant">แสดง</button>
        </div>
        <input type="password" id="f-ant" placeholder="sk-ant-api03-xxxxxxxxxxxx" style="font-family:monospace;font-size:12px">
        <div class="hint">รับที่ <a href="https://console.anthropic.com" target="_blank">console.anthropic.com</a> → API Keys</div>
      </div>
      <div id="err-s1" class="err"></div>
      <div class="brow"><button class="btn pri" id="btn-s1next">ถัดไป →</button></div>
    </div>

    <!-- S2 -->
    <div class="card" id="cs2" style="display:none">
      <div class="ct" id="lbl-s2">Step 2 · อัปโหลดไฟล์เสียง</div>
      <div class="uz" id="uz">
        <input type="file" id="f-audio" accept=".mp3,.mp4,.m4a,.wav,.webm,.ogg,.aac" style="display:none">
        <div id="uz-inner">
          <div style="font-size:34px;opacity:.3;margin-bottom:8px">🎵</div>
          <div style="font-size:13px;color:rgba(255,255,255,.5);margin-bottom:4px">คลิกเพื่อเลือกไฟล์เสียง</div>
          <div style="font-size:11px;color:rgba(255,255,255,.25)">MP3 · MP4 · M4A · WAV · WebM · AAC</div>
        </div>
      </div>
      <div class="brow" id="brow-s2" style="display:none">
        <button class="btn pri" id="btn-s2next">ถัดไป →</button>
        <button class="btn" id="btn-s2chg">เปลี่ยนไฟล์</button>
      </div>
    </div>

    <!-- S3 -->
    <div class="card" id="cs3" style="display:none">
      <div class="ct" id="lbl-s3">Step 3 · ถอดเสียงภาษาไทย</div>
      <div class="info"><span>ℹ️</span><span>ใช้ AssemblyAI ถอดเสียงภาษาไทย + อังกฤษ · ไฟล์ขนาดใหญ่อาจใช้เวลา 1–3 นาที</span></div>
      <div class="prog" id="prog-tx"><div class="spin"></div><span id="msg-tx" style="font-size:12px;color:var(--amber)"></span></div>
      <div id="brow-s3">
        <div class="brow"><button class="btn pri" id="btn-tx">🎙 เริ่มถอดเสียงอัตโนมัติ</button></div>
        <div class="div"><div class="dl"></div><div class="dt">หรือถ้าถอดไม่ได้</div><div class="dl"></div></div>
        <button class="btn" id="btn-s3skip" style="font-size:12px">✏️ วาง Transcript เองในขั้นตอนถัดไป</button>
      </div>
      <div id="err-s3" class="err"></div>
    </div>

    <!-- S4 -->
    <div class="card" id="cs4" style="display:none">
      <div class="ct" id="lbl-s4">Step 4 · ตรวจสอบ Transcript</div>
      <div style="font-size:11px;color:var(--t3);margin-bottom:6px">แก้ไขได้ถ้าถอดผิด <span id="wc"></span></div>
      <textarea id="f-tx" placeholder="วาง Transcript ที่นี่..."></textarea>
      <div class="brow"><button class="btn pri" id="btn-s4next">ถัดไป →</button></div>
    </div>

    <!-- S5 -->
    <div class="card" id="cs5" style="display:none">
      <div class="ct" style="color:var(--amber)">Step 5 · วิเคราะห์ด้วย AI</div>
      <div class="prog" id="prog-ai"><div class="spin"></div><span style="font-size:12px;color:var(--amber)">กำลังวิเคราะห์ด้วย Claude...</span></div>
      <div id="err-s5" class="err"></div>
      <div class="brow">
        <button class="btn pri" id="btn-analyze">🔍 วิเคราะห์ Consultation</button>
        <button class="btn" id="btn-reset">↺ เริ่มใหม่</button>
      </div>
    </div>
  </div>

  <div id="pane-result" style="display:none"></div>
  <div id="pane-overview" style="display:none"></div>
  <div id="pane-history" style="display:none"></div>
</div>

<script>
// ── Confirm JS loaded ──────────────────────────────────────
document.getElementById('no-js').style.display = 'none';

// ── State ──────────────────────────────────────────────────
var S = { step:1, file:null, history:[] };

// ── Init ───────────────────────────────────────────────────
document.getElementById('f-date').value = new Date().toISOString().slice(0,10);

// ── Zone helper ────────────────────────────────────────────
function zone(s) {
  if (s >= 90) return {lbl:'Excellent', c:'#22c55e', bg:'rgba(34,197,94,.1)', act:'ยกย่อง / ใช้เป็น Best Practice'};
  if (s >= 75) return {lbl:'Pass',      c:'#5DCAA5', bg:'rgba(93,202,165,.08)', act:'ผ่านมาตรฐาน'};
  if (s >= 60) return {lbl:'Warning',   c:'#EF9F27', bg:'rgba(239,159,39,.08)', act:'Coach ภายใน 3 วัน'};
  return              {lbl:'Critical',  c:'#E24B4A', bg:'rgba(226,75,74,.08)',  act:'Supervisor ดำเนินการทันที'};
}
function zicon(s) { return s>=75?'🟢':s>=60?'🟡':'🔴'; }

// ── Stepbar ────────────────────────────────────────────────
var SLABELS = ['ตั้งค่า','อัปโหลด','ถอดเสียง','ตรวจสอบ','วิเคราะห์'];
function drawStepbar() {
  var sb = document.getElementById('stepbar');
  var h = '';
  for (var i = 1; i <= 5; i++) {
    var cls = S.step > i ? 'done' : S.step === i ? 'active' : 'idle';
    var ic  = S.step > i ? '✓' : String(i);
    h += '<div class="sc">'
       + '<div class="sc-circle sc-'+cls+'">'+ic+'</div>'
       + '<div class="sc-lbl '+cls+'">'+SLABELS[i-1]+'</div>'
       + '</div>';
    if (i < 5) {
      var lineColor = S.step > i ? 'var(--teal)' : 'rgba(255,255,255,.07)';
      h += '<div class="sl" style="background:'+lineColor+'"></div>';
    }
  }
  sb.innerHTML = h;
}
drawStepbar();

// ── Show/hide cards ────────────────────────────────────────
function showCards(n) {
  var ids = ['cs1','cs2','cs3','cs4','cs5'];
  var lbls = {2:'lbl-s2', 3:'lbl-s3', 4:'lbl-s4'};
  var amberStep = ['Step 2 · อัปโหลดไฟล์เสียง','Step 3 · ถอดเสียงภาษาไทย','Step 4 · ตรวจสอบ Transcript'];
  for (var i = 0; i < ids.length; i++) {
    var idx = i + 1;
    var el = document.getElementById(ids[i]);
    if (!el) continue;
    if (idx <= n) {
      el.style.display = 'block';
      el.className = 'card' + (idx === n ? ' hi' : ' lo');
    } else {
      el.style.display = 'none';
    }
  }
  // Update sub-titles color
  for (var k in lbls) {
    var le = document.getElementById(lbls[k]);
    if (le) le.style.color = S.step === parseInt(k) ? 'var(--amber)' : 'rgba(255,255,255,.4)';
  }
}

// ── Step navigation ────────────────────────────────────────
function goStep(n) {
  S.step = n;
  drawStepbar();
  showCards(n);
}

// ── Show/hide error ────────────────────────────────────────
function showErr(id, msg) {
  var el = document.getElementById(id);
  if (!el) return;
  if (msg) { el.style.display = 'block'; el.textContent = '⚠️ ' + msg; }
  else { el.style.display = 'none'; }
}

// ── Key toggles ────────────────────────────────────────────
function bindKeyToggle(btnId, inputId) {
  document.getElementById(btnId).addEventListener('click', function() {
    var inp = document.getElementById(inputId);
    if (inp.type === 'password') { inp.type = 'text'; this.textContent = 'ซ่อน'; }
    else { inp.type = 'password'; this.textContent = 'แสดง'; }
  });
}
bindKeyToggle('tgl-aai','f-aai');
bindKeyToggle('tgl-ant','f-ant');

// ── Step 1 next ────────────────────────────────────────────
document.getElementById('btn-s1next').addEventListener('click', function() {
  showErr('err-s1', '');
  var aai = document.getElementById('f-aai').value.trim();
  var ant = document.getElementById('f-ant').value.trim();
  if (!aai && !ant) { showErr('err-s1','กรุณากรอก API Key ทั้ง 2 ช่อง'); return; }
  if (!aai) { showErr('err-s1','กรุณากรอก AssemblyAI API Key'); return; }
  if (!ant) { showErr('err-s1','กรุณากรอก Anthropic API Key'); return; }
  goStep(2);
});

// ── File upload ────────────────────────────────────────────
var uz = document.getElementById('uz');
uz.addEventListener('click', function() { document.getElementById('f-audio').click(); });
document.getElementById('f-audio').addEventListener('change', function() {
  var f = this.files[0];
  if (!f) return;
  S.file = f;
  uz.className = 'uz has';
  document.getElementById('uz-inner').innerHTML =
    '<div style="font-size:28px;margin-bottom:8px">🎙</div>'
    +'<div style="font-size:13px;font-weight:500;color:var(--teal);margin-bottom:3px">'+f.name+'</div>'
    +'<div style="font-size:11px;color:var(--t3)">'+(f.size/1024/1024).toFixed(2)+' MB</div>';
  document.getElementById('brow-s2').style.display = 'flex';
});
document.getElementById('btn-s2next').addEventListener('click', function() { goStep(3); });
document.getElementById('btn-s2chg').addEventListener('click', function() { document.getElementById('f-audio').click(); });

// ── Transcribe ────────────────────────────────────────────
document.getElementById('btn-tx').addEventListener('click', function() {
  var aai = document.getElementById('f-aai').value.trim();
  showErr('err-s3','');
  if (!S.file) { showErr('err-s3','ยังไม่ได้เลือกไฟล์เสียง'); return; }
  if (!aai)    { showErr('err-s3','ไม่พบ AssemblyAI API Key — กลับ Step 1'); return; }

  document.getElementById('brow-s3').style.display = 'none';
  document.getElementById('prog-tx').style.display = 'flex';
  var msgEl = document.getElementById('msg-tx');

  function setMsg(t) { msgEl.textContent = t; }
  function done(text) {
    document.getElementById('prog-tx').style.display = 'none';
    document.getElementById('brow-s3').style.display = 'block';
    document.getElementById('f-tx').value = text;
    updateWC();
    goStep(4);
  }
  function fail(msg) {
    document.getElementById('prog-tx').style.display = 'none';
    document.getElementById('brow-s3').style.display = 'block';
    showErr('err-s3', msg);
  }

  setMsg('กำลังเตรียมไฟล์...');
  var reader = new FileReader();
  reader.onerror = function() { fail('อ่านไฟล์ไม่ได้'); };
  reader.onload = function(ev) {
    setMsg('กำลังอัปโหลดไปยัง AssemblyAI...');
    fetch('https://api.assemblyai.com/v2/upload', {
      method:'POST',
      headers:{ authorization: aai },
      body: ev.target.result
    })
    .then(function(r) {
      if (r.status === 401) throw new Error('API Key ไม่ถูกต้อง — ตรวจสอบใน Step 1');
      if (!r.ok) throw new Error('Upload ล้มเหลว HTTP ' + r.status);
      return r.json();
    })
    .then(function(d) {
      setMsg('กำลังส่งคำขอถอดเสียง (v3)...');
      return fetch('https://api.assemblyai.com/v3/transcript', {
        method:'POST',
        headers:{ authorization:aai, 'content-type':'application/json' },
        body: JSON.stringify({
          audio_url: d.upload_url,
          speech_models: ['universal-3-pro', 'universal-2'],
          language_detection: true
        })
      });
    })
    .then(function(r) {
      if (r.status === 401) throw new Error('API Key ไม่ถูกต้อง — ตรวจสอบใน Step 1');
      if (!r.ok) return r.text().then(function(t){ throw new Error('ส่งคำขอถอดเสียงล้มเหลว: '+t); });
      return r.json();
    })
    .then(function(d) {
      if (!d.id) throw new Error('ไม่ได้รับ transcript ID จาก AssemblyAI');
      return pollTx(aai, d.id, 0, setMsg);
    })
    .then(done)
    .catch(function(e) { fail(e.message || 'เกิดข้อผิดพลาด'); });
  };
  reader.readAsArrayBuffer(S.file);
});

function pollTx(key, id, n, setMsg) {
  if (n > 80) return Promise.reject(new Error('หมดเวลา — ลองใหม่'));
  return new Promise(function(r){ setTimeout(r,3000); }).then(function() {
    setMsg('กำลังถอดเสียง... ' + ((n+1)*3) + 's');
    return fetch('https://api.assemblyai.com/v2/transcript/'+id, { headers:{ authorization:key } })
      .then(function(r){ return r.json(); });
  }).then(function(d) {
    if (d.status === 'completed') return d.text || '';
    if (d.status === 'error') throw new Error('ถอดเสียงล้มเหลว: '+d.error);
    return pollTx(key, id, n+1, setMsg);
  });
}

document.getElementById('btn-s3skip').addEventListener('click', function() { goStep(4); });

// ── Transcript word count ─────────────────────────────────
function updateWC() {
  var t = document.getElementById('f-tx').value;
  var n = t.split(/\s+/).filter(Boolean).length;
  document.getElementById('wc').textContent = n ? '· '+n+' คำ' : '';
}
document.getElementById('f-tx').addEventListener('input', updateWC);
document.getElementById('btn-s4next').addEventListener('click', function() { goStep(5); });

// ── Analyze ───────────────────────────────────────────────
var SYS = 'คุณคือผู้เชี่ยวชาญประเมินคุณภาพการให้คำปรึกษาด้านการศึกษา (Consultation QA) ของ LIC\n'
+ 'บริบท: Consultant ให้คำปรึกษาแนะนำเตรียมสอบ/วางแผนการเรียน กับนักเรียนและผู้ปกครอง 1:1 ระยะ 15-30 นาที\n'
+ 'หมายเหตุ: Transcript ถอดจากเสียงภาษาไทยและอาจมีภาษาอังกฤษปน อาจมีคำผิดบ้าง ให้พิจารณาจากบริบท\n\n'
+ 'มาตรฐาน 5 ขั้นตอน:\n'
+ '1. Opening (10%): ทักทาย แนะนำตัว เปิดโอกาสให้พูดก่อน\n'
+ '2. Needs Assessment (25%): ถามเป้าหมาย สถานการณ์ ปัญหา\n'
+ '3. Information (30%): ให้ข้อมูลถูกต้อง สนามสอบ ปฏิทิน หลักสูตร\n'
+ '4. Action Plan (25%): วางแผนชัด Personalized\n'
+ '5. Closing (10%): สรุป ถามข้อสงสัย นัดติดตาม\n\n'
+ 'Academic Quality 70% + Emotional Intelligence 30%\n'
+ 'ส่งคืน JSON เท่านั้น:\n'
+ '{"protocol":{"opening":{"score":0,"found":false,"note":""},"needs":{"score":0,"found":false,"note":""},"info":{"score":0,"found":false,"note":""},"plan":{"score":0,"found":false,"note":""},"closing":{"score":0,"found":false,"note":""}},'
+ '"academic_score":0,"emotional":{"empathy":{"score":0,"note":""},"clarity":{"score":0,"note":""},"confidence":{"score":0,"note":""}},'
+ '"emotional_score":0,"overall_score":0,"red_flags":[],"strengths":[],"improvements":[],"coaching_focus":""}';

document.getElementById('btn-analyze').addEventListener('click', function() {
  var tx  = document.getElementById('f-tx').value.trim();
  var ant = document.getElementById('f-ant').value.trim();
  showErr('err-s5','');
  if (!tx)  { showErr('err-s5','ไม่มี Transcript — กลับ Step 4'); return; }
  if (!ant) { showErr('err-s5','ไม่พบ Anthropic API Key — กลับ Step 1'); return; }

  document.getElementById('btn-analyze').disabled = true;
  document.getElementById('prog-ai').style.display = 'flex';

  fetch('https://api.anthropic.com/v1/messages', {
    method:'POST',
    headers:{'Content-Type':'application/json'},
    body: JSON.stringify({
      model:'claude-sonnet-4-20250514',
      max_tokens:2000,
      system: SYS,
      messages:[{role:'user', content:'วิเคราะห์:\n\n'+tx}]
    })
  })
  .then(function(r){ return r.json(); })
  .then(function(data) {
    var txt = data.content[0].text.trim();
    var m = txt.match(/\{[\s\S]*\}/);
    if (!m) throw new Error('ไม่สามารถ Parse ผลลัพธ์');
    var parsed = JSON.parse(m[0]);
    var entry = {
      consultant: document.getElementById('f-consultant').value,
      date:       document.getElementById('f-date').value,
      file:       S.file ? S.file.name : 'manual',
      result:     parsed
    };
    S.history.unshift(entry);
    if (S.history.length > 30) S.history.pop();
    updateUI();
    renderResult(entry);
    switchTab('result');
  })
  .catch(function(e) { showErr('err-s5', e.message || 'เกิดข้อผิดพลาด'); })
  .finally(function() {
    document.getElementById('btn-analyze').disabled = false;
    document.getElementById('prog-ai').style.display = 'none';
  });
});

document.getElementById('btn-reset').addEventListener('click', resetAll);

// ── Reset ─────────────────────────────────────────────────
function resetAll() {
  S.step = 1; S.file = null;
  document.getElementById('f-tx').value = '';
  document.getElementById('wc').textContent = '';
  document.getElementById('uz').className = 'uz';
  document.getElementById('uz-inner').innerHTML =
    '<div style="font-size:34px;opacity:.3;margin-bottom:8px">🎵</div>'
    +'<div style="font-size:13px;color:rgba(255,255,255,.5);margin-bottom:4px">คลิกเพื่อเลือกไฟล์เสียง</div>'
    +'<div style="font-size:11px;color:rgba(255,255,255,.25)">MP3 · MP4 · M4A · WAV · WebM · AAC</div>';
  document.getElementById('brow-s2').style.display = 'none';
  document.getElementById('brow-s3').style.display = 'block';
  ['err-s1','err-s3','err-s5'].forEach(function(id){ showErr(id,''); });
  drawStepbar(); showCards(1); switchTab('analyze');
}

// ── Tab switching ─────────────────────────────────────────
function switchTab(id) {
  ['analyze','result','overview','history'].forEach(function(t) {
    document.getElementById('pane-'+t).style.display = t===id ? 'block' : 'none';
    document.getElementById('t-'+t).className = 'tab-btn' + (t===id ? ' on' : '');
  });
  if (id==='overview') renderOverview();
  if (id==='history')  renderHistory();
}
['t-analyze','t-result','t-overview','t-history'].forEach(function(btnId) {
  document.getElementById(btnId).addEventListener('click', function() {
    if (!this.disabled) switchTab(btnId.replace('t-',''));
  });
});

function updateUI() {
  var n = S.history.length;
  document.getElementById('case-lbl').textContent = n ? n+' เคส' : '';
  document.getElementById('t-result').disabled   = !S.history.length;
  document.getElementById('t-overview').disabled = !S.history.length;
  document.getElementById('t-history').disabled  = !S.history.length;
}

// ── Gauge SVG ─────────────────────────────────────────────
function gauge(score, sz) {
  var z=zone(score), r=sz/2-8, circ=Math.PI*r, dash=(score/100)*circ;
  return '<svg width="'+sz+'" height="'+(sz/2+14)+'" viewBox="0 0 '+sz+' '+(sz/2+14)+'">'
    +'<path d="M8,'+sz/2+' A'+r+','+r+' 0 0,1 '+(sz-8)+','+sz/2+'" fill="none" stroke="rgba(255,255,255,.07)" stroke-width="7" stroke-linecap="round"/>'
    +'<path d="M8,'+sz/2+' A'+r+','+r+' 0 0,1 '+(sz-8)+','+sz/2+'" fill="none" stroke="'+z.c+'" stroke-width="7" stroke-linecap="round" stroke-dasharray="'+dash.toFixed(1)+' '+circ.toFixed(1)+'"/>'
    +'<text x="'+sz/2+'" y="'+(sz/2+2)+'" text-anchor="middle" fill="'+z.c+'" font-size="'+(sz*.2)+'" font-weight="600" font-family="system-ui">'+score+'</text>'
    +'<text x="'+sz/2+'" y="'+(sz/2+14)+'" text-anchor="middle" fill="rgba(255,255,255,.4)" font-size="'+(sz*.1)+'" font-family="system-ui">'+z.lbl+'</text>'
    +'</svg>';
}

// ── Render result ─────────────────────────────────────────
var PSTEPS = [
  {id:'opening',lbl:'Opening',w:10},
  {id:'needs',  lbl:'Needs Assessment',w:25},
  {id:'info',   lbl:'Information',w:30},
  {id:'plan',   lbl:'Action Plan',w:25},
  {id:'closing',lbl:'Closing',w:10},
];
function renderResult(entry) {
  var r=entry.result, z=zone(r.overall_score);
  var flags=(r.red_flags||[]).map(function(f){ return '<span style="font-size:11px;background:rgba(226,75,74,.15);color:#f09595;padding:2px 8px;border-radius:8px;border:.5px solid rgba(226,75,74,.25)">🚩 '+f+'</span>'; }).join('');
  var prRows=PSTEPS.map(function(ps){
    var s=r.protocol&&r.protocol[ps.id]; if(!s) return '';
    return '<div class="srow"><div class="shead"><div style="display:flex;align-items:center;gap:5px;font-size:11px;color:var(--t2)"><span>'+
      (s.found?'✓':'✗')+'</span>'+ps.lbl+'<span class="wbadge">×'+ps.w+'%</span></div><div style="font-size:12px;font-weight:600;color:'+zone(s.score).c+'">'+s.score+'</div></div>'+
      '<div class="sbar"><div class="sfill" style="width:'+s.score+'%;background:'+zone(s.score).c+'"></div></div>'+
      (s.note?'<div class="snote">'+s.note+'</div>':'')+'</div>';
  }).join('');
  var emRows=r.emotional?Object.entries(r.emotional).map(function(e){
    var k=e[0],v=e[1];
    return '<div class="srow"><div class="shead"><div style="font-size:11px;color:var(--t2);text-transform:capitalize">'+k+'</div><div style="font-size:12px;font-weight:600;color:'+zone(v.score).c+'">'+v.score+'</div></div>'+
      '<div class="sbar"><div class="sfill" style="width:'+v.score+'%;background:'+zone(v.score).c+'"></div></div>'+
      (v.note?'<div class="snote">'+v.note+'</div>':'')+'</div>';
  }).join('') : '';
  var str=(r.strengths||[]).map(function(s){ return '<div class="ins-i" style="border-left-color:#5DCAA5">'+s+'</div>'; }).join('');
  var imp=(r.improvements||[]).map(function(s){ return '<div class="ins-i" style="border-left-color:#EF9F27">'+s+'</div>'; }).join('');

  var html='<div class="rhero" style="background:'+z.bg+';border:.5px solid '+z.c+'40">'
    +'<div>'+gauge(r.overall_score,110)+'</div>'
    +'<div style="display:flex;flex-direction:column;gap:7px">'
    +'<div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap"><span style="font-size:18px">'+zicon(r.overall_score)+'</span><span style="font-size:17px;font-weight:600;color:'+z.c+'">'+z.lbl+'</span><span style="font-size:11px;color:var(--t3)">· '+entry.consultant+' · '+entry.date+'</span></div>'
    +'<div style="font-size:12px;background:rgba(0,0,0,.25);padding:8px 13px;border-radius:8px;color:var(--t2)"><strong style="color:'+z.c+'">Action: </strong>'+z.act+'</div>'
    +(flags?'<div style="display:flex;gap:5px;flex-wrap:wrap">'+flags+'</div>':'')
    +'</div></div>'
    +'<div class="sg2">'
    +'<div class="scard"><div class="ct" style="color:#5DCAA5">Academic Quality · '+r.academic_score+'</div>'+prRows+'</div>'
    +'<div class="scard"><div class="ct" style="color:#7F77DD">Emotional Intelligence · '+r.emotional_score+'</div>'+emRows
    +'<div class="fbox">'+r.academic_score+'×70% + '+r.emotional_score+'×30% = <strong style="color:#fff">'+r.overall_score+'</strong></div>'
    +'</div></div>'
    +'<div class="sg2">'
    +'<div class="ins" style="background:rgba(93,202,165,.06);border:.5px solid rgba(93,202,165,.18)"><div class="ins-t" style="color:#5DCAA5">✓ จุดเด่น</div>'+str+'</div>'
    +'<div class="ins" style="background:rgba(239,159,39,.06);border:.5px solid rgba(239,159,39,.18)"><div class="ins-t" style="color:#EF9F27">⚡ ควรพัฒนา</div>'+imp+'</div>'
    +'</div>'
    +(r.coaching_focus?'<div style="background:rgba(55,138,221,.07);border:.5px solid rgba(55,138,221,.2);border-radius:10px;padding:13px 15px;margin-bottom:14px"><div style="font-size:10px;font-weight:600;color:#378ADD;text-transform:uppercase;letter-spacing:.1em;margin-bottom:5px">🎯 Coaching Focus</div><div style="font-size:13px;color:var(--t2);line-height:1.65">'+r.coaching_focus+'</div></div>':'')
    +'<div class="brow"><button class="btn" onclick="resetAll()">+ เคสใหม่</button>'
    +(S.history.length>1?'<button class="btn teal" onclick="switchTab(\'overview\')">ดูภาพรวม →</button>':'')
    +'</div>';
  document.getElementById('pane-result').innerHTML = html;
}

// ── Render overview ───────────────────────────────────────
function renderOverview() {
  var h=S.history, total=h.length;
  var green=h.filter(function(x){return x.result.overall_score>=75;}).length;
  var yellow=h.filter(function(x){return x.result.overall_score>=60&&x.result.overall_score<75;}).length;
  var red=h.filter(function(x){return x.result.overall_score<60;}).length;
  var byC={};
  h.forEach(function(x){ if(!byC[x.consultant]) byC[x.consultant]=[]; byC[x.consultant].push(x.result.overall_score); });

  var perf=Object.entries(byC).map(function(e){
    var name=e[0], scores=e[1];
    var avg=Math.round(scores.reduce(function(a,b){return a+b;},0)/scores.length);
    var z=zone(avg);
    return '<div style="display:flex;align-items:center;gap:10px;margin-bottom:9px">'
      +'<div style="width:55px;font-size:12px;font-weight:500;color:var(--t2);flex-shrink:0">'+name+'</div>'
      +'<div style="flex:1;height:7px;background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden"><div style="width:'+avg+'%;height:100%;background:'+z.c+';border-radius:3px"></div></div>'
      +'<div style="width:34px;font-size:13px;font-weight:600;color:'+z.c+';text-align:right;flex-shrink:0">'+avg+'</div>'
      +'<div style="font-size:14px;flex-shrink:0">'+zicon(avg)+'</div>'
      +'<div style="width:30px;font-size:10px;color:rgba(255,255,255,.25);text-align:right;flex-shrink:0">'+scores.length+'เคส</div>'
      +'</div>';
  }).join('');

  var act = (red?'<div style="font-size:13px;color:var(--t2);margin-bottom:4px">🔴 '+red+' เคส → Supervisor ดำเนินการทันที</div>':'')
    + (yellow?'<div style="font-size:13px;color:var(--t2)">🟡 '+yellow+' เคส → Coach ภายใน 3 วัน</div>':'')
    + (!red&&!yellow?'<div style="font-size:13px;color:#5DCAA5">✓ ทุกเคสผ่านมาตรฐาน</div>':'');

  document.getElementById('pane-overview').innerHTML =
    '<div style="font-size:15px;font-weight:500;margin-bottom:3px">Overview Report</div>'
    +'<div style="font-size:11px;color:var(--t3);margin-bottom:14px">'+total+' เคส</div>'
    +'<div class="sg4">'
    +[{l:'ทั้งหมด',v:total,c:'#fff'},{l:'🟢 ผ่าน',v:green,c:'#5DCAA5'},{l:'🟡 Coach',v:yellow,c:'#EF9F27'},{l:'🔴 Critical',v:red,c:'#E24B4A'}].map(function(s){
      return '<div class="sbox"><div class="sn" style="color:'+s.c+'">'+s.v+'</div><div class="sl2">'+s.l+'</div></div>';
    }).join('')+'</div>'
    +'<div class="card" style="margin-bottom:12px"><div class="ct" style="color:var(--t3)">Performance รายบุคคล</div>'+perf+'</div>'
    +'<div style="background:rgba(226,75,74,.06);border:.5px solid rgba(226,75,74,.18);border-radius:10px;padding:13px 15px">'
    +'<div style="font-size:10px;font-weight:600;color:#E24B4A;text-transform:uppercase;letter-spacing:.1em;margin-bottom:7px">🚨 Action Required</div>'+act+'</div>';
}

// ── Render history ────────────────────────────────────────
function renderHistory() {
  var html='<div style="font-size:15px;font-weight:500;margin-bottom:3px">ประวัติการวิเคราะห์</div>'
    +'<div style="font-size:11px;color:var(--t3);margin-bottom:14px">'+S.history.length+' เคส</div>';
  S.history.forEach(function(item,i) {
    var z=zone(item.result.overall_score), flags=item.result.red_flags||[];
    html+='<div class="hi-item" data-idx="'+i+'">'
      +'<span style="font-size:16px">'+zicon(item.result.overall_score)+'</span>'
      +'<div style="flex:1;min-width:0"><div style="font-size:12px;font-weight:500;color:var(--t2);overflow:hidden;text-overflow:ellipsis;white-space:nowrap">'+item.consultant+' · '+item.date+'</div>'
      +'<div style="font-size:10px;color:var(--t3)">'+item.file+(flags.length?' · ⚠ '+flags.length+' red flag':' · ไม่มี red flag')+'</div></div>'
      +'<div style="text-align:right;flex-shrink:0"><div style="font-size:14px;font-weight:600;color:'+z.c+'">'+item.result.overall_score+'</div><div style="font-size:9px;color:'+z.c+'">'+z.lbl+'</div></div>'
      +'</div>';
  });
  document.getElementById('pane-history').innerHTML = html;
  document.querySelectorAll('.hi-item').forEach(function(el) {
    el.addEventListener('click', function() {
      var idx = parseInt(this.getAttribute('data-idx'));
      renderResult(S.history[idx]);
      switchTab('result');
    });
  });
}
</script>
</body>
</html>
