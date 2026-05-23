<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Happy Birthday - TikTok Style</title>
<style>
  body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ff6f61, #fbc531);
    width: 100%;
    height: 100vh;
    overflow: hidden;
    font-family: 'Arial', sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .video-container {
    position: relative;
    width: 90%;
    height: 90%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 20px;
    overflow: hidden;
    background: rgba(255, 255, 255, 0.2);
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
    padding: 20px;
    animation: fadeIn 2s ease-in-out;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  .title {
    font-size: 3em;
    font-weight: bold;
    color: #fff;
    text-shadow: 2px 2px 4px #000;
    margin-bottom: 20px;
    animation: slideDown 1s ease-out;
  }

  @keyframes slideDown {
    0% { transform: translateY(-50px); opacity: 0; }
    100% { transform: translateY(0); opacity: 1; }
  }

  .message {
    font-size: 1.5em;
    color: #fff;
    text-align: center;
    margin-bottom: 30px;
    padding: 0 10px;
    animation: bounce 2s infinite alternate;
  }

  @keyframes bounce {
    0% { transform: translateY(0); }
    100% { transform: translateY(-10px); }
  }

  /* Animated confetti effect */
  .confetti {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    overflow: hidden;
  }
  .confetti-piece {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #fff;
    opacity: 0.8;
    border-radius: 50%;
    animation: fall 3s linear forwards;
  }
  @keyframes fall {
    0% { transform: translateY(0) rotate(0deg); }
    100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
  }
</style>
</head>
<body>

<div class="video-container">
  <div class="title">🎉 Happy Birthday! 🎉</div>
  <div class="message">Wishing you a fantastic day filled with fun and surprises!</div>
</div>

<!-- Confetti effect -->
<div class="confetti" id="confetti"></div>

<script>
  // Generate confetti pieces randomly
  const confettiContainer = document.getElementById('confetti');
  for(let i=0; i<100; i++) {
    const confetti = document.createElement('div');
    confetti.className = 'confetti-piece';
    confetti.style.left = Math.random() * 100 + '%';
    confetti.style.top = '-10px';
    confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 70%, 60%)`;
    confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
    confetti.style.animationDelay = `${Math.random() * 2}s`;
    confetti.style.width = confetti.style.height = (Math.random() * 4 + 4) + 'px';
    confettiContainer.appendChild(confetti);
  }
</script>

</body>
</html>
