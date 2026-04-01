# alexhearn
Personal Website
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Alex Hearn</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

```
:root {
  --white:   #FFFFFF;
  --off:     #F7F5F2;
  --black:   #0A0A0A;
  --dark:    #111111;
  --mid:     #888888;
  --border:  #E2DDD8;
  --accent:  #C4922A;
}

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--white);
  color: var(--black);
  overflow-x: hidden;
}

/* ─── NAV ─── */
nav {
  position: fixed; top: 0; left: 0; right: 0;
  z-index: 300;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.6rem 3.5rem;
  background: rgba(255,255,255,0.96);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border);
}
.nav-wordmark {
  font-family: 'DM Serif Display', serif;
  font-size: 1.05rem;
  font-weight: 400;
  letter-spacing: 0.06em;
  color: var(--black);
  text-decoration: none;
}
.nav-links { display: flex; gap: 2.8rem; list-style: none; }
.nav-links a {
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--mid);
  text-decoration: none;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--black); }

/* ─── HERO ─── */
.hero {
  padding-top: 80px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: var(--white);
  position: relative;
  overflow: hidden;
}

.hero-top {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 5rem 3.5rem 3rem;
  position: relative;
}

.hero-kicker {
  font-size: 0.58rem;
  font-weight: 500;
  letter-spacing: 0.42em;
  text-transform: uppercase;
  color: var(--mid);
  margin-bottom: 2.5rem;
  opacity: 0;
  animation: up 0.9s 0.2s forwards;
}

.hero-name {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(5rem, 12vw, 14rem);
  line-height: 0.88;
  font-weight: 400;
  color: var(--black);
  opacity: 0;
  animation: up 0.9s 0.35s forwards;
}
.hero-name em {
  display: block;
  font-style: italic;
  color: var(--accent);
}

.hero-bottom {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  padding: 2.5rem 3.5rem;
  border-top: 1px solid var(--border);
  opacity: 0;
  animation: up 0.9s 0.55s forwards;
}
.hero-tagline {
  font-size: 0.78rem;
  font-weight: 300;
  letter-spacing: 0.05em;
  color: var(--mid);
  line-height: 1.8;
  max-width: 320px;
}
.hero-tagline strong { color: var(--black); font-weight: 500; }

.hero-cta {
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  font-size: 0.6rem;
  font-weight: 500;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: var(--white);
  background: var(--black);
  text-decoration: none;
  padding: 1rem 2.2rem;
  transition: background 0.3s;
}
.hero-cta:hover { background: var(--accent); }

/* ─── TICKER ─── */
.ticker-wrap {
  background: var(--black);
  padding: 1rem 0;
  overflow: hidden;
  white-space: nowrap;
}
.ticker-track {
  display: inline-flex;
  gap: 0;
  animation: ticker 28s linear infinite;
}
.ticker-track span {
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.32em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.55);
  padding: 0 3rem;
}
.ticker-track span.dot {
  color: var(--accent);
  padding: 0;
  letter-spacing: 0;
}
@keyframes ticker {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}

/* ─── INTRO ─── */
.intro {
  padding: 7rem 3.5rem;
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 5rem;
  align-items: start;
  background: var(--white);
  border-bottom: 1px solid var(--border);
}
.intro-left {
  position: sticky;
  top: 100px;
}
.section-tag {
  font-size: 0.56rem;
  font-weight: 500;
  letter-spacing: 0.42em;
  text-transform: uppercase;
  color: var(--mid);
  margin-bottom: 1rem;
}
.intro-left h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2rem, 3.5vw, 3.2rem);
  font-weight: 400;
  line-height: 1.15;
  color: var(--black);
}
.intro-left h2 em { font-style: italic; color: var(--accent); }

.intro-right {}
.intro-body {
  font-size: 1.05rem;
  font-weight: 300;
  line-height: 1.9;
  color: #444;
  margin-bottom: 2rem;
}
.intro-body strong { color: var(--black); font-weight: 500; }

.intro-large {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(1.6rem, 3vw, 2.6rem);
  font-weight: 400;
  line-height: 1.3;
  color: var(--black);
  border-top: 2px solid var(--black);
  padding-top: 2.5rem;
  margin-top: 3rem;
}
.intro-large em { font-style: italic; color: var(--accent); }

/* ─── WHAT I DO ─── */
.what {
  background: var(--off);
  padding: 7rem 3.5rem;
  border-bottom: 1px solid var(--border);
}
.what-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 4.5rem;
  padding-bottom: 2.5rem;
  border-bottom: 1px solid var(--border);
}
.what-header h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.5rem, 5vw, 5rem);
  font-weight: 400;
  line-height: 1;
  color: var(--black);
}
.what-header h2 em { font-style: italic; color: var(--accent); }
.what-header p {
  font-size: 0.8rem;
  font-weight: 300;
  line-height: 1.85;
  color: var(--mid);
  max-width: 280px;
  text-align: right;
}

.what-list { list-style: none; }
.what-item {
  display: grid;
  grid-template-columns: 3rem 1fr auto;
  gap: 2rem;
  align-items: center;
  padding: 2.2rem 0;
  border-bottom: 1px solid var(--border);
  cursor: default;
  transition: padding-left 0.3s;
}
.what-item:hover { padding-left: 0.8rem; }
.what-item:first-child { border-top: 1px solid var(--border); }

.item-num {
  font-size: 0.6rem;
  font-weight: 500;
  letter-spacing: 0.2em;
  color: var(--mid);
}
.item-title {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(1.4rem, 2.5vw, 2rem);
  font-weight: 400;
  color: var(--black);
}
.item-title em { font-style: italic; color: var(--accent); }
.item-desc {
  font-size: 0.75rem;
  font-weight: 300;
  color: var(--mid);
  max-width: 300px;
  line-height: 1.8;
  text-align: right;
}

/* ─── CONNECT ─── */
.connect {
  background: var(--black);
  padding: 7rem 3.5rem;
  color: var(--white);
}
.connect-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 4rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}
.connect-header h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.5rem, 5vw, 5rem);
  font-weight: 400;
  line-height: 1;
  color: var(--white);
}
.connect-header h2 em { font-style: italic; color: var(--accent); }
.connect-header p {
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.32em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.3);
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: rgba(255,255,255,0.08);
}
.dest-card {
  display: block;
  text-decoration: none;
  background: var(--black);
  padding: 3rem 2.5rem;
  position: relative;
  overflow: hidden;
  transition: background 0.35s;
  color: var(--white);
}
.dest-card:hover { background: #1a1a1a; }
.dest-card.dim { opacity: 0.38; pointer-events: none; }

.dest-card-tag {
  font-size: 0.55rem;
  font-weight: 500;
  letter-spacing: 0.4em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 2rem;
}
.dest-card-name {
  font-family: 'DM Serif Display', serif;
  font-size: 2.2rem;
  font-weight: 400;
  color: var(--white);
  line-height: 1.1;
  margin-bottom: 1rem;
}
.dest-card-desc {
  font-size: 0.76rem;
  font-weight: 300;
  line-height: 1.9;
  color: rgba(255,255,255,0.45);
  margin-bottom: 2.5rem;
}
.dest-card-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.58rem;
  font-weight: 500;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
  transition: color 0.25s;
}
.dest-card:hover .dest-card-link { color: var(--white); }
.dest-card-link::after { content: '↗'; font-size: 0.9rem; }

/* ─── PERSONAL STRIP ─── */
.personal {
  background: var(--white);
  padding: 7rem 3.5rem;
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  gap: 7rem;
  align-items: center;
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}
.personal h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.2rem, 4vw, 4rem);
  font-weight: 400;
  line-height: 1.15;
  color: var(--black);
  margin-bottom: 2.5rem;
}
.personal h2 em { font-style: italic; color: var(--accent); }
.personal p {
  font-size: 0.9rem;
  font-weight: 300;
  line-height: 2;
  color: #555;
  margin-bottom: 1.5rem;
}
.personal p strong { color: var(--black); font-weight: 500; }

.personal-right {
  display: flex;
  flex-direction: column;
  gap: 0;
  border: 1px solid var(--border);
}
.fact {
  padding: 2rem 2.5rem;
  border-bottom: 1px solid var(--border);
}
.fact:last-child { border-bottom: none; }
.fact-num {
  font-family: 'DM Serif Display', serif;
  font-size: 2.8rem;
  font-weight: 400;
  color: var(--accent);
  line-height: 1;
  margin-bottom: 0.3rem;
}
.fact-label {
  font-size: 0.6rem;
  font-weight: 500;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--mid);
}

/* ─── CONTACT ─── */
.contact {
  background: var(--off);
  padding: 7rem 3.5rem;
  text-align: center;
  border-bottom: 1px solid var(--border);
}
.contact-tag {
  font-size: 0.58rem;
  font-weight: 500;
  letter-spacing: 0.42em;
  text-transform: uppercase;
  color: var(--mid);
  margin-bottom: 2rem;
}
.contact h2 {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(2.5rem, 6vw, 6rem);
  font-weight: 400;
  line-height: 1.05;
  color: var(--black);
  margin-bottom: 1.5rem;
}
.contact h2 em { font-style: italic; color: var(--accent); }
.contact p {
  font-size: 0.85rem;
  font-weight: 300;
  color: var(--mid);
  margin-bottom: 3rem;
}
.contact-email {
  display: inline-flex;
  align-items: center;
  gap: 0.8rem;
  font-size: 0.62rem;
  font-weight: 500;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--white);
  background: var(--black);
  text-decoration: none;
  padding: 1.1rem 2.5rem;
  transition: background 0.3s;
}
.contact-email:hover { background: var(--accent); }

/* ─── FOOTER ─── */
footer {
  background: var(--black);
  padding: 3rem 3.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.footer-wordmark {
  font-family: 'DM Serif Display', serif;
  font-size: 1rem;
  color: rgba(255,255,255,0.3);
  text-decoration: none;
  letter-spacing: 0.05em;
}
.footer-social {
  display: flex; gap: 2rem; align-items: center;
}
.footer-social a {
  font-size: 0.58rem;
  font-weight: 500;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.35);
  text-decoration: none;
  transition: color 0.2s;
}
.footer-social a:hover { color: var(--white); }
.footer-copy {
  font-size: 0.55rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.2);
}

/* ─── REVEAL ─── */
.reveal {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.8s ease, transform 0.8s ease;
}
.reveal.on { opacity: 1; transform: none; }

/* ─── KEYFRAMES ─── */
@keyframes up {
  from { opacity: 0; transform: translateY(24px); }
  to   { opacity: 1; transform: none; }
}

/* ─── MOBILE ─── */
@media (max-width: 860px) {
  nav { padding: 1.2rem 1.5rem; }
  .nav-links { display: none; }
  .hero-top { padding: 4rem 1.5rem 2.5rem; }
  .hero-bottom { flex-direction: column; align-items: flex-start; gap: 2rem; padding: 2rem 1.5rem; }
  .intro, .what, .connect, .personal, .contact, footer { padding: 5rem 1.5rem; }
  .intro { grid-template-columns: 1fr; gap: 3rem; }
  .intro-left { position: static; }
  .what-header { flex-direction: column; align-items: flex-start; gap: 1rem; }
  .what-header p { text-align: left; }
  .what-item { grid-template-columns: 2.5rem 1fr; }
  .item-desc { display: none; }
  .card-grid { grid-template-columns: 1fr; }
  .connect-header { flex-direction: column; align-items: flex-start; gap: 1rem; }
  .personal { grid-template-columns: 1fr; gap: 3.5rem; }
  footer { flex-direction: column; gap: 1.5rem; text-align: center; }
  .footer-social { flex-wrap: wrap; justify-content: center; }
}
```

  </style>
