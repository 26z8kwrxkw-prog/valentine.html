<!DOCTYPE html>
<html>
<head>
  <title>Be My Valentine?</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 80px;
    }

    h1 {
      color: white;
      font-size: 3em;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
    }

    p {
      color: white;
      font-size: 1.3em;
      margin-bottom: 30px;
    }

    button {
      padding: 15px 30px;
      font-size: 1.2em;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.2s ease;
    }

    #yesBtn {
      background-color: #ff4d6d;
      color: white;
    }

    #noBtn {
      background-color: white;
      color: #ff4d6d;
      position: absolute;
    }

    #message {
      margin-top: 30px;
      color: white;
      font-size: 1.8em;
      font-weight: bold;
    }
  </style>
</head>

<body>
  <h1>💘 Will You Be My Valentine? 💘</h1>
  <p>You make my heart smile 💕</p>

  <button id="yesBtn" onclick="sayYes()">Yes 💖</button>
  <button id="noBtn" onmouseover="moveButton()">No 😢</button>

  <div id="message"></div>

  <script>
    function sayYes() {
      document.getElementById("message").innerHTML = 
        "YAY!! 💞 You just made my day 🥰";
    }

    function moveButton() {
      const btn = document.getElementById("noBtn");
      const x = Math.random() * (window.innerWidth - 120);
      const y = Math.random() * (window.innerHeight - 60);
      btn.style.left = x + "px";
      btn.style.top = y + "px";
    }
  </script>
</body>
</html>