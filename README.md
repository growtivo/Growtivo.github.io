<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lesedi Malatsi — Brand Strategist & Virtual Assistant</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --navy: #0a1628;
  --navy2: #0d2145;
  --blue: #1a4fa0;
  --blue2: #1e6fbf;
  --green: #2ecc5e;
  --green2: #22a84a;
  --teal: #00c6a7;
  --white: #ffffff;
  --cream: #f5f7fa;
  --ink: #0d1117;
  --muted: #5a6a7e;
  --border: rgba(10,22,40,0.10);
  --grad: linear-gradient(135deg, #0a1628 0%, #1a4fa0 60%, #2ecc5e 100%);
  --grad2: linear-gradient(90deg, #1a4fa0 0%, #2ecc5e 100%);
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { font-family: 'Inter', sans-serif; background: var(--cream); color: var(--ink); font-size: 15px; line-height: 1.7; }

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 200;
  background: rgba(10,22,40,0.97);
  backdrop-filter: blur(10px);
  height: 58px;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 32px;
  border-bottom: 1px solid rgba(46,204,94,0.2);
}
.nav-brand { display: flex; align-items: center; gap: 10px; text-decoration: none; }
.nav-brand img { height: 32px; width: auto; border-radius: 4px; }
.nav-name { font-size: 14px; font-weight: 600; color: #fff; letter-spacing: 0.02em; }
.nav-links { display: flex; gap: 28px; list-style: none; }
.nav-links a { font-size: 13px; color: rgba(255,255,255,0.55); text-decoration: none; transition: color 0.2s; }
.nav-links a:hover { color: var(--green); }
.nav-cta {
  font-size: 13px; font-weight: 600;
  background: var(--green); color: var(--navy);
  padding: 8px 20px; border-radius: 3px;
  text-decoration: none; transition: background 0.2s;
  letter-spacing: 0.02em;
}
.nav-cta:hover { background: var(--green2); color: #fff; }

/* BANNER STRIP */
.banner-strip {
  margin-top: 58px;
  width: 100%;
  overflow: hidden;
  max-height: 200px;
  position: relative;
}
.growtivobanner img {
  width: 100%;
  object-fit: cover;
  object-position: center;
  display: block;
}
.banner-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to bottom, transparent 40%, rgba(10,22,40,0.6) 100%);
}

/* HERO */
.hero {
  background: var(--navy);
  padding: 64px 40px 72px;
  position: relative;
  overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute; top: -80px; right: -80px;
  width: 420px; height: 420px; border-radius: 50%;
  background: radial-gradient(circle, rgba(46,204,94,0.08) 0%, transparent 70%);
  pointer-events: none;
}
.hero::after {
  content: '';
  position: absolute; bottom: 0; left: 0; right: 0; height: 2px;
  background: var(--grad2);
}
.hero-inner { max-width: 900px; margin: 0 auto; display: grid; grid-template-columns: 1fr auto; gap: 40px; align-items: center; }
.hero-badge {
  display: inline-flex; align-items: center; gap: 8px;
  font-size: 11px; font-weight: 600; letter-spacing: 0.14em;
  text-transform: uppercase; color: var(--green);
  background: rgba(46,204,94,0.1);
  border: 1px solid rgba(46,204,94,0.25);
  padding: 5px 14px; border-radius: 20px;
  margin-bottom: 20px;
}
.hero-badge::before { content: '●'; font-size: 8px; animation: pulse 2s infinite; }
@keyframes pulse { 0%,100%{opacity:1} 50%{opacity:0.3} }
.hero-name {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(38px, 5.5vw, 68px);
  line-height: 1.06; color: #fff;
  margin-bottom: 8px;
}
.hero-name span { color: var(--green); }
.hero-title {
  font-size: 15px; font-weight: 500; color: rgba(255,255,255,0.5);
  letter-spacing: 0.06em; text-transform: uppercase;
  margin-bottom: 22px;
}
.hero-desc {
  font-size: 16px; line-height: 1.8; color: rgba(255,255,255,0.72);
  max-width: 540px; margin-bottom: 32px;
}
.hero-actions { display: flex; gap: 14px; flex-wrap: wrap; align-items: center; margin-bottom: 48px; }
.btn-green {
  background: var(--green); color: var(--navy);
  padding: 13px 28px; border-radius: 3px;
  font-size: 14px; font-weight: 700;
  text-decoration: none; transition: all 0.2s;
  letter-spacing: 0.02em;
}
.btn-green:hover { background: var(--green2); color: #fff; transform: translateY(-1px); }
.btn-outline {
  border: 1.5px solid rgba(255,255,255,0.25); color: rgba(255,255,255,0.8);
  padding: 12px 24px; border-radius: 3px;
  font-size: 14px; font-weight: 500;
  text-decoration: none; transition: all 0.2s;
}
.btn-outline:hover { border-color: var(--green); color: var(--green); }
.hero-stats { display: grid; grid-template-columns: repeat(4,1fr); gap: 1px; background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.08); border-radius: 4px; overflow: hidden; }
.hero-stat { padding: 18px 20px; background: rgba(255,255,255,0.04); text-align: center; }
.hero-stat-num { font-family: 'DM Serif Display', serif; font-size: 32px; color: var(--green); line-height: 1; }
.hero-stat-label { font-size: 10px; font-weight: 600; color: rgba(255,255,255,0.4); text-transform: uppercase; letter-spacing: 0.1em; margin-top: 5px; }
.hero-logo-block { display: flex; flex-direction: column; align-items: center; gap: 12px; }
.hero-logo-block img { width: 140px; height: auto; filter: drop-shadow(0 4px 24px rgba(46,204,94,0.3)); }
.hero-avail { font-size: 11px; font-weight: 600; color: var(--green); text-transform: uppercase; letter-spacing: 0.1em; text-align: center; }

/* HIRE MODES */
.hire-strip { background: var(--navy2); padding: 32px 40px; border-bottom: 1px solid rgba(46,204,94,0.15); }
.hire-strip-inner { max-width: 900px; margin: 0 auto; display: flex; align-items: center; gap: 16px; flex-wrap: wrap; }
.hire-label { font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.12em; color: rgba(255,255,255,0.4); margin-right: 8px; flex-shrink: 0; }
.hire-pill {
  display: flex; align-items: center; gap: 8px;
  background: rgba(46,204,94,0.08);
  border: 1px solid rgba(46,204,94,0.2);
  border-radius: 3px; padding: 10px 18px;
}
.hire-pill-icon { font-size: 16px; }
.hire-pill-title { font-size: 13px; font-weight: 600; color: #fff; }
.hire-pill-sub { font-size: 11px; color: rgba(255,255,255,0.45); }

/* SECTIONS */
section { padding: 80px 24px; }
.container { max-width: 900px; margin: 0 auto; }
.sec-tag {
  font-size: 11px; font-weight: 700; letter-spacing: 0.14em;
  text-transform: uppercase; color: var(--green);
  margin-bottom: 10px; display: flex; align-items: center; gap: 10px;
}
.sec-tag::after { content: ''; display: block; width: 32px; height: 1.5px; background: var(--green); }
.sec-head {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(26px, 4vw, 40px);
  color: var(--navy); line-height: 1.1;
  margin-bottom: 40px;
}

/* SERVICES */
#services { background: #fff; }
.services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; }
.service-card {
  border: 1.5px solid var(--border);
  border-radius: 4px; padding: 28px 22px;
  transition: all 0.2s; position: relative; overflow: hidden;
  background: #fff;
}
.service-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
  background: var(--grad2); transform: scaleX(0); transform-origin: left;
  transition: transform 0.3s;
}
.service-card:hover { border-color: rgba(46,204,94,0.4); transform: translateY(-3px); box-shadow: 0 8px 32px rgba(10,22,40,0.08); }
.service-card:hover::before { transform: scaleX(1); }
.service-num { font-family: 'DM Serif Display', serif; font-size: 28px; color: rgba(10,22,40,0.08); margin-bottom: 14px; }
.service-icon { font-size: 22px; margin-bottom: 10px; }
.service-title { font-size: 15px; font-weight: 700; color: var(--navy); margin-bottom: 10px; }
.service-desc { font-size: 13px; color: var(--muted); line-height: 1.65; }
.service-tags { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 14px; }
.service-tag { font-size: 10px; font-weight: 600; padding: 3px 9px; border-radius: 2px; background: rgba(26,79,160,0.07); color: var(--blue); letter-spacing: 0.04em; }

