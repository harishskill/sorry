<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>I'm Sorry, Mahigill 💌</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@300;400;700&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --rose:      #E8587A;
      --rose-soft: #F2A0B4;
      --blush:     #FDE8EE;
      --cream:     #FFF7F9;
      --deep:      #2C1A22;
      --muted:     #8C5A6C;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--cream);
      color: var(--deep);
      font-family: 'Lato', sans-serif;
      overflow-x: hidden;
    }

    /* ── FLOATING PETALS ── */
    .petals { position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden; }
    .petal {
      position: absolute;
      top: -40px;
      font-size: 1.4rem;
      animation: fall linear infinite;
      opacity: 0.55;
    }
    @keyframes fall {
      to { transform: translateY(110vh) rotate(360deg); }
    }

    /* ── HERO ── */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 3rem 2rem;
      background: radial-gradient(ellipse at 50% 0%, #fcd6e2 0%, var(--cream) 70%);
      z-index: 1;
    }

    .hero__eyebrow {
      font-family: 'Lato', sans-serif;
      font-size: 0.75rem;
      letter-spacing: 0.28em;
      text-transform: uppercase;
      color: var(--rose);
      margin-bottom: 1.4rem;
      animation: fadeUp 1s ease both;
    }

    .hero__name {
      font-family: 'Playfair Display', serif;
      font-size: clamp(3.2rem, 10vw, 7rem);
      font-weight: 700;
      line-height: 1.05;
      color: var(--deep);
      animation: fadeUp 1s 0.15s ease both;
    }

    .hero__name span { color: var(--rose); font-style: italic; }

    .hero__sub {
      margin-top: 1.6rem;
      font-size: 1.15rem;
      font-weight: 300;
      color: var(--muted);
      max-width: 480px;
      line-height: 1.7;
      animation: fadeUp 1s 0.3s ease both;
    }

    .hero__heart {
      margin-top: 2.8rem;
      font-size: 3rem;
      animation: heartbeat 1.4s ease-in-out infinite, fadeUp 1s 0.45s ease both;
    }
    @keyframes heartbeat {
      0%,100% { transform: scale(1); }
      14%      { transform: scale(1.3); }
      28%      { transform: scale(1); }
      42%      { transform: scale(1.2); }
      70%      { transform: scale(1); }
    }

    .scroll-hint {
      position: absolute;
      bottom: 2.5rem;
      font-size: 0.78rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--rose-soft);
      animation: bounce 2s ease-in-out infinite;
    }
    @keyframes bounce {
      0%,100% { transform: translateY(0); }
      50%      { transform: translateY(8px); }
    }

    /* ── LETTER SECTION ── */
    .letter-wrap {
      position: relative;
      z-index: 1;
      padding: 5rem 1.5rem 4rem;
      display: flex;
      justify-content: center;
    }

    .letter {
      background: #fff;
      border-radius: 3px;
      max-width: 680px;
      width: 100%;
      padding: 3.5rem 3.5rem 4rem;
      box-shadow: 0 4px 40px rgba(232,88,122,0.10), 0 1px 6px rgba(232,88,122,0.06);
      position: relative;
      border-top: 5px solid var(--rose);
    }

    .letter::before {
      content: '❝';
      font-family: 'Playfair Display', serif;
      font-size: 6rem;
      color: var(--blush);
      position: absolute;
      top: 1.5rem;
      left: 2rem;
      line-height: 1;
      pointer-events: none;
    }

    .letter__date {
      font-size: 0.78rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 1.8rem;
      padding-left: 0.2rem;
    }

    .letter__greeting {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem;
      font-style: italic;
      color: var(--rose);
      margin-bottom: 1.5rem;
    }

    .letter p {
      font-size: 1.05rem;
      line-height: 1.9;
      color: #3d2630;
      margin-bottom: 1.3rem;
      font-weight: 300;
    }

    .letter__sign {
      margin-top: 2.5rem;
      font-family: 'Playfair Display', serif;
      font-size: 1.4rem;
      font-style: italic;
      color: var(--deep);
    }

    .letter__sign small {
      display: block;
      font-family: 'Lato', sans-serif;
      font-style: normal;
      font-size: 0.78rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
      margin-top: 0.4rem;
    }

    /* ── PROMISES ── */
    .promises {
      position: relative; z-index: 1;
      background: var(--blush);
      padding: 5rem 2rem;
      text-align: center;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.8rem, 5vw, 2.8rem);
      color: var(--deep);
      margin-bottom: 0.6rem;
    }
    .section-title span { color: var(--rose); font-style: italic; }
    .section-sub {
      font-size: 0.9rem;
      color: var(--muted);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 3rem;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.4rem;
      max-width: 860px;
      margin: 0 auto;
    }

    .card {
      background: #fff;
      border-radius: 4px;
      padding: 2rem 1.6rem;
      box-shadow: 0 2px 18px rgba(232,88,122,0.08);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
    }
    .card:hover { transform: translateY(-5px); box-shadow: 0 8px 28px rgba(232,88,122,0.16); }

    .card__icon { font-size: 2.2rem; margin-bottom: 1rem; }
    .card__title {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem;
      color: var(--deep);
      margin-bottom: 0.6rem;
    }
    .card__text {
      font-size: 0.92rem;
      color: var(--muted);
      line-height: 1.7;
      font-weight: 300;
    }

    /* ── FORGIVENESS BUTTON ── */
    .cta {
      position: relative; z-index: 1;
      padding: 5rem 2rem 7rem;
      text-align: center;
    }

    .cta p {
      font-size: 1rem;
      color: var(--muted);
      margin-bottom: 2.5rem;
      font-weight: 300;
      letter-spacing: 0.04em;
    }

    .btn-forgive {
      display: inline-block;
      background: var(--rose);
      color: #fff;
      font-family: 'Lato', sans-serif;
      font-size: 1.05rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      border: none;
      cursor: pointer;
      padding: 1.1rem 3.2rem;
      border-radius: 2px;
      transition: background 0.2s, transform 0.2s;
      box-shadow: 0 4px 20px rgba(232,88,122,0.35);
      position: relative;
    }
    .btn-forgive:hover { background: #c73f60; transform: scale(1.04); }
    .btn-forgive:active { transform: scale(0.98); }

    /* ── CELEBRATION OVERLAY ── */
    #celebration {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(253,232,238,0.96);
      z-index: 999;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem;
      animation: fadeIn 0.5s ease;
    }
    #celebration.show { display: flex; }

    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

    #celebration h2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.2rem, 8vw, 4.5rem);
      color: var(--rose);
      margin-bottom: 1rem;
      animation: fadeUp 0.7s 0.2s ease both;
    }
    #celebration p {
      font-size: 1.2rem;
      color: var(--muted);
      max-width: 420px;
      font-weight: 300;
      line-height: 1.8;
      animation: fadeUp 0.7s 0.4s ease both;
    }
    #celebration .big-hearts {
      font-size: 4rem;
      margin: 1.5rem 0;
      animation: fadeUp 0.7s 0.1s ease both, heartbeat 1.4s 1s ease-in-out infinite;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(22px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 600px) {
      .letter { padding: 2.5rem 1.8rem 3rem; }
      .letter::before { font-size: 4rem; }
    }
  </style>