</head>
<body>

  <!-- NAV -->

  <nav>
    <a class="nav-wordmark" href="#">Alex Hearn</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#connect">Connect</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->

  <section class="hero">
    <div class="hero-top">
      <p class="hero-kicker">Nashville &nbsp;·&nbsp; Project Manager &nbsp;·&nbsp; Entrepreneur</p>
      <h1 class="hero-name">Alex<br/><em>Hearn.</em></h1>
    </div>
    <div class="hero-bottom">
      <p class="hero-tagline">
        <strong>Structured by profession.</strong><br/>
        Creative by instinct.
      </p>
      <a class="hero-cta" href="#connect">Explore my work</a>
    </div>
  </section>

  <!-- TICKER -->

  <div class="ticker-wrap" aria-hidden="true">
    <div class="ticker-track">
      <span>Project Manager</span><span class="dot">◆</span>
      <span>Brand Strategist</span><span class="dot">◆</span>
      <span>Entrepreneur</span><span class="dot">◆</span>
      <span>Creative Director</span><span class="dot">◆</span>
      <span>Builder</span><span class="dot">◆</span>
      <span>Brand7.co</span><span class="dot">◆</span>
      <span>Nashville, TN</span><span class="dot">◆</span>
      <!-- duplicate for seamless loop -->
      <span>Project Manager</span><span class="dot">◆</span>
      <span>Brand Strategist</span><span class="dot">◆</span>
      <span>Entrepreneur</span><span class="dot">◆</span>
      <span>Creative Director</span><span class="dot">◆</span>
      <span>Builder</span><span class="dot">◆</span>
      <span>Brand7.co</span><span class="dot">◆</span>
      <span>Nashville, TN</span><span class="dot">◆</span>
    </div>
  </div>

  <!-- INTRO / BELIEF -->

  <section class="intro" id="about">
    <div class="intro-left reveal">
      <p class="section-tag">Who I Am</p>
      <h2>When <em>structure meets creativity,</em> real things get built.</h2>
    </div>
    <div class="intro-right reveal">
      <p class="intro-body">
        I'm <strong>Alex Hearn</strong> — a project manager who genuinely can't stop building things. I believe the most powerful work lives at the intersection of discipline and imagination.
      </p>
      <p class="intro-body">
        By day I keep complex projects on track and teams moving forward. Every other hour, I'm running <strong>Brand7</strong>, creating, and turning ideas into reality. The toolkit is always the same: <strong>clarity, execution, and relentless follow-through.</strong>
      </p>
      <p class="intro-large">
        I specialize in<br/><em>making things happen.</em>
      </p>
    </div>
  </section>

  <!-- WHAT I DO -->

  <section class="what" id="work">
    <div class="what-header reveal">
      <h2>What I<br/><em>do best.</em></h2>
      <p>Nimble and resourceful — built to get it and get it done.</p>
    </div>
    <ul class="what-list">
      <li class="what-item reveal">
        <span class="item-num">01</span>
        <span class="item-title">Project <em>Management</em></span>
        <span class="item-desc">Keeping complex projects on track, teams aligned, and stakeholders informed — without the chaos.</span>
      </li>
      <li class="what-item reveal">
        <span class="item-num">02</span>
        <span class="item-title">Brand <em>Strategy</em></span>
        <span class="item-desc">Shaping identities and messaging through Brand7 — for businesses ready to show up with intention.</span>
      </li>
      <li class="what-item reveal">
        <span class="item-num">03</span>
        <span class="item-title">Creative <em>Direction</em></span>
        <span class="item-desc">Photography and visual storytelling that lives at the intersection of art and strategy.</span>
      </li>
      <li class="what-item reveal">
        <span class="item-num">04</span>
        <span class="item-title">Entrepreneurship &amp; <em>Building</em></span>
        <span class="item-desc">From blank page to launch — turning vision into operating reality.</span>
      </li>
    </ul>
  </section>

  <!-- CONNECT / DESTINATIONS -->

  <section class="connect" id="connect">
    <div class="connect-header reveal">
      <h2>Find me<br/><em>here.</em></h2>
      <p>Connect &amp; Explore</p>
    </div>
    <div class="card-grid">

