<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JOYBOY | Le Roi des Pirates 👑🏴‍☠️</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #0a192f;
      color: #1a2c3e;
      line-height: 1.5;
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    /* Vagues animées */
    .waves-container {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 150px;
      z-index: 0;
      pointer-events: none;
    }

    .waves {
      position: relative;
      width: 100%;
      height: 100%;
    }

    .parallax > use {
      animation: moveWaves 25s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
    }

    .parallax > use:nth-child(1) {
      animation-delay: -2s;
      animation-duration: 7s;
    }
    .parallax > use:nth-child(2) {
      animation-delay: -3s;
      animation-duration: 10s;
    }
    .parallax > use:nth-child(3) {
      animation-delay: -4s;
      animation-duration: 13s;
    }
    .parallax > use:nth-child(4) {
      animation-delay: -5s;
      animation-duration: 20s;
    }

    @keyframes moveWaves {
      0% {
        transform: translate3d(-90px, 0, 0);
      }
      100% {
        transform: translate3d(85px, 0, 0);
      }
    }

    .content-wrapper {
      position: relative;
      z-index: 2;
      background: rgba(10, 25, 47, 0.85);
      backdrop-filter: blur(3px);
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    .navbar {
      position: sticky;
      top: 0;
      background: rgba(10, 25, 47, 0.95);
      backdrop-filter: blur(12px);
      z-index: 100;
      border-bottom: 2px solid #ff8c42;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }

    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      max-width: 1400px;
      margin: 0 auto;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: 800;
      background: linear-gradient(135deg, #ff6b35, #ff8c42);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
    }

    .logo i {
      background: none;
      -webkit-background-clip: unset;
      color: #ff6b35;
      margin-right: 5px;
    }

    .nav-links {
      display: flex;
      gap: 2.2rem;
      align-items: center;
    }

    .nav-links a {
      text-decoration: none;
      font-weight: 600;
      color: #ffddb0;
      transition: 0.2s;
      font-size: 1rem;
    }

    .nav-links a:hover {
      color: #ff8c42;
    }

    .btn-outline-light {
      background: transparent;
      border: 2px solid #ff8c42;
      padding: 0.45rem 1.2rem;
      border-radius: 40px;
      color: #ff8c42;
      font-weight: 700;
      transition: 0.25s;
    }

    .btn-outline-light:hover {
      background: #ff8c42;
      color: #0a192f;
    }

    .hero {
      padding: 5rem 0 6rem 0;
      position: relative;
    }

    .hero-grid {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 3rem;
    }

    .hero-content {
      flex: 1.2;
    }

    .hero-content h1 {
      font-size: 3.5rem;
      font-weight: 800;
      line-height: 1.2;
      background: linear-gradient(to right, #ff8c42, #ffcc99);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 1.2rem;
    }

    .hero-content p {
      font-size: 1.2rem;
      color: #ffddb0;
      margin-bottom: 2rem;
      max-width: 90%;
    }

    .hero-stats {
      display: flex;
      gap: 2rem;
      margin-top: 1.5rem;
    }

    .stat span {
      font-size: 1.8rem;
      font-weight: 800;
      color: #ff8c42;
    }

    .stat {
      color: #ffddb0;
    }

    .hero-image {
      flex: 0.9;
      background: rgba(255, 140, 66, 0.1);
      border-radius: 2rem;
      padding: 1.5rem;
      text-align: center;
      box-shadow: 0 20px 35px -12px rgba(255,107,53,0.3);
      border: 2px solid #ff8c42;
      backdrop-filter: blur(5px);
    }

    .hero-image i {
      font-size: 9rem;
      color: #ff8c42;
      filter: drop-shadow(2px 8px 12px rgba(0,0,0,0.3));
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }

    .btn-primary {
      background: #ff6b35;
      color: white;
      border: none;
      padding: 0.9rem 2rem;
      border-radius: 40px;
      font-weight: 700;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.2s;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .btn-primary:hover {
      background: #cc5500;
      transform: translateY(-2px);
    }

    section {
      padding: 5rem 0;
    }

    .section-title {
      text-align: center;
      font-size: 2.2rem;
      font-weight: 800;
      margin-bottom: 2.5rem;
      color: #ffcc99;
    }

    .section-title i {
      color: #ff8c42;
      margin-right: 10px;
    }

    .section-sub {
      text-align: center;
      max-width: 700px;
      margin: -1rem auto 3rem auto;
      color: #ffddb0;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
    }

    .service-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 1.8rem;
      padding: 2rem 1.5rem;
      transition: all 0.25s ease;
      text-align: center;
      border: 1px solid rgba(255, 140, 66, 0.3);
    }

    .service-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 20px 30px -12px rgba(255,107,53,0.4);
      border-color: #ff8c42;
      background: rgba(255, 140, 66, 0.15);
    }

    .service-icon {
      font-size: 2.8rem;
      background: rgba(255, 140, 66, 0.2);
      width: 70px;
      height: 70px;
      line-height: 70px;
      border-radius: 30px;
      margin: 0 auto 1.2rem auto;
      color: #ff8c42;
    }

    .service-card h3 {
      color: #ffcc99;
    }

    .service-card p {
      color: #ffddb0;
    }

    .testimonials {
      background: rgba(0, 0, 0, 0.3);
    }

    .testimonial-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
    }

    .testimonial-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 1.5rem;
      padding: 1.8rem;
      max-width: 350px;
      flex: 1;
      border-left: 4px solid #ff8c42;
    }

    .testimonial-card i.fa-quote-left {
      color: #ff8c42;
      font-size: 1.8rem;
      margin-bottom: 0.6rem;
    }

    .testimonial-text {
      font-style: normal;
      font-weight: 400;
      margin: 1rem 0;
      color: #ffddb0;
    }

    .client-name {
      font-weight: 700;
      margin-top: 1rem;
      color: #ff8c42;
    }

    .contact-form {
      max-width: 700px;
      margin: 0 auto;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 2rem;
      padding: 2.5rem;
      border: 1px solid rgba(255, 140, 66, 0.3);
    }

    .form-group {
      margin-bottom: 1.3rem;
    }

    input, textarea {
      width: 100%;
      padding: 1rem 1.2rem;
      border-radius: 60px;
      border: 1px solid #ff8c42;
      font-family: inherit;
      font-size: 1rem;
      transition: 0.2s;
      background: rgba(10, 25, 47, 0.8);
      color: #ffddb0;
    }

    textarea {
      border-radius: 28px;
      resize: vertical;
    }

    input:focus, textarea:focus {
      outline: none;
      border-color: #ffcc99;
      box-shadow: 0 0 0 3px rgba(255,140,66,0.3);
    }

    .btn-submit {
      background: #ff6b35;
      width: 100%;
      border: none;
      padding: 1rem;
      border-radius: 60px;
      font-weight: 700;
      color: white;
      font-size: 1rem;
      cursor: pointer;
      transition: 0.2s;
    }

    .btn-submit:hover {
      background: #cc5500;
    }

    .form-feedback {
      margin-top: 1rem;
      font-weight: 500;
      text-align: center;
      color: #ffcc99;
    }

    .counter-section {
      background: rgba(0, 0, 0, 0.4);
      text-align: center;
    }

    .counter-display {
      font-size: 3.2rem;
      font-weight: 800;
      color: #ff8c42;
    }

    /* Section vidéo */
    .video-section {
      padding: 4rem 0;
      background: linear-gradient(145deg, #0a192f, #020c1a);
    }

    .video-container {
      border-radius: 20px;
      overflow: hidden;
      border: 3px solid #ff8c42;
      box-shadow: 0 20px 40px rgba(255,107,53,0.3);
      background: black;
    }

    .video-caption {
      text-align: center;
      margin-top: 1.5rem;
      color: #ffddb0;
      font-style: italic;
    }

    footer {
      background: #061220;
      color: #ffddb0;
      padding: 2.5rem 0;
      text-align: center;
    }

    .social-icons a {
      color: #ffb870;
      margin: 0 0.8rem;
      font-size: 1.4rem;
      transition: 0.2s;
      display: inline-block;
    }

    .social-icons a:hover {
      color: #ff8c42;
      transform: scale(1.1);
    }

    .music-control {
      position: fixed;
      bottom: 20px;
      left: 20px;
      z-index: 1000;
      background: #ff6b35;
      border: none;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      cursor: pointer;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
      transition: 0.2s;
    }

    .music-control:hover {
      transform: scale(1.1);
      background: #cc5500;
    }

    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(18px);}
      100% { opacity: 1; transform: translateY(0);}
    }

    .fade-up {
      animation: fadeUp 0.6s ease forwards;
    }

    @media (max-width: 800px) {
      .nav-container {
        flex-direction: column;
        gap: 0.8rem;
      }
      .hero-content h1 {
        font-size: 2.4rem;
      }
      .container {
        padding: 0 1.3rem;
      }
      .hero-stats {
        flex-wrap: wrap;
      }
    }

    .service-card, .testimonial-card, .hero-content, .hero-image, .contact-form {
      opacity: 0;
    }
  </style>