/* BRAND SPOTLIGHT */
#brand { background: var(--navy); position: relative; overflow: hidden; }
#brand::before { content: ''; position: absolute; top: -100px; right: -100px; width: 500px; height: 500px; border-radius: 50%; background: radial-gradient(circle, rgba(46,204,94,0.06) 0%, transparent 70%); pointer-events: none; }
#brand .sec-tag { color: var(--green); }
#brand .sec-head { color: #fff; }
.brand-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 56px; align-items: start; }
.brand-body { font-size: 15px; color: rgba(255,255,255,0.65); line-height: 1.85; margin-bottom: 20px; }
.brand-quote {
  font-family: 'DM Serif Display', serif; font-style: italic;
  font-size: 20px; color: #fff; line-height: 1.45;
  border-left: 3px solid var(--green);
  padding: 16px 20px; margin: 28px 0;
  background: rgba(46,204,94,0.05);
}
.platforms-row { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 8px; }
.platform-chip {
  display: flex; align-items: center; gap: 6px;
  font-size: 12px; font-weight: 600;
  padding: 6px 14px; border-radius: 3px;
  background: rgba(255,255,255,0.07);
  border: 1px solid rgba(255,255,255,0.12);
  color: rgba(255,255,255,0.8);
}
.gap-list { display: flex; flex-direction: column; gap: 0; }
.gap-row {
  display: flex; align-items: flex-start; gap: 14px;
  padding: 16px 0; border-bottom: 1px solid rgba(255,255,255,0.07);
}
.gap-row:last-child { border-bottom: none; }
.gap-icon { font-size: 18px; flex-shrink: 0; margin-top: 2px; }
.gap-title { font-size: 14px; font-weight: 600; color: #fff; margin-bottom: 3px; }
.gap-desc { font-size: 13px; color: rgba(255,255,255,0.5); line-height: 1.55; }

/* WHY HIRE */
#why { background: var(--cream); }
.why-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 16px; }
.why-card {
  background: #fff; border-radius: 4px; padding: 24px 20px;
  border: 1px solid var(--border);
  position: relative;
}
.why-card-accent {
  width: 36px; height: 3px; border-radius: 2px;
  background: var(--grad2); margin-bottom: 16px;
}
.why-card-title { font-size: 14px; font-weight: 700; color: var(--navy); margin-bottom: 8px; }
.why-card-body { font-size: 13px; color: var(--muted); line-height: 1.6; }
.hire-types { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 36px; }
.hire-type {
  display: flex; align-items: center; gap: 8px;
  background: var(--navy); color: #fff;
  font-size: 13px; font-weight: 600;
  padding: 10px 18px; border-radius: 3px;
}
.hire-type-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--green); flex-shrink: 0; }

