<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sehrish Naz — Senior Talent Sourcer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ── Reset & base ─────────────────────────────────────────── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
:root {
  --ink:    #0D1117;
  --teal:   #0A7C7C;
  --teal2:  #0E9E9E;
  --teallt: #E6F7F7;
  --cream:  #F8F7F4;
  --white:  #FFFFFF;
  --mid:    #4A5568;
  --muted:  #718096;
  --border: #E2E8F0;
  --accent: #FF6B35;
  --fs-xl:  clamp(2.8rem, 7vw, 5.5rem);
  --fs-lg:  clamp(1.6rem, 3.5vw, 2.4rem);
  --fs-md:  clamp(1.1rem, 2vw, 1.3rem);
  --fs-sm:  0.95rem;
  --fs-xs:  0.8rem;
}
html { scroll-behavior: smooth; }
body { font-family: 'Inter', sans-serif; color: var(--ink); background: var(--white); line-height: 1.6; overflow-x: hidden; }
img { max-width: 100%; display: block; }
a { color: inherit; text-decoration: none; }

/* ── Nav ──────────────────────────────────────────────────── */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 100;
  display: flex; justify-content: space-between; align-items: center;
  padding: 1rem 5vw;
  background: rgba(255,255,255,0.92);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border);
}
.nav-logo { font-family: 'Syne', sans-serif; font-weight: 800; font-size: 1.1rem; color: var(--teal); letter-spacing: -0.02em; }
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a { font-size: var(--fs-xs); font-weight: 500; color: var(--mid); letter-spacing: 0.08em; text-transform: uppercase; transition: color 0.2s; }
.nav-links a:hover { color: var(--teal); }
.nav-cta { background: var(--teal); color: var(--white) !important; padding: 0.45rem 1.1rem; border-radius: 4px; }
.nav-cta:hover { background: var(--teal2); color: var(--white) !important; }

/* ── Hero ─────────────────────────────────────────────────── */
#hero {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  padding: 8rem 5vw 5rem;
  gap: 4rem;
  background: var(--ink);
  position: relative;
  overflow: hidden;
}
.hero-bg-text {
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Syne', sans-serif;
  font-size: clamp(8rem, 22vw, 20rem);
  font-weight: 800;
  color: rgba(255,255,255,0.025);
  white-space: nowrap;
  pointer-events: none;
  letter-spacing: -0.05em;
  user-select: none;
}
.hero-left { position: relative; z-index: 1; }
.hero-eyebrow {
  display: inline-flex; align-items: center; gap: 8px;
  font-size: var(--fs-xs); font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--teal2); margin-bottom: 1.5rem;
}
.hero-eyebrow::before { content: ''; width: 32px; height: 1px; background: var(--teal2); display: block; }
.hero-h1 {
  font-family: 'Syne', sans-serif;
  font-size: var(--fs-xl);
  font-weight: 800;
  color: var(--white);
  line-height: 1.0;
  letter-spacing: -0.03em;
  margin-bottom: 1.5rem;
}
.hero-h1 .accent { color: var(--teal2); }
.hero-sub { font-size: var(--fs-md); color: rgba(255,255,255,0.6); max-width: 480px; margin-bottom: 2.5rem; font-weight: 300; line-height: 1.7; }
.btn-group { display: flex; gap: 1rem; flex-wrap: wrap; }
.btn-primary {
  background: var(--teal2); color: var(--white);
  padding: 0.85rem 2rem; border-radius: 4px;
  font-size: var(--fs-sm); font-weight: 600;
  transition: background 0.2s, transform 0.2s;
  display: inline-block;
}
.btn-primary:hover { background: var(--teal); transform: translateY(-1px); }
.btn-ghost {
  border: 1px solid rgba(255,255,255,0.25); color: var(--white);
  padding: 0.85rem 2rem; border-radius: 4px;
  font-size: var(--fs-sm); font-weight: 500;
  transition: border-color 0.2s, background 0.2s;
  display: inline-block;
}
.btn-ghost:hover { border-color: var(--teal2); background: rgba(14,158,158,0.1); }
.hero-right { position: relative; z-index: 1; }
.stats-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 1px;
  background: rgba(255,255,255,0.08);
  border-radius: 12px; overflow: hidden;
}
.stat-box {
  background: rgba(255,255,255,0.04);
  padding: 2rem 1.5rem;
  transition: background 0.2s;
}
.stat-box:hover { background: rgba(14,158,158,0.12); }
.stat-num {
  font-family: 'Syne', sans-serif;
  font-size: clamp(2.5rem, 5vw, 3.8rem);
  font-weight: 800;
  color: var(--teal2);
  line-height: 1;
  margin-bottom: 0.5rem;
}
.stat-label { font-size: var(--fs-xs); color: rgba(255,255,255,0.5); font-weight: 400; letter-spacing: 0.04em; }
.stat-desc { font-size: var(--fs-xs); color: rgba(255,255,255,0.3); margin-top: 4px; }

