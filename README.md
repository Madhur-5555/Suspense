<!DOCTYPE html>
<html>
<head>
  <title>Play Google Drive Audio</title>
</head>
<body style="text-align:center; padding-top:60px; font-family:sans-serif; background:#fff0f5;">

  <h2>🎵 Play Audio from Google Drive</h2>

  <button onclick="playAudio()" style="padding:10px 25px; background:#e91e63; color:white; border:none; border-radius:8px; font-size:16px;">
    ▶️ Play Music
  </button>

  <br><br>

  <audio id="myAudio" controls style="width:80%; max-width:400px;">
    <source src="https://docs.google.com/uc?export=open&id=10EjY02zBdnJCOnH6LYU-IS8wSOxXTee6" type="audio/mp3">
    Your browser does not support the audio tag.
  </audio>

  <script>
    function playAudio() {
      const audio = document.getElementById("myAudio");
      audio.play();
    }
  </script>

</body>
</html>