/* EXPERIENCE */
#experience { background: #fff; }
.exp-timeline { position: relative; }
.exp-timeline::before { content: ''; position: absolute; left: 178px; top: 0; bottom: 0; width: 1px; background: var(--border); }
.exp-row { display: grid; grid-template-columns: 170px 1fr; gap: 32px; padding: 28px 0 28px 24px; position: relative; }
.exp-row::before { content: ''; position: absolute; left: 171px; top: 36px; width: 9px; height: 9px; border-radius: 50%; background: var(--green); border: 2px solid #fff; box-shadow: 0 0 0 1px var(--border); }
.exp-meta {}
.exp-period { font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); margin-bottom: 4px; }
.exp-company { font-size: 13px; font-weight: 600; color: var(--blue); }
.exp-role { font-size: 15px; font-weight: 700; color: var(--navy); margin-bottom: 10px; }
.exp-bullets { list-style: none; display: flex; flex-direction: column; gap: 6px; }
.exp-bullets li { font-size: 13px; color: var(--muted); padding-left: 16px; position: relative; line-height: 1.6; }
.exp-bullets li::before { content: '→'; position: absolute; left: 0; color: var(--green); font-size: 11px; top: 3px; }

/* SKILLS */
#skills { background: var(--navy); }
#skills .sec-head { color: #fff; }
.skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 32px; }
.skill-group-title { font-size: 11px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--green); margin-bottom: 14px; }
.skill-tags { display: flex; flex-wrap: wrap; gap: 7px; }
.skill-tag { font-size: 12px; font-weight: 500; padding: 6px 13px; border-radius: 2px; background: rgba(255,255,255,0.07); color: rgba(255,255,255,0.75); border: 1px solid rgba(255,255,255,0.10); transition: all 0.15s; cursor: default; }
.skill-tag:hover { background: rgba(46,204,94,0.12); border-color: rgba(46,204,94,0.3); color: var(--green); }

