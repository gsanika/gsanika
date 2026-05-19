<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sanika Galgunde — GitHub Profile</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #ffffff;
    --bg-secondary: #f5f5f4;
    --bg-info: #e6f1fb;
    --bg-success: #eaf3de;
    --bg-warning: #faeeda;
    --text: #1a1a18;
    --text-secondary: #5f5e5a;
    --text-tertiary: #888780;
    --text-info: #185fa5;
    --text-success: #3b6d11;
    --text-warning: #854f0b;
    --border: rgba(0,0,0,0.12);
    --border-secondary: rgba(0,0,0,0.22);
    --radius-md: 8px;
    --radius-lg: 12px;
    --radius-xl: 16px;
    --accent: #1a1a18;
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #1c1c1a;
      --bg-secondary: #252523;
      --bg-info: #042c53;
      --bg-success: #173404;
      --bg-warning: #412402;
      --text: #f0ede8;
      --text-secondary: #b4b2a9;
      --text-tertiary: #888780;
      --text-info: #85b7eb;
      --text-success: #97c459;
      --text-warning: #ef9f27;
      --border: rgba(255,255,255,0.1);
      --border-secondary: rgba(255,255,255,0.2);
      --accent: #f0ede8;
    }
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding: 2rem 1rem;
  }

  .container {
    width: 100%;
    max-width: 680px;
  }

  /* Hero */
  .hero {
    display: flex;
    align-items: center;
    gap: 1.25rem;
    margin-bottom: 1.75rem;
  }
  .avatar {
    width: 68px;
    height: 68px;
    border-radius: 50%;
    background: var(--bg-info);
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 600;
    font-size: 22px;
    color: var(--text-info);
    flex-shrink: 0;
    border: 0.5px solid var(--border);
  }
  .hero-info h1 {
    font-size: 22px;
    font-weight: 500;
    color: var(--text);
    line-height: 1.2;
  }
  .hero-info p {
    font-size: 14px;
    color: var(--text-secondary);
    margin-top: 4px;
  }
  .hero-badges {
    display: flex;
    gap: 6px;
    margin-top: 10px;
    flex-wrap: wrap;
  }
  .badge {
    font-size: 12px;
    padding: 3px 10px;
    border-radius: 20px;
    border: 0.5px solid var(--border);
    color: var(--text-secondary);
    background: var(--bg-secondary);
    display: flex;
    align-items: center;
    gap: 5px;
  }
  .badge.active {
    background: var(--bg-success);
    color: var(--text-success);
    border-color: transparent;
  }
  .badge .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: currentColor;
  }

  /* Tabs */
  .tabs {
    display: flex;
    gap: 2px;
    border-bottom: 0.5px solid var(--border);
    margin-bottom: 1.75rem;
    overflow-x: auto;
    scrollbar-width: none;
  }
  .tabs::-webkit-scrollbar { display: none; }
  .tab {
    padding: 8px 16px;
    font-size: 14px;
    cursor: pointer;
    color: var(--text-tertiary);
    border: none;
    background: none;
    border-bottom: 2px solid transparent;
    margin-bottom: -0.5px;
    white-space: nowrap;
    transition: color 0.15s;
    font-family: inherit;
  }
  .tab:hover:not(.active) { color: var(--text); }
  .tab.active {
    color: var(--text);
    border-bottom-color: var(--accent);
    font-weight: 500;
  }

  .panel { display: none; }
  .panel.active { display: block; }

  /* Section label */
  .section-label {
    font-size: 11px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--text-tertiary);
    margin-bottom: 12px;
  }

  /* Info grid */
  .info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 10px;
    margin-bottom: 1.5rem;
  }
  .info-card {
    background: var(--bg-secondary);
    border-radius: var(--radius-md);
    padding: 12px 14px;
  }
  .info-card .label {
    font-size: 12px;
    color: var(--text-tertiary);
    margin-bottom: 5px;
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .info-card .value {
    font-size: 14px;
    font-weight: 500;
    color: var(--text);
  }

  /* Chips */
  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 1.25rem;
  }
  .chip {
    font-size: 13px;
    padding: 5px 12px;
    border-radius: 20px;
    border: 0.5px solid var(--border-secondary);
    color: var(--text);
    background: var(--bg);
    line-height: 1;
  }

  /* Skill groups */
  .skill-group { margin-bottom: 1.5rem; }
  .skill-group .group-title {
    font-size: 12px;
    color: var(--text-tertiary);
    margin-bottom: 10px;
    font-weight: 500;
  }

  /* Projects */
  .projects-list { display: flex; flex-direction: column; gap: 10px; }
  .project-card {
    background: var(--bg);
    border: 0.5px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 14px 16px;
    transition: border-color 0.15s;
  }
  .project-card:hover { border-color: var(--border-secondary); }
  .project-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 12px;
  }
  .project-title {
    font-size: 15px;
    font-weight: 500;
    color: var(--text);
  }
  .project-desc {
    font-size: 13px;
    color: var(--text-secondary);
    margin-top: 4px;
    line-height: 1.5;
  }
  .status-pill {
    font-size: 11px;
    padding: 3px 9px;
    border-radius: 20px;
    flex-shrink: 0;
    margin-top: 2px;
    font-weight: 500;
  }
  .status-active { background: var(--bg-success); color: var(--text-success); }
  .status-done   { background: var(--bg-info);    color: var(--text-info);    }
  .status-ongoing{ background: var(--bg-warning); color: var(--text-warning); }
  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    margin-top: 10px;
  }
  .project-tag {
    font-size: 11px;
    padding: 2px 8px;
    border-radius: 4px;
    background: var(--bg-secondary);
    color: var(--text-secondary);
  }

  /* Roadmap */
  .roadmap-list { display: flex; flex-direction: column; gap: 14px; }
  .roadmap-item { display: flex; align-items: center; gap: 14px; }
  .roadmap-label {
    font-size: 14px;
    color: var(--text);
    width: 150px;
    flex-shrink: 0;
  }
  .roadmap-bar-bg {
    flex: 1;
    height: 6px;
    border-radius: 4px;
    background: var(--bg-secondary);
    overflow: hidden;
  }
  .roadmap-bar {
    height: 100%;
    border-radius: 4px;
    background: var(--accent);
    width: 0%;
    transition: width 1s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .roadmap-status {
    font-size: 12px;
    color: var(--text-tertiary);
    width: 90px;
    text-align: right;
    flex-shrink: 0;
  }

  /* Connect */
  .connect-list { display: flex; flex-direction: column; gap: 8px; }
  .connect-row {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 12px 14px;
    border: 0.5px solid var(--border);
    border-radius: var(--radius-md);
    text-decoration: none;
    color: var(--text);
    transition: border-color 0.15s, background 0.15s;
  }
  .connect-row:hover {
    border-color: var(--border-secondary);
    background: var(--bg-secondary);
  }
  .connect-icon {
    width: 36px;
    height: 36px;
    border-radius: var(--radius-md);
    background: var(--bg-secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    font-size: 18px;
    color: var(--text-secondary);
  }
  .connect-name { font-size: 14px; font-weight: 500; color: var(--text); }
  .connect-handle { font-size: 13px; color: var(--text-secondary); }
  .connect-arrow { margin-left: auto; color: var(--text-tertiary); font-size: 16px; }

  @media (max-width: 500px) {
    .roadmap-label { width: 110px; font-size: 13px; }
    .roadmap-status { width: 70px; font-size: 11px; }
    .hero { gap: 1rem; }
    .avatar { width: 56px; height: 56px; font-size: 18px; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- Hero -->
  <div class="hero">
    <div class="avatar">SG</div>
    <div class="hero-info">
      <h1>Sanika Galgunde</h1>
      <p>AI / ML Developer &bull; Full-Stack &bull; BE Computer Engineering</p>
      <div class="hero-badges">
        <span class="badge"><i class="ti ti-map-pin"></i> Maharashtra, India</span>
        <span class="badge active"><span class="dot"></span> Open to opportunities</span>
        <span class="badge">Final year student</span>
      </div>
    </div>
  </div>

  <!-- Tabs -->
  <div class="tabs">
    <button class="tab active" onclick="showTab('about')">About</button>
    <button class="tab" onclick="showTab('skills')">Skills</button>
    <button class="tab" onclick="showTab('projects')">Projects</button>
    <button class="tab" onclick="showTab('roadmap')">Roadmap</button>
    <button class="tab" onclick="showTab('connect')">Connect</button>
  </div>

  <!-- About -->
  <div id="tab-about" class="panel active">
    <p class="section-label">Quick facts</p>
    <div class="info-grid">
      <div class="info-card">
        <div class="label"><i class="ti ti-school"></i> Education</div>
        <div class="value">BE Computer Engg.</div>
      </div>
      <div class="info-card">
        <div class="label"><i class="ti ti-mail"></i> Email</div>
        <div class="value" style="font-size:12px">galgundesanika@gmail.com</div>
      </div>
      <div class="info-card">
        <div class="label"><i class="ti ti-brand-github"></i> GitHub</div>
        <div class="value">gsanika</div>
      </div>
      <div class="info-card">
        <div class="label"><i class="ti ti-cpu"></i> Focus areas</div>
        <div class="value">CV &bull; NLP &bull; ML</div>
      </div>
    </div>

    <p class="section-label">Currently building</p>
    <div class="chips">
      <span class="chip">Computer Vision apps</span>
      <span class="chip">ML pipelines</span>
      <span class="chip">Full-stack REST APIs</span>
    </div>

    <p class="section-label">Currently learning</p>
    <div class="chips">
      <span class="chip">Deep Learning</span>
      <span class="chip">NLP &amp; Transformers</span>
      <span class="chip">AI-based Applications</span>
    </div>

    <p class="section-label">Ask me about</p>
    <div class="chips">
      <span class="chip">Python</span>
      <span class="chip">OpenCV</span>
      <span class="chip">Scikit-Learn</span>
      <span class="chip">Node.js</span>
      <span class="chip">MongoDB</span>
    </div>
  </div>

  <!-- Skills -->
  <div id="tab-skills" class="panel">
    <div class="skill-group">
      <div class="group-title">Languages</div>
      <div class="chips">
        <span class="chip">Python</span>
        <span class="chip">Java</span>
        <span class="chip">JavaScript</span>
        <span class="chip">SQL</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="group-title">AI / ML / Data Science</div>
      <div class="chips">
        <span class="chip">Scikit-Learn</span>
        <span class="chip">OpenCV</span>
        <span class="chip">Pandas</span>
        <span class="chip">NumPy</span>
        <span class="chip">Matplotlib</span>
        <span class="chip">Seaborn</span>
        <span class="chip">Jupyter</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="group-title">Backend &bull; Database &bull; Mobile</div>
      <div class="chips">
        <span class="chip">Node.js</span>
        <span class="chip">Express.js</span>
        <span class="chip">MongoDB</span>
        <span class="chip">Android</span>
        <span class="chip">Kivy</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="group-title">Data &amp; BI &bull; Tools</div>
      <div class="chips">
        <span class="chip">Power BI</span>
        <span class="chip">Excel</span>
        <span class="chip">GitHub</span>
        <span class="chip">VS Code</span>
      </div>
    </div>
  </div>

  <!-- Projects -->
  <div id="tab-projects" class="panel">
    <div class="projects-list">

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">Face Recognition System</div>
            <div class="project-desc">Real-time detection &amp; recognition with live camera feed</div>
          </div>
          <span class="status-pill status-active">Active</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">OpenCV</span>
          <span class="project-tag">Kivy</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">Disease Prediction ML</div>
            <div class="project-desc">End-to-end ML pipeline with EDA &amp; model evaluation</div>
          </div>
          <span class="status-pill status-active">Active</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Scikit-Learn</span>
          <span class="project-tag">Pandas</span>
          <span class="project-tag">Seaborn</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">Student Management API</div>
            <div class="project-desc">Full CRUD REST API with auth &amp; MongoDB schemas</div>
          </div>
          <span class="status-pill status-active">Active</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Node.js</span>
          <span class="project-tag">Express</span>
          <span class="project-tag">MongoDB</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">Android Task Manager</div>
            <div class="project-desc">Native task app with SQLite local persistence</div>
          </div>
          <span class="status-pill status-done">Done</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Java</span>
          <span class="project-tag">Android SDK</span>
          <span class="project-tag">SQLite</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">EDA Notebook Collection</div>
            <div class="project-desc">Multi-dataset analysis with publication-ready plots</div>
          </div>
          <span class="status-pill status-ongoing">Ongoing</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Pandas</span>
          <span class="project-tag">NumPy</span>
          <span class="project-tag">Matplotlib</span>
        </div>
      </div>

      <div class="project-card">
        <div class="project-header">
          <div>
            <div class="project-title">NLP Text Classifier</div>
            <div class="project-desc">TF-IDF vectorization → classification pipeline</div>
          </div>
          <span class="status-pill status-active">Active</span>
        </div>
        <div class="project-tags">
          <span class="project-tag">Python</span>
          <span class="project-tag">Scikit-Learn</span>
          <span class="project-tag">NLTK</span>
        </div>
      </div>

    </div>
  </div>

  <!-- Roadmap -->
  <div id="tab-roadmap" class="panel">
    <div class="roadmap-list">
      <div class="roadmap-item">
        <div class="roadmap-label">Machine Learning</div>
        <div class="roadmap-bar-bg"><div class="roadmap-bar" data-fill="80"></div></div>
        <div class="roadmap-status">In progress</div>
      </div>
      <div class="roadmap-item">
        <div class="roadmap-label">Computer Vision</div>
        <div class="roadmap-bar-bg"><div class="roadmap-bar" data-fill="66"></div></div>
        <div class="roadmap-status">Building</div>
      </div>
      <div class="roadmap-item">
        <div class="roadmap-label">NLP</div>
        <div class="roadmap-bar-bg"><div class="roadmap-bar" data-fill="53"></div></div>
        <div class="roadmap-status">Exploring</div>
      </div>
      <div class="roadmap-item">
        <div class="roadmap-label">Deep Learning</div>
        <div class="roadmap-bar-bg"><div class="roadmap-bar" data-fill="40"></div></div>
        <div class="roadmap-status">Diving in</div>
      </div>
      <div class="roadmap-item">
        <div class="roadmap-label">AI Applications</div>
        <div class="roadmap-bar-bg"><div class="roadmap-bar" data-fill="47"></div></div>
        <div class="roadmap-status">Creating</div>
      </div>
    </div>
  </div>

  <!-- Connect -->
  <div id="tab-connect" class="panel">
    <div class="connect-list">
      <a href="mailto:galgundesanika@gmail.com" class="connect-row">
        <div class="connect-icon"><i class="ti ti-mail"></i></div>
        <div>
          <div class="connect-name">Email</div>
          <div class="connect-handle">galgundesanika@gmail.com</div>
        </div>
        <i class="ti ti-arrow-right connect-arrow"></i>
      </a>
      <a href="https://github.com/gsanika" target="_blank" rel="noopener" class="connect-row">
        <div class="connect-icon"><i class="ti ti-brand-github"></i></div>
        <div>
          <div class="connect-name">GitHub</div>
          <div class="connect-handle">gsanika</div>
        </div>
        <i class="ti ti-arrow-right connect-arrow"></i>
      </a>
      <a href="https://www.linkedin.com/in/sanika-babruvan-galgunde" target="_blank" rel="noopener" class="connect-row">
        <div class="connect-icon"><i class="ti ti-brand-linkedin"></i></div>
        <div>
          <div class="connect-name">LinkedIn</div>
          <div class="connect-handle">sanika-babruvan-galgunde</div>
        </div>
        <i class="ti ti-arrow-right connect-arrow"></i>
      </a>
      <a href="https://replit.com/@galgundesanika" target="_blank" rel="noopener" class="connect-row">
        <div class="connect-icon"><i class="ti ti-brand-replit"></i></div>
        <div>
          <div class="connect-name">Replit</div>
          <div class="connect-handle">galgundesanika</div>
        </div>
        <i class="ti ti-arrow-right connect-arrow"></i>
      </a>
    </div>
  </div>

</div>

<script>
  function showTab(name) {
    document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
    document.querySelector('[onclick="showTab(\'' + name + '\')"]').classList.add('active');
    document.getElementById('tab-' + name).classList.add('active');
    if (name === 'roadmap') animateBars();
  }

  function animateBars() {
    document.querySelectorAll('.roadmap-bar').forEach(bar => {
      bar.style.width = '0%';
      setTimeout(() => { bar.style.width = bar.dataset.fill + '%'; }, 80);
    });
  }

  // Auto-animate roadmap on first load if visible
  animateBars();
</script>
</body>
</html>
