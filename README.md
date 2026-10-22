<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>온라인 2인용 바둑</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      background-color: #f4f4f9;
      margin: 0;
      padding: 20px;
    }
    h1 { color: #333; }
    #status {
      font-size: 1.2rem;
      font-weight: bold;
      margin-bottom: 15px;
      color: #2c3e50;
    }
    #board-container {
      position: relative;
      background-color: #e2b06f;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.2);
    }
    canvas {
      cursor: pointer;
      display: block;
    }
    .controls {
      margin-top: 15px;
      display: flex;
      gap: 10px;
    }
    button {
      padding: 10px 20px;
      font-size: 1rem;
      border: none;
      border-radius: 5px;
      background-color: #3498db;
      color: white;
      cursor: pointer;
      transition: background-color 0.2s;
    }
    button:hover { background-color: #2980b9; }
    button:disabled { background-color: #bdc3c7; cursor: not-allowed; }
  </style>

  <!-- Firebase SDK 불러오기 -->
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>
</head>
<body>

  <h1>온라인 2인용 바둑</h1>
  <div id="status">연결 중...</div>

  <div id="board-container">
    <canvas id="goBoard" width="570" height="570"></canvas>
  </div>

  <div class="controls">
    <button id="passBtn">손빼기 (Pass)</button>
    <button id="resetBtn">게임 리셋</button>
  </div>

  <script src="game.js"></script>
</body>
</html>