/* CTA */
#contact { background: var(--cream); text-align: center; padding: 100px 24px; }
.cta-head { font-family: 'DM Serif Display', serif; font-size: clamp(30px, 5vw, 52px); color: var(--navy); line-height: 1.1; margin-bottom: 16px; max-width: 620px; margin-left: auto; margin-right: auto; }
.cta-head span { color: var(--green2); }
.cta-sub { font-size: 15px; color: var(--muted); margin-bottom: 36px; max-width: 480px; margin-left: auto; margin-right: auto; }
.cta-cards { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; margin-top: 48px; }
.cta-card {
  background: #fff; border: 1px solid var(--border);
  border-radius: 4px; padding: 20px 24px;
  display: flex; align-items: center; gap: 12px;
  text-decoration: none; transition: all 0.2s; min-width: 220px;
}
.cta-card:hover { border-color: var(--green); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(10,22,40,0.08); }
.cta-card-icon { font-size: 22px; flex-shrink: 0; }
.cta-card-label { font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.1em; color: var(--muted); }
.cta-card-val { font-size: 13px; font-weight: 600; color: var(--navy); }

/* FOOTER */
footer {
  background: var(--navy);
  display: flex; align-items: center; justify-content: space-between;
  padding: 22px 40px; flex-wrap: wrap; gap: 12px;
}
.footer-brand { display: flex; align-items: center; gap: 10px; }
.footer-brand img { height: 28px; }
.footer-copy { font-size: 12px; color: rgba(255,255,255,0.3); }
.footer-links { display: flex; gap: 20px; }
.footer-links a { font-size: 12px; color: rgba(255,255,255,0.35); text-decoration: none; transition: color 0.2s; }
.footer-links a:hover { color: var(--green); }

/* RESPONSIVE */
@media (max-width: 700px) {
  nav { padding: 0 16px; }
  .nav-links { display: none; }
  .hero { padding: 48px 20px 56px; }
  .hero-inner { grid-template-columns: 1fr; }
  .hero-logo-block { display: none; }
  .hero-stats { grid-template-columns: repeat(2,1fr); }
  .hire-strip { padding: 24px 20px; }
  section { padding: 60px 20px; }
  .brand-layout { grid-template-columns: 1fr; gap: 36px; }
  .exp-timeline::before { display: none; }
  .exp-row { grid-template-columns: 1fr; gap: 6px; padding-left: 0; }
  .exp-row::before { display: none; }
}
@media (prefers-reduced-motion: reduce) { * { transition: none !important; animation: none !important; } }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-brand">
    <img src="https://i.imgur.com/placeholder.png" alt="Growtivo" id="nav-logo" style="display:none">
    <span class="nav-name">Lesedi Malatsi</span>
  </a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#brand">Brand strategy</a></li>
    <li><a href="#why">Why hire me</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#skills">Skills</a></li>
  </ul>
  <a href="mailto:Lesedi.malatsi@outlook.com" class="nav-cta">Hire me</a>
</nav>

<!-- BANNER -->
<div class="banner-strip">
  <img src="IMG_8735.jpeg" alt="Growtivo — Where Marketing Meets Technology and Makes Revenue" onerror="this.parentElement.style.display='none'">
  <div class="banner-overlay"></div>
