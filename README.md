<svg width="760" height="298" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      text { font-family: 'Courier New', Courier, monospace; font-size: 13px; }
      .l1  { opacity:0; animation: show .04s  0.5s both; }
      .l2  { opacity:0; animation: show .04s  1.4s both; }
      .l3  { opacity:0; animation: show .04s  2.3s both; }
      .l4  { opacity:0; animation: show .04s  2.9s both; }
      .l5  { opacity:0; animation: show .04s  3.3s both; }
      .l6  { opacity:0; animation: show .04s  3.7s both; }
      .l7  { opacity:0; animation: show .04s  4.1s both; }
      .l8  { opacity:0; animation: show .04s  4.8s both; }
      .l9  { opacity:0; animation: show .04s  5.4s both; }
      .l10 { opacity:0; animation: show .04s  5.9s both; }
      .l11 { opacity:0; animation: show .04s  6.4s both; }
      .cur { opacity:0; animation: blink 1s   6.5s infinite; }
      @keyframes show  { to { opacity: 1; } }
      @keyframes blink { 0%,49%{opacity:1} 50%,100%{opacity:0} }
    </style>
    <!-- Scanline overlay pattern for retro CRT feel -->
    <pattern id="scan" width="1" height="3" patternUnits="userSpaceOnUse">
      <rect width="1" height="1" fill="#00FF66" opacity="0.02"/>
    </pattern>
    <!-- Glow filter for green text -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="1.5" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <!-- Terminal background -->
  <rect width="760" height="298" rx="10" fill="#0d1117"/>

  <!-- CRT scanlines -->
  <rect width="760" height="298" rx="10" fill="url(#scan)" opacity="0.4"/>

  <!-- Green inner border glow -->
  <rect x="1" y="1" width="758" height="296" rx="9" fill="none" stroke="#00FF66" stroke-width="1" opacity="0.25"/>

  <!-- Header bar -->
  <rect width="760" height="37" rx="10" fill="#161b22"/>
  <rect y="27" width="760" height="10" fill="#161b22"/>

  <!-- Divider line -->
  <line x1="0" y1="37" x2="760" y2="37" stroke="#00FF66" stroke-width="0.5" opacity="0.3"/>

  <!-- Traffic lights -->
  <circle cx="24" cy="19" r="6" fill="#ff5f57"/>
  <circle cx="46" cy="19" r="6" fill="#ffbd2e"/>
  <circle cx="68" cy="19" r="6" fill="#28ca41"/>

  <!-- Terminal title -->
  <text x="380" y="24" fill="#6e7681" font-size="12" text-anchor="middle">MoNoahSEC@kali  —  bash</text>

  <!-- ===== TERMINAL CONTENT ===== -->

  <!-- Line 1: whoami command -->
  <text x="20" y="67" class="l1" filter="url(#glow)">
    <tspan fill="#00FF66">┌──(</tspan><tspan fill="#58a6ff">MoNoahSEC</tspan><tspan fill="#00FF66">㉿kali</tspan><tspan fill="#00FF66">)-[~]</tspan>
  </text>
  <text x="20" y="83" class="l1">
    <tspan fill="#00FF66">└─$</tspan><tspan fill="#e6edf3"> whoami</tspan>
  </text>

  <!-- Line 2: whoami output -->
  <text x="20" y="101" class="l2">
    <tspan fill="#00FF66" filter="url(#glow)">MoNoahSEC</tspan>
    <tspan fill="#8b949e">  —  Cybersecurity Student &amp; Python Developer</tspan>
  </text>

  <!-- Line 3: cat skills.txt -->
  <text x="20" y="127" class="l3" filter="url(#glow)">
    <tspan fill="#00FF66">┌──(</tspan><tspan fill="#58a6ff">MoNoahSEC</tspan><tspan fill="#00FF66">㉿kali</tspan><tspan fill="#00FF66">)-[~]</tspan>
  </text>
  <text x="20" y="143" class="l3">
    <tspan fill="#00FF66">└─$</tspan><tspan fill="#e6edf3"> cat skills.txt</tspan>
  </text>

  <!-- Lines 4-7: skill categories -->
  <text x="20" y="161" class="l4">
    <tspan fill="#484f58">  ▸</tspan>
    <tspan fill="#00FF66" filter="url(#glow)"> [LANGUAGES]</tspan>
    <tspan fill="#8b949e">   Python · Java · Bash · PHP · SQL</tspan>
  </text>

  <text x="20" y="178" class="l5">
    <tspan fill="#484f58">  ▸</tspan>
    <tspan fill="#00FF66" filter="url(#glow)"> [DOMAINS]  </tspan>
    <tspan fill="#8b949e">   Network Recon · Digital Forensics · Web Security</tspan>
  </text>

  <text x="20" y="195" class="l6">
    <tspan fill="#484f58">  ▸</tspan>
    <tspan fill="#00FF66" filter="url(#glow)"> [CERTS]    </tspan>
    <tspan fill="#8b949e">   Cisco · Huawei</tspan>
  </text>

  <text x="20" y="212" class="l7">
    <tspan fill="#484f58">  ▸</tspan>
    <tspan fill="#00FF66" filter="url(#glow)"> [TOOLS]    </tspan>
    <tspan fill="#8b949e">   Nmap · Wireshark · Metasploit · Burp Suite · Git</tspan>
  </text>

  <!-- Line 8: nmap command -->
  <text x="20" y="237" class="l8" filter="url(#glow)">
    <tspan fill="#00FF66">┌──(</tspan><tspan fill="#58a6ff">MoNoahSEC</tspan><tspan fill="#00FF66">㉿kali</tspan><tspan fill="#00FF66">)-[~]</tspan>
  </text>
  <text x="20" y="253" class="l8">
    <tspan fill="#00FF66">└─$</tspan><tspan fill="#e6edf3"> nmap -sV --open github.com/MoNoahSEC</tspan>
  </text>

  <!-- Line 9: scanning output -->
  <text x="20" y="268" class="l9">
    <tspan fill="#8b949e">Starting Nmap 7.94SVN ... </tspan>
    <tspan fill="#00FF66" filter="url(#glow)">[████████████████████]</tspan>
    <tspan fill="#8b949e"> 100%</tspan>
  </text>

  <!-- Line 10: result -->
  <text x="20" y="283" class="l10">
    <tspan fill="#8b949e">Host: </tspan>
    <tspan fill="#00FF66" filter="url(#glow)">UP</tspan>
    <tspan fill="#8b949e"> | 443/tcp </tspan>
    <tspan fill="#00FF66">OPEN</tspan>
    <tspan fill="#8b949e"> | Repos: </tspan>
    <tspan fill="#00FF66">∞</tspan>
    <tspan fill="#8b949e"> | Always pushing commits</tspan>
  </text>

  <!-- ===== CURSOR LINE ===== -->
  <!-- This is a separate prompt line for the cursor -->
  <!-- The prompt is hidden inside l11 trigger but cursor blinks independently -->
  <!-- We use the existing prompt structure so cursor appears after last line -->

  <!-- Blinking cursor after the result line (no new prompt, just cursor at end of line 11 prompt) -->
  <text x="20" y="60" class="l11" opacity="0" font-size="1">&#x200B;</text>
  <rect x="176" y="268" width="0" height="0" fill="none" class="l11"/>

  <!-- Actual blinking cursor: positioned after └─$ on the last implicit prompt -->
  <!-- Since last content is l10, we show cursor blinking under it suggesting next input -->
  <rect x="20" y="272" width="8" height="14" fill="#00FF66" class="cur"/>

</svg>
