# Nikitatripathy1625.github.io<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Nikita Tripathy — Data Analyst</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    :root {
      --bg:        #080D1A;
      --bg2:       #0F1628;
      --card:      #141B30;
      --accent:    #B8A9FF;
      --accent2:   #7C6FD4;
      --text:      #F0EFFC;
      --muted:     #8A8FAD;
      --border:    rgba(184,169,255,0.12);
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ─── NAV ─── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; justify-content: space-between; align-items: center;
      padding: 1.2rem 6vw;
      background: rgba(8,13,26,0.82);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
    }
    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.15rem;
      letter-spacing: 0.04em;
      color: var(--accent);
    }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-size: 0.82rem; font-weight: 500; letter-spacing: 0.08em;
      text-transform: uppercase; color: var(--muted);
      text-decoration: none; transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--text); }

    /* ─── HERO ─── */
    #hero {
      position: relative; min-height: 100vh;
      display: flex; align-items: center;
      padding: 0 6vw; overflow: hidden;
    }
    canvas#dots {
      position: absolute; inset: 0;
      width: 100%; height: 100%;
      pointer-events: none; opacity: 0.45;
    }
    .hero-inner { position: relative; z-index: 2; max-width: 680px; }
    .hero-eyebrow {
      display: inline-block;
      font-size: 0.75rem; font-weight: 600; letter-spacing: 0.15em;
      text-transform: uppercase; color: var(--accent);
      margin-bottom: 1.2rem;
      padding: 0.3rem 0.8rem;
      border: 1px solid var(--border);
      border-radius: 40px;
    }
    h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.8rem, 6vw, 5rem);
      font-weight: 700; line-height: 1.08;
      margin-bottom: 1rem;
    }
    h1 em { font-style: italic; color: var(--accent); }
    .hero-desc {
      font-size: 1.05rem; color: var(--muted); max-width: 500px;
      margin-bottom: 2rem; line-height: 1.7;
    }
    .hero-cta {
      display: flex; gap: 1rem; flex-wrap: wrap;
    }
    .btn-primary {
      padding: 0.75rem 1.8rem;
      background: var(--accent); color: var(--bg);
      font-size: 0.85rem; font-weight: 600; letter-spacing: 0.06em;
      border: none; border-radius: 4px; cursor: pointer;
      text-decoration: none; transition: opacity 0.2s;
    }
    .btn-primary:hover { opacity: 0.85; }
    .btn-outline {
      padding: 0.75rem 1.8rem;
      background: transparent; color: var(--text);
      font-size: 0.85rem; font-weight: 500;
      border: 1px solid var(--border); border-radius: 4px;
      cursor: pointer; text-decoration: none; transition: border-color 0.2s;
    }
    .btn-outline:hover { border-color: var(--accent); }

    /* ─── SECTIONS ─── */
    section { padding: 6rem 6vw; }
    section + section { border-top: 1px solid var(--border); }
    .section-label {
      font-size: 0.72rem; font-weight: 600; letter-spacing: 0.14em;
      text-transform: uppercase; color: var(--accent);
      margin-bottom: 0.6rem;
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.8rem, 3.5vw, 2.6rem);
      font-weight: 700; margin-bottom: 3rem;
    }

    /* ─── ABOUT ─── */
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; }
    .about-text p { color: var(--muted); line-height: 1.8; margin-bottom: 1rem; }
    .about-stats { display: flex; flex-direction: column; gap: 1.5rem; }
    .stat-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px; padding: 1.4rem 1.6rem;
    }
    .stat-num {
      font-family: 'Playfair Display', serif;
      font-size: 2.4rem; font-weight: 700; color: var(--accent);
      line-height: 1;
    }
    .stat-label { font-size: 0.82rem; color: var(--muted); margin-top: 0.3rem; }

    /* ─── EXPERIENCE ─── */
    .exp-list { display: flex; flex-direction: column; gap: 0; }
    .exp-item {
      display: grid; grid-template-columns: 200px 1fr;
      gap: 0 2.5rem; padding: 2.5rem 0;
      border-bottom: 1px solid var(--border);
    }
    .exp-item:last-child { border-bottom: none; }
    .exp-meta { padding-top: 0.15rem; }
    .exp-period {
      font-size: 0.78rem; font-weight: 500;
      color: var(--accent); letter-spacing: 0.06em; margin-bottom: 0.3rem;
    }
    .exp-company { font-size: 0.82rem; color: var(--muted); }
    .exp-role {
      font-family: 'Playfair Display', serif;
      font-size: 1.2rem; font-weight: 700; margin-bottom: 1rem;
    }
    .exp-bullets { list-style: none; display: flex; flex-direction: column; gap: 0.6rem; }
    .exp-bullets li {
      font-size: 0.88rem; color: var(--muted); padding-left: 1rem;
      position: relative; line-height: 1.6;
    }
    .exp-bullets li::before {
      content: ''; position: absolute; left: 0; top: 0.55em;
      width: 4px; height: 4px; border-radius: 50%;
      background: var(--accent);
    }

    /* ─── SKILLS ─── */
    .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
    .skill-group {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 8px; padding: 1.6rem;
    }
    .skill-group-title {
      font-size: 0.75rem; font-weight: 600; letter-spacing: 0.1em;
      text-transform: uppercase; color: var(--accent); margin-bottom: 1rem;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
    .skill-tag {
      font-size: 0.78rem; color: var(--muted);
      border: 1px solid var(--border);
      border-radius: 4px; padding: 0.3rem 0.65rem;
      transition: color 0.2s, border-color 0.2s;
    }
    .skill-tag:hover { color: var(--text); border-color: var(--accent); }

    /* ─── PROJECT ─── */
    .project-card {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 10px; padding: 2.2rem 2.4rem;
      max-width: 720px;
    }
    .project-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; margin-bottom: 0.8rem;
    }
    .project-desc { font-size: 0.88rem; color: var(--muted); line-height: 1.75; }
    .project-pills { display: flex; gap: 0.6rem; flex-wrap: wrap; margin-top: 1.2rem; }
    .pill {
      font-size: 0.74rem; font-weight: 500;
      background: rgba(184,169,255,0.1); color: var(--accent);
      border-radius: 20px; padding: 0.25rem 0.7rem;
    }

    /* ─── CERTS ─── */
    .cert-list { display: flex; flex-direction: column; gap: 0.9rem; max-width: 600px; }
    .cert-item {
      display: flex; align-items: center; gap: 1rem;
      padding: 1rem 1.3rem;
      background: var(--card); border: 1px solid var(--border);
      border-radius: 6px;
    }
    .cert-icon { font-size: 1.2rem; }
    .cert-name { font-size: 0.9rem; font-weight: 500; }
    .cert-org { font-size: 0.78rem; color: var(--muted); }

    /* ─── CONTACT ─── */
    #contact { text-align: center; padding: 7rem 6vw; }
    #contact .section-title { margin-bottom: 1rem; }
    #contact p { color: var(--muted); max-width: 440px; margin: 0 auto 2.5rem; }
    .contact-links { display: flex; justify-content: center; gap: 1.2rem; flex-wrap: wrap; }
    .contact-link {
      display: flex; align-items: center; gap: 0.5rem;
      padding: 0.7rem 1.4rem;
      border: 1px solid var(--border); border-radius: 6px;
      color: var(--muted); text-decoration: none;
      font-size: 0.85rem; font-weight: 500;
      transition: color 0.2s, border-color 0.2s;
    }
    .contact-link:hover { color: var(--accent); border-color: var(--accent); }

    /* ─── FOOTER ─── */
    footer {
      text-align: center; padding: 2rem 6vw;
      border-top: 1px solid var(--border);
      font-size: 0.78rem; color: var(--muted);
    }

    /* ─── REVEAL ─── */
    .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.65s ease, transform 0.65s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    @media (max-width: 768px) {
      .about-grid { grid-template-columns: 1fr; gap: 2.5rem; }
      .skills-grid { grid-template-columns: 1fr 1fr; }
      .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
      nav { padding: 1rem 5vw; }
      .nav-links { gap: 1.2rem; }
    }
    @media (max-width: 480px) {
      .skills-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <span class="nav-logo">NT.</span>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Work</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section id="hero">
    <canvas id="dots"></canvas>
    <div class="hero-inner">
      <span class="hero-eyebrow">Data Analyst · Gurugram, India</span>
      <h1>Nikita<br><em>Tripathy</em></h1>
      <p class="hero-desc">
        Turning raw data into clarity. 4+ years building dashboards, automating reports, and driving decisions through clean, reliable insights.
      </p>
      <div class="hero-cta">
        <a href="#experience" class="btn-primary">View My Work</a>
        <a href="mailto:nikitatripathy1625@gmail.com" class="btn-outline">Get in Touch</a>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="reveal">
      <p class="section-label">About</p>
      <h2 class="section-title">Data, distilled.</h2>
    </div>
    <div class="about-grid reveal">
      <div class="about-text">
        <p>I'm a results-driven MIS & Data Analyst with a deep focus on KPI/SLA governance, business intelligence, and process automation. Currently at Boston Consulting Group, I build reporting systems that keep operations accurate and stakeholders informed.</p>
        <p>My approach is simple: reduce noise, surface signal, and automate the repetitive so people can focus on what matters. I work across Excel VBA, Power BI, SQL, and MS Access to make that happen.</p>
        <p>Beyond numbers, I'm a national-level yoga competitor, a dancer recognised by the President of India, and someone who believes discipline from sport translates directly into discipline in data.</p>
      </div>
      <div class="about-stats">
        <div class="stat-card">
          <div class="stat-num">4+</div>
          <div class="stat-label">Years in Data & Reporting Analytics</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">3</div>
          <div class="stat-label">Companies — BCG, Tangent Ideas, Knwodis</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">10%</div>
          <div class="stat-label">Project success rate improvement via cross-functional collaboration</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section id="experience">
    <div class="reveal">
      <p class="section-label">Experience</p>
      <h2 class="section-title">Where I've worked.</h2>
    </div>
    <div class="exp-list">

      <div class="exp-item reveal">
        <div class="exp-meta">
          <div class="exp-period">Jun 2025 – Present</div>
          <div class="exp-company">Boston Consulting Group</div>
        </div>
        <div>
          <div class="exp-role">MIS Analyst</div>
          <ul class="exp-bullets">
            <li>Monitor billability metrics and KPI/SLA dashboards to track project utilisation and operational efficiency.</li>
            <li>Deploy and maintain tracking mechanisms for SLA/KPI operations, ensuring contractual compliance daily.</li>
            <li>Manage governance reporting across Incident Management, Change Management, and Survey Management.</li>
            <li>Automate recurring MIS reports using Advanced Excel VBA/Macros and Power BI, significantly reducing manual effort.</li>
            <li>Identify trends, spot anomalies, and deliver actionable data insights to senior stakeholders.</li>
          </ul>
        </div>
      </div>

      <div class="exp-item reveal">
        <div class="exp-meta">
          <div class="exp-period">Feb 2024 – Nov 2024</div>
          <div class="exp-company">Tangent Ideas & Technology</div>
        </div>
        <div>
          <div class="exp-role">Data Analyst</div>
          <ul class="exp-bullets">
            <li>Performed data cleaning, validation, and quality checks to ensure accuracy and consistency across datasets.</li>
            <li>Automated recurring reports and processes using Excel VBA and MS Access to improve operational efficiency.</li>
            <li>Developed interactive dashboards in Power BI and Excel for performance tracking and decision-making.</li>
            <li>Collaborated with cross-functional teams in a matrixed organisation, improving project success rates by 10%.</li>
          </ul>
        </div>
      </div>

      <div class="exp-item reveal">
        <div class="exp-meta">
          <div class="exp-period">Aug 2022 – Feb 2024</div>
          <div class="exp-company">Knwodis Data Science LLP</div>
        </div>
        <div>
          <div class="exp-role">Data Annotator</div>
          <ul class="exp-bullets">
            <li>Annotated and labelled large datasets — text, images, audio, video — for AI/ML model training with high accuracy.</li>
            <li>Collaborated with data scientists to understand annotation requirements and deliver project goals on time.</li>
            <li>Validated and refined models; improved annotation workflows and documentation processes.</li>
          </ul>
        </div>
      </div>

    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <div class="reveal">
      <p class="section-label">Skills</p>
      <h2 class="section-title">Tools of the trade.</h2>
    </div>
    <div class="skills-grid reveal">
      <div class="skill-group">
        <div class="skill-group-title">Technical</div>
        <div class="skill-tags">
          <span class="skill-tag">Advanced Excel</span>
          <span class="skill-tag">VBA / Macros</span>
          <span class="skill-tag">Power BI</span>
          <span class="skill-tag">SQL</span>
          <span class="skill-tag">MS Access</span>
          <span class="skill-tag">Google Sheets</span>
          <span class="skill-tag">Workday</span>
          <span class="skill-tag">Data Visualisation</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">Reporting & Governance</div>
        <div class="skill-tags">
          <span class="skill-tag">MIS Reporting</span>
          <span class="skill-tag">KPI/SLA Governance</span>
          <span class="skill-tag">Dashboard Development</span>
          <span class="skill-tag">Incident Management</span>
          <span class="skill-tag">Trend Analysis</span>
          <span class="skill-tag">Anomaly Detection</span>
          <span class="skill-tag">Ad Hoc Reporting</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">Data Practices</div>
        <div class="skill-tags">
          <span class="skill-tag">Data Mining</span>
          <span class="skill-tag">Data Validation</span>
          <span class="skill-tag">Pivot Tables</span>
          <span class="skill-tag">Process Automation</span>
          <span class="skill-tag">Data Cleaning</span>
          <span class="skill-tag">Quality Checks</span>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECT -->
  <section id="project">
    <div class="reveal">
      <p class="section-label">Project</p>
      <h2 class="section-title">Personal work.</h2>
    </div>
    <div class="project-card reveal">
      <div class="project-title">HP Spectre Activation — Data Reporting & Automation</div>
      <p class="project-desc">
        Analysed activation data for the HP Spectre product line and streamlined the entire tracking process — eliminating manual errors and reducing turnaround time. Developed custom data validation rules to surface discrepancies in monthly activation records and produced periodic KPI trend analyses for cross-functional review.
      </p>
      <div class="project-pills">
        <span class="pill">Excel VBA</span>
        <span class="pill">Data Validation</span>
        <span class="pill">KPI Reporting</span>
        <span class="pill">Automation</span>
        <span class="pill">Trend Analysis</span>
      </div>
    </div>
  </section>

  <!-- CERTS -->
  <section id="certifications">
    <div class="reveal">
      <p class="section-label">Recognition</p>
      <h2 class="section-title">Certifications & achievements.</h2>
    </div>
    <div class="cert-list reveal">
      <div class="cert-item">
        <span class="cert-icon">📊</span>
        <div>
          <div class="cert-name">Data Analytics Certification</div>
          <div class="cert-org">4 Achievers, Noida</div>
        </div>
      </div>
      <div class="cert-item">
        <span class="cert-icon">🏅</span>
        <div>
          <div class="cert-name">Dancing Award</div>
          <div class="cert-org">President of India, Delhi</div>
        </div>
      </div>
      <div class="cert-item">
        <span class="cert-icon">🧘</span>
        <div>
          <div class="cert-name">Runner-Up — National School Yoga Competition</div>
          <div class="cert-org">National Level</div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="reveal">
      <p class="section-label">Contact</p>
      <h2 class="section-title">Let's connect.</h2>
      <p>Open to new opportunities, collaborations, or just a conversation about data.</p>
      <div class="contact-links">
        <a href="mailto:nikitatripathy1625@gmail.com" class="contact-link">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
          nikitatripathy1625@gmail.com
        </a>
        <a href="tel:+918810624227" class="contact-link">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 9.93a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          +91 8810624227
        </a>
        <a href="https://linkedin.com/in/nikitatripathy16" target="_blank" class="contact-link">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 Nikita Tripathy · Gurugram, India</p>
  </footer>

  <script>
    // ─── DOT GRID ANIMATION ───
    const canvas = document.getElementById('dots');
    const ctx = canvas.getContext('2d');
    let W, H, dots = [];

    function resize() {
      W = canvas.width = canvas.offsetWidth;
      H = canvas.height = canvas.offsetHeight;
      initDots();
    }

    function initDots() {
      dots = [];
      const cols = Math.floor(W / 38);
      const rows = Math.floor(H / 38);
      for (let r = 0; r <= rows; r++) {
        for (let c = 0; c <= cols; c++) {
          dots.push({
            x: c * 38 + 19,
            y: r * 38 + 19,
            base: Math.random(),
            phase: Math.random() * Math.PI * 2,
            speed: 0.003 + Math.random() * 0.004
          });
        }
      }
    }

    let frame = 0;
    function draw() {
      ctx.clearRect(0, 0, W, H);
      frame++;
      dots.forEach(d => {
        d.phase += d.speed;
        const t = (Math.sin(d.phase) + 1) / 2;
        const alpha = 0.06 + t * 0.28;
        const r = 1.2 + t * 1.4;
        ctx.beginPath();
        ctx.arc(d.x, d.y, r, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(184,169,255,${alpha})`;
        ctx.fill();
      });
      requestAnimationFrame(draw);
    }

    window.addEventListener('resize', resize);
    resize();
    draw();

    // ─── SCROLL REVEAL ───
    const reveals = document.querySelectorAll('.reveal');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); } });
    }, { threshold: 0.1 });
    reveals.forEach(el => observer.observe(el));
  </script>
</body>
</html>
