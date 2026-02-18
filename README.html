<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>El Habib — AI Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,300;0,400;0,700;1,300&family=Syne:wght@400;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #050508;
    --bg2: #090912;
    --surface: #0e0e1a;
    --border: #1a1a2e;
    --accent: #00ffc3;
    --accent2: #7b5ea7;
    --accent3: #ff6b35;
    --text: #c8ccd4;
    --text-dim: #4a4d5e;
    --glow: rgba(0,255,195,0.15);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--accent);
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    mix-blend-mode: screen;
    transition: transform 0.1s;
    box-shadow: 0 0 20px var(--accent), 0 0 40px var(--glow);
  }
  .cursor-ring {
    width: 36px; height: 36px;
    border-radius: 50%;
    border: 1px solid rgba(0,255,195,0.4);
    position: fixed;
    pointer-events: none;
    z-index: 9998;
    transition: all 0.15s ease-out;
    transform: translate(-50%, -50%);
  }

  /* Canvas background */
  canvas#bg { position: fixed; inset: 0; z-index: 0; opacity: 0.35; }

  /* Noise overlay */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none; z-index: 1;
    opacity: 0.5;
  }

  .wrapper { position: relative; z-index: 2; max-width: 900px; margin: 0 auto; padding: 0 24px; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 0 60px;
    position: relative;
  }

  .hero-tag {
    font-size: 11px;
    letter-spacing: 0.25em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 24px;
    opacity: 0;
    animation: fadeUp 0.6s 0.3s forwards;
  }
  .hero-tag::before { content: '> '; opacity: 0.5; }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: clamp(52px, 9vw, 96px);
    line-height: 0.95;
    letter-spacing: -0.03em;
    margin-bottom: 8px;
    opacity: 0;
    animation: fadeUp 0.7s 0.5s forwards;
  }
  .hero-name .line1 { display: block; color: #fff; }
  .hero-name .line2 {
    display: block;
    color: transparent;
    -webkit-text-stroke: 1px rgba(255,255,255,0.2);
  }

  .hero-title {
    font-size: 13px;
    letter-spacing: 0.12em;
    color: var(--text-dim);
    margin-top: 28px;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.7s 0.7s forwards;
  }
  .hero-title span { color: var(--accent); margin: 0 8px; }
  .hero-title span:first-child { margin-left: 0; }

  .hero-bio {
    max-width: 520px;
    font-size: 14px;
    line-height: 1.85;
    color: var(--text-dim);
    opacity: 0;
    animation: fadeUp 0.7s 0.9s forwards;
    border-left: 2px solid var(--border);
    padding-left: 20px;
  }
  .hero-bio strong { color: var(--text); font-weight: 400; }

  .hero-cta {
    display: flex; gap: 12px;
    margin-top: 48px;
    opacity: 0;
    animation: fadeUp 0.7s 1.1s forwards;
  }
  .btn {
    padding: 10px 22px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    border: none;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.25s;
  }
  .btn-primary {
    background: var(--accent);
    color: #000;
    font-weight: 700;
  }
  .btn-primary:hover {
    box-shadow: 0 0 30px var(--glow), 0 0 60px rgba(0,255,195,0.08);
    transform: translateY(-2px);
  }
  .btn-ghost {
    background: transparent;
    color: var(--text-dim);
    border: 1px solid var(--border);
  }
  .btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

  .location-pill {
    position: absolute; top: 32px; right: 0;
    font-size: 10px; letter-spacing: 0.2em;
    color: var(--text-dim); text-transform: uppercase;
    display: flex; align-items: center; gap: 6px;
    opacity: 0; animation: fadeIn 1s 1.5s forwards;
  }
  .location-pill::before {
    content: '';
    width: 6px; height: 6px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 8px var(--accent);
    animation: pulse 2s infinite;
  }

  /* ── DIVIDER ── */
  .section-divider {
    display: flex; align-items: center; gap: 16px;
    margin: 80px 0 48px;
    font-size: 10px; letter-spacing: 0.3em; color: var(--text-dim);
    text-transform: uppercase;
  }
  .section-divider::before, .section-divider::after {
    content: ''; flex: 1; height: 1px;
    background: linear-gradient(90deg, transparent, var(--border));
  }
  .section-divider::after { background: linear-gradient(90deg, var(--border), transparent); }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    overflow: hidden;
  }

  .skill-cell {
    background: var(--bg2);
    padding: 28px 24px;
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
  }
  .skill-cell:hover { background: var(--surface); }
  .skill-cell:hover .skill-bar-fill { animation: fillBar 0.8s ease forwards; }

  .skill-cell::after {
    content: attr(data-num);
    position: absolute; bottom: 16px; right: 20px;
    font-size: 40px; font-weight: 800; font-family: 'Syne', sans-serif;
    color: var(--border);
    line-height: 1;
    transition: color 0.3s;
  }
  .skill-cell:hover::after { color: rgba(0,255,195,0.06); }

  .skill-label {
    font-size: 9px; letter-spacing: 0.25em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 10px;
  }
  .skill-name {
    font-family: 'Syne', sans-serif;
    font-size: 18px; font-weight: 700;
    color: #fff; margin-bottom: 14px;
    line-height: 1.2;
  }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }
  .tag {
    font-size: 9px; letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 3px 8px;
    border: 1px solid var(--border);
    color: var(--text-dim);
    transition: all 0.2s;
  }
  .skill-cell:hover .tag { border-color: rgba(0,255,195,0.2); color: var(--text); }

  /* ── PROJECTS ── */
  .projects { display: flex; flex-direction: column; gap: 2px; }

  .project-row {
    display: grid;
    grid-template-columns: 60px 1fr auto;
    align-items: center;
    gap: 0;
    background: var(--bg2);
    border: 1px solid transparent;
    padding: 24px 28px;
    text-decoration: none;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, background 0.3s;
    cursor: none;
  }
  .project-row::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--accent);
    transform: scaleY(0);
    transition: transform 0.3s;
    transform-origin: bottom;
  }
  .project-row:hover { background: var(--surface); border-color: var(--border); }
  .project-row:hover::before { transform: scaleY(1); }

  .project-num {
    font-size: 11px; color: var(--text-dim);
    font-weight: 300; letter-spacing: 0.05em;
  }
  .project-info { padding-left: 8px; }
  .project-title {
    font-family: 'Syne', sans-serif;
    font-size: 17px; font-weight: 700;
    color: #fff; margin-bottom: 4px;
    transition: color 0.2s;
  }
  .project-row:hover .project-title { color: var(--accent); }
  .project-desc { font-size: 12px; color: var(--text-dim); line-height: 1.5; }
  .project-stack {
    display: flex; gap: 8px; align-items: center;
    font-size: 10px; color: var(--text-dim);
    letter-spacing: 0.1em; text-transform: uppercase;
    flex-shrink: 0;
  }
  .project-stack .dot {
    width: 4px; height: 4px; border-radius: 50%;
    background: var(--accent2);
  }

  /* ── STATS BAR ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    margin: 0;
  }
  .stat-cell {
    background: var(--bg2);
    padding: 32px 24px;
    text-align: center;
    transition: background 0.3s;
  }
  .stat-cell:hover { background: var(--surface); }
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 36px; font-weight: 800;
    color: #fff;
    display: block;
    line-height: 1;
    margin-bottom: 8px;
  }
  .stat-num span { color: var(--accent); }
  .stat-label {
    font-size: 9px; letter-spacing: 0.25em;
    text-transform: uppercase; color: var(--text-dim);
  }

  /* ── TERMINAL BLOCK ── */
  .terminal {
    background: var(--surface);
    border: 1px solid var(--border);
    overflow: hidden;
    margin-bottom: 2px;
  }
  .terminal-bar {
    background: #111120;
    padding: 10px 16px;
    display: flex; align-items: center; gap: 8px;
    border-bottom: 1px solid var(--border);
  }
  .terminal-dot {
    width: 10px; height: 10px; border-radius: 50%;
  }
  .terminal-body {
    padding: 24px 28px;
    font-size: 13px; line-height: 2;
    color: var(--text-dim);
  }
  .terminal-body .cmd { color: var(--accent); }
  .terminal-body .comment { color: var(--text-dim); opacity: 0.5; }
  .terminal-body .str { color: #ffcc66; }
  .terminal-body .kw { color: var(--accent2); font-style: italic; }
  .terminal-body .fn { color: #56b6c2; }
  .caret {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--accent);
    vertical-align: text-bottom;
    animation: blink 1s step-end infinite;
    margin-left: 2px;
  }

  /* ── FOOTER ── */
  footer {
    margin-top: 120px;
    padding: 48px 0;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 11px;
    color: var(--text-dim);
    letter-spacing: 0.1em;
  }
  .connect-links { display: flex; gap: 24px; }
  .connect-links a {
    color: var(--text-dim); text-decoration: none;
    letter-spacing: 0.15em; font-size: 10px; text-transform: uppercase;
    transition: color 0.2s;
  }
  .connect-links a:hover { color: var(--accent); }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeIn {
    from { opacity: 0; } to { opacity: 1; }
  }
  @keyframes blink {
    50% { opacity: 0; }
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.7); }
  }
  @keyframes fillBar {
    from { width: 0; } to { width: var(--w); }
  }

  /* Scroll reveal */
  .reveal {
    opacity: 0; transform: translateY(24px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: none; }

  @media (max-width: 640px) {
    .skills-grid { grid-template-columns: 1fr; }
    .stats-row { grid-template-columns: repeat(2, 1fr); }
    .project-row { grid-template-columns: 40px 1fr; }
    .project-stack { display: none; }
    footer { flex-direction: column; gap: 24px; text-align: center; }
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>
<canvas id="bg"></canvas>

<div class="wrapper">

  <!-- HERO -->
  <section class="hero">
    <div class="location-pill">Morocco — MAR &nbsp;·&nbsp; Open to Remote</div>
    <p class="hero-tag">AI Engineer · Full-Stack · Game Dev</p>
    <h1 class="hero-name">
      <span class="line1">El Habib</span>
      <span class="line2">Mousse</span>
    </h1>
    <p class="hero-title">
      <span>AI Agents</span>·
      <span>Deep Learning</span>·
      <span>SaaS Products</span>
    </p>
    <p class="hero-bio">
      I build <strong>AI-powered systems</strong> that solve real business problems —
      from warehouse automation to custom OCR pipelines and speech models.
      Obsessed with turning research into <strong>products that ship</strong>.
    </p>
    <div class="hero-cta">
      <a href="mailto:your@email.com" class="btn btn-primary">Get in touch</a>
      <a href="https://github.com/elhabib-bit" class="btn btn-ghost">GitHub ↗</a>
    </div>
  </section>

  <!-- TERMINAL -->
  <div class="reveal terminal">
    <div class="terminal-bar">
      <div class="terminal-dot" style="background:#ff5f57"></div>
      <div class="terminal-dot" style="background:#febc2e"></div>
      <div class="terminal-dot" style="background:#28c840"></div>
      <span style="font-size:10px;color:#333;margin-left:8px;letter-spacing:0.1em">elhabib@ai-lab ~ </span>
    </div>
    <div class="terminal-body">
      <div><span class="cmd">$</span> python engineer.py <span class="comment">--mode=build</span></div>
      <div style="margin-top:6px">
        <span class="kw">class</span> <span class="fn">ElHabib</span>(<span class="fn">AIEngineer</span>):
      </div>
      <div style="padding-left:24px"><span class="kw">focus</span> = [<span class="str">"AI Agents"</span>, <span class="str">"OCR Systems"</span>, <span class="str">"Warehouse SaaS"</span>]</div>
      <div style="padding-left:24px"><span class="kw">stack</span> = [<span class="str">"PyTorch"</span>, <span class="str">"React"</span>, <span class="str">"Flutter"</span>, <span class="str">"Docker"</span>]</div>
      <div style="padding-left:24px"><span class="kw">currently_building</span> = <span class="str">"AI-powered Warehouse SaaS 🚀"</span></div>
      <div style="padding-left:24px"><span class="fn">print</span>(<span class="str">"Always building. Always shipping."</span>)</div>
      <div style="margin-top:8px"><span class="cmd">$</span> <span class="caret"></span></div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section-divider reveal">Tech Stack</div>

  <div class="skills-grid reveal">
    <div class="skill-cell" data-num="01">
      <div class="skill-label">Core</div>
      <div class="skill-name">AI &<br>Deep Learning</div>
      <div class="skill-tags">
        <span class="tag">PyTorch</span>
        <span class="tag">TensorFlow</span>
        <span class="tag">NLP</span>
        <span class="tag">Computer Vision</span>
        <span class="tag">RL</span>
      </div>
    </div>
    <div class="skill-cell" data-num="02">
      <div class="skill-label">Frontend</div>
      <div class="skill-name">Web &<br>Mobile</div>
      <div class="skill-tags">
        <span class="tag">React</span>
        <span class="tag">TypeScript</span>
        <span class="tag">Vite</span>
        <span class="tag">Flutter</span>
        <span class="tag">REST APIs</span>
      </div>
    </div>
    <div class="skill-cell" data-num="03">
      <div class="skill-label">Infrastructure</div>
      <div class="skill-name">Tools &<br>DevOps</div>
      <div class="skill-tags">
        <span class="tag">Docker</span>
        <span class="tag">Git</span>
        <span class="tag">Firebase</span>
        <span class="tag">Supabase</span>
        <span class="tag">Unity ML</span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-row reveal" style="margin-top:2px">
    <div class="stat-cell">
      <span class="stat-num">3<span>+</span></span>
      <span class="stat-label">Years Building</span>
    </div>
    <div class="stat-cell">
      <span class="stat-num">12<span>+</span></span>
      <span class="stat-label">AI Projects</span>
    </div>
    <div class="stat-cell">
      <span class="stat-num">5<span>+</span></span>
      <span class="stat-label">Tech Domains</span>
    </div>
    <div class="stat-cell">
      <span class="stat-num">∞</span>
      <span class="stat-label">Things to Build</span>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section-divider reveal">Featured Projects</div>

  <div class="projects reveal">
    <a href="#" class="project-row">
      <span class="project-num">01</span>
      <div class="project-info">
        <div class="project-title">AI Warehouse System</div>
        <div class="project-desc">Smart inventory optimization & automation using AI agents. Real-time decisions at scale.</div>
      </div>
      <div class="project-stack">
        <span class="dot"></span>
        <span>Python</span>
        <span>·</span>
        <span>React</span>
        <span>·</span>
        <span>AI</span>
      </div>
    </a>

    <a href="#" class="project-row">
      <span class="project-num">02</span>
      <div class="project-info">
        <div class="project-title">Custom OCR Engine</div>
        <div class="project-desc">End-to-end OCR pipeline trained from scratch. Handles complex Arabic & Latin scripts.</div>
      </div>
      <div class="project-stack">
        <span class="dot" style="background:var(--accent3)"></span>
        <span>PyTorch</span>
        <span>·</span>
        <span>CV</span>
      </div>
    </a>

    <a href="#" class="project-row">
      <span class="project-num">03</span>
      <div class="project-info">
        <div class="project-title">Speech → Subtitle Model</div>
        <div class="project-desc">Automatic subtitle generation from raw audio. Sub-500ms inference latency.</div>
      </div>
      <div class="project-stack">
        <span class="dot" style="background:#56b6c2"></span>
        <span>Deep Learning</span>
        <span>·</span>
        <span>NLP</span>
      </div>
    </a>
  </div>

  <!-- FOOTER -->
  <footer class="reveal">
    <span>⭐ Always building. Always shipping.</span>
    <div class="connect-links">
      <a href="#">LinkedIn</a>
      <a href="https://github.com/elhabib-bit">GitHub</a>
      <a href="#">Portfolio</a>
      <a href="mailto:your@email.com">Email</a>
    </div>
  </footer>

</div>

<script>
// ── Cursor
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursorRing');
let mx = 0, my = 0, rx = 0, ry = 0;

document.addEventListener('mousemove', e => {
  mx = e.clientX; my = e.clientY;
  cursor.style.left = mx - 5 + 'px';
  cursor.style.top = my - 5 + 'px';
});

function animRing() {
  rx += (mx - rx) * 0.12;
  ry += (my - ry) * 0.12;
  ring.style.left = rx + 'px';
  ring.style.top = ry + 'px';
  requestAnimationFrame(animRing);
}
animRing();

document.querySelectorAll('a, button, .skill-cell, .stat-cell').forEach(el => {
  el.addEventListener('mouseenter', () => {
    cursor.style.transform = 'scale(2.5)';
    ring.style.transform = 'translate(-50%,-50%) scale(1.5)';
    ring.style.borderColor = 'rgba(0,255,195,0.6)';
  });
  el.addEventListener('mouseleave', () => {
    cursor.style.transform = 'scale(1)';
    ring.style.transform = 'translate(-50%,-50%) scale(1)';
    ring.style.borderColor = 'rgba(0,255,195,0.4)';
  });
});

// ── Canvas particle network
const canvas = document.getElementById('bg');
const ctx = canvas.getContext('2d');
let W, H, pts = [];
const N = 60;

function resize() {
  W = canvas.width = window.innerWidth;
  H = canvas.height = window.innerHeight;
}
resize();
window.addEventListener('resize', resize);

for (let i = 0; i < N; i++) {
  pts.push({
    x: Math.random() * W, y: Math.random() * H,
    vx: (Math.random() - 0.5) * 0.4,
    vy: (Math.random() - 0.5) * 0.4,
    r: Math.random() * 1.5 + 0.5
  });
}

function drawNet() {
  ctx.clearRect(0, 0, W, H);
  pts.forEach(p => {
    p.x += p.vx; p.y += p.vy;
    if (p.x < 0 || p.x > W) p.vx *= -1;
    if (p.y < 0 || p.y > H) p.vy *= -1;
    ctx.beginPath();
    ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
    ctx.fillStyle = 'rgba(0,255,195,0.5)';
    ctx.fill();
  });
  for (let i = 0; i < N; i++) {
    for (let j = i + 1; j < N; j++) {
      const dx = pts[i].x - pts[j].x;
      const dy = pts[i].y - pts[j].y;
      const d = Math.sqrt(dx * dx + dy * dy);
      if (d < 140) {
        ctx.beginPath();
        ctx.moveTo(pts[i].x, pts[i].y);
        ctx.lineTo(pts[j].x, pts[j].y);
        ctx.strokeStyle = `rgba(0,255,195,${0.12 * (1 - d / 140)})`;
        ctx.lineWidth = 0.5;
        ctx.stroke();
      }
    }
  }
  requestAnimationFrame(drawNet);
}
drawNet();

// ── Scroll reveal
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
</script>
</body>
</html>