/* ── Sections ─────────────────────────────────────────────── */
section { padding: 6rem 5vw; }
.section-eyebrow {
  font-size: var(--fs-xs); font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--teal); margin-bottom: 0.75rem;
  display: flex; align-items: center; gap: 8px;
}
.section-eyebrow::before { content: ''; width: 24px; height: 1px; background: var(--teal); display: block; }
.section-h2 {
  font-family: 'Syne', sans-serif;
  font-size: var(--fs-lg);
  font-weight: 700;
  color: var(--ink);
  letter-spacing: -0.02em;
  line-height: 1.15;
  margin-bottom: 1rem;
}
.section-sub { font-size: var(--fs-sm); color: var(--muted); max-width: 560px; line-height: 1.7; }

/* ── Process ──────────────────────────────────────────────── */
#process { background: var(--cream); }
.process-intro { max-width: 640px; margin-bottom: 3.5rem; }
.process-steps {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 0;
  position: relative;
}
.process-steps::before {
  content: '';
  position: absolute;
  top: 28px; left: 10%; right: 10%;
  height: 1px; background: var(--teal);
  opacity: 0.3; z-index: 0;
}
.process-step { text-align: center; position: relative; z-index: 1; padding: 0 0.5rem; }
.step-icon {
  width: 56px; height: 56px; border-radius: 50%;
  background: var(--white);
  border: 2px solid var(--teal);
  display: flex; align-items: center; justify-content: center;
  margin: 0 auto 1rem;
  font-size: 1.4rem;
  box-shadow: 0 0 0 6px var(--cream);
  transition: background 0.2s, transform 0.2s;
}
.process-step:hover .step-icon { background: var(--teal); transform: scale(1.1); }
.step-num { font-size: 9px; font-weight: 700; color: var(--teal); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 4px; }
.step-name { font-size: var(--fs-xs); font-weight: 600; color: var(--ink); margin-bottom: 4px; }
.step-desc { font-size: 11px; color: var(--muted); line-height: 1.5; }

/* ── Case Study ───────────────────────────────────────────── */
#casestudy { background: var(--white); }
.cs-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: start; margin-top: 3rem; }
.cs-left {}
.cs-tag {
  display: inline-block;
  background: var(--teallt); color: var(--teal);
  font-size: 11px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
  padding: 4px 12px; border-radius: 20px; margin-bottom: 1.5rem;
}
.cs-block { margin-bottom: 1.75rem; }
.cs-block-label { font-size: 11px; font-weight: 700; color: var(--muted); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 0.5rem; }
.cs-block-text { font-size: var(--fs-sm); color: var(--mid); line-height: 1.7; }
.boolean-box {
  background: var(--ink); border-radius: 8px;
  padding: 1rem 1.25rem;
  font-family: 'Courier New', monospace;
  font-size: 0.9rem; color: var(--teal2);
  letter-spacing: 0.02em;
  position: relative;
}
.boolean-box::before {
  content: 'boolean string';
  position: absolute; top: -10px; left: 12px;
  font-family: 'Inter', sans-serif; font-size: 10px; font-weight: 600;
  color: var(--muted); text-transform: uppercase; letter-spacing: 0.1em;
  background: var(--white); padding: 0 6px;
}
.channel-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 8px; }
.channel-tag {
  background: var(--teallt); color: var(--teal);
  font-size: 11px; font-weight: 500;
  padding: 4px 10px; border-radius: 4px;
}
.result-box {
  background: var(--teal); border-radius: 8px;
  padding: 1.5rem; color: var(--white);
  margin-top: 1rem;
}
.result-box .big { font-family: 'Syne', sans-serif; font-size: 2.5rem; font-weight: 800; line-height: 1; }
.result-box .label { font-size: var(--fs-xs); opacity: 0.75; margin-top: 4px; }
.result-box .note { font-size: var(--fs-xs); opacity: 0.6; margin-top: 0.75rem; }
.cs-right {}
.screenshot-frame {
  border-radius: 10px;
  overflow: hidden;
  border: 1px solid var(--border);
  box-shadow: 0 20px 60px rgba(0,0,0,0.1);
}
.browser-bar {
  background: #F1F1F1;
  padding: 8px 12px;
  display: flex; align-items: center; gap: 6px;
  border-bottom: 1px solid var(--border);
}
.dot { width: 10px; height: 10px; border-radius: 50%; }
.url-bar {
  flex: 1; background: var(--white);
  border-radius: 4px; padding: 3px 10px;
  font-size: 11px; color: var(--muted);
  border: 1px solid var(--border);
  margin-left: 8px;
}
.screenshot-img {
  width: 100%; display: block;
  background: #F8F9FA;
}
.outreach-card {
  background: var(--white);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 1.25rem;
  margin-top: 1.5rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.06);
}
.outreach-header { display: flex; align-items: center; gap: 10px; margin-bottom: 1rem; padding-bottom: 0.75rem; border-bottom: 1px solid var(--border); }
.avatar { width: 36px; height: 36px; border-radius: 50%; background: var(--teal); display: flex; align-items: center; justify-content: center; font-weight: 700; font-size: 14px; color: var(--white); flex-shrink: 0; }
.outreach-name { font-size: var(--fs-xs); font-weight: 600; color: var(--ink); }
.outreach-role { font-size: 11px; color: var(--muted); }
.outreach-body { font-size: var(--fs-xs); color: var(--mid); line-height: 1.7; }
.outreach-label { font-size: 10px; font-weight: 700; color: var(--teal); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 6px; }

