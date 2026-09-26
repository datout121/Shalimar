from pathlib import Path

html = r'''<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Le Shalimar Valence — restaurant indien, 6 Place Saint-Jean, 26000 Valence." />
  <title>Le Shalimar — Restaurant Indien à Valence</title>

  <style>
    :root{
      --bg:#120c0a;
      --card:#1d1411;
      --gold:#e7b65c;
      --gold2:#ffd98a;
      --cream:#fff7e8;
      --muted:#d6c9b7;
      --red:#8f241d;
      --red2:#b83b2f;
      --line:rgba(255,255,255,.10);
      --shadow:0 18px 50px rgba(0,0,0,.30);
    }

    *{box-sizing:border-box;scroll-behavior:smooth}

    body{
      margin:0;
      font-family:Inter,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
      background:
        radial-gradient(circle at 15% 0%, rgba(231,182,92,.13), transparent 28%),
        radial-gradient(circle at 85% 20%, rgba(143,36,29,.18), transparent 30%),
        var(--bg);
      color:var(--cream);
      line-height:1.6;
    }

    a{text-decoration:none;color:inherit}

    .container{
      width:min(1160px,92%);
      margin:auto;
    }

    header{
      position:fixed;
      z-index:20;
      top:0;left:0;right:0;
      backdrop-filter:blur(14px);
      background:rgba(18,12,10,.76);
      border-bottom:1px solid var(--line);
    }

    .nav{
      min-height:76px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:24px;
    }

    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      font-weight:900;
      letter-spacing:.08em;
      text-transform:uppercase;
    }

    .brand-mark{
      width:42px;height:42px;
      display:grid;place-items:center;
      border:1px solid var(--gold);
      border-radius:50%;
      color:var(--gold);
      font-size:20px;
    }

    nav{
      display:flex;
      gap:22px;
      align-items:center;
    }

    nav a{
      color:#f8ecda;
      font-size:14px;
      opacity:.9;
    }

    nav a:hover{color:var(--gold2)}

    .nav-phone{
      padding:10px 14px;
      border:1px solid rgba(231,182,92,.5);
      border-radius:999px;
      color:var(--gold2);
      font-weight:800;
    }

    .hero{
      min-height:100vh;
      position:relative;
      display:grid;
      place-items:center;
      overflow:hidden;
      background:
        linear-gradient(90deg, rgba(10,6,4,.88), rgba(10,6,4,.42), rgba(10,6,4,.72)),
        url("https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-1.webp")
        center/cover no-repeat;
    }

    .hero::after{
      content:"";
      position:absolute;inset:0;
      background:linear-gradient(180deg,rgba(0,0,0,.15),rgba(18,12,10,.96));
      pointer-events:none;
    }

    .hero-content{
      position:relative;
      z-index:2;
      width:min(900px,92%);
      text-align:center;
      padding-top:80px;
    }

    .eyebrow{
      display:inline-flex;
      align-items:center;
      gap:9px;
      color:var(--gold2);
      border:1px solid rgba(231,182,92,.35);
      background:rgba(0,0,0,.24);
      padding:8px 14px;
      border-radius:999px;
      font-size:13px;
      font-weight:800;
      text-transform:uppercase;
      letter-spacing:.12em;
    }

    h1{
      font-family:Georgia,"Times New Roman",serif;
      font-size:clamp(52px,9vw,104px);
      line-height:.9;
      margin:24px 0;
      letter-spacing:-.05em;
      text-shadow:0 12px 40px rgba(0,0,0,.5);
    }

    .hero p{
      max-width:700px;
      margin:0 auto 30px;
      color:#f4e6d3;
      font-size:clamp(17px,2vw,21px);
    }

    .buttons{
      display:flex;
      flex-wrap:wrap;
      justify-content:center;
      gap:12px;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:8px;
      min-height:52px;
      padding:0 22px;
      border-radius:999px;
      font-weight:900;
      border:1px solid transparent;
      transition:.2s ease;
    }

    .btn:hover{transform:translateY(-2px)}

    .btn-primary{
      background:linear-gradient(135deg,var(--gold2),var(--gold));
      color:#24170c;
      box-shadow:0 10px 30px rgba(231,182,92,.18);
    }

    .btn-dark{
      background:rgba(0,0,0,.35);
      border-color:rgba(255,255,255,.2);
      color:white;
    }

    section{padding:92px 0}

    .section-title{
      text-align:center;
      margin-bottom:45px;
    }

    .section-title span{
      color:var(--gold);
      text-transform:uppercase;
      letter-spacing:.18em;
      font-size:12px;
      font-weight:900;
    }

    .section-title h2{
      font-family:Georgia,"Times New Roman",serif;
      font-size:clamp(36px,5vw,58px);
      margin:10px 0;
    }

    .section-title p{
      color:var(--muted);
      max-width:680px;
      margin:auto;
    }

    .info-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:18px;
    }

    .info-card{
      background:linear-gradient(145deg,rgba(255,255,255,.07),rgba(255,255,255,.025));
      border:1px solid var(--line);
      padding:28px;
      border-radius:24px;
      box-shadow:var(--shadow);
    }

    .icon{
      width:48px;height:48px;
      display:grid;place-items:center;
      border-radius:14px;
      background:rgba(231,182,92,.11);
      color:var(--gold2);
      font-size:23px;
      margin-bottom:15px;
    }

    .info-card h3{margin:0 0 7px}
    .info-card p{margin:0;color:var(--muted)}

    .menu-wrap{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:20px;
    }

    .menu-card{
      background:var(--card);
      border:1px solid var(--line);
      border-radius:24px;
      overflow:hidden;
      box-shadow:var(--shadow);
    }

    .menu-photo{
      width:100%;
      height:230px;
      object-fit:cover;
      display:block;
    }

    .menu-card-body{padding:24px}

    .menu-card h3{
      font-family:Georgia,"Times New Roman",serif;
      font-size:28px;
      margin:0 0 16px;
    }

    .dish{
      display:flex;
      gap:15px;
      justify-content:space-between;
      padding:15px 0;
      border-bottom:1px solid var(--line);
    }

    .dish:last-child{border-bottom:0}

    .dish-name{font-weight:850}
    .dish-desc{color:#bcae9d;font-size:13px;margin-top:3px}
    .price{white-space:nowrap;color:var(--gold2);font-weight:900}

    .gallery{
      display:grid;
      grid-template-columns:1.25fr .75fr;
      gap:18px;
    }

    .gallery img{
      width:100%;
      height:100%;
      min-height:270px;
      object-fit:cover;
      border-radius:24px;
      border:1px solid var(--line);
      box-shadow:var(--shadow);
    }

    .gallery-side{
      display:grid;
      gap:18px;
    }

    .gallery-side img{min-height:200px}

    .contact{
      background:
        linear-gradient(135deg,rgba(143,36,29,.72),rgba(18,12,10,.88)),
        url("https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-3.webp")
        center/cover no-repeat;
      border-top:1px solid rgba(255,255,255,.08);
      border-bottom:1px solid rgba(255,255,255,.08);
    }

    .contact-box{
      display:grid;
      grid-template-columns:1fr auto;
      gap:25px;
      align-items:center;
      padding:40px;
      border:1px solid rgba(255,255,255,.15);
      background:rgba(0,0,0,.28);
      border-radius:30px;
    }

    .contact-box h2{
      font-family:Georgia,"Times New Roman",serif;
      font-size:42px;
      margin:0 0 8px;
    }

    .contact-box p{margin:5px 0;color:#f0e3d2}

    footer{
      padding:35px 0;
      color:#a99b89;
      text-align:center;
      font-size:13px;
    }

    .mobile-cta{
      display:none;
      position:fixed;
      z-index:30;
      left:14px;right:14px;bottom:14px;
      padding:13px;
      background:rgba(18,12,10,.94);
      border:1px solid rgba(231,182,92,.45);
      border-radius:18px;
      box-shadow:0 15px 45px rgba(0,0,0,.45);
      text-align:center;
    }

    @media(max-width:820px){
      nav{display:none}
      .nav-phone{display:none}
      .info-grid,.menu-wrap,.gallery{grid-template-columns:1fr}
      .contact-box{grid-template-columns:1fr;padding:28px}
      .mobile-cta{display:block}
      body{padding-bottom:72px}
    }

    @media(max-width:520px){
      .hero{min-height:88vh}
      section{padding:70px 0}
      .hero-content{padding-top:60px}
      .buttons .btn{width:100%}
      .menu-photo{height:200px}
      .contact-box h2{font-size:34px}
    }
  </style>
</head>

<body>

<header>
  <div class="container nav">
    <a class="brand" href="#accueil" aria-label="Le Shalimar accueil">
      <span class="brand-mark">✦</span>
      <span>Le Shalimar</span>
    </a>

    <nav>
      <a href="#accueil">Accueil</a>
      <a href="#menu">La carte</a>
      <a href="#photos">Photos</a>
      <a href="#contact">Contact</a>
    </nav>

    <a class="nav-phone" href="tel:+33970351774">📞 09 70 35 17 74</a>
  </div>
</header>

<main id="accueil">

  <section class="hero">
    <div class="hero-content">
      <div class="eyebrow">✦ Cuisine indienne à Valence ✦</div>

      <h1>Le Shalimar</h1>

      <p>
        Des spécialités indiennes aux saveurs authentiques,
        au cœur de Valence.
      </p>

      <div class="buttons">
        <a class="btn btn-primary" href="#menu">🍛 Voir les plats</a>
        <a class="btn btn-dark" href="tel:+33970351774">📞 Appeler le restaurant</a>
      </div>
    </div>
  </section>

  <section>
    <div class="container">
      <div class="section-title">
        <span>Bienvenue</span>
        <h2>Une table aux couleurs de l'Inde</h2>
        <p>
          Une adresse au centre de Valence avec cuisine indienne,
          service sur place, à emporter et livraison.
        </p>
      </div>

      <div class="info-grid">
        <article class="info-card">
          <div class="icon">📍</div>
          <h3>Nous trouver</h3>
          <p>6 Place Saint-Jean, 26000 Valence</p>
        </article>

        <article class="info-card">
          <div class="icon">📞</div>
          <h3>Réserver / appeler</h3>
          <p><a href="tel:+33970351774">09 70 35 17 74</a></p>
        </article>

        <article class="info-card">
          <div class="icon">🛍️</div>
          <h3>Sur place & à emporter</h3>
          <p>Sur place, à emporter et livraison à domicile.</p>
        </article>
      </div>
    </div>
  </section>

  <section id="menu">
    <div class="container">
      <div class="section-title">
        <span>La carte</span>
        <h2>Les plats du Shalimar</h2>
        <p>
          Une sélection de plats et de formules présents sur la carte du restaurant.
        </p>
      </div>

      <div class="menu-wrap">

        <article class="menu-card">
          <img
            class="menu-photo"
            src="https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-2.webp"
            alt="Spécialités indiennes du Shalimar"
          />
          <div class="menu-card-body">
            <h3>Entrées & Tandoori</h3>

            <div class="dish">
              <div>
                <div class="dish-name">Raita</div>
                <div class="dish-desc">Yaourt, concombre, tomate, menthe et épices</div>
              </div>
              <div class="price">5,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Samoussa légumes</div>
                <div class="dish-desc">Pommes de terre, petits pois, noix de cajou</div>
              </div>
              <div class="price">7,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Tandoori</div>
                <div class="dish-desc">Poulet mariné aux épices et jus de citron</div>
              </div>
              <div class="price">8,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Tikka Tandoori</div>
                <div class="dish-desc">Filet de poulet mariné puis grillé au tandoori</div>
              </div>
              <div class="price">8,50 €</div>
            </div>
          </div>
        </article>

        <article class="menu-card">
          <img
            class="menu-photo"
            src="https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-3.webp"
            alt="Salle du restaurant Le Shalimar"
          />
          <div class="menu-card-body">
            <h3>Plats principaux</h3>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Masala</div>
                <div class="dish-desc">Poulet au curry et épices traditionnelles</div>
              </div>
              <div class="price">12,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Makhani</div>
                <div class="dish-desc">Tomate, crème, beurre et épices</div>
              </div>
              <div class="price">13,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Tikka Masala</div>
                <div class="dish-desc">Poulet mariné, poivrons, oignons et épices</div>
              </div>
              <div class="price">13,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Agneau Shahi Korma</div>
                <div class="dish-desc">Crème, noix de cajou, fruits secs et amandes</div>
              </div>
              <div class="price">14,50 €</div>
            </div>
          </div>
        </article>

        <article class="menu-card">
          <div class="menu-card-body">
            <h3>Biryanis</h3>

            <div class="dish">
              <div>
                <div class="dish-name">Sabzi Biryani</div>
                <div class="dish-desc">Riz mijoté aux légumes et aux épices</div>
              </div>
              <div class="price">12,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Poulet Biryani</div>
                <div class="dish-desc">Riz mijoté au poulet et fines herbes</div>
              </div>
              <div class="price">13,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Agneau Biryani</div>
                <div class="dish-desc">Riz mijoté à l'agneau et épices</div>
              </div>
              <div class="price">14,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Biryani Royal</div>
                <div class="dish-desc">Agneau, crevettes, poulet et riz parfumé</div>
              </div>
              <div class="price">16,50 €</div>
            </div>
          </div>
        </article>

        <article class="menu-card">
          <div class="menu-card-body">
            <h3>Naans & accompagnements</h3>

            <div class="dish">
              <div>
                <div class="dish-name">Sada Naan</div>
                <div class="dish-desc">Galette de farine cuite au tandoori</div>
              </div>
              <div class="price">3,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Cheese Naan</div>
                <div class="dish-desc">Naan farci au fromage fondu</div>
              </div>
              <div class="price">3,50 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Garlic Naan</div>
                <div class="dish-desc">Naan à l'ail et fromage fondu</div>
              </div>
              <div class="price">4,00 €</div>
            </div>

            <div class="dish">
              <div>
                <div class="dish-name">Palak Paneer</div>
                <div class="dish-desc">Curry d'épinards et fromage</div>
              </div>
              <div class="price">10,50 €</div>
            </div>
          </div>
        </article>

      </div>

      <div class="buttons" style="margin-top:32px">
        <a class="btn btn-primary" href="https://www.restaurant-indien-valence.fr/carte.php" target="_blank" rel="noopener">
          📖 Voir toute la carte
        </a>
        <a class="btn btn-dark" href="tel:+33970351774">📞 Réserver</a>
      </div>
    </div>
  </section>

  <section id="photos">
    <div class="container">
      <div class="section-title">
        <span>Le restaurant</span>
        <h2>Découvrez le cadre</h2>
        <p>Quelques photos du Shalimar à Valence.</p>
      </div>

      <div class="gallery">
        <img
          src="https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-1.webp"
          alt="Intérieur du restaurant Le Shalimar à Valence"
        />

        <div class="gallery-side">
          <img
            src="https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-3.webp"
            alt="Salle colorée du restaurant Le Shalimar"
          />
          <img
            src="https://trsuqfufpfgyawgjmxyw.supabase.co/storage/v1/object/public/restaurant-gallery/valence/restaurant-le-shalimar-valence-2.webp"
            alt="Spécialités indiennes du Shalimar"
          />
        </div>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <div class="container">
      <div class="contact-box">
        <div>
          <div class="eyebrow">📍 Valence 26000</div>
          <h2>Venez au Shalimar</h2>
          <p>6 Place Saint-Jean, 26000 Valence</p>
          <p>📞 <a href="tel:+33970351774">09 70 35 17 74</a></p>
        </div>

        <div class="buttons">
          <a
            class="btn btn-primary"
            href="https://www.google.com/maps/search/?api=1&query=Le+Shalimar+6+Place+Saint-Jean+26000+Valence"
            target="_blank"
            rel="noopener"
          >
            📍 Itinéraire
          </a>
          <a class="btn btn-dark" href="tel:+33970351774">📞 Appeler</a>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="container">
    © 2026 Le Shalimar — Restaurant indien à Valence · 6 Place Saint-Jean, 26000 Valence
  </div>
</footer>

<div class="mobile-cta">
  <a class="btn btn-primary" style="width:100%" href="#menu">🍛 Voir les plats</a>
</div>

</body>
</html>
'''

path = Path("/mnt/data/shalimar-valence.html")
path.write_text(html, encoding="utf-8")

print(f"Fichier créé : {path}")
