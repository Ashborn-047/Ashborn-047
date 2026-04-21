<svg width="900" height="32" viewBox="0 0 900 32" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      /* Each divider gets 70s, 53s offset — unique from all others */
      .line-left  { animation: lineC 70s 53s steps(1) infinite, linePulse 3s ease-in-out infinite alternate; }
      .line-right { animation: lineC 70s 53s steps(1) infinite, linePulse 3s ease-in-out infinite alternate 1.5s; }
      @keyframes lineC {
        0%  { stroke: #00d4ff; }
        25% { stroke: #cc44ff; }
        50% { stroke: #ffaa00; }
        75% { stroke: #00ffcc; }
      }
      @keyframes linePulse { from{stroke-opacity:.2;} to{stroke-opacity:.7;} }

      .center-dot { animation: dotC 70s 53s steps(1) infinite, dotPulse 2s ease-in-out infinite; }
      @keyframes dotC { 0%{fill:#00d4ff;} 25%{fill:#cc44ff;} 50%{fill:#ffaa00;} 75%{fill:#00ffcc;} }
      @keyframes dotPulse { 0%,100%{r:4; opacity:1;} 50%{r:6; opacity:.5;} }

      .side-dot { animation: dotC 70s 53s steps(1) infinite, dotPulse 2s ease-in-out infinite; }

      .label { animation: labelC 70s 53s steps(1) infinite, labelFade 3s ease-in-out infinite alternate; }
      @keyframes labelC { 0%{fill:#00d4ff;} 25%{fill:#cc44ff;} 50%{fill:#ffaa00;} 75%{fill:#00ffcc;} }
      @keyframes labelFade { from{opacity:.3;} to{opacity:.8;} }

      .travel { animation: travelX 4s ease-in-out infinite; }
      .travel-r { animation: travelXR 4s 2s ease-in-out infinite; }
      @keyframes travelX  { 0%{transform:translateX(0);   opacity:0;} 10%{opacity:.8;} 90%{opacity:.4;} 100%{transform:translateX(380px); opacity:0;} }
      @keyframes travelXR { 0%{transform:translateX(0);   opacity:0;} 10%{opacity:.8;} 90%{opacity:.4;} 100%{transform:translateX(-380px);opacity:0;} }
    </style>
    <linearGradient id="divLeft" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="transparent"/>
      <stop offset="100%" stop-color="currentColor"/>
    </linearGradient>
    <linearGradient id="divRight" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="currentColor"/>
      <stop offset="100%" stop-color="transparent"/>
    </linearGradient>
  </defs>

  <!-- Left line -->
  <line x1="30" y1="16" x2="416" y2="16" stroke-width="1" class="line-left"/>
  <!-- Right line -->
  <line x1="484" y1="16" x2="870" y2="16" stroke-width="1" class="line-right"/>

  <!-- Center cluster -->
  <circle cx="450" cy="16" r="4" class="center-dot"/>
  <circle cx="432" cy="16" r="2" class="side-dot" opacity=".6" style="animation-delay:.2s"/>
  <circle cx="468" cy="16" r="2" class="side-dot" opacity=".6" style="animation-delay:.4s"/>
  <circle cx="418" cy="16" r="1.5" class="side-dot" opacity=".3" style="animation-delay:.6s"/>
  <circle cx="482" cy="16" r="1.5" class="side-dot" opacity=".3" style="animation-delay:.8s"/>

  <!-- Traveling particles -->
  <circle cx="70" cy="16" r="2" class="center-dot travel" opacity="0"/>
  <circle cx="830" cy="16" r="2" class="center-dot travel-r" opacity="0"/>
</svg>