</div>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-inner">
    <div>
      <div class="hero-badge">Available for remote contracts worldwide</div>
      <p class="hero-title">Virtual Assistant · Brand Strategist · Growth Partner</p>
      <h1 class="hero-name">Lesedi<br><span>Malatsi</span></h1>
      <p class="hero-desc">10+ years helping businesses run smoother, show up louder, and close the gaps that cost them money — as part of your team, a contractor, or a freelancer. Remotely. Reliably. Without hand-holding.</p>
      <div class="hero-actions">
        <a href="mailto:Lesedi.malatsi@outlook.com" class="btn-green">Hire me now</a>
        <a href="#services" class="btn-outline">See what I do</a>
        <a href="https://linkedin.com/in/lesedi-malatsi-14905025a" target="_blank" rel="noopener" class="btn-outline">LinkedIn ↗</a>
      </div>
      <div class="hero-stats">
        <div class="hero-stat"><div class="hero-stat-num">10+</div><div class="hero-stat-label">Years experience</div></div>
        <div class="hero-stat"><div class="hero-stat-num">3+</div><div class="hero-stat-label">Years freelancing</div></div>
        <div class="hero-stat"><div class="hero-stat-num">5+</div><div class="hero-stat-label">Industries served</div></div>
        <div class="hero-stat"><div class="hero-stat-num">100%</div><div class="hero-stat-label">Remote ready</div></div>
      </div>
    </div>
    <div class="hero-logo-block">
      <img src="IMG_8738.jpeg" alt="Growtivo" onerror="this.style.display='none'">
      <div class="hero-avail">● Open to opportunities</div>
    </div>
  </div>
</section>

<!-- HIRE MODES STRIP -->
<div class="hire-strip">
  <div class="hire-strip-inner">
    <span class="hire-label">Hire me as</span>
    <div class="hire-pill">
      <span class="hire-pill-icon">🏢</span>
      <div><div class="hire-pill-title">Full team member</div><div class="hire-pill-sub">In-house or remote employee</div></div>
    </div>
    <div class="hire-pill">
      <span class="hire-pill-icon">🤝</span>
      <div><div class="hire-pill-title">Independent contractor</div><div class="hire-pill-sub">Flexible, project-based</div></div>
    </div>
    <div class="hire-pill">
      <span class="hire-pill-icon">🚀</span>
      <div><div class="hire-pill-title">Freelancer</div><div class="hire-pill-sub">One-off or retainer</div></div>
    </div>
  </div>
</div>

<!-- SERVICES -->
<section id="services">
  <div class="container">
    <p class="sec-tag">What I do</p>
    <h2 class="sec-head">Six ways I drive<br>your business forward</h2>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-num">01</div>
        <div class="service-icon">📱</div>
        <div class="service-title">Brand strategy</div>
        <div class="service-desc">LinkedIn, TikTok, Instagram, and Facebook setup plus content strategy that turns followers into clients and platforms into revenue channels.</div>
        <div class="service-tags"><span class="service-tag">LinkedIn</span><span class="service-tag">TikTok</span><span class="service-tag">Instagram</span></div>
      </div>
      <div class="service-card">
        <div class="service-num">02</div>
        <div class="service-icon">✍️</div>
        <div class="service-title">Storytelling & content</div>
        <div class="service-desc">Compelling brand stories, founder narratives, case studies, and social content that builds trust and drives action across every platform.</div>
        <div class="service-tags"><span class="service-tag">Copywriting</span><span class="service-tag">Content</span><span class="service-tag">Storytelling</span></div>
      </div>
      <div class="service-card">
        <div class="service-num">03</div>
        <div class="service-icon">🗂️</div>
        <div class="service-title">Virtual assistance</div>
        <div class="service-desc">Email and calendar management, CRM maintenance, document handling, scheduling, and the operational work that keeps everything running.</div>
        <div class="service-tags"><span class="service-tag">Admin</span><span class="service-tag">CRM</span><span class="service-tag">Operations</span></div>
      </div>
      <div class="service-card">
        <div class="service-num">04</div>
        <div class="service-icon">🎯</div>
        <div class="service-title">Lead generation</div>
        <div class="service-desc">Outbound outreach, LinkedIn prospecting, appointment setting, CRM pipeline management, and market research that fills your funnel.</div>
        <div class="service-tags"><span class="service-tag">Outreach</span><span class="service-tag">LinkedIn</span><span class="service-tag">Pipeline</span></div>
      </div>
      <div class="service-card">
        <div class="service-num">05</div>
        <div class="service-icon">🎧</div>
        <div class="service-title">Customer support</div>
        <div class="service-desc">Client communication, quality assurance monitoring, inquiry resolution, and customer experience improvements backed by real data.</div>
        <div class="service-tags"><span class="service-tag">QA</span><span class="service-tag">CX</span><span class="service-tag">Communication</span></div>
      </div>
      <div class="service-card">
        <div class="service-num">06</div>
        <div class="service-icon">📊</div>
        <div class="service-title">Business analysis</div>
        <div class="service-desc">Process improvement, requirements gathering, operational efficiency audits, and data-driven insights that inform smarter decisions.</div>
        <div class="service-tags"><span class="service-tag">Analysis</span><span class="service-tag">Process</span><span class="service-tag">Reporting</span></div>
      </div>
    </div>
  </div>
