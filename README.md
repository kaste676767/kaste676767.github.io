<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>exodus</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
      background: #050505;
      color: #eaeaea;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      border-bottom: 1px solid #111;
    }

    .logo {
      font-size: 20px;
      font-weight: 600;
      color: #a855f7;
      letter-spacing: 0.5px;
    }

    .cta {
      text-decoration: none;
      background: #a855f7;
      color: white;
      padding: 10px 18px;
      border-radius: 8px;
      font-size: 14px;
      transition: 0.2s;
    }

    .cta:hover {
      background: #9333ea;
    }

    .hero {
      padding: 120px 20px 80px;
      text-align: center;
      max-width: 900px;
      margin: auto;
    }

    .hero h1 {
      font-size: 48px;
      font-weight: 600;
      margin-bottom: 15px;
    }

    .hero h1 span {
      color: #a855f7;
    }

    .hero p {
      color: #9ca3af;
      font-size: 18px;
      margin-bottom: 35px;
    }

    .hero .main-btn {
      text-decoration: none;
      background: #a855f7;
      color: white;
      padding: 14px 28px;
      border-radius: 10px;
      font-size: 16px;
      transition: 0.2s;
    }

    .hero .main-btn:hover {
      background: #9333ea;
    }

    .section {
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .card {
      background: #0b0b0b;
      border: 1px solid #141414;
      border-radius: 12px;
      padding: 20px;
    }

    .card h3 {
      margin-bottom: 10px;
      font-size: 16px;
      color: #c084fc;
    }

    .card p {
      color: #9ca3af;
      font-size: 14px;
      line-height: 1.5;
    }

    footer {
      text-align: center;
      padding: 30px;
      color: #666;
      font-size: 14px;
      border-top: 1px solid #111;
    }
  </style>
</head>

<body>

<header>
  <div class="logo">exodus</div>
  <!-- replace link -->
  <a class="cta" href="https://discord.gg/Q5qShnsEJH" target="_blank">join</a>
</header>

<section class="hero">
  <h1><span>exodus</span> gives you the edge</h1>
  <p>fast, stable, and built for people who don’t want limits</p>

  <a class="main-btn" href="https://discord.gg/Q5qShnsEJH" target="_blank">
    get access
  </a>
</section>

<section class="section">
  <div class="grid">
    <div class="card">
      <h3>performance</h3>
      <p>runs clean and fast without unnecessary load or clutter</p>
    </div>

    <div class="card">
      <h3>stability</h3>
      <p>consistent behavior across updates and long sessions</p>
    </div>

    <div class="card">
      <h3>support</h3>
      <p>active help and updates through the community</p>
    </div>
  </div>
</section>

<footer>
  © 2026 exodus
</footer>

</body>
</html>
