# robo-server
Salom siz buyerda robo serveri haqida malumot olasiz
<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#080b18">
<title>ROBO SERVER | Minecraft</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#080b18;color:#f4f7ff;font-family:Arial,sans-serif}
header,main,footer{width:min(950px,92%);margin:auto}
header{padding:22px 0;border-bottom:1px solid #28334c;display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap}
.logo{font-weight:900;letter-spacing:2px;color:#00f5ff}
nav{display:flex;gap:15px;flex-wrap:wrap}
a{color:#b6c4dc;text-decoration:none}
a:hover{color:#00f5ff}
.hero{text-align:center;padding:75px 0 55px}
h1{font-size:clamp(40px,9vw,76px);margin:18px 0;text-shadow:0 0 25px #00f5ff66}
h1 span{color:#00f5ff}
p{line-height:1.8;color:#a7b1cc}
.tag{color:#d8b4fe;border:1px solid #a855f7;padding:8px 12px;border-radius:30px;font-size:12px}
.btn{display:inline-block;padding:13px 18px;border:1px solid #00f5ff;border-radius:9px;color:#00f5ff;background:#00f5ff12;margin:6px;cursor:pointer}
.primary{background:#00f5ff;color:#08101a;font-weight:bold}
section{padding:25px 0 40px}
h2{text-align:center}
.card{padding:23px;border:1px solid #34405f;border-radius:15px;background:#10172b;margin:12px 0}
.center{text-align:center}
.status{color:#ffd166;border:1px solid #ffd16666;padding:7px 12px;border-radius:20px;font-size:13px}
.ip{font-family:monospace;color:#00f5ff;overflow-wrap:anywhere;background:#080b18;padding:15px;border-radius:8px}
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px}
footer{text-align:center;border-top:1px solid #28334c;padding:20px 0;font-size:12px}
@media(max-width:600px){.grid{grid-template-columns:1fr}.hero{padding:50px 0 30px}nav{font-size:13px}.btn{max-width:100%}}
</style>
</head>
<body>
<header>
<a class="logo" href="#home">◆ ROBO SERVER</a>
<nav>
<a href="#home">Bosh sahifa</a>
<a href="#server">Server</a>
<a href="#modes">Rejimlar</a>
</nav>
</header>
<main>
<section class="hero" id="home">
<span class="tag">MINECRAFT JAVA EDITION</span>
<h1>ROBO <span>SERVER</span></h1>
<p>Yangi sarguzashtlar, do‘stlar va cheksiz imkoniyatlar olamiga xush kelibsiz!</p>
<a class="btn primary" href="#server">SERVER MA'LUMOTI</a>
<a class="btn" href="#modes">REJIMLARNI KO‘RISH</a>
</section>
<section id="server">
<h2>Server ma'lumotlari</h2>
<div class="card center">
<span class="status">● Tekshirilmagan</span>
<h3>Minecraft Java 1.17</h3>
<p>Server manzili:</p>
<div class="ip" id="ip">IP_HALI_SOZLANMAGAN</div>
<button class="btn" id="copy">IP ni nusxalash</button>
<p id="msg">Haqiqiy IP hali kiritilmagan. Server holati tekshirilmagan.</p>
</div>
</section>
<section id="modes">
<h2>O‘yin rejimlari</h2>
<div class="grid">
<div class="card"><h3>⛏ Survival</h3><p>Resurs yig‘ing va o‘z dunyongizni quring.</p></div>
<div class="card"><h3>☁ SkyWars</h3><p>Osmondagi orollarda mahoratingizni sinang.</p></div>
<div class="card"><h3>🏰 Creative</h3><p>O‘z ijodingiz bilan ajoyib binolar yarating.</p></div>
</div>
<p class="center">Bu rejimlar namuna, serverda mavjudligi tasdiqlanmagan.</p>
</section>
</main>
<footer>© <span id="year"></span> ROBO SERVER · Minecraft Java</footer>
<script>
const SERVER_IP="IP_HALI_SOZLANMAGAN";
document.getElementById("year").textContent=new Date().getFullYear();
document.getElementById("ip").textContent=SERVER_IP;
document.getElementById("copy").onclick=async()=>{
const msg=document.getElementById("msg");
if(SERVER_IP==="IP_HALI_SOZLANMAGAN"){msg.textContent="Avval haqiqiy server IP kiriting.";return;}
try{await navigator.clipboard.writeText(SERVER_IP);msg.textContent="IP nusxalandi!";}
catch(e){msg.textContent="IP manzilini qo‘lda nusxalang: "+SERVER_IP;}
};
</script>
</body>
</html>

