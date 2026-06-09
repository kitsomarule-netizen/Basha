<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Instax × Basha Uhuru 2026 — Pitch Deck</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    :root { --basha-yellow: #F4B824; --basha-orange: #E65C2B; --basha-teal: #1F9296; --instax-teal: #3DBFB8; --cream: #FAF6F0; --charcoal: #1A1817; --white: #FFFFFF; --soft-gray: #EAE3D8; --warm-gray: #C4B8A8; }
    html { scroll-behavior: smooth; }
    body { font-family: 'DM Sans', sans-serif; background-color: var(--charcoal); color: var(--charcoal); line-height: 1.6; }
    h1, h2, h3 { font-family: 'DM Serif Display', serif; font-weight: 400; }
    .container { max-width: 1100px; margin: 0 auto; padding: 0 1.5rem; }
    img { max-width: 100%; height: auto; display: block; }
    .deco-line { height: 3px; width: 60px; background: linear-gradient(90deg, var(--basha-orange), var(--basha-yellow)); border-radius: 2px; margin: 1rem 0; }
    .deco-dots { display: flex; gap: 6px; margin: 0.5rem 0; }
    .deco-dots span { width: 6px; height: 6px; border-radius: 50%; background: var(--basha-yellow); }
    .deco-dots span:nth-child(2) { background: var(--basha-orange); }
    .deco-dots span:nth-child(3) { background: var(--instax-teal); }
    .section-badge { display: inline-flex; align-items: center; gap: 0.5rem; background: var(--charcoal); color: var(--basha-yellow); padding: 0.4rem 1rem; border-radius: 30px; font-size: 0.75rem; font-weight: 700; text-transform: uppercase; letter-spacing: 1.5px; margin-bottom: 1rem; }
    .section-badge.light { background: var(--white); color: var(--charcoal); border: 1px solid var(--soft-gray); }
    .hero { background: linear-gradient(135deg, var(--charcoal) 0%, #2A2522 50%, #1A1817 100%); color: var(--cream); min-height: 100vh; display: flex; flex-direction: column; position: relative; overflow: hidden; border-bottom: 4px solid var(--basha-yellow); }
    .hero::before { content: ''; position: absolute; top: 0; right: 0; width: 400px; height: 400px; border-radius: 50%; background: radial-gradient(circle, rgba(61,191,184,0.08) 0%, transparent 70%); z-index: 1; }
    .hero::after { content: ''; position: absolute; bottom: -100px; left: -100px; width: 300px; height: 300px; border-radius: 50%; background: radial-gradient(circle, rgba(244,184,36,0.06) 0%, transparent 70%); z-index: 1; }
    .hero-bg-img { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; opacity: 0.3; z-index: 0; }
    .hero-header { display: flex; justify-content: space-between; align-items: center; padding: 1.5rem; border-bottom: 1px solid rgba(255,255,255,0.08); position: relative; z-index: 2; }
    .brand-pills { display: flex; align-items: center; gap: 0.5rem; font-weight: 700; font-size: 0.75rem; letter-spacing: 1px; flex-wrap: wrap; }
    .pill { padding: 0.35rem 0.9rem; border-radius: 4px; text-transform: uppercase; }
    .pill.instax { background: var(--instax-teal); color: var(--white); }
    .pill.basha { background: rgba(255,255,255,0.1); color: var(--basha-yellow); border: 1px solid var(--basha-yellow); }
    .hero-content { flex-grow: 1; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; padding: 2rem 1.5rem; position: relative; z-index: 2; }
    .hero-title { font-size: clamp(2.5rem, 8vw, 5rem); line-height: 1.05; margin-bottom: 1.5rem; color: var(--white); }
    .hero-title span { color: var(--instax-teal); font-style: italic; }
    .hero-subtitle { font-size: clamp(1rem, 3vw, 1.3rem); opacity: 0.7; max-width: 500px; line-height: 1.6; }
    .hero-meta { margin-top: 2.5rem; padding-top: 1.5rem; border-top: 1px solid rgba(255,255,255,0.1); display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; font-size: 0.8rem; text-transform: uppercase; letter-spacing: 1px; opacity: 0.5; }
    .scroll-hint { position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%); display: flex; flex-direction: column; align-items: center; gap: 0.5rem; opacity: 0.4; font-size: 0.7rem; text-transform: uppercase; letter-spacing: 2px; z-index: 2; }
    .scroll-arrow { width: 24px; height: 36px; border: 2px solid rgba(255,255,255,0.3); border-radius: 12px; position: relative; }
    .scroll-arrow::after { content: ''; position: absolute; top: 6px; left: 50%; transform: translateX(-50%); width: 4px; height: 8px; background: var(--basha-yellow); border-radius: 2px; animation: scrollBounce 2s infinite; }
    @keyframes scrollBounce { 0%, 100% { top: 6px; opacity: 1; } 50% { top: 16px; opacity: 0.3; } }
    .section { padding: 4rem 0; position: relative; }
    .section-light { background: var(--cream); }
    .section-dark { background: var(--charcoal); color: var(--cream); }
    .section-alt { background: linear-gradient(180deg, var(--cream) 0%, #F0EBE3 100%); }
    .section-header { margin-bottom: 2.5rem; }
    .section-title { font-size: clamp(2rem, 5vw, 3.2rem); line-height: 1.1; margin-bottom: 0.75rem; }
    .section-title span { color: var(--basha-orange); font-style: italic; }
    .section-dark .section-title span { color: var(--basha-yellow); }
    .section-desc { font-size: 1.1rem; opacity: 0.75; max-width: 600px; line-height: 1.6; }
    .timeline-infographic { position: relative; padding-left: 2rem; }
    .timeline-infographic::before { content: ''; position: absolute; left: 8px; top: 0; bottom: 0; width: 3px; background: linear-gradient(180deg, var(--basha-orange), var(--basha-yellow), var(--instax-teal)); border-radius: 2px; }
    .timeline-item { position: relative; margin-bottom: 1.5rem; background: var(--white); border-radius: 10px; overflow: hidden; box-shadow: 0 4px 15px rgba(0,0,0,0.04); border: 1px solid var(--soft-gray); }
    .timeline-item-img { width: 100%; height: 200px; object-fit: cover; }
    .timeline-item-content { padding: 1.5rem 1.5rem 1.5rem 2.5rem; }
    .timeline-item::before { content: ''; position: absolute; left: -1.35rem; top: 1.8rem; width: 16px; height: 16px; border-radius: 50%; background: var(--basha-orange); border: 3px solid var(--cream); box-shadow: 0 0 0 3px var(--basha-orange); z-index: 10; }
    .timeline-item:nth-child(2)::before { background: var(--basha-teal); box-shadow: 0 0 0 3px var(--basha-teal); }
    .timeline-item:nth-child(3)::before { background: var(--basha-yellow); box-shadow: 0 0 0 3px var(--basha-yellow); }
    .timeline-item h4 { font-size: 1.15rem; margin-bottom: 0.4rem; }
    .timeline-tag { display: inline-block; padding: 0.15rem 0.5rem; border-radius: 4px; font-size: 0.65rem; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; background: var(--basha-orange); color: white; }
    .timeline-item:nth-child(2) .timeline-tag { background: var(--basha-teal); }
    .timeline-item:nth-child(3) .timeline-tag { background: var(--basha-yellow); color: var(--charcoal); }
    .metrics-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.2rem; }
    .metric-card { background: var(--white); border-radius: 12px; overflow: hidden; border: 1px solid var(--soft-gray); box-shadow: 0 6px 20px rgba(0,0,0,0.04); position: relative; }
    .metric-card-img { width: 100%; height: 220px; object-fit: cover; }
    .metric-card-content { padding: 1.5rem; text-align: center; }
    .metric-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 4px; background: linear-gradient(90deg, var(--basha-teal), var(--instax-teal)); z-index: 10; }
    .metric-card.orange::before { background: linear-gradient(90deg, var(--basha-orange), #FF8A5C); }
    .metric-card.yellow::before { background: linear-gradient(90deg, var(--basha-yellow), #FFD700); }
    .metric-card.teal::before { background: linear-gradient(90deg, var(--instax-teal), #5DD9D2); }
    .metric-num { font-size: 2.4rem; font-family: 'DM Serif Display', serif; line-height: 1; margin-bottom: 0.4rem; }
    .metric-label { font-size: 0.85rem; opacity: 0.7; line-height: 1.4; }
    .stat-row { margin-bottom: 1.5rem; }
    .stat-header { display: flex; justify-content: space-between; margin-bottom: 0.4rem; }
    .stat-name { font-size: 0.9rem; font-weight: 500; }
    .stat-value { font-size: 0.85rem; font-weight: 700; color: var(--basha-orange); }
    .stat-bar-bg { height: 8px; background: var(--soft-gray); border-radius: 4px; overflow: hidden; }
    .stat-bar-fill { height: 100%; border-radius: 4px; background: linear-gradient(90deg, var(--basha-orange), var(--basha-yellow)); }
    .stat-bar-fill.teal { background: linear-gradient(90deg, var(--basha-teal), var(--instax-teal)); }
    .stat-bar-fill.yellow { background: linear-gradient(90deg, var(--basha-yellow), #FFD700); }
    .tier-cards { display: flex; flex-direction: column; gap: 1rem; }
    .tier-card { display: flex; justify-content: space-between; align-items: center; background: var(--white); padding: 1.3rem 1.5rem; border-radius: 10px; border: 1px solid var(--soft-gray); position: relative; }
    .tier-card::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 5px; background: var(--soft-gray); }
    .tier-card.active::before { background: var(--instax-teal); }
    .tier-card.active { border: 2px solid var(--instax-teal); background: rgba(61, 191, 184, 0.03); box-shadow: 0 4px 20px rgba(61,191,184,0.08); }
    .tier-title { font-size: 1.1rem; margin-bottom: 0.2rem; }
    .tier-desc { font-size: 0.85rem; opacity: 0.6; }
    .tier-badge { padding: 0.3rem 0.8rem; border-radius: 6px; font-size: 0.7rem; font-weight: 700; text-transform: uppercase; background: var(--soft-gray); }
    .tier-card.active .tier-badge { background: var(--instax-teal); color: white; }
    .roi-grid { display: flex; flex-direction: column; gap: 1rem; }
    .roi-item { display: flex; gap: 0; align-items: stretch; background: var(--white); border-radius: 10px; border: 1px solid var(--soft-gray); box-shadow: 0 3px 12px rgba(0,0,0,0.03); overflow: hidden; }
    .roi-item-img { width: 220px; object-fit: cover; flex-shrink: 0; }
    .roi-content { padding: 1.5rem; display: flex; flex-direction: column; justify-content: center; }
    .roi-content h4 { font-size: 1rem; margin-bottom: 0.2rem; }
    .roi-content p { font-size: 0.85rem; opacity: 0.65; line-height: 1.5; }
    .blueprint-container { background: linear-gradient(145deg, #242220, #1A1817); border-radius: 16px; padding: 2rem; border: 1px solid rgba(255,255,255,0.06); position: relative; overflow: hidden; }
    .blueprint-step { display: flex; gap: 1.2rem; margin-bottom: 1.5rem; padding-bottom: 1.5rem; border-bottom: 1px solid rgba(255,255,255,0.06); position: relative; z-index: 1; }
    .blueprint-step:last-child { margin-bottom: 0; padding-bottom: 0; border-bottom: none; }
    .step-num { min-width: 48px; height: 48px; border-radius: 12px; background: linear-gradient(135deg, var(--basha-yellow), var(--basha-orange)); display: flex; align-items: center; justify-content: center; font-family: 'DM Serif Display', serif; font-size: 1.4rem; color: var(--charcoal); font-weight: 400; flex-shrink: 0; }
    .step-content h4 { color: var(--basha-yellow); font-size: 1.05rem; margin-bottom: 0.4rem; text-transform: uppercase; }
    .step-content p { color: rgba(250,246,240,0.6); font-size: 0.9rem; line-height: 1.6; }
    .polaroid-deco { width: 200px; background: white; padding: 0.7rem 0.7rem 1.8rem 0.7rem; box-shadow: 0 10px 25px rgba(0,0,0,0.08); transform: rotate(-3deg); border-radius: 3px; margin: 0 auto; }
    .polaroid-deco img { width: 100%; height: 140px; object-fit: cover; border-radius: 0; margin-bottom: 0.7rem; }
    .polaroid-label { text-align: center; font-family: 'DM Serif Display', serif; font-size: 1rem; color: var(--charcoal); }
    .reach-visual { display: flex; align-items: center; gap: 2rem; flex-wrap: wrap; justify-content: center; }
    .donut-chart { width: 140px; height: 140px; border-radius: 50%; background: conic-gradient(var(--instax-teal) 0deg 165deg, var(--basha-yellow) 165deg 300deg, var(--basha-orange) 300deg 345deg, var(--soft-gray) 345deg 360deg); position: relative; flex-shrink: 0; }
    .donut-hole { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 90px; height: 90px; border-radius: 50%; background: var(--cream); display: flex; flex-direction: column; align-items: center; justify-content: center; }
    .donut-hole .num { font-family: 'DM Serif Display', serif; font-size: 1.3rem; line-height: 1; }
    .donut-hole .label { font-size: 0.6rem; text-transform: uppercase; letter-spacing: 1px; opacity: 0.5; }
    .channel-list { display: flex; flex-direction: column; gap: 0.6rem; }
    .channel-item { display: flex; align-items: center; gap: 0.6rem; font-size: 0.85rem; }
    .channel-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }
    .two-col { display: grid; grid-template-columns: 1fr; gap: 2.5rem; }
    @media (min-width: 768px) { .two-col { grid-template-columns: 1.1fr 0.9fr; } .metrics-grid { grid-template-columns: repeat(4, 1fr); } .roi-item { flex-direction: row; } }
    .deck-footer { background: var(--charcoal); color: var(--cream); padding: 2rem 0; text-align: center; border-top: 3px solid var(--basha-yellow); }
    .footer-pills { display: flex; justify-content: center; gap: 1rem; margin-bottom: 1rem; flex-wrap: wrap; }
    .footer-text { font-size: 0.75rem; opacity: 0.4; text-transform: uppercase; letter-spacing: 1px; }
    .section-divider { height: 6px; background: linear-gradient(90deg, var(--basha-orange) 0%, var(--basha-yellow) 30%, var(--instax-teal) 70%, var(--basha-teal) 100%); }
    .section-divider.thin { height: 3px; }
    .section-divider.dashed { height: 3px; background: repeating-linear-gradient(90deg, var(--basha-yellow) 0, var(--basha-yellow) 10px, transparent 10px, transparent 20px); opacity: 0.4; }
    .pulse-dot { width: 10px; height: 10px; border-radius: 50%; background: var(--instax-teal); position: relative; }
    .pulse-dot::after { content: ''; position: absolute; inset: -4px; border-radius: 50%; border: 2px solid var(--instax-teal); animation: pulse 2s infinite; }
    @keyframes pulse { 0% { transform: scale(1); opacity: 0.6; } 100% { transform: scale(1.8); opacity: 0; } }
    @media (max-width: 768px) { .roi-item { flex-direction: column; } .roi-item-img { width: 100%; } }
    @media (max-width: 480px) { .hero-title { font-size: 2.2rem; } .section { padding: 2.5rem 0; } .metrics-grid { grid-template-columns: 1fr; } .metric-num { font-size: 1.8rem; } }
  </style>
</head>
<body>
  <section class="hero">
    <img src="images-1.jpeg" alt="Constitution Hill" class="hero-bg-img">
    <div class="hero-header">
      <div class="brand-pills"><span class="pill instax">FUJIFILM instax</span><span style="color:var(--basha-yellow);">×</span><span class="pill basha">BASHA UHURU 2026</span></div>
      <div class="deco-dots"><span></span><span></span><span></span></div>
    </div>
    <div class="hero-content">
      <div class="deco-line" style="margin: 0 auto 1.5rem;"></div>
      <h1 class="hero-title">The Festival<br><span>Archive</span></h1>
      <div class="deco-dots" style="justify-content:center; margin-bottom:1.5rem;"><span></span><span></span><span></span></div>
      <p class="hero-subtitle">Freezing youth culture and creative expression live on the historic stones of Constitution Hill.</p>
      <p style="opacity:0.4; font-size:0.9rem; margin-top:1rem;">An experiential, content-led partnership proposal — 14th edition</p>
      <div class="hero-meta"><div style="display:flex;align-items:center;gap:0.5rem;"><div class="pulse-dot"></div>Live Proposal</div><div>Impacta Marketing</div><div>June 2026</div></div>
    </div>
    <div class="scroll-hint"><span>Scroll</span><div class="scroll-arrow"></div></div>
  </section>
  <div class="section-divider"></div>
  <section class="section section-light">
    <div class="container">
      <div class="section-header">
        <div class="section-badge"><span style="font-size:1rem;">●</span> The Platform</div>
        <h2 class="section-title">Unlocking the<br><span>Flagship</span></h2>
        <div class="deco-line"></div>
      </div>
      <div class="two-col">
        <div>
          <p style="font-size:1.15rem; margin-bottom:1.5rem;"><strong style="color:var(--basha-orange);">Timeline:</strong> 25 – 27 June 2026<br><strong style="color:var(--basha-orange);">Venue:</strong> Constitution Hill, Johannesburg</p>
          <p style="opacity:0.75; margin-bottom:1.5rem; line-height:1.7;">This landmark run commemorates the <strong>50th Anniversary of the Youth Uprising</strong>. We activate directly inside Constitution Hill. We establish emotional connection first, then pipeline to commercial activations.</p>
          <div style="background:var(--white); border-radius:10px; padding:1.2rem; border:1px solid var(--soft-gray); border-left:4px solid var(--basha-yellow);"><p style="font-size:0.85rem; opacity:0.7; font-style:italic;">"We establish the emotional connection here first, setting up a perfect pipeline for commercial mall activations later."</p></div>
        </div>
        <div class="timeline-infographic">
          <div class="timeline-item"><img src="images-3.jpeg" alt="Day 01" class="timeline-item-img"><div class="timeline-item-content"><span class="timeline-tag">Day 01</span><h4>Creative Conference</h4><p style="font-size:0.9rem; opacity:0.65; margin-top:0.3rem;">Masterclasses and digital designer panels with industry leaders.</p></div></div>
          <div class="timeline-item"><img src="images-2.jpeg" alt="Day 02" class="timeline-item-img"><div class="timeline-item-content"><span class="timeline-tag">Day 02</span><h4>Curated Makers Market</h4><p style="font-size:0.9rem; opacity:0.65; margin-top:0.3rem;">Direct touchpoints with alternative creative brands and artisans.</p></div></div>
          <div class="timeline-item"><img src="images-3.png" alt="Day 03" class="timeline-item-img"><div class="timeline-item-content"><span class="timeline-tag">Day 03</span><h4>Freedom Soundstage</h4><p style="font-size:0.9rem; opacity:0.65; margin-top:0.3rem;"><strong>7,000+</strong> fashion-forward, energetic spectators live.</p></div></div>
        </div>
      </div>
    </div>
  </section>
  <div class="section-divider dashed"></div>
  <section class="section section-alt">
    <div class="container">
      <div class="section-header" style="text-align:center;">
        <div class="section-badge"><span style="font-size:1rem;">●</span> Footprint Metrics</div>
        <h2 class="section-title">High Impact<br><span>Human Traffic</span></h2>
        <div class="deco-line" style="margin:1rem auto;"></div>
        <p class="section-desc" style="max-width:550px; margin:0 auto;">Direct product-in-hand exposure with active South African lifestyle architects, creators, and cultural innovators.</p>
      </div>
      <div class="metrics-grid" style="margin: 2.5rem 0;">
        <div class="metric-card orange"><img src="images-4.jpeg" alt="Attendees" class="metric-card-img"><div class="metric-card-content"><div class="metric-num" style="color:var(--basha-orange);">7,400+</div><div class="metric-label">Ticketed Festival Attendees</div></div></div>
        <div class="metric-card yellow"><img src="images-2.jpeg" alt="Age" class="metric-card-img"><div class="metric-card-content"><div class="metric-num" style="color:#B8860B;">18-35</div><div class="metric-label">Core Creator Age Demo</div></div></div>
        <div class="metric-card"><img src="images-5.jpeg" alt="Media" class="metric-card-img"><div class="metric-card-content"><div class="metric-num" style="color:var(--basha-teal);">675+</div><div class="metric-label">On-Site Media & Specialists</div></div></div>
        <div class="metric-card teal"><img src="images-6.jpeg" alt="Makers" class="metric-card-img"><div class="metric-card-content"><div class="metric-num" style="color:var(--instax-teal);">172+</div><div class="metric-label">Makers Market Small Businesses</div></div></div>
      </div>
      <div style="background:var(--white); border-radius:14px; padding:2rem; border:1px solid var(--soft-gray);"><h3 style="font-size:1.1rem; margin-bottom:1.5rem; color:var(--basha-orange);">Audience Composition</h3>
        <div class="stat-row"><div class="stat-header"><span class="stat-name">Creators & Influencers</span><span class="stat-value">42%</span></div><div class="stat-bar-bg"><div class="stat-bar-fill" style="width:42%"></div></div></div>
        <div class="stat-row"><div class="stat-header"><span class="stat-name">Fashion & Style Enthusiasts</span><span class="stat-value" style="color:var(--basha-teal);">28%</span></div><div class="stat-bar-bg"><div class="stat-bar-fill teal" style="width:28%"></div></div></div>
        <div class="stat-row"><div class="stat-header"><span class="stat-name">Music & Arts Collectors</span><span class="stat-value" style="color:var(--basha-yellow);">18%</span></div><div class="stat-bar-bg"><div class="stat-bar-fill yellow" style="width:18%"></div></div></div>
        <div class="stat-row" style="margin-bottom:0;"><div class="stat-header"><span class="stat-name">Press, Media & VIPs</span><span class="stat-value" style="color:var(--warm-gray);">12%</span></div><div class="stat-bar-bg"><div class="stat-bar-fill" style="width:12%; background:var(--warm-gray);"></div></div></div>
      </div>
    </div>
  </section>
  <div class="section-divider thin"></div>
  <section class="section section-light">
    <div class="container">
      <div class="section-header">
        <div class="section-badge"><span style="font-size:1rem;">●</span> Sponsorship</div>
        <h2 class="section-title">Ecosystem<br><span>Integration</span></h2>
        <div class="deco-line"></div>
      </div>
      <div class="two-col">
        <div><p style="font-size:1.1rem; margin-bottom:1.5rem; line-height:1.6;">Massive macro-media campaign reach. The festival operates an intensive <strong style="color:var(--basha-orange);">2-Month Media Runway</strong> generating exceptional brand visibility.</p>
          <div style="background:var(--white); border-radius:14px; padding:1.5rem; border:1px solid var(--soft-gray); margin-bottom:1.5rem;"><img src="images-4.jpeg" alt="Media Reach" style="width:100%; border-radius:10px; margin-bottom:1rem;"><h4 style="font-size:0.95rem; margin-bottom:1rem; text-transform:uppercase; letter-spacing:1px; opacity:0.5;">Media Reach Distribution</h4>
            <div class="reach-visual"><div class="donut-chart"><div class="donut-hole"><span class="num">6.98M</span><span class="label">Total Reach</span></div></div>
              <div class="channel-list">
                <div class="channel-item"><div class="channel-dot" style="background:var(--instax-teal);"></div><span>Digital & Social (46%)</span></div>
                <div class="channel-item"><div class="channel-dot" style="background:var(--basha-yellow);"></div><span>Radio & Broadcast (38%)</span></div>
                <div class="channel-item"><div class="channel-dot" style="background:var(--basha-orange);"></div><span>Print & OOH (13%)</span></div>
                <div class="channel-item"><div class="channel-dot" style="background:var(--soft-gray);"></div><span>Other (3%)</span></div>
              </div>
            </div>
          </div>
          <div style="display:flex; align-items:center; gap:1rem; background: linear-gradient(135deg, rgba(61,191,184,0.08), rgba(244,184,36,0.08)); border-radius:10px; padding:1.2rem 1.5rem; border:1px solid rgba(61,191,184,0.2);"><div style="font-size:2.5rem; font-family:'DM Serif Display', serif; color:var(--instax-teal);">92%</div><div><div style="font-weight:700; font-size:0.9rem;">Positive Brand Sentiment</div><div style="font-size:0.8rem; opacity:0.5; margin-top:0.2rem;">Across all tracked national channels</div></div></div>
        </div>
        <div class="tier-cards">
          <div class="tier-card"><div><div class="tier-title">Headline Sponsor</div><div class="tier-desc">Complete festival platform presence</div></div><span class="tier-badge">Tier 1</span></div>
          <div class="tier-card active"><div><div class="tier-title" style="color:var(--instax-teal);">Supporting Partner</div><div class="tier-desc">Immersive experiential execution & photo hubs</div></div><span class="tier-badge">✓ Fit</span></div>
          <div class="tier-card"><div><div class="tier-title">Program Sponsor</div><div class="tier-desc">Creative conference workshop co-presentation</div></div><span class="tier-badge">Tier 3</span></div>
        </div>
      </div>
    </div>
  </section>
  <div class="section-divider dashed"></div>
  <section class="section section-alt">
    <div class="container">
      <div class="section-header" style="text-align:center;">
        <div class="section-badge"><span style="font-size:1rem;">●</span> Deliverable Track</div>
        <h2 class="section-title">Strategic<br><span>Value Delivery</span></h2>
        <div class="deco-line" style="margin:1rem auto;"></div>
        <p class="section-desc" style="margin:0 auto;">Converting collaborative brand equity into long-term cultural alignment.</p>
      </div>
      <div class="roi-grid" style="max-width:900px; margin:2rem auto 0;">
        <div class="roi-item"><img src="images-5.jpeg" alt="Presence" class="roi-item-img"><div class="roi-content"><h4>Structural Presence</h4><p>Premium custom interactive experiential photo zones with full brand immersion.</p></div></div>
        <div class="roi-item"><img src="images-6.jpeg" alt="Content" class="roi-item-img"><div class="roi-content"><h4>Content Dominance</h4><p>Logo placement on all digital assets, video highlights, and PR rollouts for maximum visibility.</p></div></div>
        <div class="roi-item"><img src="images-7.jpeg" alt="Sampling" class="roi-item-img"><div class="roi-content"><h4>Direct Sampling</h4><p>Premium bundling inside official artist, press, and VIP gift packs for tactile brand experience.</p></div></div>
        <div class="roi-item"><img src="images-6.jpeg" alt="Hospitality" class="roi-item-img"><div class="roi-content"><h4>Hospitality Suite</h4><p>Assigned allocations for live performance arenas and executive networking lounges.</p></div></div>
      </div>
    </div>
  </section>
  <div class="section-divider thin"></div>
  <section class="section section-dark">
    <div class="container">
      <div class="section-header" style="text-align:center;">
        <div class="section-badge light"><span style="font-size:1rem;">●</span> Blueprint</div>
        <h2 class="section-title">The Blueprint:<br><span>The Archive Hub</span></h2>
        <div class="deco-line" style="margin:1rem auto; background:linear-gradient(90deg, var(--basha-yellow), var(--instax-teal));"></div>
        <p class="section-desc" style="color:rgba(250,246,240,0.6);">Turning attendees into dynamic curators of history. We make the camera feel essential to creative preservation.</p>
      </div>
      <div class="two-col" style="margin-top:2rem;">
        <div><p style="font-size:1.05rem; color:rgba(250,246,240,0.7); line-height:1.7; margin-bottom:2rem;">By highlighting self-expression at Constitution Hill, we build the ultimate brand foundation to launch upcoming commercial pushes with maximum cultural backing.</p>
          <div class="polaroid-deco"><img src="images-7.jpeg" alt="Archive"><div class="polaroid-label">CULTURE '26</div></div>
        </div>
        <div class="blueprint-container">
          <div class="blueprint-step">
            <div class="step-num">1</div>
            <div class="step-content">
              <h4>The Living Archive Installation</h4>
              <p>A striking physical structure in the central courtyard where attendees pin their live street style Instax snaps, building an interactive art mosaic.</p>
            </div>
          </div>
          <div class="blueprint-step">
            <div class="step-num">2</div>
            <div class="step-content">
              <h4>Masterclass Creative Roamers</h4>
              <p>Equipping design student leaders with Instax setups during June 26 conference panels to log instant behind-the-scenes portfolios.</p>
            </div>
          </div>
          <div class="blueprint-step">
            <div class="step-num">3</div>
            <div class="step-content">
              <h4>Soundstage Lookbook Zones</h4>
              <p>Vibrant photo framing installations at the main concert gates to tag incoming alternative fashion looks in real time.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <footer class="deck-footer">
    <div class="container">
      <div class="footer-pills"><span class="pill instax">FUJIFILM instax</span><span style="color:var(--basha-yellow);">×</span><span class="pill basha">BASHA UHURU 2026</span></div>
      <div class="deco-dots" style="justify-content:center; margin-bottom:1rem;"><span></span><span></span><span></span></div>
      <div class="footer-text">Impacta Marketing Partner Strategy | June 2026</div>
    </div>
  </footer>
</body>
</html>
