<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Happy Birthday!</title>
<style>
  body {
    background: linear-gradient(135deg, #f9d423, #ff4e50);
    font-family: 'Arial', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }
  .card {
    background-color: white;
    padding: 40px;
    border-radius: 15px;
    box-shadow: 0 8px 16px rgba(0,0,0,0.3);
    text-align: center;
    max-width: 500px;
  }
  h1 {
    font-size: 2.5em;
    color: #ff4e50;
    margin-bottom: 20px;
  }
  p {
    font-size: 1.2em;
    color: #333;
  }
  .balloons {
    margin-top: 30px;
  }
  .balloon {
    display: inline-block;
    width: 40px;
    height: 60px;
    margin: 0 5px;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
    background-color: #ff6f61;
    position: relative;
    animation: bounce 2s infinite;
  }
  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
  }
</style>
</head>
<body>
  <div class="card">
    <h1>Happy Birthday!</h1>
    <p>Wishing you a day filled with love, joy, and unforgettable moments. Have a fantastic year ahead!</p>
    <div class="balloons">
      <div class="balloon"></div>
      <div class="balloon"></div>
      <div class="balloon"></div>
    </div>
  </div>
</body>
</html>