</section>

<!-- BRAND STRATEGY -->
<section id="brand">
  <div class="container">
    <p class="sec-tag">Brand strategy spotlight</p>
    <h2 class="sec-head">Where marketing meets<br>technology — and makes revenue</h2>
    <div class="brand-layout">
      <div>
        <p class="brand-body">Most businesses are brilliant at what they do. Where they leave money on the table is visibility. No LinkedIn means corporate buyers can't find you. No TikTok means the next generation of clients never discovers you. No storytelling means you're just another option — not the obvious choice.</p>
        <div class="brand-quote">"Every day without the right social presence is a day your competitors are reaching clients that should be yours."</div>
        <p class="brand-body">I identify the gaps, build the platforms, craft the stories, create the content, and track what converts. Commercial, not creative for its own sake.</p>
        <p style="font-size:12px;font-weight:700;text-transform:uppercase;letter-spacing:0.12em;color:rgba(255,255,255,0.4);margin-bottom:12px;margin-top:24px;">Platforms I work across</p>
        <div class="platforms-row">
          <span class="platform-chip">💼 LinkedIn</span>
          <span class="platform-chip">🎵 TikTok</span>
          <span class="platform-chip">📸 Instagram</span>
          <span class="platform-chip">📘 Facebook</span>
          <span class="platform-chip">🐦 X / Twitter</span>
          <span class="platform-chip">▶️ YouTube Shorts</span>
        </div>
      </div>
      <div>
        <p style="font-size:12px;font-weight:700;text-transform:uppercase;letter-spacing:0.12em;color:rgba(255,255,255,0.4);margin-bottom:16px;">Revenue gaps I close</p>
        <div class="gap-list">
          <div class="gap-row"><div class="gap-icon">🔍</div><div><div class="gap-title">No LinkedIn presence</div><div class="gap-desc">Corporate buyers, HR managers, and investors search LinkedIn first. Invisible there means invisible to your best clients.</div></div></div>
          <div class="gap-row"><div class="gap-icon">📱</div><div><div class="gap-title">No TikTok or Instagram Reels</div><div class="gap-desc">The UK and global market's fastest-growing discovery platforms. Property tours, day-in-the-life, and city content drive real bookings.</div></div></div>
          <div class="gap-row"><div class="gap-icon">✍️</div><div><div class="gap-title">No brand story</div><div class="gap-desc">Facts tell, stories sell. Without a compelling narrative, you're competing on price instead of value.</div></div></div>
          <div class="gap-row"><div class="gap-icon">⭐</div><div><div class="gap-title">Reviews not working for you</div><div class="gap-desc">A 4.9 rating sitting on one page. Amplified across platforms it becomes a conversion machine.</div></div></div>
          <div class="gap-row"><div class="gap-icon">👤</div><div><div class="gap-title">No founder personal brand</div><div class="gap-desc">People buy from people. Visible founders build trust faster and cheaper than any ad campaign.</div></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- WHY HIRE ME -->
