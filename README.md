# Birthday-<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday, Ivana! 🌸</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            font-family: 'Georgia', serif;
            overflow: hidden;
            position: relative;
        }
        .container {
            text-align: center;
            position: relative;
            z-index: 10;
        }
        h1 {
            font-size: 3.5em;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            margin: 0;
            animation: glow 2s ease-in-out infinite alternate;
        }
        p {
            font-size: 1.5em;
            color: #fff;
            margin: 20px 0;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }
        .flower {
            position: absolute;
            width: 20px;
            height: 20px;
            background: radial-gradient(circle, #ff69b4, #ff1493);
            border-radius: 50% 0 50% 0;
            animation: bloom 4s infinite ease-in-out;
        }
        .flower::before, .flower::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: radial-gradient(circle, #ffb6c1, #ff69b4);
            border-radius: 50% 0 50% 0;
            transform: rotate(45deg);
        }
        .flower::after {
            transform: rotate(-45deg);
            background: radial-gradient(circle, #ffc0cb, #ff1493);
        }
        .sparkle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #fff;
            border-radius: 50%;
            animation: sparkle 2s infinite linear;
        }
        @keyframes bloom {
            0%, 100% { transform: scale(0) rotate(0deg); opacity: 0; }
            50% { transform: scale(1.2) rotate(180deg); opacity: 1; }
        }
        @keyframes glow {
            from { text-shadow: 2px 2px 4px rgba(0,0,0,0.3), 0 0 20px #ff69b4; }
            to { text-shadow: 2px 2px 4px rgba(0,0,0,0.3), 0 0 30px #ff1493; }
        }
        @keyframes sparkle {
            0% { transform: scale(0) rotate(0deg); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: scale(1) rotate(180deg); opacity: 0; }
        }
        @media (max-width: 768px) {
            h1 { font-size: 2.5em; }
            p { font-size: 1.2em; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Happy Birthday, Ivana! 🌹</h1>
        <p>May your day bloom with love, joy, and endless magic, my dearest. You're the flower that lights up my world. 💕</p>
    </div>

    <script>
        // Create floating flowers
        function createFlower() {
            const flower = document.createElement('div');
            flower.className = 'flower';
            flower.style.left = Math.random() * 100 + '%';
            flower.style.top = Math.random() * 100 + '%';
            flower.style.animationDelay = Math.random() * 4 + 's';
            flower.style.animationDuration = (Math.random() * 3 + 3) + 's';
            document.body.appendChild(flower);

            // Remove after animation
            setTimeout(() => {
                flower.remove();
            }, 7000);
        }

        // Create sparkles
        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            sparkle.style.left = Math.random() * 100 + '%';
            sparkle.style.top = Math.random() * 100 + '%';
            sparkle.style.animationDelay = Math.random() * 2 + 's';
            document.body.appendChild(sparkle);

            setTimeout(() => {
                sparkle.remove();
            }, 2000);
        }

        // Generate flowers and sparkles continuously
        setInterval(createFlower, 500);
        setInterval(createSparkle, 300);
    </script>
</body>
</html>
