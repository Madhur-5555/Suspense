<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday 🎂</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom right, #ffdde1, #ee9ca7);
      color: #333;
      overflow-x: hidden;
    }

    h1 {
      text-align: center;
      font-size: 3em;
      margin-top: 20px;
      color: #ff4081;
    }

    .button {
      display: inline-block;
      padding: 12px 24px;
      font-size: 1.1em;
      margin: 10px;
      background-color: #ff4081;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .button:hover {
      background-color: #e91e63;
    }

    .center {
      text-align: center;
    }

    .hidden-message {
      display: none;
      font-size: 1.5em;
      margin: 20px;
      text-align: center;
      background: rgba(255, 255, 255, 0.8);
      padding: 20px;
      border-radius: 10px;
      color: #4a148c;
    }

    .slideshow-container {
      max-width: 90%;
      margin: auto;
      position: relative;
    }

    .slide {
      display: none;
      width: 100%;
      border-radius: 10px;
    }

    video, img {
      width: 100%;
      border-radius: 10px;
      max-height: 400px;
      object-fit: cover;
    }
  </style>
</head>
<body>

  <h1>🎉 Happy Birthday Khushi 🎉</h1>

  <div class="center">
    <button class="button" onclick="playAudio()">Play Music 🎵</button>
    <button class="button" onclick="toggleMessage()">Show Secret Message 💌</button>
  </div>

  <audio id="birthdayAudio" src="https://drive.google.com/file/d/10EjY02zBdnJCOnH6LYU-IS8wSOxXTee6/preview"></audio>

  <div class="slideshow-container">
    <div class="slide">
      <img src="https://drive.google.com/file/d/1A2UOdfxUJLHkcpgMdKBo4wdpRNNTg5EW/preview" alt="Photo 1" />
    </div>
    <div class="slide">
      <img src="https://drive.google.com/file/d/1RL-I7Gq1yTjc14sZuk6Jhf6dlwv99Xcj/preview" alt="Photo 2" />
    </div>
    <div class="slide">
      <video controls>
        <source src="https://drive.google.com/file/d/1-4vgC5I49ewo02tM1M0WAubgwCUQ9J8X/preview">
        Your browser does not support video.
      </video>
    </div>
    <div class="slide">
      <img src="https://drive.google.com/file/d/1uZvFFqwMtNfIWWQmBXaazVwMn6HwxRnu/preview" alt="Photo 3" />
    </div>
  </div>

  <div class="center">
    <p class="hidden-message" id="secretMsg">
      🥳 Khushi, You are truly special and amazing. May your day be filled with love, surprises, and smiles. Happy Birthday once again! 🎂
    </p>
  </div>

  <script>
    // Audio Play
    function playAudio() {
      const audio = document.getElementById('birthdayAudio');
      audio.play();
    }

    // Toggle Hidden Message
    function toggleMessage() {
      const msg = document.getElementById('secretMsg');
      msg.style.display = msg.style.display === "none" || msg.style.display === "" ? "block" : "none";
    }

    // Slideshow
    let slideIndex = 0;
    const slides = document.getElementsByClassName("slide");

    function showSlides() {
      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slideIndex++;
      if (slideIndex > slides.length) { slideIndex = 1 }
      slides[slideIndex - 1].style.display = "block";
      setTimeout(showSlides, 3000); // 3 seconds
    }

    showSlides();
  </script>

</body>
</html>