<section id="why">
  <div class="container">
    <p class="sec-tag">Why hire me</p>
    <h2 class="sec-head">What hiring managers<br>actually get</h2>
    <div class="why-grid">
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Zero ramp-up time</div>
        <div class="why-card-body">10+ years across VA, brand strategy, lead gen, QA, and business analysis. I integrate fast, ask the right questions, and deliver from week one.</div>
      </div>
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Commercial thinking</div>
        <div class="why-card-body">Every task I do is tied to a business outcome. I don't post content for the sake of it or manage inboxes robotically — I ask what it needs to achieve and work backwards from there.</div>
      </div>
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Fully self-managed</div>
        <div class="why-card-body">Remote-native since 2022. No micromanaging needed. I manage my own pipeline, hit my own targets, and communicate proactively so you're never chasing me for updates.</div>
      </div>
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Multi-disciplinary</div>
        <div class="why-card-body">Brand strategy, virtual assistance, lead generation, customer support, and business analysis — in one person. Rare, and valuable for lean teams that need range.</div>
      </div>
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Passion-led results</div>
        <div class="why-card-body">I genuinely care about the businesses I work with. That comes through in the quality, the initiative, and the willingness to go beyond the job description when it matters.</div>
      </div>
      <div class="why-card">
        <div class="why-card-accent"></div>
        <div class="why-card-title">Flexible engagement</div>
        <div class="why-card-body">Full team member, independent contractor, or freelancer — whatever structure works best for your business and budget. Introductory rates available for first engagements.</div>
      </div>
    </div>
    <div class="hire-types">
      <div class="hire-type"><div class="hire-type-dot"></div>Available as a full team member</div>
      <div class="hire-type"><div class="hire-type-dot"></div>Available as an independent contractor</div>
      <div class="hire-type"><div class="hire-type-dot"></div>Available for freelance projects</div>
      <div class="hire-type"><div class="hire-type-dot"></div>Open to retainer arrangements</div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="container">
    <p class="sec-tag">Experience</p>
    <h2 class="sec-head">Ten years of showing up<br>and delivering results</h2>
    <div class="exp-timeline">
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2022 – Present</div><div class="exp-company">Remote · Freelance</div></div>
        <div><div class="exp-role">Virtual Assistant</div><ul class="exp-bullets"><li>Managed scheduling, email correspondence, and task workflows across multiple remote clients using ClickUp.</li><li>Maintained CRM systems, generated reports, and tracked pipeline progress with spreadsheet tools.</li><li>Collaborated with cross-functional teams via Slack, Zoom, and cloud platforms to improve workflow efficiency.</li></ul></div>
      </div>
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2022 – 2025</div><div class="exp-company">LDG Reliance</div></div>
        <div><div class="exp-role">Customer Service Representative — QA Support</div><ul class="exp-bullets"><li>Monitored calls, chats, and emails against KPIs including accuracy, empathy, and resolution rate.</li><li>Produced QA reports and operational insights using Microsoft Office and Google Workspace.</li><li>Enhanced customer experience through data-driven feedback and targeted support improvements.</li></ul></div>
      </div>
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2022 – 2025</div><div class="exp-company">Brand Guru Ltd & Web Leads</div></div>
        <div><div class="exp-role">Lead Generation Specialist</div><ul class="exp-bullets"><li>Managed outbound outreach and lead generation campaigns across multiple B2B clients.</li><li>Built and maintained CRM workflows and conducted market research to support customer acquisition.</li><li>Collaborated with teams to support and improve customer acquisition strategies.</li></ul></div>
      </div>
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2014 – 2015</div><div class="exp-company">Malatsi-Tefo Attorneys</div></div>
        <div><div class="exp-role">Marketing & IT Consultant</div><ul class="exp-bullets"><li>Developed outreach strategies, marketing materials, and business development opportunities.</li><li>Provided technical support for hardware, software, and desktop systems.</li></ul></div>
      </div>
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2010 – 2013</div><div class="exp-company">Nashua Mobile</div></div>
        <div><div class="exp-role">Junior Business Analyst</div><ul class="exp-bullets"><li>Gathered business requirements, identified process improvements, and supported UAT testing and user training.</li></ul></div>
      </div>
      <div class="exp-row">
        <div class="exp-meta"><div class="exp-period">2007 – 2010</div><div class="exp-company">Nashua Mobile</div></div>
        <div><div class="exp-role">Helpdesk Support</div><ul class="exp-bullets"><li>Provided technical support for devices, routers, and connectivity issues across diverse user base.</li></ul></div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="container">
    <p class="sec-tag">Skills & tools</p>
    <h2 class="sec-head">Built to work anywhere,<br>with anyone</h2>
    <div class="skills-grid">
      <div>
        <p class="skill-group-title">Core skills</p>
        <div class="skill-tags">
          <span class="skill-tag">Email management</span><span class="skill-tag">Calendar coordination</span><span class="skill-tag">CRM management</span><span class="skill-tag">Lead generation</span><span class="skill-tag">LinkedIn outreach</span><span class="skill-tag">Data entry</span><span class="skill-tag">QA monitoring</span><span class="skill-tag">Appointment setting</span><span class="skill-tag">Report generation</span>
        </div>
      </div>
      <div>
        <p class="skill-group-title">Brand & content</p>
        <div class="skill-tags">
          <span class="skill-tag">LinkedIn strategy</span><span class="skill-tag">TikTok content</span><span class="skill-tag">Instagram management</span><span class="skill-tag">Facebook</span><span class="skill-tag">Storytelling</span><span class="skill-tag">Content planning</span><span class="skill-tag">B2B outreach</span><span class="skill-tag">Social media audits</span><span class="skill-tag">Landlord acquisition</span>
        </div>
      </div>
      <div>
        <p class="skill-group-title">Tools & platforms</p>
        <div class="skill-tags">
          <span class="skill-tag">ClickUp</span> <span class="skill-tag">Github</span> <span class="skill-tag">Slack</span><span class="skill-tag">Zoom</span><span class="skill-tag">Microsoft Office</span><span class="skill-tag">Google Workspace</span><span class="skill-tag">CRM systems</span><span class="skill-tag">Canva</span>
        </div>
      </div>
      <div>
        <p class="skill-group-title">Strengths</p>
        <div class="skill-tags">
          <span class="skill-tag">Self-managed</span><span class="skill-tag">Remote-native</span><span class="skill-tag">Multitasking</span><span class="skill-tag">Problem solving</span><span class="skill-tag">Attention to detail</span><span class="skill-tag">Client communication</span><span class="skill-tag">Commercial thinking</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA -->
