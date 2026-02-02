index.html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Valentine 💘</title>
  <style>
    body {
      background: #ffe6e6;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }
    .box {
      background: white;
      padding: 25px;
      border-radius: 20px;
      text-align: center;
      width: 320px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      margin: 10px;
      border-radius: 10px;
      border: none;
      cursor: pointer;
    }
    #yes { background: #ff4d4d; color: white; }
    #no { background: #ccc; }
  </style>
</head>
<body>

<div class="box">
  <h2 id="title">💖 Sophie 💖</h2>
  <img src="https://cataas.com/cat/cute" width="120">
  <p id="question">Would you be my Valentine?</p>
  <button id="yes">YES</button>
  <button id="no">NO</button>
</div>

<script>
  document.getElementById("yes").onclick = function () {
    document.getElementById("question").innerHTML =
      "💖 YAY!!! BEST VALENTINE EVER 💖";
  };

  document.getElementById("no").onmouseover = function () {
    this.style.transform =
      "translate(" + (Math.random()*80 - 40) + "px," +
      (Math.random()*40 - 20) + "px)";
  };
</script>

</body>
</html>

