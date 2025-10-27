<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Click Game</title>
  <style>
    body { font-family: sans-serif; text-align: center; margin-top: 50px; }
    button {
      font-size: 20px; padding: 10px 20px;
      background: dodgerblue; color: white; border: none; border-radius: 8px;
    }
    button:hover { background: deepskyblue; }
  </style>
</head>
<body>
  <h1>Click the Button Game!</h1>
  <p>Score: <span id="score">0</span></p>
  <button id="clickBtn">Click me!</button>

  <script>
    let score = 0;
    const scoreDisplay = document.getElementById('score');
    const button = document.getElementById('clickBtn');

    button.addEventListener('click', () => {
      score++;
      scoreDisplay.textContent = score;
      button.style.background = `hsl(${Math.random() * 360}, 80%, 60%)`;
    });
  </script>
</body>
</html>
