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