/* ── Tools ────────────────────────────────────────────────── */
#tools { background: var(--cream); }
.tools-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-top: 3rem; }
.tool-category {
  background: var(--white);
  border-radius: 10px;
  padding: 1.75rem;
  border: 1px solid var(--border);
  transition: border-color 0.2s, box-shadow 0.2s;
}
.tool-category:hover { border-color: var(--teal); box-shadow: 0 8px 30px rgba(10,124,124,0.08); }
.tool-cat-icon { font-size: 1.8rem; margin-bottom: 1rem; }
.tool-cat-name { font-family: 'Syne', sans-serif; font-size: 1rem; font-weight: 700; color: var(--ink); margin-bottom: 1rem; }
.tool-list { list-style: none; }
.tool-list li {
  font-size: var(--fs-xs); color: var(--mid); padding: 5px 0;
  border-bottom: 1px solid var(--border);
  display: flex; align-items: center; gap: 8px;
}
.tool-list li:last-child { border-bottom: none; }
.tool-list li::before { content: '→'; color: var(--teal); font-size: 10px; flex-shrink: 0; }
.learning-strip {
  margin-top: 2rem;
  background: var(--ink);
  border-radius: 10px;
  padding: 1.5rem 2rem;
  display: flex; align-items: center; gap: 1.5rem; flex-wrap: wrap;
}
.learning-label { font-size: var(--fs-xs); font-weight: 700; color: var(--teal2); text-transform: uppercase; letter-spacing: 0.1em; white-space: nowrap; }
.learning-tags { display: flex; flex-wrap: wrap; gap: 8px; }
.learning-tag {
  background: rgba(14,158,158,0.15); color: var(--teal2);
  font-size: 11px; padding: 4px 12px; border-radius: 20px;
  border: 1px solid rgba(14,158,158,0.3);
}

/* ── Results ──────────────────────────────────────────────── */
#results { background: var(--ink); }
#results .section-eyebrow { color: var(--teal2); }
#results .section-eyebrow::before { background: var(--teal2); }
#results .section-h2 { color: var(--white); }
.results-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: rgba(255,255,255,0.06); border-radius: 12px; overflow: hidden; margin-top: 3rem; }
.result-card {
  background: rgba(255,255,255,0.03);
  padding: 2.5rem 1.5rem;
  text-align: center;
  transition: background 0.2s;
}
.result-card:hover { background: rgba(14,158,158,0.1); }
.result-num {
  font-family: 'Syne', sans-serif;
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 800; color: var(--teal2); line-height: 1; margin-bottom: 0.5rem;
}
.result-label { font-size: var(--fs-xs); color: rgba(255,255,255,0.5); font-weight: 500; margin-bottom: 0.5rem; }
.result-note { font-size: 11px; color: rgba(255,255,255,0.3); line-height: 1.5; }
.growth-bar { margin-top: 3rem; }
.growth-label { display: flex; justify-content: space-between; font-size: var(--fs-xs); color: rgba(255,255,255,0.5); margin-bottom: 8px; }
.growth-track { background: rgba(255,255,255,0.08); border-radius: 4px; height: 6px; overflow: hidden; }
.growth-fill { height: 100%; background: linear-gradient(90deg, var(--teal), var(--teal2)); border-radius: 4px; animation: grow 2s ease-out forwards; width: 0; }
@keyframes grow { to { width: 82%; } }
.growth-note { font-size: 11px; color: rgba(255,255,255,0.3); margin-top: 8px; }

