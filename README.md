
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Atelier Milesia — Graphisme & Création Vidéo</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  /* ==========================================================================
     DESIGN RESPONSIVE (MOBILE) - Ajustements stricts
     ========================================================================= */
  @media (max-width: 768px) {
    header, nav, #main-nav {
      position: relative !important;
      top: 0 !important;
      left: 0 !important;
      height: auto !important;
      min-height: auto !important;
      display: flex !important;
      flex-direction: column !important;
      align-items: center !important;
      justify-content: center !important;
      padding: 20px 0 !important;
      width: 100% !important;
      gap: 5px !important; /* Réduit pour rapprocher le logo Instagram du texte en dessous */
      z-index: 101 !important;
    }

    header img, nav img, .logo, .nav-logo img {
      max-height: 55px !important;
      height: 55px !important;
      width: auto !important;
      margin-bottom: 5px !important;
      display: block !important;
      box-shadow: none !important;
      filter: none !important;
    }

    .nav-right {
      flex-direction: column !important;
      gap: 12px !important;
      width: 100% !important;
      align-items: center !important;
    }

    nav a, #main-nav a, header a, .nav-link, .nav-instagram {
      display: block !important;
      padding: 6px 20px !important;
      font-size: 14px !important;
      text-align: center !important;
      text-decoration: none !important;
    }

    /* Réduction drastique de l'espace au-dessus de la phrase pour la rapprocher du menu/instagram */
    .hero-title {
      margin-top: 0.5rem !important; 
    }

    /* Augmentation de l'écart entre la phrase principale et le bouton En savoir plus */
    .hero-btn {
      margin-top: 3.5rem !important;
    }

    /* Changement de la couleur de fond de la zone d'accueil pour correspondre à la seconde section */
    .hero {
      background: var(--beige-bg) !important;
    }

    .grid, .container, .about-inner {
      display: flex !important;
      flex-direction: column !important;
      width: 100% !important;
      padding: 20px !important;
      box-sizing: border-box !important;
      gap: 2rem !important;
    }

    .home-scrolling-wrapper {
      height: 220px !important;
    }
    .home-scrolling-wrapper .portfolio-item {
      width: 220px !important;
      height: 220px !important;
    }

    .services-banner-container {
      width: 100vw !important;
      margin-left: -3rem !important;
      margin-right: -3rem !important;
      left: 0 !important;
      position: relative !important;
      margin-bottom: 2.5rem !important;
      margin-top: -3rem !important;
    }
    /* Descente de l'image de fond pour un meilleur cadrage */
    .services-banner {
      width: 100% !important;
      min-height: 320px !important;
      max-height: 400px !important;
      object-position: 50% 25% !important;
    }
    .services-banner-title-container {
      top: 10% !important;
    }
    /* Ajustement du conteneur pour afficher la phrase complète sur plusieurs lignes */
    .services-banner-sub-container {
      bottom: 8% !important; 
      padding: 12px !important;
      box-sizing: border-box !important;
      width: 92% !important;
      left: 4% !important;
      background: rgba(42, 37, 32, 0.55) !important; /* Encadré transparent assombri pour lisibilité */
      border: 1px solid rgba(255, 255, 255, 0.2) !important;
    }
    .banner-sub-text {
      text-align: center !important;
      font-size: 13px !important; 
      white-space: normal !important; /* Permet le retour à la ligne pour bien cadrer */
      color: #ffffff !important; /* Force la phrase en blanc */
      line-height: 1.4 !important;
    }

    .portfolio-grid {
      display: flex !important;
      flex-direction: column !important;
      gap: 2rem !important;
      padding: 0 !important;
    }
    .portfolio-grid .portfolio-item {
      width: 100% !important;
      aspect-ratio: 1 / 1 !important;
    }

    button, .btn, .submit-btn, .target-btn {
      margin: 10px auto !important;
      display: block !important;
    }

    .contact-page, #page-portfolio section {
      margin-top: 0 !important;
    }
    
    .contact-page.success-active {
      min-height: auto !important;
      padding-bottom: 5rem !important;
    }
  }

  /* ==========================================================================
     DESIGN ORDINATEUR / BASE GÉNÉRALE
     ========================================================================= */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --beige: #c8bfaf;
    --beige-light: #e8e3dc;
    --beige-bg: #ddd8d0;
    --dark: #2a2520;
    --rouge: #8b2635;
    --white: #f5f2ee;
    --text: #3a3530;
    --text-muted: #7a736a;
    --font-serif: 'Cormorant Garamond', Georgia, serif;
    --font-sans: 'Jost', sans-serif;
  }
  html { scroll-behavior: smooth; overflow-x: hidden; }
  body {
    font-family: var(--font-sans);
    background: var(--beige-bg);
    color: var(--text);
    min-height: 100vh;
    font-weight: 300;
    letter-spacing: 0.02em;
    overflow-x: hidden;
  }
  .page { 
    display: none; 
    min-height: 100vh; 
    flex-direction: column;
  }
  .page.active { 
    display: flex;
  }
  .main-content {
    position: relative;
    z-index: 2;
    background: var(--beige-bg);
    box-shadow: 0 20px 30px rgba(0,0,0,0.15);
    flex-grow: 1;
  }
  #page-home .main-content, #page-mentions .main-content {
    background: var(--white);
  }
  footer { 
    background: var(--dark); 
    color: var(--beige-light); 
    padding: 5rem 3rem 3rem 3rem; 
    text-align: center;
    position: sticky;
    bottom: 0;
    left: 0;
    width: 100%;
    z-index: 1;
  }
  .footer-links {
    margin-top: 1rem;
    display: flex;
    justify-content: center;
    gap: 1.5rem;
  }
  .footer-link-btn {
    background: transparent;
    border: none;
    color: var(--text-muted);
    font-family: var(--font-sans);
    font-size: 0.8rem;
    letter-spacing: 0.05em;
    cursor: pointer;
    text-decoration: underline;
    transition: color 0.2s;
  }
  .footer-link-btn:hover { color: var(--white); }
  
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 3rem;
    transition: background 0.4s;
  }
  nav.scrolled { background: rgba(200,191,175,0.95); backdrop-filter: blur(8px); }
  .nav-logo { display: flex; align-items: center; }
  .nav-logo img { height: 150px; width: auto; object-fit: contain; cursor: pointer; transition: none; }
  .nav-right { display: flex; align-items: center; gap: 2rem; }
  .nav-link, .nav-instagram {
    font-family: var(--font-sans);
    font-weight: 400;
    font-size: 0.85rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--white);
    text-decoration: none;
    cursor: pointer;
    transition: opacity 0.2s;
  }
  .nav-link:hover, .nav-instagram:hover { opacity: 0.7; }
  .nav-link.dark, .nav-instagram.dark { color: var(--dark); }
  
  .hero {
    min-height: 100vh;
    background: #c2b8aa; 
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 8rem 2rem 4rem 2rem;
  }
  .hero-title {
    font-family: var(--font-serif);
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 400;
    font-style: italic;
    letter-spacing: -0.03em;
    color: var(--white);
    line-height: 1.25;
    max-width: 900px;
    padding: 0 2rem;
    text-shadow: 0 1px 3px rgba(0,0,0,0.15);
    margin-top: 9rem;
  }
  .hero-btn {
    display: inline-block;
    margin-top: 7.5rem;
    padding: 1rem 2.5rem;
    border: 1.5px solid var(--rouge);
    color: var(--rouge);
    font-family: var(--font-sans);
    font-size: 0.85rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    cursor: pointer;
    background: transparent;
    transition: background 0.3s, color 0.3s;
  }
  .hero-btn:hover { background: var(--rouge); color: var(--white); }
  
  section { padding: 5rem 3rem; }
  .section-title {
    font-family: var(--font-serif);
    font-size: 2.5rem;
    font-weight: 300;
    color: var(--dark);
    margin-bottom: 1.5rem;
    text-align: center;
  }
  
  .services-banner-container { 
    width: 100vw; 
    margin-left: -3rem; 
    margin-top: 0;
    margin-bottom: 3rem; 
    overflow: hidden; 
    position: relative; 
  }
  .services-banner { 
    width: 100%; 
    height: 100vh; 
    max-height: 850px; 
    min-height: 550px; 
    object-fit: cover; 
    object-position: top;
    display: block; 
  }
  .services-banner-title-container {
    position: absolute;
    top: 20%; left: 5%; width: 90%;
    color: var(--white); font-family: var(--font-serif); text-align: center;
    z-index: 10;
  }
  .banner-main-title { font-size: clamp(3rem, 6vw, 4.5rem); font-weight: 300; text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2); }
  
  .services-banner-sub-container {
    position: absolute;
    bottom: 60%; 
    left: 0; 
    width: 100%; 
    max-width: none;
    filter: drop-shadow(0px 4px 10px rgba(0, 0, 0, 0.5));
    background: rgba(42, 37, 32, 0.063); 
    padding: 15px 25px;                 
    border-radius: 0;                   
    backdrop-filter: blur(3px);         
  }
  .banner-sub-text {
    font-family: var(--font-sans);
    font-weight: 400;
    font-size: 1.15rem; 
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--white);
    text-align: center;
    text-shadow: 0 2px 15px rgba(0, 0, 0, 0.45);
    white-space: nowrap; 
  }
  
  .target-section { text-align: center; margin: 4rem 0 0 0; }
  .target-title { font-family: var(--font-serif); font-size: 2rem; font-weight: 300; color: var(--dark); margin-bottom: 2rem; }
  .target-buttons { display: flex; justify-content: center; gap: 1.5rem; flex-wrap: wrap; }
  .target-btn {
    padding: 0.8rem 2rem; border: 1px solid var(--dark); color: var(--dark); background: transparent;
    font-family: var(--font-sans); font-size: 1.05rem; letter-spacing: 0.05em; text-transform: uppercase;
    transition: all 0.3s; cursor: pointer;
  }
  .target-btn:hover { background: var(--dark); color: var(--white); }
  
  .services-text-layout {
    max-width: 800px; margin: 6rem auto 0 auto; display: flex; flex-direction: column; gap: 4rem;
  }
  .service-text-block { text-align: center; padding-bottom: 3.5rem; border-bottom: 1px solid rgba(42, 37, 32, 0.15); }
  .service-text-block:last-child { border-bottom: none; }
  .service-title-serif { font-family: var(--font-serif); font-size: 2.2rem; font-weight: 400; font-style: italic; color: var(--dark); margin-bottom: 1rem; letter-spacing: -0.01em; }
  .service-text-desc { font-family: var(--font-sans); font-size: 1rem; color: var(--text-muted); line-height: 1.8; max-width: 600px; margin: 0 auto; }
  
  .home-scrolling-wrapper { display: flex; width: max-content; animation: scrollGallery 30s linear infinite; }
  .home-scrolling-wrapper .portfolio-item { width: 40vw; height: 450px; flex-shrink: 0; background: var(--white); display: flex; align-items: center; justify-content: center; overflow: hidden; }
  .home-scrolling-wrapper .portfolio-item img { width: 100%; height: 100%; object-fit: cover; }
  @keyframes scrollGallery { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
  
  #page-portfolio section {
    margin-top: 6rem;
  }
  .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 2rem; max-width: 1200px; margin: 0 auto; }
  .portfolio-grid .portfolio-item { background: var(--beige-light); aspect-ratio: 1 / 1; overflow: hidden; position: relative; cursor: pointer; }
  .portfolio-grid .portfolio-item img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.5s ease; }
  .portfolio-grid .portfolio-item:hover img { transform: scale(1.05); }
  .portfolio-overlay {
    position: absolute; top: 0; left: 0; right: 0; bottom: 0; background: rgba(245, 242, 238, 0.8);
    display: flex; align-items: center; justify-content: center; padding: 1.5rem; text-align: center; opacity: 0; pointer-events: none; transition: opacity 0.3s ease;
  }
  .portfolio-item:hover .portfolio-overlay { opacity: 1; }
  .portfolio-overlay span { font-family: var(--font-serif); font-size: 1.3rem; color: var(--dark); font-style: italic; line-height: 1.4; }
  
  .modal-overlay { position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(42, 37, 32, 0.6); backdrop-filter: blur(4px); z-index: 1000; display: none; align-items: center; justify-content: center; padding: 2rem; }
  .modal-overlay.open { display: flex; }
  .modal-content { background: var(--white); padding: 3rem; max-width: 700px; width: 100%; max-height: 85vh; overflow-y: auto; position: relative; box-shadow: 0 15px 40px rgba(0,0,0,0.15); animation: fadeInModal 0.4s ease; }
  @keyframes fadeInModal { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }
  .modal-close { position: absolute; top: 1.5rem; right: 1.5rem; background: transparent; border: none; font-size: 1.5rem; color: var(--dark); cursor: pointer; }
  
  /* Titres des modals alignés au milieu */
  .modal-title { font-family: var(--font-serif); font-size: 1.6rem; color: var(--dark); margin-bottom: 1.5rem; padding-bottom: 0.5rem; text-align: center; }
  .modal-subtitle { font-family: var(--font-sans); font-weight: 500; font-size: 0.95rem; text-transform: uppercase; color: var(--dark); margin-bottom: 0.8rem; letter-spacing: 0.05em; }
  
  .modal-section-divider { border: none; border-top: 1px solid rgba(42, 37, 32, 0.15); margin: 1.5rem 0; }
  .modal-desc-text { font-size: 1rem; color: var(--text); line-height: 1.6; margin-bottom: 0.4rem; text-align: left; }
  .modal-list { list-style-type: none; padding-left: 0; }
  .modal-list li { font-size: 1rem; color: var(--text); line-height: 1.6; margin-bottom: 0.4rem; position: relative; padding-left: 1.2rem; }
  .modal-list li::before { content: "•"; position: absolute; left: 0; color: var(--rouge); font-size: 1.1rem; top: -1px; }

  .about-inner { max-width: 1000px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
  .about-img-box { background: var(--beige-light); aspect-ratio: 3/4; display: flex; align-items: center; justify-content: center; overflow: hidden; cursor: pointer; }
  .about-img-box img { width: 100%; height: 100%; object-fit: cover; }
  .about-text h2 { font-family: var(--font-serif); font-size: 2.2rem; font-weight: 300; color: var(--dark); margin-bottom: 1.5rem; line-height: 1.3; }
  .about-text p { font-size: 0.9rem; color: var(--text-muted); line-height: 1.9; margin-bottom: 1.2rem; }
  
  .mentions-inner { max-width: 800px; margin: 0 auto; padding: 0 1rem; }
  .mentions-title-line { font-family: var(--font-serif); font-size: clamp(2rem, 4vw, 2.5rem); font-weight: 300; color: var(--dark); margin-bottom: 3rem; text-align: left; white-space: nowrap; }
  .mentions-text-block { margin-bottom: 2.5rem; }
  .mentions-text-block h3 { font-family: var(--font-sans); font-weight: 500; color: var(--dark); text-transform: uppercase; font-size: 1rem; letter-spacing: 0.05em; margin-bottom: 1rem; border-bottom: 1px solid rgba(42, 37, 32, 0.15); padding-bottom: 0.5rem; }
  .mentions-text-block p { font-size: 0.95rem; color: var(--text); line-height: 1.8; margin-bottom: 1rem; }

  .email-link { color: var(--dark) !important; text-decoration: underline; }

  /* ==========================================================================
     MODIFICATIONS FORMULAIRE : ÉCRITURES ET AFFICHAGE FINAL ALIGNÉ
     ========================================================================= */
  .contact-page { padding: 4rem 3rem 5rem; margin-top: 12rem; }
  .contact-page.success-active { min-height: calc(100vh - 12rem); display: flex; align-items: center; justify-content: center; padding-bottom: 10rem; }
  .contact-inner { max-width: 850px; margin: 0 auto; width: 100%; }
  .contact-title { font-family: var(--font-serif); font-size: 3.2rem; font-weight: 300; color: var(--dark); margin-bottom: 0.5rem; }
  .contact-intro { font-family: var(--font-sans); font-size: 1.1rem; color: var(--text-muted); line-height: 1.9; margin-bottom: 3.5rem; }
  
  .form-group { margin-bottom: 2.2rem; }
  .form-radio-group { display: flex; flex-direction: column; gap: 1rem; margin-top: 0.8rem; }
  
  .form-label { display: block; font-size: 1.1rem; letter-spacing: 0.05em; color: var(--dark); margin-bottom: 0.8rem; font-weight: 400; }
  .form-label span { color: var(--text-muted); font-weight: 300; font-size: 0.85rem; margin-left: 6px; }
  
  .form-input, .form-textarea { width: 100%; background: var(--beige-light); border: none; border-bottom: 1px solid var(--beige); padding: 1rem 0.5rem; font-family: var(--font-sans); font-size: 1.1rem; color: var(--text); outline: none; font-weight: 300; }
  .form-input:focus, .form-textarea:focus { border-bottom-color: var(--rouge); }
  .form-textarea { resize: vertical; min-height: 140px; }

  .radio-label { display: flex; align-items: center; gap: 0.8rem; font-size: 1.1rem; color: var(--text); cursor: pointer; }
  .radio-label input[type="radio"] { accent-color: var(--rouge); width: 18px; height: 18px; cursor: pointer; }
  
  .submit-btn {
    display: inline-block;
    margin-top: 2rem;
    padding: 1.2rem 3rem;
    border: 1.5px solid var(--rouge);
    color: var(--rouge);
    font-family: var(--font-sans);
    font-size: 1.05rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    text-decoration: none;
    cursor: pointer;
    background: transparent;
    transition: background 0.3s, color 0.3s;
  }
  .submit-btn:hover { background: var(--rouge); color: var(--white); }

  .discovery-block { background: var(--beige-light); padding: 2.5rem; border-radius: 4px; margin: 2.5rem 0; border-bottom: 1px solid var(--beige); }
  
  footer .footer-logo { font-family: var(--font-serif); font-size: 1.5rem; font-weight: 300; letter-spacing: 0.2em; text-transform: uppercase; margin-bottom: 1rem; color: var(--white); }
  footer p { font-size: 0.8rem; color: var(--text-muted); letter-spacing: 0.05em; }
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-thumb { background: var(--beige); }

  /* Style d'écriture identique à l'introduction du formulaire, légèrement plus grand, aéré et centré */
  .final-success-box {
    font-family: var(--font-sans);
    font-size: 1.2rem;
    color: var(--text-muted);
    line-height: 1.9;
    text-align: center;
    max-width: 700px;
    margin: 0 auto;
    animation: fadeInSuccess 0.6s ease forwards;
  }
  @keyframes fadeInSuccess {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>
</head>
<body>

<nav id="main-nav">
  <div class="nav-logo" onclick="showPage('home')">
    <img id="main-logo-img" src="image/Logo AM blanc.png" alt="Atelier Milesia Logo">
  </div>
  <div class="nav-right">
    <a class="nav-link" onclick="showPage('services')">Services</a>
    <a class="nav-link" onclick="showPage('portfolio')">Mes créations</a>
    <a class="nav-link" onclick="showPage('contact')">Contact</a>
    <a href="https://www.instagram.com/atelier.milesia/" target="_blank" class="nav-instagram">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
        <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
      </svg>
    </a>
  </div>
</nav>

<div class="page active" id="page-home">
  <div class="main-content">
    <div class="hero">
      <h1 class="hero-title">Atelier Milesia est un atelier de graphisme et de création vidéos</h1>
      <button class="hero-btn" onclick="showPage('services')">En savoir plus</button>
    </div>
    <section style="background: var(--white); padding: 0; overflow: hidden;">
      <div class="home-scrolling-wrapper" id="home-portfolio-grid"></div>
    </section>
    <section style="padding-top: 5rem; padding-bottom: 5rem;">
      <div class="about-inner">
        <div class="about-img-box" id="about-img-box" onclick="document.getElementById('about-img-input').click()">
          <img src="image/DSC05245 (1).jpg" alt="Photo">
          <input type="file" id="about-img-input" accept="image/*" style="display:none;" onchange="loadAboutImg(this)">
        </div>
        <div class="about-text">
          <h2>D’une idée, à un univers unique.</h2>
          <p>Graphiste freelance basée dans le sud de la France, j’ai fondé Atelier Milesia pour accompagner les marques et les entreprises dans la création d’identités visuelles fortes et cohérentes. Ici, chaque idée devient le point de départ d’un univers graphique singulier.</p>
          <p>Chaque projet est avant tout une rencontre : une vision à comprendre, un univers à explorer, une histoire à révéler. J’allie exigence créative et sensibilité esthétique pour imaginer des visuels qui racontent votre histoire et refléter pleinement votre identity.</p>
          <p>Aujourd’hui, mon travail s’articule autour de trois axes complémentaires : l’identité de marque, la création graphique et la production vidéo. Trois domaines qui me permettent d’offrir un accompagnement complet et cohérent, au service d’une communication claire et alignée avec vos valeurs.</p>
          <button class="hero-btn" onclick="showPage('contact')">Travaillons ensemble</button>
        </div>
      </div>
    </section>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Creation Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<div class="page" id="page-services">
  <div class="main-content">
    <section style="padding-top: 0; padding-bottom: 5rem;">
      <div class="services-banner-container">
        <img src="image/DSC05234.jpg" alt="Bannière" class="services-banner">
        <div class="services-banner-title-container">
          <div class="banner-main-title">Services</div>
        </div>
        <div class="services-banner-sub-container">
          <div class="banner-sub-text">De l'identité visuelle au contenu vidéo, chaque projet est pensé avec soin pour refléter votre univers.</div>
        </div>
      </div>
      <div class="target-section">
        <h3 class="target-title">À qui s'adressent mes services ?</h3>
        <div class="target-buttons">
          <div class="target-btn" onclick="openModal('entreprise')">Entreprise et marque</div>
          <div class="target-btn" onclick="openModal('evenementiel')">Évènementiel</div>
          <div class="target-btn" onclick="openModal('particulier')">Particulier</div>
        </div>
      </div>
      <div class="services-text-layout">
        <div class="service-text-block">
          <h4 class="service-title-serif">Identité visuelle</h4>
          <p class="service-text-desc">Création complète de votre univers graphique : logo, typographies, palette de couleurs et déclinaisons visuelles.</p>
        </div>
        <div class="service-text-block">
          <h4 class="service-title-serif">Création graphique</h4>
          <p class="service-text-desc">Flyers, dépliants, cartes de visite, brochures, affiches, menus, etc.</p>
        </div>
        <div class="service-text-block">
          <h4 class="service-title-serif">Création de site vitrine</h4>
          <p class="service-text-desc">Conception d’un site web sur mesure, ergonomique et esthétique, pensé pour refléter votre identity.</p>
        </div>
        <div class="service-text-block">
          <h4 class="service-title-serif">Réseaux sociaux</h4>
          <p class="service-text-desc">Création de contenus visuels et de vidéos courtes pour vos plateformes.</p>
        </div>
        <div class="service-text-block">
          <h4 class="service-title-serif">Création vidéo</h4>
          <p class="service-text-desc">Production et montage de vidéos sur mesure pour le web et les réseaux sociaux.</p>
        </div>
      </div>
      <div style="text-align:center; margin-top:2rem;"><button class="hero-btn" onclick="showPage('contact')">Démarrer un projet</button></div>
    </section>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Création Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<div class="modal-overlay" id="modal-entreprise" onclick="closeModal(event)">
  <div class="modal-content">
    <button class="modal-close" onclick="closeModal(event, true)">&times;</button>
    <h2 class="modal-title">Entreprise et marque</h2>
    
    <div class="modal-subtitle">Identité visuelle</div>
    <ul class="modal-list">
      <li>Création d’une identity graphique complète</li>
      <li>Définition d’une charte graphique</li>
      <li>Déclinaisons visuelles pour tous les supports de communication</li>
    </ul>

    <hr class="modal-section-divider">

    <div class="modal-subtitle">Création de logo</div>

    <hr class="modal-section-divider">

    <div class="modal-subtitle">Conception de supports professionnels</div>
    <ul class="modal-list">
      <li>Cartes de visite, dépliants, flyers, affiches</li>
      <li>Cartes cadeaux, brochures, menus, etc.</li>
    </ul>

    <hr class="modal-section-divider">

    <div class="modal-subtitle">Packagings - étiquettes</div>
    <ul class="modal-list">
      <li>Boîtes d’emballages</li>
    </ul>

    <hr class="modal-section-divider">

    <div class="modal-subtitle">Site vitrine</div>

    <hr class="modal-section-divider">

    <div class="modal-subtitle">Création de vidéos courtes</div>
    <ul class="modal-list">
      <li>Création de vidéos pour les réseaux sociaux</li>
      <li>Création de vidéos pour le web</li>
      <li>Campagnes publicitaires</li>
    </ul>
  </div>
</div>

<div class="modal-overlay" id="modal-evenementiel" onclick="closeModal(event)">
  <div class="modal-content">
    <button class="modal-close" onclick="closeModal(event, true)">&times;</button>
    <h2 class="modal-title">Évènementiel</h2>
    <div class="modal-subtitle">
      Événement professionnel ou particulier
      <div style="text-transform: uppercase; font-weight: 500; margin-top: 0.3rem;">(mariage, baptême, anniversaire, séminaire, etc…) :</div>
    </div>
    <ul class="modal-list">
      <li>Faire part</li>
      <li>Carton d’invitation</li>
      <li>Logo</li>
      <li>Affiche, flyer, etc…</li>
    </ul>
  </div>
</div>

<div class="modal-overlay" id="modal-particulier" onclick="closeModal(event)">
  <div class="modal-content">
    <button class="modal-close" onclick="closeModal(event, true)">&times;</button>
    <h2 class="modal-title">Particulier</h2>
    <p class="modal-desc-text">Création et impression personnalisée sur papier ou objet.</p>
  </div>
</div>

<div class="page" id="page-mentions">
  <div class="main-content">
    <section style="padding-top: 4rem; padding-bottom: 5rem;">
      <div class="mentions-inner">
        <h2 class="mentions-title-line">Mentions légales</h2>
        <div class="mentions-text-block">
          <h3>1. Éditeur du site</h3>
          <p>Le site internet Atelier Milesia éditée et géré par l'Atelier Milesia.</p>
          <p>Statut : Entreprise Individuelle (Freelance)<br>Activité : Graphisme, création visuelle et production vidéo.<br>Lieu d'activité : Sud de la France, Lot.<br>Contact : Via le formulaire de contact du site ou à l'adresse e-mail suivante : <a href="mailto:contact@atelier-milesia.fr" class="email-link">contact@atelier-milesia.fr</a></p>
        </div>
        <div class="mentions-text-block">
          <h3>2. Hébergement</h3>
          <p>Ce site est hébergé par Vercel.</p>
        </div>
        <div class="mentions-text-block">
          <h3>3. Propriété intellectuelle</h3>
          <p>L’ensemble des contenus de ce site (textes, photographies, logos, créations graphiques, vidéos, maquettes) constitutes une œuvre protégée par les lois en vigueur sur la propriété intellectuelle. Toute reproduction, representation, modification ou adaptation totale ou partielle des éléments du site sans accord écrit préalable est strictement interdite.</p>
        </div>
        <div class="mentions-text-block">
          <h3>4. Données personnelles</h3>
          <p>Les informations recueillies via le formulaire de contact (Nom, Prénom, E-mail, détails du projet) sont uniquement destinées au traitement de votre demande de projet par l'Atelier Milesia. Elles ne sont en aucun cas cédées ou vendues à des tiers.</p>
        </div>
        <div style="margin-top: 4rem;">
          <button class="target-btn" onclick="showPage('home')">Retour à l'accueil</button>
        </div>
      </div>
    </section>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Création Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<div class="page" id="page-portfolio">
  <div class="main-content">
    <section>
      <p class="section-title">Mes créations</p>
      <div class="portfolio-grid" id="main-portfolio-grid"></div>
    </section>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Création Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<div class="page" id="page-contact">
  <div class="main-content">
    <div class="contact-page">
      <div class="contact-inner">
        <h1 class="contact-title">Contact</h1>
        <p class="contact-intro">Que vous ayez une question, une idée de projet ou le souhait de réaliser un projet déjà établi, n'hésitez pas à me contacter.</p>
        <div>
          <div class="form-group"><label class="form-label">Nom et Prénom <span>(obligatoire)</span></label><input type="text" class="form-input" id="f-name" name="Nom_Prenom"></div>
          <div class="form-group"><label class="form-label">Nom de l'entreprise</label><input type="text" class="form-input" id="f-company" name="Nom_Entreprise"></div>
          <div class="form-group"><label class="form-label">E-mail <span>(obligatoire)</span></label><input type="email" class="form-input" id="f-email" name="Email"></div>
          <div class="form-group"><label class="form-label">Téléphone</label><input type="tel" class="form-input" id="f-phone" name="Telephone"></div>
          <div class="form-group">
            <label class="form-label">Type de projet</label>
            <div class="form-radio-group">
              <label class="radio-label"><input type="radio" name="project_type" value="identite_visuelle"> Identité visuelle</label>
              <label class="radio-label"><input type="radio" name="project_type" value="logo"> Logo</label>
              <label class="radio-label"><input type="radio" name="project_type" value="video"> Création vidéo(s)</label>
              <label class="radio-label"><input type="radio" name="project_type" value="object"> Création graphique sur objet</label>
              <label class="radio-label"><input type="radio" name="project_type" value="autre"> Autre</label>
            </div>
          </div>
          <div class="form-group"><label class="form-label">Date de début du projet</label><input type="date" class="form-input" id="f-date" name="Date_Debut" style="max-width: 250px;"></div>
          <div class="form-group"><label class="form-label">Détails du projet <span>(obligatoire)</span></label><textarea class="form-textarea" id="f-details" name="Details_Projet" rows="5"></textarea></div>
          <button class="submit-btn" id="f-submit-btn" onclick="submitForm()">Envoyer</button>
        </div>
      </div>
    </div>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Création Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<div class="page" id="page-discovery">
  <div class="main-content">
    <div class="contact-page" id="discovery-container-box">
      <div class="contact-inner">
        <div id="discovery-form-block">
          <h1 class="contact-title">Merci !</h1>
          <div class="form-group discovery-block" style="margin-top: 2rem;">
            <label class="form-label">Dernière petite question : Par quel moyen avez-vous entendu parler d'Atelier Milesia ?</label>
            <div class="form-radio-group">
              <label class="radio-label"><input type="radio" name="discovery_source" value="bouche-oreille"> Le bouche-à-oreille</label>
              <label class="radio-label"><input type="radio" name="discovery_source" value="moteurs-recherche"> Les moteurs de recherches</label>
              <label class="radio-label"><input type="radio" name="discovery_source" value="reseaux-sociaux"> Les réseaux sociaux</label>
              <label class="radio-label"><input type="radio" name="discovery_source" value="cartes-visites"> Les cartes de visites</label>
            </div>
          </div>
          <button class="submit-btn" id="f-discovery-btn" onclick="submitDiscoveryForm()">Terminer</button>
        </div>
        
        <div class="final-success-box" id="final-success-msg" style="display: none;">
          Merci pour ces informations. Votre demande de projet a bien été prise en compte et sera traitée dans les plus brefs délais. À très bientôt.
        </div>
      </div>
    </div>
  </div>
  <footer>
    <div class="footer-logo">Atelier Milesia</div>
    <p>© 2026 Atelier Milesia — Graphisme & Création Vidéo</p>
    <div class="footer-links">
      <button class="footer-link-btn" onclick="showPage('mentions')">Mentions légales</button>
    </div>
  </footer>
</div>

<script>
const portfolioImages = ["image/Carte AM1.jpg","image/Business_Card_Mockup_1.jpg","image/Free Stickers on a Bag Mockup.jpg","image/Business_Card_Mockup_2.jpg","image/Affiche1.jpg","image/Iphone zoom copie.jpg","image/lop.jpg","image/Free_Book_Mockup_1 copie.jpg","image/Poster_on_Concrete.jpg"];

function forceScrollAnimation() {
  const el = document.getElementById('home-portfolio-grid');
  if (!el) return;
  el.style.animation = 'none';
  el.offsetHeight;
  el.style.animation = 'scrollGallery 30s linear infinite';
}

function showPage(name) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + name).classList.add('active');
  window.scrollTo(0, 0);
  const nav = document.getElementById('main-nav');
  const action = (name === 'home' || name === 'mentions') ? 'remove' : 'add';
  nav.querySelectorAll('.nav-link').forEach(l => l.classList[action]('dark'));
  nav.querySelector('.nav-instagram').classList[action]('dark');
  
  if (name === 'home') {
    setTimeout(forceScrollAnimation, 50);
  }
}

