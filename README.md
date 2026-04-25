<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Inza Iqbal — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #f5f5f7;
    --surface: #ffffff;
    --surface2: #f0f0f5;
    --border: rgba(0,0,0,0.07);
    --border2: rgba(0,0,0,0.11);
    --text: #111114;
    --muted: #7a7a8a;
    --accent: #5a50e0;
    --accent2: #1a9e6e;
    --accent3: #e07a2f;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Sora', sans-serif;
    font-size: 15px;
    line-height: 1.6;
    min-height: 100vh;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(90,80,224,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(90,80,224,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .page { max-width: 760px; margin: 0 auto; padding: 48px 24px 80px; position: relative; z-index: 1; }

  /* HERO */
  .hero {
    background: var(--surface);
    border: 1px solid var(--border2);
    border-radius: 20px;
    padding: 28px;
    margin-bottom: 16px;
    animation: fadeUp 0.5s ease both;
  }

  .hero-top { display: flex; align-items: flex-start; gap: 16px; margin-bottom: 20px; }

  .avatar {
    width: 58px; height: 58px; border-radius: 50%;
    background: linear-gradient(135deg, #7c6ff7, #4fd1a5);
    display: flex; align-items: center; justify-content: center;
    font-size: 20px; font-weight: 700; color: #fff; flex-shrink: 0;
    letter-spacing: -0.5px;
  }

  .hero-info { flex: 1; }

  .hero-name {
    font-size: 22px; font-weight: 700; letter-spacing: -0.5px;
    display: flex; align-items: center; gap: 10px; flex-wrap: wrap;
    margin-bottom: 5px;
  }

  .badge-green {
    font-size: 11px; font-weight: 600; padding: 3px 10px;
    background: rgba(26,158,110,0.12); color: var(--accent2);
    border: 1px solid rgba(26,158,110,0.3); border-radius: 20px;
  }

  .hero-tagline { font-size: 13px; color: var(--muted); line-height: 1.5; margin-bottom: 10px; }

  .hero-meta { display: flex; flex-wrap: wrap; gap: 14px; font-size: 12px; color: var(--muted); }
  .hero-meta a { color: var(--accent); text-decoration: none; }
  .hero-meta a:hover { text-decoration: underline; }
  .hero-meta .loc::before { content: '📍 '; }

  .stat-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; }

  .stat-box {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 14px 16px;
    text-align: center;
  }

  .stat-icon { font-size: 20px; margin-bottom: 4px; }
  .stat-label { font-size: 14px; font-weight: 600; color: var(--text); }
  .stat-sub { font-size: 11px; color: var(--muted); margin-top: 2px; }

  /* SECTIONS */
  .section { margin-bottom: 16px; animation: fadeUp 0.5s ease both; }
  .section:nth-child(2) { animation-delay: 0.07s; }
  .section:nth-child(3) { animation-delay: 0.14s; }
  .section:nth-child(4) { animation-delay: 0.21s; }
  .section:nth-child(5) { animation-delay: 0.28s; }
  .section:nth-child(6) { animation-delay: 0.35s; }
  .section:nth-child(7) { animation-delay: 0.42s; }
  .section:nth-child(8) { animation-delay: 0.49s; }

  .section-label {
    font-size: 10px; font-weight: 600; letter-spacing: 0.12em;
    color: var(--muted); text-transform: uppercase; margin-bottom: 10px;
    padding-left: 2px;
  }

  .card {
    background: var(--surface);
    border: 1px solid var(--border2);
    border-radius: 16px;
    padding: 20px 24px;
  }

  /* ABOUT */
  .about-text { font-size: 14px; color: #444455; line-height: 1.8; }
  .about-text strong { color: var(--text); font-weight: 600; }

  /* PROJECTS */
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }

  .repo-card {
    background: var(--surface);
    border: 1px solid var(--border2);
    border-radius: 14px;
    padding: 16px 18px;
    transition: border-color 0.2s, transform 0.2s;
    text-decoration: none;
    display: block;
  }

  .repo-card:hover { border-color: var(--accent); transform: translateY(-2px); }

  .repo-name {
    font-size: 14px; font-weight: 600; color: var(--accent);
    margin-bottom: 6px; font-family: 'JetBrains Mono', monospace;
  }

  .repo-desc { font-size: 12px; color: var(--muted); line-height: 1.55; margin-bottom: 12px; }

  .tag-row { display: flex; flex-wrap: wrap; gap: 5px; margin-bottom: 10px; }

  .tag {
    font-size: 11px; padding: 2px 9px; border-radius: 20px;
    font-weight: 500; border: 1px solid;
  }
  .tag-purple { background: rgba(90,80,224,0.08); color: #4a40c0; border-color: rgba(90,80,224,0.2); }
  .tag-teal   { background: rgba(26,158,110,0.08); color: #1a7a55; border-color: rgba(26,158,110,0.2); }
  .tag-orange { background: rgba(224,122,47,0.08); color: #b05a1a; border-color: rgba(224,122,47,0.2); }

  .repo-meta { display: flex; gap: 12px; font-size: 11px; color: var(--muted); align-items: center; }
  .lang-dot { width: 9px; height: 9px; border-radius: 50%; display: inline-block; margin-right: 4px; }

  /* TECH STACK */
  .stack-group { margin-bottom: 16px; }
  .stack-group:last-child { margin-bottom: 0; }
  .stack-group-label { font-size: 12px; font-weight: 500; color: var(--muted); margin-bottom: 8px; }

  .chips { display: flex; flex-wrap: wrap; gap: 7px; }

  .chip {
    display: inline-flex; align-items: center; gap: 6px;
    background: var(--surface2); border: 1px solid var(--border2);
    border-radius: 8px; padding: 6px 12px; font-size: 12px; font-weight: 500;
    color: #333344; transition: border-color 0.2s;
  }
  .chip-icon { font-size: 14px; }

  /* LANGUAGES */
  .lang-row { margin-bottom: 14px; }
  .lang-row:last-child { margin-bottom: 0; }
  .lang-top { display: flex; justify-content: space-between; font-size: 13px; margin-bottom: 6px; }
  .lang-name { font-weight: 500; }
  .lang-pct { color: var(--muted); font-family: 'JetBrains Mono', monospace; font-size: 12px; }
  .bar-track { background: var(--surface2); border-radius: 4px; height: 5px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 4px; transition: width 1s ease; }

  /* CONTRIBUTION */
  .contrib-note { font-size: 12px; color: var(--muted); margin-bottom: 12px; }
  .contrib-note span { color: var(--accent2); }
  #contrib-grid { display: flex; gap: 3px; }
  .contrib-col { display: flex; flex-direction: column; gap: 3px; }
  .contrib-cell { width: 12px; height: 12px; border-radius: 2px; }
  .contrib-legend { display: flex; align-items: center; gap: 5px; margin-top: 10px; font-size: 11px; color: var(--muted); }
  .legend-cell { width: 10px; height: 10px; border-radius: 2px; }

  /* GITHUB STATS */
  .stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; }

  .stat-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 12px;
    text-align: center;
  }

  .stat-card-icon { font-size: 24px; margin-bottom: 8px; }
  .stat-card-label { font-size: 13px; font-weight: 600; color: var(--text); }
  .stat-card-sub { font-size: 11px; color: var(--muted); margin-top: 3px; }

  /* CONNECT */
  .connect-row { display: flex; gap: 10px; flex-wrap: wrap; }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 20px; border-radius: 10px; font-size: 13px; font-weight: 600;
    text-decoration: none; transition: opacity 0.2s, transform 0.2s; border: 1px solid;
  }
  .connect-btn:hover { opacity: 0.85; transform: translateY(-1px); }
  .btn-linkedin { background: #0a66c2; border-color: #0a66c2; color: #fff; }
  .btn-gmail    { background: #ea4335; border-color: #ea4335; color: #fff; }
  .btn-github   { background: var(--surface2); border-color: var(--border2); color: var(--text); }

  /* QUOTE */
  .quote {
    text-align: center; font-size: 13px; color: var(--muted);
    font-style: italic; padding: 24px 0 0;
    font-family: 'JetBrains Mono', monospace;
  }

  /* WATERMARK */
  .readme-note {
    background: rgba(90,80,224,0.06);
    border: 1px dashed rgba(90,80,224,0.25);
    border-radius: 12px;
    padding: 12px 18px;
    font-size: 12px;
    color: var(--muted);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .readme-note strong { color: var(--accent); }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 520px) {
    .projects-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: repeat(3,1fr); }
  }
</style>
</head>
<body>
<div class="page">

  <!-- NOTE -->
  <div class="readme-note">
    <span style="font-size:18px;">📄</span>
    <span>This is a <strong>visual preview</strong> of your GitHub Profile README — same style as your portfolio. Copy the raw markdown from the <strong>README.md</strong> file included in this download.</span>
  </div>

  <!-- HERO -->
  <div class="hero">
    <div class="hero-top">
      <div class="avatar">II</div>
      <div class="hero-info">
        <div class="hero-name">
          Inza Iqbal
          <span class="badge-green">Open to work</span>
        </div>
        <div class="hero-tagline">
          Machine Learning Engineer · Building AI systems with Python, FastAPI & LLMs · Turning raw data into real-world AI solutions
        </div>
        <div class="hero-meta">
          <span class="loc">Pakistan</span>
          <a href="https://linkedin.com/in/inza-iqbal" target="_blank">linkedin.com/in/inza-iqbal</a>
          <a href="mailto:inzaiqbal54@gmail.com" target="_blank">inzaiqbal54@gmail.com</a>
        </div>
      </div>
    </div>
    <div class="stat-row">
      <div class="stat-box">
        <div class="stat-icon">🔥</div>
        <div class="stat-label">Active</div>
        <div class="stat-sub">Current streak</div>
      </div>
      <div class="stat-box">
        <div class="stat-icon">🧠</div>
        <div class="stat-label">ML / AI</div>
        <div class="stat-sub">Primary focus</div>
      </div>
      <div class="stat-box">
        <div class="stat-icon">⚡</div>
        <div class="stat-label">FastAPI</div>
        <div class="stat-sub">Currently building</div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-label">About</div>
    <div class="card">
      <p class="about-text">
        I'm a Machine Learning Engineer who builds AI systems that ship to production — not just notebooks.
        From <strong>LLM-powered scam detectors</strong> to <strong>multi-agent news pipelines</strong>,
        I work across the full ML stack: data → model → API → deployment.
        Currently deepening expertise in <strong>model optimization</strong> and <strong>MLOps</strong>.
        Actively looking to collaborate on impactful ML &amp; Deep Learning projects.
      </p>
    </div>
  </div>

  <!-- PINNED REPOS -->
  <div class="section">
    <div class="section-label">Pinned Repositories</div>
    <div class="projects-grid">

      <a class="repo-card" href="https://github.com/InzaIqbal/jobverify_ai" target="_blank">
        <div class="repo-name">jobverify_ai</div>
        <div class="repo-desc">AI job scam detector — trust score 0–100 using Groq LLaMA 3, keyword scanning & live website verification</div>
        <div class="tag-row">
          <span class="tag tag-purple">FastAPI</span>
          <span class="tag tag-teal">Groq LLaMA</span>
          <span class="tag tag-orange">Railway</span>
        </div>
        <div class="repo-meta">
          <span><span class="lang-dot" style="background:#3572A5;"></span>Python</span>
          <span>★ Stars</span>
        </div>
      </a>

      <a class="repo-card" href="https://github.com/InzaIqbal/Ai_news-agerator" target="_blank">
        <div class="repo-name">ai-news-aggregator</div>
        <div class="repo-desc">Multi-agent pipeline: scrapes AI blogs & YouTube, LLM summaries, ranked by interest, auto daily email digest</div>
        <div class="tag-row">
          <span class="tag tag-teal">PostgreSQL</span>
          <span class="tag tag-purple">OpenRouter</span>
        </div>
        <div class="repo-meta">
          <span><span class="lang-dot" style="background:#3572A5;"></span>Python</span>
          <span>★ 1</span>
        </div>
      </a>

      <a class="repo-card" href="https://github.com/InzaIqbal/Task_2Movie_Recommender" target="_blank">
        <div class="repo-name">movie-recommender</div>
        <div class="repo-desc">Content-based filtering on TMDB 5000 dataset using TF-IDF & cosine similarity with Streamlit interface</div>
        <div class="tag-row">
          <span class="tag tag-orange">Scikit-learn</span>
          <span class="tag tag-teal">Pandas</span>
        </div>
        <div class="repo-meta">
          <span><span class="lang-dot" style="background:#DA5B0B;"></span>Jupyter</span>
          <span>★ Stars</span>
        </div>
      </a>

      <a class="repo-card" href="https://github.com/InzaIqbal" target="_blank" style="border-style:dashed; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:6px; min-height:140px;">
        <div style="font-size:24px;">+</div>
        <div style="font-size:12px; color:var(--muted);">More on GitHub</div>
      </a>

    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-label">Core Tech Stack</div>
    <div class="card">
      <div class="stack-group">
        <div class="stack-group-label">ML / AI</div>
        <div class="chips">
          <span class="chip"><span class="chip-icon">🐍</span>Python</span>
          <span class="chip"><span class="chip-icon">🔥</span>PyTorch</span>
          <span class="chip"><span class="chip-icon">🧠</span>TensorFlow</span>
          <span class="chip"><span class="chip-icon">🤗</span>HuggingFace</span>
          <span class="chip"><span class="chip-icon">📊</span>Scikit-learn</span>
          <span class="chip"><span class="chip-icon">🐼</span>Pandas</span>
          <span class="chip"><span class="chip-icon">🔢</span>NumPy</span>
        </div>
      </div>
      <div class="stack-group" style="margin-top:16px;">
        <div class="stack-group-label">Deployment &amp; Infra</div>
        <div class="chips">
          <span class="chip"><span class="chip-icon">⚡</span>FastAPI</span>
          <span class="chip"><span class="chip-icon">🐳</span>Docker</span>
          <span class="chip"><span class="chip-icon">🗄️</span>PostgreSQL</span>
          <span class="chip"><span class="chip-icon">📮</span>Redis</span>
          <span class="chip"><span class="chip-icon">🔧</span>Git</span>
          <span class="chip"><span class="chip-icon">🧪</span>Postman</span>
        </div>
      </div>
      <div class="stack-group" style="margin-top:16px;">
        <div class="stack-group-label">Also familiar with</div>
        <div class="chips">
          <span class="chip"><span class="chip-icon">⚛️</span>React</span>
          <span class="chip"><span class="chip-icon">📘</span>TypeScript</span>
          <span class="chip"><span class="chip-icon">📱</span>Flutter</span>
          <span class="chip"><span class="chip-icon">🍃</span>MongoDB</span>
          <span class="chip"><span class="chip-icon">🔥</span>Firebase</span>
        </div>
      </div>
    </div>
  </div>

  <!-- TOP LANGUAGES -->
  <div class="section">
    <div class="section-label">Top Languages</div>
    <div class="card">
      <div class="lang-row">
        <div class="lang-top"><span class="lang-name">Python</span><span class="lang-pct">75%</span></div>
        <div class="bar-track"><div class="bar-fill" id="bar1" style="width:0%;background:#3572A5;"></div></div>
      </div>
      <div class="lang-row">
        <div class="lang-top"><span class="lang-name">Jupyter Notebook</span><span class="lang-pct">12%</span></div>
        <div class="bar-track"><div class="bar-fill" id="bar2" style="width:0%;background:#DA5B0B;"></div></div>
      </div>
      <div class="lang-row">
        <div class="lang-top"><span class="lang-name">JavaScript / TypeScript</span><span class="lang-pct">8%</span></div>
        <div class="bar-track"><div class="bar-fill" id="bar3" style="width:0%;background:#e4c84b;"></div></div>
      </div>
      <div class="lang-row">
        <div class="lang-top"><span class="lang-name">Other</span><span class="lang-pct">5%</span></div>
        <div class="bar-track"><div class="bar-fill" id="bar4" style="width:0%;background:#7a7a8a;"></div></div>
      </div>
    </div>
  </div>

  <!-- CONTRIBUTION -->
  <div class="section">
    <div class="section-label">Contribution Activity</div>
    <div class="card">
      <div class="contrib-note">Consistent commits = consistent dedication <span>🟩</span></div>
      <div id="contrib-grid"></div>
      <div class="contrib-legend">
        <span>Less</span>
        <div class="legend-cell" style="background:#e8e8ee;border:1px solid #ccc;"></div>
        <div class="legend-cell" style="background:#1a4d2e;"></div>
        <div class="legend-cell" style="background:#2d7a4f;"></div>
        <div class="legend-cell" style="background:#40c463;"></div>
        <div class="legend-cell" style="background:#7ae89e;"></div>
        <span>More</span>
      </div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-label">GitHub Stats</div>
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-card-icon">⭐</div>
        <div class="stat-card-label">Stars earned</div>
        <div class="stat-card-sub">On public repos</div>
      </div>
      <div class="stat-card">
        <div class="stat-card-icon">🔀</div>
        <div class="stat-card-label">Total commits</div>
        <div class="stat-card-sub">This year</div>
      </div>
      <div class="stat-card">
        <div class="stat-card-icon">🔁</div>
        <div class="stat-card-label">Pull requests</div>
        <div class="stat-card-sub">Merged</div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-label">Connect</div>
    <div class="card">
      <div class="connect-row">
        <a href="https://linkedin.com/in/inza-iqbal" target="_blank" class="connect-btn btn-linkedin">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
        <a href="mailto:inzaiqbal54@gmail.com" class="connect-btn btn-gmail">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 010 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
          Gmail
        </a>
        <a href="https://github.com/InzaIqbal" target="_blank" class="connect-btn btn-github">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
          GitHub
        </a>
      </div>
    </div>
  </div>

  <div class="quote">"I don't just train models — I ship AI products that work in the real world."</div>

</div>
<script>
  setTimeout(() => {
    document.getElementById('bar1').style.width = '75%';
    document.getElementById('bar2').style.width = '12%';
    document.getElementById('bar3').style.width = '8%';
    document.getElementById('bar4').style.width = '5%';
  }, 300);

  const grid = document.getElementById('contrib-grid');
  const colors = ['#e8e8ee','#9be9a8','#40c463','#30a14e','#216e39'];
  const weeks = 22;
  for (let w = 0; w < weeks; w++) {
    const col = document.createElement('div');
    col.className = 'contrib-col';
    for (let d = 0; d < 7; d++) {
      const cell = document.createElement('div');
      cell.className = 'contrib-cell';
      const r = Math.random();
      const ci = r < 0.30 ? 0 : r < 0.50 ? 1 : r < 0.68 ? 2 : r < 0.84 ? 3 : 4;
      cell.style.background = colors[ci];
      col.appendChild(cell);
    }
    grid.appendChild(col);
  }
</script>
</body>
</html>
