# my-website-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kuttu 🐶🧿🎀</title>

<!-- PREMIUM FONTS -->
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
:root{
  --pink:#ffd1dc;
  --rose:#ff8fb1;
  --soft:#fff0f5;
}
*{margin:0;padding:0;box-sizing:border-box}
body{
  font-family:'Poppins',sans-serif;
  background:var(--soft);
  color:#4a2c2a;
  overflow-x:hidden;
}

/* 🔐 PASSWORD */
#lock{
  position:fixed;inset:0;
  background:linear-gradient(135deg,#ffd1dc,#ffe6f0);
  display:flex;flex-direction:column;
  justify-content:center;align-items:center;
  z-index:9999;
}
#lock h2{margin-bottom:15px}
#lock input{
  padding:14px 22px;
  border:none;border-radius:30px;
  font-size:16px;
  text-align:center;
}
#lock button{
  margin-top:15px;
  padding:12px 28px;
  border:none;border-radius:30px;
  background:var(--rose);
  color:#fff;font-size:16px;
}

/* 🌍 HERO */
.hero{
  height:100vh;
  background:url('hero-bg.jpg') center/cover no-repeat;
  position:relative;
}
.hero::after{
  content:'';
  position:absolute;inset:0;
  background:rgba(255,182,193,.55);
}
.hero-content{
  position:relative;
  z-index:2;
  height:100%;
  padding:20px;
  display:flex;
  flex-direction:column;
  justify-content:center;
  text-align:center;
  color:white;
}
.hero h1{
  font-family:'Playfair Display',serif;
  font-size:28px;
  line-height:1.3;
}
.hero p{
  margin-top:12px;
  font-size:14px;
}

/* 🎀 SECTION */
.section{padding:30px 15px}
.section h3{
  font-family:'Playfair Display',serif;
  text-align:center;
  margin-bottom:15px;
}

/* 🖼️ IMAGE GALLERY */
.grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:12px;
}
.card{perspective:1200px}
.inner{
  position:relative;
  width:100%;
  padding-top:130%;
  transform-style:preserve-3d;
  transition:1s;
}
.card.active .inner{
  transform:rotateY(180deg) rotateZ(2deg);
}
.face{
  position:absolute;inset:0;
  border-radius:18px;
  overflow:hidden;
  backface-visibility:hidden;
  box-shadow:0 12px 25px rgba(0,0,0,.15);
}
.face img{
  width:100%;height:100%;
  object-fit:cover;
}
.back{
  background:#ffe6f0;
  transform:rotateY(180deg);
  display:flex;
  align-items:center;
  justify-content:center;
  padding:15px;
  font-size:13px;
  text-align:center;
}

/* 🎥 VIDEO */
video{
  width:100%;
  border-radius:18px;
  box-shadow:0 12px 25px rgba(0,0,0,.15);
}

/* 🎶 MUSIC */
.audio-btn{
  position:fixed;
  bottom:15px;right:15px;
  z-index:999;
  background:var(--rose);
  border:none;
  padding:12px;
  border-radius:50%;
  color:white;
}

/* 💕 FLOATING EMOJIS */
.float{
  position:fixed;
  animation:float 10s linear infinite;
  opacity:.7;
}
@keyframes float{
  from{transform:translateY(100vh)}
  to{transform:translateY(-10vh)}
}
</style>
</head>

<body>

<!-- 🔐 PASSWORD SCREEN -->
<div id="lock">
  <h2>Enter Our World 🌍 💕</h2>
  <input id="pwd" type="password" placeholder="Password">
  <button onclick="unlock()">Kuttu 🧿🎀🐶</button>
</div>

<!-- 🌍 HERO -->
<section class="hero">
  <div class="hero-content">
    <h1>Happy Birthday My Woman 🧿 🎀 Bangaaaraaa 🫂 🫀 ❤️</h1>
    <p>
      Renu 🧿🎀👸🏻🫂<br>
      Bachha 🎀👸🏻🧿🌍<br>
      Bangara 🤍👑🌍🥹💋🫂❤️‍🩹<br>
      Kuttu 🐶👸🏻🧿🌍
    </p>
    <p>You Are Mine 🧿 🎀 Today, My Tomorrow, My Forever 🛐🐶👑</p>
  </div>
</section>

<!-- 🖼️ IMAGE MEMORIES -->
<section class="section">
<h3>Our Memories 🧿🎀</h3>
<div class="grid">

<!-- Replace this image with your gallery photo -->
<div class="card" onclick="this.classList.toggle('active')">
  <div class="inner">
    <div class="face"><img src="image1.jpg"></div>
    <div class="face back">I'm Urs & U R Mine Forever Bangara 🐶</div>
  </div>
</div>

<!-- Duplicate this block for more images -->
<div class="card" onclick="this.classList.toggle('active')">
  <div class="inner">
    <div class="face"><img src="image2.jpg"></div>
    <div class="face back">Me + You = ❤️🫂</div>
  </div>
</div>

</div>
</section>

<!-- 🎥 VIDEO MEMORIES -->
<section class="section">
<h3>Our Videos 🎥</h3>
<div class="grid">

<!-- Replace this video with your gallery video -->
<video src="video1.mp4" muted loop controls></video>

</div>
</section>

<!-- 💌 LOVE LETTER -->
<section class="section">
<p style="font-size:14px;line-height:1.7">
Hey ! Listen Kuttu 🐶 👸🏻 🧿 🌍 No matter what, I’ll always hold your hand...
<br><br>
<strong>I'm Forever Your's, Always Your's and Endlessly Yours 💯 🫂 🧿 🥺 🐶 🙇🏻 ❤️</strong>
</p>
</section>

<!-- 🎶 BACKGROUND MUSIC -->
<audio id="bgm" src="song.mp3" loop muted></audio>
<button class="audio-btn" onclick="toggleMusic()">🎵</button>

<script>
function unlock(){
  if(pwd.value==="182004032007"){
    lock.style.display="none";
    bgm.play();
  }
}
function toggleMusic(){
  bgm.muted=!bgm.muted;
  bgm.play();
}

/* floating emojis */
['🐶','🧿','🎀','🫂','🌍','👑'].forEach(e=>{
  let s=document.createElement('div');
  s.className='float';
  s.innerText=e;
  s.style.left=Math.random()*100+'%';
  s.style.fontSize=20+Math.random()*10+'px';
  s.style.animationDuration=8+Math.random()*6+'s';
  document.body.appendChild(s);
});
</script>

</body>
</html>
