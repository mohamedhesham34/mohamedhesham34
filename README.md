<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mohamed Hesham — Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Courier+Prime:wght@400;700&family=IM+Fell+English:ital@0;1&display=swap" rel="stylesheet"/>
<style>
*{box-sizing:border-box;margin:0;padding:0}

:root{
  --felt:#0C3020;
  --felt-mid:#114228;
  --card:#FAFAF5;
  --red:#B8102A;
  --black:#1A1A1A;
  --gold:#B8860B;
  --gold-light:#DAA520;
  --gold-dim:#8B6914;
}

body{
  background-color:var(--felt);
  background-image:
    radial-gradient(ellipse 80% 60% at 20% 10%, #155232 0%, transparent 55%),
    radial-gradient(ellipse 60% 50% at 80% 90%, #0d3a24 0%, transparent 50%),
    url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='6' height='6'%3E%3Ccircle cx='1' cy='1' r='0.8' fill='rgba(255,255,255,0.018)'/%3E%3Ccircle cx='4' cy='4' r='0.8' fill='rgba(255,255,255,0.018)'/%3E%3C/svg%3E");
  min-height:100vh;
  font-family:'IM Fell English', serif;
  color:var(--card);
  padding:50px 20px 70px;
  overflow-x:hidden;
}

.container{max-width:860px;margin:0 auto;position:relative;}

/* ── FELT EDGE SHADOW ── */
body::before{
  content:'';position:fixed;inset:0;
  box-shadow:inset 0 0 120px rgba(0,0,0,0.55);
  pointer-events:none;z-index:0;
}

/* ── CARD BASE ── */
.card{
  background:var(--card);
  color:var(--black);
  border-radius:14px;
  position:relative;
  box-shadow:
    0 14px 50px rgba(0,0,0,0.65),
    0 0 0 1.5px rgba(184,134,11,0.45),
    inset 0 1px 0 rgba(255,255,255,0.9);
  transition:transform .35s ease, box-shadow .35s ease;
  background-image:
    url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3CfeColorMatrix type='saturate' values='0'/%3E%3C/filter%3E%3Crect width='200' height='200' filter='url(%23n)' opacity='0.018'/%3E%3C/svg%3E");
}
.card:hover{
  transform:translateY(-8px) rotate(.25deg);
  box-shadow:0 26px 70px rgba(0,0,0,0.75),0 0 0 1.5px rgba(218,165,32,0.7),inset 0 1px 0 rgba(255,255,255,0.9);
}

/* ── CORNER INDEX ── */
.ci{
  position:absolute;
  display:flex;flex-direction:column;align-items:center;
  font-family:'Playfair Display',serif;font-weight:900;
  line-height:1.05;
}
.ci.tl{top:11px;left:15px}
.ci.br{bottom:11px;right:15px;transform:rotate(180deg)}
.ci .r{font-size:1.05rem}
.ci .s{font-size:.8rem;margin-top:1px}
.ci.rb{color:var(--red)}
.ci.bk{color:var(--black)}

/* ── GOLD RULE ── */
.rule{
  display:flex;align-items:center;gap:10px;
  margin:18px auto;width:70%;
}
.rule::before,.rule::after{
  content:'';flex:1;height:1px;
  background:linear-gradient(to right,transparent,var(--gold-light),transparent);
}
.rule-sym{color:var(--gold-light);font-size:.85rem}

/* ═══════════════════════════════
   HERO CARD
═══════════════════════════════ */
.hero-card{
  text-align:center;
  padding:70px 48px 56px;
  margin-bottom:32px;
  background:linear-gradient(160deg,#FDFDF8 0%,#F4EFE4 100%);
  border:2px solid var(--gold);
}

.hero-suits{
  display:flex;justify-content:center;gap:22px;
  font-size:2.2rem;margin-bottom:24px;
  animation:suitFadeIn 1s ease both;
}
.hero-suits .s-black{color:var(--black);opacity:.85}
.hero-suits .s-red{color:var(--red);opacity:.85}

.hero-rank{
  font-family:'Playfair Display',serif;
  font-size:3.6rem;font-weight:900;
  color:var(--black);
  letter-spacing:-.025em;
  line-height:1;
  animation:slideUp .8s ease both .1s;
}
.hero-rank span{color:var(--red)}

.hero-subtitle{
  font-family:'IM Fell English',serif;
  font-style:italic;
  font-size:.95rem;
  color:var(--red);
  letter-spacing:.18em;
  text-transform:uppercase;
  margin-top:10px;
  animation:slideUp .8s ease both .2s;
}

.hero-loc{
  color:#666;
  font-size:.88rem;
  margin-top:6px;
  font-style:italic;
  animation:slideUp .8s ease both .3s;
}

.social-row{
  display:flex;justify-content:center;gap:12px;
  margin-top:22px;
  animation:slideUp .8s ease both .4s;
}
.social-btn{
  display:inline-flex;align-items:center;gap:7px;
  padding:9px 22px;
  border:1.5px solid var(--gold);
  border-radius:5px;
  font-family:'Playfair Display',serif;
  font-size:.82rem;font-weight:700;
  color:var(--black);
  text-decoration:none;
  letter-spacing:.06em;
  transition:all .2s;
  background:transparent;
}
.social-btn:hover{background:var(--gold);color:#fff;border-color:var(--gold)}
.social-btn svg{width:16px;height:16px;flex-shrink:0}

/* ── ACE PIP CENTER ── */
.ace-pip{
  font-size:4rem;
  margin:0 auto;
  display:block;
  line-height:1;
  color:var(--black);
  opacity:.08;
  position:absolute;
  bottom:30px;
  right:36px;
  pointer-events:none;
  font-family:'Playfair Display',serif;
  font-weight:900;
}

/* ═══════════════════════════════
   THREE-CARD ROW
═══════════════════════════════ */
.trio{
  display:grid;
  grid-template-columns:1fr 1fr 1fr;
  gap:22px;
  margin-bottom:28px;
}

@media(max-width:680px){
  .trio{grid-template-columns:1fr}
  .hero-rank{font-size:2.6rem}
  .hero-suits{font-size:1.6rem}
}

.trio-card{padding:42px 22px 32px}
.trio-card .card-title{
  font-family:'Playfair Display',serif;
  font-size:1rem;font-weight:700;
  text-align:center;
  margin-bottom:18px;
  padding-bottom:12px;
  border-bottom:1px solid rgba(0,0,0,.08);
  display:flex;align-items:center;justify-content:center;gap:7px;
}
.trio-card .card-title .ts{font-size:1rem}
.ts-red{color:var(--red)}
.ts-blk{color:var(--black)}

/* ── ABOUT: code block ── */
.code-block{
  background:#0F1117;
  border-radius:7px;
  padding:14px 15px;
  font-family:'Courier Prime',monospace;
  font-size:.68rem;
  line-height:1.7;
  overflow:hidden;
}
.ck{color:#C792EA}   /* keyword */
.cv{color:#FFCB6B}   /* var name */
.cs{color:#C3E88D}   /* string */
.cp{color:#89DDFF}   /* punctuation */
.cc{color:#546E7A;font-style:italic} /* comment */
.cn{color:#F78C6C}   /* number/const */

/* ── TECH STACK ── */
.tech-section{margin-bottom:10px}
.tech-label{
  font-size:.6rem;
  text-transform:uppercase;
  letter-spacing:.12em;
  color:#888;
  margin-bottom:5px;
  font-family:'Playfair Display',serif;
}
.badge-row{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:10px}
.badge{
  padding:3px 9px;
  border-radius:3px;
  font-family:'Courier Prime',monospace;
  font-size:.65rem;font-weight:700;
  letter-spacing:.04em;
}
.badge-black{background:var(--black);color:var(--card)}
.badge-red{background:var(--red);color:#fff}
.badge-gold{background:var(--gold-dim);color:#fff}
.badge-outline{
  background:transparent;
  border:1px solid var(--black);
  color:var(--black);
}

/* ── STATS MINI ── */
.stat-row{
  display:flex;justify-content:space-between;align-items:center;
  padding:9px 0;
  border-bottom:1px dashed rgba(0,0,0,.1);
  font-size:.82rem;
}
.stat-row:last-child{border-bottom:none}
.stat-label{color:#555;font-style:italic}
.stat-val{
  font-family:'Playfair Display',serif;
  font-weight:700;font-size:1.05rem;
  color:var(--red);
}

/* ═══════════════════════════════
   STATS CARD (WIDE)
═══════════════════════════════ */
.wide-card{
  padding:38px 36px 34px;
  margin-bottom:28px;
}
.wide-card .card-title{
  font-family:'Playfair Display',serif;
  font-size:1.05rem;font-weight:700;
  margin-bottom:22px;
  padding-bottom:14px;
  border-bottom:1px solid rgba(0,0,0,.08);
  display:flex;align-items:center;gap:8px;
}

.stats-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:14px;
  margin-bottom:14px;
}
.stats-grid img{
  width:100%;border-radius:8px;
  filter:drop-shadow(0 4px 12px rgba(0,0,0,.15));
}
.activity-img{
  width:100%;border-radius:8px;
  filter:drop-shadow(0 4px 12px rgba(0,0,0,.15));
}

@media(max-width:600px){
  .stats-grid{grid-template-columns:1fr}
  .wide-card{padding:38px 20px 30px}
}

/* ═══════════════════════════════
   FOOTER CARD
═══════════════════════════════ */
.footer-band{
  text-align:center;
  padding:28px 20px;
  position:relative;
  z-index:1;
}
.footer-suits{
  display:flex;justify-content:center;gap:18px;
  font-size:1.1rem;margin-bottom:10px;opacity:.3;
}
.footer-suits .fr{color:var(--red)}
.footer-text{
  font-style:italic;
  font-size:.8rem;
  color:rgba(255,255,255,.35);
  letter-spacing:.08em;
}

/* ── DECORATIVE ROTATIONS ── */
.card-tilt-l{transform:rotate(-.6deg)}
.card-tilt-l:hover{transform:translateY(-8px) rotate(-.3deg)}
.card-tilt-r{transform:rotate(.6deg)}
.card-tilt-r:hover{transform:translateY(-8px) rotate(.3deg)}

/* ── ANIMATIONS ── */
@keyframes slideUp{
  from{opacity:0;transform:translateY(18px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes suitFadeIn{
  from{opacity:0;transform:scale(.8)}
  to{opacity:1;transform:scale(1)}
}

/* Staggered entry for cards */
.hero-card{animation:slideUp .9s ease both}
.trio .card:nth-child(1){animation:slideUp .8s ease both .15s;opacity:0;animation-fill-mode:both}
.trio .card:nth-child(2){animation:slideUp .8s ease both .25s;opacity:0;animation-fill-mode:both}
.trio .card:nth-child(3){animation:slideUp .8s ease both .35s;opacity:0;animation-fill-mode:both}
.wide-card{animation:slideUp .8s ease both .4s;opacity:0;animation-fill-mode:both}

/* ── SCATTERED CHIPS DECORATION ── */
.chip{
  position:fixed;
  border-radius:50%;
  border:3px solid;
  display:flex;align-items:center;justify-content:center;
  font-size:.55rem;
  font-family:'Playfair Display',serif;
  font-weight:700;
  opacity:.12;
  pointer-events:none;z-index:0;
  animation:chipFloat 8s ease-in-out infinite;
}
.chip1{width:42px;height:42px;top:8%;left:3%;border-color:var(--red);color:var(--red);animation-delay:0s}
.chip2{width:34px;height:34px;top:22%;right:4%;border-color:#DAA520;color:#DAA520;animation-delay:2s}
.chip3{width:38px;height:38px;bottom:20%;left:2%;border-color:var(--card);color:var(--card);animation-delay:4s}
.chip4{width:30px;height:30px;bottom:35%;right:3%;border-color:var(--red);color:var(--red);animation-delay:1s}

@keyframes chipFloat{
  0%,100%{transform:translateY(0) rotate(0deg)}
  50%{transform:translateY(-8px) rotate(6deg)}
}

/* ── OPEN LEARNING BADGE ── */
.learning-badge{
  display:inline-flex;align-items:center;gap:6px;
  padding:5px 14px;
  background:var(--gold-dim);
  color:#fff;
  border-radius:3px;
  font-size:.68rem;
  font-family:'Courier Prime',monospace;
  font-weight:700;
  letter-spacing:.06em;
  margin-top:12px;
}
</style>
</head>
<body>

<!-- Floating chips decoration -->
<div class="chip chip1">♥</div>
<div class="chip chip2">♦</div>
<div class="chip chip3">♠</div>
<div class="chip chip4">♣</div>

<div class="container">

  <!-- ══════════════════ HERO CARD ══════════════════ -->
  <div class="card hero-card">
    <!-- Corners -->
    <div class="ci tl bk"><span class="r">A</span><span class="s">♠</span></div>
    <div class="ci br bk"><span class="r">A</span><span class="s">♠</span></div>

    <div class="hero-suits">
      <span class="s-black">♠</span>
      <span class="s-red">♥</span>
      <span class="s-red">♦</span>
      <span class="s-black">♣</span>
    </div>

    <h1 class="hero-rank">Mohamed <span>Hesham</span></h1>
    <p class="hero-subtitle">Backend &amp; DevOps Engineer</p>
    <p class="hero-loc">Alexandria, Egypt 🇪🇬</p>

    <div class="rule"><span class="rule-sym">✦</span></div>

    <div class="social-row">
      <a href="https://linkedin.com/in/mohamedhesham34" class="social-btn">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="mailto:mohameddev34@gmail.com" class="social-btn">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
        Email
      </a>
    </div>

    <div class="learning-badge">🃏 &nbsp;Currently: Building cool things &amp; shipping fast</div>

    <span class="ace-pip">♠</span>
  </div>

  <!-- ══════════════════ THREE-CARD ROW ══════════════════ -->
  <div class="trio">

    <!-- CARD 1 — About Me (♥ Hearts) -->
    <div class="card trio-card card-tilt-l">
      <div class="ci tl rb"><span class="r">K</span><span class="s">♥</span></div>
      <div class="ci br rb"><span class="r">K</span><span class="s">♥</span></div>
      <div class="card-title">
        <span class="ts ts-red">♥</span> About Me
      </div>
      <div class="code-block">
<span class="ck">const</span> <span class="cv">mo</span> <span class="cp">= {</span><br/>
&nbsp;&nbsp;<span class="cv">role</span><span class="cp">:</span> <span class="cs">"Backend &amp; DevOps"</span><span class="cp">,</span><br/>
&nbsp;&nbsp;<span class="cv">stack</span><span class="cp">:</span> <span class="cp">[</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"TypeScript"</span><span class="cp">,</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Node.js"</span><span class="cp">,</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Bun"</span><br/>
&nbsp;&nbsp;<span class="cp">],</span><br/>
&nbsp;&nbsp;<span class="cv">focus</span><span class="cp">:</span> <span class="cp">[</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Scalable APIs"</span><span class="cp">,</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"CI/CD"</span><span class="cp">,</span><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Containers"</span><br/>
&nbsp;&nbsp;<span class="cp">],</span><br/>
&nbsp;&nbsp;<span class="cc">// Remote · Open to work</span><br/>
<span class="cp">};</span>
      </div>
    </div>

    <!-- CARD 2 — Tech Stack (♦ Diamonds) -->
    <div class="card trio-card">
      <div class="ci tl rb"><span class="r">Q</span><span class="s">♦</span></div>
      <div class="ci br rb"><span class="r">Q</span><span class="s">♦</span></div>
      <div class="card-title">
        <span class="ts ts-red">♦</span> Tech Stack
      </div>
      <div class="tech-section">
        <div class="tech-label">Languages</div>
        <div class="badge-row">
          <span class="badge badge-black">TypeScript</span>
          <span class="badge badge-outline">JavaScript</span>
        </div>
        <div class="tech-label">Runtime &amp; Backend</div>
        <div class="badge-row">
          <span class="badge badge-red">Node.js</span>
          <span class="badge badge-black">Bun</span>
          <span class="badge badge-outline">Express</span>
        </div>
        <div class="tech-label">DevOps &amp; Tools</div>
        <div class="badge-row">
          <span class="badge badge-gold">Docker</span>
          <span class="badge badge-black">Linux</span>
          <span class="badge badge-outline">Git</span>
          <span class="badge badge-outline">GitHub</span>
        </div>
        <div class="tech-label">Editor</div>
        <div class="badge-row">
          <span class="badge badge-black">VS Code</span>
        </div>
      </div>
    </div>

    <!-- CARD 3 — GitHub Stats (♣ Clubs) -->
    <div class="card trio-card card-tilt-r">
      <div class="ci tl bk"><span class="r">J</span><span class="s">♣</span></div>
      <div class="ci br bk"><span class="r">J</span><span class="s">♣</span></div>
      <div class="card-title">
        <span class="ts ts-blk">♣</span> My Hand
      </div>
      <div class="stat-row">
        <span class="stat-label">Commits</span>
        <span class="stat-val">📈</span>
      </div>
      <div class="stat-row">
        <span class="stat-label">Languages</span>
        <span class="stat-val">TS · JS</span>
      </div>
      <div class="stat-row">
        <span class="stat-label">Focus</span>
        <span class="stat-val">Backend</span>
      </div>
      <div class="stat-row">
        <span class="stat-label">Goal</span>
        <span class="stat-val">Remote 🎯</span>
      </div>
      <div class="stat-row">
        <span class="stat-label">Status</span>
        <span class="stat-val" style="color:#1a6b35;font-size:.82rem">● Learning</span>
      </div>
    </div>

  </div>

  <!-- ══════════════════ STATS WIDE CARD ══════════════════ -->
  <div class="card wide-card">
    <div class="ci tl rb"><span class="r">10</span><span class="s">♦</span></div>
    <div class="ci br rb"><span class="r">10</span><span class="s">♦</span></div>
    <div class="card-title">
      <span style="color:var(--red)">♦</span> GitHub Statistics
    </div>
    <div class="stats-grid">
      <img src="https://github-readme-stats.vercel.app/api?username=mohamedhesham34&theme=tokyonight&hide_border=true&show_icons=true" alt="GitHub Stats" onerror="this.parentNode.innerHTML='<div style=&quot;background:#1a1a2e;border-radius:8px;padding:20px;text-align:center;color:#a9b7d9;font-family:Courier Prime,monospace;font-size:.8rem&quot;>[ github-readme-stats ]<br/>Stats card renders on GitHub</div>'" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohamedhesham34&theme=tokyonight&hide_border=true&layout=compact&langs_count=6" alt="Top Languages" onerror="this.parentNode.innerHTML='<div style=&quot;background:#1a1a2e;border-radius:8px;padding:20px;text-align:center;color:#a9b7d9;font-family:Courier Prime,monospace;font-size:.8rem&quot;>[ top-langs card ]<br/>Renders on GitHub</div>'" />
    </div>
    <img class="activity-img" src="https://github-readme-activity-graph.vercel.app/graph?username=mohamedhesham34&theme=tokyo-night&hide_border=true&area=true" alt="Activity Graph" onerror="this.style.display='none'" />
  </div>

  <!-- ══════════════════ VISITOR CARD ══════════════════ -->
  <div style="text-align:center;position:relative;z-index:1;margin-top:4px">
    <div class="rule" style="margin:0 auto 20px"><span class="rule-sym">♠ ♥ ♦ ♣</span></div>
    <a href="https://visitcount.itsvg.in">
      <img src="https://visitcount.itsvg.in/api?id=mohamedhesham34&icon=6&color=6" alt="visitor count" style="border-radius:6px"/>
    </a>
  </div>

  <!-- FOOTER -->
  <div class="footer-band">
    <div class="footer-suits">
      <span>♠</span><span class="fr">♥</span><span class="fr">♦</span><span>♣</span>
    </div>
    <p class="footer-text">The house always ships on time &nbsp;·&nbsp; Alexandria, Egypt 🇪🇬</p>
  </div>

</div>
</body>
</html>
