<svg width="700" height="340" viewBox="0 0 700 340" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&amp;display=swap');

      .line1  { animation: appear 0.1s 0.5s forwards;  opacity: 0; }
      .line2  { animation: appear 0.1s 1.2s forwards;  opacity: 0; }
      .line3  { animation: appear 0.1s 1.9s forwards;  opacity: 0; }
      .line4  { animation: appear 0.1s 2.6s forwards;  opacity: 0; }
      .line5  { animation: appear 0.1s 3.3s forwards;  opacity: 0; }
      .line6  { animation: appear 0.1s 4.0s forwards;  opacity: 0; }
      .line7  { animation: appear 0.1s 4.7s forwards;  opacity: 0; }
      .line8  { animation: appear 0.1s 5.4s forwards;  opacity: 0; }
      .line9  { animation: appear 0.1s 6.1s forwards;  opacity: 0; }
      .line10 { animation: appear 0.1s 6.8s forwards;  opacity: 0; }

      @keyframes appear {
        to { opacity: 1; }
      }

      .cursor-blink {
        animation: blink 1s step-end infinite;
      }
      @keyframes blink {
        0%, 100% { opacity: 1; }
        50%       { opacity: 0; }
      }

      .border-glow {
        animation: glow 3s ease-in-out infinite alternate;
      }
      @keyframes glow {
        from { stroke-opacity: 0.5; filter: drop-shadow(0 0 2px #00d4ff); }
        to   { stroke-opacity: 1.0; filter: drop-shadow(0 0 8px #00d4ff); }
      }

      .dot-pulse {
        animation: dotpulse 2s ease-in-out infinite;
      }
      @keyframes dotpulse {
        0%, 100% { opacity: 1;   r: 5; }
        50%       { opacity: 0.5; r: 4; }
      }
    </style>

    <linearGradient id="termBg" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%"   stop-color="#080f1e"/>
      <stop offset="100%" stop-color="#040a16"/>
    </linearGradient>
    <linearGradient id="titleBar" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%"   stop-color="#0a1628"/>
      <stop offset="100%" stop-color="#0d1e35"/>
    </linearGradient>
  </defs>

  <!-- Terminal window -->
  <rect width="700" height="340" rx="10" fill="#040a16"/>
  <rect width="700" height="340" rx="10" fill="none" stroke="#00d4ff" stroke-width="1.2" class="border-glow"/>

  <!-- Title bar -->
  <rect x="0" y="0" width="700" height="36" rx="10" fill="url(#titleBar)"/>
  <rect x="0" y="26" width="700" height="10" fill="url(#titleBar)"/>

  <!-- Title bar border -->
  <line x1="0" y1="36" x2="700" y2="36" stroke="#0d3a6e" stroke-width="1"/>

  <!-- Traffic light dots -->
  <circle cx="22" cy="18" r="5" fill="#ff5f57" class="dot-pulse" style="animation-delay:0s"/>
  <circle cx="42" cy="18" r="5" fill="#febc2e" class="dot-pulse" style="animation-delay:0.3s"/>
  <circle cx="62" cy="18" r="5" fill="#28c840" class="dot-pulse" style="animation-delay:0.6s"/>

  <!-- Terminal title -->
  <text x="350" y="23" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="12" fill="#4da6ff" letter-spacing="2">ashborn@matrix:~</text>

  <!-- Terminal content -->
  <g font-family="'Share Tech Mono', monospace" font-size="13.5">

    <!-- Line 1: prompt + command -->
    <text x="24" y="68" class="line1">
      <tspan fill="#00ff88">ashborn</tspan>
      <tspan fill="#4da6ff">@matrix</tspan>
      <tspan fill="#ffffff">:</tspan>
      <tspan fill="#00d4ff">~</tspan>
      <tspan fill="#ffffff">$ </tspan>
      <tspan fill="#e2e8f0">cat profile.json</tspan>
    </text>

    <!-- Line 2: opening brace -->
    <text x="24" y="92" class="line2" fill="#6b7280">{</text>

    <!-- Line 3 -->
    <text x="24" y="114" class="line3">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"role"</tspan>
      <tspan fill="#6b7280">: </tspan>
      <tspan fill="#00d4ff">"Frontend Architect &amp; AI Orchestrator"</tspan>
      <tspan fill="#6b7280">,</tspan>
    </text>

    <!-- Line 4 -->
    <text x="24" y="136" class="line4">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"rank"</tspan>
      <tspan fill="#6b7280">: </tspan>
      <tspan fill="#febc2e">"S-Tier"</tspan>
      <tspan fill="#6b7280">,</tspan>
    </text>

    <!-- Line 5 -->
    <text x="24" y="158" class="line5">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"stack"</tspan>
      <tspan fill="#6b7280">: [</tspan>
      <tspan fill="#00d4ff">"Next.js"</tspan>
      <tspan fill="#6b7280">, </tspan>
      <tspan fill="#00d4ff">"TypeScript"</tspan>
      <tspan fill="#6b7280">, </tspan>
      <tspan fill="#00d4ff">"AI Agents"</tspan>
      <tspan fill="#6b7280">],</tspan>
    </text>

    <!-- Line 6 -->
    <text x="24" y="180" class="line6">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"philosophy"</tspan>
      <tspan fill="#6b7280">: </tspan>
      <tspan fill="#00ff88">"Elegant Scalability &gt; Brute Force"</tspan>
      <tspan fill="#6b7280">,</tspan>
    </text>

    <!-- Line 7 -->
    <text x="24" y="202" class="line7">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"status"</tspan>
      <tspan fill="#6b7280">: </tspan>
      <tspan fill="#28c840">"building_the_future"</tspan>
      <tspan fill="#6b7280">,</tspan>
    </text>

    <!-- Line 8 -->
    <text x="24" y="224" class="line8">
      <tspan fill="#6b7280">  </tspan>
      <tspan fill="#7c3aed">"open_to"</tspan>
      <tspan fill="#6b7280">: [</tspan>
      <tspan fill="#00d4ff">"collab"</tspan>
      <tspan fill="#6b7280">, </tspan>
      <tspan fill="#00d4ff">"OSS"</tspan>
      <tspan fill="#6b7280">, </tspan>
      <tspan fill="#00d4ff">"ambitious_builds"</tspan>
      <tspan fill="#6b7280">]</tspan>
    </text>

    <!-- Line 9: closing brace -->
    <text x="24" y="248" class="line9" fill="#6b7280">}</text>

    <!-- Line 10: next prompt -->
    <text x="24" y="278" class="line10">
      <tspan fill="#00ff88">ashborn</tspan>
      <tspan fill="#4da6ff">@matrix</tspan>
      <tspan fill="#ffffff">:</tspan>
      <tspan fill="#00d4ff">~</tspan>
      <tspan fill="#ffffff">$ </tspan>
      <tspan fill="#e2e8f0" class="cursor-blink">█</tspan>
    </text>
  </g>

  <!-- Scanline overlay -->
  <rect x="0" y="36" width="700" height="304" rx="0"
        fill="url(#termBg)" opacity="0.05"
        style="pointer-events:none"/>
</svg>