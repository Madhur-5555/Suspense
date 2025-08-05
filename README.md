<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday Khushi 🎉</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffe0ec, #f9f9f9);
      color: #333;
      overflow-x: hidden;
    }
    .center {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .welcome {
      height: 100vh;
      flex-direction: column;
      text-align: center;
      background: url('https://i.imgur.com/5H4vLhZ.gif') no-repeat center center/cover;
    }
    .welcome h1 {
      font-size: 3rem;
      color: white;
      text-shadow: 2px 2px 5px #000;
    }
    .start-btn {
      padding: 14px 28px;
      font-size: 1.2rem;
      background: #ff3c7d;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 20px;
      transition: 0.3s;
    }
    .start-btn:hover {
      background: #c91a5b;
    }
    .section {
      padding: 50px 20px;
      max-width: 900px;
      margin: auto;
    }
    .hidden {
      display: none;
    }
    .show { opacity: 1; transition: 1s ease-in; }
    .message p {
      font-size: 1.2rem;
      margin-top: 15px;
    }
    .slideshow img {
      width: 100%;
      max-height: 400px;
      object-fit: cover;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
    .slider-controls {
      display: flex;
      justify-content: center;
      margin-top: 10px;
      gap: 20px;
    }
    button.slider-btn {
      background: #ff4d6d;
      color: white;
      border: none;
      padding: 8px 14px;
      border-radius: 6px;
      cursor: pointer;
    }
    ul li {
      margin: 12px 0;
      background: #fff5f8;
      padding: 12px;
      border-left: 4px solid #ff3c7d;
    }
    .gift-box {
      width: 120px;
      height: 120px;
      background: linear-gradient(#ffc0cb, #ff69b4);
      margin: 20px auto;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.5rem;
      cursor: pointer;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    .surprise {
      display: none;
      background: #fff0f5;
      padding: 20px;
      margin-top: 20px;
      border-radius: 10px;
      text-align: center;
    }
    .ending {
      text-align: center;
      margin-top: 50px;
    }
    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      color: #777;
    }
    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

<!-- 🎵 BACKGROUND MUSIC -->
<audio id="bg-music" src="YOUR-MP3-FILE-LINK.mp3" loop></audio>

<!-- 🎉 WELCOME -->
<section class="welcome center" id="welcome">
  <h1>Happy Birthday Khushi 🎂</h1>
  <button class="start-btn" onclick="startSite()">Click to Start</button>
</section>

<!-- 🌸 MAIN CONTENT -->
<section class="section hidden" id="main">

  <!-- 💌 MESSAGE -->
  <div class="message show">
    <h2> Khushi 💖</h2>
    <p>
      <!-- WRITE YOUR MESSAGE HERE -->
      You are the most beautiful blessing in my life... 💕<br>
    </p>
  </div>

  <!-- 📸 SLIDESHOW -->
  <div class="slideshow show">
    <h2>Our Best Memories 📸</h2>
    <img id="slide" src="https://via.placeholder.com/800x400?text=Image+1" alt="Slide">
    <div class="slider-controls">
      <button class="slider-btn" onclick="prevSlide()">Previous</button>
      <button class="slider-btn" onclick="nextSlide()">Next</button>
    </div>
  </div>

  <!-- 🌟 REASONS -->
  <div class="reasons show">
    <h2>Why You're So Special 🌟</h2>
    <ul>
      <li>Your kindness touches hearts</li>
      <li>Your smile makes everything better</li>
      <li>Tujhse baat kare bina din adhura lagta hai.</li>
      <li>Tu milti nahi roz, par yaadon mein roz hoti hai</li>
      <!-- Add more -->
    </ul>
  </div>

  <!-- 🎁 GIFT -->
  <div class="gift show">
    <h2>Surprise Box 🎁</h2>
    <div class="gift-box" onclick="revealGift()">Click Me</div>
    <div class="surprise" id="gift-msg">
      <!-- WRITE YOUR SURPRISE MESSAGE HERE -->
      Behind every gift is a heart that loves you ❤️ — and mine always will.
    </div>
  </div>

  <!-- 🌹 ENDING -->
  <div class="ending show">
    <h2>Made with Love 💝</h2>
    <p>By Madhur</p>
  </div>

</section>

<!-- 🦶 FOOTER -->
<footer>
  &copy; 2025 | Happy Birthday Khushi | Designed by Madhur
</footer>

<!-- 🧠 JAVASCRIPT LOGIC -->
<script>
  const slides = [
    "https://via.placeholder.com/800x400?text=Image+1",
    "https://via.placeholder.com/800x400?text=Image+2",
    "https://via.placeholder.com/800x400?text=Image+3"
    // 👉 Replace these with actual image URLs
  ];
  let current = 0;

  function nextSlide() {
    current = (current + 1) % slides.length;
    document.getElementById("slide").src = slides[current];
  }

  function prevSlide() {
    current = (current - 1 + slides.length) % slides.length;
    document.getElementById("slide").src = slides[current];
  }

  function revealGift() {
    document.getElementById("gift-msg").style.display = "block";
  }

  function startSite() {
    document.getElementById("welcome").style.display = "none";
    document.getElementById("main").classList.remove("hidden");
    document.getElementById("bg-music").play();
    showConfetti();
  }

  function showConfetti() {
    for (let i = 0; i < 100; i++) {
      const confetti = document.createElement("div");
      confetti.style.position = "fixed";
      confetti.style.top = Math.random() * window.innerHeight + "px";
      confetti.style.left = Math.random() * window.innerWidth + "px";
      confetti.style.width = "10px";
      confetti.style.height = "10px";
      confetti.style.backgroundColor = "#" + Math.floor(Math.random()*16777215).toString(16);
      confetti.style.opacity = "0.7";
      confetti.style.borderRadius = "50%";
      confetti.style.zIndex = 9999;
      confetti.style.animation = "fall 3s linear infinite";
      document.body.appendChild(confetti);
      setTimeout(() => confetti.remove(), 3000);
    }
  }
</script>

</body>
</html>
