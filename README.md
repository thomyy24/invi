# invi<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mis 15 Años - Agus ✨</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#000000;
    --bg-2:#0a0a0c;
    --silver:#e8e9ec;
    --silver-2:#b9bcc4;
    --silver-dim:#8b8e97;
    --hot:#d4d6de;
    --card:rgba(255,255,255,0.035);
    --card-border:rgba(255,255,255,0.12);
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html,body{background:var(--bg);}
  body{
    font-family:'Montserrat',sans-serif;
    color:var(--silver);
    min-height:100vh;
    display:flex;
    justify-content:center;
    overflow-x:hidden;
    position:relative;
  }

  /* ---------- Fondo negro con brillos en movimiento ---------- */
  #glitter-canvas{
    position:fixed;
    inset:0;
    width:100%;
    height:100%;
    z-index:999;
    pointer-events:none;
  }

  .stage{
    width:100%;
    max-width:460px;
    min-height:100vh;
    position:relative;
    z-index:2;
    padding:0 22px 60px;
  }

  /* ---------- Marco decorativo (elementos enviados) ---------- */
  .frame-deco{
    position:absolute;
    top:0;
    left:50%;
    transform:translateX(-50%);
    width:100%;
    max-width:460px;
    height:100%;
    min-height:100%;
    object-fit:cover;
    object-position:top;
    z-index:1;
    pointer-events:none;
    opacity:0.9;
    mix-blend-mode:screen;
  }

  /* ---------- Bolas de espejos reales (detrás de las estrellas) ---------- */
  .bg-disco{
    position:fixed;
    z-index:1;
    border-radius:50%;
    pointer-events:none;
    background:
      repeating-linear-gradient(45deg, rgba(255,255,255,0.30) 0 2px, rgba(4,4,6,0.6) 2px 4.2px),
      repeating-linear-gradient(-45deg, rgba(255,255,255,0.24) 0 2px, rgba(4,4,6,0.4) 2px 4.2px),
      repeating-linear-gradient(0deg, rgba(0,0,0,0.45) 0 0.8px, transparent 0.8px 4.2px),
      repeating-linear-gradient(90deg, rgba(0,0,0,0.45) 0 0.8px, transparent 0.8px 4.2px),
      radial-gradient(circle at 30% 24%, #ffffff 0%, #e7e9ee 10%, #c3c5cd 30%, #90929c 55%, #4c4e55 78%, #202124 100%);
    box-shadow:
      inset -18px -18px 30px rgba(0,0,0,0.7),
      inset 14px 14px 24px rgba(255,255,255,0.45),
      inset 0 0 2px rgba(255,255,255,0.3),
      0 0 50px 12px rgba(255,255,255,0.28),
      0 25px 45px rgba(0,0,0,0.55);
  }
  .bg-disco::before{
    content:'';
    position:absolute;
    inset:0;
    border-radius:50%;
    background:
      radial-gradient(circle at 22% 16%, rgba(255,255,255,0.95) 0%, transparent 2.5%),
      radial-gradient(circle at 52% 9%, rgba(255,255,255,0.8) 0%, transparent 2%),
      radial-gradient(circle at 74% 26%, rgba(255,255,255,0.9) 0%, transparent 1.8%),
      radial-gradient(circle at 13% 48%, rgba(255,255,255,0.7) 0%, transparent 2.2%),
      radial-gradient(circle at 38% 62%, rgba(255,255,255,0.85) 0%, transparent 1.8%),
      radial-gradient(circle at 82% 55%, rgba(255,255,255,0.75) 0%, transparent 2%),
      radial-gradient(circle at 63% 80%, rgba(255,255,255,0.65) 0%, transparent 1.8%),
      radial-gradient(circle at 90% 20%, rgba(255,255,255,0.6) 0%, transparent 1.6%),
      radial-gradient(circle at 28% 85%, rgba(255,255,255,0.55) 0%, transparent 1.6%);
    mix-blend-mode:screen;
    animation: sparkleTwinkle 2.2s ease-in-out infinite;
  }
  @keyframes sparkleTwinkle{
    0%,100%{opacity:0.45;}
    50%{opacity:1;}
  }
  .bg-disco--1{
    width:150px;
    height:150px;
    top:8%;
    right:-35px;
    opacity:0.95;
    animation: discoRotate 22s linear infinite, discoDrift1 14s ease-in-out infinite;
  }
  .bg-disco--1::before{ animation-delay:0s; }
  .bg-disco--2{
    width:100px;
    height:100px;
    bottom:12%;
    left:-30px;
    opacity:0.9;
    animation: discoRotate 28s linear infinite reverse, discoDrift2 18s ease-in-out infinite;
  }
  .bg-disco--2::before{ animation-delay:1.1s; }
  @keyframes discoRotate{
    from{transform:rotate(0deg);}
    to{transform:rotate(360deg);}
  }
  @keyframes discoDrift1{
    0%,100%{transform:translateY(0px);}
    50%{transform:translateY(18px);}
  }
  @keyframes discoDrift2{
    0%,100%{transform:translateY(0px);}
    50%{transform:translateY(-16px);}
  }

  header{
    position:relative;
    z-index:3;
    text-align:center;
    padding-top:20px;
    margin-bottom:10px;
  }

  .eyebrow{
    font-family:'Cormorant Garamond',serif;
    font-style:italic;
    font-size:13.5pt;
    color:var(--silver-2);
    letter-spacing:0.5px;
    max-width:300px;
    margin:0 auto 22px;
    line-height:1.5;
  }

  .main-title{
    font-family:'Cormorant Garamond',serif;
    font-weight:600;
    font-size:80pt;
    line-height:0.85;
    letter-spacing:2px;
    background:linear-gradient(135deg,#ffffff 0%,#cfd2da 30%,#8f939e 55%,#e9ebef 75%,#ffffff 100%);
    background-size:250% 250%;
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
    animation:shine-text 6s ease-in-out infinite;
    filter:drop-shadow(0 0 22px rgba(255,255,255,0.18));
  }
  @keyframes shine-text{
    0%,100%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
  }

  .subtitle{
    font-size:10.5pt;
    text-transform:uppercase;
    letter-spacing:6px;
    color:var(--silver-dim);
    font-weight:600;
    margin-top:8px;
  }

  .divider{
    width:60px;
    height:1px;
    background:linear-gradient(90deg,transparent,var(--silver-2),transparent);
    margin:26px auto;
  }

  /* ---------- Cuenta regresiva ---------- */
  .countdown-container{
    margin:30px 0 36px;
    background:linear-gradient(180deg,rgba(255,255,255,0.05),rgba(255,255,255,0.01));
    border:1px solid var(--card-border);
    border-radius:18px;
    padding:24px 12px;
    position:relative;
    z-index:3;
    backdrop-filter:blur(6px);
  }
  .countdown-title{
    font-size:8.5pt;
    text-transform:uppercase;
    letter-spacing:3px;
    color:var(--silver-dim);
    margin-bottom:16px;
    text-align:center;
  }
  .timer{display:flex;justify-content:space-around;}
  .time-block{display:flex;flex-direction:column;align-items:center;width:23%;}
  .time-number{
    font-family:'Cormorant Garamond',serif;
    font-size:30pt;
    font-weight:600;
    color:var(--silver);
    text-shadow:0 0 14px rgba(255,255,255,0.35);
    line-height:1;
  }
  .time-label{
    font-size:7.5pt;
    text-transform:uppercase;
    letter-spacing:1.5px;
    color:var(--silver-dim);
    margin-top:6px;
  }
  .time-sep{
    font-family:'Cormorant Garamond',serif;
    font-size:22pt;
    color:var(--silver-dim);
    align-self:flex-start;
    margin-top:2px;
  }

  /* ---------- Tarjetas de info ---------- */
  .info-section{position:relative;z-index:3;}
  .info-card{
    background:var(--card);
    border:1px solid var(--card-border);
    border-radius:16px;
    padding:26px 22px;
    margin-bottom:20px;
    text-align:center;
    backdrop-filter:blur(6px);
    transition:transform .3s ease, border-color .3s ease;
  }
  .info-card:hover{transform:translateY(-3px);border-color:rgba(255,255,255,0.3);}

  .icon-row{
    font-size:20pt;
    margin-bottom:12px;
    letter-spacing:6px;
  }

  .info-card h3{
    font-family:'Cormorant Garamond',serif;
    font-size:19pt;
    font-weight:600;
    color:var(--silver);
    margin-bottom:12px;
    letter-spacing:1px;
  }
  .info-card p{
    font-size:10.5pt;
    color:var(--silver-2);
    line-height:1.7;
  }
  .highlight{color:var(--silver);font-weight:600;}

  .btn{
    display:inline-block;
    width:100%;
    padding:14px;
    margin-top:16px;
    border-radius:30px;
    border:none;
    font-family:'Montserrat',sans-serif;
    font-size:9.5pt;
    font-weight:600;
    text-transform:uppercase;
    letter-spacing:2px;
    cursor:pointer;
    text-decoration:none;
    transition:all .3s ease;
  }
  .btn-primary{
    background:linear-gradient(135deg,#e8e9ec 0%,#9a9dab 100%);
    color:#0a0a0a;
    box-shadow:0 4px 18px rgba(255,255,255,0.15);
  }
  .btn-primary:hover{box-shadow:0 6px 24px rgba(255,255,255,0.3);transform:translateY(-1px);}
  .btn-outline{
    background:transparent;
    color:var(--silver);
    border:1px solid rgba(255,255,255,0.35);
  }
  .btn-outline:hover{background:rgba(255,255,255,0.08);}

  .alias-box{
    background:rgba(255,255,255,0.04);
    border:1px dashed rgba(255,255,255,0.35);
    padding:13px;
    border-radius:10px;
    font-size:12.5pt;
    font-weight:600;
    letter-spacing:1px;
    color:var(--silver);
    margin:16px 0 0;
    display:flex;
    justify-content:center;
    align-items:center;
    gap:10px;
  }

  .map-tap{
    margin-top:16px;
    display:flex;
    align-items:center;
    gap:14px;
    background:rgba(255,255,255,0.04);
    border:1px solid var(--card-border);
    border-radius:14px;
    padding:16px 18px;
    text-decoration:none;
    transition:background .3s ease, transform .3s ease;
  }
  .map-tap:hover{background:rgba(255,255,255,0.08);transform:translateY(-2px);}
  .map-tap-icon{font-size:20pt;line-height:1;}
  .map-tap-text{flex:1;text-align:left;}
  .map-tap-title{display:block;font-family:'Cormorant Garamond',serif;font-size:14.5pt;font-weight:600;color:var(--silver);}
  .map-tap-sub{display:block;font-size:9pt;color:var(--silver-dim);margin-top:2px;letter-spacing:0.5px;}
  .map-tap-arrow{font-size:18pt;color:var(--silver-dim);}

  .toast{
    position:fixed;
    bottom:30px;
    left:50%;
    transform:translateX(-50%) translateY(100px);
    background:var(--silver);
    color:#0a0a0a;
    padding:11px 26px;
    border-radius:20px;
    font-size:10pt;
    font-weight:600;
    box-shadow:0 8px 20px rgba(0,0,0,0.5);
    transition:transform .4s cubic-bezier(.175,.885,.32,1.275), opacity .4s;
    opacity:0;
    z-index:999;
  }
  .toast.show{transform:translateX(-50%) translateY(0);opacity:1;}

  footer{
    margin-top:28px;
    text-align:center;
    font-size:9pt;
    color:var(--silver-dim);
    letter-spacing:2px;
    position:relative;
    z-index:3;
  }
  footer span{display:block;font-family:'Cormorant Garamond',serif;font-size:16pt;font-style:italic;color:var(--silver-2);margin-bottom:6px;letter-spacing:0.5px;}

  @media (max-width:380px){
    .main-title{font-size:62pt;}
  }
</style>
</head>
<body>

<div class="bg-disco bg-disco--1"></div>
<div class="bg-disco bg-disco--2"></div>

<canvas id="glitter-canvas"></canvas>

<div class="stage">
  <img class="frame-deco" src="frame.png" alt="">

  <header>
    <p class="eyebrow">Hay noches que brillan por sí solas,<br>pero compartirla con ustedes la hará inolvidable.</p>
    <h1 class="main-title">AGUS</h1>
    <p class="subtitle">Mis Quince Años</p>
    <div class="divider"></div>
  </header>

  <div class="countdown-container">
    <p class="countdown-title">Faltan para la gran noche</p>
    <div class="timer">
      <div class="time-block"><span class="time-number" id="days">00</span><span class="time-label">Días</span></div>
      <div class="time-block"><span class="time-number" id="hours">00</span><span class="time-label">Hs</span></div>
      <div class="time-block"><span class="time-number" id="minutes">00</span><span class="time-label">Min</span></div>
      <div class="time-block"><span class="time-number" id="seconds">00</span><span class="time-label">Seg</span></div>
    </div>
  </div>

  <div class="info-section">

    <div class="info-card">
      <div class="icon-row">🪩</div>
      <h3>Cuándo y Dónde</h3>
      <p><span class="highlight">Fecha:</span> Sábado, 17 de Octubre</p>
      <p><span class="highlight">Hora:</span> 21:00 hs</p>
      <p><span class="highlight">Lugar:</span> Salón La Bodega</p>
      <a href="https://maps.app.goo.gl/y8UZKLg9iahFu7wT7?g_st=ic" target="_blank" class="map-tap">
        <span class="map-tap-icon">📍</span>
        <span class="map-tap-text">
          <span class="map-tap-title">Ver ubicación</span>
          <span class="map-tap-sub">Abrir en Google Maps</span>
        </span>
        <span class="map-tap-arrow">›</span>
      </a>
      <a href="https://maps.app.goo.gl/y8UZKLg9iahFu7wT7?g_st=ic" target="_blank" class="btn btn-primary">Cómo llegar</a>
    </div>

    <div class="info-card">
      <div class="icon-row">🥂</div>
      <h3>Dress Code</h3>
      <p class="highlight" style="font-size:14pt;letter-spacing:2px;">ELEGANTE</p>
      <p>Preparate para brillar en esta gran noche con tu mejor look.</p>
    </div>

    <div class="info-card">
      <div class="icon-row">🎁</div>
      <h3>Mesa de Regalos</h3>
      <p>Tu presencia es mi mayor regalo. Si de todas formas deseás hacerme un presente, podés transferir al siguiente alias:</p>
      <div class="alias-box" id="alias-text">agus.mica.15</div>
      <button onclick="copyAlias()" class="btn btn-outline">Copiar Alias</button>
    </div>

    <div class="info-card" style="background:linear-gradient(180deg,rgba(255,255,255,0.05),rgba(255,255,255,0.01));">
      <div class="icon-row">💌</div>
      <h3>Confirmación</h3>
      <p>Por favor, confirmá tu asistencia para organizar cada detalle a la perfección.</p>
      <a href="https://wa.me/5492625452505?text=%C2%A1Hola!%20Confirmo%20mi%20asistencia%20al%20cumple%20de%20Agus%20%E2%9C%A8" target="_blank" class="btn btn-primary">Confirmar por WhatsApp</a>
    </div>

  </div>

  <footer>
    <span>¡Te espero para brillar juntas!</span>
    Agus · 15 años
  </footer>
</div>

<div class="toast" id="copy-toast">¡Alias copiado al portapapeles! ✨</div>

<script>
  /* ---------- Cuenta regresiva ---------- */
  const targetDate = new Date('October 17, 2026 21:00:00').getTime();
  function updateCountdown(){
    const now = new Date().getTime();
    const diff = targetDate - now;
    if(diff <= 0){
      ['days','hours','minutes','seconds'].forEach(id=>document.getElementById(id).innerText='00');
      return;
    }
    const d = Math.floor(diff/(1000*60*60*24));
    const h = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
    const m = Math.floor((diff%(1000*60*60))/(1000*60));
    const s = Math.floor((diff%(1000*60))/1000);
    document.getElementById('days').innerText = String(d).padStart(2,'0');
    document.getElementById('hours').innerText = String(h).padStart(2,'0');
    document.getElementById('minutes').innerText = String(m).padStart(2,'0');
    document.getElementById('seconds').innerText = String(s).padStart(2,'0');
  }
  setInterval(updateCountdown,1000);
  updateCountdown();

  /* ---------- Copiar alias ---------- */
  function copyAlias(){
    navigator.clipboard.writeText("agus.mica.15").then(()=>{
      const toast = document.getElementById('copy-toast');
      toast.classList.add('show');
      setTimeout(()=>toast.classList.remove('show'),2500);
    }).catch(err=>console.error('Error al copiar: ', err));
  }

  /* ---------- Brillos animados de fondo (canvas) ---------- */
  const canvas = document.getElementById('glitter-canvas');
  const ctx = canvas.getContext('2d');
  let W, H, particles;

  function resize(){
    W = canvas.width = window.innerWidth;
    H = canvas.height = document.documentElement.scrollHeight;
  }

  let flares;

  function makeParticles(){
    const count = Math.floor((W*H)/3200); // mucho más densidad de brillos
    particles = Array.from({length: count}, () => ({
      x: Math.random()*W,
      y: Math.random()*H,
      size: Math.random()*3.2 + 1.6,
      rot: Math.random()*Math.PI*2,
      rotSpeed: (Math.random()-0.5)*0.01,
      baseAlpha: Math.random()*0.75 + 0.25,
      speed: Math.random()*0.35 + 0.05,
      drift: (Math.random()-0.5)*0.25,
      twinkleSpeed: Math.random()*0.011 + 0.0025,
      phase: Math.random()*Math.PI*2
    }));

    // estrellitas más grandes, ocasionales, con destello más notorio
    const flareCount = Math.max(6, Math.floor((W*H)/160000));
    flares = Array.from({length: flareCount}, () => ({
      x: Math.random()*W,
      y: Math.random()*H,
      size: Math.random()*9 + 7,
      rot: Math.random()*Math.PI*2,
      rotSpeed: (Math.random()-0.5)*0.006,
      speed: Math.random()*0.12 + 0.03,
      drift: (Math.random()-0.5)*0.1,
      twinkleSpeed: Math.random()*0.005 + 0.0018,
      phase: Math.random()*Math.PI*2
    }));
  }

  function drawSparkleStar(x, y, size, alpha, rot){
    ctx.save();
    ctx.translate(x, y);
    ctx.rotate(rot);
    ctx.globalAlpha = alpha;
    ctx.fillStyle = '#ffffff';
    ctx.shadowColor = 'rgba(255,255,255,0.95)';
    ctx.shadowBlur = size * 2.2;
    ctx.beginPath();
    ctx.moveTo(0, -size);
    ctx.bezierCurveTo(size*0.18, -size*0.18, size*0.18, -size*0.18, size, 0);
    ctx.bezierCurveTo(size*0.18, size*0.18, size*0.18, size*0.18, 0, size);
    ctx.bezierCurveTo(-size*0.18, size*0.18, -size*0.18, size*0.18, -size, 0);
    ctx.bezierCurveTo(-size*0.18, -size*0.18, -size*0.18, -size*0.18, 0, -size);
    ctx.closePath();
    ctx.fill();
    ctx.restore();
  }

  function draw(t){
    ctx.clearRect(0,0,W,H);

    for(const p of particles){
      const alpha = p.baseAlpha * (0.5 + 0.5*Math.sin(t*p.twinkleSpeed + p.phase));
      p.rot += p.rotSpeed;
      drawSparkleStar(p.x, p.y, p.size, alpha, p.rot);

      p.y -= p.speed;
      p.x += p.drift;
      if(p.y < -5){ p.y = H+5; p.x = Math.random()*W; }
      if(p.x < -5) p.x = W+5;
      if(p.x > W+5) p.x = -5;
    }

    for(const f of flares){
      const alpha = 0.2 + 0.7 * Math.max(0, Math.sin(t*f.twinkleSpeed + f.phase));
      f.rot += f.rotSpeed;
      if(alpha > 0.06) drawSparkleStar(f.x, f.y, f.size, alpha, f.rot);

      f.y -= f.speed;
      f.x += f.drift;
      if(f.y < -20){ f.y = H+20; f.x = Math.random()*W; }
      if(f.x < -20) f.x = W+20;
      if(f.x > W+20) f.x = -20;
    }

    requestAnimationFrame(draw);
  }

  function init(){
    resize();
    makeParticles();
  }
  window.addEventListener('resize', () => { resize(); makeParticles(); });
  window.addEventListener('load', () => { resize(); makeParticles(); });
  init();
  requestAnimationFrame(draw);
</script>
</body>
</html>
