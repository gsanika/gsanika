<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sanika Babruvan Galgunde – Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0a0a0f;
    --surface: #111118;
    --card: #16161f;
    --border: #2a2a3d;
    --accent: #bf5fff;
    --accent2: #ff4fa3;
    --accent3: #00d4ff;
    --text: #e8e8f0;
    --muted: #7070a0;
    --glow: rgba(191,95,255,0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Background grid */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(191,95,255,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(191,95,255,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    position: relative; z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 48px 24px 80px;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 56px 32px 48px;
    border: 1px solid var(--border);
    border-radius: 20px;
    background: var(--card);
    position: relative;
    overflow: hidden;
    margin-bottom: 32px;
    animation: fadeUp 0.6s ease both;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; left: 50%; transform: translateX(-50%);
    width: 340px; height: 340px;
    background: radial-gradient(circle, rgba(191,95,255,0.22) 0%, transparent 70%);
    pointer-events: none;
  }
  .wave { font-size: 2.6rem; display: block; margin-bottom: 8px; animation: wave 2s ease-in-out infinite; }
  @keyframes wave { 0%,100%{transform:rotate(0deg)} 25%{transform:rotate(20deg)} 75%{transform:rotate(-10deg)} }

  .hero h1 {
    font-size: clamp(1.5rem, 4vw, 2.2rem);
    font-weight: 800;
    background: linear-gradient(120deg, var(--accent), var(--accent2), var(--accent3));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.2;
    margin-bottom: 16px;
  }

  .tagline {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 10px;
    margin-top: 8px;
  }
  .tag {
    background: rgba(191,95,255,0.12);
    border: 1px solid rgba(191,95,255,0.3);
    color: var(--accent);
    padding: 5px 14px;
    border-radius: 20px;
    font-size: 0.82rem;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
  }
  .tag.pink { background: rgba(255,79,163,0.12); border-color: rgba(255,79,163,0.3); color: var(--accent2); }
  .tag.blue { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.3); color: var(--accent3); }

  /* ── SECTIONS ── */
  .section {
    border: 1px solid var(--border);
    border-radius: 16px;
    background: var(--card);
    padding: 28px 32px;
    margin-bottom: 24px;
    animation: fadeUp 0.6s ease both;
  }
  .section:nth-child(2) { animation-delay: 0.1s; }
  .section:nth-child(3) { animation-delay: 0.2s; }
  .section:nth-child(4) { animation-delay: 0.3s; }
  .section:nth-child(5) { animation-delay: 0.4s; }
  .section:nth-child(6) { animation-delay: 0.5s; }

  .section-title {
    font-size: 0.72rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, var(--border), transparent);
  }

  /* ── ABOUT ── */
  .about-list { list-style: none; display: flex; flex-direction: column; gap: 10px; }
  .about-list li {
    padding: 10px 16px;
    background: rgba(255,255,255,0.03);
    border-left: 3px solid var(--accent);
    border-radius: 0 8px 8px 0;
    font-size: 0.92rem;
    line-height: 1.5;
    color: #c8c8e0;
  }
  .about-list li span { color: var(--text); font-weight: 600; }

  /* ── BADGES ── */
  .badges-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  .badge-item {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(255,255,255,0.05);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 8px 14px;
    font-size: 0.78rem;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    transition: all 0.2s ease;
    cursor: default;
    text-decoration: none;
  }
  .badge-item:hover {
    transform: translateY(-2px);
    border-color: var(--accent);
    background: rgba(191,95,255,0.1);
    box-shadow: 0 4px 20px rgba(191,95,255,0.15);
  }
  .badge-dot {
    width: 10px; height: 10px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  /* badge color themes */
  .b-android   { color: #3DDC84; } .b-android .badge-dot   { background: #3DDC84; }
  .b-python    { color: #3776AB; } .b-python .badge-dot    { background: #3776AB; }
  .b-node      { color: #43853D; } .b-node .badge-dot      { background: #43853D; }
  .b-express   { color: #aaaaaa; } .b-express .badge-dot   { background: #aaaaaa; }
  .b-mongo     { color: #4EA94B; } .b-mongo .badge-dot     { background: #4EA94B; }
  .b-kivy      { color: #4CAF50; } .b-kivy .badge-dot      { background: #4CAF50; }
  .b-pandas    { color: #150458; background-color: rgba(21,4,88,0.3);} .b-pandas .badge-dot { background: #a855f7; }
  .b-numpy     { color: #6ab4d0; } .b-numpy .badge-dot     { background: #6ab4d0; }
  .b-sklearn   { color: #F7931E; } .b-sklearn .badge-dot   { background: #F7931E; }
  .b-jupyter   { color: #FA0F00; } .b-jupyter .badge-dot   { background: #FA0F00; }
  .b-powerbi   { color: #F2C811; } .b-powerbi .badge-dot   { background: #F2C811; }
  .b-excel     { color: #217346; } .b-excel .badge-dot     { background: #217346; }
  .b-sql       { color: #4479A1; } .b-sql .badge-dot       { background: #4479A1; }
  .b-github    { color: #c8c8c8; } .b-github .badge-dot    { background: #c8c8c8; }
  .b-matplotlib{ color: #11557C; } .b-matplotlib .badge-dot{ background: #11557C; }
  .b-seaborn   { color: #4C72B0; } .b-seaborn .badge-dot   { background: #4C72B0; }

  /* badge category label */
  .badge-category {
    font-size: 0.68rem;
    font-family: 'Space Mono', monospace;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 10px;
    margin-top: 16px;
  }
  .badge-category:first-child { margin-top: 0; }

  /* ── LEARNING ── */
  .learning-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 12px;
  }
  .learn-card {
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 16px;
    font-size: 0.85rem;
    display: flex;
    align-items: center;
    gap: 10px;
    transition: border-color 0.2s;
  }
  .learn-card:hover { border-color: var(--accent3); }
  .learn-icon { font-size: 1.3rem; }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 14px;
  }
  .stats-grid img {
    width: 100%;
    border-radius: 10px;
    border: 1px solid var(--border);
    display: block;
  }

  /* ── CONNECT ── */
  .connect-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
  }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 22px;
    border-radius: 10px;
    font-family: 'Space Mono', monospace;
    font-size: 0.82rem;
    font-weight: 700;
    text-decoration: none;
    border: 1px solid transparent;
    transition: all 0.2s ease;
    letter-spacing: 0.05em;
  }
  .connect-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,0,0,0.4); }
  .cb-email   { background: rgba(209,72,54,0.15);  border-color: rgba(209,72,54,0.4);  color: #ff6b5b; }
  .cb-github  { background: rgba(200,200,200,0.08); border-color: rgba(200,200,200,0.25); color: #e0e0e0; }
  .cb-linkedin{ background: rgba(10,102,194,0.15); border-color: rgba(10,102,194,0.4); color: #5ba4f5; }
  .cb-replit  { background: rgba(102,102,255,0.15); border-color: rgba(102,102,255,0.4); color: #a0a0ff; }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding-top: 12px;
    font-size: 0.82rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
  }
  .footer span { color: var(--accent); }

  /* ANIMATION */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* RESPONSIVE */
  @media (max-width: 560px) {
    .section { padding: 22px 18px; }
    .hero { padding: 40px 18px 36px; }
  }
</style>
</head>
<body>
<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <span class="wave">👋</span>
    <h1>Hi, I'm Sanika Babruvan Galgunde</h1>
    <div class="tagline">
      <span class="tag">🚀 Aspiring AI/ML Developer</span>
      <span class="tag pink">💻 Full-Stack Enthusiast</span>
      <span class="tag blue">🎓 BE Computer Engineering</span>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-title">💡 About Me</div>
    <ul class="about-list">
      <li>Computer Engineering student passionate about <span>AI, ML, and Full-Stack Development</span>.</li>
      <li>Currently exploring <span>Computer Vision, NLP, and intelligent systems</span>.</li>
      <li>Building projects using <span>Python, Java, Node.js, and modern web technologies</span>.</li>
      <li>Always curious about solving <span>real-world problems with technology</span>.</li>
    </ul>
  </div>

  <!-- TECH STACK / BADGES -->
  <div class="section">
    <div class="section-title">🚀 Tech Stack &amp; Tools</div>

    <div class="badge-category">Mobile &amp; Backend</div>
    <div class="badges-grid">
      <span class="badge-item b-android"><span class="badge-dot"></span>Android</span>
      <span class="badge-item b-python"><span class="badge-dot"></span>Python</span>
      <span class="badge-item b-node"><span class="badge-dot"></span>Node.js</span>
      <span class="badge-item b-express"><span class="badge-dot"></span>Express.js</span>
      <span class="badge-item b-mongo"><span class="badge-dot"></span>MongoDB</span>
      <span class="badge-item b-kivy"><span class="badge-dot"></span>Kivy</span>
    </div>

    <div class="badge-category">Data Science &amp; ML</div>
    <div class="badges-grid">
      <span class="badge-item b-pandas"><span class="badge-dot"></span>Pandas</span>
      <span class="badge-item b-numpy"><span class="badge-dot"></span>NumPy</span>
      <span class="badge-item b-matplotlib"><span class="badge-dot"></span>Matplotlib</span>
      <span class="badge-item b-seaborn"><span class="badge-dot"></span>Seaborn</span>
      <span class="badge-item b-sklearn"><span class="badge-dot"></span>Scikit-Learn</span>
      <span class="badge-item b-jupyter"><span class="badge-dot"></span>Jupyter</span>
    </div>

    <div class="badge-category">Analytics &amp; DevTools</div>
    <div class="badges-grid">
      <span class="badge-item b-powerbi"><span class="badge-dot"></span>Power BI</span>
      <span class="badge-item b-excel"><span class="badge-dot"></span>Microsoft Excel</span>
      <span class="badge-item b-sql"><span class="badge-dot"></span>SQL</span>
      <span class="badge-item b-github"><span class="badge-dot"></span>GitHub</span>
    </div>
  </div>

  <!-- CURRENTLY LEARNING -->
  <div class="section">
    <div class="section-title">🧠 Currently Learning</div>
    <div class="learning-grid">
      <div class="learn-card"><span class="learn-icon">🤖</span> Machine Learning</div>
      <div class="learn-card"><span class="learn-icon">💬</span> NLP</div>
      <div class="learn-card"><span class="learn-icon">👁️</span> Computer Vision</div>
      <div class="learn-card"><span class="learn-icon">🧬</span> Deep Learning</div>
      <div class="learn-card"><span class="learn-icon">🛠️</span> AI Applications</div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-title">📊 GitHub Stats</div>
    <div class="stats-grid">
      <img src="https://streak-stats.demolab.com?user=gsanika&theme=radical&hide_border=true" alt="GitHub Streak"/>
      <img src="https://github-readme-stats.vercel.app/api?username=gsanika&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats"/>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=gsanika&layout=compact&theme=radical&hide_border=true" alt="Top Languages"/>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section">
    <div class="section-title">🌍 Connect With Me</div>
    <div class="connect-grid">
      <a href="mailto:sbgalgunde@gmail.com" class="connect-btn cb-email">
        ✉️ Email
      </a>
      <a href="https://github.com/cd23co66" class="connect-btn cb-github" target="_blank">
        🐙 GitHub
      </a>
      <a href="https://www.linkedin.com/in/sanika-babruvan-galgunde" class="connect-btn cb-linkedin" target="_blank">
        💼 LinkedIn
      </a>
      <a href="https://replit.com/@galgundesanika" class="connect-btn cb-replit" target="_blank">
        ⚡ Replit
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <p>✨ Always learning, building, and exploring new technologies.</p>
    <br/>
    <img src="https://komarev.com/ghpvc/?username=gsanika&color=blueviolet&style=flat-square" alt="Profile Views" style="border-radius:4px;margin-top:8px;"/>
  </div>

</div>
</body>
</html>
