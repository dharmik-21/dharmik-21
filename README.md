<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>dharmik-21 · README</title>
<style>
  :root{
    --bg-page:#0d1117;
    --bg-card:#161b22;
    --bg-card-hover:#1c2128;
    --border:#30363d;
    --text-primary:#e6edf3;
    --text-secondary:#7d8590;
    --text-muted:#57606a;
    --green-0:#161b22;
    --green-1:#0e4429;
    --green-2:#006d32;
    --green-3:#26a641;
    --green-4:#39d353;
    --font: -apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--bg-page);
    color:var(--text-primary);
    font-family:var(--font);
    -webkit-font-smoothing:antialiased;
  }
  .wrap{
    max-width:882px;
    margin:0 auto;
    padding:40px 16px 64px;
  }
  .page-head{
    display:flex;
    align-items:center;
    gap:14px;
    margin-bottom:24px;
  }
  .page-head .mono-avatar{
    width:44px;height:44px;border-radius:50%;
    background:linear-gradient(135deg,#1f6feb,#39d353);
    display:flex;align-items:center;justify-content:center;
    font-weight:700;font-size:15px;color:#0d1117;
    flex-shrink:0;
  }
  .page-head h1{font-size:20px;margin:0;font-weight:600;}
  .page-head .handle{color:var(--text-secondary);font-size:14px;font-weight:400;margin-left:6px;}
  .page-head .role{color:var(--text-secondary);font-size:13px;margin-top:2px;}

  .row{display:grid;gap:16px;margin-bottom:16px;}
  .row1, .row2{grid-template-columns:264px 1fr;}
  .row3{grid-template-columns:1fr 264px;}

  .card{
    background:var(--bg-card);
    border:1px solid var(--border);
    border-radius:12px;
    padding:24px;
  }
  .card.flush{padding:0;overflow:hidden;}

  /* ---- Avatar / photo card ---- */
  .avatar-card{
    aspect-ratio:1/1;
    position:relative;
    background:
      radial-gradient(circle at 30% 20%, rgba(57,211,83,0.18), transparent 45%),
      linear-gradient(155deg,#0b3d91 0%, #0d1117 55%, #062617 100%);
    display:flex;align-items:center;justify-content:center;
    overflow:hidden;
  }
  .avatar-card svg.circuit{position:absolute;inset:0;width:100%;height:100%;opacity:0.35;}
  .avatar-card .initials{
    font-size:78px;
    font-weight:800;
    letter-spacing:-2px;
    background:linear-gradient(135deg,#58a6ff,#39d353);
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
    z-index:1;
    font-family:var(--font);
  }
  .avatar-card .tag{
    position:absolute;
    bottom:14px;left:14px;right:14px;
    font-size:11px;
    color:#c9d1d9;
    background:rgba(13,17,23,0.55);
    border:1px solid rgba(255,255,255,0.08);
    padding:5px 8px;
    border-radius:6px;
    text-align:center;
    letter-spacing:0.3px;
    z-index:1;
  }

  /* ---- Bio card ---- */
  .breadcrumb{
    display:flex;align-items:center;gap:6px;
    color:var(--text-secondary);
    font-size:13px;margin-bottom:14px;
  }
  .bio-card h2{font-size:22px;margin:0 0 14px;font-weight:600;}
  .bio-card p{
    color:#c9d1d9;
    font-size:14px;
    line-height:1.65;
    margin:0 0 14px;
  }
  .bio-card p:last-child{margin-bottom:0;}
  .bio-card a{color:#c9d1d9;text-decoration:underline;text-underline-offset:2px;}
  .bio-card a:hover{color:#58a6ff;}

  /* ---- Badge rows (achievements) ---- */
  .badge-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
  }
  .badge-item{position:relative;display:flex;justify-content:center;cursor:default;}
  .badge-circle{
    width:52px;height:52px;border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    font-size:24px;
    border:2px solid rgba(255,255,255,0.06);
  }
  .badge-mult{
    position:absolute;bottom:-4px;right:8px;
    background:#21262d;border:1px solid var(--border);
    color:var(--text-secondary);
    font-size:10px;font-weight:600;
    padding:1px 5px;border-radius:8px;
  }
  .card-heading-row{
    display:flex;align-items:center;justify-content:space-between;
    margin-bottom:18px;
  }
  .card-heading-row h3{font-size:15px;margin:0;font-weight:600;}
  .beta-row{
    display:flex;align-items:center;gap:10px;
    margin-top:18px;
  }
  .beta-tag{
    font-size:10px;font-weight:600;color:var(--text-secondary);
    border:1px solid var(--border);padding:1px 7px;border-radius:10px;
  }
  .feedback-link{font-size:12px;color:var(--text-secondary);text-decoration:underline;}

  /* ---- Contributions card ---- */
  .contrib-head{
    display:flex;align-items:center;justify-content:space-between;
    margin-bottom:18px;flex-wrap:wrap;gap:10px;
  }
  .contrib-head h3{font-size:16px;margin:0;font-weight:600;}
  select.year-select{
    background:#21262d;color:var(--text-primary);
    border:1px solid var(--border);border-radius:6px;
    font-size:13px;padding:5px 10px;font-family:var(--font);
    cursor:pointer;
  }
  .month-labels{
    display:grid;
    grid-auto-flow:column;
    font-size:11px;color:var(--text-secondary);
    margin-bottom:6px;
    padding-left:2px;
  }
  .heatmap-scroll{overflow-x:auto;}
  .heatmap{
    display:grid;
    grid-template-rows:repeat(7,11px);
    grid-auto-flow:column;
    grid-auto-columns:11px;
    gap:3px;
  }
  .cell{width:11px;height:11px;border-radius:2px;background:var(--green-0);}

  /* ---- Repos ---- */
  .repo-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:16px;
  }
  .repo-card{
    border:1px solid var(--border);
    border-radius:10px;
    padding:16px;
    background:#0d1117;
  }
  .repo-top{display:flex;align-items:center;gap:8px;flex-wrap:wrap;}
  .repo-name{font-size:14px;font-weight:600;color:#58a6ff;text-decoration:none;}
  .repo-name:hover{text-decoration:underline;}
  .pill{
    font-size:11px;color:var(--text-secondary);
    border:1px solid var(--border);
    padding:1px 8px;border-radius:12px;
  }
  .repo-desc{
    font-size:12px;color:var(--text-secondary);
    margin:10px 0 14px;line-height:1.5;
    min-height:52px;
  }
  .repo-foot{display:flex;align-items:center;gap:14px;font-size:12px;color:var(--text-secondary);flex-wrap:wrap;}
  .lang-dot{width:10px;height:10px;border-radius:50%;display:inline-block;margin-right:4px;vertical-align:-1px;}
  .stat{display:inline-flex;align-items:center;gap:4px;}

  svg.icon{width:14px;height:14px;fill:var(--text-secondary);}

  @media (max-width:720px){
    .row1,.row2,.row3{grid-template-columns:1fr;}
    .row3{display:flex;flex-direction:column;}
    .repo-grid{grid-template-columns:1fr;}
    .badge-grid{grid-template-columns:repeat(4,1fr);}
  }
</style>
</head>
<body>
<div class="wrap">

  <div class="page-head">
    <div class="mono-avatar">DB</div>
    <div>
      <h1>Dharmik Barot<span class="handle">@dharmik-21</span></h1>
      <div class="role">AI/ML Engineer · Bangalore, India</div>
    </div>
  </div>

  <!-- ROW 1: Photo + Howdy bio -->
  <div class="row row1">
    <div class="card flush avatar-card">
      <svg class="circuit" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
        <g stroke="#39d353" stroke-width="1" fill="none">
          <path d="M10 40 H70 V90 H140 V150"/>
          <path d="M190 30 H130 V70 H60 V120 H10"/>
          <path d="M20 180 H90 V130 H160 V60"/>
        </g>
        <g fill="#39d353">
          <circle cx="70" cy="90" r="3"/>
          <circle cx="140" cy="150" r="3"/>
          <circle cx="130" cy="70" r="3"/>
          <circle cx="60" cy="120" r="3"/>
          <circle cx="90" cy="130" r="3"/>
          <circle cx="160" cy="60" r="3"/>
        </g>
      </svg>
      <div class="initials">DB</div>
      <div class="tag">AI/ML Engineer · Building intelligent systems</div>
    </div>

    <div class="card bio-card">
      <div class="breadcrumb">
        <svg class="icon" viewBox="0 0 16 16"><path d="M0 1.75A1.75 1.75 0 0 1 1.75 0h8.5A1.75 1.75 0 0 1 12 1.75v12.5a.75.75 0 0 1-1.2.6l-3.3-2.475-3.3 2.475a.75.75 0 0 1-1.2-.6V1.75Z"/></svg>
        dharmik-21 / README.md
      </div>
      <h2>Howdy!</h2>
      <p>
        I'm an <strong>AI/ML Engineer</strong> and MCA (AI &amp; ML) student at Jain University, specializing in
        Large Language Models, Agentic AI, and Computer Vision. Right now I'm building
        <a href="#cortex-lens">CortexLens</a>, wearable smart glasses that give real-time spatial
        awareness to the visually impaired. I build with TensorFlow, PyTorch, LangChain, Hugging Face
        Transformers, and the OpenAI API — turning research ideas into working, data-driven products.
      </p>
      <p>
        I've also shipped <a href="#hisab-ai">HisabAI</a>, an invoice-processing &amp; financial
        analytics tool, <a href="#cyclonevision">CycloneVisionAI</a>, a satellite-based cyclone
        detector, and an <a href="#blog-generator">AI Blog Generator</a> built on LangChain. Along with
        deep learning, I'm comfortable across the <a href="https://github.com/dharmik-21" target="_blank" rel="noopener">MERN stack</a>
        (MongoDB, Express, React, Node.js) and FastAPI, so I can take a model from notebook to a real,
        usable app. Find me on <a href="https://linkedin.com/in/barot-dharmik2105" target="_blank" rel="noopener">LinkedIn</a>
        or check out my code on <a href="https://github.com/dharmik-21" target="_blank" rel="noopener">GitHub</a>.
      </p>
    </div>
  </div>

  <!-- ROW 2: Skill badges + contributions -->
  <div class="row row2">
    <div class="card">
      <div class="card-heading-row"><h3>Achievements</h3></div>
      <div class="badge-grid">
        <div class="badge-item" title="Python"><div class="badge-circle" style="background:linear-gradient(135deg,#3572A5,#0d1117)">🐍</div></div>
        <div class="badge-item" title="Deep Learning — TensorFlow &amp; PyTorch"><div class="badge-circle" style="background:linear-gradient(135deg,#ee6f57,#7a2c1d)">🔥</div></div>
        <div class="badge-item" title="LLMs &amp; Agentic AI"><div class="badge-circle" style="background:linear-gradient(135deg,#8957e5,#3d1f7a)">🤖</div></div>
        <div class="badge-item" title="Computer Vision"><div class="badge-circle" style="background:linear-gradient(135deg,#39d353,#0e4429)">👁️</div></div>
        <div class="badge-item" title="Natural Language Processing"><div class="badge-circle" style="background:linear-gradient(135deg,#58a6ff,#0d3a6b)">💬</div></div>
        <div class="badge-item" title="Full-Stack — MERN"><div class="badge-circle" style="background:linear-gradient(135deg,#26a641,#0b5)">🌐</div></div>
        <div class="badge-item" title="Docker"><div class="badge-circle" style="background:linear-gradient(135deg,#2496ed,#0b3d91)">🐳</div></div>
        <div class="badge-item" title="Data Analytics — Pandas &amp; Plotly"><div class="badge-circle" style="background:linear-gradient(135deg,#f2b807,#7a5c00)">📊</div></div>
      </div>
      <div class="beta-row">
        <span class="beta-tag">Beta</span>
        <a class="feedback-link" href="#">Send feedback</a>
      </div>
    </div>

    <div class="card">
      <div class="contrib-head">
        <h3 id="contribCount">684 contributions in the last year</h3>
        <select class="year-select" id="yearSelect">
          <option value="2026" selected>2026</option>
          <option value="2025">2025</option>
          <option value="2024">2024</option>
        </select>
      </div>
      <div class="month-labels" id="monthLabels"></div>
      <div class="heatmap-scroll">
        <div class="heatmap" id="heatmap"></div>
      </div>
    </div>
  </div>

  <!-- ROW 3: Popular repositories + Achievements sidebar -->
  <div class="row row3">
    <div class="card">
      <div class="card-heading-row"><h3>Popular repositories</h3><span style="color:var(--text-secondary);font-size:12px;">▾</span></div>
      <div class="repo-grid">

        <div class="repo-card" id="cortex-lens">
          <div class="repo-top">
            <svg class="icon" viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 1 1 0-1.5h1.75v-2H4.5a1 1 0 0 0-.6 1.8.75.75 0 0 1-.9 1.2A2.5 2.5 0 0 1 2 11.5v-9Z"/></svg>
            <a class="repo-name" href="#">CortexLens</a>
            <span class="pill">Public</span>
          </div>
          <p class="repo-desc">AI-powered assistive smart glasses that give real-time audio awareness of surroundings and obstacles to the visually impaired.</p>
          <div class="repo-foot">
            <span><span class="lang-dot" style="background:#3572A5"></span>Python</span>
            <span class="stat">⭐ 21</span>
            <span class="stat">🍴 4</span>
          </div>
        </div>

        <div class="repo-card" id="hisab-ai">
          <div class="repo-top">
            <svg class="icon" viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 1 1 0-1.5h1.75v-2H4.5a1 1 0 0 0-.6 1.8.75.75 0 0 1-.9 1.2A2.5 2.5 0 0 1 2 11.5v-9Z"/></svg>
            <a class="repo-name" href="#">HisabAI</a>
            <span class="pill">Public</span>
          </div>
          <p class="repo-desc">Streamlit invoice management system — OCR extraction, NLP structuring of GST data, and a real-time Pandas + Plotly analytics dashboard.</p>
          <div class="repo-foot">
            <span><span class="lang-dot" style="background:#3572A5"></span>Python</span>
            <span class="stat">⭐ 15</span>
            <span class="stat">🍴 2</span>
          </div>
        </div>

        <div class="repo-card" id="cyclonevision">
          <div class="repo-top">
            <svg class="icon" viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 1 1 0-1.5h1.75v-2H4.5a1 1 0 0 0-.6 1.8.75.75 0 0 1-.9 1.2A2.5 2.5 0 0 1 2 11.5v-9Z"/></svg>
            <a class="repo-name" href="#">CycloneVisionAI</a>
            <span class="pill">Public</span>
          </div>
          <p class="repo-desc">One-class autoencoder cyclone detector for satellite imagery, with CNN encoder-decoder anomaly scoring and center localization.</p>
          <div class="repo-foot">
            <span><span class="lang-dot" style="background:#3572A5"></span>Python</span>
            <span class="stat">⭐ 12</span>
            <span class="stat">🍴 1</span>
          </div>
        </div>

        <div class="repo-card" id="blog-generator">
          <div class="repo-top">
            <svg class="icon" viewBox="0 0 16 16"><path d="M2 2.5A2.5 2.5 0 0 1 4.5 0h8.75a.75.75 0 0 1 .75.75v12.5a.75.75 0 0 1-.75.75h-2.5a.75.75 0 1 1 0-1.5h1.75v-2H4.5a1 1 0 0 0-.6 1.8.75.75 0 0 1-.9 1.2A2.5 2.5 0 0 1 2 11.5v-9Z"/></svg>
            <a class="repo-name" href="#">AI-Blog-Generator</a>
            <span class="pill">Public</span>
          </div>
          <p class="repo-desc">LangChain-orchestrated blog writing tool that customizes tone and structure from a topic, served through a Streamlit UI.</p>
          <div class="repo-foot">
            <span><span class="lang-dot" style="background:#3572A5"></span>Python</span>
            <span class="stat">⭐ 9</span>
            <span class="stat">🍴 1</span>
          </div>
        </div>

      </div>
    </div>

    <div class="card">
      <div class="card-heading-row"><h3>8 Achievements</h3></div>
      <div class="badge-grid">
        <div class="badge-item" title="Microsoft Career Essentials in Generative AI"><div class="badge-circle" style="background:linear-gradient(135deg,#00a4ef,#003a6b)">🧠</div></div>
        <div class="badge-item" title="NVIDIA Hackathon &amp; OneEarth International Hackathon 2025"><div class="badge-circle" style="background:linear-gradient(135deg,#f2b807,#7a5c00)">🏆</div><span class="badge-mult">2x</span></div>
        <div class="badge-item" title="NVIDIA CUDA — Python, C, C++"><div class="badge-circle" style="background:linear-gradient(135deg,#76b900,#2e4a00)">⚡</div></div>
        <div class="badge-item" title="AI/ML for Geodata Analysis — IIRS, ISRO"><div class="badge-circle" style="background:linear-gradient(135deg,#1f6feb,#0d1a33)">🛰️</div></div>
        <div class="badge-item" title="1 Million Prompters — Dubai.AI"><div class="badge-circle" style="background:linear-gradient(135deg,#e05fc4,#5c1a4d)">💬</div></div>
        <div class="badge-item" title="LangChain &amp; RAG"><div class="badge-circle" style="background:linear-gradient(135deg,#8957e5,#3d1f7a)">🔗</div></div>
        <div class="badge-item" title="Published Research — Multimodal AI"><div class="badge-circle" style="background:linear-gradient(135deg,#39d353,#0e4429)">📄</div></div>
        <div class="badge-item" title="MERN Stack Development"><div class="badge-circle" style="background:linear-gradient(135deg,#26a641,#0b5)">🌐</div></div>
      </div>
      <div class="beta-row">
        <span class="beta-tag">Beta</span>
        <a class="feedback-link" href="#">Send feedback</a>
      </div>
    </div>
  </div>

</div>

<script>
  // ---- Contribution heatmap ----
  const heatmap = document.getElementById('heatmap');
  const monthLabels = document.getElementById('monthLabels');
  const yearSelect = document.getElementById('yearSelect');
  const contribCount = document.getElementById('contribCount');

  const yearData = {
    '2026': { total: 684, months: ['Aug','Sep','Oct','Nov','Dec','Jan','Feb','Mar','Apr','May','Jun','Jul'],
      weight: {8:2,9:2,10:4,11:4,12:2,1:2,2:2,3:5,4:5,5:4,6:4,7:4} },
    '2025': { total: 512, months: ['Aug','Sep','Oct','Nov','Dec','Jan','Feb','Mar','Apr','May','Jun','Jul'],
      weight: {8:1,9:2,10:3,11:3,12:2,1:2,2:2,3:2,4:2,5:2,6:2,7:2} },
    '2024': { total: 298, months: ['Aug','Sep','Oct','Nov','Dec','Jan','Feb','Mar','Apr','May','Jun','Jul'],
      weight: {8:2,9:2,10:1,11:3,12:3,1:1,2:1,3:1,4:1,5:1,6:1,7:1} }
  };

  function buildHeatmap(year){
    heatmap.innerHTML = '';
    monthLabels.innerHTML = '';
    const data = yearData[year];
    const totalWeeks = 52;
    const monthCount = data.months.length;
    data.months.forEach(m=>{
      const label = document.createElement('span');
      label.textContent = m;
      label.style.gridColumn = 'span ' + Math.round(totalWeeks/monthCount);
      monthLabels.appendChild(label);
    });

    for(let week=0; week<totalWeeks; week++){
      const monthIdx = Math.min(monthCount-1, Math.floor(week/(totalWeeks/monthCount)));
      const monthNum = [8,9,10,11,12,1,2,3,4,5,6,7][monthIdx];
      const w = data.weight[monthNum] || 1;
      for(let day=0; day<7; day++){
        const cell = document.createElement('div');
        cell.className = 'cell';
        const r = Math.random() * w;
        let color = 'var(--green-0)';
        if(r > 3.2) color = 'var(--green-4)';
        else if(r > 2.2) color = 'var(--green-3)';
        else if(r > 1.2) color = 'var(--green-2)';
        else if(r > 0.55) color = 'var(--green-1)';
        cell.style.background = color;
        heatmap.appendChild(cell);
      }
    }
    contribCount.textContent = data.total + ' contributions in the last year';
  }

  buildHeatmap('2026');
  yearSelect.addEventListener('change', (e)=> buildHeatmap(e.target.value));
</script>
</body>
</html>