/* ── Reviews ──────────────────────────────────────────────── */
#testimonial { background: var(--teallt); }
.reviews-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.25rem;
  margin-top: 3rem;
}
.review-card {
  background: var(--white);
  border-radius: 12px;
  padding: 1.5rem;
  border: 1px solid var(--border);
  display: flex; flex-direction: column; gap: 1rem;
  transition: box-shadow 0.2s, transform 0.2s;
}
.review-card:hover { box-shadow: 0 12px 40px rgba(10,124,124,0.1); transform: translateY(-2px); }
.review-card.featured { border-color: var(--teal); box-shadow: 0 8px 30px rgba(10,124,124,0.12); }
.review-stars { color: #F59E0B; font-size: 1rem; letter-spacing: 2px; }
.review-text { font-size: var(--fs-xs); color: var(--mid); line-height: 1.7; font-style: italic; flex: 1; }
.review-author { display: flex; align-items: center; gap: 10px; padding-top: 1rem; border-top: 1px solid var(--border); }
.review-flag { font-size: 1.4rem; }
.review-name { font-size: var(--fs-xs); font-weight: 600; color: var(--ink); }
.review-platform { font-size: 11px; color: var(--muted); margin-top: 2px; }
.reviews-footer { text-align: center; margin-top: 2rem; }
.fiverr-badge {
  display: inline-flex; align-items: center; gap: 12px;
  background: var(--white); border: 1px solid var(--border);
  border-radius: 8px; padding: 0.75rem 1.5rem;
  font-size: var(--fs-xs); color: var(--muted);
}
@media (max-width: 768px) { .reviews-grid { grid-template-columns: 1fr; } }

/* ── Testimonial (old, keep for compat) ───────────────────── */
#testimonial { background: var(--teallt); }
.testimonial-card {
  max-width: 720px; margin: 3rem auto 0;
  background: var(--white); border-radius: 16px;
  padding: 3rem; text-align: center;
  box-shadow: 0 20px 60px rgba(10,124,124,0.1);
  position: relative;
}
.quote-mark {
  font-family: 'Syne', sans-serif;
  font-size: 8rem; line-height: 0.6;
  color: var(--teallt); font-weight: 800;
  position: absolute; top: 1.5rem; left: 2rem;
  user-select: none;
}
.testimonial-text {
  font-size: var(--fs-md); color: var(--mid);
  font-style: italic; line-height: 1.7;
  position: relative; z-index: 1;
  margin-bottom: 2rem;
}
.testimonial-author { font-size: var(--fs-xs); font-weight: 600; color: var(--teal); text-transform: uppercase; letter-spacing: 0.1em; }
.stars { color: #F59E0B; font-size: 1.2rem; margin-bottom: 1.5rem; letter-spacing: 2px; }
.fiverr-note { font-size: 11px; color: var(--muted); margin-top: 4px; }

/* ── Contact ──────────────────────────────────────────────── */
#contact { background: var(--white); }
.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; margin-top: 3rem; }
.contact-left .section-h2 { margin-bottom: 1rem; }
.contact-detail {
  display: flex; align-items: flex-start; gap: 12px;
  padding: 1rem 0; border-bottom: 1px solid var(--border);
}
.contact-detail:last-of-type { border-bottom: none; }
.contact-icon { font-size: 1.2rem; flex-shrink: 0; margin-top: 2px; }
.contact-info { font-size: var(--fs-xs); color: var(--mid); }
.contact-info strong { display: block; font-size: var(--fs-sm); color: var(--ink); margin-bottom: 2px; }
.contact-right {
  background: var(--ink);
  border-radius: 16px; padding: 2.5rem;
}
.contact-right .section-eyebrow { color: var(--teal2); }
.contact-right .section-eyebrow::before { background: var(--teal2); }
.contact-right h3 { font-family: 'Syne', sans-serif; font-size: 1.4rem; font-weight: 700; color: var(--white); margin-bottom: 1rem; }
.contact-right p { font-size: var(--fs-sm); color: rgba(255,255,255,0.6); line-height: 1.7; margin-bottom: 2rem; }
.au-badge {
  display: inline-flex; align-items: center; gap: 8px;
  background: rgba(14,158,158,0.15); border: 1px solid rgba(14,158,158,0.3);
  border-radius: 6px; padding: 8px 14px;
  font-size: var(--fs-xs); color: var(--teal2); margin-bottom: 1.5rem;
}
.email-btn {
  display: block; width: 100%;
  background: var(--teal2); color: var(--white);
  padding: 1rem; border-radius: 6px;
  text-align: center; font-weight: 600; font-size: var(--fs-sm);
  transition: background 0.2s, transform 0.2s;
  margin-top: 1rem;
}
.email-btn:hover { background: var(--teal); transform: translateY(-1px); }

/* ── Footer ───────────────────────────────────────────────── */
footer {
  background: var(--ink); color: rgba(255,255,255,0.4);
  padding: 2rem 5vw;
  display: flex; justify-content: space-between; align-items: center;
  font-size: 12px; flex-wrap: wrap; gap: 1rem;
}
footer a { color: var(--teal2); }

/* ── Scroll reveal ────────────────────────────────────────── */
.reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.6s ease, transform 0.6s ease; }
.reveal.visible { opacity: 1; transform: none; }

