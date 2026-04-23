<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>🎮 WebDev | Gaming & Esports | GitHub Profile README</title>
  <!-- Font Awesome 6 for professional icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0a0c0f;
      font-family: 'Segoe UI', 'Poppins', system-ui, -apple-system, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem;
      background-image: radial-gradient(circle at 20% 10%, #1e2a3a 0%, #030507 90%);
      position: relative;
      overflow-x: hidden;
    }

    /* subtle animated grid overlay (game feel) */
    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        linear-gradient(rgba(0, 255, 196, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0, 255, 196, 0.03) 1px, transparent 1px);
      background-size: 50px 50px;
      pointer-events: none;
      animation: gridPulse 8s infinite alternate ease-in-out;
    }

    @keyframes gridPulse {
      0% { opacity: 0.3; }
      100% { opacity: 0.7; }
    }

    .profile-card {
      max-width: 1000px;
      width: 100%;
      background: rgba(10, 15, 22, 0.8);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border: 1px solid rgba(0, 255, 200, 0.25);
      border-radius: 3rem 1rem 3rem 1rem;
      box-shadow: 0 30px 50px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(0, 255, 200, 0.15), 0 0 30px rgba(0, 180, 216, 0.5);
      padding: 2.5rem 2.2rem;
      position: relative;
      z-index: 10;
      transition: all 0.3s ease;
      color: #e0f2fe;
      animation: floatCard 6s infinite ease-in-out;
    }

    @keyframes floatCard {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
      100% { transform: translateY(0px); }
    }

    /* neon corner accents */
    .profile-card::after {
      content: "";
      position: absolute;
      top: -2px;
      left: -2px;
      right: -2px;
      bottom: -2px;
      background: linear-gradient(45deg, #00f2fe, #4facfe, #00e5ff, #1effbc);
      z-index: -1;
      border-radius: 3.2rem 1.2rem 3.2rem 1.2rem;
      opacity: 0.4;
      filter: blur(10px);
      animation: borderGlow 4s linear infinite;
    }

    @keyframes borderGlow {
      0% { opacity: 0.3; filter: blur(8px); }
      50% { opacity: 0.7; filter: blur(14px); }
      100% { opacity: 0.3; filter: blur(8px); }
    }

    /* header section with game-like title */
    .header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      margin-bottom: 2.5rem;
      border-bottom: 2px solid rgba(0, 255, 200, 0.4);
      padding-bottom: 1.5rem;
    }

    .level-badge {
      background: #111c2b;
      padding: 0.5rem 1.5rem;
      border-radius: 3rem;
      font-weight: 700;
      font-size: 1.2rem;
      letter-spacing: 2px;
      color: #00f2fe;
      text-shadow: 0 0 8px #00e5ff;
      border: 1px solid #2dd4bf;
      box-shadow: 0 0 15px rgba(0, 229, 255, 0.6);
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .title h1 {
      font-size: 2.8rem;
      font-weight: 800;
      background: linear-gradient(to right, #a5f3fc, #67e8f9, #22d3ee);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 0 0 25px #06b6d4;
      letter-spacing: 1px;
    }

    .subtitle {
      color: #9ca3af;
      font-size: 1.1rem;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      margin-top: 0.3rem;
    }

    .stats-grid {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
      margin: 2rem 0 1.8rem;
    }

    .stat-item {
      background: rgba(0, 20, 30, 0.7);
      backdrop-filter: blur(12px);
      border: 1px solid #00e5ff40;
      border-radius: 1.5rem;
      padding: 1rem 1.8rem;
      display: flex;
      align-items: center;
      gap: 1rem;
      transition: 0.25s;
      box-shadow: 0 8px 20px rgba(0,0,0,0.6);
    }

    .stat-item:hover {
      transform: scale(1.05);
      border-color: #2dd4bf;
      box-shadow: 0 0 25px #00e5ff;
    }

    .stat-icon {
      font-size: 2rem;
      color: #2dd4bf;
      filter: drop-shadow(0 0 8px cyan);
    }

    .demo-section {
      margin: 2.8rem 0 2rem;
    }

    .section-title {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 1.8rem;
      display: flex;
      align-items: center;
      gap: 0.8rem;
      color: #bae6fd;
      text-transform: uppercase;
      letter-spacing: 3px;
      border-left: 6px solid #06b6d4;
      padding-left: 1.5rem;
      text-shadow: 0 0 10px #38bdf8;
    }

    .demo-cards {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
      justify-content: center;
    }

    .demo-card {
      background: linear-gradient(145deg, #0b1a2f, #030c17);
      border: 1px solid rgba(0, 255, 200, 0.5);
      border-radius: 2rem 0.5rem 2rem 0.5rem;
      padding: 1.8rem 1.5rem;
      flex: 1 1 250px;
      min-width: 220px;
      backdrop-filter: blur(10px);
      position: relative;
      transition: all 0.3s cubic-bezier(0.23, 1, 0.32, 1);
      box-shadow: 0 12px 28px rgba(0,0,0,0.7), inset 0 0 25px rgba(0,180,216,0.2);
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .demo-card:hover {
      transform: translateY(-10px) scale(1.02);
      border-color: #f0e68c;
      box-shadow: 0 0 40px #ffd966, 0 20px 30px black;
    }

    .game-icon {
      font-size: 3.2rem;
      margin-bottom: 1rem;
      filter: drop-shadow(0 0 12px currentColor);
    }

    .demo-card h3 {
      font-size: 1.6rem;
      font-weight: 700;
      color: #facc15;
      text-shadow: 0 0 15px #fbbf24;
      margin: 0.5rem 0;
    }

    .demo-card p {
      color: #cbd5e1;
      margin: 0.8rem 0 1.5rem;
      font-size: 0.95rem;
    }

    .demo-link {
      background: #0f1a2b;
      border: 1px solid #2dd4bf;
      padding: 0.6rem 1.8rem;
      border-radius: 3rem;
      color: #bae6fd;
      font-weight: bold;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      transition: 0.25s;
      letter-spacing: 0.5px;
      margin-top: auto;
      background: rgba(0, 229, 255, 0.1);
    }

    .demo-link:hover {
      background: #06b6d4;
      color: #020617;
      border-color: #facc15;
      box-shadow: 0 0 30px #fbbf24;
      font-weight: 800;
    }

    .footer-note {
      margin-top: 2.8rem;
      text-align: center;
      font-size: 1rem;
      color: #94a3b8;
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
      border-top: 1px dashed #2dd4bf;
      padding-top: 2rem;
    }

    .glitch-text {
      animation: textFlicker 1.8s infinite alternate;
    }

    @keyframes textFlicker {
      0% { opacity: 1; text-shadow: 0 0 8px cyan; }
      50% { opacity: 0.9; text-shadow: 0 0 18px #f0e68c; }
      100% { opacity: 1; text-shadow: 0 0 12px #06b6d4; }
    }

    @media (max-width: 650px) {
      .profile-card {
        padding: 1.8rem;
      }
      .title h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>
  <div class="profile-card">
    
    <!-- Header with gamer identity -->
    <div class="header">
      <div class="title">
        <h1>⚡ VENOM_X/WebDev</h1>
        <div class="subtitle">
          <i class="fas fa-gamepad"></i> <span>Gaming & Esports Architect</span>
          <i class="fas fa-code"></i> <span>Full-Stack</span>
        </div>
      </div>
      <div class="level-badge">
        <i class="fas fa-crown"></i> LVL. 99 <i class="fas fa-star"></i>
      </div>
    </div>

    <!-- Stats / skills showcase -->
    <div class="stats-grid">
      <div class="stat-item">
        <i class="fas fa-rocket stat-icon"></i>
        <div><strong>5+</strong><br><small>Years PvP</small></div>
      </div>
      <div class="stat-item">
        <i class="fas fa-globe stat-icon"></i>
        <div><strong>20+</strong><br><small>Sites Deployed</small></div>
      </div>
      <div class="stat-item">
        <i class="fas fa-trophy stat-icon"></i>
        <div><strong>Esports</strong><br><small>Specialist</small></div>
      </div>
    </div>

    <!-- Demo sites section with game animations -->
    <div class="demo-section">
      <div class="section-title">
        <i class="fas fa-ghost"></i> FEATURED QUESTS <i class="fas fa-sword"></i>
      </div>
      <div class="demo-cards">
        
        <!-- Dead by Daylight Fan Made -->
        <div class="demo-card">
          <div class="game-icon" style="color: #ff4d4d;">
            <i class="fas fa-skull"></i>
          </div>
          <h3>DEAD BY DAYLIGHT</h3>
          <p><i class="fas fa-fan"></i> Fan Made Hub · Killers & Survivors</p>
          <a href="https://deadbydaylight-fanmade.example.com" target="_blank" rel="noopener" class="demo-link">
            <i class="fas fa-external-link-alt"></i> ENTER FOG
          </a>
          <div style="margin-top: 0.8rem; font-size:0.8rem; color:#86efac;">
            <i class="fas fa-check-circle"></i> Interactive bloodweb
          </div>
        </div>

        <!-- Rody Gamer Blog -->
        <div class="demo-card">
          <div class="game-icon" style="color: #fbbf24;">
            <i class="fas fa-blog"></i>
          </div>
          <h3>RODY GAMER</h3>
          <p><i class="fas fa-pen-fancy"></i> Personal Gaming Blog · Reviews</p>
          <a href="https://rodygamer-blog.example.com" target="_blank" rel="noopener" class="demo-link">
            <i class="fas fa-external-link-alt"></i> READ BLOG
          </a>
          <div style="margin-top: 0.8rem; font-size:0.8rem; color:#86efac;">
            <i class="fas fa-fire"></i> Latest: Elden Ring DLC
          </div>
        </div>

        <!-- Esports Blog -->
        <div class="demo-card">
          <div class="game-icon" style="color: #38bdf8;">
            <i class="fas fa-trophy"></i>
          </div>
          <h3>ESPORTS ARENA</h3>
          <p><i class="fas fa-newspaper"></i> Competitive News & Analysis</p>
          <a href="https://esportsblog-pro.example.com" target="_blank" rel="noopener" class="demo-link">
            <i class="fas fa-external-link-alt"></i> VIEW COVERAGE
          </a>
          <div style="margin-top: 0.8rem; font-size:0.8rem; color:#86efac;">
            <i class="fas fa-headset"></i> Live tournament updates
          </div>
        </div>
      </div>
    </div>

    <!-- Extra gaming flare / skill tags -->
    <div style="display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center; margin: 2rem 0 0.5rem;">
      <span style="background:#0f1a2b; padding:0.4rem 1.4rem; border-radius: 20px; border:1px solid cyan;"><i class="fab fa-react"></i> React</span>
      <span style="background:#0f1a2b; padding:0.4rem 1.4rem; border-radius: 20px; border:1px solid cyan;"><i class="fab fa-node-js"></i> Node.js</span>
      <span style="background:#0f1a2b; padding:0.4rem 1.4rem; border-radius: 20px; border:1px solid cyan;"><i class="fas fa-database"></i> MongoDB</span>
      <span style="background:#0f1a2b; padding:0.4rem 1.4rem; border-radius: 20px; border:1px solid cyan;"><i class="fab fa-unity"></i> Three.js</span>
    </div>

    <!-- Footer with animated glitch text -->
    <div class="footer-note">
      <span class="glitch-text"><i class="fas fa-terminal"></i> READY FOR BATTLE</span>
      <span><i class="fas fa-map-pin"></i> GITHUB/PROFILE · GAMING FIRST</span>
      <span><i class="fas fa-headphones"></i> COMMISSIONS OPEN</span>
    </div>

    <!-- subtle animated particles (pure css illusion) -->
    <div style="position: absolute; top: 15px; right: 25px; font-size: 0.9rem; opacity:0.7; animation: spinSlow 10s linear infinite;">
      <i class="fas fa-circle" style="color:#2dd4bf;"></i> <i class="fas fa-circle" style="color:#facc15; margin-left:5px;"></i>
    </div>
    @keyframes spinSlow {
      from {transform: rotate(0deg);}
      to {transform: rotate(360deg);}
    }
  </div>
</body>
</html>
