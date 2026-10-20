
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#070014">
<title>GALAXY NEON • 20/10</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800;900&family=Quicksand:wght@400;500;600;700;800&display=swap');

:root {
  --pink:#ff36c7;
  --blue:#34eaff;
  --purple:#a855ff;
  --gold:#ffe89a;
  --white:#fff8ff;
}
* {box-sizing:border-box;margin:0;padding:0}
html {scroll-behavior:smooth}
body {
  min-height:100vh;
  min-height:100dvh;
  overflow-x:hidden;
  background:#070014;
  color:white;
  font-family:'Quicksand',Arial,sans-serif;
}
button {font:inherit;cursor:pointer;touch-action:manipulation}
button:focus-visible {outline:2px solid white;outline-offset:4px}

/* VŨ TRỤ ĐỘNG */
#space {
  position:fixed;inset:0;width:100%;height:100%;
  z-index:0;pointer-events:none;
}
.nebula {
  position:fixed;z-index:0;pointer-events:none;
  width:65vw;height:65vw;max-width:650px;max-height:650px;
  border-radius:50%;filter:blur(85px);opacity:.25;
  animation:nebulaMove 12s ease-in-out infinite alternate;
}
.n1 {background:#9b00ff;top:-20%;left:-25%}
.n2 {background:#ff008c;right:-30%;top:25%;animation-delay:-5s}
.n3 {background:#004fff;left:20%;bottom:-45%;animation-delay:-8s}
@keyframes nebulaMove {
  0% {transform:translate(0,0) scale(.9)}
  50% {transform:translate(9vw,7vh) scale(1.2)}
  100% {transform:translate(-5vw,-4vh) scale(1.05)}
}
.scanlines {
  position:fixed;inset:0;z-index:1;pointer-events:none;opacity:.12;
  background:repeating-linear-gradient(
    0deg,transparent 0px,transparent 3px,#a78bfa 4px
  );
}
#particles {
  position:fixed;inset:0;z-index:2;pointer-events:none;overflow:hidden;
}
.float {
  position:absolute;bottom:-50px;
  animation:floatUp linear forwards;
  filter:drop-shadow(0 0 10px #ff36c7);
}
@keyframes floatUp {
  0% {transform:translate(0,0) rotate(0) scale(.6);opacity:0}
  12% {opacity:1}
  85% {opacity:.8}
  100% {transform:translate(var(--drift),-115vh) rotate(360deg) scale(1.3);opacity:0}
}
.shooting {
  position:fixed;width:130px;height:2px;z-index:2;pointer-events:none;
  background:linear-gradient(90deg,transparent,#fff,#34eaff,transparent);
  filter:drop-shadow(0 0 7px #34eaff);
  transform:rotate(-28deg);
  animation:shoot 1s ease-out forwards;
}
@keyframes shoot {
  from {opacity:0;transform:translate(0,0) rotate(-28deg)}
  15% {opacity:1}
  to {opacity:0;transform:translate(-220px,180px) rotate(-28deg)}
}

/* BỐ CỤC */
.app {
  position:relative;z-index:3;
  width:min(100%,760px);min-height:100vh;min-height:100dvh;
  margin:auto;padding:22px 18px 30px;
  display:flex;flex-direction:column;
}
.header {
  display:flex;align-items:center;justify-content:space-between;
  gap:12px;margin-bottom:32px;
}
.brand {
  font-family:'Orbitron',sans-serif;font-size:11px;font-weight:900;
  letter-spacing:2px;color:var(--blue);
  text-shadow:0 0 8px var(--blue),0 0 25px var(--blue);
}
.status {
  border:1px solid #ff36c766;background:#ff36c711;
  border-radius:30px;padding:8px 11px;
  color:#ffc7f0;font-size:10px;letter-spacing:1px;
  box-shadow:0 0 18px #ff36c71c;
}
.status i {
  display:inline-block;width:6px;height:6px;border-radius:50%;
  background:#54ffb0;margin-right:5px;
  box-shadow:0 0 10px #54ffb0;
  animation:blink 1s infinite alternate;
}
@keyframes blink {to{opacity:.25}}

.progress-wrap {margin-bottom:28px}
.progress-info {
  display:flex;justify-content:space-between;align-items:center;
  color:#a8a0d2;font-size:10px;letter-spacing:2px;margin-bottom:9px;
}
.progress-track {
  width:100%;height:4px;border-radius:20px;
  background:#ffffff12;overflow:hidden;
}
#progressBar {
  width:20%;height:100%;border-radius:20px;
  background:linear-gradient(90deg,var(--pink),var(--purple),var(--blue));
  box-shadow:0 0 15px var(--pink);
  transition:width .7s cubic-bezier(.2,.8,.2,1);
}
.page {
  width:100%;
  animation:pageEnter .65s cubic-bezier(.2,.8,.2,1) both;
}
.page.hidden {display:none}
@keyframes pageEnter {
  from {opacity:0;transform:translateY(25px) scale(.97);filter:blur(5px)}
  to {opacity:1;transform:translateY(0) scale(1);filter:blur(0)}
}
.kicker {
  font-family:'Orbitron',sans-serif;text-align:center;
  font-size:10px;letter-spacing:3px;color:var(--blue);
  margin-bottom:15px;text-shadow:0 0 15px var(--blue);
}
h1 {
  font-family:'Orbitron',sans-serif;text-align:center;
  font-size:clamp(29px,8vw,56px);font-weight:900;
  line-height:1.22;letter-spacing:-1.5px;
  color:white;
  text-shadow:0 0 8px #fff,0 0 24px #ff36c7,0 0 55px #a855ff;
}
.gradient-text {
  background:linear-gradient(100deg,#fff 5%,#ff7bdf 35%,#8ef5ff 70%,#fff);
  background-size:250% auto;
  color:transparent;background-clip:text;-webkit-background-clip:text;
  animation:textFlow 4s linear infinite;
}
@keyframes textFlow {to{background-position:250% center}}
.subtitle {
  max-width:490px;margin:17px auto 25px;
  text-align:center;color:#c5bce9;font-size:14px;line-height:1.9;
}

/* HÀNH TINH 3D */
.planet-area {
  height:205px;display:grid;place-items:center;
  position:relative;margin:0 auto 10px;
}
.planet {
  position:relative;width:112px;height:112px;border-radius:50%;
  display:grid;place-items:center;font-size:46px;
  background:
    radial-gradient(circle at 28% 22%,#fff 0%,#ffc8f3 5%,transparent 19%),
    radial-gradient(circle at 35% 30%,#ff74d8,#8d32ff 45%,#180b65 80%);
  box-shadow:inset -20px -15px 28px #050014,
    0 0 25px #ff36c7,0 0 65px #a855ff,0 0 110px #7c3aed55;
  animation:planetFloat 4s ease-in-out infinite;
}
.planet:before {
  content:"";position:absolute;width:165px;height:43px;
  border:4px solid #ffffffcc;border-left-color:#34eaff;
  border-right-color:#ff36c7;border-radius:50%;
  transform:rotate(-24deg);
  box-shadow:0 0 15px #34eaff77,inset 0 0 10px #ff36c744;
}
.planet:after {
  content:"";position:absolute;width:185px;height:185px;
  border:1px dashed #dca5ff55;border-radius:50%;
  animation:orbit 18s linear infinite;
}
.orbit-dot {
  position:absolute;width:12px;height:12px;border-radius:50%;
  background:#34eaff;box-shadow:0 0 15px #34eaff;
  top:17px;right:calc(50% - 80px);
}
@keyframes planetFloat {
  0%,100% {transform:translateY(0) rotate(-3deg)}
  50% {transform:translateY(-10px) rotate(4deg)}
}
@keyframes orbit {to{transform:rotate(360deg)}}

/* BẢNG HOLOGRAM */
.panel {
  position:relative;width:100%;padding:23px 19px;
  border-radius:22px;overflow:hidden;
  background:linear-gradient(135deg,#ffffff12,#b35cff0b,#20eaff09);
  backdrop-filter:blur(17px);-webkit-backdrop-filter:blur(17px);
  border:1px solid transparent;
  background-clip:padding-box;
  box-shadow:0 0 25px #9b5cff15,0 18px 60px #0007,
  inset 0 0 25px #ffffff05;
}
.panel:before {
  content:"";position:absolute;inset:0;border-radius:22px;
  padding:1px;
  background:linear-gradient(120deg,#ff36c7,#34eaff,#a855ff,#ff36c7);
  background-size:300% 300%;
  animation:borderFlow 5s linear infinite;
  -webkit-mask:linear-gradient(#fff 0 0) content-box,linear-gradient(#fff 0 0);
  -webkit-mask-composite:xor;mask-composite:exclude;
  pointer-events:none;
}
@keyframes borderFlow {to{background-position:300% 0}}
.panel h2 {font-family:'Orbitron',sans-serif;font-size:15px;color:#ffe3fa;margin-bottom:12px}
.panel p {color:#d2c8ec;font-size:13px;line-height:1.9}
.panel-content {position:relative;z-index:1}
.neon-line {
  height:1px;margin:16px 0;
  background:linear-gradient(90deg,transparent,#ff36c7,#34eaff,transparent);
  box-shadow:0 0 10px #ff36c7;
}

/* NÚT */
.btn {
  position:relative;overflow:hidden;
  width:100%;min-height:49px;margin-top:13px;padding:13px 15px;
  border:1px solid #ffffff25;border-radius:13px;
  background:#ffffff09;color:white;
  font-size:12px;font-weight:800;letter-spacing:.6px;
  transition:transform .2s,box-shadow .25s,border-color .25s;
}
.btn:before {
  content:"";position:absolute;top:-50%;left:-100%;
  width:50%;height:200%;transform:rotate(25deg);
  background:linear-gradient(90deg,transparent,#ffffff55,transparent);
  transition:left .6s;
}
.btn:active {transform:scale(.96)}
.btn:active:before {left:150%}
.btn-main {
  color:#170627;border:0;
  background:linear-gradient(100deg,#ff7cde,#c8a4ff,#8af5ff);
  background-size:200% auto;
  box-shadow:0 0 18px #ff36c744,0 0 35px #a855ff20;
  animation:buttonGlow 3s ease-in-out infinite alternate;
}
@keyframes buttonGlow {
  to {background-position:100% center;box-shadow:0 0 25px #34eaff66,0 0 40px #ff36c733}
}
.btn-ghost {border-color:#a855ff66;color:#f1dfff}
.btn-small {width:auto;min-width:110px}

/* THẺ LỜI CHÚC */
.menu {
  display:grid;grid-template-columns:1fr 1fr;gap:11px;margin-top:17px;
}
.tile {
  position:relative;min-height:120px;padding:15px 12px;
  border:1px solid #a855ff50;border-radius:17px;
  color:white;text-align:left;
  background:linear-gradient(145deg,#8c3dff22,#ff36c70a,#34eaff08);
  transition:transform .25s,border-color .25s,box-shadow .25s;
}
.tile:active {transform:scale(.95)}
.tile:hover {border-color:#ff7cde;box-shadow:0 0 22px #ff36c722}
.tile .emoji {font-size:29px;display:block;margin-bottom:10px;filter:drop-shadow(0 0 8px #ff36c7)}
.tile strong {display:block;font-size:12px;margin-bottom:5px}
.tile small {display:block;color:#bcb1de;font-size:10px;line-height:1.6}
.message {
  margin-top:15px;padding:17px;border-radius:15px;
  border:1px solid #ff76d855;background:#ff36c70c;
  color:#ffe5f8;font-size:13px;line-height:1.9;text-align:center;
  box-shadow:inset 0 0 20px #ff36c709,0 0 18px #ff36c70b;
  animation:pageEnter .4s ease both;
}
.hidden {display:none!important}
.big-icon {font-size:58px;text-align:center;margin:8px 0 15px;filter:drop-shadow(0 0 16px #ff36c7)}
.choice-grid {display:grid;grid-template-columns:repeat(3,1fr);gap:9px;margin-top:17px}
.star-choice {
  min-height:100px;border:1px solid #a855ff66;border-radius:15px;
  color:white;background:linear-gradient(160deg,#a855ff22,#34eaff08);
  font-size:12px;font-weight:800;transition:.25s;
}
.star-choice span {display:block;font-size:29px;margin-bottom:9px}
.star-choice:active {transform:scale(.92)}
.star-choice:disabled {opacity:.4}
.letter {
  min-height:135px;display:flex;align-items:center;justify-content:center;
  text-align:center;padding:18px;line-height:1.9;font-size:13px;color:#ffe5f8;
  border:1px dashed #ff76d877;border-radius:15px;
  background:radial-gradient(ellipse at center,#ff36c714,transparent 75%);
}
.footer {
  margin-top:auto;padding-top:35px;text-align:center;
  color:#9485b8;font-family:'Orbitron',sans-serif;
  font-size:9px;letter-spacing:2px;line-height:2;
}
.footer span {color:#ff76d8}

/* PHÁO HOA VÀ POPUP */
.confetti {
  position:fixed;z-index:30;top:-25px;pointer-events:none;
  animation:confettiFall linear forwards;
}
@keyframes confettiFall {
  to {transform:translate3d(var(--x),110vh,0) rotate(900deg);opacity:0}
}
#toast {
  position:fixed;left:50%;bottom:25px;z-index:50;
  transform:translate(-50%,30px);opacity:0;pointer-events:none;
  width:max-content;max-width:90vw;text-align:center;
  padding:13px 18px;border:1px solid #ff76d888;border-radius:30px;
  color:white;background:#17072beF;box-shadow:0 0 25px #ff36c744;
  font-size:12px;transition:.35s;
}
#toast.show {opacity:1;transform:translate(-50%,0)}
@media(min-width:600px) {
  .app {padding:30px 28px}
  .panel {padding:28px}
  .planet-area {height:225px}
}
@media(prefers-reduced-motion:reduce) {
  *,*:before,*:after {animation-duration:.01ms!important;animation-iteration-count:1!important;scroll-behavior:auto!important}
}
</style>
</head>

<body>
<canvas id="space"></canvas>
<div class="nebula n1"></div>
<div class="nebula n2"></div>
<div class="nebula n3"></div>
<div class="scanlines"></div>
<div id="particles"></div>
<div id="toast" role="status"></div>

<main class="app">
<header class="header">
  <div class="brand">✦ GALAXY 20/10 DESBY CÔNG ĐẶNG </div>
  <div class="status"><i>hihi</i></div>
</header>

<div class="progress-wrap">
  <div class="progress-info">
    <span>have a nice day:3</span><span id="stageText">STAGE 01 / 05</span>
  </div>
  <div class="progress-track"><div id="progressBar"></div></div>
</div>

<!-- STAGE 1 -->
<section class="page" id="page1">
  <div class="planet-area">
    <div class="planet">💖</div><div class="orbit-dot"></div>
  </div>
  <div class="kicker">✧ A SPECIAL UNIVERSE ✧</div>
  <h1 class="gradient-text">HAPPY<br>20 · 10</h1>
  <p class="subtitle">Một vũ trụ nhỏ, một ngàn vì sao và vô vàn lời chúc dễ thương dành riêng cho ngày đặc biệt này. 🌌</p>

  <div class="panel">
    <div class="panel-content">
      <h2>🌷 CHÀO MỪNG BẠN ĐẾN VŨ TRỤ NEON</h2>
      <div class="neon-line"></div>
      <p>Hôm nay, mọi ánh sáng đều dành để tôn vinh những người phụ nữ tuyệt vời. Chúc bạn luôn hạnh phúc, tự tin, được yêu thương và có thật nhiều khoảnh khắc đáng nhớ.</p>
      <button class="btn btn-main" onclick="go(2)">KHỞI ĐỘNG HÀNH TRÌNH ✦</button>
    </div>
  </div>
  <p class="subtitle" style="font-size:10px;letter-spacing:2px;margin-top:18px">SCROLL LESS · FEEL MORE · SHINE BRIGHT</p>
</section>

<!-- STAGE 2 -->
<section class="page hidden" id="page2">
  <div class="kicker">STAGE 02 · WISH GENERATOR</div>
  <h1 class="gradient-text">VŨ TRỤ<br>LỜI CHÚC</h1>
  <p class="subtitle">Chọn một cánh cổng ánh sáng để mở khóa thông điệp bí mật. Mỗi lựa chọn là một điều tốt đẹp gửi đến bạn. 💫</p>

  <div class="menu">
    <button class="tile" onclick="wish(0)"><span class="emoji">🌸</span><strong>NGỌT NGÀO</strong><small>Chạm để nhận một lời chúc dịu dàng</small></button>
    <button class="tile" onclick="wish(1)"><span class="emoji">💎</span><strong>TỎA SÁNG</strong><small>Mở khóa nguồn năng lượng tự tin</small></button>
    <button class="tile" onclick="wish(2)"><span class="emoji">🌙</span><strong>BÌNH YÊN</strong><small>Gửi bạn một chút an nhiên</small></button>
    <button class="tile" onclick="wish(3)"><span class="emoji">🍀</span><strong>MAY MẮN</strong><small>Nạp đầy năng lượng tích cực</small></button>
  </div>
  <div id="wishBox" class="message hidden" aria-live="polite"></div>
  <button class="btn btn-main" onclick="go(3)">MỞ LÁ THƯ BÍ MẬT →</button>
  <button class="btn btn-ghost" onclick="go(1)">← QUAY LẠI</button>
</section>

<!-- STAGE 3 -->
<section class="page hidden" id="page3">
  <div class="kicker">STAGE 03 · ENCRYPTED LOVE</div>
  <div class="big-icon" id="mailIcon">💌</div>
  <h1 class="gradient-text">SECRET<br>MESSAGE</h1>
  <p class="subtitle">Một thông điệp nhỏ đang được mã hóa. Sẵn sàng mở khóa chưa? 🔐</p>

  <div class="panel">
    <div class="panel-content">
      <div class="letter" id="letterText">╭─────── ✦ ───────╮<br><br>MESSAGE LOCKED<br><br>Nhấn nút bên dưới để giải mã<br><br>╰─────── ✦ ───────╯</div>
      <button class="btn btn-main" id="mailBtn" onclick="openMail()">🔓 GIẢI MÃ THÔNG ĐIỆP</button>
      <button class="btn btn-ghost" onclick="go(4)">ĐẾN MINI GAME →</button>
    </div>
  </div>
</section>

<!-- STAGE 4 -->
<section class="page hidden" id="page4">
  <div class="kicker">STAGE 04 · LUCKY PLANET</div>
  <h1 class="gradient-text">CHỌN SAO<br>MAY MẮN</h1>
  <p class="subtitle">Ba hành tinh đang chờ bạn khám phá. Chọn một hành tinh theo trực giác để nhận phần thưởng của riêng mình! 🪐</p>

  <div class="panel">
    <div class="panel-content">
      <div class="choice-grid" id="starChoices">
        <button class="star-choice" onclick="pickStar(0)"><span>🌟</span>PLANET A</button>
        <button class="star-choice" onclick="pickStar(1)"><span>💫</span>PLANET B</button>
        <button class="star-choice" onclick="pickStar(2)"><span>✨</span>PLANET C</button>
      </div>
      <div id="gameResult" class="message" aria-live="polite">🎮 Một lượt chọn đang chờ bạn. Vận may nằm trong tay bạn!</div>
      <button class="btn btn-ghost" onclick="resetGame()">↻ CHƠI LẠI</button>
      <button class="btn btn-main" onclick="go(5)">MỞ KHO BÁU CUỐI CÙNG →</button>
    </div>
  </div>
</section>

<!-- STAGE 5 -->
<section class="page hidden" id="page5">
  <div class="kicker">STAGE 05 · FINAL UNLOCK</div>
  <div class="planet-area"><div class="planet" id="giftIcon">🎁</div></div>
  <h1 class="gradient-text">FINAL<br>GIFT</h1>
  <p class="subtitle">Bạn đã đi đến cuối hành trình. Phần quà đặc biệt đang chờ được mở! 🎀</p>

  <div class="panel">
    <div class="panel-content">
      <h2 style="text-align:center">✧ MÓN QUÀ DÀNH CHO BẠN ✧</h2>
      <div class="neon-line"></div>
      <div class="letter" id="giftText">Một điều tốt đẹp đang chờ phía trước. Mở quà để nhận lời chúc cuối cùng nhé!</div>
      <button class="btn btn-main" id="giftBtn" onclick="openGift()">🎁 UNLOCK THE GIFT</button>
      <button class="btn btn-ghost" onclick="go(1)">↻ TRẢI NGHIỆM LẠI TỪ ĐẦU</button>
    </div>
  </div>
</section>

<footer class="footer">POWERED BY <span>LOVE ✦ LIGHT ✦ GALAXY</span><br>MADE FOR A BEAUTIFUL 20/10</footer>
</main>

<script>
/* ===== CANVAS STARFIELD ===== */
const canvas=document.getElementById('space');
const ctx=canvas.getContext('2d');
let W=0,H=0,dpr=1,stars=[],shootTimer=0;

function resize(){
  dpr=Math.min(devicePixelRatio||1,2);
  W=innerWidth;H=innerHeight;
  canvas.width=W*dpr;canvas.height=H*dpr;
  canvas.style.width=W+'px';canvas.style.height=H+'px';
  ctx.setTransform(dpr,0,0,dpr,0,0);
  stars=Array.from({length:Math.min(240,Math.floor(W*H/2800))},()=>({
    x:Math.random()*W,y:Math.random()*H,
    r:Math.random()*1.5+.25,a:Math.random()*6,
    s:Math.random()*.02+.004,dx:(Math.random()-.5)*.12
  }));
}
function draw(){
  ctx.clearRect(0,0,W,H);
  for(const s of stars){
    s.a+=s.s;s.x+=s.dx;
    if(s.x<0)s.x=W;if(s.x>W)s.x=0;
    const alpha=.25+(Math.sin(s.a)+1)*.35;
    ctx.beginPath();ctx.arc(s.x,s.y,s.r,0,Math.PI*2);
    ctx.fillStyle=`rgba(220,230,255,${alpha})`;ctx.fill();
    if(s.r>1.25){
      ctx.strokeStyle=`rgba(150,220,255,${alpha*.4})`;
      ctx.beginPath();ctx.moveTo(s.x-3,s.y);ctx.lineTo(s.x+3,s.y);ctx.stroke();
    }
  }
  requestAnimationFrame(draw);
}
addEventListener('resize',resize);resize();draw();

/* ===== SHOOTING STARS ===== */
function shootingStar(){
  const el=document.createElement('div');
  el.className='shooting';
  el.style.left=(Math.random()*90+5)+'vw';
  el.style.top=(Math.random()*55+5)+'vh';
  document.body.appendChild(el);
  setTimeout(()=>el.remove(),1200);
}
setInterval(()=>{if(Math.random()>.25)shootingStar()},1900);

/* ===== FLOATING HEARTS AND PETALS ===== */
const particles=document.getElementById('particles');
const symbols=['💖','💗','💕','✨','🌸','💫','🩷','✦'];
function floatParticle(){
  const el=document.createElement('span');
  el.className='float';
  el.textContent=symbols[Math.floor(Math.random()*symbols.length)];
  el.style.left=Math.random()*100+'vw';
  el.style.fontSize=(12+Math.random()*23)+'px';
  el.style.setProperty('--drift',(Math.random()*130-65)+'px');
  el.style.animationDuration=(7+Math.random()*7)+'s';
  particles.appendChild(el);
  setTimeout(()=>el.remove(),15000);
}
setInterval(floatParticle,450);

/* ===== TOAST ===== */
let toastTimer;
function toast(text){
  const el=document.getElementById('toast');
  el.textContent=text;el.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer=setTimeout(()=>el.classList.remove('show'),2400);
}

/* ===== NAVIGATION ===== */
let current=1;
function go(n){
  current=n;
  document.querySelectorAll('.page').forEach(p=>p.classList.add('hidden'));
  const target=document.getElementById('page'+n);
  target.classList.remove('hidden');
  target.style.animation='none';void target.offsetWidth;target.style.animation='';
  document.getElementById('progressBar').style.width=(n/5*100)+'%';
  document.getElementById('stageText').textContent=`STAGE 0${n} / 05`;
  window.scrollTo({top:0,behavior:'smooth'});
  if(n===5)confetti(35);
  if(n===2)toast('✨ Đã mở khóa: Vũ trụ lời chúc');
  if(n===4)toast('🪐 Mini game đã sẵn sàng!');
}

/* ===== WISH GENERATOR ===== */
const wishes=[
'🌸 Chúc bạn luôn tươi vui như những đóa hoa, mỗi ngày đều có một lý do để mỉm cười. Mong bạn được yêu thương bằng sự chân thành và luôn gặp những điều dễ thương.',
'💎 Chúc bạn tự tin tỏa sáng theo cách riêng của mình. Mong mọi cố gắng đều được đền đáp và những ước mơ đẹp sẽ dần trở thành hiện thực.',
'🌙 Chúc bạn có những ngày bình yên, tâm hồn nhẹ nhàng và luôn có người sẵn lòng lắng nghe. Mong bạn đủ mạnh mẽ để vượt qua ngày khó khăn.',
'🍀 Chúc bạn gặp nhiều may mắn, học tập thuận lợi, có thêm nhiều niềm vui và luôn tìm thấy điều tích cực trong những chuyện nhỏ bé.'
];
function wish(i){
  const box=document.getElementById('wishBox');
  box.textContent=wishes[i];
  box.classList.remove('hidden');
  confetti(10);
  toast('💖 Đã nhận được lời chúc!');
}

/* ===== SECRET LETTER WITH TYPEWRITER ===== */
let mailOpened=false;
const letterMessage='Gửi bạn thân mến! Chúc bạn một ngày 20/10 thật vui vẻ và đáng nhớ. Mong bạn luôn biết trân trọng bản thân, giữ nụ cười trên môi và không ngừng theo đuổi điều mình yêu thích. Bạn không cần phải hoàn hảo để trở nên đặc biệt. Chỉ cần là chính mình, bạn đã có nét đẹp riêng rồi. Chúc bạn luôn bình an, tự tin và gặp thật nhiều điều tốt lành! 💖🌷';
function openMail(){
  if(mailOpened)return;
  mailOpened=true;
  const box=document.getElementById('letterText');
  box.innerHTML='';
  let i=0;
  const timer=setInterval(()=>{
    box.textContent+=letterMessage.charAt(i);
    i++;
    if(i>=letterMessage.length){
      clearInterval(timer);
      box.textContent=letterMessage;
    }
  },25);
  document.getElementById('mailIcon').textContent='💖';
  document.getElementById('mailBtn').textContent='💗 THÔNG ĐIỆP ĐÃ MỞ';
  confetti(24);
  toast('🔓 Giải mã thành công!');
}

/* ===== MINI GAME ===== */
let played=false;
const prizes=[
'🌸 PHẦN THƯỞNG: Một ngày thật nhiều tiếng cười. Mong bạn luôn có lý do để vui vẻ!',
'💎 PHẦN THƯỞNG: May mắn +100! Chúc những điều bạn cố gắng đều có kết quả tốt.',
'🌈 PHẦN THƯỞNG: Bình an +100! Mong bạn luôn gặp người tử tế và những điều ấm áp.'
];
function pickStar(i){
  if(played){toast('✨ Bạn đã chọn rồi, chơi lại nhé!');return}
  played=true;
  document.getElementById('gameResult').textContent=prizes[i];
  document.querySelectorAll('.star-choice').forEach((b,j)=>{
    b.disabled=true;
    if(j===i){
      b.style.opacity='1';b.style.borderColor='#ff76d8';
      b.style.boxShadow='0 0 25px #ff36c766';
      b.querySelector('span').textContent='💖';
    }else b.style.opacity='.35';
  });
  confetti(22);
  toast('🎉 Chúc mừng bạn nhận quà!');
}
function resetGame(){
  played=false;
  document.getElementById('gameResult').textContent='🎮 Một lượt chọn đang chờ bạn. Vận may nằm trong tay bạn!';
  document.querySelectorAll('.star-choice').forEach((b,i)=>{
    b.disabled=false;b.style.opacity='1';b.style.borderColor='';b.style.boxShadow='';
    b.querySelector('span').textContent=['🌟','💫','✨'][i];
  });
  toast('🔄 Đã làm mới trò chơi!');
}

/* ===== FINAL GIFT ===== */
let giftOpened=false;
function openGift(){
  if(giftOpened){toast('💖 Món quà đã được mở rồi!');return}
  giftOpened=true;
  document.getElementById('giftIcon').textContent='💝';
  const msg='CHÚC MỪNG NGÀY 20/10! 🌷 Chúc bạn luôn hạnh phúc, khỏe mạnh, tự tin và gặp nhiều điều tốt lành. Mong rằng mỗi ngày đều mang đến một niềm vui mới, những ước mơ sẽ dần thành hiện thực và nụ cười luôn ở trên môi bạn. Hãy luôn yêu thương bản thân và tỏa sáng theo cách riêng của mình nhé! 💖✨';
  const box=document.getElementById('giftText');
  box.textContent=msg;
  document.getElementById('giftBtn').textContent='💖 QUÀ ĐÃ ĐƯỢC MỞ';
  confetti(65);
  for(let i=0;i<5;i++)setTimeout(shootingStar,i*250);
  toast('🎁 Chúc mừng! Bạn đã mở kho báu!');
}

/* ===== CONFETTI BURST ===== */
function confetti(amount=25){
  const pieces=['💖','✨','🌸','💗','⭐','🎉','💕','✦','💫'];
  for(let i=0;i<amount;i++){
    const el=document.createElement('span');
    el.className='confetti';
    el.textContent=pieces[Math.floor(Math.random()*pieces.length)];
    el.style.left=Math.random()*100+'vw';
    el.style.fontSize=(12+Math.random()*20)+'px';
    el.style.animationDuration=(2+Math.random()*2.5)+'s';
    el.style.setProperty('--x',(Math.random()*200-100)+'px');
    document.body.appendChild(el);
    setTimeout(()=>el.remove(),5000);
  }
}

/* CHẠM NỀN ĐỂ TẠO HIỆU ỨNG */
document.addEventListener('click',e=>{
  if(e.target.closest('button'))return;
  const el=document.createElement('span');
  el.className='float';el.textContent='💖';
  el.style.left=e.clientX+'px';
  el.style.bottom=(innerHeight-e.clientY)+'px';
  el.style.fontSize='25px';el.style.animationDuration='2.5s';
  particles.appendChild(el);
  setTimeout(()=>el.remove(),3000);
});
</script>
</body>
</html>
