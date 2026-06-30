
<html lang="en" data-theme="dark">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Justin Horton — Developer Portfolio</title>
  <meta name="description" content="Full-stack developer, Linux systems engineer, and blockchain developer from East Moline, Illinois. Specializing in automation, cybersecurity, and DeFi development.">
  <meta property="og:title" content="Justin Horton — Developer Portfolio">
  <meta property="og:description" content="Linux. Blockchain. Automation. Built from the ground up.">
  <meta name="theme-color" content="#0f3638">

  <!-- Fonts -->
  <link href="https://api.fontshare.com/v2/css?f[]=satoshi@400,500,700&f[]=cabinet-grotesk@400,500,700,800&display=swap" rel="stylesheet">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>

  <style>
    /* ART DIRECTION:
       Dark hacker aesthetic — deep slate surfaces, electric teal accent
       Cabinet Grotesk display + Satoshi body + JetBrains Mono for code
       Dense but breathable; terminal-inspired with modern polish */

    :root {
      --text-xs:   clamp(0.75rem,  0.7rem  + 0.25vw, 0.875rem);
      --text-sm:   clamp(0.875rem, 0.8rem  + 0.35vw, 1rem);
      --text-base: clamp(1rem,     0.95rem + 0.25vw, 1.125rem);
      --text-lg:   clamp(1.125rem, 1rem    + 0.75vw, 1.5rem);
      --text-xl:   clamp(1.5rem,   1.2rem  + 1.25vw, 2.25rem);
      --text-2xl:  clamp(2rem,     1.2rem  + 2.5vw,  3.5rem);
      --text-3xl:  clamp(2.5rem,   1rem    + 4vw,    5rem);
      --text-hero: clamp(3rem,     0.5rem  + 7vw,    8rem);

      --space-1:  0.25rem; --space-2:  0.5rem;  --space-3:  0.75rem;
      --space-4:  1rem;    --space-5:  1.25rem; --space-6:  1.5rem;
      --space-8:  2rem;    --space-10: 2.5rem;  --space-12: 3rem;
      --space-16: 4rem;    --space-20: 5rem;    --space-24: 6rem;
      --space-32: 8rem;

      --radius-sm: 0.375rem; --radius-md: 0.5rem;
      --radius-lg: 0.75rem;  --radius-xl: 1rem; --radius-full: 9999px;
      --transition-interactive: 180ms cubic-bezier(0.16, 1, 0.3, 1);
      --content-narrow: 640px; --content-default: 960px;
      --content-wide: 1200px;
      --font-display: 'Cabinet Grotesk', 'Helvetica Neue', sans-serif;
      --font-body: 'Satoshi', 'Inter', sans-serif;
      --font-mono: 'JetBrains Mono', 'Courier New', monospace;
    }

    /* DARK MODE (default) */
    :root, [data-theme="dark"] {
      --color-bg:             #0d0f0e;
      --color-surface:        #131614;
      --color-surface-2:      #181b1a;
      --color-surface-offset: #1e2220;
      --color-surface-offset-2: #242927;
      --color-surface-dynamic: #2d3330;
      --color-divider:        #252927;
      --color-border:         #303633;
      --color-text:           #d4d8d5;
      --color-text-muted:     #7a8480;
      --color-text-faint:     #4a524f;
      --color-text-inverse:   #0d0f0e;
      --color-primary:        #00e5cc;
      --color-primary-hover:  #00bfaa;
      --color-primary-active: #009988;
      --color-primary-highlight: #0d2e2c;
      --color-accent2:        #39d353;
      --color-accent3:        #f7a41b;
      --color-blue:           #58a6ff;
      --color-purple:         #bc8cff;
      --color-error:          #ff4c4c;
      --shadow-sm: 0 1px 2px oklch(0 0 0 / 0.3);
      --shadow-md: 0 4px 12px oklch(0 0 0 / 0.4);
      --shadow-lg: 0 12px 32px oklch(0 0 0 / 0.5);
      --glow-primary: 0 0 20px oklch(0.7 0.2 185 / 0.25);
    }

    [data-theme="light"] {
      --color-bg:             #f4f6f5;
      --color-surface:        #f9faf9;
      --color-surface-2:      #ffffff;
      --color-surface-offset: #ecefed;
      --color-surface-offset-2: #e4e8e5;
      --color-surface-dynamic: #d8deda;
      --color-divider:        #d0d5d2;
      --color-border:         #c8cec9;
      --color-text:           #1a2421;
      --color-text-muted:     #4a5c55;
      --color-text-faint:     #8a9e97;
      --color-text-inverse:   #f4f6f5;
      --color-primary:        #007a6e;
      --color-primary-hover:  #005f56;
      --color-primary-active: #004540;
      --color-primary-highlight: #d0eae8;
      --color-accent2:        #1a6f2e;
      --color-accent3:        #a05c00;
      --color-blue:           #0969da;
      --color-purple:         #7c3aed;
      --color-error:          #c01c1c;
      --shadow-sm: 0 1px 2px oklch(0.2 0.01 160 / 0.07);
      --shadow-md: 0 4px 12px oklch(0.2 0.01 160 / 0.09);
      --shadow-lg: 0 12px 32px oklch(0.2 0.01 160 / 0.13);
      --glow-primary: none;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html {
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
      scroll-behavior: smooth;
      scroll-padding-top: var(--space-20);
    }
    body {
      min-height: 100dvh;
      line-height: 1.6;
      font-family: var(--font-body);
      font-size: var(--text-base);
      color: var(--color-text);
      background-color: var(--color-bg);
      overflow-x: hidden;
    }
    img, svg { display: block; max-width: 100%; }
    input, button { font: inherit; color: inherit; }
    h1,h2,h3,h4 { text-wrap: balance; line-height: 1.1; font-family: var(--font-display); }
    p, li { text-wrap: pretty; }
    ::selection { background: oklch(from var(--color-primary, #00e5cc) l c h / 0.2); }
    :focus-visible { outline: 2px solid var(--color-primary); outline-offset: 3px; border-radius: var(--radius-sm); }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; }
    }
    button { cursor: pointer; background: none; border: none; }

    /* ── SKIP LINK ── */
    .skip-link {
      position: absolute; top: -100%; left: var(--space-4); z-index: 9999;
      background: var(--color-primary); color: var(--color-text-inverse);
      padding: var(--space-2) var(--space-4); border-radius: var(--radius-md);
      font-weight: 700; text-decoration: none;
      transition: top var(--transition-interactive);
    }
    .skip-link:focus { top: var(--space-4); }

    /* ── NAVIGATION ── */
    .nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: var(--space-4) var(--space-8);
      background: color-mix(in oklch, var(--color-bg) 85%, transparent);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--color-divider);
      transition: background var(--transition-interactive);
    }
    .nav-logo {
      display: flex; align-items: center; gap: var(--space-3);
      text-decoration: none; color: var(--color-text);
      font-family: var(--font-display); font-weight: 800;
      font-size: var(--text-sm); letter-spacing: -0.02em;
    }
    .nav-logo svg { color: var(--color-primary); flex-shrink: 0; }
    .nav-links { display: flex; align-items: center; gap: var(--space-6); list-style: none; }
    .nav-links a {
      text-decoration: none; color: var(--color-text-muted);
      font-size: var(--text-sm); font-weight: 500; letter-spacing: 0.01em;
      transition: color var(--transition-interactive);
    }
    .nav-links a:hover { color: var(--color-text); }
    .nav-actions { display: flex; align-items: center; gap: var(--space-3); }
    .btn-nav {
      display: flex; align-items: center; gap: var(--space-2);
      padding: var(--space-2) var(--space-4); border-radius: var(--radius-md);
      font-size: var(--text-sm); font-weight: 600; text-decoration: none;
      background: var(--color-primary); color: var(--color-text-inverse);
      transition: background var(--transition-interactive), transform var(--transition-interactive), box-shadow var(--transition-interactive);
      box-shadow: var(--glow-primary);
    }
    .btn-nav:hover { background: var(--color-primary-hover); transform: translateY(-1px); box-shadow: var(--glow-primary), var(--shadow-md); }
    .btn-nav:active { transform: translateY(0); }
    .theme-toggle {
      display: flex; align-items: center; justify-content: center;
      width: 36px; height: 36px; border-radius: var(--radius-md);
      color: var(--color-text-muted); border: 1px solid var(--color-border);
      transition: color var(--transition-interactive), border-color var(--transition-interactive), background var(--transition-interactive);
    }
    .theme-toggle:hover { color: var(--color-text); border-color: var(--color-text-muted); background: var(--color-surface-offset); }

    /* ── HERO ── */
    .hero {
      min-height: 100vh; display: flex; flex-direction: column;
      align-items: center; justify-content: center;
      padding: calc(var(--space-20) + 60px) var(--space-8) var(--space-20);
      text-align: center; position: relative; overflow: hidden;
    }
    .hero-bg {
      position: absolute; inset: 0; z-index: 0;
      background:
        radial-gradient(ellipse 80% 50% at 50% -10%, oklch(0.55 0.22 185 / 0.12), transparent),
        radial-gradient(ellipse 60% 40% at 80% 80%, oklch(0.55 0.22 185 / 0.07), transparent),
        radial-gradient(ellipse 40% 30% at 20% 60%, oklch(0.6 0.2 280 / 0.05), transparent);
    }
    .hero-grid {
      position: absolute; inset: 0; z-index: 0; opacity: 0.04;
      background-image: linear-gradient(var(--color-primary) 1px, transparent 1px),
        linear-gradient(90deg, var(--color-primary) 1px, transparent 1px);
      background-size: 60px 60px;
    }
    .hero-content { position: relative; z-index: 1; max-width: 900px; }
    .hero-tag {
      display: inline-flex; align-items: center; gap: var(--space-2);
      padding: var(--space-1) var(--space-4); border-radius: var(--radius-full);
      border: 1px solid color-mix(in oklch, var(--color-primary) 40%, transparent);
      background: color-mix(in oklch, var(--color-primary) 8%, transparent);
      color: var(--color-primary); font-size: var(--text-xs); font-weight: 600;
      letter-spacing: 0.08em; text-transform: uppercase; font-family: var(--font-mono);
      margin-bottom: var(--space-6);
    }
    .hero-tag .dot {
      width: 6px; height: 6px; border-radius: 50%; background: var(--color-accent2);
      animation: pulse 2s ease-in-out infinite;
    }
    @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.5;transform:scale(0.8)} }
    .hero h1 {
      font-size: var(--text-hero); font-weight: 800; letter-spacing: -0.04em;
      line-height: 0.95; margin-bottom: var(--space-6);
      color: var(--color-text);
    }
    .hero h1 span { color: var(--color-primary); }
    .hero-sub {
      font-size: var(--text-lg); color: var(--color-text-muted);
      max-width: 60ch; margin: 0 auto var(--space-10);
      font-weight: 400; line-height: 1.6;
    }
    .hero-ctas {
      display: flex; flex-wrap: wrap; gap: var(--space-4);
      justify-content: center; margin-bottom: var(--space-12);
    }
    .btn-primary {
      display: flex; align-items: center; gap: var(--space-2);
      padding: var(--space-3) var(--space-8); border-radius: var(--radius-md);
      font-size: var(--text-sm); font-weight: 700; text-decoration: none;
      background: var(--color-primary); color: #0d0f0e;
      transition: background var(--transition-interactive), transform var(--transition-interactive), box-shadow var(--transition-interactive);
      box-shadow: var(--glow-primary);
    }
    .btn-primary:hover { background: var(--color-primary-hover); transform: translateY(-2px); box-shadow: var(--glow-primary), var(--shadow-lg); }
    .btn-ghost {
      display: flex; align-items: center; gap: var(--space-2);
      padding: var(--space-3) var(--space-8); border-radius: var(--radius-md);
      font-size: var(--text-sm); font-weight: 600; text-decoration: none;
      border: 1px solid var(--color-border); color: var(--color-text-muted);
      transition: color var(--transition-interactive), border-color var(--transition-interactive), transform var(--transition-interactive);
    }
    .btn-ghost:hover { color: var(--color-text); border-color: var(--color-text-muted); transform: translateY(-2px); }
    .hero-stats {
      display: flex; gap: var(--space-8); justify-content: center;
      padding-top: var(--space-8); border-top: 1px solid var(--color-divider);
    }
    .hero-stat { text-align: center; }
    .hero-stat .num {
      font-size: var(--text-xl); font-weight: 800; font-family: var(--font-display);
      color: var(--color-primary); letter-spacing: -0.03em; display: block;
    }
    .hero-stat .label { font-size: var(--text-xs); color: var(--color-text-muted); letter-spacing: 0.05em; }

    /* ── SECTION SHARED ── */
    section { padding: clamp(var(--space-16), 8vw, var(--space-32)) var(--space-8); }
    .section-tag {
      display: inline-flex; align-items: center; gap: var(--space-2);
      font-family: var(--font-mono); font-size: var(--text-xs); font-weight: 500;
      color: var(--color-primary); letter-spacing: 0.1em; text-transform: uppercase;
      margin-bottom: var(--space-4);
    }
    .section-tag::before { content:'// '; }
    .section-title {
      font-size: var(--text-2xl); font-weight: 800; letter-spacing: -0.03em;
      color: var(--color-text); margin-bottom: var(--space-4);
    }
    .section-sub { font-size: var(--text-base); color: var(--color-text-muted); max-width: 55ch; margin-bottom: var(--space-12); }
    .container { max-width: var(--content-wide); margin-inline: auto; }

    /* ── ABOUT ── */
    .about-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-12);
      align-items: start;
    }
    .about-card {
      background: var(--color-surface); border: 1px solid var(--color-border);
      border-radius: var(--radius-xl); padding: var(--space-8);
      box-shadow: var(--shadow-md);
    }
    .about-card p { color: var(--color-text-muted); line-height: 1.7; margin-bottom: var(--space-4); font-size: var(--text-base); }
    .about-card p:last-child { margin-bottom: 0; }
    .terminal {
      background: var(--color-bg); border: 1px solid var(--color-border);
      border-radius: var(--radius-xl); overflow: hidden; box-shadow: var(--shadow-lg);
    }
    .terminal-header {
      display: flex; align-items: center; gap: var(--space-2);
      padding: var(--space-3) var(--space-4); background: var(--color-surface);
      border-bottom: 1px solid var(--color-divider);
    }
    .dot-red { width: 12px; height: 12px; border-radius: 50%; background: #ff5f57; }
    .dot-yellow { width: 12px; height: 12px; border-radius: 50%; background: #ffbd2e; }
    .dot-green { width: 12px; height: 12px; border-radius: 50%; background: #28ca41; }
    .terminal-title { font-size: var(--text-xs); color: var(--color-text-muted); margin-left: auto; font-family: var(--font-mono); }
    .terminal-body { padding: var(--space-6); font-family: var(--font-mono); font-size: var(--text-xs); line-height: 1.8; }
    .t-prompt { color: var(--color-primary); }
    .t-cmd { color: var(--color-text); }
    .t-out { color: var(--color-text-muted); margin-left: var(--space-4); }
    .t-str { color: var(--color-accent3); }
    .t-key { color: var(--color-blue); }
    .t-val { color: var(--color-accent2); }
    .t-comment { color: var(--color-text-faint); }
    .cursor { display: inline-block; width: 8px; height: 1em; background: var(--color-primary); animation: blink 1.2s step-end infinite; vertical-align: text-bottom; }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

    /* ── SKILLS ── */
    .skills-section { background: var(--color-surface); }
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: var(--space-4); }
    .skill-card {
      background: var(--color-surface-2); border: 1px solid var(--color-border);
      border-radius: var(--radius-lg); padding: var(--space-6);
      transition: transform var(--transition-interactive), box-shadow var(--transition-interactive), border-color var(--transition-interactive);
    }
    .skill-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-lg), var(--glow-primary); border-color: color-mix(in oklch, var(--color-primary) 40%, transparent); }
    .skill-card-header { display: flex; align-items: center; gap: var(--space-3); margin-bottom: var(--space-4); }
    .skill-icon {
      width: 40px; height: 40px; border-radius: var(--radius-md);
      display: flex; align-items: center; justify-content: center;
      background: var(--color-primary-highlight);
      color: var(--color-primary); flex-shrink: 0;
    }
    .skill-card h3 { font-size: var(--text-sm); font-weight: 700; color: var(--color-text); font-family: var(--font-display); }
    .skill-card .skill-level { font-size: var(--text-xs); color: var(--color-text-faint); font-family: var(--font-mono); }
    .skill-tags { display: flex; flex-wrap: wrap; gap: var(--space-2); }
    .tag {
      padding: 2px var(--space-3); border-radius: var(--radius-full);
      font-size: var(--text-xs); font-weight: 500; font-family: var(--font-mono);
      background: var(--color-surface-offset); color: var(--color-text-muted);
      border: 1px solid var(--color-divider);
    }
    .tag.teal { background: var(--color-primary-highlight); color: var(--color-primary); border-color: color-mix(in oklch, var(--color-primary) 20%, transparent); }
    .tag.green { background: color-mix(in oklch, var(--color-accent2) 10%, var(--color-surface)); color: var(--color-accent2); border-color: color-mix(in oklch, var(--color-accent2) 20%, transparent); }
    .tag.orange { background: color-mix(in oklch, var(--color-accent3) 10%, var(--color-surface)); color: var(--color-accent3); border-color: color-mix(in oklch, var(--color-accent3) 20%, transparent); }
    .tag.blue { background: color-mix(in oklch, var(--color-blue) 10%, var(--color-surface)); color: var(--color-blue); border-color: color-mix(in oklch, var(--color-blue) 20%, transparent); }
    .tag.purple { background: color-mix(in oklch, var(--color-purple) 10%, var(--color-surface)); color: var(--color-purple); border-color: color-mix(in oklch, var(--color-purple) 20%, transparent); }

    /* ── TECH STACK BARS ── */
    .stack-section {}
    .stack-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-8); }
    .stack-group { background: var(--color-surface); border: 1px solid var(--color-border); border-radius: var(--radius-xl); padding: var(--space-6); }
    .stack-group h3 { font-size: var(--text-sm); font-weight: 700; font-family: var(--font-display); color: var(--color-text); margin-bottom: var(--space-5); display: flex; align-items: center; gap: var(--space-2); }
    .stack-item { margin-bottom: var(--space-4); }
    .stack-item:last-child { margin-bottom: 0; }
    .stack-item-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: var(--space-2); }
    .stack-name { font-size: var(--text-xs); font-weight: 600; font-family: var(--font-mono); color: var(--color-text); }
    .stack-pct { font-size: var(--text-xs); font-family: var(--font-mono); color: var(--color-primary); }
    .stack-bar { height: 4px; background: var(--color-surface-offset); border-radius: var(--radius-full); overflow: hidden; }
    .stack-fill {
      height: 100%; border-radius: var(--radius-full);
      background: linear-gradient(90deg, var(--color-primary), var(--color-accent2));
      transform-origin: left; animation: fillBar 1.4s cubic-bezier(0.16, 1, 0.3, 1) both;
    }
    @keyframes fillBar { from{transform:scaleX(0)} to{transform:scaleX(1)} }
    .stack-fill.b { background: linear-gradient(90deg, var(--color-blue), var(--color-purple)); }
    .stack-fill.o { background: linear-gradient(90deg, var(--color-accent3), var(--color-error)); }

    /* ── PROJECTS ── */
    .projects-section { background: var(--color-surface); }
    .projects-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: var(--space-6); }
    .project-card {
      background: var(--color-surface-2); border: 1px solid var(--color-border);
      border-radius: var(--radius-xl); padding: var(--space-6);
      transition: transform var(--transition-interactive), box-shadow var(--transition-interactive), border-color var(--transition-interactive);
      display: flex; flex-direction: column;
    }
    .project-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-lg), var(--glow-primary); border-color: color-mix(in oklch, var(--color-primary) 35%, transparent); }
    .project-card-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: var(--space-4); }
    .project-icon { font-size: 1.5rem; }
    .project-links { display: flex; gap: var(--space-2); }
    .project-link {
      display: flex; align-items: center; justify-content: center;
      width: 32px; height: 32px; border-radius: var(--radius-md);
      border: 1px solid var(--color-border); color: var(--color-text-muted);
      text-decoration: none;
      transition: color var(--transition-interactive), border-color var(--transition-interactive), background var(--transition-interactive);
    }
    .project-link:hover { color: var(--color-primary); border-color: var(--color-primary); background: var(--color-primary-highlight); }
    .project-card h3 { font-size: var(--text-base); font-weight: 700; color: var(--color-text); margin-bottom: var(--space-2); font-family: var(--font-display); }
    .project-card p { font-size: var(--text-sm); color: var(--color-text-muted); line-height: 1.6; margin-bottom: var(--space-4); flex: 1; }
    .project-stack { display: flex; flex-wrap: wrap; gap: var(--space-2); }

    /* ── EXPERIENCE ── */
    .timeline { position: relative; padding-left: var(--space-8); }
    .timeline::before {
      content: ''; position: absolute; left: 11px; top: var(--space-2); bottom: var(--space-2);
      width: 2px; background: linear-gradient(180deg, var(--color-primary), var(--color-primary-highlight), transparent);
    }
    .timeline-item { position: relative; margin-bottom: var(--space-10); }
    .timeline-dot {
      position: absolute; left: calc(-1 * var(--space-8) + 3px); top: 5px;
      width: 18px; height: 18px; border-radius: 50%;
      border: 2px solid var(--color-primary); background: var(--color-bg);
      box-shadow: var(--glow-primary);
    }
    .timeline-dot.active { background: var(--color-primary); }
    .timeline-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: var(--space-2); margin-bottom: var(--space-2); }
    .timeline-role { font-size: var(--text-sm); font-weight: 700; color: var(--color-text); font-family: var(--font-display); }
    .timeline-date { font-size: var(--text-xs); font-family: var(--font-mono); color: var(--color-primary); }
    .timeline-company { font-size: var(--text-xs); color: var(--color-text-muted); font-weight: 500; margin-bottom: var(--space-3); }
    .timeline-desc { font-size: var(--text-sm); color: var(--color-text-muted); line-height: 1.65; }
    .timeline-tags { display: flex; flex-wrap: wrap; gap: var(--space-2); margin-top: var(--space-3); }

    /* ── CONTACT ── */
    .contact-section { background: var(--color-surface); }
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-10); align-items: start; }
    .contact-links { display: flex; flex-direction: column; gap: var(--space-4); margin-top: var(--space-8); }
    .contact-link {
      display: flex; align-items: center; gap: var(--space-4);
      padding: var(--space-4) var(--space-5); border-radius: var(--radius-lg);
      background: var(--color-surface-2); border: 1px solid var(--color-border);
      text-decoration: none; color: var(--color-text);
      transition: transform var(--transition-interactive), border-color var(--transition-interactive), box-shadow var(--transition-interactive);
    }
    .contact-link:hover { transform: translateX(4px); border-color: var(--color-primary); box-shadow: var(--shadow-md); }
    .contact-link .cl-icon { width: 40px; height: 40px; border-radius: var(--radius-md); background: var(--color-primary-highlight); color: var(--color-primary); display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
    .contact-link .cl-label { font-size: var(--text-xs); color: var(--color-text-faint); margin-bottom: 2px; }
    .contact-link .cl-val { font-size: var(--text-sm); font-weight: 600; }
    .contact-form { display: flex; flex-direction: column; gap: var(--space-4); }
    .form-group { display: flex; flex-direction: column; gap: var(--space-2); }
    .form-group label { font-size: var(--text-xs); font-weight: 600; color: var(--color-text-muted); letter-spacing: 0.05em; text-transform: uppercase; font-family: var(--font-mono); }
    .form-group input, .form-group textarea {
      padding: var(--space-3) var(--space-4); border-radius: var(--radius-md);
      border: 1px solid var(--color-border); background: var(--color-surface-2);
      color: var(--color-text); font-family: var(--font-body); font-size: var(--text-sm);
      transition: border-color var(--transition-interactive), box-shadow var(--transition-interactive);
      resize: vertical;
    }
    .form-group input:focus, .form-group textarea:focus { outline: none; border-color: var(--color-primary); box-shadow: 0 0 0 3px color-mix(in oklch, var(--color-primary) 15%, transparent); }
    .form-group input::placeholder, .form-group textarea::placeholder { color: var(--color-text-faint); }
    .btn-form {
      display: flex; align-items: center; justify-content: center; gap: var(--space-2);
      padding: var(--space-3) var(--space-6); border-radius: var(--radius-md);
      font-size: var(--text-sm); font-weight: 700; cursor: pointer;
      background: var(--color-primary); color: #0d0f0e;
      border: none; width: 100%;
      transition: background var(--transition-interactive), transform var(--transition-interactive);
    }
    .btn-form:hover { background: var(--color-primary-hover); transform: translateY(-1px); }

    /* ── FOOTER ── */
    footer {
      padding: var(--space-8); border-top: 1px solid var(--color-divider);
      display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: var(--space-4);
    }
    footer p { font-size: var(--text-xs); color: var(--color-text-faint); font-family: var(--font-mono); }
    footer p span { color: var(--color-primary); }
    .footer-links { display: flex; gap: var(--space-6); }
    .footer-links a { font-size: var(--text-xs); color: var(--color-text-faint); text-decoration: none; transition: color var(--transition-interactive); }
    .footer-links a:hover { color: var(--color-primary); }

    /* ── MOBILE NAV TOGGLE ── */
    .nav-hamburger { display: none; flex-direction: column; gap: 5px; padding: var(--space-2); cursor: pointer; }
    .nav-hamburger span { display: block; width: 22px; height: 2px; background: var(--color-text); border-radius: 2px; transition: transform var(--transition-interactive), opacity var(--transition-interactive); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .nav-links, .btn-nav { display: none; }
      .nav-hamburger { display: flex; }
      .about-grid, .stack-grid, .contact-grid { grid-template-columns: 1fr; }
      .hero-stats { gap: var(--space-6); }
    }
    @media (max-width: 600px) {
      .nav { padding: var(--space-4); }
      section { padding: var(--space-12) var(--space-4); }
      footer { flex-direction: column; text-align: center; }
    }

    /* ── SCROLL REVEAL ── */
    .reveal { opacity: 0; transform: translateY(20px); transition: opacity 0.6s cubic-bezier(0.16,1,0.3,1), transform 0.6s cubic-bezier(0.16,1,0.3,1); }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    .reveal-delay-1 { transition-delay: 0.1s; }
    .reveal-delay-2 { transition-delay: 0.2s; }
    .reveal-delay-3 { transition-delay: 0.3s; }
  </style>
</head>
<body>

  <a href="#main" class="skip-link">Skip to content</a>

  <!-- ── NAVIGATION ── -->
  <nav class="nav" aria-label="Main navigation">
    <a href="#" class="nav-logo" aria-label="Justin Horton Home">
      <svg width="28" height="28" viewBox="0 0 28 28" fill="none" aria-hidden="true">
        <rect width="28" height="28" rx="6" fill="currentColor"/>
        <path d="M7 9l5 5-5 5M14 19h7" stroke="#0d0f0e" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
      Justin Horton
    </a>
    <ul class="nav-links" role="list">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#stack">Stack</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="nav-actions">
      <button class="theme-toggle" data-theme-toggle aria-label="Switch to light mode">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/>
        </svg>
      </button>
      <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="btn-nav" aria-label="View GitHub">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        GitHub
      </a>
    </div>
    <button class="nav-hamburger" aria-label="Toggle mobile menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </nav>

  <main id="main">

    <!-- ── HERO ── -->
    <section class="hero" aria-labelledby="hero-heading">
      <div class="hero-bg" aria-hidden="true"></div>
      <div class="hero-grid" aria-hidden="true"></div>
      <div class="hero-content">
        <div class="hero-tag"><span class="dot"></span>Available for freelance &amp; collabs</div>
        <h1 id="hero-heading">
          Justin<br><span>Horton</span>
        </h1>
        <p class="hero-sub">
          Linux systems engineer, blockchain developer, and automation architect from East Moline, Illinois.
          I build fast, automated, and self-sustaining systems — from bare metal to DeFi protocols.
        </p>
        <div class="hero-ctas">
          <a href="#projects" class="btn-primary">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/></svg>
            View Projects
          </a>
          <a href="#contact" class="btn-ghost">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,12 2,6"/></svg>
            Get in Touch
          </a>
        </div>
        <div class="hero-stats" role="list" aria-label="Key statistics">
          <div class="hero-stat" role="listitem">
            <span class="num">5+</span>
            <span class="label">Languages</span>
          </div>
          <div class="hero-stat" role="listitem">
            <span class="num">10+</span>
            <span class="label">Tech Areas</span>
          </div>
          <div class="hero-stat" role="listitem">
            <span class="num">∞</span>
            <span class="label">Drive to Build</span>
          </div>
          <div class="hero-stat" role="listitem">
            <span class="num">IL</span>
            <span class="label">Chicago IL</span>
          </div>
        </div>
      </div>
    </section>

    <!-- ── ABOUT ── -->
    <section id="about" aria-labelledby="about-heading">
      <div class="container">
        <div class="section-tag">about me</div>
        <h2 class="section-title" id="about-heading">Built different.</h2>
        <div class="about-grid">
          <div class="about-card reveal">
            <p>
              I'm a self-taught developer and systems engineer based in East Moline, Illinois. I got my start in hands-on technical work — building computers, automotive repair, and industrial maintenance — which gave me a ground-up understanding of how systems work.
            </p>
            <p>
              That same methodical mindset is what I bring to software. I specialize in Linux security, blockchain/DeFi development on Solana, and building automated systems that run without hand-holding. My toolkit spans Python, JavaScript/TypeScript, C++, and shell scripting.
            </p>
            <p>
              I'm not just writing code — I'm building revenue-generating, automated digital infrastructure. Currently deep in n8n workflow automation, AI agent integration, and Solana DeFi protocol development.
            </p>
          </div>
          <div class="terminal reveal reveal-delay-1" aria-label="Terminal showing developer profile">
            <div class="terminal-header">
              <div class="dot-red"></div><div class="dot-yellow"></div><div class="dot-green"></div>
              <span class="terminal-title">justin@eastmoline ~ </span>
            </div>
            <div class="terminal-body" aria-live="polite">
              <div><span class="t-prompt">❯ </span><span class="t-cmd">cat profile.json</span></div>
              <div class="t-out">{</div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"name"</span>: <span class="t-str">"Justin Horton"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"location"</span>: <span class="t-str">"East Moline, Illinois"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"role"</span>: <span class="t-str">"Full-Stack Dev &amp; Systems Eng"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"focus"</span>: [</div>
              <div class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"Linux &amp; Cybersecurity"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"Blockchain / Solana DeFi"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"Automation &amp; n8n Workflows"</span>,</div>
              <div class="t-out">&nbsp;&nbsp;&nbsp;&nbsp;<span class="t-str">"AI Agent Development"</span></div>
              <div class="t-out">&nbsp;&nbsp;],</div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"status"</span>: <span class="t-val">true</span>, <span class="t-comment">// actively building</span></div>
              <div class="t-out">&nbsp;&nbsp;<span class="t-key">"available"</span>: <span class="t-val">true</span></div>
              <div class="t-out">}</div>
              <div style="margin-top:var(--space-3)"><span class="t-prompt">❯ </span><span class="cursor"></span></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ── SKILLS ── -->
    <section id="skills" class="skills-section" aria-labelledby="skills-heading">
      <div class="container">
        <div class="section-tag">expertise</div>
        <h2 class="section-title" id="skills-heading">Skills &amp; Domains</h2>
        <p class="section-sub">From bare-metal Linux to DeFi protocols — here's where I live and breathe.</p>
        <div class="skills-grid">

          <div class="skill-card reveal">
            <div class="skill-card-header">
              <div class="skill-icon"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg></div>
              <div><div class="skill-level">// core</div><h3>Linux &amp; Systems</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag teal">Kali Linux</span><span class="tag teal">Debian</span><span class="tag">Shell Scripting</span><span class="tag">System Admin</span><span class="tag">Docker</span><span class="tag">VPS Management</span><span class="tag">Network Config</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-1">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-accent3) 12%, var(--color-surface)); color:var(--color-accent3)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div>
              <div><div class="skill-level">// advanced</div><h3>Cybersecurity</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag orange">Penetration Testing</span><span class="tag orange">Security Auditing</span><span class="tag">Kali Tools</span><span class="tag">Network Security</span><span class="tag">Android Rooting</span><span class="tag">Forensics</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-2">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-blue) 12%, var(--color-surface)); color:var(--color-blue)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg></div>
              <div><div class="skill-level">// proficient</div><h3>Programming</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag blue">Python</span><span class="tag blue">JavaScript</span><span class="tag blue">TypeScript</span><span class="tag">C++</span><span class="tag">SQL</span><span class="tag">Bash/Shell</span>
            </div>
          </div>

          <div class="skill-card reveal">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-purple) 12%, var(--color-surface)); color:var(--color-purple)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg></div>
              <div><div class="skill-level">// building</div><h3>Blockchain &amp; DeFi</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag purple">Solana</span><span class="tag purple">Rust/Anchor</span><span class="tag">DeFi Protocols</span><span class="tag">Flash Loans</span><span class="tag">Crypto Bots</span><span class="tag">Web3</span><span class="tag">Arbitrage</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-1">
            <div class="skill-card-header">
              <div class="skill-icon"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg></div>
              <div><div class="skill-level">// advanced</div><h3>Automation &amp; n8n</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag teal">n8n</span><span class="tag teal">Workflow Design</span><span class="tag">API Integration</span><span class="tag">Webhooks</span><span class="tag">Bot Development</span><span class="tag">Task Automation</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-2">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-accent2) 12%, var(--color-surface)); color:var(--color-accent2)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg></div>
              <div><div class="skill-level">// full-stack</div><h3>Web Development</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag green">Node.js</span><span class="tag green">React</span><span class="tag">REST APIs</span><span class="tag">HTML/CSS</span><span class="tag">Databases</span><span class="tag">E-commerce</span>
            </div>
          </div>

          <div class="skill-card reveal">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-accent3) 12%, var(--color-surface)); color:var(--color-accent3)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/></svg></div>
              <div><div class="skill-level">// devops</div><h3>Containerization</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag orange">Docker</span><span class="tag orange">Docker Compose</span><span class="tag">VPS Deploy</span><span class="tag">CI/CD Basics</span><span class="tag">Cloud Services</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-1">
            <div class="skill-card-header">
              <div class="skill-icon" style="background:color-mix(in oklch, var(--color-purple) 12%, var(--color-surface)); color:var(--color-purple)"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9.5 2A2.5 2.5 0 0 1 12 4.5v15a2.5 2.5 0 0 1-4.96.44 2.5 2.5 0 0 1-2.96-3.08 3 3 0 0 1-.34-5.58 2.5 2.5 0 0 1 1.32-4.24 2.5 2.5 0 0 1 1.98-3A2.5 2.5 0 0 1 9.5 2Z"/><path d="M14.5 2A2.5 2.5 0 0 0 12 4.5v15a2.5 2.5 0 0 0 4.96.44 2.5 2.5 0 0 0 2.96-3.08 3 3 0 0 0 .34-5.58 2.5 2.5 0 0 0-1.32-4.24 2.5 2.5 0 0 0-1.98-3A2.5 2.5 0 0 0 14.5 2Z"/></svg></div>
              <div><div class="skill-level">// integrating</div><h3>AI &amp; LLMs</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag purple">Claude API</span><span class="tag purple">Local LLMs</span><span class="tag">AI Agents</span><span class="tag">Prompt Engineering</span><span class="tag">Code Generation</span>
            </div>
          </div>

          <div class="skill-card reveal reveal-delay-2">
            <div class="skill-card-header">
              <div class="skill-icon"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg></div>
              <div><div class="skill-level">// hands-on</div><h3>Hardware &amp; IT</h3></div>
            </div>
            <div class="skill-tags">
              <span class="tag teal">PC Building</span><span class="tag">Hardware Repair</span><span class="tag">Network Setup</span><span class="tag">Troubleshooting</span><span class="tag">Android Dev</span>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ── TECH STACK BARS ── -->
    <section id="stack" aria-labelledby="stack-heading">
      <div class="container">
        <div class="section-tag">proficiency</div>
        <h2 class="section-title" id="stack-heading">Tech Stack</h2>
        <p class="section-sub">Tools I reach for every day, ordered by how deep I've gone.</p>
        <div class="stack-grid">

          <div class="stack-group reveal">
            <h3><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg> Languages</h3>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Python</span><span class="stack-pct">90%</span></div><div class="stack-bar"><div class="stack-fill" style="width:90%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Bash / Shell</span><span class="stack-pct">88%</span></div><div class="stack-bar"><div class="stack-fill" style="width:88%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">JavaScript / TypeScript</span><span class="stack-pct">78%</span></div><div class="stack-bar"><div class="stack-fill" style="width:78%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">C++</span><span class="stack-pct">60%</span></div><div class="stack-bar"><div class="stack-fill" style="width:60%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">SQL</span><span class="stack-pct">65%</span></div><div class="stack-bar"><div class="stack-fill" style="width:65%"></div></div></div>
          </div>

          <div class="stack-group reveal reveal-delay-1">
            <h3><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/></svg> Systems &amp; DevOps</h3>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Linux (Kali / Debian)</span><span class="stack-pct">92%</span></div><div class="stack-bar"><div class="stack-fill b" style="width:92%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Docker &amp; Containers</span><span class="stack-pct">82%</span></div><div class="stack-bar"><div class="stack-fill b" style="width:82%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">VPS / Cloud</span><span class="stack-pct">80%</span></div><div class="stack-bar"><div class="stack-fill b" style="width:80%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">n8n Automation</span><span class="stack-pct">85%</span></div><div class="stack-bar"><div class="stack-fill b" style="width:85%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Network / Security Tools</span><span class="stack-pct">75%</span></div><div class="stack-bar"><div class="stack-fill b" style="width:75%"></div></div></div>
          </div>

          <div class="stack-group reveal">
            <h3><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg> Blockchain</h3>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Solana / Web3.js</span><span class="stack-pct">72%</span></div><div class="stack-bar"><div class="stack-fill o" style="width:72%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">DeFi / DEX Protocols</span><span class="stack-pct">68%</span></div><div class="stack-bar"><div class="stack-fill o" style="width:68%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Crypto Trading Bots</span><span class="stack-pct">70%</span></div><div class="stack-bar"><div class="stack-fill o" style="width:70%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Flash Loans / Arbitrage</span><span class="stack-pct">55%</span></div><div class="stack-bar"><div class="stack-fill o" style="width:55%"></div></div></div>
          </div>

          <div class="stack-group reveal reveal-delay-1">
            <h3><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg> Web &amp; AI</h3>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Node.js / Express</span><span class="stack-pct">75%</span></div><div class="stack-bar"><div class="stack-fill" style="width:75%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">React</span><span class="stack-pct">65%</span></div><div class="stack-bar"><div class="stack-fill" style="width:65%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Claude / OpenAI API</span><span class="stack-pct">80%</span></div><div class="stack-bar"><div class="stack-fill" style="width:80%"></div></div></div>
            <div class="stack-item"><div class="stack-item-header"><span class="stack-name">Local LLM Deploy</span><span class="stack-pct">70%</span></div><div class="stack-bar"><div class="stack-fill" style="width:70%"></div></div></div>
          </div>

        </div>
      </div>
    </section>

    <!-- ── PROJECTS ── -->
    <section id="projects" class="projects-section" aria-labelledby="projects-heading">
      <div class="container">
        <div class="section-tag">portfolio</div>
        <h2 class="section-title" id="projects-heading">Projects &amp; Builds</h2>
        <p class="section-sub">Things I've built, automated, or am currently deep in. Real systems, real code.</p>
        <div class="projects-grid">

          <div class="project-card reveal">
            <div class="project-card-header">
              <div class="project-icon">⚡</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>Solana Trading Bot</h3>
            <p>Automated crypto trading bot targeting Solana DEX arbitrage opportunities. Scans multiple pools for price discrepancies and executes trades with sub-second latency.</p>
            <div class="project-stack">
              <span class="tag purple">Solana</span><span class="tag blue">TypeScript</span><span class="tag">Web3.js</span><span class="tag orange">DeFi</span>
            </div>
          </div>

          <div class="project-card reveal reveal-delay-1">
            <div class="project-card-header">
              <div class="project-icon">🤖</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>n8n AI Workflow Automation</h3>
            <p>Complex n8n automation pipelines with AI agent integration using Claude API. Automates content creation, data processing, lead generation, and multi-platform publishing.</p>
            <div class="project-stack">
              <span class="tag teal">n8n</span><span class="tag purple">Claude API</span><span class="tag blue">JavaScript</span><span class="tag">Webhooks</span>
            </div>
          </div>

          <div class="project-card reveal reveal-delay-2">
            <div class="project-card-header">
              <div class="project-icon">🛡️</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>Linux Security Audit Tool</h3>
            <p>Custom Kali Linux security auditing toolkit with automated vulnerability scanning, network enumeration, and report generation. Built for personal lab and learning environments.</p>
            <div class="project-stack">
              <span class="tag teal">Kali Linux</span><span class="tag blue">Python</span><span class="tag">Bash</span><span class="tag orange">Security</span>
            </div>
          </div>

          <div class="project-card reveal">
            <div class="project-card-header">
              <div class="project-icon">🏪</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>Digital Product Store</h3>
            <p>Automated e-commerce setup for selling digital products — templates, tools, and automation scripts. Integrated with payment processing, delivery automation, and customer management.</p>
            <div class="project-stack">
              <span class="tag green">Node.js</span><span class="tag teal">n8n</span><span class="tag blue">JavaScript</span><span class="tag">E-commerce</span>
            </div>
          </div>

          <div class="project-card reveal reveal-delay-1">
            <div class="project-card-header">
              <div class="project-icon">🧠</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>Local LLM Agent Stack</h3>
            <p>Self-hosted AI agent infrastructure running on local hardware. Uses Ollama + custom Python wrappers to run specialized AI agents for code review, research, and content generation.</p>
            <div class="project-stack">
              <span class="tag purple">Ollama</span><span class="tag blue">Python</span><span class="tag">Docker</span><span class="tag teal">Linux</span>
            </div>
          </div>

          <div class="project-card reveal reveal-delay-2">
            <div class="project-card-header">
              <div class="project-icon">📡</div>
              <div class="project-links">
                <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="project-link" aria-label="View on GitHub"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></a>
              </div>
            </div>
            <h3>Solana Node &amp; RPC Setup</h3>
            <p>Custom Solana validator / RPC node configuration on Debian VPS. Optimized for low-latency transaction submission for trading bots and real-time on-chain data.</p>
            <div class="project-stack">
              <span class="tag purple">Solana</span><span class="tag teal">Linux</span><span class="tag orange">Docker</span><span class="tag">Networking</span>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ── EXPERIENCE ── -->
    <section id="experience" aria-labelledby="experience-heading">
      <div class="container" style="max-width:var(--content-default)">
        <div class="section-tag">background</div>
        <h2 class="section-title" id="experience-heading">Experience</h2>
        <p class="section-sub">Hands-on work across industries that shaped how I think about systems, reliability, and problem-solving.</p>

        <div class="timeline reveal">
          <div class="timeline-item">
            <div class="timeline-dot active"></div>
            <div class="timeline-header">
              <span class="timeline-role">Indie Developer &amp; Automation Builder</span>
              <span class="timeline-date">2024 — Present</span>
            </div>
            <div class="timeline-company">Self-Employed · East Moline, Illinois</div>
            <p class="timeline-desc">Building automated digital products, n8n workflow systems, and blockchain applications. Developing Solana trading bots, AI agent pipelines, and monetized automation tools. Currently working toward full income replacement through scalable digital infrastructure.</p>
            <div class="timeline-tags">
              <span class="tag teal">Solana</span><span class="tag teal">n8n</span><span class="tag blue">Python</span><span class="tag purple">AI Agents</span><span class="tag orange">Docker</span>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-header">
              <span class="timeline-role">IT Support &amp; PC Builder</span>
              <span class="timeline-date">Ongoing</span>
            </div>
            <div class="timeline-company">Independent · East Moline, Illinois</div>
            <p class="timeline-desc">Building, configuring, and troubleshooting custom computers. Hardware selection, OS installation, networking setup, and performance optimization for clients and personal projects. Deep hands-on experience with Linux dual-boot, Kali setups, and custom system builds.</p>
            <div class="timeline-tags">
              <span class="tag teal">Linux</span><span class="tag">Hardware</span><span class="tag">Networking</span><span class="tag orange">Kali</span>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-header">
              <span class="timeline-role">Maintenance Technician</span>
              <span class="timeline-date">Past</span>
            </div>
            <div class="timeline-company">Tyson Foods · East Moline, Illinois</div>
            <p class="timeline-desc">Industrial maintenance in a large-scale production environment. Troubleshooting, mechanical repair, and keeping critical systems operational under pressure. Built a systems-level mindset: understand the whole before touching the parts.</p>
            <div class="timeline-tags">
              <span class="tag">Systems Thinking</span><span class="tag">Industrial Maintenance</span><span class="tag">Problem Solving</span>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-header">
              <span class="timeline-role">Automotive Technician</span>
              <span class="timeline-date">Past</span>
            </div>
            <div class="timeline-company">Jack's Brake &amp; Auto · East Moline, Illinois</div>
            <p class="timeline-desc">Brake systems, diagnostics, and general auto repair. Precision work under time constraints and customer pressure. Translated complex mechanical systems into explainable solutions — a skill that transfers directly to debugging code.</p>
            <div class="timeline-tags">
              <span class="tag">Diagnostics</span><span class="tag">Precision Work</span><span class="tag">Client Communication</span>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-header">
              <span class="timeline-role">Technician Program</span>
              <span class="timeline-date">Past</span>
            </div>
            <div class="timeline-company">Hamilton Technician College · East Moline, Illinois</div>
            <p class="timeline-desc">Technical education with a focus on applied systems and troubleshooting methodology. Formal grounding in technical problem-solving that underpins my approach to software engineering and systems administration.</p>
            <div class="timeline-tags">
              <span class="tag">Technical Education</span><span class="tag">Applied Systems</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ── CONTACT ── -->
    <section id="contact" class="contact-section" aria-labelledby="contact-heading">
      <div class="container">
        <div class="section-tag">let's build</div>
        <h2 class="section-title" id="contact-heading">Get in Touch</h2>
        <div class="contact-grid">
          <div class="reveal">
            <p style="color:var(--color-text-muted);font-size:var(--text-base);line-height:1.7;margin-bottom:var(--space-2)">
              Open to freelance projects, collaborations on automation or blockchain systems, and conversations about interesting technical problems.
            </p>
            <p style="color:var(--color-text-muted);font-size:var(--text-sm);line-height:1.7;margin-bottom:var(--space-6)">
              Based in East Moline, Illinois. Available for remote work worldwide.
            </p>
            <div class="contact-links">
              <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer" class="contact-link">
                <div class="cl-icon"><svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg></div>
                <div><div class="cl-label">GitHub</div><div class="cl-val">github.com/dutch71086</div></div>
              </a>
              <a href="mailto:justin@example.com" class="contact-link">
                <div class="cl-icon"><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,12 2,6"/></svg></div>
                <div><div class="cl-label">Email</div><div class="cl-val">Drop me a message →</div></div>
              </a>
              <a href="https://twitter.com/justinsnortin" target="_blank" rel="noopener noreferrer" class="contact-link">
                <div class="cl-icon"><svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg></div>
                <div><div class="cl-label">Twitter / X</div><div class="cl-val">@justinhorton</div></div>
              </a>
            </div>
          </div>
          <div class="reveal reveal-delay-1">
            <form class="contact-form" onsubmit="handleSubmit(event)" aria-label="Contact form">
              <div class="form-group">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" placeholder="Your name" required autocomplete="name">
              </div>
              <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="your@email.com" required autocomplete="email">
              </div>
              <div class="form-group">
                <label for="message">Message</label>
                <textarea id="message" name="message" rows="5" placeholder="What are you building?" required></textarea>
              </div>
              <button type="submit" class="btn-form" id="submit-btn">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
                Send Message
              </button>
              <div id="form-success" style="display:none;text-align:center;padding:var(--space-4);background:var(--color-primary-highlight);border-radius:var(--radius-md);color:var(--color-primary);font-size:var(--text-sm);font-weight:600;">
                ✓ Message sent! I'll get back to you soon.
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- ── FOOTER ── -->
  <footer>
    <p>Built with <span>💚</span> in East Moline, Illinois · <span>© 2026 Justin Horton</span></p>
    <nav class="footer-links" aria-label="Footer navigation">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="https://github.com/dutch71086" target="_blank" rel="noopener noreferrer">GitHub</a>
    </nav>
  </footer>

  <script>
    // ── THEME TOGGLE ──
    (function(){
      const t = document.querySelector('[data-theme-toggle]');
      const r = document.documentElement;
      let d = 'dark'; // default dark
      r.setAttribute('data-theme', d);
      function updateIcon() {
        if (!t) return;
        t.setAttribute('aria-label', 'Switch to ' + (d === 'dark' ? 'light' : 'dark') + ' mode');
        t.innerHTML = d === 'dark'
          ? '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="5"/><path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"/></svg>'
          : '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>';
      }
      updateIcon();
      if (t) t.addEventListener('click', () => {
        d = d === 'dark' ? 'light' : 'dark';
        r.setAttribute('data-theme', d);
        updateIcon();
      });
    })();

    // ── SCROLL REVEAL ──
    (function(){
      const els = document.querySelectorAll('.reveal');
      const io = new IntersectionObserver((entries) => {
        entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); io.unobserve(e.target); } });
      }, { threshold: 0.1 });
      els.forEach(el => io.observe(el));
    })();

    // ── ACTIVE NAV ──
    (function(){
      const sections = document.querySelectorAll('section[id]');
      const navLinks = document.querySelectorAll('.nav-links a');
      const io = new IntersectionObserver((entries) => {
        entries.forEach(e => {
          if (e.isIntersecting) {
            navLinks.forEach(a => {
              a.style.color = '';
              if (a.getAttribute('href') === '#' + e.target.id) a.style.color = 'var(--color-primary)';
            });
          }
        });
      }, { rootMargin: '-40% 0px -50% 0px' });
      sections.forEach(s => io.observe(s));
    })();

    // ── FORM SUBMIT ──
    function handleSubmit(e) {
      e.preventDefault();
      const btn = document.getElementById('submit-btn');
      const success = document.getElementById('form-success');
      btn.disabled = true;
      btn.innerHTML = '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" style="animation:spin 1s linear infinite"><path d="M21 12a9 9 0 1 1-6.219-8.56"/></svg> Sending...';
      const style = document.createElement('style');
      style.textContent = '@keyframes spin{from{transform:rotate(0deg)}to{transform:rotate(360deg)}}';
      document.head.appendChild(style);
      setTimeout(() => {
        btn.style.display = 'none';
        success.style.display = 'block';
        e.target.reset();
      }, 1200);
    }

    // ── ANIMATED COUNTERS ──
    (function(){
      // Simple hero stats are static — let CSS animations handle bar fills
    })();
  </script>

</body>
</html>
