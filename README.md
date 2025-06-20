<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para Mi Amor 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      width: 100%;
      height: 100%;
      font-family: 'Great Vibes', cursive;
      background: linear-gradient(135deg, #ffc0cb, #ffe4e1);
      overflow-x: hidden;
    }

    .page {
      width: 100vw;
      min-height: 100vh;
      position: absolute;
      top: 0;
      left: 100vw;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
      transition: left 1s ease-in-out;
    }

    .page.active {
      left: 0;
    }

    h1 {
      font-size: 3.5rem;
      color: #c71585;
      text-shadow: 2px 2px 5px #fff;
      word-wrap: break-word;
    }

    p {
      font-size: 1.6rem;
      color: #800040;
      max-width: 90%;
      margin-top: 1.2rem;
      line-height: 1.5;
      word-wrap: break-word;
    }

    button {
      margin-top: 2rem;
      padding: 1rem 2.5rem;
      font-size: 1.2rem;
      background: #ff69b4;
      color: white;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: background 0.3s;
    }

    button:hover {
      background: #ff1493;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 10s infinite ease-in;
      opacity: 0.6;
      z-index: -1;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      top: 0;
      left: -10px;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
      }
    }

    /* Ajustes para celulares pequeños */
    @media (max-width: 768px) {
      h1 {
        font-size: 2.2rem;
      }

      p {
        font-size: 1.1rem;
        line-height: 1.4;
      }

      button {
        font-size: 1rem;
        padding: 0.8rem 1.8rem;
      }
    }

    /* Ajustes para celulares MUY pequeños (menos de 400px) */
    @media (max-width: 400px) {
      h1 {
        font-size: 1.9rem;
      }

      p {
        font-size: 1rem;
      }

      button {
        font-size: 0.9rem;
        padding: 0.7rem 1.4rem;
      }
    }
  </style>
</head>
<body>

  <!-- Páginas -->
  <div class="page active" id="page1">
    <h1>Hola mi niña 💌</h1>
    <p>Hoy quiero regalarte algo especial… una pequeña carta hecha con todo mi corazón, solo para ti.</p>
    <button onclick="nextPage()">Ver más</button>
  </div>

  <div class="page" id="page2">
    <h1>Gracias por existir 💖</h1>
    <p>Gracias por estar a mi lado, por hacerme feliz, por aguantarme y simplemente por existir. Me haces la persona más feliz del mundo. Me encanta cómo eres, tus defectos que te hacen única, tu sonrisa, tus ojos hermosos... pero sobre todo, me encantas tú.</p>
    <button onclick="nextPage()">Siguiente</button>
  </div>

  <div class="page" id="page3">
    <h1>Siempre juntos 💘</h1>
    <p>Tal vez no soy el mejor novio, pero cada día me esfuerzo por darte lo mejor de mí. Estoy orgulloso de ti, de todo lo que logras. Prometo cuidarte, respetarte y amarte todos los días de nuestras vidas. Eres mi todo. 🖤</p>
    <button onclick="nextPage()">Última</button>
  </div>

  <div class="page" id="page4">
    <h1>Te amo 💞</h1>
    <p>Siempre te amaré, más allá del tiempo y la vida. Eres el lugar favorito de mi corazón. Quiero que seas mi último amor. Nunca olvides que este loco te ama inefablemente. Mi amor por ti es eterno. ❤</p>
    <button onclick="restart()">Volver a leer</button>
  </div>

  <!-- Corazones flotantes -->
  <script>
    const totalHearts = 30;
    for (let i = 0; i < totalHearts; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (5 + Math.random() * 5) + 's';
      heart.style.opacity = Math.random();
      document.body.appendChild(heart);
    }

    let currentPage = 1;
    function nextPage() {
      document.getElementById(page${currentPage}).classList.remove('active');
      currentPage++;
      document.getElementById(page${currentPage}).classList.add('active');
    }

    function restart() {
      document.getElementById(page${currentPage}).classList.remove('active');
      currentPage = 1;
      document.getElementById(page${currentPage}).classList.add('active');
    }
  </script>

</body>
</html>