</head>
<body>

<!-- Floating petals -->
<div class="petals" id="petals"></div>

<!-- ── HERO ── -->
<section class="hero">
  <p class="hero__eyebrow">A message from the heart</p>
  <h1 class="hero__name">Dear <span>Mahigill</span>,</h1>
  <p class="hero__sub">I messed up. And I know that "sorry" alone isn't enough — but I mean every single word that follows.</p>
  <div class="hero__heart">💗</div>
  <p class="scroll-hint">↓ keep reading ↓</p>
</section>

<!-- ── LETTER ── -->
<section class="letter-wrap">
  <article class="letter">
    <p class="letter__date">June 2026 &nbsp;·&nbsp; Written with love &amp; regret</p>
    <p class="letter__greeting">My dearest Mahigill,</p>

    <p>
      There are moments in life when you realize, too late, that you let something precious slip through your hands — and this is one of them. I hurt you, and there is no excuse in the world that could undo what happened.
    </p>
    <p>
      You deserve someone who always chooses you, who thinks before speaking, and who treats your heart with the gentleness it deserves. I failed to be that person in that moment, and I am deeply, truly sorry.
    </p>
    <p>
      Every laugh we've shared, every quiet moment, every inside joke — they remind me of how lucky I am to have you in my life. The thought of losing you hurts more than anything I can put into words.
    </p>
    <p>
      I don't ask for forgiveness because I deserve it. I ask because I love you, because I want to do better, and because you are worth every effort I can give.
    </p>
    <p>
      This isn't just a sorry — it's a promise to grow, to listen, and to be the person who matches your kindness every single day.
    </p>

    <div class="letter__sign">
      Yours, always 💌
      <small>with all the love I have</small>
    </div>
  </article>
