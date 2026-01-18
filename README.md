<!DOCTYPE html>
<html lang="ka">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Geonation SMP</title>
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
  font-family:'Press Start 2P',cursive;
  color:#fff;
  background:linear-gradient(180deg,#00ff99,#0099ff);
  overflow-x:hidden;
  transition:background 1s ease;
}

@keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-12px)}100%{transform:translateY(0)}}
@keyframes glow{0%{box-shadow:0 0 10px}50%{box-shadow:0 0 30px}100%{box-shadow:0 0 10px}}

header{
  position:fixed;top:0;left:0;width:100%;height:70px;
  display:flex;align-items:center;padding:0 25px;
  background:rgba(0,0,0,.5);z-index:999
}
.socials a{font-size:26px;margin-right:15px;animation:float 3s infinite}

.hero{
  min-height:100vh;display:flex;flex-direction:column;
  align-items:center;justify-content:center;text-align:center
}
.hero h1{font-size:48px;animation:float 4s infinite;text-shadow:4px 4px #000}

.status{
  margin-top:25px;padding:20px 35px;
  border:3px solid #00ff99;background:rgba(0,0,0,.6);
  animation:glow 3s infinite;color:#00ff99
}

section{padding:120px 40px}
section h2{text-align:center;font-size:32px;margin-bottom:50px}

/* GAMEMODES */
.gamemodes{
  display:flex;justify-content:center;gap:30px;flex-wrap:wrap
}
.mode{
  width:260px;padding:30px;text-align:center;
  border:3px solid #00ffff;background:rgba(0,0,0,.6);
  animation:glow 4s infinite;transition:.3s
}
.mode:hover{transform:scale(1.1)}

/* RANKS */
.ranks{
  display:flex;flex-wrap:wrap;gap:20px;justify-content:flex-end
}
.rank{
  width:200px;padding:18px;text-align:center;
  border:3px solid;animation:float 3s infinite
}

.elite{border-color:#00ffff;color:#00ffff}
.admin{border-color:#ff3333;color:#ff3333}
.helper{border-color:#33ff99;color:#33ff99}
.warrior{border-color:#ffaa00;color:#ffaa00}
.hero-r{border-color:#aa00ff;color:#aa00ff}
.media{border-color:#00ccff;color:#00ccff}
.member{border-color:#ffffff;color:#ffffff}

/* PARTICLES */
.particle{
  position:fixed;width:6px;height:6px;
  background:rgba(0,255,255,.7);
  animation:particleMove linear infinite;z-index:-1
}
@keyframes particleMove{from{transform:translateY(100vh)}to{transform:translateY(-10vh);opacity:0}}

footer{text-align:center;padding:70px;background:rgba(0,0,0,.7)}
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
<h1>GEONATION SMP ⛏️</h1>
<div class="status">
<p>🟢 ONLINE</p>
<p>Version: 1.21</p>
<p>IP: Geonation.aternos.me</p>
</div>
</div>

<section>
<h2>🎮 GAMEMODES</h2>
<div class="gamemodes">
<div class="mode">🔥 LifeSteal</div>
<div class="mode">🌍 Survival</div>
<div class="mode">🧱 OneBlock</div>
<div class="mode">⚔️ Kit-PvP</div>
</div>
</section>

<section>
<h2>👑 RANKS</h2>
<div class="ranks">
<div class="rank elite">💎 Elite</div>
<div class="rank admin">🛑 Admin</div>
<div class="rank helper">🛠 Helper</div>
<div class="rank warrior">⚔️ Warrior</div>
<div class="rank hero-r">🦸 Hero</div>
<div class="rank media">🎥 Media</div>
<div class="rank member">👤 Member</div>
<div class="rank member">👤 Member</div>
</div>
</section>

<footer>© 2026 Geonation SMP</footer>

<script>
for(let i=0;i<45;i++){
 const p=document.createElement('div');
 p.className='particle';
 p.style.left=Math.random()*100+'vw';
 p.style.animationDuration=5+Math.random()*10+'s';
 document.body.appendChild(p);
}

window.addEventListener('scroll',()=>{
 const p=window.scrollY/(document.body.scrollHeight-window.innerHeight);
 if(p<0.5){document.body.style.background='linear-gradient(180deg,#00ff99,#0066ff)'}
 else{document.body.style.background='linear-gradient(180deg,#0066ff,#00ffff)'}
});
</script>
</body>
</html>
