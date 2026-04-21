<svg width="900" height="60" viewBox="0 0 900 60" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&amp;display=swap');

      .dot-on {
        animation: ondot 2s ease-in-out infinite;
      }
      @keyframes ondot {
        0%, 100% { r: 4; opacity: 1; }
        50%       { r: 6; opacity: 0.6; }
      }

      .slide-in {
        animation: slidein 1s ease-out forwards;
        opacity: 0;
        transform: translateX(-10px);
      }
      .si1 { animation-delay: 0.1s; }
      .si2 { animation-delay: 0.3s; }
      .si3 { animation-delay: 0.5s; }
      .si4 { animation-delay: 0.7s; }
      .si5 { animation-delay: 0.9s; }
      @keyframes slidein {
        to { opacity: 1; transform: translateX(0); }
      }

      .border-anim {
        animation: borderflash 3s ease-in-out infinite alternate;
      }
      @keyframes borderflash {
        from { stroke-opacity: 0.3; }
        to   { stroke-opacity: 0.9; }
      }

      .progress-bar {
        animation: progressfill 3s 0.5s ease-out forwards;
        width: 0;
      }
      @keyframes progressfill {
        to { width: var(--pw); }
      }
    </style>
    <linearGradient id="statusBg" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%"   stop-color="#040d1e"/>
      <stop offset="50%"  stop-color="#060f24"/>
      <stop offset="100%" stop-color="#040d1e"/>
    </linearGradient>
    <linearGradient id="pbar" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%"   stop-color="#00d4ff"/>
      <stop offset="100%" stop-color="#0044cc"/>
    </linearGradient>
  </defs>

  <rect width="900" height="60" rx="8" fill="url(#statusBg)"/>
  <rect width="900" height="60" rx="8" fill="none" stroke="#00d4ff" stroke-width="1" class="border-anim"/>

  <!-- Dividers -->
  <line x1="200" y1="8"  x2="200" y2="52" stroke="#0d3060" stroke-width="1"/>
  <line x1="400" y1="8"  x2="400" y2="52" stroke="#0d3060" stroke-width="1"/>
  <line x1="600" y1="8"  x2="600" y2="52" stroke="#0d3060" stroke-width="1"/>
  <line x1="760" y1="8"  x2="760" y2="52" stroke="#0d3060" stroke-width="1"/>

  <!-- Status 1: Online -->
  <circle cx="30" cy="30" r="4" fill="#00ff88" class="dot-on"/>
  <text x="44" y="26" font-family="'Share Tech Mono', monospace" font-size="9" fill="#6b7280" class="slide-in si1">STATUS</text>
  <text x="44" y="42" font-family="'Share Tech Mono', monospace" font-size="12" fill="#00ff88" class="slide-in si1">ONLINE</text>

  <!-- Status 2: Current focus -->
  <text x="220" y="26" font-family="'Share Tech Mono', monospace" font-size="9" fill="#6b7280" class="slide-in si2">CURRENT MISSION</text>
  <text x="220" y="42" font-family="'Share Tech Mono', monospace" font-size="11" fill="#00d4ff" class="slide-in si2">AI Agent Systems</text>

  <!-- Status 3: Build progress -->
  <text x="420" y="22" font-family="'Share Tech Mono', monospace" font-size="9" fill="#6b7280" class="slide-in si3">BUILD PROGRESS</text>
  <rect x="420" y="28" width="160" height="6" rx="3" fill="#0a2040"/>
  <rect x="420" y="28" height="6" rx="3" fill="url(#pbar)" class="progress-bar" style="--pw:136px"/>
  <text x="420" y="48" font-family="'Share Tech Mono', monospace" font-size="9" fill="#4da6ff" class="slide-in si3">85% — Vibe→Code Pipeline</text>

  <!-- Status 4: Coffee -->
  <text x="620" y="26" font-family="'Share Tech Mono', monospace" font-size="9" fill="#6b7280" class="slide-in si4">COFFEE LEVEL</text>
  <rect x="620" y="32" width="120" height="6" rx="3" fill="#0a2040"/>
  <rect x="620" y="32" height="6" rx="3" fill="#ff8c42" class="progress-bar" style="--pw:40px"/>
  <text x="620" y="48" font-family="'Share Tech Mono', monospace" font-size="9" fill="#ff8c42" class="slide-in si4">CRITICAL ☕</text>

  <!-- Status 5: Open to collab -->
  <circle cx="778" cy="22" r="4" fill="#00d4ff" class="dot-on" style="animation-delay:1s"/>
  <text x="792" y="26" font-family="'Share Tech Mono', monospace" font-size="9" fill="#6b7280" class="slide-in si5">COLLAB</text>
  <text x="778" y="42" font-family="'Share Tech Mono', monospace" font-size="11" fill="#4da6ff" class="slide-in si5">OPEN</text>
</svg>