</section>

<!-- ── PROMISES ── -->
<section class="promises">
  <h2 class="section-title">My <span>Promises</span> to You</h2>
  <p class="section-sub">Because actions speak louder</p>

  <div class="cards">
    <div class="card">
      <div class="card__icon">👂</div>
      <h3 class="card__title">I will listen</h3>
      <p class="card__text">Really listen — not just wait for my turn to speak. Your feelings matter and I will honour them.</p>
    </div>
    <div class="card">
      <div class="card__icon">🤝</div>
      <h3 class="card__title">I will be honest</h3>
      <p class="card__text">No more half-truths or silence when it counts. You deserve full honesty, always.</p>
    </div>
    <div class="card">
      <div class="card__icon">🌷</div>
      <h3 class="card__title">I will cherish you</h3>
      <p class="card__text">Every day, in small ways and big ones, I'll remind you how much you mean to me.</p>
    </div>
    <div class="card">
      <div class="card__icon">🛡️</div>
      <h3 class="card__title">I will protect your peace</h3>
      <p class="card__text">I never want to be the reason your day is harder. I'll choose your peace over my pride.</p>
    </div>
  </div>
</section>

<!-- ── CTA ── -->
<section class="cta">
  <p>Only when you're ready, Mahigill — no pressure, no rush. 🌸</p>
  <button class="btn-forgive" onclick="celebrate()">
    I forgive you 💕
  </button>
</section>

<!-- ── CELEBRATION ── -->
<div id="celebration">
  <div class="big-hearts">💖</div>
  <h2>Thank you, Mahigill! 🎉</h2>
  <p>You just made me the happiest person alive. I promise to spend every day proving I deserve this second chance. I love you so much. 🌹</p>
</div>

<script>
  // Generate falling petals
  const petals = document.getElementById('petals');
  const emojis = ['🌸','🌺','💮','🌷','💗','🌹','✨'];
  for (let i = 0; i < 28; i++) {
    const p = document.createElement('span');
    p.classList.add('petal');
    p.textContent = emojis[Math.floor(Math.random() * emojis.length)];
    p.style.left = Math.random() * 100 + 'vw';
    p.style.fontSize = (0.9 + Math.random() * 1.2) + 'rem';
    p.style.animationDuration = (7 + Math.random() * 10) + 's';
    p.style.animationDelay = (Math.random() * 12) + 's';
    petals.appendChild(p);
  }

  function celebrate() {
    const el = document.getElementById('celebration');
    el.classList.add('show');
    // burst confetti-like extra petals
    for (let i = 0; i < 18; i++) {
      const p = document.createElement('span');
      p.classList.add('petal');
      p.textContent = ['💖','🎉','✨','🌸','💕'][Math.floor(Math.random()*5)];
      p.style.left = Math.random() * 100 + 'vw';
      p.style.fontSize = (1.2 + Math.random() * 1.5) + 'rem';
      p.style.animationDuration = (4 + Math.random() * 5) + 's';
      p.style.animationDelay = '0s';
      petals.appendChild(p);
    }
  }

  // Click overlay to close (if she changes her mind she can re-open)
  document.getElementById('celebration').addEventListener('click', function() {
    this.classList.remove('show');
  });
</script>
</body>
</html>y
