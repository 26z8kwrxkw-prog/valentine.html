<!DOCTYPE html>
<html>
<head>
  <title>Skyler, Be My Valentine?</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      text-align: center;
      overflow: hidden;
      margin-top: 80px;
    }

    h1 {
      color: white;
      font-size: 3em;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
    }

    p {
      color: white;
      font-size: 1.4em;
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

    /* Floating Hearts */
    .heart {
      position: fixed;
      bottom: -20px;
      font-size: 20px;
      animation: floatUp 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) scale(1.5);
        opacity: 0;
      }
    }
  </style>
</head>

<body>
  <h1>💘 Skyler, Will You Be My Valentine? 💘</h1>
  <p>You make my heart skip a beat 💕</p>

  <button id="yesBtn" onclick="sayYes()">Yes 💖</button>
  <button id="noBtn" onmouseover="moveButton()">No 😢</button>

  <div id="message"></div>

  <script>
    function sayYes() {
      document.getElementById("message").innerHTML =
        "YAY Skyler!! 💞 You just made my heart so happy 🥰";
    }

    function moveButton() {
      const btn = document.getElementById("noBtn");
      const x = Math.random() * (window.innerWidth - 120);
      const y = Math.random() * (window.innerHeight - 60);
      btn.style.left = x + "px";
      btn.style.top = y + "px";
    }

    // Create floating hearts
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "💖";
      heart.style.left = Math.random() * window.innerWidth + "px";
      heart.style.fontSize = Math.random() * 20 + 15 + "px";

      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>
