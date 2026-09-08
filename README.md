<div align="center">

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- ANIMATED HEADER WITH GLITCH NAME -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=JetBrains+Mono:wght@300;400;700&family=Share+Tech+Mono&display=swap');

@keyframes glitch1 {
  0%, 100% { clip-path: inset(40% 0 61% 0); transform: translate(-2px, 2px); }
  20% { clip-path: inset(92% 0 1% 0); transform: translate(1px, -1px); }
  40% { clip-path: inset(43% 0 1% 0); transform: translate(-1px, 3px); }
  60% { clip-path: inset(25% 0 58% 0); transform: translate(3px, 1px); }
  80% { clip-path: inset(54% 0 7% 0); transform: translate(-3px, -2px); }
}
@keyframes glitch2 {
  0%, 100% { clip-path: inset(65% 0 1% 0); transform: translate(2px, -1px); }
  20% { clip-path: inset(10% 0 85% 0); transform: translate(-3px, 2px); }
  40% { clip-path: inset(70% 0 12% 0); transform: translate(1px, -3px); }
  60% { clip-path: inset(5% 0 60% 0); transform: translate(-2px, 1px); }
  80% { clip-path: inset(45% 0 30% 0); transform: translate(3px, -1px); }
}
@keyframes flicker {
  0%, 19.999%, 22%, 62.999%, 64%, 64.999%, 70%, 100% { opacity: 1; }
  20%, 21.999%, 63%, 63.999%, 65%, 69.999% { opacity: 0.33; }
}
@keyframes textShadow {
  0% { text-shadow: 0.08em 0 0.14em #00e5ff, -0.08em 0 0.14em #00e5ff, 0 0 20px #00e5ff, 0 0 40px #00e5ff; }
  50% { text-shadow: 0.04em 0 0.07em #00e5ff, -0.04em 0 0.07em #00e5ff, 0 0 10px #00e5ff, 0 0 20px #00e5ff; }
  100% { text-shadow: 0.08em 0 0.14em #00e5ff, -0.08em 0 0.14em #00e5ff, 0 0 20px #00e5ff, 0 0 40px #00e5ff; }
}
@keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: 0.4; } }
@keyframes scanline {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100vh); }
}
@keyframes borderGlow {
  0%, 100% { box-shadow: 0 0 5px #00e5ff, inset 0 0 5px #00e5ff33; border-color: #00e5ff; }
  50% { box-shadow: 0 0 20px #00e5ff, 0 0 40px #00e5ff55, inset 0 0 10px #00e5ff22; border-color: #00c4e8; }
}
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-6px); }
}
@keyframes shimmer {
  0% { background-position: -200% center; }
  100% { background-position: 200% center; }
}
@keyframes typeWriter { from { width: 0; } to { width: 100%; } }
@keyframes blink { 0%, 100% { border-right-color: #00e5ff; } 50% { border-right-color: transparent; } }
@keyframes rotate { 0% { filter: hue-rotate(0deg); } 100% { filter: hue-rotate(360deg); } }
@keyframes neonPulse {
  0%, 100% { text-shadow: 0 0 5px #00e5ff, 0 0 10px #00e5ff, 0 0 20px #00e5ff, 0 0 40px #00e5ff; }
  50% { text-shadow: 0 0 2px #00e5ff, 0 0 5px #00e5ff, 0 0 10px #00e5ff, 0 0 20px #00e5ff; }
}
@keyframes dash { to { stroke-dashoffset: 0; } }
@keyframes fadeInUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
@keyframes gridScroll { 0% { background-position: 0 0; } 100% { background-position: 0 50px; } }

.hdr-wrap {
  position: relative;
  width: 100%;
  background: linear-gradient(180deg, #050816 0%, #0a0f2e 50%, #050816 100%);
  border-bottom: 1px solid #00e5ff33;
  overflow: hidden;
  padding: 20px 0;
}
.hdr-wrap::before {
  content: '';
  position: absolute; top: 0; left: 0; right: 0; bottom: 0;
  background-image:
    linear-gradient(#00e5ff08 1px, transparent 1px),
    linear-gradient(90deg, #00e5ff08 1px, transparent 1px);
  background-size: 50px 50px;
  animation: gridScroll 4s linear infinite;
  pointer-events: none;
}
.hdr-wrap::after {
  content: '';
  position: absolute; top: -50%; left: 0; width: 100%; height: 2px;
  background: linear-gradient(90deg, transparent, #00e5ff66, transparent);
  animation: scanline 4s linear infinite;
  pointer-events: none;
}
.glitch-name {
  font-family: 'Orbitron', monospace;
  font-size: 68px;
  font-weight: 900;
  letter-spacing: 12px;
  color: #fff;
  position: relative;
  display: inline-block;
  animation: textShadow 3s infinite alternate;
}
.glitch-name::before, .glitch-name::after {
  content: 'SHUBHAM';
  position: absolute; top: 0; left: 0;
  width: 100%; height: 100%;
  font-family: 'Orbitron', monospace;
  font-weight: 900;
  letter-spacing: 12px;
}
.glitch-name::before {
  color: #ff00ff;
  animation: glitch1 3s infinite linear alternate-reverse;
  opacity: 0.7;
}
.glitch-name::after {
  color: #00e5ff;
  animation: glitch2 2s infinite linear alternate-reverse;
  opacity: 0.7;
}
.sub-role {
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  letter-spacing: 6px;
  color: #00e5ff;
  text-transform: uppercase;
  margin-top: 8px;
}
.scanline-overlay {
  position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: repeating-linear-gradient(
    0deg,
    transparent,
    transparent 2px,
    rgba(0, 229, 255, 0.015) 2px,
    rgba(0, 229, 255, 0.015) 4px
  );
  pointer-events: none;
  z-index: 9999;
}

/* ── Terminal Status Box ── */
.term-box {
  background: linear-gradient(135deg, #0a0f2e 0%, #0d1117 100%);
  border: 1px solid #00e5ff44;
  border-radius: 8px;
  padding: 0;
  max-width: 680px;
  margin: 0 auto 10px;
  font-family: 'Share Tech Mono', monospace;
  animation: borderGlow 3s ease-in-out infinite;
  overflow: hidden;
  text-align: left;
}
.term-titlebar {
  background: linear-gradient(90deg, #00e5ff22, transparent);
  padding: 8px 16px;
  display: flex;
  align-items: center;
  gap: 8px;
  border-bottom: 1px solid #00e5ff22;
}
.term-dot { width: 10px; height: 10px; border-radius: 50%; }
.term-dot.r { background: #ff5f56; }
.term-dot.y { background: #ffbd2e; }
.term-dot.g { background: #27c93f; }
.term-label {
  font-size: 11px;
  color: #00e5ff88;
  letter-spacing: 2px;
  margin-left: 8px;
}
.term-body {
  padding: 16px 20px;
  font-size: 13px;
  line-height: 1.7;
  color: #c9d1d9;
}
.term-body .lbl { color: #00e5ff; font-weight: bold; }
.term-body .val { color: #ffffff; }
.term-body .grn { color: #27c93f; }
.term-body .pur { color: #8b5cf6; }
.term-body .ylw { color: #fbbf24; }
.term-cursor {
  display: inline-block;
  width: 8px;
  height: 16px;
  background: #00e5ff;
  animation: pulse 1s step-end infinite;
  vertical-align: middle;
  margin-left: 4px;
}

/* ── Holographic Project Cards ── */
.holo-card {
  background: linear-gradient(135deg, #0d1117 0%, #0a0f2e 50%, #0d1117 100%);
  border: 1px solid #00e5ff33;
  border-radius: 12px;
  padding: 24px;
  margin: 12px auto;
  max-width: 600px;
  position: relative;
  overflow: hidden;
  animation: fadeInUp 0.6s ease-out forwards, borderGlow 4s ease-in-out infinite;
}
.holo-card::before {
  content: '';
  position: absolute; top: 0; left: -100%; width: 50%; height: 100%;
  background: linear-gradient(90deg, transparent, #00e5ff08, transparent);
  animation: shimmer 4s infinite;
}
.holo-card::after {
  content: '';
  position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, #00e5ff, transparent);
}
.holo-card .card-num {
  font-family: 'Orbitron', monospace;
  font-size: 11px;
  color: #00e5ff;
  letter-spacing: 4px;
  margin-bottom: 8px;
}
.holo-card .card-title {
  font-family: 'Orbitron', monospace;
  font-size: 16px;
  color: #fff;
  font-weight: 700;
  margin-bottom: 8px;
}
.holo-card .card-desc {
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
  color: #8b949e;
  line-height: 1.6;
  margin-bottom: 12px;
}
.holo-card .card-meta {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: #00e5ff;
  background: #00e5ff08;
  border: 1px solid #00e5ff22;
  border-radius: 4px;
  padding: 10px 14px;
  line-height: 1.8;
}
.status-badge {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 20px;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 2px;
  font-family: 'JetBrains Mono', monospace;
}
.status-dev { background: #00e5ff15; color: #00e5ff; border: 1px solid #00e5ff44; }
.status-bld { background: #fbbf2415; color: #fbbf24; border: 1px solid #fbbf2444; }
.status-exp { background: #8b5cf615; color: #8b5cf6; border: 1px solid #8b5cf644; }
.status-pro { background: #27c93f15; color: #27c93f; border: 1px solid #27c93f44; }

/* ── Skill Bars ── */
.skill-row {
  display: flex;
  align-items: center;
  margin: 6px 0;
  font-family: 'JetBrains Mono', monospace;
  font-size: 12px;
}
.skill-label {
  width: 140px;
  color: #8b949e;
  text-align: right;
  padding-right: 14px;
}
.skill-bar {
  flex: 1;
  height: 6px;
  background: #0d1117;
  border-radius: 3px;
  overflow: hidden;
  border: 1px solid #00e5ff15;
}
.skill-fill {
  height: 100%;
  border-radius: 3px;
  background: linear-gradient(90deg, #00e5ff, #8b5cf6);
  box-shadow: 0 0 8px #00e5ff66;
}

/* ── Animated Divider ── */
.divider {
  height: 1px;
  max-width: 600px;
  margin: 40px auto;
  background: linear-gradient(90deg, transparent, #00e5ff66, #8b5cf666, #00e5ff66, transparent);
  position: relative;
}
.divider::after {
  content: '';
  position: absolute;
  top: -3px; left: 50%;
  width: 6px; height: 6px;
  background: #00e5ff;
  border-radius: 50%;
  transform: translateX(-50%);
  box-shadow: 0 0 10px #00e5ff, 0 0 20px #00e5ff;
  animation: pulse 2s infinite;
}

/* ── Section Headers ── */
.sec-hdr {
  font-family: 'Orbitron', monospace;
  font-size: 14px;
  letter-spacing: 4px;
  color: #00e5ff;
  text-transform: uppercase;
  margin-bottom: 20px;
  animation: neonPulse 3s infinite;
}
.sec-hdr::before { content: '> '; color: #8b5cf6; }

/* ── Protocol Steps ── */
.proto-steps {
  display: flex;
  justify-content: center;
  gap: 8px;
  flex-wrap: wrap;
  max-width: 700px;
  margin: 0 auto;
}
.proto-step {
  background: #0d1117;
  border: 1px solid #00e5ff33;
  border-radius: 6px;
  padding: 10px 16px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: #c9d1d9;
  position: relative;
  animation: float 3s ease-in-out infinite;
}
.proto-step:nth-child(2) { animation-delay: 0.3s; }
.proto-step:nth-child(3) { animation-delay: 0.6s; }
.proto-step:nth-child(4) { animation-delay: 0.9s; }
.proto-step:nth-child(5) { animation-delay: 1.2s; }
.proto-step:nth-child(6) { animation-delay: 1.5s; }
.proto-step:nth-child(7) { animation-delay: 1.8s; }
.proto-step:nth-child(8) { animation-delay: 2.1s; }
.proto-step .step-num {
  font-family: 'Orbitron', monospace;
  font-size: 18px;
  color: #00e5ff;
  font-weight: 900;
  display: block;
  margin-bottom: 4px;
}
.proto-step .step-arrow {
  color: #8b5cf6;
  font-size: 10px;
}

/* ── Neon Text ── */
.neon {
  color: #00e5ff;
  text-shadow: 0 0 7px #00e5ff, 0 0 10px #00e5ff, 0 0 21px #00e5ff;
}
.neon-pur {
  color: #8b5cf6;
  text-shadow: 0 0 7px #8b5cf6, 0 0 10px #8b5cf6;
}

/* ── Circular Avatars ── */
.avatar-ring {
  width: 140px; height: 140px;
  border-radius: 50%;
  border: 2px solid #00e5ff;
  padding: 4px;
  box-shadow: 0 0 15px #00e5ff55, 0 0 30px #00e5ff22, inset 0 0 15px #00e5ff11;
  animation: rotate 8s linear infinite;
}

/* ── Quote ── */
.quote-box {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px 30px;
  background: linear-gradient(135deg, #00e5ff08, #8b5cf608);
  border-left: 3px solid #00e5ff;
  border-radius: 0 8px 8px 0;
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  color: #c9d1d9;
  font-style: italic;
  position: relative;
}
.quote-box::before {
  content: '"';
  font-family: 'Orbitron', monospace;
  font-size: 60px;
  color: #00e5ff33;
  position: absolute;
  top: -10px; left: 10px;
}

/* ── Activity Graph wrapper ── */
.activity-wrap {
  border: 1px solid #00e5ff22;
  border-radius: 8px;
  overflow: hidden;
  max-width: 800px;
  margin: 0 auto;
}

/* ── Footer ── */
.foot-text {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: #00e5ff88;
  letter-spacing: 3px;
}
</style>

<div class="scanline-overlay"></div>

<!-- ═══ HERO ═══ -->
<div class="hdr-wrap">

<!-- STATUS BAR -->
<table style="width:100%;max-width:700px;margin:0 auto 16px;border-collapse:collapse;font-family:'JetBrains Mono',monospace;font-size:11px;color:#8b949e;">
<tr>
  <td style="text-align:left;padding:4px 10px;border-bottom:1px solid #00e5ff15;">
    <span style="color:#27c93f;">●</span> ONLINE
  </td>
  <td style="text-align:center;padding:4px 10px;border-bottom:1px solid #00e5ff15;color:#00e5ff;">
    SESSION://mshubham5937-alt
  </td>
  <td style="text-align:right;padding:4px 10px;border-bottom:1px solid #00e5ff15;">
    <span id="live-clock"></span>
  </td>
</tr>
</table>

<!-- GLITCH NAME -->
<div style="padding:30px 0 10px;">
  <div class="glitch-name">SHUBHAM</div>
</div>

<!-- SUBTITLE -->
<div class="sub-role">
  <span style="color:#8b5cf6;">//</span> SOFTWARE DEVELOPER <span style="color:#8b5cf6;">•</span> BUILDER <span style="color:#8b5cf6;">•</span> PROBLEM SOLVER
</div>

<!-- TYPING LINE -->
<div style="margin-top:20px;">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=14&duration=3000&pause=800&color=00E5FF&center=true&vCenter=true&width=600&lines=Building+ideas+into+reality;Exploring+Web+%7C+Games+%7C+AI+%7C+3D;Always+learning.+Always+building.;SYSTEM+STATUS%3A+OPERATIONAL" />
</div>

<!-- SOCIAL BADGES -->
<div style="margin-top:20px;padding-bottom:20px;">
  <a href="https://github.com/mshubham5937-alt"><img src="https://img.shields.io/badge/GITHUB-0d1117?style=for-the-badge&logo=github&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" /></a>
  <a href="https://www.linkedin.com/"><img src="https://img.shields.io/badge/LINKEDIN-0d1117?style=for-the-badge&logo=linkedin&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" /></a>
  <a href="mailto:"><img src="https://img.shields.io/badge/EMAIL-0d1117?style=for-the-badge&logo=maildotru&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" /></a>
  <img src="https://komarev.com/ghpvc/?username=mshubham5937-alt&style=for-the-badge&color=00e5ff&label=PROFILE+VIEWS&labelColor=0d1117" />
</div>

</div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: SYSTEM STATUS -->
<!-- ═══════════════════════════════════════════════ -->
<div style="margin-top:40px;">
  <div class="sec-hdr">SYSTEM STATUS</div>
</div>

<div class="term-box">
  <div class="term-titlebar">
    <div class="term-dot r"></div>
    <div class="term-dot y"></div>
    <div class="term-dot g"></div>
    <span class="term-label">SYSTEM INTERFACE v3.2</span>
  </div>
  <div class="term-body">
    <span class="lbl">USER</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="val">SHUBHAM</span><br>
    <span class="lbl">ROLE</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="val">COMPUTER SCIENCE STUDENT</span><br>
    <span class="lbl">STATUS</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="grn">● ONLINE</span><br>
    <span class="lbl">MODE</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="pur">BUILD</span><br>
    <span class="lbl">UPTIME</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="val">24/7/365</span><br>
    <br>
    <span class="lbl">CURRENT FOCUS</span><br>
    <span class="grn">├──</span> <span class="val">Web Development</span><br>
    <span class="grn">├──</span> <span class="val">Software Development</span><br>
    <span class="grn">├──</span> <span class="val">Game Development</span><br>
    <span class="grn">├──</span> <span class="val">3D Experiences</span><br>
    <span class="grn">└──</span> <span class="ylw">Exploring AI</span><br>
    <br>
    <span class="lbl">MISSION</span><br>
    <span class="pur">└──</span> Turn interesting ideas into real products.<span class="term-cursor"></span>
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: ABOUT ME -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">ABOUT ME</div>

<div style="max-width:650px;margin:0 auto;">
  <div style="background:#0d1117;border:1px solid #00e5ff22;border-radius:8px;padding:24px 28px;font-family:'JetBrains Mono',monospace;font-size:13px;line-height:1.8;color:#c9d1d9;position:relative;overflow:hidden;">
    <div style="position:absolute;top:0;left:0;width:100%;height:1px;background:linear-gradient(90deg,transparent,#00e5ff,transparent);"></div>
    <span style="color:#00e5ff;font-family:'Orbitron',monospace;font-size:11px;letter-spacing:3px;">ABOUT // </span><span style="color:#8b949e;">user.personal_log</span><br><br>
    I am a Computer Science student who enjoys building things.<br>
    I like turning ideas from <span class="neon">concept</span> to <span class="neon-pur">reality</span>.<br><br>
    <div style="display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin:16px 0;">
      <span style="color:#8b5cf6;">IDEA</span>
      <span style="color:#00e5ff;">→</span>
      <span style="color:#8b5cf6;">PROTOTYPE</span>
      <span style="color:#00e5ff;">→</span>
      <span style="color:#8b5cf6;">BUILD</span>
      <span style="color:#00e5ff;">→</span>
      <span style="color:#8b5cf6;">TEST</span>
      <span style="color:#00e5ff;">→</span>
      <span style="color:#8b5cf6;">PRODUCT</span>
    </div>
    <br>
    Currently exploring: software, web, games, 3D, and AI.<br><br>
    <span style="color:#00e5ff;font-weight:bold;">BUILD</span> → <span style="color:#ff5f56;font-weight:bold;">BREAK</span> → <span style="color:#fbbf24;font-weight:bold;">LEARN</span> → <span style="color:#27c93f;font-weight:bold;">IMPROVE</span> → <span style="color:#8b5cf6;font-weight:bold;">REPEAT</span>
    <div style="position:absolute;bottom:0;left:0;width:100%;height:1px;background:linear-gradient(90deg,transparent,#8b5cf6,transparent);"></div>
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: TECH STACK -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">TECH STACK</div>

<div style="max-width:650px;margin:0 auto;">
  <!-- LANGUAGES -->
  <div style="background:#0d1117;border:1px solid #00e5ff22;border-radius:8px;padding:20px;margin-bottom:12px;">
    <div style="font-family:'Orbitron',monospace;font-size:11px;color:#00e5ff;letter-spacing:3px;margin-bottom:14px;">
      <span style="color:#8b5cf6;">01 //</span> LANGUAGES
    </div>
    <div style="display:flex;justify-content:center;flex-wrap:wrap;gap:16px;">
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=cpp" width="40" style="animation:float 3s ease-in-out infinite;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">C++</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=python" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.2s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Python</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=js" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.4s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">JavaScript</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=ts" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.6s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">TypeScript</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=java" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.8s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Java</span>
      </div>
    </div>
  </div>

  <!-- WEB & BACKEND -->
  <div style="background:#0d1117;border:1px solid #8b5cf622;border-radius:8px;padding:20px;margin-bottom:12px;">
    <div style="font-family:'Orbitron',monospace;font-size:11px;color:#8b5cf6;letter-spacing:3px;margin-bottom:14px;">
      <span style="color:#00e5ff;">02 //</span> WEB &amp; BACKEND
    </div>
    <div style="display:flex;justify-content:center;flex-wrap:wrap;gap:16px;">
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=html" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.1s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">HTML</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=css" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.3s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">CSS</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=react" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.5s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">React</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=nodejs" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.7s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Node.js</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=express" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.9s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Express</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=postgres" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:1.1s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">PostgreSQL</span>
      </div>
    </div>
  </div>

  <!-- TOOLS -->
  <div style="background:#0d1117;border:1px solid #00e5ff22;border-radius:8px;padding:20px;">
    <div style="font-family:'Orbitron',monospace;font-size:11px;color:#00e5ff;letter-spacing:3px;margin-bottom:14px;">
      <span style="color:#8b5cf6;">03 //</span> TOOLS &amp; TECHNOLOGIES
    </div>
    <div style="display:flex;justify-content:center;flex-wrap:wrap;gap:16px;">
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=git" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.15s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Git</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=github" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.35s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">GitHub</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=vscode" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.55s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">VS Code</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=figma" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.75s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Figma</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=threejs" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:0.95s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Three.js</span>
      </div>
      <div class="skill-row" style="flex-direction:column;align-items:center;gap:4px;width:70px;">
        <img src="https://skillicons.dev/icons?i=firebase" width="40" style="animation:float 3s ease-in-out infinite;animation-delay:1.15s;" />
        <span style="font-size:10px;color:#8b949e;font-family:'JetBrains Mono',monospace;">Firebase</span>
      </div>
    </div>
  </div>
</div>

<!-- SKILL BARS -->
<div style="max-width:600px;margin:24px auto 0;">
  <div class="skill-row"><span class="skill-label">C / C++</span><div class="skill-bar"><div class="skill-fill" style="width:85%;"></div></div></div>
  <div class="skill-row"><span class="skill-label">JavaScript</span><div class="skill-bar"><div class="skill-fill" style="width:75%;"></div></div></div>
  <div class="skill-row"><span class="skill-label">Python</span><div class="skill-bar"><div class="skill-fill" style="width:70%;"></div></div></div>
  <div class="skill-row"><span class="skill-label">React / Node.js</span><div class="skill-bar"><div class="skill-fill" style="width:65%;"></div></div></div>
  <div class="skill-row"><span class="skill-label">Three.js / 3D</span><div class="skill-bar"><div class="skill-fill" style="width:55%;"></div></div></div>
  <div class="skill-row"><span class="skill-label">Git / DevOps</span><div class="skill-bar"><div class="skill-fill" style="width:72%;"></div></div></div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: PROJECTS -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">PROJECT DATABASE</div>

<!-- PROJECT 1 -->
<div class="holo-card" style="animation-delay:0.1s;">
  <div class="card-num"><span style="color:#8b5cf6;">SYS://</span>PROJECT_01</div>
  <div class="card-title">FREE_TOOLS_HUB</div>
  <div class="card-desc">A collection of useful free tools for students and creators.</div>
  <div class="card-meta">
    TYPE &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Web Platform<br>
    CATEGORY &nbsp;&nbsp;: Productivity<br>
    FOCUS &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Useful • Simple • Free<br>
    STACK &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: React • Node.js • Firebase
  </div>
  <div style="margin-top:12px;">
    <span class="status-badge status-dev">IN DEVELOPMENT</span>
  </div>
</div>

<!-- PROJECT 2 -->
<div class="holo-card" style="animation-delay:0.2s;">
  <div class="card-num"><span style="color:#8b5cf6;">SYS://</span>PROJECT_02</div>
  <div class="card-title">GAME DEVELOPMENT</div>
  <div class="card-desc">Experimental game projects focused on simple mechanics, addictive gameplay and mobile-first experiences.</div>
  <div class="card-meta">
    TYPE &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Game<br>
    CATEGORY &nbsp;&nbsp;: Interactive Entertainment<br>
    FOCUS &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Gameplay • UX • Monetization<br>
    ENGINE &nbsp;&nbsp;&nbsp;&nbsp;: Unity / Custom
  </div>
  <div style="margin-top:12px;">
    <span class="status-badge status-bld">BUILDING</span>
  </div>
</div>

<!-- PROJECT 3 -->
<div class="holo-card" style="animation-delay:0.3s;">
  <div class="card-num"><span style="color:#8b5cf6;">SYS://</span>PROJECT_03</div>
  <div class="card-title">IMMERSIVE_3D_COMMERCE</div>
  <div class="card-desc">An experimental immersive 3D experience for a cycle and tyre business, using futuristic interfaces and spatial navigation concepts.</div>
  <div class="card-meta">
    TYPE &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Web Experience<br>
    CATEGORY &nbsp;&nbsp;: 3D / Three.js<br>
    FOCUS &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Immersive UI • Animation • Interaction<br>
    LIBRARY &nbsp;&nbsp;&nbsp;: Three.js • GSAP
  </div>
  <div style="margin-top:12px;">
    <span class="status-badge status-exp">EXPERIMENTAL</span>
  </div>
</div>

<!-- PROJECT 4 -->
<div class="holo-card" style="animation-delay:0.4s;">
  <div class="card-num"><span style="color:#8b5cf6;">SYS://</span>PROJECT_04</div>
  <div class="card-title">SMART_CAMPUS / CIVIC_TECH</div>
  <div class="card-desc">A problem-reporting and resolution platform connecting citizens, institutions and authorities through a structured workflow.</div>
  <div class="card-meta">
    TYPE &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Full-Stack Platform<br>
    CATEGORY &nbsp;&nbsp;: Social Impact / Smart Systems<br>
    FOCUS &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Reporting • Tracking • Resolution<br>
    STACK &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: MERN • PostgreSQL
  </div>
  <div style="margin-top:12px;">
    <span class="status-badge status-pro">PROTOTYPE</span>
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: GITHUB TELEMETRY -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">GITHUB TELEMETRY</div>

<div style="max-width:800px;margin:0 auto;">
  <!-- Stats Row -->
  <div style="display:flex;justify-content:center;gap:16px;flex-wrap:wrap;margin-bottom:16px;">
    <div style="background:#0d1117;border:1px solid #00e5ff22;border-radius:8px;padding:4px;animation:borderGlow 5s ease-in-out infinite;">
      <img src="https://github-readme-stats.vercel.app/api?username=mshubham5937-alt&show_icons=true&theme=transparent&hide_border=true&title_color=00E5FF&icon_color=8B5CF6&text_color=FFFFFF&bg_color=00000000" height="170"/>
    </div>
    <div style="background:#0d1117;border:1px solid #8b5cf622;border-radius:8px;padding:4px;animation:borderGlow 5s ease-in-out infinite;animation-delay:1s;">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mshubham5937-alt&layout=compact&theme=transparent&hide_border=true&title_color=8B5CF6&text_color=FFFFFF&bg_color=00000000" height="170"/>
    </div>
  </div>

  <!-- Streak -->
  <div style="text-align:center;margin-bottom:16px;">
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=mshubham5937-alt&theme=transparent&hide_border=true&ring=00E5FF&fire=8B5CF6&currStreakLabel=00E5FF&sideLabels=FFFFFF" height="120"/>
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: CONTRIBUTION MATRIX -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">CONTRIBUTION MATRIX</div>

<div class="activity-wrap">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=mshubham5937-alt&bg_color=050816&color=00E5FF&line=8B5CF6&point=FFFFFF&area=true&hide_border=true&area_color=00E5FF11" width="100%"/>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: CURRENTLY BUILDING -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">CURRENTLY BUILDING</div>

<div style="max-width:550px;margin:0 auto;">
  <div style="background:#0d1117;border:1px solid #00e5ff22;border-radius:8px;padding:20px 24px;font-family:'Share Tech Mono',monospace;font-size:12px;color:#c9d1d9;">
    <div style="display:flex;justify-content:space-between;margin-bottom:8px;">
      <span style="color:#00e5ff;">EXPLORING_NEW_IDEAS</span>
      <span style="color:#27c93f;">80%</span>
    </div>
    <!-- Progress bar -->
    <div style="height:6px;background:#161b22;border-radius:3px;overflow:hidden;margin-bottom:16px;border:1px solid #00e5ff22;">
      <div style="height:100%;width:80%;background:linear-gradient(90deg,#00e5ff,#8b5cf6);border-radius:3px;box-shadow:0 0 10px #00e5ff66;"></div>
    </div>
    <span style="color:#00e5ff;">→</span> Building projects<br>
    <span style="color:#8b5cf6;">→</span> Learning new technologies<br>
    <span style="color:#00e5ff;">→</span> Experimenting with UI/UX<br>
    <span style="color:#8b5cf6;">→</span> Improving development skills<br>
    <span style="color:#00e5ff;">→</span> Turning prototypes into products
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: DEVELOPER PROTOCOL -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">DEVELOPER PROTOCOL</div>

<div class="proto-steps">
  <div class="proto-step"><span class="step-num">01</span>THINK<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">02</span>DESIGN<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">03</span>BUILD<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">04</span>TEST<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">05</span>BREAK<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">06</span>DEBUG<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">07</span>LEARN<span class="step-arrow"> ▸</span></div>
  <div class="proto-step"><span class="step-num">08</span>SHIP<span class="step-arrow"> ▸</span></div>
</div>

<div style="margin-top:30px;">
  <div class="quote-box">
    The best way to learn development is to build something.
  </div>
</div>

<div class="divider"></div>

<!-- ═══════════════════════════════════════════════ -->
<!-- SECTION: CONNECT -->
<!-- ═══════════════════════════════════════════════ -->
<div class="sec-hdr">CONNECT</div>

<div style="display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin:20px 0;">
  <a href="https://github.com/mshubham5937-alt">
    <img src="https://img.shields.io/badge/GITHUB-0d1117?style=for-the-badge&logo=github&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" />
  </a>
  <a href="https://www.linkedin.com/">
    <img src="https://img.shields.io/badge/LINKEDIN-0d1117?style=for-the-badge&logo=linkedin&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" />
  </a>
  <a href="mailto:">
    <img src="https://img.shields.io/badge/EMAIL-0d1117?style=for-the-badge&logo=maildotru&logoColor=00E5FF&labelColor=0d1117&color=00e5ff" />
  </a>
</div>

<div style="margin:20px 0;">
  <div style="font-family:'Share Tech Mono',monospace;font-size:12px;color:#00e5ff;letter-spacing:3px;animation:neonPulse 2s infinite;">
    SYSTEM STATUS : <span style="color:#27c93f;">ONLINE</span>
  </div>
  <div style="font-family:'Share Tech Mono',monospace;font-size:11px;color:#8b949e;letter-spacing:2px;margin-top:6px;">
    ACCESS LEVEL : DEVELOPER
  </div>
</div>

<!-- ═══ FOOTER ═══ -->
<div style="margin-top:30px;">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00E5FF,25:050816,50:8B5CF6,75:050816,100:00E5FF&height=120&section=footer" width="100%"/>
</div>

<div style="margin-top:12px;padding-bottom:30px;">
  <div class="foot-text">
    <span style="color:#8b5cf6;">◈</span> DESIGNED WITH PRECISION <span style="color:#8b5cf6;">◈</span> BUILT WITH PASSION <span style="color:#8b5cf6;">◈</span>
  </div>
</div>

</div>
