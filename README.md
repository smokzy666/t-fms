[index.html](https://github.com/user-attachments/files/25848877/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>SENTINEL SECURITY GROUP</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@400;600;700&display=swap" rel="stylesheet" />
<style>
  :root {
    --black: #0a0a0a;
    --charcoal: #141414;
    --steel: #1e1e1e;
    --mid: #2a2a2a;
    --border: #2f2f2f;
    --muted: #666;
    --light: #a0a0a0;
    --white: #f0ede8;
    --accent: #c8972a;
    --accent2: #e8b84b;
    --red: #c0392b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--black);
    color: var(--white);
    font-family: 'Barlow', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 48px;
    height: 64px;
    background: rgba(10,10,10,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 22px;
    letter-spacing: 4px;
    color: var(--accent);
    cursor: pointer;
  }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--light);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  #home {
    position: relative;
    height: 100vh;
    display: flex; align-items: center;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background:
      linear-gradient(135deg, rgba(200,151,42,0.06) 0%, transparent 60%),
      repeating-linear-gradient(
        0deg,
        transparent,
        transparent 60px,
        rgba(255,255,255,0.015) 60px,
        rgba(255,255,255,0.015) 61px
      ),
      repeating-linear-gradient(
        90deg,
        transparent,
        transparent 60px,
        rgba(255,255,255,0.015) 60px,
        rgba(255,255,255,0.015) 61px
      );
  }
  .hero-line {
    position: absolute; top: 0; left: 48px;
    width: 1px; height: 100%;
    background: linear-gradient(to bottom, transparent, var(--accent), transparent);
    opacity: 0.3;
  }
  .hero-content {
    position: relative;
    padding: 0 48px 0 80px;
    max-width: 900px;
  }
  .hero-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 24px;
    display: flex; align-items: center; gap: 16px;
  }
  .hero-label::before {
    content: '';
    display: block;
    width: 32px; height: 1px;
    background: var(--accent);
  }
  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(72px, 10vw, 140px);
    line-height: 0.92;
    letter-spacing: 2px;
    color: var(--white);
    margin-bottom: 32px;
  }
  h1 span { color: var(--accent); }
  .hero-sub {
    font-size: 16px;
    font-weight: 300;
    color: var(--light);
    line-height: 1.7;
    max-width: 480px;
    margin-bottom: 48px;
  }
  .hero-cta {
    display: flex; gap: 16px; flex-wrap: wrap;
  }
  .btn-primary {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 14px 36px;
    background: var(--accent);
    color: var(--black);
    border: none; cursor: pointer; text-decoration: none;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--accent2); transform: translateY(-1px); }
  .btn-outline {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 14px 36px;
    background: transparent;
    color: var(--white);
    border: 1px solid var(--border);
    cursor: pointer; text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

  .hero-contact {
    position: absolute; right: 48px; bottom: 80px;
    display: flex; flex-direction: column; gap: 12px;
    text-align: right;
  }
  .contact-item {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px; letter-spacing: 1.5px;
    color: var(--light);
    text-decoration: none;
    transition: color 0.2s;
  }
  .contact-item:hover { color: var(--accent); }
  .contact-item span {
    display: block;
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 2px;
  }

  /* ── SECTION BASE ── */
  section { padding: 120px 48px; }
  .section-header {
    display: flex; align-items: flex-end; justify-content: space-between;
    margin-bottom: 80px;
    padding-bottom: 24px;
    border-bottom: 1px solid var(--border);
  }
  .section-tag {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
  }
  h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(40px, 5vw, 72px);
    letter-spacing: 2px;
    color: var(--white);
    line-height: 1;
  }
  .section-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 100px;
    color: var(--border);
    line-height: 1;
  }

  /* ── ABOUT ── */
  #about { background: var(--charcoal); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .about-text p {
    font-size: 15px;
    line-height: 1.85;
    color: var(--light);
    margin-bottom: 20px;
  }
  .timeline {
    display: flex; flex-direction: column; gap: 0;
  }
  .tl-item {
    display: grid;
    grid-template-columns: 80px 1fr;
    gap: 24px;
    padding: 24px 0;
    border-bottom: 1px solid var(--border);
    position: relative;
  }
  .tl-item::before {
    content: '';
    position: absolute;
    left: 72px; top: 0; bottom: 0;
    width: 1px;
    background: var(--border);
  }
  .tl-year {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 2px;
    color: var(--accent);
    padding-top: 3px;
  }
  .tl-content strong {
    display: block;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 15px;
    font-weight: 600;
    letter-spacing: 1px;
    color: var(--white);
    margin-bottom: 4px;
  }
  .tl-content p {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
  }

  /* ── STATS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--border);
    margin-top: 80px;
  }
  .stat {
    background: var(--charcoal);
    padding: 40px 32px;
    text-align: center;
  }
  .stat-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 64px;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 8px;
  }
  .stat-label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--muted);
  }

  /* ── PROJECTS ── */
  #former { background: var(--black); }
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
  }
  .project-card {
    background: var(--charcoal);
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    transition: background 0.2s;
  }
  .project-card:hover { background: var(--steel); }
  .project-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }
  .project-card:hover::after { transform: scaleX(1); }
  .project-tag {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
  }
  .project-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 22px;
    font-weight: 700;
    letter-spacing: 1px;
    color: var(--white);
    margin-bottom: 8px;
  }
  .project-sub {
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 20px;
    line-height: 1.5;
  }
  .project-meta {
    display: flex; gap: 24px;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 1px;
    border-top: 1px solid var(--border);
    padding-top: 20px;
    margin-top: auto;
  }
  .project-meta span { color: var(--light); }

  /* ── ONGOING ── */
  #ongoing { background: var(--charcoal); }
  .ongoing-list { display: flex; flex-direction: column; gap: 1px; background: var(--border); }
  .ongoing-item {
    background: var(--charcoal);
    display: grid;
    grid-template-columns: 60px 1fr 200px 160px;
    align-items: center;
    gap: 32px;
    padding: 28px 32px;
    transition: background 0.2s;
  }
  .ongoing-item:hover { background: var(--steel); }
  .ongoing-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    color: var(--border);
  }
  .ongoing-name {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 18px;
    font-weight: 700;
    letter-spacing: 1px;
    color: var(--white);
    margin-bottom: 4px;
  }
  .ongoing-desc { font-size: 13px; color: var(--muted); }
  .progress-wrap { }
  .progress-label {
    display: flex; justify-content: space-between;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    letter-spacing: 2px;
    color: var(--muted);
    margin-bottom: 8px;
    text-transform: uppercase;
  }
  .progress-bar {
    height: 3px;
    background: var(--border);
    position: relative;
  }
  .progress-fill {
    position: absolute; top: 0; left: 0; bottom: 0;
    background: linear-gradient(to right, var(--accent), var(--accent2));
    transition: width 1s ease;
  }
  .status-badge {
    display: inline-flex; align-items: center; gap: 8px;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 6px 14px;
    border: 1px solid;
    justify-self: end;
  }
  .status-badge.active { color: #2ecc71; border-color: #2ecc71; background: rgba(46,204,113,0.05); }
  .status-badge.planning { color: var(--accent); border-color: var(--accent); background: rgba(200,151,42,0.05); }
  .status-badge.review { color: #3498db; border-color: #3498db; background: rgba(52,152,219,0.05); }
  .status-badge::before {
    content: '';
    width: 6px; height: 6px;
    border-radius: 50%;
    background: currentColor;
  }

  /* ── PIPELINE ── */
  #pipeline { background: var(--black); }
  .pipeline-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--border);
  }
  .pipeline-col {
    background: var(--charcoal);
    padding: 32px 24px;
  }
  .pipeline-col-header {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 24px;
    padding-bottom: 16px;
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
  }
  .pipeline-count {
    background: var(--accent);
    color: var(--black);
    font-size: 10px;
    font-weight: 700;
    width: 20px; height: 20px;
    display: flex; align-items: center; justify-content: center;
    border-radius: 0;
  }
  .pipeline-card {
    background: var(--steel);
    padding: 16px;
    margin-bottom: 8px;
    border-left: 2px solid transparent;
    transition: border-color 0.2s;
    cursor: default;
  }
  .pipeline-card:hover { border-left-color: var(--accent); }
  .pipeline-card-title {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 4px;
    letter-spacing: 0.5px;
  }
  .pipeline-card-sub {
    font-size: 11px;
    color: var(--muted);
    margin-bottom: 10px;
  }
  .pipeline-card-value {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 13px;
    font-weight: 600;
    color: var(--accent);
    letter-spacing: 1px;
  }

  /* ── CONTACT ── */
  #contact { background: var(--charcoal); }
  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .contact-info { display: flex; flex-direction: column; gap: 32px; }
  .contact-block span {
    display: block;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 8px;
  }
  .contact-block p {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 20px;
    font-weight: 400;
    letter-spacing: 1px;
    color: var(--white);
  }
  .contact-block a {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 20px;
    font-weight: 400;
    letter-spacing: 1px;
    color: var(--white);
    text-decoration: none;
    transition: color 0.2s;
  }
  .contact-block a:hover { color: var(--accent); }

  /* ── FOOTER ── */
  footer {
    padding: 32px 48px;
    border-top: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    background: var(--black);
  }
  .footer-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 18px;
    letter-spacing: 4px;
    color: var(--accent);
  }
  .footer-copy {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px;
    letter-spacing: 2px;
    color: var(--muted);
    text-transform: uppercase;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-label { animation: fadeUp 0.6s ease 0.2s both; }
  h1 { animation: fadeUp 0.7s ease 0.35s both; }
  .hero-sub { animation: fadeUp 0.7s ease 0.5s both; }
  .hero-cta { animation: fadeUp 0.7s ease 0.65s both; }
  .hero-contact { animation: fadeUp 0.7s ease 0.8s both; }

  @media (max-width: 900px) {
    nav { padding: 0 24px; }
    .nav-links { gap: 20px; }
    section { padding: 80px 24px; }
    .about-grid, .contact-grid { grid-template-columns: 1fr; gap: 48px; }
    .projects-grid { grid-template-columns: 1fr; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .pipeline-grid { grid-template-columns: 1fr 1fr; }
    .ongoing-item { grid-template-columns: 40px 1fr; }
    .progress-wrap, .status-badge { display: none; }
    .hero-contact { display: none; }
    .hero-content { padding: 0 24px 0 40px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">SENTINEL</div>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#former">Former Projects</a></li>
    <li><a href="#ongoing">Ongoing</a></li>
    <li><a href="#pipeline">Pipeline</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="home">
  <div class="hero-bg"></div>
  <div class="hero-line"></div>
  <div class="hero-content">
    <div class="hero-label">Sentinel Security Group — Est. 2008</div>
    <h1>PROTECTING<br>WHAT <span>MATTERS</span></h1>
    <p class="hero-sub">Enterprise-grade physical and electronic security solutions. From perimeter defense to integrated monitoring systems — we secure critical infrastructure across Scandinavia and beyond.</p>
    <div class="hero-cta">
      <a href="#contact" class="btn-primary">Get in Touch</a>
      <a href="#former" class="btn-outline">Our Work</a>
    </div>
  </div>
  <div class="hero-contact">
    <a href="tel:+4512345678" class="contact-item">
      <span>Phone</span>
      +45 12 34 56 78
    </a>
    <a href="mailto:info@sentinelsecurity.dk" class="contact-item">
      <span>Email</span>
      info@sentinelsecurity.dk
    </a>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-header">
    <div>
      <div class="section-tag">Who We Are</div>
      <h2>Company History</h2>
    </div>
    <div class="section-num">01</div>
  </div>
  <div class="about-grid">
    <div class="about-text">
      <p>Sentinel Security Group was founded in 2008 by a team of former law enforcement and military professionals with a shared vision: to deliver security solutions that actually work under pressure.</p>
      <p>What began as a small consultancy in Copenhagen has grown into a full-spectrum security firm operating across Denmark, Sweden, and Norway — with clients ranging from financial institutions and data centers to cultural venues and private estates.</p>
      <p>We combine deep operational expertise with the latest in electronic surveillance, access control, and threat assessment technology. Every solution we build is tailored, tested, and backed by 24/7 response capability.</p>
    </div>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-year">2008</div>
        <div class="tl-content">
          <strong>Founded in Copenhagen</strong>
          <p>Started as a 4-person consultancy specializing in risk assessment.</p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-year">2012</div>
        <div class="tl-content">
          <strong>First Major Contract</strong>
          <p>Secured a 3-year agreement with a major Nordic financial institution.</p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-year">2016</div>
        <div class="tl-content">
          <strong>Expanded to Sweden & Norway</strong>
          <p>Opened regional offices in Malmö and Oslo, doubling staff count.</p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-year">2020</div>
        <div class="tl-content">
          <strong>Technology Division Launch</strong>
          <p>Launched dedicated electronic security and cyber-physical division.</p>
        </div>
      </div>
      <div class="tl-item">
        <div class="tl-year">2024</div>
        <div class="tl-content">
          <strong>ISO 9001 Certified</strong>
          <p>Achieved full quality management certification across all operations.</p>
        </div>
      </div>
    </div>
  </div>
  <div class="stats-row">
    <div class="stat"><div class="stat-num">16</div><div class="stat-label">Years Active</div></div>
    <div class="stat"><div class="stat-num">240+</div><div class="stat-label">Projects Completed</div></div>
    <div class="stat"><div class="stat-num">80+</div><div class="stat-label">Employees</div></div>
    <div class="stat"><div class="stat-num">3</div><div class="stat-label">Countries</div></div>
  </div>
</section>

<!-- FORMER PROJECTS -->
<section id="former">
  <div class="section-header">
    <div>
      <div class="section-tag">Track Record</div>
      <h2>Former Projects</h2>
    </div>
    <div class="section-num">02</div>
  </div>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-tag">Financial</div>
      <div class="project-title">Nordbank HQ Security Overhaul</div>
      <div class="project-sub">Complete redesign of access control, CCTV infrastructure, and guard protocols across 12 floors.</div>
      <div class="project-meta">
        Location: <span>Copenhagen</span> &nbsp;|&nbsp; Year: <span>2022</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-tag">Infrastructure</div>
      <div class="project-title">Malmö Data Center Perimeter</div>
      <div class="project-sub">Multi-layer perimeter defense including thermal imaging, motion analytics, and rapid response integration.</div>
      <div class="project-meta">
        Location: <span>Malmö, SE</span> &nbsp;|&nbsp; Year: <span>2021</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-tag">Cultural Venue</div>
      <div class="project-title">National Museum Event Security</div>
      <div class="project-sub">Crowd management planning, undercover personnel, and real-time threat monitoring for high-footfall exhibits.</div>
      <div class="project-meta">
        Location: <span>Oslo, NO</span> &nbsp;|&nbsp; Year: <span>2023</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-tag">Residential</div>
      <div class="project-title">Private Estate — Hellerup</div>
      <div class="project-sub">Discreet executive protection and full smart-home security integration for a UHNW client.</div>
      <div class="project-meta">
        Location: <span>Hellerup, DK</span> &nbsp;|&nbsp; Year: <span>2023</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-tag">Logistics</div>
      <div class="project-title">Port of Aarhus Cargo Security</div>
      <div class="project-sub">High-value cargo transit monitoring, personnel vetting, and loss-prevention system for port operations.</div>
      <div class="project-meta">
        Location: <span>Aarhus, DK</span> &nbsp;|&nbsp; Year: <span>2020</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-tag">Pharmaceutical</div>
      <div class="project-title">Leo Pharma R&D Facility</div>
      <div class="project-sub">Secure access zones, visitor management, and 24/7 monitoring for sensitive research environments.</div>
      <div class="project-meta">
        Location: <span>Ballerup, DK</span> &nbsp;|&nbsp; Year: <span>2019</span>
      </div>
    </div>
  </div>
</section>

<!-- ONGOING -->
<section id="ongoing">
  <div class="section-header">
    <div>
      <div class="section-tag">Live Operations</div>
      <h2>Ongoing Projects</h2>
    </div>
    <div class="section-num">03</div>
  </div>
  <div class="ongoing-list">
    <div class="ongoing-item">
      <div class="ongoing-num">01</div>
      <div>
        <div class="ongoing-name">Copenhagen Airport — Terminal 3 Upgrade</div>
        <div class="ongoing-desc">Full CCTV refresh and behavioral analytics rollout across departure zones</div>
      </div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Progress</span><span>72%</span></div>
        <div class="progress-bar"><div class="progress-fill" style="width:72%"></div></div>
      </div>
      <div class="status-badge active">Active</div>
    </div>
    <div class="ongoing-item">
      <div class="ongoing-num">02</div>
      <div>
        <div class="ongoing-name">Stockholm Financial District Patrol</div>
        <div class="ongoing-desc">Ongoing roving patrol and incident response contract, 24/7</div>
      </div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Progress</span><span>Ongoing</span></div>
        <div class="progress-bar"><div class="progress-fill" style="width:100%"></div></div>
      </div>
      <div class="status-badge active">Active</div>
    </div>
    <div class="ongoing-item">
      <div class="ongoing-num">03</div>
      <div>
        <div class="ongoing-name">Novo Nordisk Campus — Access Overhaul</div>
        <div class="ongoing-desc">Biometric access control and visitor management across 4 buildings</div>
      </div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Progress</span><span>38%</span></div>
        <div class="progress-bar"><div class="progress-fill" style="width:38%"></div></div>
      </div>
      <div class="status-badge review">In Review</div>
    </div>
    <div class="ongoing-item">
      <div class="ongoing-num">04</div>
      <div>
        <div class="ongoing-name">Roskilde Festival — 2025 Security Plan</div>
        <div class="ongoing-desc">Pre-event threat modeling, crowd control planning, and staff deployment</div>
      </div>
      <div class="progress-wrap">
        <div class="progress-label"><span>Progress</span><span>15%</span></div>
        <div class="progress-bar"><div class="progress-fill" style="width:15%"></div></div>
      </div>
      <div class="status-badge planning">Planning</div>
    </div>
  </div>
</section>

<!-- PIPELINE -->
<section id="pipeline">
  <div class="section-header">
    <div>
      <div class="section-tag">Business Development</div>
      <h2>Project Pipeline</h2>
    </div>
    <div class="section-num">04</div>
  </div>
  <div class="pipeline-grid">
    <div class="pipeline-col">
      <div class="pipeline-col-header">Prospect <div class="pipeline-count">3</div></div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Nordic Logistics Hub</div>
        <div class="pipeline-card-sub">Gothenburg — Perimeter & Cargo</div>
        <div class="pipeline-card-value">Est. DKK 2.4M</div>
      </div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Private Hospital Group</div>
        <div class="pipeline-card-sub">Copenhagen — Access & Patrol</div>
        <div class="pipeline-card-value">Est. DKK 1.8M</div>
      </div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Municipality Facilities</div>
        <div class="pipeline-card-sub">Odense — Multi-site CCTV</div>
        <div class="pipeline-card-value">Est. DKK 900K</div>
      </div>
    </div>
    <div class="pipeline-col">
      <div class="pipeline-col-header">Proposal Sent <div class="pipeline-count">2</div></div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Scandinavian Airlines</div>
        <div class="pipeline-card-sub">CPH Office Security Review</div>
        <div class="pipeline-card-value">DKK 3.1M</div>
      </div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Embassy Row Contract</div>
        <div class="pipeline-card-sub">Copenhagen — Close Protection</div>
        <div class="pipeline-card-value">DKK 1.2M/yr</div>
      </div>
    </div>
    <div class="pipeline-col">
      <div class="pipeline-col-header">Negotiation <div class="pipeline-count">2</div></div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Aarhus Tech Park</div>
        <div class="pipeline-card-sub">Smart Security Integration</div>
        <div class="pipeline-card-value">DKK 4.5M</div>
      </div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">Retail Chain — 22 Sites</div>
        <div class="pipeline-card-sub">Nationwide LP & CCTV</div>
        <div class="pipeline-card-value">DKK 2.8M</div>
      </div>
    </div>
    <div class="pipeline-col">
      <div class="pipeline-col-header">Closing <div class="pipeline-count">1</div></div>
      <div class="pipeline-card">
        <div class="pipeline-card-title">DFDS Ferry Terminal</div>
        <div class="pipeline-card-sub">Copenhagen — Full Security Ops</div>
        <div class="pipeline-card-value">DKK 6.2M</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-header">
    <div>
      <div class="section-tag">Reach Us</div>
      <h2>Get In Touch</h2>
    </div>
    <div class="section-num">05</div>
  </div>
  <div class="contact-grid">
    <div class="contact-info">
      <div class="contact-block">
        <span>Phone</span>
        <a href="tel:+4512345678">+45 12 34 56 78</a>
      </div>
      <div class="contact-block">
        <span>Email</span>
        <a href="mailto:info@sentinelsecurity.dk">info@sentinelsecurity.dk</a>
      </div>
      <div class="contact-block">
        <span>Address</span>
        <p>Gothersgade 103, 2. sal<br>1123 Copenhagen K, Denmark</p>
      </div>
      <div class="contact-block">
        <span>Hours</span>
        <p>Mon–Fri  08:00–18:00<br>Emergency line 24/7</p>
      </div>
    </div>
    <div>
      <p style="font-size:15px; color: var(--light); line-height: 1.8; margin-bottom: 32px;">
        Whether you need a full security assessment, an ongoing patrol contract, or a single-event deployment — we respond quickly and without unnecessary overhead. Reach out and we'll get back to you within one business day.
      </p>
      <a href="mailto:info@sentinelsecurity.dk" class="btn-primary">Send Us a Message</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">SENTINEL</div>
  <div class="footer-copy">© 2025 Sentinel Security Group — All Rights Reserved</div>
</footer>

</body>
</html>
