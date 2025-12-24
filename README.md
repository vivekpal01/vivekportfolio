<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Neon Hacker Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    :root {
      --bg: #05060a;
      --card: #0b1020;
      --neon-green: #00ff9c;
      --neon-blue: #00cfff;
      --neon-purple: #a855f7;
      --text: #e5e7eb;
      --muted: #9ca3af;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Courier New", monospace;
    }

    body {
      background: radial-gradient(circle at top, #0b1020, var(--bg));
      color: var(--text);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* === HERO === */
    header {
      padding: 90px 20px 60px;
      text-align: center;
      animation: fadeDown 1.2s ease forwards;
    }

    header h1 {
      font-size: 3.2rem;
      color: var(--neon-green);
      text-shadow:
        0 0 10px var(--neon-green),
        0 0 25px var(--neon-green);
      margin-bottom: 10px;
    }

    header p {
      color: var(--muted);
      font-size: 1.05rem;
      letter-spacing: 1px;
    }

    /* === PROFILE IMAGE === */
    .avatar {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      margin: 0 auto 25px;
      position: relative;
      background: url("https://i.imgur.com/8Km9tLL.png") center/cover no-repeat;
      animation: float 4s ease-in-out infinite;
    }

    .avatar::after {
      content: "";
      position: absolute;
      inset: -10px;
      border-radius: 50%;
      background: linear-gradient(120deg,
        var(--neon-green),
        var(--neon-blue),
        var(--neon-purple)
      );
      filter: blur(20px);
      opacity: 0.8;
      z-index: -1;
      animation: pulse 3s ease-in-out infinite;
    }

    /* === SECTIONS === */
    section {
      max-width: 1100px;
      margin: auto;
      padding: 40px 20px 70px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 25px;
    }

    .card {
      background: linear-gradient(180deg, #0d1328, var(--card));
      border-radius: 16px;
      padding: 25px;
      border: 1px solid rgba(0,255,156,0.15);
      position: relative;
      overflow: hidden;
      opacity: 0;
      transform: translateY(30px);
      animation: reveal 0.9s ease forwards;
    }

    .card:nth-child(1){animation-delay:0.2s}
    .card:nth-child(2){animation-delay:0.4s}
    .card:nth-child(3){animation-delay:0.6s}
    .card:nth-child(4){animation-delay:0.8s}

    .card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        120deg,
        transparent,
        rgba(0,255,156,0.12),
        transparent
      );
      opacity: 0;
      transition: opacity 0.4s ease;
    }

    .card:hover::before {
      opacity: 1;
    }

    .card:hover {
      box-shadow:
        0 0 25px rgba(0,255,156,0.25),
        inset 0 0 20px rgba(0,255,156,0.15);
      transform: translateY(-6px) scale(1.02);
    }

    .card h3 {
      color: var(--neon-blue);
      margin-bottom: 10px;
    }

    .card p {
      color: var(--muted);
      line-height: 1.5;
      font-size: 0.95rem;
    }

    /* === SKILLS === */
    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 15px;
    }

    .skill {
      padding: 6px 12px;
      border-radius: 999px;
      font-size: 0.75rem;
      color: var(--neon-green);
      border: 1px solid rgba(0,255,156,0.4);
      text-shadow: 0 0 6px var(--neon-green);
    }

    footer {
      text-align: center;
      padding: 30px 20px;
      color: var(--muted);
      font-size: 0.8rem;
      opacity: 0.7;
    }

    /* === ANIMATIONS === */
    @keyframes fadeDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes reveal {
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    @keyframes pulse {
      0%,100% { opacity: 0.6; }
      50% { opacity: 1; }
    }
  </style>
</head>

<body>

  <header>
    <div class="avatar"></div>
    <h1>YOUR NAME</h1>
    <p>NEON / HACKER / GAME DEV STYLE</p>
  </header>

  <section>
    <div class="grid">
      <div class="card">
        <h3>About</h3>
        <p>Minimalist hacker-style portfolio focused on performance, visuals, and clean UI.</p>
      </div>

      <div class="card">
        <h3>Projects</h3>
        <p>Web apps, game dashboards, neon UI experiments, and interactive demos.</p>
      </div>

      <div class="card">
        <h3>Skills</h3>
        <div class="skills">
          <div class="skill">HTML</div>
          <div class="skill">CSS</div>
          <div class="skill">JavaScript</div>
          <div class="skill">UI Effects</div>
          <div class="skill">Game UI</div>
        </div>
      </div>

      <div class="card">
        <h3>Contact</h3>
        <p>
          email@domain.com<br>
          github.com/username<br>
          discord: yourname#0001
        </p>
      </div>
    </div>
  </section>

  <footer>
    © 2025 YOUR NAME — SYSTEM ONLINE
  </footer>

</body>
</html>