```
  <a class="dest-card reveal" href="https://brand7.co" target="_blank" rel="noopener">
    <p class="dest-card-tag">Business</p>
    <h3 class="dest-card-name">Brand7</h3>
    <p class="dest-card-desc">Consulting, brand strategy, and creative services. If you're building something worth talking about, this is where we start.</p>
    <span class="dest-card-link">brand7.co</span>
  </a>

  <a class="dest-card reveal" href="https://www.instagram.com/brand7.co" target="_blank" rel="noopener">
    <p class="dest-card-tag">Social</p>
    <h3 class="dest-card-name">Instagram</h3>
    <p class="dest-card-desc">Behind the scenes — projects, ideas, and the ongoing experiment of building in public.</p>
    <span class="dest-card-link">@brand7.co</span>
  </a>

  <div class="dest-card dim reveal">
    <p class="dest-card-tag">Portfolio · Coming Soon</p>
    <h3 class="dest-card-name">Pixieset</h3>
    <p class="dest-card-desc">A curated portfolio of creative and visual work. This one's worth the wait.</p>
    <span class="dest-card-link">Coming Soon</span>
  </div>

</div>
```

  </section>

  <!-- PERSONAL -->

  <section class="personal">
    <div class="reveal">
      <p class="section-tag">The Person Behind It</p>
      <h2>The kind of person who<br/><em>can't just pick one thing.</em></h2>
      <p>I didn't choose between being organized and being creative — I decided both were non-negotiable. The same energy that makes me a great project manager makes me a driven entrepreneur.</p>
      <p>Whether managing a complex project, developing a brand, or working behind the lens — the goal is always the same: <strong>make something that matters.</strong></p>
    </div>
    <div class="personal-right reveal">
      <div class="fact">
        <div class="fact-num">PM</div>
        <div class="fact-label">Project Manager · By Day</div>
      </div>
      <div class="fact">
        <div class="fact-num">B7</div>
        <div class="fact-label">Brand7 · Founder &amp; Creative</div>
      </div>
      <div class="fact">
        <div class="fact-num">∞</div>
        <div class="fact-label">Builder. Always.</div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->

  <section class="contact" id="contact">
    <p class="contact-tag">Let's Partner Up</p>
    <h2>Ready to start<br/>a <em>conversation?</em></h2>
    <p>What are you trying to build? Let's figure it out.</p>
    <a class="contact-email" href="mailto:alex@brand7.co">alex@brand7.co</a>
  </section>

  <!-- FOOTER -->

  <footer>
    <a class="footer-wordmark" href="#">Alex Hearn</a>
    <div class="footer-social">
      <a href="https://brand7.co" target="_blank" rel="noopener">Brand7.co</a>
      <a href="https://www.instagram.com/brand7.co" target="_blank" rel="noopener">Instagram</a>
      <a href="mailto:alex@brand7.co">Email</a>
    </div>
    <p class="footer-copy">© 2026 Alex Hearn</p>
  </footer>

  <script>
    const els = document.querySelectorAll('.reveal');
    const io = new IntersectionObserver((entries) => {
      entries.forEach((e, i) => {
        if (e.isIntersecting) {
          setTimeout(() => e.target.classList.add('on'), i * 100);
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.08 });
    els.forEach(el => io.observe(el));
  </script>

</body>
</html>