</head>
<body>

<!-- Vagues animées SVG -->
<div class="waves-container">
  <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
    viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
    <defs>
      <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
    </defs>
    <g class="parallax">
      <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(255,140,66,0.3)" />
      <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(255,107,53,0.2)" />
      <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(255,140,66,0.15)" />
      <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(10,25,47,0.4)" />
    </g>
  </svg>
</div>

<!-- Contrôle musique -->
<button class="music-control" id="musicToggleBtn">
  <i class="fas fa-music" id="musicIcon"></i>
</button>

<div class="content-wrapper">
  <nav class="navbar">
    <div class="nav-container">
      <div class="logo"><i class="fas fa-crown"></i> JOYBOY Studio</div>
      <div class="nav-links">
        <a href="#accueil"><i class="fas fa-home"></i> Accueil</a>
        <a href="#services"><i class="fas fa-skull-crossbones"></i> Services</a>
        <a href="#temoignages"><i class="fas fa-comments"></i> Équipage</a>
        <a href="#contact"><i class="fas fa-paper-plane"></i> Contact</a>
        <a href="#" id="demoInteractBtn" class="btn-outline-light"><i class="fas fa-magic"></i> Gomu Gomu !</a>
      </div>
    </div>
  </nav>

  <main>
    <section id="accueil" class="hero">
      <div class="container hero-grid">
        <div class="hero-content">
          <h1>⚓ JOYBOY ⚓<br>Le Futur Roi des Pirates</h1>
          <p>👒 "Je vais devenir le Roi des Pirates !" - Monkey D. Luffy 👒<br>Embarquez pour une aventure digitale légendaire.</p>
          <button class="btn-primary" id="exploreBtn"><i class="fas fa-ship"></i> Voguer vers l'aventure →</button>
          <div class="hero-stats">
            <div class="stat"><span>1,000,000+</span><br>Berrys dépensés</div>
            <div class="stat"><span>100%</span><br>Volonté du D.</div>
            <div class="stat"><span>∞</span><br>Rêves infinis</div>
          </div>
        </div>
        <div class="hero-image">
          <i class="fas fa-hat-wizard"></i>
          <p style="margin-top: 1rem; font-weight: 700; color:#ff8c42;">👒 Chapeau de paille 👒</p>
        </div>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <h2 class="section-title"><i class="fas fa-skull-crossbones"></i> Nos Pouvoirs du Fruit du Démon</h2>
        <p class="section-sub">Des compétences sur mesure pour conquérir le Grand Line du web.</p>
        <div class="services-grid" id="servicesGrid"></div>
      </div>
    </section>

    <!-- SECTION VIDÉO ÉPIQUE DE LUFFY - LE VOID -->
    <section class="video-section">
      <div class="container">
        <h2 class="section-title" style="text-align: center;">
          <i class="fas fa-crown"></i> 🔥 LE RÉVEIL DE JOYBOY 🔥
        </h2>
        <p style="text-align: center; color: #ff8c42; margin-bottom: 2rem; font-size: 1.3rem; font-weight: bold;">
          <i class="fas fa-fist-raised"></i> "Je vais devenir le Roi des Pirates !" <i class="fas fa-fist-raised"></i>
        </p>
        <div class="video-container">
          <video width="100%" controls autoplay loop muted>
            <source src="luffy-void.mp4" type="video/mp4">
            Votre navigateur ne supporte pas la vidéo.
          </video>
        </div>
        <p class="video-caption">
          🏴‍☠️ Le moment où la légende s'est éveillée... Le Void du Roi des Pirates 🏴‍☠️
        </p>
      </div>
    </section>

    <section id="temoignages" class="testimonials">
      <div class="container">
        <h2 class="section-title"><i class="fas fa-users"></i> L'Équipage du Chapeau de Paille</h2>
        <p class="section-sub">Ceux qui ont cru en la légende JOYBOY.</p>
        <div class="testimonial-grid" id="testimonialGrid"></div>
      </div>
    </section>

    <section class="counter-section">
      <div class="container">
        <h2 class="section-title" style="font-size:1.8rem;"><i class="fas fa-heart"></i> Puissance du Roi</h2>
        <p style="margin-bottom: 1rem; color:#ffddb0;">Cliquez pour libérer le Haki du Conquérant ! 👊</p>
        <div class="counter-display" id="liveCounter">0</div>
        <button id="incrementCounterBtn" class="btn-primary" style="margin-top: 0.7rem; background:#ff6b35;"><i class="fas fa-fist-raised"></i> Gomu Gomu no... PISTOLET</button>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <h2 class="section-title"><i class="fas fa-envelope"></i> Envoyez une Vivre Card</h2>
        <p class="section-sub">Un projet, une alliance ? Écrivons la prochaine ère ensemble.</p>
        <div class="contact-form">
          <form id="contactForm">
            <div class="form-group">
              <input type="text" id="name" placeholder="Votre nom de pirate" required>
            </div>
            <div class="form-group">
              <input type="email" id="email" placeholder="Adresse email (Poneglyphe secret)" required>
            </div>
            <div class="form-group">
              <textarea rows="3" id="message" placeholder="Votre message au Roi des Pirates..."></textarea>
            </div>
            <button type="submit" class="btn-submit"><i class="fas fa-paper-plane"></i> Envoyer la Vivre Card</button>
            <div class="form-feedback" id="formFeedback"></div>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="social-icons">
        <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="https://github.com/JOYBOY" aria-label="Github"><i class="fab fa-github"></i></a>
      </div>
      <p style="margin-top: 1.5rem;">🏴‍☠️ © 2025 JOYBOY Studio — La Volonté du D. guide nos créations. 🏴‍☠️</p>
      <p style="font-size:0.8rem; margin-top:0.5rem;"><i class="fas fa-hat-wizard"></i> "Le Roi des Pirates ? C'est celui qui est le plus libre !"</p>
    </div>
  </footer>
