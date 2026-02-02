<!DOCTYPE html>
<html>
<head>
  <title>Valentine 💘</title>
  <style>
    body {
      background-color: #ffe6e6;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    #valentineBox {
      background-color: #fff0f5;
      border: 2px solid #cc0000;
      border-radius: 30px;
      padding: 50px;
      text-align: center;
      width: 550px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.25);
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    h1 {
      color: #cc0000;
      margin-bottom: 20px;
      font-size: 36px;
    }

    p {
      font-size: 22px;
      margin: 20px 0;
    }

    img {
      width: 280px; /* BIG CAT */
      border-radius: 25px;
      margin: 20px 0;
    }

    button {
      padding: 15px 35px;
      font-size: 20px;
      border-radius: 15px;
      border: none;
      cursor: pointer;
      margin: 10px;
      position: absolute;
    }

    #yesBtn {
      background-color: #ff4d4d;
      color: white;
      position: static;
    }

    #noBtn {
      background-color: #cccccc;
    }
  </style>
</head>

<body>

  <div id="valentineBox">
    <h1>💖 Sophie 💖</h1>

    <!-- BIG CAT WITH FLOWERS -->
    <img src="https://cataas.com/cat/cute" alt="Cat with flowers">

    <p id="question">Would you be my Valentine?</p>

    <button id="yesBtn">YES 💕</button>
    <button id="noBtn">NO 😈</button>
  </div>

  <script>
    const noBtn = document.getElementById('noBtn');
    const yesBtn = document.getElementById('yesBtn');

    function moveNoButton() {
      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    noBtn.addEventListener('mouseenter', moveNoButton);
    noBtn.addEventListener('click', moveNoButton);

    yesBtn.addEventListener('click', () => {
      document.getElementById("question").innerHTML =
        "💖 YAAAAAY!!! 💖";
    });
  </script>

</body>
</html>

