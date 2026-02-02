<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Valentine 💘</title>

  <style>
    body {
      background: linear-gradient(135deg, #ffd6e8, #ffe6e6);
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .box {
      background: white;
      padding: 50px;
      border-radius: 30px;
      text-align: center;
      width: 520px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.25);
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 2;
    }

    h2 {
      font-size: 36px;
      color: #d6336c;
    }

    p {
      font-size: 22px;
      margin: 25px 0;
    }

    img {
      width: 180px;
      border-radius: 20px;
      margin: 20px 0;
    }

    button {
      padding: 15px 35px;
      font-size: 20px;
      border-radius: 15px;
      border: none;
      cursor: pointer;
      position: absolute;
      transition: transform 0.15s;
    }

    #yes {
      background: #ff4d6d;
      color: white;
      position: static;
      transition: transform 0.3s;
    }

    #no {
      background: #dee2e6;
      color: #333;
    }

    .heart {
      position: fixed;
      font-size: 24px;
      animation: fly 2.5s linear forwards;
      pointer-events: none;
    }

    @keyframes fly {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-350px); opacity: 0; }
    }
  </style>
</head>

<body>

  <div class="box">
    <h2>💖 Sophie 💖</h2>
    <img src="https://cataas.com/cat/cute" alt="Cute cat with flowers">
    <p id="question">Would you be my Valentine?</p>
    <button id="yes">YES 💕</button>
    <button id="no">NO 😈</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    let escapeCount = 0;

    function moveNoButton() {
      escapeCount++;

      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";

      // YES button grows each escape
      const scale = 1 + escapeCount * 0.05;
      yesBtn.style.transform = `scale(${scale})`;
    }

    noBtn.addEventListener("mouseenter", moveNoButton);
    noBtn.addEventListener("click", moveNoButton);

    yesBtn.addEventListener("click", () => {
      document.getElementById("question").innerHTML =
        "💖 YAAAAAY!!! BEST. VALENTINE. EVER. 💖";
      explodeHearts();
    });

    function explodeHearts() {
      for (let i = 0; i < 30; i++) {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerText = "💖";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.bottom = "0px";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 2500);
      }
    }
  </script>

</body>
</html>

