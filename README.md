<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GitHub Profile README – Jericho Earl B. Martin</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&family=Segoe+UI:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #9b0f57;
    --primary-dark: #a0155f;
    --blue: #2563eb;
    --bg: #ffffff;
    --secondary-bg: #f8f9fa;
    --card-bg: #ffffff;
    --text: #333333;
    --border: #e9ecef;
    --shadow: 0 4px 20px rgba(0,0,0,0.1);
    --glow-m: rgba(255,0,127,0.18);
    --glow-b: rgba(37,99,235,0.14);
    --tag-bg: rgba(155,15,87,0.07);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: linear-gradient(to bottom, #ffffff, #f0f2f4);
    color: var(--text);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
  }

  /* === HEADER === */
  .wave-header {
    background: linear-gradient(135deg, #ffffff 0%, #fce4ec 40%, #9b0f57 75%, #2563eb 100%);
    padding: 3.5rem 2rem 3rem;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: var(--shadow);
  }
  .wave-header::before {
    content: '';
    position: absolute; inset: 0;
    background: repeating-linear-gradient(
      55deg,
      rgba(255,255,255,0.06) 0px, rgba(255,255,255,0.06) 1px,
      transparent 1px, transparent 40px
    );
  }
  .wave-header h1 {
    font-size: 2.6rem; font-weight: 700;
    color: white;
    text-shadow: 0 2px 12px rgba(155,15,87,0.5);
    letter-spacing: -0.02em;
    position: relative;
  }
  .wave-header p {
    color: #fce4ec;
    font-size: 1rem;
    margin-top: 0.5rem;
    font-weight: 400;
    letter-spacing: 0.04em;
    position: relative;
  }

  /* === CONTAINER === */
  .container { max-width: 880px; margin: 0 auto; padding: 2.5rem 1.5rem 5rem; }

  hr { border: none; border-top: 1px solid var(--border); margin: 2.2rem 0; }

  /* === ABOUT === */
  .about-text { font-size: 0.96rem; line-height: 1.8; color: var(--text); margin-bottom: 1.3rem; }
  .about-text strong { color: var(--primary); }
  .about-text .blue { color: var(--blue); font-weight: 600; }

  .code-block {
    background: var(--secondary-bg);
    border: 1px solid var(--border);
    border-left: 3px solid var(--primary);
    border-radius: 12px;
    padding: 1.3rem 1.5rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    line-height: 2.2;
    position: relative;
    box-shadow: var(--shadow);
  }
  .code-block::before {
    content: '● ● ●';
    position: absolute; top: 0.6rem; left: 1rem;
    font-size: 0.5rem; letter-spacing: 0.3rem; color: var(--border);
  }
  .code-line { display: flex; gap: 0.8rem; }
  .code-key { color: var(--primary); }
  .code-val { color: var(--blue); }

  /* === SECTION TITLE === */
  .section-title {
    font-size: 1.15rem; font-weight: 700; color: var(--primary);
    display: flex; align-items: center; gap: 0.6rem; margin-bottom: 1.3rem;
  }

  /* === TECH STACK === */
  .stack-group { margin-bottom: 1.2rem; }
  .stack-label {
    font-size: 0.7rem; font-weight: 700; text-transform: uppercase;
    letter-spacing: 0.14em; color: var(--primary); margin-bottom: 0.65rem;
  }
  .badges { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .badge {
    display: inline-flex; align-items: center; gap: 0.4rem;
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 20px; padding: 0.35rem 0.9rem;
    font-size: 0.78rem; font-weight: 600; color: var(--text);
    transition: all 0.3s ease; cursor: default;
    box-shadow: 0 2px 8px rgba(0,0,0,0.06);
  }
  .badge:hover {
    border-color: var(--primary);
    background: var(--tag-bg);
    transform: translateY(-2px);
    box-shadow: 0 4px 15px rgba(155,15,87,0.2);
    color: var(--primary);
  }
  .badge .dot { width: 7px; height: 7px; border-radius: 50%; flex-shrink: 0; }

  /* === STATS === */
  .stats-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1rem; margin-bottom: 0.75rem; }
  .stat-card {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 15px; padding: 1.3rem; text-align: center;
    box-shadow: var(--shadow); transition: all 0.3s ease;
    position: relative; overflow: hidden;
  }
  .stat-card::after {
    content: '';
    position: absolute; bottom: 0; left: 0; right: 0; height: 3px;
    background: linear-gradient(90deg, var(--primary), var(--blue));
  }
  .stat-card:hover { transform: translateY(-4px); box-shadow: 0 8px 25px rgba(155,15,87,0.2); }
  .stat-number {
    font-size: 2.2rem; font-weight: 700;
    font-family: 'JetBrains Mono', monospace;
    color: var(--primary);
  }
  .stat-label { font-size: 0.7rem; color: #666; margin-top: 0.2rem; text-transform: uppercase; letter-spacing: 0.09em; }
  .stat-note { font-size: 0.72rem; color: #aaa; text-align: center; font-style: italic; }

  /* === FEATURED PROJECTS === */
  .project-note { font-size: 0.82rem; color: #888; font-style: italic; margin-bottom: 1rem; border-left: 3px solid var(--blue); padding-left: 0.75rem; }
  .featured-grid { display: flex; flex-direction: column; gap: 1.2rem; margin-bottom: 1.2rem; }

  .feat-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 1.5rem 1.6rem;
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 1.1rem;
    align-items: start;
    box-shadow: var(--shadow);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  .feat-card::before {
    content: '';
    position: absolute; top: 0; left: 0; bottom: 0; width: 4px;
  }
  .feat-card.h1::before { background: linear-gradient(180deg, var(--primary), #a0155f); }
  .feat-card.h2::before { background: linear-gradient(180deg, var(--blue), #1d4ed8); }
  .feat-card.h3::before { background: linear-gradient(180deg, #059669, #10b981); }
  .feat-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(0,0,0,0.15); }

  .feat-icon { font-size: 2rem; line-height: 1; }
  .feat-name {
    font-size: 1.05rem; font-weight: 700; color: var(--primary);
    margin-bottom: 0.25rem; display: flex; align-items: center; gap: 0.5rem; flex-wrap: wrap;
  }
  .feat-card.h2 .feat-name { color: var(--blue); }
  .feat-card.h3 .feat-name { color: #059669; }

  .wip {
    font-size: 0.63rem; font-weight: 700;
    background: linear-gradient(135deg, var(--primary), #a0155f);
    color: white; padding: 0.15rem 0.55rem; border-radius: 20px; letter-spacing: 0.04em;
  }
  .feat-stack { font-family: 'JetBrains Mono', monospace; font-size: 0.75rem; color: var(--blue); margin-bottom: 0.55rem; }
  .feat-desc { font-size: 0.84rem; color: #555; line-height: 1.65; }
  .feat-desc strong { color: var(--text); font-weight: 700; }
  .feat-client {
    display: inline-flex; align-items: center; gap: 0.3rem;
    font-size: 0.72rem; font-weight: 600; color: var(--primary);
    background: var(--tag-bg); border: 1px solid rgba(155,15,87,0.15);
    border-radius: 20px; padding: 0.2rem 0.7rem; margin-top: 0.6rem;
  }
  .feat-card.h2 .feat-client { color: var(--blue); background: rgba(37,99,235,0.07); border-color: rgba(37,99,235,0.15); }

  /* === OTHER PROJECTS === */
  .other-box {
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 15px; overflow: hidden; box-shadow: var(--shadow);
  }
  .other-hdr {
    padding: 0.9rem 1.2rem; font-size: 0.82rem; font-weight: 600;
    color: #888; background: var(--secondary-bg);
    border-bottom: 1px solid var(--border); display: flex; align-items: center; gap: 0.5rem;
  }
  .other-table { width: 100%; border-collapse: collapse; font-size: 0.82rem; }
  .other-table th {
    text-align: left; padding: 0.55rem 1.2rem;
    font-size: 0.68rem; text-transform: uppercase; letter-spacing: 0.1em;
    color: var(--primary); border-bottom: 1px solid var(--border); font-weight: 700;
  }
  .other-table td { padding: 0.8rem 1.2rem; border-bottom: 1px solid rgba(233,236,239,0.6); }
  .other-table tr:last-child td { border-bottom: none; }
  .other-table tr:hover td { background: var(--secondary-bg); }
  .oname { font-weight: 600; color: var(--text); }
  .ostack { font-family: 'JetBrains Mono', monospace; font-size: 0.72rem; color: var(--blue); }
  .odesc { color: #888; font-size: 0.78rem; }

  /* === CERTIFICATIONS === */
  .cert-list { display: flex; flex-direction: column; gap: 0.75rem; }
  .cert-item {
    display: flex; align-items: flex-start; gap: 1rem;
    background: var(--card-bg); border: 1px solid var(--border);
    border-radius: 12px; padding: 1rem 1.2rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.06); transition: all 0.3s ease;
    position: relative; overflow: hidden;
  }
  .cert-item:hover { transform: translateX(4px); box-shadow: var(--shadow); }
  .cert-item.top {
    background: linear-gradient(135deg, var(--primary), #a0155f);
    border-color: var(--primary); color: white;
  }
  .cert-item.top .cert-name { color: white; }
  .cert-item.top .cert-date { color: rgba(255,255,255,0.75); }
  .cert-item.top .cert-sub { color: rgba(255,255,255,0.85); }
  .cert-icon { font-size: 1.3rem; flex-shrink: 0; }
  .cert-name { font-weight: 600; font-size: 0.9rem; color: var(--text); }
  .cert-date { font-size: 0.73rem; color: #888; margin-top: 0.2rem; font-family: 'JetBrains Mono', monospace; }
  .cert-sub { font-size: 0.78rem; color: #666; margin-top: 0.25rem; line-height: 1.5; }

  /* === EXPERIENCE === */
  .exp-card {
    background: var(--card-bg); border: 1px solid var(--border);
    border-left: 4px solid var(--blue); border-radius: 15px;
    padding: 1.5rem 1.6rem; box-shadow: var(--shadow);
  }
  .exp-title { font-weight: 700; font-size: 1rem; color: var(--primary); }
  .exp-company { color: var(--blue); font-size: 0.85rem; margin: 0.3rem 0 0.1rem; font-weight: 600; }
  .exp-date { font-size: 0.73rem; color: #888; margin-bottom: 0.85rem; }
  .exp-list { padding-left: 1.2rem; }
  .exp-list li { font-size: 0.84rem; color: #555; margin-bottom: 0.4rem; line-height: 1.55; }
  .exp-list li::marker { color: var(--primary); }

  /* === CONTACT === */
  .contact-row { display: flex; flex-wrap: wrap; gap: 0.8rem; justify-content: center; }
  .contact-badge {
    display: inline-flex; align-items: center; gap: 0.5rem;
    padding: 0.65rem 1.4rem; border-radius: 25px;
    font-size: 0.85rem; font-weight: 600; text-decoration: none;
    transition: all 0.3s ease; box-shadow: var(--shadow);
  }
  .contact-badge:hover { transform: translateY(-3px); box-shadow: 0 8px 25px rgba(0,0,0,0.2); }
  .cb-li { background: #0A66C2; color: white; }
  .cb-gh { background: var(--primary); color: white; }
  .cb-gm { background: var(--primary); color: white; }
  .cb-fb { background: var(--blue); color: white; }

  /* === FOOTER === */
  .wave-footer {
    background: linear-gradient(135deg, #2563eb 0%, #9b0f57 55%, #ffffff 100%);
    text-align: center; padding: 2rem 1rem 2.5rem;
  }
  .wave-footer p { color: white; font-size: 0.9rem; font-style: italic; font-weight: 500; text-shadow: 0 1px 4px rgba(0,0,0,0.2); }

  /* === COPY BUTTON === */
  .copy-btn {
    position: fixed; bottom: 1.5rem; right: 1.5rem;
    background: linear-gradient(135deg, var(--primary), #a0155f);
    color: white; border: none; border-radius: 25px;
    padding: 0.8rem 1.6rem; font-family: inherit;
    font-size: 0.85rem; font-weight: 700; cursor: pointer;
    box-shadow: 0 4px 20px rgba(155,15,87,0.4); transition: all 0.3s ease; z-index: 999;
  }
  .copy-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 30px rgba(155,15,87,0.5); }

  @media(max-width:600px) {
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .wave-header h1 { font-size: 1.8rem; }
    .feat-card { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="wave-header">
  <h1>👋 Jericho Earl B. Martin</h1>
  <p>IT Student &nbsp;·&nbsp; Web & Software Developer &nbsp;·&nbsp; COIL International Alumnus</p>
</div>

<div class="container">

  <!-- ABOUT -->
  <h2 class="section-title">🧑‍💻 About Me</h2>
  <p class="about-text">
    I'm a <strong>3rd Year BSIT student</strong> from <strong>Davao del Sur State College</strong>, Philippines 🇵🇭 — building things that actually get used, not just things that pass.
    I work across <strong>full-stack web development</strong> (Laravel 12, PHP, React) and <strong>desktop/software development</strong> (.NET 10, C#, WPF), and right now I'm deep in the most challenging projects of my student career — a <span class="blue">construction estimation system</span> for a real engineering firm, and a <span class="blue">scholarship management system</span> commissioned by an actual municipality.
  </p>
  <div class="code-block">
    <br>
    <div class="code-line"><span class="code-key">🎓</span><span class="code-val">Davao del Sur State College · BSIT · Expected 2027</span></div>
    <div class="code-line"><span class="code-key">💻</span><span class="code-val">Web Dev (Laravel/React)  +  Software Dev (.NET/C#/WPF)</span></div>
    <div class="code-line"><span class="code-key">🌍</span><span class="code-val">COIL International Alumnus · Team Lead of 8 (PH × Indonesia)</span></div>
    <div class="code-line"><span class="code-key">📍</span><span class="code-val">Davao City, Philippines</span></div>
  </div>

  <hr>

  <!-- TECH STACK -->
  <h2 class="section-title">🛠️ Tech Stack</h2>
  <div class="stack-group">
    <div class="stack-label">Languages</div>
    <div class="badges">
      <span class="badge"><span class="dot" style="background:#9b4f96"></span>C#</span>
      <span class="badge"><span class="dot" style="background:#b07219"></span>Java</span>
      <span class="badge"><span class="dot" style="background:#4F5D95"></span>PHP</span>
      <span class="badge"><span class="dot" style="background:#d4a800"></span>JavaScript</span>
      <span class="badge"><span class="dot" style="background:#e34c26"></span>HTML</span>
      <span class="badge"><span class="dot" style="background:#563d7c"></span>CSS</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-label">Frameworks & Tools</div>
    <div class="badges">
      <span class="badge"><span class="dot" style="background:#ff2d20"></span>Laravel 12</span>
      <span class="badge"><span class="dot" style="background:#61dafb"></span>React</span>
      <span class="badge"><span class="dot" style="background:#512bd4"></span>.NET 10</span>
      <span class="badge"><span class="dot" style="background:#646cff"></span>Vite</span>
      <span class="badge"><span class="dot" style="background:#f05032"></span>Git</span>
      <span class="badge"><span class="dot" style="background:#333"></span>GitHub</span>
      <span class="badge"><span class="dot" style="background:#f24e1e"></span>Figma</span>
      <span class="badge"><span class="dot" style="background:#007ACC"></span>VS Code</span>
      <span class="badge"><span class="dot" style="background:#68217a"></span>Visual Studio</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-label">Databases & Productivity</div>
    <div class="badges">
      <span class="badge"><span class="dot" style="background:#4479A1"></span>MySQL</span>
      <span class="badge"><span class="dot" style="background:#ef5b25"></span>Postman</span>
      <span class="badge"><span class="dot" style="background:#000"></span>Notion</span>
      <span class="badge"><span class="dot" style="background:#00b4a0"></span>Canva</span>
    </div>
  </div>

  <hr>

  <!-- GITHUB STATS -->
  <h2 class="section-title">📊 GitHub Stats</h2>
  <div class="stats-grid">
    <div class="stat-card"><div class="stat-number">5+</div><div class="stat-label">Public Repos</div></div>
    <div class="stat-card"><div class="stat-number">2</div><div class="stat-label">Real Clients</div></div>
    <div class="stat-card"><div class="stat-number">8</div><div class="stat-label">Int'l Team</div></div>
  </div>
  <p class="stat-note">📌 Live cards (github-readme-stats + streak-stats) auto-render with your real data once deployed on GitHub</p>

  <hr>

  <!-- FEATURED PROJECTS -->
  <h2 class="section-title">🚀 Featured Projects</h2>
  <p class="project-note">💡 Real, client-commissioned projects — not just school compliance work.</p>

  <div class="featured-grid">

    <div class="feat-card h1">
      <div class="feat-icon">🏗️</div>
      <div>
        <div class="feat-name">AzaBuild <span class="wip">IN PROGRESS</span></div>
        <div class="feat-stack">Laravel 12 · React · Vite · MySQL · Laravel Sanctum · DomPDF · Expo (mobile)</div>
        <div class="feat-desc">
          Construction <strong>Quantity Takeoff, Cost Estimation & CPM Project Management</strong> system — built solo.
          Powered by 1,617 material coefficients from Fajardo (1995) with full interpolation/extrapolation engine.
          156 REST API routes, React frontend, task management, worker assignment, weather integration, PDF reports, and mobile offline sync in progress.
        </div>
        <div class="feat-client">🏢 Client: Azacon Builders and Realty OPC, Davao City</div>
      </div>
    </div>

    <div class="feat-card h2">
      <div class="feat-icon">🎓</div>
      <div>
        <div class="feat-name">eSkolar+: LSAS <span class="wip" style="background:linear-gradient(135deg,#2563eb,#1d4ed8)">IN PROGRESS</span></div>
        <div class="feat-stack">.NET 10 · WPF · MySQL · EF Core 9 · QuestPDF · LiveCharts · ClosedXML · WebView2</div>
        <div class="feat-desc">
          <strong>LGU Scholarship Administration System</strong> — full desktop app managing the complete scholarship lifecycle.
          Beneficiary validation against Civil Registry System (CRS), GGMS government fund integration, email OTP login, PDF/Excel reports with in-app preview, and Hostinger cloud deployment.
        </div>
        <div class="feat-client">🏛️ Commissioned by: Municipality of Sulop, Davao del Sur</div>
      </div>
    </div>

    <div class="feat-card h3">
      <div class="feat-icon">🌏</div>
      <div>
        <div class="feat-name" style="color:#059669">TravelWeave</div>
        <div class="feat-stack">Laravel · Figma · MySQL · PHP</div>
        <div class="feat-desc">
          Full-stack <strong>tourism platform</strong> for the COIL International Program.
          Led UI/UX design and coordinated a team of 8 students across <strong>Philippines and Indonesia</strong>.
        </div>
        <div class="feat-client" style="color:#059669;background:rgba(5,150,105,0.07);border-color:rgba(5,150,105,0.15)">🌍 COIL International Program · Philippines × Indonesia</div>
      </div>
    </div>

  </div>

  <!-- OTHER PROJECTS -->
  <div class="other-box">
    <div class="other-hdr">📁 Earlier Academic Projects — compliance work, kept for context</div>
    <table class="other-table">
      <thead><tr><th>Project</th><th>Stack</th><th>Notes</th></tr></thead>
      <tbody>
        <tr><td class="oname">📚 LibraryHub Laravel</td><td class="ostack">Laravel · PHP · MySQL</td><td class="odesc">Full-stack LMS with auth and admin dashboard</td></tr>
        <tr><td class="oname">🏨 Hotel Mgmt System</td><td class="ostack">C# · WinForms · SQL</td><td class="odesc">Desktop app for hotel bookings</td></tr>
        <tr><td class="oname">📖 LibraryHub WinForms</td><td class="ostack">C# · WinForms</td><td class="odesc">Desktop LMS with user authentication</td></tr>
        <tr><td class="oname">🛒 JEM Digital Solutions</td><td class="ostack">Wix</td><td class="odesc">E-commerce for PC components and IoT</td></tr>
      </tbody>
    </table>
  </div>

  <hr>

  <!-- CERTIFICATIONS -->
  <h2 class="section-title">🏅 Certifications & Achievements</h2>
  <div class="cert-list">
    <div class="cert-item top">
      <span class="cert-icon">🌟</span>
      <div>
        <div class="cert-name">COIL International Collaboration Certificate</div>
        <div class="cert-date">September – October 2025</div>
        <div class="cert-sub">Philippines × Indonesia · "Global Web Design: Bridging Cultures through Digital Interfaces"</div>
      </div>
    </div>
    <div class="cert-item"><span class="cert-icon">⛓️</span><div><div class="cert-name">XENEA Campus-Wide Blockchain Experience</div><div class="cert-date">July 25, 2025</div></div></div>
    <div class="cert-item"><span class="cert-icon">🎨</span><div><div class="cert-name">PAGHULAGWAY: A Graphic Design Workshop</div><div class="cert-date">September 26, 2025</div></div></div>
    <div class="cert-item"><span class="cert-icon">🔧</span><div><div class="cert-name">BATCHES Workshop Series</div><div class="cert-date">May 7, 2025</div></div></div>
  </div>

  <hr>

  <!-- EXPERIENCE -->
  <h2 class="section-title">💼 Experience</h2>
  <div class="exp-card">
    <div class="exp-title">Administrative Support (Volunteer)</div>
    <div class="exp-company">Medapharma and Medical Supplies Distribution</div>
    <div class="exp-date">2024 – Present</div>
    <ul class="exp-list">
      <li>Coordinated pharmacy license renewal with government agencies</li>
      <li>Assisted in FDA warehouse registration process</li>
      <li>Managed compliance documents and professional communications</li>
      <li>Data encoding for EDPMS (Electronic Drug Price Monitoring System)</li>
    </ul>
  </div>

  <hr>

  <!-- CONTACT -->
  <h2 class="section-title" style="justify-content:center">📬 Let's Connect</h2>
  <div class="contact-row">
    <a href="https://www.linkedin.com/in/jericho-earl-martin-7262a8362/" class="contact-badge cb-li" target="_blank">in &nbsp;LinkedIn</a>
    <a href="https://github.com/Martinnitram21" class="contact-badge cb-gh" target="_blank">⌥ GitHub</a>
    <a href="mailto:jerichomartin805@gmail.com" class="contact-badge cb-gm" target="_blank">✉ Gmail</a>
    <a href="https://www.facebook.com/jericho.earl.martin/" class="contact-badge cb-fb" target="_blank">f Facebook</a>
  </div>

</div>

<div class="wave-footer">
  <p>"We suffer more in imagination than in reality." — Seneca</p>
</div>

<button class="copy-btn" onclick="copyReadme()">📋 Copy README.md</button>

<script>
const readme = `<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ffffff,40:fce4ec,70:9b0f57,100:2563eb&height=200&section=header&text=Jericho%20Earl%20B.%20Martin&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=IT%20Student%20%7C%20Web%20%26%20Software%20Developer&descAlignY=58&descSize=18&descColor=fce4ec&animation=fadeIn" width="100%"/>

</div>

---

### 👋 Hey there! I'm Jericho

I'm a **3rd Year BSIT student** from **Davao del Sur State College**, Philippines 🇵🇭 — building things that actually get used, not just things that pass.

I work across **full-stack web development** (Laravel 12, PHP, React) and **desktop/software development** (.NET 10, C#, WPF), and right now I'm deep in the most challenging projects of my student career — a construction estimation system for a real engineering firm, and a scholarship management system commissioned by an actual municipality.

\`\`\`text
🎓  Davao del Sur State College  |  BSIT - Expected 2027
💻  Web Dev (Laravel/React)  +  Software Dev (.NET/C#/WPF)
🌍  COIL International Alumnus  |  Team Lead of 8 (PH × Indonesia)
📍  Davao City, Philippines
\`\`\`

---

### 🛠️ Tech Stack

**Languages**

[![My Skills](https://skillicons.dev/icons?i=cs,java,php,js,html,css)](https://skillicons.dev)

**Frameworks & Tools**

[![My Skills](https://skillicons.dev/icons?i=laravel,react,dotnet,vite,git,github,figma,vscode)](https://skillicons.dev)

**Databases & More**

[![My Skills](https://skillicons.dev/icons?i=mysql,postman,notion)](https://skillicons.dev)

---

### 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Martinnitram21&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&title_color=9b0f57&icon_color=2563eb&text_color=333333&bg_color=ffffff" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Martinnitram21&layout=compact&hide_border=true&langs_count=6&title_color=9b0f57&text_color=333333&bg_color=ffffff" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Martinnitram21&hide_border=true&background=ffffff&ring=9b0f57&fire=2563eb&currStreakLabel=9b0f57)](https://git.io/streak-stats)

</div>

---

### 🚀 Featured Projects

> 💡 Real, client-commissioned projects — not just school compliance work.

| | Project | Stack | About |
|---|---|---|---|
| 🏗️ | **AzaBuild** *(In Progress)* | Laravel 12 · React · Vite · MySQL · Sanctum | Construction Quantity Takeoff, Cost Estimation & CPM Project Management system. Built solo for **Azacon Builders and Realty OPC**, Davao City. Based on Fajardo (1995) — 1,617 material coefficients, interpolation/extrapolation engine, React frontend, PDF generation, mobile sync in progress. |
| 🎓 | **eSkolar+: LSAS** *(In Progress)* | .NET 10 · WPF · MySQL · EF Core · QuestPDF | LGU Scholarship Administration System commissioned by the **Municipality of Sulop, Davao del Sur**. Manages applications, disbursements, beneficiary verification (CRS), GGMS fund integration, OTP login, PDF/Excel reports, and cloud deployment on Hostinger. |
| 🌏 | **TravelWeave** | Laravel · Figma · MySQL | Full-stack tourism platform built with a PH–Indonesia team for the COIL International Program. Led UI/UX and a team of 8 across two countries. |

---

### 📁 Other Projects

<details>
<summary>Earlier academic work (click to expand)</summary>

| Project | Stack | Notes |
|---|---|---|
| 📚 LibraryHub (Laravel) | Laravel · PHP · MySQL | Full-stack LMS with auth and admin dashboard |
| 🏨 Hotel Management System | C# · WinForms · SQL | Desktop app for hotel bookings and admin |
| 📖 LibraryHub (WinForms) | C# · WinForms | Desktop LMS with user authentication |
| 🛒 JEM Digital Solutions | Wix | E-commerce site for PC components and IoT devices |

</details>

---

### 🏅 Certifications & Achievements

- 🌟 **COIL International Collaboration** — *Philippines × Indonesia, Global Web Design Program* \`Sept–Oct 2025\`
- ⛓️ **XENEA Campus-Wide Blockchain Experience** \`July 2025\`
- 🎨 **PAGHULAGWAY: Graphic Design Workshop** \`September 2025\`
- 🔧 **BATCHES Workshop Series** \`May 2025\`

---

### 💼 Experience

**Administrative Support (Volunteer)** · *Medapharma and Medical Supplies Distribution* · \`2024 – Present\`
- Coordinated pharmacy license renewal with government agencies
- Assisted in FDA warehouse registration
- Data encoding for EDPMS (Electronic Drug Price Monitoring System)

---

### 📬 Let's Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jericho-earl-martin-7262a8362/)
[![GitHub](https://img.shields.io/badge/GitHub-9b0f57?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Martinnitram21)
[![Email](https://img.shields.io/badge/Gmail-9b0f57?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jerichomartin805@gmail.com)
[![Facebook](https://img.shields.io/badge/Facebook-2563eb?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/jericho.earl.martin/)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,50:9b0f57,100:ffffff&height=100&section=footer" width="100%"/>

*"We suffer more in imagination than in reality." — Seneca*

</div>`;

function copyReadme() {
  navigator.clipboard.writeText(readme).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✅ Copied!';
    btn.style.background = 'linear-gradient(135deg,#059669,#10b981)';
    setTimeout(() => { btn.textContent = '📋 Copy README.md'; btn.style.background = ''; }, 2500);
  });
}
</script>
</body>
</html>
