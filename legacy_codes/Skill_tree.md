<svg width="900" height="420" viewBox="0 0 900 420" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&amp;family=Orbitron:wght@600;700&amp;display=swap');

      /* Independent — 95s, 29s offset */
      .bg { animation: bgC 95s 29s steps(1) infinite; }
      @keyframes bgC { 0%{fill:#020818;} 25%{fill:#0d0418;} 50%{fill:#120a00;} 75%{fill:#001412;} }

      .grid-line { animation: gridC 95s 29s steps(1) infinite; }
      @keyframes gridC { 0%{stroke:#0a2040;} 25%{stroke:#2a0a40;} 50%{stroke:#2a1500;} 75%{stroke:#003830;} }

      .border-frame { animation: borderC 95s 29s steps(1) infinite, bPulse 3s ease-in-out infinite alternate; }
      @keyframes borderC { 0%{stroke:#0d3a6e;} 25%{stroke:#4a1570;} 50%{stroke:#5a3000;} 75%{stroke:#005540;} }
      @keyframes bPulse { from{stroke-opacity:.3;} to{stroke-opacity:1;} }

      .accent-fill  { animation: accentF 95s 29s steps(1) infinite; }
      .accent-stroke { animation: accentS 95s 29s steps(1) infinite; }
      .accent-s-pulse { animation: accentS 95s 29s steps(1) infinite, bPulse 3s ease-in-out infinite alternate; }
      @keyframes accentF { 0%{fill:#00d4ff;} 25%{fill:#cc44ff;} 50%{fill:#ffaa00;} 75%{fill:#00ffcc;} }
      @keyframes accentS { 0%{stroke:#00d4ff;} 25%{stroke:#cc44ff;} 50%{stroke:#ffaa00;} 75%{stroke:#00ffcc;} }

      .header-text { animation: hC 95s 29s steps(1) infinite, hGlow 3s ease-in-out infinite alternate; }
      @keyframes hC { 0%{fill:#00d4ff;} 25%{fill:#cc44ff;} 50%{fill:#ffaa00;} 75%{fill:#00ffcc;} }
      @keyframes hGlow { from{filter:drop-shadow(0 0 4px currentColor);} to{filter:drop-shadow(0 0 14px currentColor);} }

      /* ── NODE STYLES ── */
      /* Root node */
      .node-root-bg { animation: rootBgC 95s 29s steps(1) infinite; }
      @keyframes rootBgC { 0%{fill:#001830;} 25%{fill:#1a0030;} 50%{fill:#1e1000;} 75%{fill:#002820;} }
      .node-root-border { animation: accentS 95s 29s steps(1) infinite, nodeGlow 2s ease-in-out infinite alternate; stroke-width:2; }
      @keyframes nodeGlow { from{stroke-opacity:.5; filter:drop-shadow(0 0 3px currentColor);} to{stroke-opacity:1; filter:drop-shadow(0 0 10px currentColor);} }

      /* Branch nodes (frontend/agentic) */
      .node-branch-bg { animation: branchBgC 95s 29s steps(1) infinite; }
      @keyframes branchBgC { 0%{fill:#030e22;} 25%{fill:#0e0322;} 50%{fill:#140c00;} 75%{fill:#001a16;} }
      .node-branch-border { animation: accentS 95s 29s steps(1) infinite, nodeGlow2 2.5s 0.3s ease-in-out infinite alternate; stroke-width:1.5; }
      @keyframes nodeGlow2 { from{stroke-opacity:.3;} to{stroke-opacity:.8;} }

      /* Leaf nodes */
      .node-leaf-bg { animation: leafBgC 95s 29s steps(1) infinite; }
      @keyframes leafBgC { 0%{fill:#020c1c;} 25%{fill:#0c021c;} 50%{fill:#100900;} 75%{fill:#001612;} }
      .node-leaf-border { animation: accentS 95s 29s steps(1) infinite; stroke-width:1; opacity:.5; }

      /* Outcome node */
      .node-out-bg { animation: rootBgC 95s 29s steps(1) infinite; }
      .node-out-border { animation: accentS 95s 29s steps(1) infinite, nodeGlow 1.8s 0.6s ease-in-out infinite alternate; stroke-width:2; }

      /* ── CONNECTING LINES ── */
      /* Animated dash-draw effect */
      .conn { animation: connDraw 1.5s ease-out both; }
      .c1  { animation-delay:.3s; }
      .c2  { animation-delay:.5s; }
      .c3  { animation-delay:.7s; }
      .c4  { animation-delay:.9s; }
      .c5  { animation-delay:1.1s; }
      .c6  { animation-delay:1.3s; }
      .c7  { animation-delay:1.5s; }
      .c8  { animation-delay:1.7s; }
      @keyframes connDraw {
        from { stroke-dashoffset: 300; opacity:0; }
        to   { stroke-dashoffset: 0;   opacity:1; }
      }
      /* Pulse travel along lines */
      .travel-dot { animation: travelDot 3s ease-in-out infinite; }
      .td1 { animation-delay:0s; }
      .td2 { animation-delay:.8s; }
      .td3 { animation-delay:1.6s; }
      .td4 { animation-delay:2.4s; }
      @keyframes travelDot { 0%,100%{opacity:0; r:2;} 10%{opacity:1; r:3;} 90%{opacity:.4; r:2;} }

      .conn-line { animation: accentS 95s 29s steps(1) infinite, connDraw 1.5s ease-out both; stroke-width:1.5; stroke-dasharray:300; fill:none; }

      /* Node text */
      .node-title { font-family:'Orbitron', monospace; font-size:11px; font-weight:600; fill:#e2e8f0; }
      .node-sub   { font-family:'Share Tech Mono', monospace; font-size:9px; fill:#5a7a8a; }
      .node-rank  { font-family:'Share Tech Mono', monospace; font-size:8px; }
      .node-rank-accent { animation: accentF 95s 29s steps(1) infinite; }

      /* Node appear */
      .na1 { animation: nAppear .4s .2s ease-out both; }
      .na2 { animation: nAppear .4s .5s ease-out both; }
      .na3 { animation: nAppear .4s .8s ease-out both; }
      .na4 { animation: nAppear .4s .6s ease-out both; }
      .na5 { animation: nAppear .4s .9s ease-out both; }
      .na6 { animation: nAppear .4s 1.1s ease-out both; }
      .na7 { animation: nAppear .4s 1.3s ease-out both; }
      .na8 { animation: nAppear .4s 1.5s ease-out both; }
      .na9 { animation: nAppear .4s 1.7s ease-out both; }
      @keyframes nAppear { from{opacity:0; transform:scale(.9);} to{opacity:1; transform:scale(1);} }

      .scanline { animation: accentF 95s 29s steps(1) infinite, scan 10s linear infinite; }
      @keyframes scan { 0%{transform:translateY(-4px);opacity:.025;} 100%{transform:translateY(424px);opacity:.025;} }

      .bracket-ping { animation: accentF 95s 29s steps(1) infinite, ping 2s ease-out infinite; }
      @keyframes ping { 0%{r:3;opacity:1;} 100%{r:10;opacity:0;} }

      .badge-bg { animation: badgeBgC 95s 29s steps(1) infinite; }
      @keyframes badgeBgC { 0%{fill:#001830;} 25%{fill:#1a0030;} 50%{fill:#1e1000;} 75%{fill:#002820;} }
      .b0{animation:sB0 95s 29s steps(1) infinite;} @keyframes sB0{0%{opacity:1;}25%,100%{opacity:0;}}
      .b1{animation:sB1 95s 29s steps(1) infinite;} @keyframes sB1{25%{opacity:1;}0%,50%,100%{opacity:0;}}
      .b2{animation:sB2 95s 29s steps(1) infinite;} @keyframes sB2{50%{opacity:1;}0%,25%,75%,100%{opacity:0;}}
      .b3{animation:sB3 95s 29s steps(1) infinite;} @keyframes sB3{75%,99%{opacity:1;}0%,50%,100%{opacity:0;}}
    </style>

    <!-- Arrow marker -->
    <marker id="arrow" markerWidth="6" markerHeight="6" refX="5" refY="3" orient="auto">
      <path d="M0,0 L0,6 L6,3 z" fill="#00d4ff" opacity=".6"/>
    </marker>
  </defs>

  <rect width="900" height="420" rx="10" class="bg"/>

  <!-- Grid -->
  <g stroke-width=".5" opacity=".35" class="grid-line">
    <line x1="0" y1="60"  x2="900" y2="60"/>
    <line x1="0" y1="150" x2="900" y2="150"/>
    <line x1="0" y1="240" x2="900" y2="240"/>
    <line x1="0" y1="330" x2="900" y2="330"/>
    <line x1="225" y1="60" x2="225" y2="420"/>
    <line x1="450" y1="60" x2="450" y2="420"/>
    <line x1="675" y1="60" x2="675" y2="420"/>
  </g>

  <rect class="scanline" x="0" y="0" width="900" height="3" rx="1"/>

  <!-- Corner brackets -->
  <g fill="none" stroke-width="1.2" class="accent-s-pulse">
    <line x1="12" y1="12" x2="38" y2="12"/><line x1="12" y1="12" x2="12" y2="38"/>
    <line x1="888" y1="12" x2="862" y2="12"/><line x1="888" y1="12" x2="888" y2="38"/>
    <line x1="12" y1="408" x2="38" y2="408"/><line x1="12" y1="408" x2="12" y2="382"/>
    <line x1="888" y1="408" x2="862" y2="408"/><line x1="888" y1="408" x2="888" y2="382"/>
  </g>
  <circle cx="12"  cy="12"  r="3" class="bracket-ping" style="animation-delay:0s,0s"/>
  <circle cx="888" cy="12"  r="3" class="bracket-ping" style="animation-delay:0s,.7s"/>
  <circle cx="12"  cy="408" r="3" class="bracket-ping" style="animation-delay:0s,1.4s"/>
  <circle cx="888" cy="408" r="3" class="bracket-ping" style="animation-delay:0s,2.1s"/>

  <!-- Header -->
  <text x="26" y="42" font-family="'Orbitron', monospace" font-size="15" font-weight="600" letter-spacing="2" class="header-text">🌲 SKILL TREE — NODE GRAPH</text>

  <!-- Theme badge -->
  <rect x="726" y="20" width="148" height="18" rx="4" class="badge-bg"/>
  <rect x="726" y="20" width="148" height="18" rx="4" fill="none" class="accent-stroke" stroke-width=".8"/>
  <text x="800" y="33" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="9" letter-spacing="1" class="b0" fill="#00d4ff">◈ MIDNIGHT BLUE</text>
  <text x="800" y="33" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="9" letter-spacing="1" class="b1" fill="#cc44ff">◈ NEON PURPLE</text>
  <text x="800" y="33" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="9" letter-spacing="1" class="b2" fill="#ffaa00">◈ AMBER GOLD</text>
  <text x="800" y="33" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="9" letter-spacing="1" class="b3" fill="#00ffcc">◈ ARCTIC TEAL</text>

  <line x1="26" y1="52" x2="874" y2="52" stroke-width="1" class="accent-stroke" opacity=".35"/>

  <!--
    LAYOUT:
    Row 1 (y~100): ROOT — Hero Initiation (center: 450,100)
    Row 2 (y~190): BRANCH — Frontend Sorcery (240,195) | Agentic Mastery (660,195)
    Row 3 (y~285): LEAF — React/Next (160,285) | Tailwind (320,285) | Claude Agents (580,285) | Cursor (740,285)
    Row 4 (y~375): OUTCOME — Full Stack Legend (450,375)
  -->

  <!-- ── CONNECTING LINES ── -->
  <!-- Root → Frontend branch -->
  <path class="conn-line c1" d="M 450,130 C 450,165 240,165 240,180" stroke-dasharray="300"/>
  <!-- Root → Agentic branch -->
  <path class="conn-line c2" d="M 450,130 C 450,165 660,165 660,180" stroke-dasharray="300"/>

  <!-- Frontend → React -->
  <path class="conn-line c3" d="M 240,218 C 240,250 160,250 160,268" stroke-dasharray="200"/>
  <!-- Frontend → Tailwind -->
  <path class="conn-line c4" d="M 240,218 C 240,250 320,250 320,268" stroke-dasharray="200"/>
  <!-- Agentic → Claude -->
  <path class="conn-line c5" d="M 660,218 C 660,250 580,250 580,268" stroke-dasharray="200"/>
  <!-- Agentic → Cursor -->
  <path class="conn-line c6" d="M 660,218 C 660,250 740,250 740,268" stroke-dasharray="200"/>

  <!-- React → Outcome -->
  <path class="conn-line c7" d="M 160,310 C 160,345 450,345 450,360" stroke-dasharray="400"/>
  <!-- Tailwind → Outcome -->
  <path class="conn-line c7" d="M 320,310 C 320,345 450,345 450,360" stroke-dasharray="300"/>
  <!-- Claude → Outcome -->
  <path class="conn-line c8" d="M 580,310 C 580,345 450,345 450,360" stroke-dasharray="300"/>
  <!-- Cursor → Outcome -->
  <path class="conn-line c8" d="M 740,310 C 740,345 450,345 450,360" stroke-dasharray="400"/>

  <!-- ── TRAVEL DOTS on connections ── -->
  <circle r="3" fill="#00d4ff" opacity="0" class="travel-dot td1">
    <animateMotion dur="3s" repeatCount="indefinite" begin="0s">
      <mpath href="#path-root-fe"/>
    </animateMotion>
  </circle>
  <circle r="3" fill="#00d4ff" opacity="0" class="travel-dot td2">
    <animateMotion dur="3s" repeatCount="indefinite" begin="1s">
      <mpath href="#path-root-ag"/>
    </animateMotion>
  </circle>

  <!-- ── NODE: ROOT — Hero Initiation ── -->
  <g class="na1">
    <rect x="360" y="68" width="180" height="62" rx="10" class="node-root-bg"/>
    <rect x="360" y="68" width="180" height="62" rx="10" fill="none" class="node-root-border"/>
    <text x="450" y="88" text-anchor="middle" class="node-title">⚡ HERO INITIATION</text>
    <text x="450" y="103" text-anchor="middle" class="node-sub">Origin Class</text>
    <text x="450" y="120" text-anchor="middle" class="node-rank node-rank-accent">[ RANK: LEGENDARY ]</text>
  </g>

  <!-- ── NODE: BRANCH — Frontend Sorcery ── -->
  <g class="na2">
    <rect x="148" y="180" width="184" height="58" rx="8" class="node-branch-bg"/>
    <rect x="148" y="180" width="184" height="58" rx="8" fill="none" class="node-branch-border"/>
    <text x="240" y="200" text-anchor="middle" class="node-title">🔮 FRONTEND FORGE</text>
    <text x="240" y="216" text-anchor="middle" class="node-sub">React · Next.js · Tailwind</text>
    <text x="240" y="230" text-anchor="middle" class="node-rank node-rank-accent">[ S-TIER ]</text>
  </g>

  <!-- ── NODE: BRANCH — Agentic Mastery ── -->
  <g class="na3">
    <rect x="568" y="180" width="184" height="58" rx="8" class="node-branch-bg"/>
    <rect x="568" y="180" width="184" height="58" rx="8" fill="none" class="node-branch-border"/>
    <text x="660" y="200" text-anchor="middle" class="node-title">🤖 AGENTIC MASTERY</text>
    <text x="660" y="216" text-anchor="middle" class="node-sub">Claude · Python · LangChain</text>
    <text x="660" y="230" text-anchor="middle" class="node-rank node-rank-accent">[ ANCIENT GRIMOIRE ]</text>
  </g>

  <!-- ── LEAF NODES ── -->
  <!-- React/Next.js -->
  <g class="na4">
    <rect x="88" y="268" width="144" height="52" rx="6" class="node-leaf-bg"/>
    <rect x="88" y="268" width="144" height="52" rx="6" fill="none" class="node-leaf-border"/>
    <text x="160" y="287" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="11" fill="#c0ccd8">React / Next.js</text>
    <text x="160" y="302" text-anchor="middle" class="node-sub">App Router · RSC · SSR</text>
    <text x="160" y="314" text-anchor="middle" class="node-rank node-rank-accent" font-size="8">[ MASTERED ]</text>
  </g>

  <!-- Tailwind -->
  <g class="na5">
    <rect x="248" y="268" width="144" height="52" rx="6" class="node-leaf-bg"/>
    <rect x="248" y="268" width="144" height="52" rx="6" fill="none" class="node-leaf-border"/>
    <text x="320" y="287" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="11" fill="#c0ccd8">Tailwind + Motion</text>
    <text x="320" y="302" text-anchor="middle" class="node-sub">Framer · WebGL · GSAP</text>
    <text x="320" y="314" text-anchor="middle" class="node-rank node-rank-accent" font-size="8">[ MASTERED ]</text>
  </g>

  <!-- Claude Agents -->
  <g class="na6">
    <rect x="508" y="268" width="144" height="52" rx="6" class="node-leaf-bg"/>
    <rect x="508" y="268" width="144" height="52" rx="6" fill="none" class="node-leaf-border"/>
    <text x="580" y="287" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="11" fill="#c0ccd8">Claude Agents</text>
    <text x="580" y="302" text-anchor="middle" class="node-sub">Multi-agent · Orchestration</text>
    <text x="580" y="314" text-anchor="middle" class="node-rank node-rank-accent" font-size="8">[ UNLOCKED ]</text>
  </g>

  <!-- Cursor Flow -->
  <g class="na7">
    <rect x="668" y="268" width="144" height="52" rx="6" class="node-leaf-bg"/>
    <rect x="668" y="268" width="144" height="52" rx="6" fill="none" class="node-leaf-border"/>
    <text x="740" y="287" text-anchor="middle" font-family="'Share Tech Mono', monospace" font-size="11" fill="#c0ccd8">Cursor Flow</text>
    <text x="740" y="302" text-anchor="middle" class="node-sub">AI-native · Vibe coding</text>
    <text x="740" y="314" text-anchor="middle" class="node-rank node-rank-accent" font-size="8">[ UNLOCKED ]</text>
  </g>

  <!-- ── NODE: OUTCOME — Full Stack Legend ── -->
  <g class="na9">
    <rect x="320" y="360" width="260" height="44" rx="10" class="node-out-bg"/>
    <rect x="320" y="360" width="260" height="44" rx="10" fill="none" class="node-out-border"/>
    <text x="450" y="379" text-anchor="middle" font-family="'Orbitron', monospace" font-size="13" font-weight="700" class="accent-fill">⚡ FULL STACK LEGEND</text>
    <text x="450" y="396" text-anchor="middle" class="node-sub" font-size="10">Rank: S-Tier  ·  Status: Ascending</text>
  </g>

  <!-- Level indicator dots (bottom left) -->
  <g font-family="'Share Tech Mono', monospace" font-size="9">
    <circle cx="34" cy="400" r="4" fill="#00ff88"/>
    <text x="44" y="404" fill="#4a7a5a">MASTERED</text>
    <circle cx="134" cy="400" r="4" fill="#00d4ff" opacity=".6"/>
    <text x="144" y="404" fill="#4a6a7a">UNLOCKED</text>
    <circle cx="234" cy="400" r="4" fill="#2a3a4a"/>
    <text x="244" y="404" fill="#3a4a5a">LOCKED</text>
  </g>

  <rect x="2" y="2" width="896" height="416" rx="9" fill="none" stroke-width="1.5" class="border-frame"/>
</svg>