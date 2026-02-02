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

    .buttons {
      margin-top: 20px;
      position: relative;
    }

    button {
      padding: 15px 35px;
      font-size: 20px;
      border-radius: 15px;
      border: none;
      cursor: pointer;
      margin: 10px;
    }

    #yes {
      background: #ff4d6d;
      color: white;
    }

    #no {
      background: #dee2e6;
      color: #333;
      position: absolute;
    }

    .hearts {
      font-size: 40px;
      margin-top: 20px;
    }
  </style>
</head>

<body>

  <div class="box">
    <h2>💖 Sophie 💖</h2>
    <img src="https://cataas.com/cat/cute" alt="Cute cat with flowers">
    <p id="question">Would you be my Valentine?</p>

    <div class="buttons">
      <button id="yes">YES 💕</button>
      <button id="no">NO 😈</button>
    </div>

    <div id="hearts" class="hearts"></div>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const heartsDiv = document.getElementById("hearts");

    function moveNo() {
      const box = document.querySelector(".box");
      const rect = box.getBoundingClientRect();

      const x = Math.random() * (rect.width - 100);
      const y = Math.random() * (rect.height - 100);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    noBtn.addEventListener("mouseenter", moveNo);
    noBtn.addEventListener("click", moveNo);

    yesBtn.addEventListener("click", () => {
      document.getElementById("question").innerHTML =
        "💖 YAAAAAY!!! BEST VALENTINE EVER 💖";

      heartsDiv.innerHTML = "💖 💕 💖 💕 💖 💕 💖 💕 💖";
    });
  </script>

</body>
</html>