</div>

<script>
  // Musique et voix
  let backgroundMusic = null;
  let isPlaying = false;
  const musicBtn = document.getElementById('musicToggleBtn');
  const musicIcon = document.getElementById('musicIcon');

  function initMusic() {
    backgroundMusic = new Audio('https://cdn.pixabay.com/download/audio/2022/05/16/audio_0c6e5b6f6c.mp3?filename=epic-adventure-148031.mp3');
    backgroundMusic.loop = true;
    backgroundMusic.volume = 0.3;
  }

  function playLuffyQuote() {
    const utterance = new SpeechSynthesisUtterance("Je vais devenir le Roi des Pirates !");
    utterance.lang = 'fr-FR';
    utterance.rate = 0.9;
    utterance.pitch = 1.1;
    window.speechSynthesis.cancel();
    window.speechSynthesis.speak(utterance);
  }

  function toggleMusic() {
    if (!backgroundMusic) {
      initMusic();
    }
    if (isPlaying) {
      backgroundMusic.pause();
      musicIcon.className = 'fas fa-music';
      isPlaying = false;
    } else {
      backgroundMusic.play().catch(e => console.log('Click again to play music'));
      musicIcon.className = 'fas fa-stop';
      isPlaying = true;
      setTimeout(() => { playLuffyQuote(); }, 500);
    }
  }

  if (musicBtn) {
    musicBtn.addEventListener('click', toggleMusic);
  }

  const servicesData = [
    { icon: "fas fa-globe-americas", title: "Sites Légendaires", desc: "Naviguez avec des designs réactifs dignes du Thousand Sunny." },
    { icon: "fas fa-crown", title: "Identité de Roi", desc: "Logos et chartes avec le Haki du Roi." },
    { icon: "fas fa-chart-line", title: "Grand Line Analytics", desc: "Stratégie data pour trouver le One Piece." },
    { icon: "fas fa-fist-raised", title: "Gear Fifth Tech", desc: "Applications web surpuissantes, UI explosive." }
  ];

  const testimonialsData = [
    { quote: "Grâce à JOYBOY Studio, je vais devenir le Roi des Pirates !", author: "Monkey D. Luffy" },
    { quote: "Un travail digne du meilleur sabreur. Code précis, design tranchant.", author: "Roronoa Zoro" },
    { quote: "Les cartes sont incroyables. Le site de notre île est devenu légendaire.", author: "Nami" }
  ];

  function buildServices() {
    const container = document.getElementById('servicesGrid');
    if(!container) return;
    container.innerHTML = '';
    servicesData.forEach(service => {
      const card = document.createElement('div');
      card.className = 'service-card';
      card.innerHTML = `
        <div class="service-icon"><i class="${service.icon}"></i></div>
        <h3 style="margin-bottom: 0.7rem;">${service.title}</h3>
        <p>${service.desc}</p>
      `;
      container.appendChild(card);
    });
  }

  function buildTestimonials() {
    const container = document.getElementById('testimonialGrid');
    if(!container) return;
    container.innerHTML = '';
    testimonialsData.forEach(t => {
      const card = document.createElement('div');
      card.className = 'testimonial-card';
      card.innerHTML = `
        <i class="fas fa-quote-left"></i>
        <p class="testimonial-text">"${t.quote}"</p>
        <div class="client-name">— ${t.author}</div>
      `;
      container.appendChild(card);
    });
  }

  let likeCount = 0;
  const counterDisplay = document.getElementById('liveCounter');
  const incrementBtn = document.getElementById('incrementCounterBtn');
  
  function updateCounterUI() {
    if(counterDisplay) counterDisplay.innerText = likeCount;
  }
  
  if(incrementBtn) {
    incrementBtn.addEventListener('click', () => {
      likeCount++;
      updateCounterUI();
      incrementBtn.style.transform = 'scale(0.95)';
      setTimeout(() => { if(incrementBtn) incrementBtn.style.transform = ''; }, 120);
      const roar = document.createElement('div');
      roar.innerHTML = '💥 GOMU GOMU NO... PISTOLET 💥';
      roar.style.position = 'fixed';
      roar.style.top = '40%';
      roar.style.left = '50%';
      roar.style.transform = 'translate(-50%, -50%)';
      roar.style.background = '#ff6b35';
      roar.style.color = 'white';
      roar.style.padding = '1rem 2rem';
      roar.style.borderRadius = '60px';
      roar.style.fontWeight = 'bold';
      roar.style.zIndex = '1000';
      roar.style.fontSize = '1.5rem';
      roar.style.boxShadow = '0 0 30px rgba(0,0,0,0.5)';
      document.body.appendChild(roar);
      setTimeout(() => roar.remove(), 800);
      playLuffyQuote();
    });
  }
  
  const contactForm = document.getElementById('contactForm');
  const feedbackDiv = document.getElementById('formFeedback');
  
  if(contactForm) {
    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('name')?.value.trim();
      const email = document.getElementById('email')?.value.trim();
      const message = document.getElementById('message')?.value.trim();
      
      if(!name || !email || !message) {
        feedbackDiv.innerHTML = '<span style="color:#ff8c42;">❌ Remplis tous les champs, moussaillon !</span>';
        return;
      }
      if(!email.includes('@') || !email.includes('.')) {
        feedbackDiv.innerHTML = '<span style="color:#ff8c42;">📧 Ton email ressemble à un Poneglyphe illisible !</span>';
        return;
      }
      feedbackDiv.innerHTML = '<span style="color:#ff8c42;">✅ Merci '+ name +' ! Ta Vivre Card est en route vers Joy Boy !</span>';
      contactForm.reset();
      setTimeout(() => {
        if(feedbackDiv) feedbackDiv.innerHTML = '';
      }, 4000);
    });
  }
  
  const exploreBtn = document.getElementById('exploreBtn');
  if(exploreBtn) {
    exploreBtn.addEventListener('click', () => {
      const servicesSection = document.getElementById('services');
      if(servicesSection) {
        servicesSection.scrollIntoView({ behavior: 'smooth' });
      }
      playLuffyQuote();
    });
  }
  
  const demoBtn = document.getElementById('demoInteractBtn');
  if(demoBtn) {
    demoBtn.addEventListener('click', (e) => {
      e.preventDefault();
      likeCount += 5;
      updateCounterUI();
      const toast = document.createElement('div');
      toast.innerHTML = '🔥 HAKI DU CONQUÉRANT ! +5 en puissance 🔥';
      toast.style.position = 'fixed';
      toast.style.bottom = '30px';
      toast.style.right = '20px';
      toast.style.backgroundColor = '#ff6b35';
      toast.style.color = 'white';
      toast.style.padding = '12px 20px';
      toast.style.borderRadius = '40px';
      toast.style.fontWeight = 'bold';
      toast.style.zIndex = '1000';
      toast.style.boxShadow = '0 6px 14px rgba(0,0,0,0.3)';
      document.body.appendChild(toast);
      setTimeout(() => { toast.remove(); }, 2200);
      if(counterDisplay) {
        counterDisplay.style.transform = 'scale(1.2)';
        setTimeout(() => { if(counterDisplay) counterDisplay.style.transform = ''; }, 200);
      }
      playLuffyQuote();
    });
  }
  
  document.addEventListener('DOMContentLoaded', () => {
    buildServices();
    buildTestimonials();
    likeCount = 56;
    updateCounterUI();
    
    const fadeElements = document.querySelectorAll('.service-card, .testimonial-card, .hero-content, .hero-image, .contact-form');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.classList.add('fade-up');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1 });
    
    fadeElements.forEach(el => observer.observe(el));
    
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        const targetId = this.getAttribute('href');
        if(targetId === "#" || targetId === "") return;
        const targetElem = document.querySelector(targetId);
        if(targetElem) {
          e.preventDefault();
          targetElem.scrollIntoView({ behavior: 'smooth' });
        }
      });
    });
  });
</script>
</body>
</html>
