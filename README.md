<html>
<head>
  <title>Play Google Drive Audio</title>
</head>
<body style="text-align:center; font-family:Arial; padding-top:50px; background:#fff0f5;">

  <h2>🎵 Play Birthday Music from Google Drive</h2>

  <button onclick="playAudio()" style="padding:12px 24px; font-size:16px; background-color:#e91e63; color:white; border:none; border-radius:8px; cursor:pointer;">
    ▶️ Play Audio
  </button>

  <!-- Your Google Drive audio -->
  <audio id="myAudio" src="https://docs.google.com/uc?export=open&id=10EjY02zBdnJCOnH6LYU-IS8wSOxXTee6"></audio>

  <script>
    function playAudio() {
      var audio = document.getElementById("myAudio");
      audio.play();
    }
  </script>

</body>
</html>
