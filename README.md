<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Merry Christmas Quỳnh Anh 10A2 🎄✨</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      height: 100vh;
      background: linear-gradient(to bottom, #0f0c29, #302b63, #24243e);
      color: white;
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
      position: relative;
      cursor: pointer;
    }
    .container {
      position: relative;
      z-index: 10;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
    }
    h1 {
      font-family: 'Dancing Script', cursive;
      font-size: clamp(3.5rem, 10vw, 5rem);
      color: #fff;
      text-shadow: 0 0 20px #ff69b4, 0 0 40px #ff1493;
      margin-bottom: 10px;
      animation: glow 2s ease-in-out infinite alternate;
    }
    .name {
      font-size: clamp(2.5rem, 8vw, 3.8rem);
      color: #ffd700;
      text-shadow: 0 0 15px #ffcc00;
      margin: 20px 0;
      animation: float 5s ease-in-out infinite;
    }
    .message {
      max-width: 90%;
      font-size: 1.2rem;
      line-height: 1.7;
      background: rgba(255,255,255,0.08);
      backdrop-filter: blur(10px);
      padding: 25px;
      border-radius: 20px;
      border: 1px solid rgba(255,255,255,0.15);
      margin: 30px 0;
      opacity: 0;
      transform: scale(0.8);
      transition: all 1.2s ease;
    }
    .message.show { opacity: 1; transform: scale(1); }
    .gift-box {
      width: clamp(180px, 50vw, 240px);
      height: clamp(180px, 50vw, 240px);
      position: relative;
      cursor: pointer;
      margin: 40px 0;
    }
    .box {
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, #ff6b6b, #ff8e53);
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.4);
      position: relative;
      transition: transform 0.8s ease;
      overflow: hidden;
      z-index: 2;
    }
    .gift-box.open .box { transform: translateY(-50px) rotateX(60deg); }
    .lid {
      width: 100%;
      height: 70px;
      background: #ff4757;
      position: absolute;
      top: -70px;
      left: 0;
      border-radius: 15px 15px 0 0;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
      transition: all 0.9s ease;
      transform-origin: bottom;
      z-index: 3;
    }
    .gift-box.open .lid { transform: rotateX(90deg) translateY(-100px); }
    .ribbon {
      width: 80px;
      height: 20px;
      background: #ffd700;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      border-radius: 5px;
      z-index: 4;
    }
    .ribbon::before, .ribbon::after {
      content: '';
      position: absolute;
      width: 100px;
      height: 100px;
      background: #ffd700;
      top: -40px;
      left: -10px;
      clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
      z-index: 1;
    }
    .gift-box.open .ribbon { opacity: 0; }
    .gift-content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: clamp(2.5rem, 8vw, 4rem);
      opacity: 0;
      transition: all 1.2s ease;
      z-index: 5;
    }
    .gift-box.open .gift-content { opacity: 1; animation: pop 1s ease; }
    .tree {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 300px;
      height: 400px;
      background: url('https://www.pngall.com/wp-content/uploads/2016/06/Christmas-Tree-PNG-Free-Download.png') no-repeat center bottom;
      background-size: contain;
      pointer-events: none;
      z-index: 1;
      opacity: 0.7;
    }
    .snowflake {
      position: absolute;
      width: 8px;
      height: 8px;
      background: white;
      border-radius: 50%;
      pointer-events: none;
      animation: fall linear infinite;
      opacity: 0.8;
    }
    @keyframes fall { to { transform: translateY(100vh) rotate(360deg); } }
    @keyframes glow { from { text-shadow: 0 0 10px #ff69b4, 0 0 20px #ff1493; } to { text-shadow: 0 0 30px #ff69b4, 0 0 60px #ff1493; } }
    @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-15px); } }
    @keyframes pop { 0% { transform: translate(-50%, -50%) scale(0); } 50% { transform: translate(-50%, -50%) scale(1.4); } 100% { transform: translate(-50%, -50%) scale(1); } }
  </style>
</head>
<body>
  <div class="container">
    <h1>Merry Christmas!</h1>
    <div class="name">Quỳnh Anh 10A2 🎅✨</div>
    
    <div class="gift-box" id="giftBox">
      <div class="lid"></div>
      <div class="box">
        <div class="ribbon"></div>
        <div class="gift-content" id="gift">🎁</div>
      </div>
    </div>

    <div class="message" id="message">
      Chúc Quỳnh Anh Giáng sinh thật vui, thật ấm áp và tràn đầy hạnh phúc nhaaa! 🎄<br>
      Mong năm học mới của mình sẽ thật nhiều niềm vui, nhiều thành tích xịn xò,<br>
      và đặc biệt là luôn cười thật tươi như bây giờ! 😊<br><br>
      Cảm ơn vì đã là một người bạn tuyệt vời của tụi mình.<br>
      Yêu thương & ôm cái thật chặt nèee! 🤗❤️
    </div>
  </div>

  <div class="tree"></div>

  <!-- Confetti -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <script>
    const giftBox = document.getElementById('giftBox');
    const giftContent = document.getElementById('gift');
    const message = document.getElementById('message');

    const gifts = [
      "🌟 Chúc Quỳnh Anh luôn là ngôi sao sáng nhất lớp!",
      "🍫 Một thanh socola siêu to khổng lồ từ bạn!",
      "💖 Một cái ôm thật chặt từ cả đám bạn 10A2!"
    ];

    function openGift() {
      if (!giftBox.classList.contains('open')) {
        giftBox.classList.add('open');

        setTimeout(() => {
          message.classList.add('show');
        }, 1000);

        const randomGift = gifts[Math.floor(Math.random() * gifts.length)];
        giftContent.innerHTML = randomGift;

        // Confetti
        confetti({
          particleCount: 120,
          spread: 70,
          origin: { y: 0.6 }
        });

        // Confetti liên tục
        const duration = 3000;
        const end = Date.now() + duration;
        (function frame() {
          confetti({
            particleCount: 5,
            angle: 60,
            spread: 55,
            origin: { x: 0 }
          });
          confetti({
            particleCount: 5,
            angle: 120,
            spread: 55,
            origin: { x: 1 }
          });
          if (Date.now() < end) requestAnimationFrame(frame);
        })();
      }
    }

    // Hỗ trợ click chuột + chạm màn hình
    giftBox.addEventListener('click', openGift);
    giftBox.addEventListener('touchstart', (e) => {
      e.preventDefault();
      openGift();
    });

    // Tuyết rơi (giảm tần suất để không lag)
    function createSnowflake() {
      const snowflake = document.createElement('div');
      snowflake.className = 'snowflake';
      const size = Math.random() * 6 + 4;
      snowflake.style.width = `${size}px`;
      snowflake.style.height = `${size}px`;
      snowflake.style.left = Math.random() * 100 + 'vw';
      const duration = Math.random() * 12 + 10;
      snowflake.style.animationDuration = `${duration}s`;
      snowflake.style.animationDelay = Math.random() * 5 + 's';
      document.body.appendChild(snowflake);
      setTimeout(() => snowflake.remove(), duration * 1000 + 3000);
    }

    setInterval(createSnowflake, 400); // 400ms thay vì 200ms
    for(let i = 0; i < 30; i++) createSnowflake();
  </script>
</body>
</html>
