<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MuK1n Studio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body, html { height: 100%; font-family: 'Segoe UI', sans-serif; }

    .hero {
      background-image: url('https://images.unsplash.com/photo-1488426862026-3ee34a7d66df');
      background-size: cover;
      background-position: center;
      position: relative;
      height: 100vh;
      color: #fff;
    }

    .overlay {
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.6);
    }

    .content {
      position: relative;
      z-index: 2;
      height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
    }

    p {
      font-size: 1.2rem;
      margin-bottom: 30px;
      opacity: 0.85;
    }

    .btn {
      padding: 12px 30px;
      background: #ffffff10;
      border: 1px solid #fff;
      border-radius: 25px;
      color: #fff;
      text-decoration: none;
      transition: all 0.3s ease;
      backdrop-filter: blur(5px);
    }

    .btn:hover {
      background: #ffffff25;
      transform: scale(1.05);
    }
  </style>
</head>
<body>
  <div class="hero">
    <div class="overlay"></div>
    <div class="content">
      <h1>MuK1n Studio</h1>
      <p>Здесь рождается музыка души</p>
      <a href="studio.html" class="btn">Войти в студию</a>
    </div>
  </div>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Твоя студия</title>
  <style>
    body {
      background-color: #111;
      color: #fff;
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
    }

    header {
      padding: 20px;
      background: #1a1a1a;
      text-align: center;
    }

    h1 {
      margin: 0;
      font-size: 2rem;
    }

    main {
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 30px;
    }

    .upload-block {
      background: #222;
      padding: 20px;
      border-radius: 10px;
    }

    input[type="file"] {
      display: block;
      margin-top: 10px;
    }

    audio, img {
      margin-top: 15px;
      max-width: 100%;
    }

    a.back {
      color: #aaa;
      text-decoration: none;
      display: block;
      margin-top: 20px;
      text-align: center;
    }

    a.back:hover {
      color: #fff;
    }
  </style>
</head>
<body>
  <header>
    <h1>Добро пожаловать в студию, брат</h1>
  </header>

  <main>
    <div class="upload-block">
      <h2>Залей трек</h2>
      <input type="file" id="musicInput" accept="audio/*" />
      <audio id="audioPlayer" controls></audio>
    </div>

    <div class="upload-block">
      <h2>Залей фото</h2>
      <input type="file" id="photoInput" accept="image/*" />
      <img id="photoPreview" src="" alt="Твоё фото здесь" />
    </div>

    <a class="back" href="index.html">← Назад на главную</a>
  </main>

  <script>
    document.getElementById('musicInput').addEventListener('change', function(e) {
      const file = e.target.files[0];
      const audio = document.getElementById('audioPlayer');
      if (file) {
        audio.src = URL.createObjectURL(file);
        audio.play();
      }
    });

    document.getElementById('photoInput').addEventListener('change', function(e) {
      const file = e.target.files[0];
      const img = document.getElementById('photoPreview');
      if (file) {
        img.src = URL.createObjectURL(file);
      }
    });
  </script>
</body>
</html>
