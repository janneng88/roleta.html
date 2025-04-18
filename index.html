<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rigged Roulette</title>
  <style>
    body { font-family: Arial; text-align: center; }
    canvas { margin-top: 30px; }
    #spinBtn { margin-top: 20px; padding: 10px 20px; font-size: 18px; cursor: pointer; }
    #winner { margin-top: 20px; font-size: 24px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Manipulated Roleta</h1>
  <canvas id="wheelCanvas" width="500" height="500"></canvas>
  <br><button id="spinBtn">Paikutin</button>
  <div id="winner"></div>

  <script>
    const canvas = document.getElementById("wheelCanvas");
    const ctx = canvas.getContext("2d");
    const totalPlayers = 50;
    const winnerIndex = 16;
    const names = Array.from({ length: totalPlayers }, (_, i) => "Player " + (i + 1));
    const anglePerSlice = 2 * Math.PI / totalPlayers;
    const colors = ['#FF6384', '#36A2EB', '#FFCE56', '#4BC0C0', '#9966FF', '#FF9F40'];

    function drawWheel() {
      for (let i = 0; i < totalPlayers; i++) {
        const angle = i * anglePerSlice;
        ctx.beginPath();
        ctx.moveTo(250, 250);
        ctx.arc(250, 250, 200, angle, angle + anglePerSlice);
        ctx.fillStyle = colors[i % colors.length];
        ctx.fill();
        ctx.save();
        ctx.translate(250, 250);
        ctx.rotate(angle + anglePerSlice / 2);
        ctx.textAlign = "right";
        ctx.fillStyle = "#000";
        ctx.font = "12px Arial";
        ctx.fillText(names[i], 190, 5);
        ctx.restore();
      }
    }

    drawWheel();

    let angle = 0;
    let spinning = false;

    document.getElementById("spinBtn").addEventListener("click", () => {
      if (spinning) return;
      spinning = true;

      const extraSpins = 5;
      const stopAngle = (totalPlayers - winnerIndex) * anglePerSlice;
      const finalAngle = extraSpins * 2 * Math.PI + stopAngle + (Math.random() * 0.05 - 0.025);

      const duration = 5000;
      const start = performance.now();

      function animateWheel(timestamp) {
        const progress = Math.min((timestamp - start) / duration, 1);
        angle = finalAngle * easeOutCubic(progress);
        drawRotatedWheel(angle);
        if (progress < 1) {
          requestAnimationFrame(animateWheel);
        } else {
          document.getElementById("winner").textContent = "Panalo: " + names[winnerIndex];
          spinning = false;
        }
      }

      requestAnimationFrame(animateWheel);
    });

    function drawRotatedWheel(rot) {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.save();
      ctx.translate(250, 250);
      ctx.rotate(rot);
      ctx.translate(-250, -250);
      drawWheel();
      ctx.restore();
      ctx.beginPath();
      ctx.moveTo(250, 10);
      ctx.lineTo(240, 30);
      ctx.lineTo(260, 30);
      ctx.fillStyle = "red";
      ctx.fill();
    }

    function easeOutCubic(t) {
      return 1 - Math.pow(1 - t, 3);
    }
  </script>
</body>
</html>
