<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kapd el az Érmét!</title>
    <!-- A Telegram Mini App szkriptje -->
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        /* CSS Stílusok */
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            color: #333;
            text-align: center;
        }
        #game-area {
            width: 90vw;
            height: 60vh;
            max-width: 400px;
            border: 2px solid #333;
            position: relative;
            background-color: #fff;
            overflow: hidden; /* Ne lógjon ki az érme */
        }
        #coin {
            width: 50px;
            height: 50px;
            background-color: gold;
            border-radius: 50%;
            border: 2px solid darkorange;
            position: absolute;
            cursor: pointer;
            transition: all 0.1s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
            display: none; /* Kezdetben rejtett */
        }
        #coin:active {
            transform: scale(0.9);
        }
        .info-panel {
            font-size: 24px;
            margin: 15px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin-top: 20px;
            border-radius: 8px;
            border: none;
            background-color: #0088cc;
            color: white;
            cursor: pointer;
        }
        #send-score-button {
            background-color: #28a745;
            display: none; /* Kezdetben rejtett */
        }
    </style>
</head>
<body>

    <h1>Kapd el az Érmét!</h1>
    
    <div class="info-panel">
        Pontszám: <span id="score">0</span> | Idő: <span id="time">30</span>s
    </div>

    <div id="game-area">
        <div id="coin"></div>
    </div>

    <button id="start-button">Játék Indítása</button>
    <button id="send-score-button">Pontszám elküldése</button>

    <script>
        // JavaScript Logika

        // 1. Elemek elérése a DOM-ból
        const gameArea = document.getElementById('game-area');
        const coin = document.getElementById('coin');
        const scoreDisplay = document.getElementById('score');
        const timeLeftDisplay = document.getElementById('time');
        const startButton = document.getElementById('start-button');
        const sendScoreButton = document.getElementById('send-score-button');

        // 2. Játék állapotát tároló változók
        let score = 0;
        let timeLeft = 30;
        let gameInterval = null;
        let isGameRunning = false;

        // 3. Függvények
        function moveCoin() {
            const gameAreaWidth = gameArea.clientWidth;
            const gameAreaHeight = gameArea.clientHeight;
            
            // Véletlenszerű pozíció a játéktéren belül
            const randomX = Math.floor(Math.random() * (gameAreaWidth - 50)); // 50 az érme szélessége
            const randomY = Math.floor(Math.random() * (gameAreaHeight - 50)); // 50 az érme magassága

            coin.style.left = randomX + 'px';
            coin.style.top = randomY + 'px';
        }

        function startGame() {
            if (isGameRunning) return; // Ne induljon el újra, ha már fut

            // Alaphelyzetbe állítás
            isGameRunning = true;
            score = 0;
            timeLeft = 30;
            scoreDisplay.textContent = score;
            timeLeftDisplay.textContent = timeLeft;

            startButton.style.display = 'none';
            sendScoreButton.style.display = 'none';
            coin.style.display = 'block';
            
            moveCoin();

            // Időzítő indítása
            gameInterval = setInterval(() => {
                timeLeft--;
                timeLeftDisplay.textContent = timeLeft;

                if (timeLeft <= 0) {
                    endGame();
                }
            }, 1000);
        }

        function endGame() {
            clearInterval(gameInterval); // Időzítő leállítása
            isGameRunning = false;
            coin.style.display = 'none';
            alert('Játék vége! A pontszámod: ' + score);
            
            startButton.style.display = 'inline-block';
            // Csak akkor mutatjuk a pontszám küldése gombot, ha van pont
            if (score > 0) {
                sendScoreButton.style.display = 'inline-block';
            }
        }

        function onCoinClick() {
            if (!isGameRunning) return;
            score++;
            scoreDisplay.textContent = score;
            moveCoin();
        }

        function sendScore() {
            // Ez a kulcs! Adatküldés a botnak.
            const dataToSend = JSON.stringify({ score: score });
            Telegram.WebApp.sendData(dataToSend);
        }

        // 4. Eseménykezelők
        startButton.addEventListener('click', startGame);
        coin.addEventListener('click', onCoinClick);
        sendScoreButton.addEventListener('click', sendScore);
        
        // Jelzés a Telegram appnak, hogy a Mini App betöltődött és kész.
        Telegram.WebApp.ready();
    </script>
</body>
</html>
