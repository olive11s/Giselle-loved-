# Giselle-loved-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Giselle 💖</title>

<style>
body {
  margin: 0;
  background: linear-gradient(to bottom, #ffe6f0, #fff);
  font-family: 'Georgia', serif;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  overflow-x: hidden;
}

.card {
  background: white;
  width: 90%;
  max-width: 380px;
  border-radius: 30px;
  padding: 25px;
  text-align: center;
  box-shadow: 0 0 40px rgba(255,105,180,0.4);
  position: relative;
}

h1 {
  color: #e75480;
  margin-bottom: 8px;
}

.subtitle {
  font-style: italic;
  color: #b85c7a;
  margin-bottom: 20px;
}

img {
  width: 100%;
  border-radius: 22px;
  margin: 18px 0;
}

.text {
  color: #6b2c3e;
  font-size: 16px;
  line-height: 1.6;
}

.buttons {
  margin-top: 25px;
  display: flex;
  justify-content: center;
  gap: 15px;
  position: relative;
}

button {
  padding: 14px 26px;
  font-size: 18px;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.3s ease;
}

#yesBtn {
  background: #e75480;
  color: white;
}

#noBtn {
  background: #ccc;
}

#message {
  display: none;
  margin-top: 20px;
  font-size: 18px;
  color: #e75480;
  font-weight: bold;
}

/* Falling hearts & flowers */
.fall {
  position: fixed;
  top: -20px;
  font-size: 20px;
  animation: fall linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(110vh);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="card">
  <h1>My Giselle 💕</h1>
  <div class="subtitle">You are my favorite place to exist</div>

  <!-- TULIP IMAGE -->
  <img src="https://images.pexels.com/photos/36729/tulips-spring-flowers-colorful.jpg" alt="Tulips">

  <div class="text">
    Every laugh. Every memory. Every moment that feels like home.
    It’s always been you. And it will always be you.
  </div>

  <div class="buttons">
    <button id="yesBtn" onclick="yesClicked()">Yes 💖</button>
    <button id="noBtn" onmouseover="moveNo()">No 🙈</button>
  </div>

  <div id="message">
    You chose yes… and honestly, my heart already knew.  
    I choose you today, tomorrow, and for the rest of my life 💕🌷
  </div>
</div>

<script>
let yesScale = 1;

function moveNo() {
  const noBtn = document.getElementById("noBtn");
  const x = Math.random() * 200 - 100;
  const y = Math.random() * 200 - 100;
  noBtn.style.transform = `translate(${x}px, ${y}px)`;
}

function yesClicked() {
  const yesBtn = document.getElementById("yesBtn");
  yesScale += 0.2;
  if (yesScale <= 1.6) {
    yesBtn.style.transform = `scale(${yesScale})`;
  }

  document.getElementById("message").style.display = "block";
  startFalling();
}

function startFalling() {
  setInterval(() => {
    const el = document.createElement("div");
    el.className = "fall";
    el.innerText = Math.random() > 0.5 ? "💖" : "🌷";
    el.style.left = Math.random() * 100 + "vw";
    el.style.animationDuration = (Math.random() * 3 + 3) + "s";
    document.body.appendChild(el);

    setTimeout(() => el.remove(), 6000);
  }, 300);
}
</script>

</body>
</html>