function openModal(id) { document.getElementById('modal-' + id).classList.add('open'); }
function closeModal(event, forceClose = false) {
  if (forceClose || event.target.classList.contains('modal-overlay')) {
    document.querySelectorAll('.modal-overlay').forEach(m => m.classList.remove('open'));
  }
}

function buildGrids() {
  const mainGrid = document.getElementById('main-portfolio-grid');
  if(mainGrid) {
    mainGrid.innerHTML = portfolioImages.map((src, index) => {
      let text = "";
      if (index < 4) { text = "Création logo et support imprimé"; }
      else if (index === 4 || index === 8) { text = "Affiche"; }
      else if (index === 5) { text = "Support numérique"; }
      else if (index === 6) { text = "Carte cadeau"; }
      else if (index === 7) { text = "Édition"; }
      return `
        <div class="portfolio-item">
          <img src="${src}" alt="Création">
          <div class="portfolio-overlay">
            <span>${text}</span>
          </div>
        </div>`;
    }).join('');
  }
  const homeGrid = document.getElementById('home-portfolio-grid');
  if(homeGrid) {
    const firstFour = portfolioImages.slice(0, 4);
    homeGrid.innerHTML = [...firstFour, ...firstFour].map(src => `<div class="portfolio-item"><img src="${src}" alt="Création"></div>`).join('');
  }
}