<section id="contact">
  <div class="container">
    <p class="sec-tag" style="justify-content:center;">Let's work together</p>
    <h2 class="cta-head">Ready to close the gaps <span>costing your business money?</span></h2>
    <p class="cta-sub">Introductory rates for first engagements. No agency overhead. Flexible engagement — hire me your way.</p>
    <a href="mailto:Lesedi.malatsi@outlook.com" class="btn-green" style="font-size:15px;padding:15px 36px;">Send me an email</a>
    <div class="cta-cards">
      <a class="cta-card" href="mailto:Lesedi.malatsi@outlook.com">
        <div class="cta-card-icon">✉️</div>
        <div><div class="cta-card-label">Email</div><div class="cta-card-val">Lesedi.malatsi@outlook.com</div></div>
      </a>
      <a class="cta-card" href="tel:+27680231839">
        <div class="cta-card-icon">📞</div>
        <div><div class="cta-card-label">Phone / WhatsApp</div><div class="cta-card-val">+27 68 023 1839</div></div>
      </a>
      <a class="cta-card" href="https://linkedin.com/in/lesedi-malatsi-14905025a" target="_blank" rel="noopener">
        <div class="cta-card-icon">💼</div>
        <div><div class="cta-card-label">LinkedIn</div><div class="cta-card-val">lesedi-malatsi-14905025a</div></div>
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-brand">
    <img src="IMG_8738.jpeg" alt="Growtivo" onerror="this.style.display='none'">
    <span class="footer-copy">Lesedi Malatsi · Brand Strategist & Virtual Assistant</span>
  </div>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#brand">Brand strategy</a>
    <a href="#experience">Experience</a>
    <a href="mailto:Lesedi.malatsi@outlook.com">Contact</a>
  </div>
  <span class="footer-copy">© 2026 All rights reserved</span>
</footer>

</body>
</html>
