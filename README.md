<!DOCTYPE html>
<html lang="ka">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Geonation SMP</title>

  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Press Start 2P', cursive;
      color: white;
      background: linear-gradient(180deg, #00ff99, #00cc66);
      transition: background 1s ease;
      overflow-x: hidden;
    }

    /* FLOATING ANIMATION */
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0px); }
    }

    /* GLOW */
    @keyframes glow {
      0% { box-shadow: 0 0 10px #00ff99; }
      50% { box-shadow: 0 0 25px #00ffff; }
      100% { box-shadow: 0 0 10px #00ff99; }
    }

    header {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 70px;
      display: flex; align-items: center;
      padding: 0 20px;
      background: rgba(0,0,0,0.45);
      z-index: 1000;
    }

    .socials a {
      font-size: 26px;
      margin-right: 15px;
      animation: float 3s ease-in-out infinite;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding-top: 70px;
    }

    .hero h1 {
      font-size: 46px;
      text-shadow: 4px 4px #000;
      animation: float 4s ease-in-out infinite;
    }

    .pickaxe { animation: float 2s ease-in-out infinite; }

    .status {
      margin-top: 25px;
      padding: 20px 30px;
      border: 3px solid #00ff99;
      background: rgba(0,0,0,0.6);
      animation: glow 3s infinite;
    }

    section { padding: 120px 20px; text-align: center; }

    h2 { font-size: 30px; margin-bottom: 40px; }

    .cards, .ranks {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 25px;
      max-width: 1100px;
      margin: auto;
    }

    .card, .rank {
      padding: 25px;
      background: rgba(0,0,0,0.6);
      border: 3px solid #00ffff;
      animation: glow 4s infinite;
      transition: transform 0.3s ease;
    }

    .card:hover, .rank:hover {
      transform: scale(1.08) rotate(-1deg);
    }

    footer {
      padding: 70px 20px;
      background: rgba(0,0,0,0.7);
      text-align: center;
    }
  
    /* PARTICLES */
    .particle {
      position: fixed;
      width: 6px;
      height: 6px;
      background: rgba(0,255,255,0.7);
      animation: particleMove linear infinite;
      z-index: -1;
    }

    @keyframes particleMove {
      from { transform: translateY(100vh); opacity: 1; }
      to { transform: translateY(-10vh); opacity: 0; }
    }
  </style>
</head>
<body>

<header>
  <div class="socials">
    <a href="https://discord.gg/34VAZTR8" target="_blank">💬</a>
    <a href="https://www.tiktok.com/@mc_itzzmg" target="_blank">🎵</a>
  </div>
</header>

<div class="hero">
  <h1>GEONATION SMP <span class="pickaxe">⛏️</span></h1>
  <p>Minecraft Georgian Server</p>
  <div class="status">
    <p>სტატუსი: 🟢 ONLINE</p>
    <p>ვერსია: 1.21</p>
    <p>IP: Geonation.aternos.me</p>
  </div>
</div>

<section>
  <h2>გეიმოდები</h2>
  <div class="cards">
    <div class="card">🔥 LifeSteal</div>
    <div class="card">🌍 Survival</div>
    <div class="card">🧱 OneBlock</div>
    <div class="card">⚔️ Kit-PvP</div>
  </div>
</section>

<section>
  <h2>რანკები</h2>
  <div class="ranks">
    <div class="rank">Elite</div>
    <div class="rank">Admin</div>
    <div class="rank">Helper</div>
    <div class="rank">Warrior</div>
    <div class="rank">Hero</div>
    <div class="rank">Media</div>
    <div class="rank">Member</div>
    <div class="rank">Member</div>
  </div>
</section>

<footer>
  <p>© 2026 Geonation SMP</p>
</footer>

<script>
window.addEventListener('scroll', () => {
  const p = window.scrollY / (document.body.scrollHeight - window.innerHeight);
  if (p < 0.5) {
    document.body.style.background = 'linear-gradient(180deg,#00ff99,#0066ff)';
  } else {
    document.body.style.background = 'linear-gradient(180deg,#0066ff,#00ffff)';
  }
});


// PARTICLE GENERATOR
for (let i = 0; i < 40; i++) {
  const p = document.createElement('div');
  p.className = 'particle';
  p.style.left = Math.random() * 100 + 'vw';
  p.style.animationDuration = 5 + Math.random() * 10 + 's';
  p.style.animationDelay = Math.random() * 5 + 's';
  document.body.appendChild(p);
}

</script>

</body>
</html>
