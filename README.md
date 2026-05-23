<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 300" width="1200" height="300">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&amp;family=Orbitron:wght@700&amp;display=swap');

      .bg { fill: #020b18; }
      .grid-line { stroke: #0d3b5e; stroke-width: 0.5; opacity: 0.6; }

      /* Scan line sweep */
      @keyframes scan {
        0%   { transform: translateY(-300px); opacity: 0; }
        10%  { opacity: 1; }
        90%  { opacity: 1; }
        100% { transform: translateY(300px); opacity: 0; }
      }

      /* Wave animations */
      @keyframes wave1 {
        0%   { d: path("M0,200 C150,170 300,230 450,200 C600,170 750,230 900,200 C1050,170 1150,210 1200,200 L1200,300 L0,300 Z"); }
        50%  { d: path("M0,210 C150,230 300,170 450,210 C600,240 750,170 900,210 C1050,240 1150,190 1200,210 L1200,300 L0,300 Z"); }
        100% { d: path("M0,200 C150,170 300,230 450,200 C600,170 750,230 900,200 C1050,170 1150,210 1200,200 L1200,300 L0,300 Z"); }
      }
      @keyframes wave2 {
        0%   { d: path("M0,220 C200,195 350,245 500,220 C650,195 800,245 950,215 C1100,190 1160,225 1200,220 L1200,300 L0,300 Z"); }
        50%  { d: path("M0,230 C200,250 350,200 500,230 C650,255 800,200 950,230 C1100,255 1160,210 1200,230 L1200,300 L0,300 Z"); }
        100% { d: path("M0,220 C200,195 350,245 500,220 C650,195 800,245 950,215 C1100,190 1160,225 1200,220 L1200,300 L0,300 Z"); }
      }
      @keyframes wave3 {
        0%   { d: path("M0,240 C180,215 360,260 540,235 C720,210 880,255 1060,230 C1130,215 1170,240 1200,240 L1200,300 L0,300 Z"); }
        50%  { d: path("M0,250 C180,265 360,220 540,250 C720,270 880,220 1060,250 C1130,265 1170,230 1200,250 L1200,300 L0,300 Z"); }
        100% { d: path("M0,240 C180,215 360,260 540,235 C720,210 880,255 1060,230 C1130,215 1170,240 1200,240 L1200,300 L0,300 Z"); }
      }

      .wave1 { animation: wave1 6s ease-in-out infinite; }
      .wave2 { animation: wave2 5s ease-in-out infinite 0.5s; }
      .wave3 { animation: wave3 4s ease-in-out infinite 1s; }

      /* Floating particles */
      @keyframes floatUp1 {
        0%   { transform: translateY(0px) translateX(0px); opacity: 0; }
        10%  { opacity: 0.8; }
        90%  { opacity: 0.6; }
        100% { transform: translateY(-280px) translateX(20px); opacity: 0; }
      }
      @keyframes floatUp2 {
        0%   { transform: translateY(0px) translateX(0px); opacity: 0; }
        10%  { opacity: 0.7; }
        90%  { opacity: 0.5; }
        100% { transform: translateY(-280px) translateX(-15px); opacity: 0; }
      }
      @keyframes floatUp3 {
        0%   { transform: translateY(0px); opacity: 0; }
        10%  { opacity: 0.9; }
        90%  { opacity: 0.4; }
        100% { transform: translateY(-280px); opacity: 0; }
      }

      .p1 { animation: floatUp1 8s ease-in-out infinite; }
      .p2 { animation: floatUp2 7s ease-in-out infinite 1.2s; }
      .p3 { animation: floatUp3 9s ease-in-out infinite 2.5s; }
      .p4 { animation: floatUp1 6s ease-in-out infinite 0.8s; }
      .p5 { animation: floatUp2 10s ease-in-out infinite 3s; }
      .p6 { animation: floatUp3 7.5s ease-in-out infinite 1.8s; }
      .p7 { animation: floatUp1 8.5s ease-in-out infinite 4s; }
      .p8 { animation: floatUp2 6.5s ease-in-out infinite 2s; }

      /* Binary rain */
      @keyframes rain1 { 0%{transform:translateY(-20px);opacity:0} 5%{opacity:1} 95%{opacity:0.6} 100%{transform:translateY(320px);opacity:0} }
      @keyframes rain2 { 0%{transform:translateY(-20px);opacity:0} 5%{opacity:0.8} 95%{opacity:0.4} 100%{transform:translateY(320px);opacity:0} }
      .rain1 { animation: rain1 4s linear infinite; font-size:10px; fill:#00ff88; font-family:'Share Tech Mono',monospace; opacity:0.5; }
      .rain2 { animation: rain2 5s linear infinite 1s; font-size:9px; fill:#00ccff; font-family:'Share Tech Mono',monospace; opacity:0.4; }
      .rain3 { animation: rain1 3.5s linear infinite 2s; font-size:8px; fill:#00ff88; font-family:'Share Tech Mono',monospace; opacity:0.3; }
      .rain4 { animation: rain2 6s linear infinite 0.5s; font-size:10px; fill:#00ccff; font-family:'Share Tech Mono',monospace; opacity:0.35; }
      .rain5 { animation: rain1 4.5s linear infinite 3s; font-size:9px; fill:#00ff88; font-family:'Share Tech Mono',monospace; opacity:0.4; }

      /* Glitch effect on title */
      @keyframes glitch1 {
        0%,94%,100% { clip-path: none; transform: none; }
        95% { clip-path: inset(20% 0 60% 0); transform: translate(-3px, 0); }
        97% { clip-path: inset(60% 0 10% 0); transform: translate(3px, 0); }
        99% { clip-path: inset(40% 0 40% 0); transform: translate(-2px, 0); }
      }
      @keyframes glitch2 {
        0%,96%,100% { clip-path: none; transform: none; opacity:0; }
        97% { clip-path: inset(30% 0 50% 0); transform: translate(4px, 0); opacity:0.7; }
        99% { clip-path: inset(50% 0 20% 0); transform: translate(-4px, 0); opacity:0.5; }
      }
      .title-main { font-family: 'Orbitron', 'Arial Black', sans-serif; font-weight: 700; font-size: 42px; fill: #00ff88; letter-spacing: 4px; }
      .title-glitch1 { font-family: 'Orbitron', 'Arial Black', sans-serif; font-weight: 700; font-size: 42px; fill: #00ccff; letter-spacing: 4px; animation: glitch1 5s infinite; }
      .title-glitch2 { font-family: 'Orbitron', 'Arial Black', sans-serif; font-weight: 700; font-size: 42px; fill: #ff0066; letter-spacing: 4px; animation: glitch2 5s infinite; }
      .subtitle { font-family: 'Share Tech Mono', 'Courier New', monospace; font-size: 14px; fill: #4dbfff; letter-spacing: 6px; }

      /* Pulse rings */
      @keyframes pulse {
        0%   { r: 4; opacity: 1; }
        100% { r: 30; opacity: 0; }
      }
      .pulse-ring { animation: pulse 3s ease-out infinite; fill: none; stroke: #00ff88; stroke-width: 1; }
      .pulse-ring2 { animation: pulse 3s ease-out infinite 1s; fill: none; stroke: #00ccff; stroke-width: 0.8; }

      /* Hex grid nodes */
      @keyframes nodeFlash {
        0%,80%,100% { fill: #0d3b5e; }
        85% { fill: #00ff88; }
        90% { fill: #00ccff; }
      }
      .hex-node { animation: nodeFlash 4s infinite; }
      .hex-node2 { animation: nodeFlash 4s infinite 0.8s; }
      .hex-node3 { animation: nodeFlash 4s infinite 1.6s; }
      .hex-node4 { animation: nodeFlash 4s infinite 2.4s; }

      /* Shield icon pulse */
      @keyframes shieldGlow {
        0%,100% { filter: drop-shadow(0 0 4px #00ff88); opacity: 0.8; }
        50%      { filter: drop-shadow(0 0 12px #00ff88); opacity: 1; }
      }
      .shield { animation: shieldGlow 2.5s ease-in-out infinite; }

      /* Connecting lines flicker */
      @keyframes lineFade {
        0%,100%{ opacity:0.15; } 50%{ opacity:0.5; }
      }
      .conn-line { stroke: #00ff88; stroke-width:0.5; animation: lineFade 3s ease-in-out infinite; }
      .conn-line2 { stroke: #00ccff; stroke-width:0.5; animation: lineFade 3s ease-in-out infinite 1.5s; }
    </style>

    <!-- Gradients -->
    <linearGradient id="bgGrad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#020b18"/>
      <stop offset="100%" stop-color="#041428"/>
    </linearGradient>
    <linearGradient id="waveGrad1" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#003a6e" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#001a3a" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="waveGrad2" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#00255c" stop-opacity="0.85"/>
      <stop offset="100%" stop-color="#00122a" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="waveGrad3" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#001540" stop-opacity="0.9"/>
      <stop offset="100%" stop-color="#000a1e" stop-opacity="1"/>
    </linearGradient>
    <linearGradient id="scanGrad" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#00ff88" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00ff88" stop-opacity="0.05"/>
      <stop offset="100%" stop-color="#00ff88" stop-opacity="0"/>
    </linearGradient>
    <filter id="glow-green">
      <feGaussianBlur in="SourceGraphic" stdDeviation="3" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
    <filter id="glow-blue">
      <feGaussianBlur in="SourceGraphic" stdDeviation="2" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
    <filter id="title-glow">
      <feGaussianBlur in="SourceGraphic" stdDeviation="6" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
  </defs>

  <!-- Background -->
  <rect width="1200" height="300" fill="url(#bgGrad)"/>

  <!-- Grid -->
  <g opacity="0.4">
    <line class="grid-line" x1="0" y1="50"  x2="1200" y2="50"/>
    <line class="grid-line" x1="0" y1="100" x2="1200" y2="100"/>
    <line class="grid-line" x1="0" y1="150" x2="1200" y2="150"/>
    <line class="grid-line" x1="0" y1="200" x2="1200" y2="200"/>
    <line class="grid-line" x1="0" y1="250" x2="1200" y2="250"/>
    <line class="grid-line" x1="100"  y1="0" x2="100"  y2="300"/>
    <line class="grid-line" x1="200"  y1="0" x2="200"  y2="300"/>
    <line class="grid-line" x1="300"  y1="0" x2="300"  y2="300"/>
    <line class="grid-line" x1="400"  y1="0" x2="400"  y2="300"/>
    <line class="grid-line" x1="500"  y1="0" x2="500"  y2="300"/>
    <line class="grid-line" x1="600"  y1="0" x2="600"  y2="300"/>
    <line class="grid-line" x1="700"  y1="0" x2="700"  y2="300"/>
    <line class="grid-line" x1="800"  y1="0" x2="800"  y2="300"/>
    <line class="grid-line" x1="900"  y1="0" x2="900"  y2="300"/>
    <line class="grid-line" x1="1000" y1="0" x2="1000" y2="300"/>
    <line class="grid-line" x1="1100" y1="0" x2="1100" y2="300"/>
  </g>

  <!-- Binary rain columns -->
  <text class="rain1" x="60"   y="300">10110</text>
  <text class="rain2" x="140"  y="300">01001</text>
  <text class="rain3" x="230"  y="300">11010</text>
  <text class="rain4" x="390"  y="300">00111</text>
  <text class="rain5" x="480"  y="300">10001</text>
  <text class="rain1" x="680"  y="300">01110</text>
  <text class="rain2" x="760"  y="300">11001</text>
  <text class="rain3" x="870"  y="300">00101</text>
  <text class="rain4" x="990"  y="300">10110</text>
  <text class="rain5" x="1080" y="300">01011</text>
  <text class="rain1" x="1150" y="300">11100</text>

  <!-- Connecting circuit lines (left) -->
  <line class="conn-line"  x1="60"  y1="80"  x2="160" y2="80"/>
  <line class="conn-line"  x1="160" y1="80"  x2="160" y2="130"/>
  <line class="conn-line2" x1="80"  y1="130" x2="200" y2="130"/>
  <line class="conn-line"  x1="80"  y1="60"  x2="80"  y2="130"/>
  <circle cx="160" cy="80"  r="3" fill="#00ff88" opacity="0.7"/>
  <circle cx="80"  cy="130" r="3" fill="#00ccff" opacity="0.7"/>
  <circle cx="200" cy="130" r="2" fill="#00ff88" opacity="0.5"/>

  <!-- Connecting circuit lines (right) -->
  <line class="conn-line2" x1="1100" y1="80"  x2="1000" y2="80"/>
  <line class="conn-line2" x1="1000" y1="80"  x2="1000" y2="140"/>
  <line class="conn-line"  x1="1000" y1="140" x2="1140" y2="140"/>
  <line class="conn-line2" x1="1140" y1="60"  x2="1140" y2="140"/>
  <circle cx="1000" cy="80"  r="3" fill="#00ccff" opacity="0.7"/>
  <circle cx="1140" cy="140" r="3" fill="#00ff88" opacity="0.7"/>

  <!-- Hex nodes -->
  <circle class="hex-node"  cx="50"   cy="50"  r="5" opacity="0.7"/>
  <circle class="hex-node2" cx="1150" cy="50"  r="5" opacity="0.7"/>
  <circle class="hex-node3" cx="50"   cy="250" r="5" opacity="0.7"/>
  <circle class="hex-node4" cx="1150" cy="250" r="5" opacity="0.7"/>
  <circle class="hex-node"  cx="300"  cy="40"  r="3" opacity="0.6"/>
  <circle class="hex-node2" cx="900"  cy="40"  r="3" opacity="0.6"/>
  <circle class="hex-node3" cx="600"  cy="30"  r="4" opacity="0.5"/>

  <!-- Pulse rings (left shield position) -->
  <circle class="pulse-ring"  cx="100" cy="150" r="4"/>
  <circle class="pulse-ring2" cx="100" cy="150" r="4"/>
  <!-- Pulse rings (right) -->
  <circle class="pulse-ring"  cx="1100" cy="150" r="4"/>
  <circle class="pulse-ring2" cx="1100" cy="150" r="4"/>

  <!-- Floating particles -->
  <g class="p1"><circle cx="150"  cy="260" r="2.5" fill="#00ff88" opacity="0.8"/></g>
  <g class="p2"><circle cx="350"  cy="270" r="2"   fill="#00ccff" opacity="0.7"/></g>
  <g class="p3"><circle cx="550"  cy="265" r="3"   fill="#00ff88" opacity="0.6"/></g>
  <g class="p4"><circle cx="700"  cy="260" r="2"   fill="#00ccff" opacity="0.8"/></g>
  <g class="p5"><circle cx="850"  cy="270" r="2.5" fill="#00ff88" opacity="0.7"/></g>
  <g class="p6"><circle cx="1000" cy="265" r="2"   fill="#00ccff" opacity="0.6"/></g>
  <g class="p7"><circle cx="250"  cy="255" r="1.5" fill="#00ff88" opacity="0.9"/></g>
  <g class="p8"><circle cx="950"  cy="260" r="1.5" fill="#00ccff" opacity="0.8"/></g>

  <!-- Shield icon (left) -->
  <g class="shield" transform="translate(60, 115)">
    <path d="M20,0 L38,8 L38,22 Q38,34 20,42 Q2,34 2,22 L2,8 Z" fill="none" stroke="#00ff88" stroke-width="1.5" opacity="0.9"/>
    <path d="M20,0 L38,8 L38,22 Q38,34 20,42 Q2,34 2,22 L2,8 Z" fill="#00ff88" opacity="0.05"/>
    <path d="M12,20 L18,26 L28,14" fill="none" stroke="#00ff88" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
  </g>

  <!-- Shield icon (right) -->
  <g class="shield" transform="translate(1102, 115)">
    <path d="M20,0 L38,8 L38,22 Q38,34 20,42 Q2,34 2,22 L2,8 Z" fill="none" stroke="#00ccff" stroke-width="1.5" opacity="0.9"/>
    <path d="M20,0 L38,8 L38,22 Q38,34 20,42 Q2,34 2,22 L2,8 Z" fill="#00ccff" opacity="0.05"/>
    <path d="M12,20 L18,26 L28,14" fill="none" stroke="#00ccff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
  </g>

  <!-- Title (glitch layers) -->
  <g filter="url(#title-glow)">
    <text class="title-glitch2" x="600" y="140" text-anchor="middle">ADHITHYAN P K</text>
    <text class="title-glitch1" x="600" y="140" text-anchor="middle">ADHITHYAN P K</text>
    <text class="title-main"   x="600" y="140" text-anchor="middle">ADHITHYAN P K</text>
  </g>

  <!-- Subtitle -->
  <text class="subtitle" x="600" y="175" text-anchor="middle">CYBERSECURITY ENGINEER</text>

  <!-- Decorative bracket lines around subtitle -->
  <line x1="300" y1="182" x2="380" y2="182" stroke="#00ff88" stroke-width="0.8" opacity="0.4"/>
  <line x1="300" y1="182" x2="300" y2="178" stroke="#00ff88" stroke-width="0.8" opacity="0.4"/>
  <line x1="820" y1="182" x2="900" y2="182" stroke="#00ff88" stroke-width="0.8" opacity="0.4"/>
  <line x1="900" y1="182" x2="900" y2="178" stroke="#00ff88" stroke-width="0.8" opacity="0.4"/>

  <!-- Animated waves (back to front) -->
  <path class="wave3" fill="url(#waveGrad3)" d="M0,240 C180,215 360,260 540,235 C720,210 880,255 1060,230 C1130,215 1170,240 1200,240 L1200,300 L0,300 Z"/>
  <path class="wave2" fill="url(#waveGrad2)" d="M0,220 C200,195 350,245 500,220 C650,195 800,245 950,215 C1100,190 1160,225 1200,220 L1200,300 L0,300 Z"/>
  <path class="wave1" fill="url(#waveGrad1)" d="M0,200 C150,170 300,230 450,200 C600,170 750,230 900,200 C1050,170 1150,210 1200,200 L1200,300 L0,300 Z"/>

  <!-- Wave crest highlights -->
  <path fill="none" stroke="#00ccff" stroke-width="1" opacity="0.3"
    d="M0,200 C150,170 300,230 450,200 C600,170 750,230 900,200 C1050,170 1150,210 1200,200"/>

  <!-- Scan line sweep -->
  <rect width="1200" height="40" fill="url(#scanGrad)" style="animation: scan 6s linear infinite;"/>
</svg>
## 👋 Hi, I'm Adhi!

🌟 **Cybersecurity Student | Python Developer | Tech Explorer**

I'm currently a polytechnic student specializing in Electronics & Communication Engineering, with a deep curiosity for the world of cybersecurity. My journey goes beyond classrooms: I dive into coding with Python, experiment with AI, and even enjoy the art of video editing.

### About Me

- 🔐 Aspiring Ethical Hacker, passionate about building and breaking things to understand how technology works.
- 🧑‍💻 Python enthusiast—I'm always exploring new ways to leverage it for automation, security, and creative applications.
- 🎬 I like mixing tech with creativity—coding, video editing, and playing with AI.
- 🚀 Always eager to learn about the latest trends and breakthroughs in technology.

### My Vision

> To become a skilled ethical hacker protecting the systems and innovations of tomorrow, while continuously learning and experimenting with new tech.

---
🌐 Socials:
[Facebook](https://facebook.com/Adhithyan pk) Instagram

💻 Tech Stack:
Python

📊 GitHub Stats:







