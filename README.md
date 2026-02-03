# Giselle-loved-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>My Giselle 💖</title>

<style>
body {
  margin: 0;
  font-family: 'Georgia', serif;
  background: linear-gradient(to bottom, #ffe6f0, #fff);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.card {
  background: white;
  width: 90%;
  max-width: 380px;
  border-radius: 30px;
  padding: 25px;
  text-align: center;
  box-shadow: 0 0 40px rgba(255, 105, 180, 0.4);
}

h1 {
  color: #e75480;
  margin-bottom: 10px;
}

.subtitle {
  font-style: italic;
  color: #b85c7a;
  margin-bottom: 20px;
}

img {
  width: 100%;
  border-radius: 20px;
  margin: 20px 0;
}

.text {
  color: #6b2c3e;
  font-size: 16px;
  line-height: 1.6;
}

button {
  margin-top: 20px;
  padding: 14px 28px;
  font-size: 18px;
  border: none;
  border-radius: 30px;
  background: #e75480;
  color: white;
  cursor: pointer;
  box-shadow: 0 10px 20px rgba(231,84,128,0.4);
}

button:hover {
  transform: scale(1.05);
}
</style>
</head>

<body>

<div class="card">
  <h1>My Giselle 💕</h1>
  <div class="subtitle">You are my favorite place to exist</div>

  <!-- TULIP IMAGE (WORKING) -->
  <img src="https://images.unsplash.com/photo-1528825871115-3581a5387919?auto=format&fit=crop&w=900&q=80" alt="Tulips">

  <div class="text">
    Every laugh. Every memory. Every moment that feels like home.  
    It’s always been you.  
    And it will always be you.
  </div>

  <!-- PLAY MUSIC BUTTON -->
  <button onclick="playMusic()">Play Our Song 🎶</button>
</div>

<!-- AUDIO -->
<audio id="music">
  <source src="https://cdn.pixabay.com/audio/2022/03/15/audio_7c3bffb8d4.mp3" type="audio/mpeg">
</audio>

<script>
function playMusic() {
  const music = document.getElementById("music");
  music.play();
}
</script>

</body>
</html>
