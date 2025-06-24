<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Baba Barışalım Mı?</title>
  <style>
    body {
      text-align: center;
      margin-top: 100px;
      font-family: Arial, sans-serif;
    }
    button {
      font-size: 24px;
      padding: 10px 20px;
      margin: 20px;
    }
    #yes {
      background-color: green;
      color: white;
    }
    #no {
      background-color: red;
      color: white;
      position: relative;
    }
  </style>
</head>
<body>
  <h1>Baba benimle barışır mısın? 😊</h1>
  <button id="yes" onclick="baristik()">Evet</button>
  <button id="no" onclick="hayir()">Hayır</button>

  <script>
    let noClick = 0;
    function baristik() {
      document.body.innerHTML = "<h1>🎉 Harikasın Baba! Hadi sarılmaya! 💙</h1>";
    }
    function hayir() {
      noClick++;
      let noBtn = document.getElementById("no");
      noBtn.style.fontSize = (24 - noClick * 3) + "px";
      noBtn.innerText = "Cidden mi?";
      if (noClick >= 5) {
        noBtn.disabled = true;
        noBtn.innerText = "Olmaz artık 😢";
      }
    }
  </script>
</body>
</html>
