<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Louis Phan | Profile</title>
  <style>
    body, html {
      margin: 0; padding: 0;
      height: 100%;
      font-family: 'Segoe UI', sans-serif;
      background: black;
      overflow-x: hidden;
      color: #fff;
      position: relative;
    }
    canvas#galaxy {
      position: fixed; top: 0; left: 0;
      z-index: 0;
    }
    .container {
      position: relative; z-index: 10;
      min-height: 100vh;
      display: flex; flex-direction: column;
      align-items: center; justify-content: center;
      text-align: center; padding: 20px;
    }
    .avatar {
      width: 160px; height: 160px;
      border-radius: 50%;
      border: 4px solid #adff2f;
      box-shadow: 0 0 15px #adff2f, 0 0 25px #ffffff;
      margin-bottom: 20px;
      transition: transform 0.3s ease;
    }
    .avatar:hover { transform: scale(1.05); }
    h1 {
      font-size: 2.8rem;
      color: #adff2f;
      text-shadow: 0 0 10px #adff2f, 0 0 20px #ffffff;
      margin: 0;
    }
    h2.shine-text {
      font-size: 1.2rem;
      font-weight: bold;
      background: linear-gradient(90deg, #adff2f, #ffffff, #adff2f);
      background-size: 200% auto;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: shine 2s linear infinite;
      text-shadow: 0 0 10px rgba(173,255,47,0.5), 0 0 15px white;
      margin: 10px 0 30px;
    }
    @keyframes shine {
      0% { background-position: 0% center; }
      100% { background-position: 200% center; }
    }
    .social {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin-bottom: 15px;
    }
    .social a {
      padding: 10px 20px;
      background-color: transparent;
      border: 2px solid #adff2f;
      border-radius: 30px;
      color: #adff2f;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
      box-shadow: 0 0 10px #adff2f, 0 0 15px #ffffff;
    }
    .social a:hover {
      background-color: #adff2f;
      color: black;
      box-shadow: 0 0 15px #ffffff, 0 0 20px #adff2f;
    }
    .music-toggle { margin-bottom: 20px; }
    .music-toggle button {
      padding: 8px 18px;
      font-weight: bold;
      font-size: 1rem;
      color: #adff2f;
      background: transparent;
      border: 2px solid #adff2f;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 0 10px #adff2f, 0 0 15px #ffffff;
      transition: 0.3s;
    }
    .music-toggle button:hover {
      background-color: #adff2f;
      color: black;
      box-shadow: 0 0 15px #ffffff, 0 0 20px #adff2f;
    }
    .music-toggle button.playing {
      background-color: #adff2f;
      color: black;
      box-shadow: 0 0 20px #adff2f, 0 0 30px #ffffff;
      transform: scale(1.05);
    }
    .tagline {
      margin-top: 0;
      font-style: italic;
      font-size: 1.1rem;
      color: #ccffcc;
      min-height: 24px;
      margin-bottom: 10px;
    }
    .glow-typewriter {
      color: #adff2f;
      text-shadow: 0 0 5px #adff2f, 0 0 10px #ffffff, 0 0 15px #adff2f;
      border-right: .1em solid #adff2f;
      white-space: nowrap;
      overflow: hidden;
    }
    #clock {
      margin-top: 15px;
      font-size: 1.2rem;
      color: #adff2f;
      text-shadow: 0 0 5px #adff2f, 0 0 10px #ffffff;
    }
    .about {
      max-width: 600px;
      background: rgba(173, 255, 47, 0.05);
      padding: 20px;
      border-radius: 10px;
      border: 1px solid #adff2f33;
      margin-top: 30px;
    }
    .about h3 {
      color: #adff2f;
      margin-bottom: 10px;
      text-shadow: 0 0 10px #adff2f, 0 0 20px #ffffff;
    }
    .about p {
      color: #ccffcc;
      text-shadow: 0 0 5px #adff2f;
    }
    .about img {
      margin-top: 15px;
      max-width: 100%;
      border-radius: 10px;
      box-shadow: 0 0 10px #adff2f, 0 0 15px #ffffff;
    }
    .anime-logo {
      position: fixed;
      width: 70px; height: 70px;
      border-radius: 50%;
      object-fit: cover;
      filter: drop-shadow(0 0 8px #adff2f);
      opacity: 0.7;
      transition: transform 0.3s ease, opacity 0.3s ease;
      z-index: 5;
    }
    .anime-logo:hover {
      transform: scale(1.3) rotate(5deg);
      opacity: 1;
      filter: drop-shadow(0 0 20px #ffffff);
      z-index: 15;
    }
    footer {
      margin-top: 30px;
      font-size: 0.9rem;
      color: #adff2faa;
      text-shadow: 0 0 10px #adff2f, 0 0 15px #ffffff;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <canvas id="galaxy"></canvas>
  <div class="container">
    <img class="avatar" src="https://i.imgur.com/Adj8Q5F.png" alt="KH Linh Avatar">
    <h1>Louis Phan 🌸</h1>
    <h2 class="shine-text">UY TÍN CHẤT LƯỢNG HÀNG ĐẦU VIỆT  NAM</h2>

    <div class="social">
      <a href="https://www.facebook.com/share/1FASAwmRaj/" target="_blank">📘 Facebook</a>
      <a href="https://zalo.me/0904687009" target="_blank">🛍️ Zalo</a>
      <a href="https://www.facebook.com/share/v/1Bp4Mhw5fz/" target="_blank">🌐Tus Ghim TCN</a>
    </div>

    <div class="music-toggle">
      <button id="music-btn">Bật Nhạc 🎵</button>
    </div>

    <p class="tagline"><span id="typewriter" class="glow-typewriter"></span></p>
    <p id="clock"></p>

    <div class="about">
      <h3>💬 Giới thiệu</h3>
      <p>Nhận cày thuê - GamePass - Sell Robux - thiết kế banner giá rẻ</p>
      <img src="https://i.imgur.com/W0U68pS.jpeg" alt="Cosplay GIF">
      <img src="https://i.imgur.com/SdbgwYJ.png" alt="Cap Wall Image">
    </div>

    <footer>© 2025 Website By TRẦN HÀO | DARKSTACK TEAM</footer>
  </div>

  <!-- Logo anime -->
  <img src="https://i.imgur.com/CYmY9aQ.jpeg" class="anime-logo" style="top: 10vh; left: 5vw;" alt="Anime 1" />
  <img src="https://i.imgur.com/p1zHbbR.jpeg" class="anime-logo" style="top: 30vh; right: 8vw;" alt="Anime 2" />
  <img src="https://i.imgur.com/G5ZhIdd.png" class="anime-logo" style="bottom: 20vh; left: 10vw;" alt="Anime 3" />
  <img src="https://i.imgur.com/grr6Cl6.jpeg" class="anime-logo" style="bottom: 12vh; right: 12vw;" alt="Anime 4" />

  <!-- Nhạc nền -->
  <audio id="background-music" preload="auto" loop>
    <source src="https://pomf2.lain.la/f/ya8ix3yd.mp3" type="audio/mpeg">
  </audio>

  <script>
    const canvas = document.getElementById('galaxy');
    const ctx = canvas.getContext('2d');
    let stars = [];

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }
    function createStars(count) {
      stars = [];
      for (let i = 0; i < count; i++) {
        stars.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          radius: Math.random() * 1.5,
          velocity: Math.random() * 0.5 + 0.2
        });
      }
    }
    function drawStars() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.fillStyle = "#ffffff";
      stars.forEach(star => {
        ctx.beginPath();
        ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
        ctx.fill();
      });
    }
    function animateStars() {
      stars.forEach(star => {
        star.y += star.velocity;
        if (star.y > canvas.height) {
          star.y = 0;
          star.x = Math.random() * canvas.width;
        }
      });
      drawStars();
      requestAnimationFrame(animateStars);
    }
    window.addEventListener('resize', () => {
      resizeCanvas();
      createStars(150);
    });
    resizeCanvas();
    createStars(150);
    animateStars();

    // Typewriter
    const quotes = [
      "💖 Tiền không ngủ, và tôi cũng vậy.",
      "💫 Làm MMO : ai hiểu luật, người đó ăn tiền.",
      "💎 Shop uy tín – khách là bạn.",
      "🧸 Hỏi gì cũng rep, khỏi ngại!"
    ];
    let currentQuote = 0;
    const typewriter = document.getElementById("typewriter");
    function typeWriterEffect(text, index = 0) {
      if (index === 0) {
        typewriter.textContent = '';
        typewriter.classList.remove("glow-typewriter");
        void typewriter.offsetWidth;
        typewriter.classList.add("glow-typewriter");
      }
      if (index < text.length) {
        typewriter.textContent += text.charAt(index);
        setTimeout(() => typeWriterEffect(text, index + 1), 60);
      }
    }
    function showNextQuote() {
      typeWriterEffect(quotes[currentQuote]);
      currentQuote = (currentQuote + 1) % quotes.length;
    }
    showNextQuote();
    setInterval(showNextQuote, 5000);

    // Đồng hồ
    function updateClock() {
      const now = new Date(Date.now() + 7 * 3600 * 1000);
      const h = now.getUTCHours().toString().padStart(2, '0');
      const m = now.getUTCMinutes().toString().padStart(2, '0');
      const s = now.getUTCSeconds().toString().padStart(2, '0');
      document.getElementById("clock").textContent = `🕒 ${h}:${m}:${s} (Giờ Việt Nam)`;
    }
    setInterval(updateClock, 1000);
    updateClock();

    // Nhạc nền
    const musicBtn = document.getElementById('music-btn');
    const music = document.getElementById('background-music');
    let isPlaying = false;

    musicBtn.addEventListener('click', () => {
      if (isPlaying) {
        music.pause();
        musicBtn.textContent = 'Bật Nhạc 🎵';
        musicBtn.classList.remove('playing');
        isPlaying = false;
      } else {
        music.play().then(() => {
          musicBtn.textContent = 'Tắt Nhạc 🔇';
          musicBtn.classList.add('playing');
          isPlaying = true;
        }).catch(() => {
          alert("⚠️ Trình duyệt yêu cầu bạn phải *nhấn lại* để bật nhạc.");
        });
      }
    });
  </script>
</body>
</html>