function loadAboutImg(input) {
  if (!input.files[0]) return;
  const reader = new FileReader();
  reader.onload = e => document.getElementById('about-img-box').innerHTML = `<img src="${e.target.result}" alt="Photo">`;
  reader.readAsDataURL(input.files[0]);
}

function submitForm() {
  const nameInput = document.getElementById('f-name');
  const companyInput = document.getElementById('f-company');
  const emailInput = document.getElementById('f-email');
  const phoneInput = document.getElementById('f-phone');
  const dateInput = document.getElementById('f-date');
  const detailsInput = document.getElementById('f-details');
  const submitBtn = document.getElementById('f-submit-btn');

  const name = nameInput.value.trim();
  const company = companyInput.value.trim();
  const email = emailInput.value.trim();
  const phone = phoneInput.value.trim();
  const date = dateInput.value;
  const details = detailsInput.value.trim();
  
  let projectRadio = document.querySelector('input[name="project_type"]:checked');
  let projectType = projectRadio ? projectRadio.value : "Non spécifié";

  if (!name || !email || !details) {
    alert('Veuillez remplir les champs obligatoires.');
    return;
  }

  if (submitBtn) {
    submitBtn.disabled = true;
    submitBtn.innerText = "Envoi...";
  }

  const formData = new FormData();
  formData.append('Nom et Prenom', name);
  formData.append('Nom Entreprise', company);
  formData.append('Email', email);
  formData.append('Telephone', phone);
  formData.append('Type de Projet', projectType);
  formData.append('Date de Debut', date);
  formData.append('Details du Projet', details);

  document.getElementById('discovery-form-block').style.display = 'block';
  document.getElementById('final-success-msg').style.display = 'none';
  document.getElementById('discovery-container-box').classList.remove('success-active');

  fetch('https://formspree.io/f/mjgdqppk', {
    method: 'POST',
    body: formData,
    headers: {
      'Accept': 'application/json'
    }
  })
  .then(response => {
    if (response.ok) {
      nameInput.value = "";
      companyInput.value = "";
      emailInput.value = "";
      phoneInput.value = "";
      dateInput.value = "";
      detailsInput.value = "";
      if (projectRadio) projectRadio.checked = false;

      showPage('discovery');
    } else {
      response.json().then(data => {
        if (Object.prototype.hasOwnProperty.call(data, 'errors')) {
          alert(data.errors.map(error => error.message).join(", "));
        } else {
          alert("Une erreur est survenue lors de la soumission. Veuillez réessayer.");
        }
      });
    }
  })
  .catch(error => {
    alert("Impossible de joindre le serveur. Veuillez vérifier votre connexion internet.");
  })
  .finally(() => {
    if (submitBtn) {
      submitBtn.disabled = false;
      submitBtn.innerText = "Envoyer";
    }
  });
}

