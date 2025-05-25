<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para ti, Michel</title>
  <style>
    body {
      background: #ffeef2;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      overflow: hidden;
      position: relative;
    }

    .carta {
      background: white;
      padding: 40px;
      max-width: 600px;
      margin: 100px auto;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      text-align: center;
      position: relative;
      z-index: 2;
      animation: fadeIn 2s ease-out;
    }

    h1 {
      color: #d6336c;
      animation: slideDown 1.2s ease-out;
    }

    p {
      color: #444;
      font-size: 18px;
      line-height: 1.6;
      animation: fadeInText 2s ease-out;
    }

    .firma {
      margin-top: 30px;
      font-style: italic;
      color: #666;
    }

    /* Animaciones */
    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes slideDown {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInText {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* Corazones animados */
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 10s linear infinite;
      opacity: 0.6;
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
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <!-- Corazones flotando -->
  <script>
    for (let i = 0; i < 20; i++) {
      let heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (5 + Math.random() * 5) + "s";
      document.body.appendChild(heart);
    }
  </script>

  <div class="carta">
    <h1>Para ti, Michel</h1>
    <p>
      Amor mío,<br><br>
      Quiero que sepas cuánto significas para mí. Cada día a tu lado es un regalo,
      una bendición que agradezco con todo mi corazón. Tu sonrisa ilumina mi mundo
      y tu amor me hace sentir la persona más afortunada del universo.<br><br>
      Gracias por estar conmigo, por tu paciencia, tu ternura y tu infinita belleza,
      por dentro y por fuera. Te amo más de lo que las palabras pueden decir.
    </p>
    <div class="firma">
      Con todo mi amor,<br>
      Alex
    </div>
  </div>

  <!-- Música: I Wanna Be Yours -->
  <div style="text-align:center; margin-bottom: 50px;">
    <iframe width="300" height="200" src="https://www.youtube.com/embed/NYxqD1cBn1k?autoplay=0"
      title="I Wanna Be Yours - Arctic Monkeys"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
    </iframe>
  </div>

</body>
</html>