/* ── Mobile ───────────────────────────────────────────────── */
@media (max-width: 768px) {
  #hero { grid-template-columns: 1fr; padding-top: 7rem; }
  .hero-right { display: none; }
  .process-steps { grid-template-columns: repeat(2, 1fr); gap: 1.5rem; }
  .process-steps::before { display: none; }
  .cs-grid, .contact-grid { grid-template-columns: 1fr; }
  .tools-grid { grid-template-columns: 1fr; }
  .results-grid { grid-template-columns: repeat(2, 1fr); }
  .nav-links { display: none; }
}
@media (prefers-reduced-motion: reduce) {
  .reveal { opacity: 1; transform: none; }
  .growth-fill { animation: none; width: 82%; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">SN</div>
  <ul class="nav-links">
    <li><a href="#process">Process</a></li>
    <li><a href="#casestudy">Case Study</a></li>
    <li><a href="#tools">Tools</a></li>
    <li><a href="#results">Results</a></li>
    <li><a href="#contact" class="nav-cta">Work with me</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-text">SOURCE</div>
  <div class="hero-left">
    <div class="hero-eyebrow">Senior Talent Sourcer</div>
    <h1 class="hero-h1">I find<br>the right<br><span class="accent">people.</span></h1>
    <p class="hero-sub">8+ years building candidate pipelines across Construction, Healthcare, Tech & Finance — for UK and Australian clients. Remote-first. Results-driven.</p>
    <div class="btn-group">
      <a href="#casestudy" class="btn-primary">See my work</a>
      <a href="#contact" class="btn-ghost">Work with me</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="stats-grid">
      <div class="stat-box">
        <div class="stat-num">460%</div>
        <div class="stat-label">Platform growth</div>
        <div class="stat-desc">10K → 56K users</div>
      </div>
      <div class="stat-box">
        <div class="stat-num">8+</div>
        <div class="stat-label">Years sourcing</div>
        <div class="stat-desc">Multi-sector experience</div>
      </div>
      <div class="stat-box">
        <div class="stat-num">4yr+</div>
        <div class="stat-label">Client retained</div>
        <div class="stat-desc">Long-term partnership</div>
      </div>
      <div class="stat-box">
        <div class="stat-num">6</div>
        <div class="stat-label">Industries</div>
        <div class="stat-desc">Construction to HealthTech</div>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section id="process">
  <div class="process-intro reveal">
    <div class="section-eyebrow">How I work</div>
    <h2 class="section-h2">A process that delivers quality, not just volume</h2>
    <p class="section-sub">Every search starts with understanding exactly what success looks like for your role — then I build the pipeline around that definition.</p>
  </div>
  <div class="process-steps reveal">
    <div class="process-step">
      <div class="step-icon">📋</div>
      <div class="step-num">01</div>
      <div class="step-name">Brief</div>
      <div class="step-desc">Role, sector, location, urgency — I understand before I search</div>
    </div>
    <div class="process-step">
      <div class="step-icon">🔍</div>
      <div class="step-num">02</div>
      <div class="step-name">Source</div>
      <div class="step-desc">Boolean strings, LinkedIn, job boards, social groups</div>
    </div>
    <div class="process-step">
      <div class="step-icon">💬</div>
      <div class="step-num">03</div>
      <div class="step-name">Engage</div>
      <div class="step-desc">Personalised outreach — messages that actually get replies</div>
    </div>
    <div class="process-step">
      <div class="step-icon">✅</div>
      <div class="step-num">04</div>
      <div class="step-name">Screen</div>
      <div class="step-desc">Availability, salary fit, experience — before you see anyone</div>
    </div>
    <div class="process-step">
      <div class="step-icon">📊</div>
      <div class="step-num">05</div>
      <div class="step-name">Present</div>
      <div class="step-desc">Clean shortlists with summaries, not raw lists</div>
    </div>
    <div class="process-step">
      <div class="step-icon">🎯</div>
      <div class="step-num">06</div>
      <div class="step-name">Submit</div>
      <div class="step-desc">Deliver shortlisted candidates to hiring manager, ready for interview</div>
    </div>
  </div>
</section>

<!-- CASE STUDY -->
<section id="casestudy">
  <div class="reveal">
    <div class="section-eyebrow">Case study</div>
    <h2 class="section-h2">Sourcing in action:<br>CPCS Telehandler — UK Construction</h2>
  </div>
  <div class="cs-grid">
    <div class="cs-left reveal">
      <span class="cs-tag">Construction · UK · LinkedIn Sourcing</span>

      <div class="cs-block">
        <div class="cs-block-label">The brief</div>
        <div class="cs-block-text">Client needed certified CPCS Telehandler operators for a project in Morpeth, UK. Requirement: active operators within commuting distance, open to short-term contracts. Urgency: same-week pipeline needed.</div>
      </div>

      <div class="cs-block">
        <div class="cs-block-label">Boolean search string</div>
        <div class="boolean-box">(Telehandler OR "Tele-handler" OR "Tele handler")</div>
      </div>

      <div class="cs-block">
        <div class="cs-block-label">Filters applied</div>
        <div class="cs-block-text">Location: Morpeth & Newcastle upon Tyne · Keywords: Telehandler · Seniority: mid-level · Current companies filter applied</div>
      </div>

      <div class="cs-block">
        <div class="cs-block-label">Channels used</div>
        <div class="channel-tags">
          <span class="channel-tag">LinkedIn People Search</span>
          <span class="channel-tag">Facebook construction groups</span>
          <span class="channel-tag">WhatsApp trade networks</span>
          <span class="channel-tag">Recruitment app database</span>
        </div>
      </div>

      <div class="result-box">
        <div class="big">3</div>
        <div class="label">Qualified candidates registered on app — in 1 day</div>
        <div class="note">Active pipeline maintained for future Telehandler requirements across North East UK</div>
      </div>
    </div>

    <div class="cs-right reveal">
      <div class="screenshot-frame">
        <div class="browser-bar">
          <div class="dot" style="background:#FF5F56"></div>
          <div class="dot" style="background:#FFBD2E"></div>
          <div class="dot" style="background:#27C93F"></div>
          <div class="url-bar">linkedin.com/search/results/people</div>
        </div>
        <div style="background:#F3F2EF; padding: 1rem;">
          <div style="background:white; border-radius:8px; padding:1rem; font-size:12px; font-family:sans-serif; border:1px solid #e0e0e0;">
            <div style="background:#0A66C2; border-radius:6px; padding:8px 12px; color:white; font-size:11px; margin-bottom:12px; display:flex; align-items:center; gap:8px;">
              <span style="font-size:16px;">in</span>
              <span style="flex:1; background:rgba(255,255,255,0.15); padding:4px 8px; border-radius:4px; color:white;">🔍 (Telehandler OR "Tele-handler" OR "Tele handler")</span>
            </div>
            <div style="display:flex; gap:6px; flex-wrap:wrap; margin-bottom:12px;">
              <span style="background:#0A66C2; color:white; border-radius:16px; padding:3px 10px; font-size:10px; font-weight:600;">People ▾</span>
              <span style="border:1px solid #0A66C2; color:#0A66C2; border-radius:16px; padding:3px 10px; font-size:10px;">1st</span>
              <span style="border:1px solid #0A66C2; color:#0A66C2; border-radius:16px; padding:3px 10px; font-size:10px;">2nd</span>
              <span style="border:1px solid #ccc; color:#444; border-radius:16px; padding:3px 10px; font-size:10px;">📍 2 Locations ▾</span>
              <span style="border:1px solid #ccc; color:#444; border-radius:16px; padding:3px 10px; font-size:10px;">🔑 1 Keyword ▾</span>
            </div>
            <div style="border-bottom:1px solid #eee; padding-bottom:10px; margin-bottom:10px;">
              <div style="display:flex; align-items:center; gap:10px; margin-bottom:8px;">
                <div style="width:36px; height:36px; border-radius:50%; background:#ccc; flex-shrink:0;"></div>
                <div>
                  <div style="font-weight:600; color:#333; font-size:12px;">Terry Bailey · 1st</div>
                  <div style="color:#666; font-size:11px;">Telehandler at For Merit</div>
                  <div style="color:#888; font-size:10px;">📍 Newcastle Upon Tyne, England</div>
                </div>
                <div style="margin-left:auto; border:1px solid #0A66C2; color:#0A66C2; border-radius:16px; padding:4px 12px; font-size:10px; font-weight:600;">✉ Message</div>
              </div>
              <div style="display:flex; align-items:center; gap:10px;">
                <div style="width:36px; height:36px; border-radius:50%; background:#aaa; flex-shrink:0;"></div>
                <div>
                  <div style="font-weight:600; color:#333; font-size:12px;">Les Pattinson · 1st</div>
                  <div style="color:#666; font-size:11px;">Telehandler at TEXO Recruitment</div>
                  <div style="color:#888; font-size:10px;">📍 Newcastle Upon Tyne, England</div>
                </div>
                <div style="margin-left:auto; border:1px solid #0A66C2; color:#0A66C2; border-radius:16px; padding:4px 12px; font-size:10px; font-weight:600;">✉ Message</div>
              </div>
            </div>
            <div style="font-size:10px; color:#888; text-align:center;">Showing results for Morpeth · Newcastle upon Tyne</div>
          </div>
        </div>
      </div>

      <div class="outreach-card">
        <div class="outreach-label">Outreach message sent</div>
        <div class="outreach-header">
          <div class="avatar">SN</div>
          <div>
            <div class="outreach-name">Sehrish Naz</div>
            <div class="outreach-role">Talent Sourcer · Construction Recruitment</div>
          </div>
        </div>
        <div class="outreach-body">
          Hi [Name], hope you're doing well! Our client is currently looking for experienced candidates like yourself for a <strong>CPCS Telehandler</strong> position in Morpeth, UK. Would you be open to a quick chat?<br><br>
          We post new roles daily through our recruitment app — I'd love to keep you in the loop for future positions. Registration is completely free.<br><br>
          Happy to jump on a call at your convenience — these roles move quickly and we'd love to have you as a strong fit in our talent pool. Looking forward to hearing from you!
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TOOLS -->
<section id="tools">
  <div class="reveal">
    <div class="section-eyebrow">Toolkit</div>
    <h2 class="section-h2">The tools behind the results</h2>
    <p class="section-sub">Not just listed — actively used in real client projects across UK and international markets.</p>
  </div>
  <div class="tools-grid reveal">
    <div class="tool-category">
      <div class="tool-cat-icon">🎯</div>
      <div class="tool-cat-name">Sourcing</div>
      <ul class="tool-list">
        <li>LinkedIn Recruiter & People Search</li>
        <li>Advanced Boolean search strings</li>
        <li>Indeed & Seek.com.au</li>
        <li>Facebook Groups & WhatsApp networks</li>
        <li>GitHub candidate sourcing</li>
        <li>Job board strategy & optimisation</li>
      </ul>
    </div>
    <div class="tool-category">
      <div class="tool-cat-icon">🗂️</div>
      <div class="tool-cat-name">Candidate Management</div>
      <ul class="tool-list">
        <li>ATS platforms (Greenhouse, Bullhorn)</li>
        <li>CRM & database management</li>
        <li>Pipeline tracking & reporting</li>
        <li>Jobadder (Australian market)</li>
        <li>Candidate shortlisting & summaries</li>
        <li>Onboarding & database registration</li>
      </ul>
    </div>
    <div class="tool-category">
      <div class="tool-cat-icon">💬</div>
      <div class="tool-cat-name">Communication</div>
      <ul class="tool-list">
        <li>LinkedIn InMail & messaging</li>
        <li>Email outreach campaigns</li>
        <li>WhatsApp Business</li>
        <li>Microsoft Teams & Slack</li>
        <li>Zoom video interviewing</li>
        <li>Microsoft Office & Google Workspace</li>
      </ul>
    </div>
  </div>
  <div class="learning-strip reveal">
    <div class="learning-label">Currently building →</div>
    <div class="learning-tags">
      <span class="learning-tag">Power BI</span>
      <span class="learning-tag">SQL for HR Analytics</span>
      <span class="learning-tag">SeekOut AI sourcing</span>
      <span class="learning-tag">Phenom People</span>
      <span class="learning-tag">People Analytics</span>
      <span class="learning-tag">AU Market Intelligence</span>
    </div>
  </div>
</section>

<!-- RESULTS -->
<section id="results">
  <div class="reveal">
    <div class="section-eyebrow">Track record</div>
    <h2 class="section-h2">Numbers that matter</h2>
  </div>
  <div class="results-grid reveal">
    <div class="result-card">
      <div class="result-num">460%</div>
      <div class="result-label">Platform user growth</div>
      <div class="result-note">Grew recruitment app from 10K to 56K+ active users over 4 years</div>
    </div>
    <div class="result-card">
      <div class="result-num">4yr+</div>
      <div class="result-label">Client retained</div>
      <div class="result-note">First project converted to a 4+ year exclusive long-term partnership</div>
    </div>
    <div class="result-card">
      <div class="result-num">8+</div>
      <div class="result-label">Years of experience</div>
      <div class="result-note">Consistent delivery across agency, in-house and platform recruitment</div>
    </div>
    <div class="result-card">
      <div class="result-num">6</div>
      <div class="result-label">Industries sourced</div>
      <div class="result-note">Construction · Healthcare · IT · Finance · Retail · Automotive</div>
    </div>
  </div>
  <div class="growth-bar reveal">
    <div class="growth-label">
      <span>App user growth · 4 years</span>
      <span>10K → 56K users</span>
    </div>
    <div class="growth-track"><div class="growth-fill"></div></div>
    <div class="growth-note">460% growth through targeted sourcing, outreach campaigns, and candidate engagement strategy</div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonial">
  <div class="reveal" style="text-align:center;">
    <div class="section-eyebrow" style="justify-content:center;">Client reviews</div>
    <h2 class="section-h2">What clients say</h2>
    <p class="section-sub" style="margin:0 auto; text-align:center;">Real reviews from clients across Pakistan, United States, Romania, Netherlands & more</p>
  </div>

  <div class="reviews-grid reveal">
    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Working with Sehar was a fantastic experience. She provided clear instructions and was always available for feedback, making the project smooth and enjoyable. Looking forward to collaborating again in the future!"</p>
      <div class="review-author">
        <div class="review-flag">🇵🇰</div>
        <div>
          <div class="review-name">Client from Pakistan</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>

    <div class="review-card featured">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Wanted someone to find open jobs that would be a great match for some of our candidates. Sehrish did a really great job! She had excellent attention to detail and was great to work with. Found great jobs for our candidates and was a valuable asset to the team, for our outreach and candidate marketing efforts. Thanks so much, Sehrish."</p>
      <div class="review-author">
        <div class="review-flag">🇺🇸</div>
        <div>
          <div class="review-name">Client from United States</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Good leads, match the requirements. Happy to work with."</p>
      <div class="review-author">
        <div class="review-flag">🇷🇴</div>
        <div>
          <div class="review-name">Client from Romania</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Nice seller!!!!"</p>
      <div class="review-author">
        <div class="review-flag">🇺🇸</div>
        <div>
          <div class="review-name">Client from United States</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Good sourcing skills! Super Sourcer!"</p>
      <div class="review-author">
        <div class="review-flag">🇳🇱</div>
        <div>
          <div class="review-name">Client from Netherlands</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Delivered order professionally."</p>
      <div class="review-author">
        <div class="review-flag">🇵🇰</div>
        <div>
          <div class="review-name">Client from Pakistan</div>
          <div class="review-platform">Fiverr · 5★ verified</div>
        </div>
      </div>
    </div>
  </div>

  <div class="reviews-footer reveal">
    <div class="fiverr-badge">
      <span style="color:#1dbf73; font-weight:700; font-size:1.1rem;">fiverr</span>
      <span>4.6★ overall rating · Multiple international clients · Sourcing specialist gig</span>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-grid">
    <div class="contact-left reveal">
      <div class="section-eyebrow">Get in touch</div>
      <h2 class="section-h2">Open to Australian remote roles — right now.</h2>
      <p class="section-sub" style="margin-bottom:2rem;">Looking for a Talent Sourcer or Recruitment Research Specialist who delivers quality pipelines remotely? Let's talk.</p>

      <div class="contact-detail">
        <div class="contact-icon">🌏</div>
        <div class="contact-info">
          <strong>Location</strong>
          Islamabad, Pakistan · Available for fully remote roles
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-icon">🕐</div>
        <div class="contact-info">
          <strong>Australian hours availability</strong>
          Available from 8AM AEST — full overlap with AU business hours
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-icon">💼</div>
        <div class="contact-info">
          <strong>LinkedIn</strong>
          <a href="#" style="color:var(--teal);">linkedin.com/in/sehrish-naz</a>
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-icon">📄</div>
        <div class="contact-info">
          <strong>Portfolio & CV</strong>
          <a href="https://seharn.my.canva.site/recruitment" style="color:var(--teal);">seharn.my.canva.site/recruitment</a>
        </div>
      </div>
    </div>

    <div class="contact-right reveal">
      <div class="section-eyebrow">For Australian employers</div>
      <h3>Why hire remotely from Pakistan?</h3>
      <p>Pakistan Standard Time is only 5 hours behind AEST — meaning I can comfortably work during your core afternoon business hours with no late-night calls required on either side.</p>
      <div class="au-badge">
        🇦🇺 &nbsp; Familiar with seek.com.au · Jobadder · Fair Work basics · AU salary benchmarks
      </div>
      <a href="mailto:your-email@gmail.com" class="email-btn">📧 Send me a message</a>
      <a href="Sehrish_Naz_CV_Australia.docx" class="email-btn" style="background:transparent; border:1px solid rgba(255,255,255,0.2); margin-top:0.75rem;">📄 Download my CV</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div>© 2026 Sehrish Naz · Senior Talent Sourcer</div>
  <div>Built for Australian remote recruitment roles · <a href="https://seharn.my.canva.site/recruitment">Canva Portfolio</a></div>
</footer>

<script>
// Scroll reveal
const observer = new IntersectionObserver((entries) => {
  entries.forEach(el => { if (el.isIntersecting) { el.target.classList.add('visible'); } });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// Animate growth bar when visible
const bar = document.querySelector('.growth-fill');
const barObserver = new IntersectionObserver((entries) => {
  entries.forEach(el => { if (el.isIntersecting) bar.style.animationPlayState = 'running'; });
}, { threshold: 0.5 });
if (bar) barObserver.observe(bar);
</script>
</body>
</html>
