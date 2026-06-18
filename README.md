<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Agro Forte - Solo e Água</title>

<style>
/* =========================
   FUNDO GERAL ANIMADO
========================= */
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(to bottom, #0b3d2e, #145a32, #1e8449);
    overflow: hidden;
    color: white;
}

h1 {
    text-align: center;
    font-size: 40px;
    margin-top: 20px;
    color: #a3ffb0;
    text-shadow: 2px 2px 10px black;
}

.subtitle {
    text-align: center;
    font-size: 18px;
    margin-bottom: 10px;
    color: #d1f7c4;
}

/* =========================
   SOLO
========================= */
#soil {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 120px;
    background: linear-gradient(to top, #5d4037, #8d6e63);
    box-shadow: inset 0 10px 20px rgba(0,0,0,0.5);
}

/* =========================
   PLANTAS
========================= */
.plant {
    position: absolute;
    bottom: 100px;
    width: 6px;
    height: 0px;
    background: #00ff88;
    border-radius: 10px;
    animation: grow 6s infinite;
}

@keyframes grow {
    0% { height: 0px; }
    50% { height: 80px; }
    100% { height: 0px; }
}

/* =========================
   GOTAS DE ÁGUA
========================= */
.drop {
    position: absolute;
    top: -20px;
    width: 3px;
    height: 15px;
    background: #00e5ff;
    animation: fall linear infinite;
    border-radius: 50%;
}

@keyframes fall {
    to {
        transform: translateY(100vh);
        opacity: 0;
    }
}

/* =========================
   NUVENS
========================= */
.cloud {
    position: absolute;
    top: 50px;
    width: 120px;
    height: 60px;
    background: rgba(255,255,255,0.8);
    border-radius: 100px;
    animation: moveClouds 20s linear infinite;
}

@keyframes moveClouds {
    from { left: -200px; }
    to { left: 110%; }
}

/* =========================
   TEXTO INFORMATIVO
========================= */
.info {
    position: absolute;
    top: 120px;
    width: 100%;
    text-align: center;
    font-size: 16px;
    color: #eaffea;
}
</style>
</head>

<body>

<h1>🌱 Agro Forte e Futuro Sustentável 💧</h1>
<div class="subtitle">Solo saudável + Água limpa = Vida abundante</div>

<div class="info">
Preservar o solo e a água é garantir o futuro da agricultura e do planeta.
</div>

<div id="soil"></div>

<script>
// =========================
// CRIA PLANTAS
// =========================
for (let i = 0; i < 25; i++) {
    let plant = document.createElement("div");
    plant.className = "plant";
    plant.style.left = (Math.random() * window.innerWidth) + "px";
    plant.style.animationDelay = (Math.random() * 5) + "s";
    document.body.appendChild(plant);
}

// =========================
// CRIA GOTAS DE ÁGUA
// =========================
for (let i = 0; i < 80; i++) {
    let drop = document.createElement("div");
    drop.className = "drop";
    drop.style.left = (Math.random() * window.innerWidth) + "px";
    drop.style.animationDuration = (1 + Math.random() * 3) + "s";
    drop.style.animationDelay = (Math.random() * 5) + "s";
    document.body.appendChild(drop);
}

// =========================
// CRIA NUVENS
// =========================
for (let i = 0; i < 5; i++) {
    let cloud = document.createElement("div");
    cloud.className = "cloud";
    cloud.style.top = (Math.random() * 100) + "px";
    cloud.style.animationDuration = (15 + Math.random() * 20) + "s";
    cloud.style.opacity = 0.5 + Math.random() * 0.5;
    document.body.appendChild(cloud);
}
</script>

</body>
</html>