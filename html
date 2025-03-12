<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate Fishing Game</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        canvas {
            background: #87CEEB;
            display: block;
        }
        #info {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.6);
            color: white;
            padding: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div id="info">Click & hold to cast. Reel in when a fish bites!</div>
    <canvas id="gameCanvas"></canvas>
    
    <script>
        const canvas = document.getElementById("gameCanvas");
        const ctx = canvas.getContext("2d");

        // Set canvas size
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        // Game variables
        let isCasting = false;
        let castPower = 0;
        let maxPower = 50;
        let castX = canvas.width / 2, castY = canvas.height - 100;
        let lureX = castX, lureY = castY;
        let fish = { x: Math.random() * canvas.width, y: canvas.height / 2, speed: 1.5, caught: false };
        let isReeling = false;
        let tension = 0;
        let maxTension = 100;
        let fishBiting = false;
        let score = 0;

        // Mouse Events
        canvas.addEventListener("mousedown", () => { 
            isCasting = true; 
            castPower = 0;
        });

        canvas.addEventListener("mouseup", () => {
            if (isCasting) {
                // Launch lure
                lureX = castX;
                lureY = castY - castPower * 5;
                isCasting = false;
                fishBiting = Math.random() < 0.5; // 50% chance of a bite
            }
        });

        document.addEventListener("keydown", (e) => {
            if (e.key === " ") isReeling = true;
        });

        document.addEventListener("keyup", (e) => {
            if (e.key === " ") isReeling = false;
        });

        function update() {
            if (isCasting) {
                castPower = Math.min(castPower + 1, maxPower);
            }

            // Fish movement
            if (!fish.caught) {
                fish.x += Math.sin(Date.now() / 500) * fish.speed;
                fish.y += Math.cos(Date.now() / 700) * fish.speed;
            }

            // Reeling mechanic
            if (isReeling && fishBiting) {
                tension += 2;
                lureY += 3;
                if (tension >= maxTension) {
                    fishBiting = false;
                    tension = 0;
                    alert("The fish escaped!");
                }
            } else if (isReeling) {
                lureY += 2;
            } else if (lureY < canvas.height - 100) {
                lureY += 1.5;
            }

            // Catching fish
            if (fishBiting && Math.abs(lureX - fish.x) < 20 && Math.abs(lureY - fish.y) < 20) {
                fish.caught = true;
                score++;
                alert("You caught a fish! Score: " + score);
                resetFish();
            }
        }

        function resetFish() {
            fish = { x: Math.random() * canvas.width, y: canvas.height / 2, speed: 1.5, caught: false };
            fishBiting = false;
            tension = 0;
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            // Draw water
            ctx.fillStyle = "#1E90FF";
            ctx.fillRect(0, canvas.height / 2, canvas.width, canvas.height / 2);

            // Draw lure
            ctx.fillStyle = "red";
            ctx.beginPath();
            ctx.arc(lureX, lureY, 5, 0, Math.PI * 2);
            ctx.fill();

            // Draw fishing line
            ctx.strokeStyle = "black";
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(castX, castY);
            ctx.lineTo(lureX, lureY);
            ctx.stroke();

            // Draw fish
            if (!fish.caught) {
                ctx.fillStyle = "orange";
                ctx.beginPath();
                ctx.arc(fish.x, fish.y, 10, 0, Math.PI * 2);
                ctx.fill();
            }

            // Draw tension bar
            if (fishBiting) {
                ctx.fillStyle = "gray";
                ctx.fillRect(20, 20, 100, 10);
                ctx.fillStyle = tension > 70 ? "red" : "green";
                ctx.fillRect(20, 20, tension, 10);
            }
        }

        function gameLoop() {
            update();
            draw();
            requestAnimationFrame(gameLoop);
        }

        gameLoop();
    </script>
</body>
</html>