function submitDiscoveryForm() {
  const formBlock = document.getElementById('discovery-form-block');
  const successBox = document.getElementById('final-success-msg');
  const discoveryBtn = document.getElementById('f-discovery-btn');
  const containerBox = document.getElementById('discovery-container-box');
  
  let discoveryRadio = document.querySelector('input[name="discovery_source"]:checked');
  let discoverySource = discoveryRadio ? discoveryRadio.value : "Non spécifié";

  if (discoveryBtn) discoveryBtn.disabled = true;

  const dData = new FormData();
  dData.append('Source de decouverte', discoverySource);

  fetch('https://formspree.io/f/mjgdqppk', {
    method: 'POST',
    body: dData,
    headers: { 'Accept': 'application/json' }
  }).catch(() => {});

  if (formBlock) formBlock.style.display = 'none';
  if (successBox) successBox.style.display = 'block';
  if (containerBox) containerBox.classList.add('success-active');
  
  setTimeout(() => {
    showPage('home');
    
    if (formBlock) formBlock.style.display = 'block';
    if (successBox) successBox.style.display = 'none';
    if (containerBox) containerBox.classList.remove('success-active');
    if (discoveryRadio) discoveryRadio.checked = false;
    if (discoveryBtn) discoveryBtn.disabled = false;
  }, 5000);
}

window.addEventListener('scroll', () => {
  if(window.innerWidth > 768) {
    document.getElementById('main-nav').classList[window.scrollY > 50 ? 'add' : 'remove']('scrolled');
  }
});

buildGrids();
window.addEventListener('DOMContentLoaded', () => {
  setTimeout(forceScrollAnimation, 100);
});
</script>
</body>
</html>
