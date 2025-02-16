
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SONSK // NEON SYSTEM</title>
  <style>
    /* НЕОНОВИЙ ФОН */
    body {
      background: black;
      color: #00ffcc;
      font-family: "Courier New", monospace;
      text-align: center;
      overflow: hidden;
      animation: neonBg 5s infinite alternate;
      transition: background 0.3s ease-in-out;
    }

    @keyframes neonBg {
      0% {
        background: linear-gradient(45deg, #000066, #0033cc, #0066ff);
      }

      50% {
        background: linear-gradient(45deg, #0033cc, #0066ff, #000066);
      }

      100% {
        background: linear-gradient(45deg, #000066, #0033cc, #0066ff);
      }
    }

    /* ШАПКА */
    header {
      width: 100%;
      background: rgba(0, 50, 100, 0.9);
      padding: 15px 20px;
      position: fixed;
      top: 0;
      left: 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 0 20px cyan;
      z-index: 1000;
      text-transform: uppercase;
    }

    .logo {
      width: 70px;
      height: 70px;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .logo:hover {
      transform: rotateY(10deg);
      box-shadow: 0 0 25px cyan;
    }

    .nav a {
      color: white;
      text-decoration: none;
      font-size: 1.3em;
      transition: 0.3s;
      font-weight: bold;
    }

    .nav a:hover {
      text-shadow: 0 0 20px cyan;
    }

    /* ПАНЕЛЬ СТАТУСУ */
    .status-panel {
      margin: 20px auto;
      padding: 20px;
      background: rgba(0, 255, 255, 0.2);
      border-radius: 15px;
      width: 50%;
      box-shadow: 0 0 20px cyan;
      font-size: 1.3em;
      font-weight: bold;
      text-transform: uppercase;
      text-shadow: 0 0 10px cyan;
    }

    /* НЕОНОВА КНОПКА */
    .neon-button {
      background: transparent;
      border: 3px solid cyan;
      color: cyan;
      padding: 18px 36px;
      font-size: 22px;
      font-weight: bold;
      text-transform: uppercase;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 0 20px cyan;
      position: relative;
      overflow: hidden;
    }

    .neon-button:hover {
      background: cyan;
      color: black;
      box-shadow: 0 0 30px cyan;
    }

    /* МИГОТІННЯ ЕКРАНУ */
    .shock-effect {
      animation: screenFlash 0.1s infinite alternate;
    }

    @keyframes screenFlash {
      0% {
        background: black;
      }

      100% {
        background: #000066;
      }
    }

    /* ТРЕМТІННЯ */
    .shake {
      animation: shakeEffect 0.1s infinite alternate;
    }

    @keyframes shakeEffect {
      0% {
        transform: translate(2px, 2px);
      }

      100% {
        transform: translate(-2px, -2px);
      }
    }

    /* ФУТЕР */
    footer {
      background: rgba(0, 50, 100, 0.9);
      padding: 20px;
      font-size: 1em;
      box-shadow: 0 -5px 20px cyan;
      text-transform: uppercase;
    }

    .footer-links a {
      color: cyan;
      text-decoration: none;
      font-size: 1.2em;
      font-weight: bold;
      transition: 0.3s;
    }

    .footer-links a:hover {
      text-shadow: 0 0 20px cyan;
    }
  </style>
</head>

<body>

  <header>
    <img src="https://i.pinimg.com/736x/2a/f8/06/2af80672c5eb3ee8c87b4f4732b62102.jpg" alt="Логотип SONSK" class="logo">
    <nav class="nav">
      <a href="#">Головна</a>
      <a href="#">Про нас</a>
      <a href="#">Контакти</a>
    </nav>
  </header>

  <main style="margin-top: 150px;">
    <h1 class="glitch">🔓 Вхід у систему SONSK</h1>

    <div class="status-panel">
      <p>🔹 <strong>Статус сервера</strong>: <span style="color: lime;">🟢 Онлайн</span></p>
      <p>🕒 <strong>Час серверу</strong>: <span id="server-time"></span></p>
    </div>

    <button class="neon-button" onclick="activateHackMode()">⚡ АКТИВУВАТИ РОЗРЯД</button>
  </main>

  <footer>
    <p>&copy; 2025 SONSK. Усі права захищені.</p>
    <div class="footer-links">
      <a href="#">Політика конфіденційності</a>
      <a href="https://t.me/Scout_1212" target="_blank">Підтримка</a>
    </div>
  </footer>

  <script>
    // ЧАС СЕРВЕРА
    function updateServerTime() {
      const now = new Date();
      document.getElementById('server-time').innerText = now.toLocaleTimeString('uk-UA');
    }
    setInterval(updateServerTime, 1000);
    updateServerTime();
    // АКТИВАЦІЯ РОЗРЯДУ + ВІДКРИТТЯ СИЛКИ
    function activateHackMode() {
      document.body.classList.add("shock-effect");
      document.querySelector("main").classList.add("shake");
      setTimeout(() => {
        document.body.classList.remove("shock-effect");
        document.querySelector("main").classList.remove("shake");
        let telegramLink = "https://t.me/+786etnxYDlZiZmZi";
        let newTab = window.open(telegramLink, "_blank");
        // Якщо браузер заблокував відкриття нового вікна, спробувати редирект
        if (!newTab || newTab.closed || typeof newTab.closed === "undefined") {
          window.location.href = telegramLink;
        }
      }, 2000);
    }
  </script>

</body>

</html>
