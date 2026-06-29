<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>README Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Inter:wght@300;400;500;600;700;800&display=swap');

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:        #0d1117;
    --surface:   #161b22;
    --surface2:  #1c2230;
    --border:    #30363d;
    --text:      #c9d1d9;
    --muted:     #8b949e;
    --blue:      #58a6ff;
    --cyan:      #39d0d8;
    --green:     #3fb950;
    --purple:    #bc8cff;
    --orange:    #f78166;
    --yellow:    #e3b341;
    --pink:      #f778ba;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    line-height: 1.6;
    min-height: 100vh;
    padding: 32px 16px;
  }

  .wrapper {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 28px;
  }

  /* ── SECTION CARD ── */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 28px;
  }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 24px;
    align-items: start;
  }
  .hero-left {}
  .greeting { font-size: 15px; color: var(--muted); margin-bottom: 4px; }
  .hero-name {
    font-size: 52px;
    font-weight: 800;
    background: linear-gradient(90deg, var(--blue) 0%, var(--purple) 50%, var(--cyan) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.1;
    margin-bottom: 6px;
  }
  .hero-title { font-size: 15px; color: var(--muted); font-weight: 500; margin-bottom: 14px; }
  .hero-bio { font-size: 14px; color: var(--text); margin-bottom: 18px; line-height: 1.7; }
  .hero-bio span.fast   { color: var(--orange); }
  .hero-bio span.scale  { color: var(--blue);   }
  .hero-bio span.modern { color: var(--cyan);   }

  .links { display: flex; gap: 20px; flex-wrap: wrap; margin-bottom: 18px; }
  .links a {
    color: var(--muted);
    text-decoration: none;
    font-size: 13px;
    display: flex;
    align-items: center;
    gap: 5px;
    transition: color .2s;
  }
  .links a:hover { color: var(--blue); }

  .tags { display: flex; gap: 8px; flex-wrap: wrap; }
  .tag {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: .05em;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid;
  }
  .tag-blue   { border-color: var(--blue);   color: var(--blue);   background: rgba(88,166,255,.08); }
  .tag-purple { border-color: var(--purple); color: var(--purple); background: rgba(188,140,255,.08); }
  .tag-cyan   { border-color: var(--cyan);   color: var(--cyan);   background: rgba(57,208,216,.08); }
  .tag-green  { border-color: var(--green);  color: var(--green);  background: rgba(63,185,80,.08); }
  .tag-orange { border-color: var(--orange); color: var(--orange); background: rgba(247,129,102,.08); }

  /* profile card */
  .profile-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    min-width: 210px;
    text-align: center;
  }
  .status-dot { display: flex; align-items: center; justify-content: flex-end; gap: 6px; font-size: 12px; color: var(--green); margin-bottom: 10px; }
  .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--green); }
  .avatar-wrap {
    width: 80px; height: 80px;
    margin: 0 auto 14px;
    border-radius: 50%;
    padding: 3px;
    background: linear-gradient(135deg, var(--blue), var(--purple), var(--cyan));
  }
  .avatar-wrap img, .avatar-placeholder {
    width: 100%; height: 100%;
    border-radius: 50%;
    object-fit: cover;
    background: #2a2060;
    display: flex; align-items: center; justify-content: center;
    font-size: 30px;
  }
  .stats-row { display: flex; justify-content: space-between; gap: 8px; margin-bottom: 14px; }
  .stat { text-align: center; }
  .stat-num { font-size: 20px; font-weight: 800; color: #fff; }
  .stat-label { font-size: 11px; color: var(--muted); margin-top: 1px; }
  .open-btn {
    width: 100%;
    background: linear-gradient(90deg, var(--blue), var(--purple));
    border: none;
    border-radius: 8px;
    color: #fff;
    font-size: 13px;
    font-weight: 600;
    padding: 9px;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center; gap: 6px;
  }

  /* ── SECTION HEADING ── */
  .section-head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  .section-title {
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .view-all {
    font-size: 12px;
    color: var(--blue);
    text-decoration: none;
    border: 1px solid var(--border);
    padding: 5px 12px;
    border-radius: 6px;
    transition: background .2s;
  }
  .view-all:hover { background: rgba(88,166,255,.1); }

  /* ── TECH STACK ── */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 12px;
  }
  .tech-col {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px;
    text-align: center;
  }
  .tech-col-title { font-size: 12px; font-weight: 600; margin-bottom: 12px; }
  .tc-front  { color: var(--blue); }
  .tc-back   { color: var(--green); }
  .tc-mobile { color: var(--cyan); }
  .tc-db     { color: var(--yellow); }
  .tc-tools  { color: var(--orange); }

  .tech-icons { display: flex; justify-content: center; gap: 8px; flex-wrap: wrap; margin-bottom: 8px; }
  .tech-icon {
    width: 32px; height: 32px;
    border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px;
    background: var(--surface);
    border: 1px solid var(--border);
  }
  .tech-names { font-size: 10px; color: var(--muted); line-height: 1.8; }

  /* ── STRENGTHS ── */
  .strengths-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 12px;
  }
  .strength-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
  }
  .strength-card.highlight-pink   { border-color: var(--pink);   background: rgba(247,120,186,.06); }
  .strength-card.highlight-green  { border-color: var(--green);  background: rgba(63,185,80,.06); }
  .strength-card.highlight-orange { border-color: var(--orange); background: rgba(247,129,102,.06); }
  .str-head { display: flex; align-items: center; gap: 8px; margin-bottom: 8px; font-weight: 600; font-size: 13px; color: #fff; }
  .str-icon { font-size: 16px; }
  .str-body { font-size: 12px; color: var(--muted); line-height: 1.5; }

  /* ── DEVELOPER OVERVIEW ── */
  .overview-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .code-block {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px;
    font-family: 'Fira Code', monospace;
    font-size: 12px;
    line-height: 1.8;
  }
  .ln { color: #3d4451; margin-right: 14px; user-select: none; }
  .kw  { color: var(--purple); }
  .fn  { color: var(--blue); }
  .str { color: var(--orange); }
  .arr { color: var(--cyan); }
  .cmt { color: var(--green); }

  .stats-col { display: flex; flex-direction: column; gap: 14px; }

  .gh-stats-card, .lang-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
  }
  .mini-title {
    font-size: 13px; font-weight: 700; color: var(--cyan);
    display: flex; align-items: center; gap: 6px;
    margin-bottom: 12px;
  }
  .stat-row { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; font-size: 12px; }
  .stat-row:last-child { margin-bottom: 0; }
  .stat-label2 { color: var(--muted); display: flex; align-items: center; gap: 6px; }
  .stat-val { font-weight: 700; }
  .sv-blue   { color: var(--blue);   }
  .sv-cyan   { color: var(--cyan);   }
  .sv-red    { color: var(--orange); }
  .sv-green  { color: var(--green);  }

  /* donut */
  .lang-row { display: flex; align-items: center; gap: 14px; }
  .donut-wrap { flex-shrink: 0; }
  .lang-list { flex: 1; }
  .lang-item { display: flex; justify-content: space-between; font-size: 12px; margin-bottom: 6px; align-items: center; gap: 6px; }
  .lang-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .lang-name { color: var(--text); flex:1; }
  .lang-pct  { color: var(--muted); }

  /* contribution graph */
  .contrib-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
  }
  .contrib-months { display: flex; justify-content: space-between; font-size: 10px; color: var(--muted); margin-bottom: 6px; padding: 0 2px; }
  .contrib-grid-wrap { display: flex; gap: 3px; align-items: flex-start; }
  .day-labels { display: flex; flex-direction: column; gap: 3px; font-size: 10px; color: var(--muted); padding-top: 0; }
  .day-label { height: 12px; line-height: 12px; }
  .contrib-grid { display: flex; gap: 3px; flex: 1; }
  .contrib-col { display: flex; flex-direction: column; gap: 3px; }
  .contrib-cell { width: 12px; height: 12px; border-radius: 2px; }
  .c0 { background: #161b22; }
  .c1 { background: #0e4429; }
  .c2 { background: #006d32; }
  .c3 { background: #26a641; }
  .c4 { background: #39d353; }
  .contrib-footer { display: flex; justify-content: space-between; margin-top: 10px; font-size: 12px; }
  .streak-label { color: var(--muted); }
  .streak-val   { color: var(--cyan); font-weight: 600; }

  /* ── QUOTE ── */
  .quote-card {
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 24px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
  }
  .quote-mark { font-size: 48px; color: var(--blue); font-family: Georgia, serif; line-height: .8; flex-shrink: 0; }
  .quote-text { font-size: 15px; color: var(--text); font-style: italic; margin-bottom: 6px; }
  .quote-author { font-size: 13px; color: var(--cyan); }
  .code-art { font-size: 36px; opacity: .4; }

  /* ── FOOTER ── */
  .footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 13px;
    color: var(--muted);
    padding: 0 4px;
  }
  .views-badge {
    display: flex; align-items: center; gap: 8px;
  }
  .badge-pill {
    background: var(--purple);
    color: #fff;
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 20px;
    font-size: 12px;
  }
  .last-updated { display: flex; align-items: center; gap: 6px; }

  @media (max-width: 700px) {
    .hero { grid-template-columns: 1fr; }
    .tech-grid { grid-template-columns: repeat(2, 1fr); }
    .strengths-grid { grid-template-columns: repeat(2, 1fr); }
    .overview-grid { grid-template-columns: 1fr; }
    .hero-name { font-size: 36px; }
  }
</style>
</head>
<body>
<div class="wrapper">

  <!-- ── HERO ── -->
  <div class="card">
    <div class="hero">
      <div class="hero-left">
        <p class="greeting">Hi there 👋, I'm</p>
        <h1 class="hero-name">Designing</h1>
        <p class="hero-title">Full Stack Developer | Web &amp; Mobile Specialist</p>
        <p class="hero-bio">
          I build <span class="fast">fast</span>, <span class="scale">scalable</span>, and <span class="modern">modern</span>
          web &amp; mobile applications<br>with clean code and great user experiences.
        </p>
        <div class="links">
          <a href="#">💬 Portfolio</a>
          <a href="#">in LinkedIn</a>
          <a href="#">✉ Email</a>
          <a href="#">📍 Location</a>
        </div>
        <div class="tags">
          <span class="tag tag-blue">FULL STACK</span>
          <span class="tag tag-purple">FRONTEND FOCUSED</span>
          <span class="tag tag-cyan">MODERN UI/UX</span>
          <span class="tag tag-green">BACKEND AWARE</span>
          <span class="tag tag-orange">SCALABLE SYSTEMS</span>
        </div>
      </div>

      <div class="profile-card">
        <div class="status-dot"><span>Online</span><span class="dot"></span></div>
        <div class="avatar-wrap">
          <div class="avatar-placeholder">🧑‍💻</div>
        </div>
        <div class="stats-row">
          <div class="stat"><div class="stat-num">50+</div><div class="stat-label">Projects</div></div>
          <div class="stat"><div class="stat-num">8+</div><div class="stat-label">Years Exp.</div></div>
          <div class="stat"><div class="stat-num">100+</div><div class="stat-label">Happy Clients</div></div>
        </div>
        <button class="open-btn">🚀 Open to Work</button>
      </div>
    </div>
  </div>

  <!-- ── TECH STACK ── -->
  <div class="card">
    <div class="section-head">
      <h2 class="section-title">🔷 Tech Stack</h2>
      <a href="#" class="view-all">View All Technologies →</a>
    </div>
    <div class="tech-grid">
      <div class="tech-col">
        <div class="tech-col-title tc-front">Frontend</div>
        <div class="tech-icons">
          <div class="tech-icon" title="React">⚛️</div>
          <div class="tech-icon" title="Next.js" style="color:#fff;font-weight:800;font-size:13px;">N</div>
          <div class="tech-icon" title="Vue">🟢</div>
          <div class="tech-icon" title="Angular">🔴</div>
          <div class="tech-icon" title="TypeScript" style="color:#3178c6;font-weight:800;font-size:11px;">TS</div>
        </div>
        <div class="tech-names">React &nbsp; Next.js &nbsp; Vue<br>Angular &nbsp; TypeScript</div>
      </div>
      <div class="tech-col">
        <div class="tech-col-title tc-back">Backend</div>
        <div class="tech-icons">
          <div class="tech-icon">🟩</div>
          <div class="tech-icon" style="font-size:11px;font-weight:700;color:#999;">ex</div>
          <div class="tech-icon">🐍</div>
          <div class="tech-icon" style="font-size:11px;font-weight:700;color:#8892b0;">php</div>
        </div>
        <div class="tech-names">Node.js &nbsp; Express<br>Python &nbsp; PHP</div>
      </div>
      <div class="tech-col">
        <div class="tech-col-title tc-mobile">Mobile</div>
        <div class="tech-icons">
          <div class="tech-icon">🦋</div>
          <div class="tech-icon">⚛️</div>
        </div>
        <div class="tech-names">Flutter &nbsp; React Native</div>
      </div>
      <div class="tech-col">
        <div class="tech-col-title tc-db">Database &amp; Cloud</div>
        <div class="tech-icons">
          <div class="tech-icon">🍃</div>
          <div class="tech-icon">🐘</div>
          <div class="tech-icon">🔴</div>
          <div class="tech-icon" style="font-size:11px;color:#f90;font-weight:800;">aws</div>
        </div>
        <div class="tech-names">MongoDB &nbsp; PostgreSQL<br>Redis &nbsp; AWS</div>
      </div>
      <div class="tech-col">
        <div class="tech-col-title tc-tools">Tools &amp; Others</div>
        <div class="tech-icons">
          <div class="tech-icon">🐳</div>
          <div class="tech-icon">🌿</div>
          <div class="tech-icon">🐙</div>
          <div class="tech-icon">🔵</div>
        </div>
        <div class="tech-names">Docker &nbsp; Git<br>GitHub &nbsp; VS Code</div>
      </div>
    </div>
  </div>

  <!-- ── CORE STRENGTHS ── -->
  <div class="card">
    <div class="section-head"><h2 class="section-title">💎 Core Strengths</h2></div>
    <div class="strengths-grid">
      <div class="strength-card">
        <div class="str-head"><span class="str-icon" style="color:var(--blue)">&lt;/&gt;</span> Clean Code</div>
        <div class="str-body">Writing maintainable, testable and efficient code.</div>
      </div>
      <div class="strength-card">
        <div class="str-head"><span class="str-icon" style="color:var(--yellow)">⚡</span> Performance</div>
        <div class="str-body">Optimizing speed, scalability and user experience.</div>
      </div>
      <div class="strength-card highlight-pink">
        <div class="str-head"><span class="str-icon">🎨</span> UI/UX Focus</div>
        <div class="str-body">Designing intuitive and engaging user interfaces.</div>
      </div>
      <div class="strength-card highlight-green">
        <div class="str-head"><span class="str-icon">🧩</span> Problem Solver</div>
        <div class="str-body">Turning complex problems into simple solutions.</div>
      </div>
      <div class="strength-card highlight-orange">
        <div class="str-head"><span class="str-icon">👥</span> Team Player</div>
        <div class="str-body">Collaborating effectively in agile environments.</div>
      </div>
    </div>
  </div>

  <!-- ── DEVELOPER OVERVIEW ── -->
  <div class="card">
    <div class="section-head"><h2 class="section-title">&gt;_ Developer Overview</h2></div>
    <div class="overview-grid">

      <!-- code block -->
      <div class="code-block">
        <div><span class="ln">1</span><span class="kw">const</span> <span class="fn">developer</span> = {</div>
        <div><span class="ln">2</span>  role: <span class="str">"Full Stack Developer"</span>,</div>
        <div><span class="ln">3</span>  focus: [<span class="arr">"Web"</span>, <span class="arr">"Mobile"</span>],</div>
        <div><span class="ln">4</span>  experience: <span class="str">"8+ Years"</span>,</div>
        <div><span class="ln">5</span>  code: [<span class="arr">"JavaScript"</span>, <span class="arr">"TypeScript"</span>, <span class="arr">"Python"</span>],</div>
        <div><span class="ln">6</span>  architecture: [<span class="arr">"Microservices"</span>, <span class="arr">"REST APIs"</span>, <span class="arr">"Serverless"</span>],</div>
        <div><span class="ln">7</span>  passion: <span class="str">"Building products that make a difference!"</span>,</div>
        <div><span class="ln">8</span>};</div>
        <div><span class="ln">9</span></div>
        <div><span class="ln">10</span><span class="cmt">// Always learning, always building 🚀</span></div>
      </div>

      <!-- stats col -->
      <div class="stats-col">
        <!-- github stats -->
        <div class="gh-stats-card">
          <div class="mini-title">⌨️ GitHub Stats</div>
          <div class="stat-row"><span class="stat-label2">☆ Total Stars Earned</span><span class="stat-val sv-blue">1.2k</span></div>
          <div class="stat-row"><span class="stat-label2">⏱ Total Commits</span><span class="stat-val sv-cyan">2.5k</span></div>
          <div class="stat-row"><span class="stat-label2">↗ Total PRs</span><span class="stat-val sv-red">340</span></div>
          <div class="stat-row"><span class="stat-label2">📦 Repositories</span><span class="stat-val sv-green">65</span></div>
        </div>
        <!-- top languages -->
        <div class="lang-card">
          <div class="mini-title">Top Languages</div>
          <div class="lang-row">
            <div class="donut-wrap">
              <svg width="70" height="70" viewBox="0 0 70 70">
                <circle cx="35" cy="35" r="28" fill="none" stroke="#1c2230" stroke-width="12"/>
                <!-- TypeScript 45% -->
                <circle cx="35" cy="35" r="28" fill="none" stroke="#3178c6" stroke-width="12"
                  stroke-dasharray="79.2 176" stroke-dashoffset="44" transform="rotate(-90 35 35)"/>
                <!-- JavaScript 30% -->
                <circle cx="35" cy="35" r="28" fill="none" stroke="#f0db4f" stroke-width="12"
                  stroke-dasharray="52.8 176" stroke-dashoffset="-35.2" transform="rotate(-90 35 35)"/>
                <!-- Python 15% -->
                <circle cx="35" cy="35" r="28" fill="none" stroke="#306998" stroke-width="12"
                  stroke-dasharray="26.4 176" stroke-dashoffset="-88" transform="rotate(-90 35 35)"/>
                <!-- Other 10% -->
                <circle cx="35" cy="35" r="28" fill="none" stroke="#30363d" stroke-width="12"
                  stroke-dasharray="17.6 176" stroke-dashoffset="-114.4" transform="rotate(-90 35 35)"/>
              </svg>
            </div>
            <div class="lang-list">
              <div class="lang-item"><span class="lang-dot" style="background:#3178c6"></span><span class="lang-name">TypeScript</span><span class="lang-pct">45%</span></div>
              <div class="lang-item"><span class="lang-dot" style="background:#f0db4f"></span><span class="lang-name">JavaScript</span><span class="lang-pct">30%</span></div>
              <div class="lang-item"><span class="lang-dot" style="background:#306998"></span><span class="lang-name">Python</span><span class="lang-pct">15%</span></div>
              <div class="lang-item"><span class="lang-dot" style="background:#30363d"></span><span class="lang-name">Other</span><span class="lang-pct">10%</span></div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- contribution graph -->
    <div class="contrib-card" style="margin-top:16px;">
      <div class="mini-title" style="margin-bottom:10px;">Contribution Graph</div>
      <div class="contrib-months">
        <span>Jan</span><span>Feb</span><span>Mar</span><span>Apr</span><span>May</span>
        <span>Jun</span><span>Jul</span><span>Aug</span><span>Sep</span><span>Oct</span>
        <span>Nov</span><span>Dec</span>
      </div>
      <div class="contrib-grid-wrap" id="contrib-grid">
        <div class="day-labels">
          <div class="day-label">&nbsp;</div>
          <div class="day-label">Mon</div>
          <div class="day-label">&nbsp;</div>
          <div class="day-label">Wed</div>
          <div class="day-label">&nbsp;</div>
          <div class="day-label">Fri</div>
          <div class="day-label">&nbsp;</div>
        </div>
        <div class="contrib-grid" id="grid-cols"></div>
      </div>
      <div class="contrib-footer">
        <span><span class="streak-label">Longest Streak: </span><span class="streak-val">42 days</span></span>
        <span><span class="streak-label">Current Streak: </span><span class="streak-val">12 days</span></span>
      </div>
    </div>
  </div>

  <!-- ── QUOTE ── -->
  <div class="quote-card">
    <div class="quote-mark">"</div>
    <div>
      <p class="quote-text">Code is like humor. When you have to explain it, it's bad.</p>
      <p class="quote-author">– Cory House</p>
    </div>
    <div class="code-art">&lt;/&gt;</div>
  </div>

  <!-- ── FOOTER ── -->
  <div class="footer">
    <div class="views-badge">
      👁 Profile Views <span class="badge-pill">12,345+</span>
    </div>
    <div class="last-updated">
      📅 Last Updated: June 27, 2025
    </div>
  </div>

</div>

<script>
// Generate contribution grid
const grid = document.getElementById('grid-cols');
const weeks = 52;
const days  = 7;
// Weighted random cell levels
function randLevel() {
  const r = Math.random();
  if (r < .35) return 0;
  if (r < .55) return 1;
  if (r < .75) return 2;
  if (r < .90) return 3;
  return 4;
}
for (let w = 0; w < weeks; w++) {
  const col = document.createElement('div');
  col.className = 'contrib-col';
  for (let d = 0; d < days; d++) {
    const cell = document.createElement('div');
    cell.className = 'contrib-cell c' + randLevel();
    col.appendChild(cell);
  }
  grid.appendChild(col);
}
</script>
</body>
</html>
