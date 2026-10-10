<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Live Digital Clock</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #0f172a;
      color: #38bdf8;
      margin: 0;
    }
    .clock {
      font-size: 3rem;
      font-weight: bold;
      background: #1e293b;
      padding: 1.5rem 3rem;
      border-radius: 12px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
      letter-spacing: 2px;
    }
  </style>
</head>
<body>

  <div class="clock" id="liveClock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      const timeString = now.toLocaleTimeString();
      document.getElementById('liveClock').textContent = timeString;
    }
    
    // Har 1 second baad clock update hogi
    setInterval(updateClock, 1000);
    updateClock(); // Initial call taaki foran show ho
  </script>

</body>
</html>