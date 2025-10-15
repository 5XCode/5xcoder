<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>3D Black Animation</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      overflow: hidden;
    }
    body {
      height: 100vh;
      background: black;
      display: flex;
      justify-content: center;
      align-items: center;
      perspective: 800px;
    }
    .cube {
      position: relative;
      width: 200px;
      transform-style: preserve-3d;
      animation: rotate 6s linear infinite;
    }
    .cube div {
      position: absolute;
      width: 200px;
      height: 200px;
      background: rgba(0, 217, 255, 0.1);
      border: 2px solid #00d9ff;
      box-shadow: 0 0 20px #00d9ff;
    }
    .front  { transform: translateZ(100px); }
    .back   { transform: rotateY(180deg) translateZ(100px); }
    .right  { transform: rotateY(90deg) translateZ(100px); }
    .left   { transform: rotateY(-90deg) translateZ(100px); }
    .top    { transform: rotateX(90deg) translateZ(100px); }
    .bottom { transform: rotateX(-90deg) translateZ(100px); }

    @keyframes rotate {
      0%   { transform: rotateX(0deg) rotateY(0deg); }
      100% { transform: rotateX(360deg) rotateY(360deg); }
    }
    h1 {
      position: absolute;
      color: #00d9ff;
      font-family: 'Orbitron', sans-serif;
      font-size: 2em;
      text-shadow: 0 0 15px #00d9ff;
      bottom: 30px;
    }
  </style>
</head>
<body>
  <div class="cube">
    <div class="front"></div>
    <div class="back"></div>
    <div class="right"></div>
    <div class="left"></div>
    <div class="top"></div>
    <div class="bottom"></div>
  </div>
  <h1>5XCoder System Loading...</h1>
</body>
</html>
