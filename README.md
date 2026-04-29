[4/30/2026 12:47 AM] Vijay Mali: github.com/omraut9011/Hotel-Om/settings/pages
[4/30/2026 1:23 AM] Vijay Mali: https://github.com/omraut9011/Hotel-Om/upload/main
[4/30/2026 2:58 AM] Vijay Mali: <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hotel Om – Pure Vegetarian</title>
  <link href="https://fonts.googleapis.com/css2?family=Yatra+One&family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --saffron: #FF6B1A;
      --gold: #FFB830;
      --maroon: #7B1C1C;
      --cream: #FFF8EE;
      --dark: #1A0A00;
      --green: #2E7D32;
      --light-gold: #FFF3D0;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }

    body {
      font-family: 'Poppins', sans-serif;
      background: var(--cream);
      color: var(--dark);
      overflow-x: hidden;
    }

    /* ── NAVBAR ── */
    nav {
      position: fixed; top: 0; width: 100%; z-index: 999;
      background: rgba(26,10,0,0.97);
      display: flex; justify-content: space-between; align-items: center;
      padding: 14px 40px;
      box-shadow: 0 2px 20px rgba(255,107,26,0.3);
    }
    .logo {
      font-family: 'Yatra One', cursive;
      font-size: 1.8rem;
      color: var(--gold);
      letter-spacing: 2px;
    }
    .logo span { color: var(--saffron); }
    .nav-links { display: flex; gap: 28px; list-style: none; }
    .nav-links a {
      color: #ddd; text-decoration: none; font-size: 0.9rem;
      font-weight: 500; transition: color 0.3s;
    }
    .nav-links a:hover { color: var(--gold); }
    #live-time {
      color: var(--gold); font-size: 0.85rem; font-weight: 600;
      background: rgba(255,184,48,0.1);
      padding: 6px 14px; border-radius: 20px;
      border: 1px solid rgba(255,184,48,0.3);
    }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      background: linear-gradient(135deg, #1A0A00 0%, #3D1500 50%, #1A0A00 100%);
      display: flex; align-items: center; justify-content: center;
      text-align: center; padding: 100px 20px 60px;
      position: relative; overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(ellipse at center, rgba(255,184,48,0.12) 0%, transparent 70%);
    }
    .mandala {
      position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%);
      width: 600px; height: 600px; opacity: 0.04;
      border-radius: 50%;
      border: 40px solid var(--gold);
      animation: spin 60s linear infinite;
    }
    .mandala2 {
      position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%);
      width: 400px; height: 400px; opacity: 0.05;
      border-radius: 50%;
      border: 20px solid var(--saffron);
      animation: spin 40s linear infinite reverse;
    }
    @keyframes spin { to { transform: translate(-50%,-50%) rotate(360deg); } }

    .hero-content { position: relative; z-index: 2; }
    .hero-badge {
      display: inline-block;
      background: linear-gradient(90deg, var(--saffron), var(--gold));
      color: white; font-size: 0.75rem; font-weight: 700;
      padding: 6px 20px; border-radius: 30px;
      text-transform: uppercase; letter-spacing: 3px;
      margin-bottom: 20px;
      animation: fadeDown 0.8s ease forwards;
    }
    .hero h1 {
      font-family: 'Yatra One', cursive;
      font-size: clamp(3rem, 8vw, 6rem);
      color: white; line-height: 1.1;
      animation: fadeDown 1s ease 0.2s both;
    }
    .hero h1 span { color: var(--gold); }
    .hero-sub {
      font-family: 'Playfair Display', serif;
      font-style: italic; color: rgba(255,255,255,0.7);
      font-size: 1.2rem; margin: 16px 0 32px;
      animation: fadeDown 1s ease 0.4s both;
    }
    .status-pill {
      display: inline-flex; align-items: center; gap: 10px;
      padding: 12px 28px; border-radius: 40px;
[4/30/2026 2:58 AM] Vijay Mali: font-weight: 600; font-size: 1rem;
      animation: fadeDown 1s ease 0.6s both;
      margin-bottom: 20px;
    }
    .status-pill.open { background: rgba(46,125,50,0.2); color: #81C784; border: 2px solid #2E7D32; }
    .status-pill.closed { background: rgba(183,28,28,0.2); color: #EF9A9A; border: 2px solid #B71C1C; }
    .status-dot { width: 10px; height: 10px; border-radius: 50%; animation: blink 1.2s infinite; }
    .open .status-dot { background: #81C784; }
    .closed .status-dot { background: #EF9A9A; }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }

    .hero-timing {
      color: rgba(255,255,255,0.6); font-size: 0.85rem;
      animation: fadeDown 1s ease 0.8s both;
    }
    .hero-timing strong { color: var(--gold); }

    .cta-row {
      display: flex; gap: 16px; justify-content: center; flex-wrap: wrap;
      margin-top: 36px;
      animation: fadeDown 1s ease 1s both;
    }
    .btn-primary {
      background: linear-gradient(135deg, var(--saffron), var(--gold));
      color: white; padding: 14px 36px; border-radius: 40px;
      text-decoration: none; font-weight: 700; font-size: 0.95rem;
      box-shadow: 0 8px 24px rgba(255,107,26,0.4);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .btn-primary:hover { transform: translateY(-3px); box-shadow: 0 14px 30px rgba(255,107,26,0.5); }
    .btn-outline {
      border: 2px solid var(--gold); color: var(--gold);
      padding: 14px 36px; border-radius: 40px;
      text-decoration: none; font-weight: 600; font-size: 0.95rem;
      transition: all 0.3s;
    }
    .btn-outline:hover { background: var(--gold); color: var(--dark); }

    @keyframes fadeDown { from{opacity:0;transform:translateY(-20px)} to{opacity:1;transform:translateY(0)} }

    /* ── SECTION BASE ── */
    section { padding: 80px 40px; }
    .section-title {
      text-align: center; margin-bottom: 60px;
    }
    .section-title h2 {
      font-family: 'Yatra One', cursive;
      font-size: 2.6rem; color: var(--maroon);
    }
    .section-title p { color: #888; margin-top: 8px; font-size: 1rem; }
    .divider {
      width: 80px; height: 3px;
      background: linear-gradient(90deg, var(--saffron), var(--gold));
      margin: 12px auto 0; border-radius: 10px;
    }

    /* ── OFFERS TICKER ── */
    .offers-ticker {
      background: linear-gradient(90deg, var(--maroon), #5C1111, var(--maroon));
      padding: 14px 0; overflow: hidden; white-space: nowrap;
    }
    .ticker-inner {
      display: inline-block;
      animation: ticker 30s linear infinite;
    }
    .ticker-inner span {
      display: inline-block; padding: 0 40px;
      color: var(--gold); font-weight: 600; font-size: 0.9rem;
    }
    .ticker-inner span::before { content: "🔥 "; }
    @keyframes ticker { from{transform:translateX(0)} to{transform:translateX(-50%)} }

    /* ── FEATURES ROW ── */
    .features {
      background: var(--dark);
      display: flex; flex-wrap: wrap; justify-content: center; gap: 0;
    }
    .feature-item {
      flex: 1; min-width: 200px;
      padding: 36px 28px; text-align: center;
      border-right: 1px solid rgba(255,184,48,0.15);
      transition: background 0.3s;
    }
    .feature-item:last-child { border-right: none; }
    .feature-item:hover { background: rgba(255,184,48,0.05); }
    .feature-icon { font-size: 2.4rem; margin-bottom: 12px; }
    .feature-item h3 { color: var(--gold); font-size: 1rem; font-weight: 700; }
    .feature-item p { color: #aaa; font-size: 0.82rem; margin-top: 6px; }

    /* ── MENU ── */
    #menu { background: white; }
    .menu-tabs {
      display: flex; flex-wrap: wrap; justify-content: center; gap: 12px;
      margin-bottom: 48px;
    }
    .tab-btn {
      padding: 10px 26px; border-radius: 30px; border: 2px solid #ddd;
      background: white; cursor: pointer; font-family: 'Poppins', sans-serif;
[4/30/2026 2:58 AM] Vijay Mali: font-weight: 600; font-size: 0.85rem; transition: all 0.3s;
      color: #666;
    }
    .tab-btn.active, .tab-btn:hover {
      background: linear-gradient(135deg, var(--saffron), var(--gold));
      border-color: transparent; color: white;
    }
    .menu-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 28px; max-width: 1100px; margin: 0 auto;
    }
    .menu-card {
      border-radius: 20px; overflow: hidden;
      box-shadow: 0 4px 24px rgba(0,0,0,0.08);
      background: white; border: 1px solid #f0f0f0;
      transition: transform 0.3s, box-shadow 0.3s;
      display: none;
    }
    .menu-card.show { display: block; }
    .menu-card:hover { transform: translateY(-6px); box-shadow: 0 12px 36px rgba(255,107,26,0.15); }
    .menu-card-img {
      height: 180px; font-size: 5rem;
      display: flex; align-items: center; justify-content: center;
    }
    .menu-card-body { padding: 20px; }
    .menu-card-body h3 { font-size: 1rem; font-weight: 700; color: var(--dark); }
    .menu-card-body p { font-size: 0.78rem; color: #888; margin: 6px 0 14px; }
    .menu-footer { display: flex; align-items: center; justify-content: space-between; }
    .price { font-size: 1.1rem; font-weight: 800; color: var(--saffron); }
    .veg-dot {
      width: 14px; height: 14px; border-radius: 50%; background: var(--green);
      border: 2px solid var(--green); display: inline-block;
    }
    .tag {
      font-size: 0.68rem; padding: 3px 10px; border-radius: 20px;
      font-weight: 700;
    }
    .tag.best { background: #FFF3D0; color: #E65100; }
    .tag.new { background: #E8F5E9; color: #2E7D32; }
    .tag.spicy { background: #FCE4EC; color: #B71C1C; }

    /* ── SPECIAL ── */
    #specials {
      background: linear-gradient(135deg, #FFF8EE 0%, #FFF3D0 100%);
    }
    .specials-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 32px; max-width: 1100px; margin: 0 auto;
    }
    .special-card {
      background: white; border-radius: 24px;
      padding: 32px 28px; text-align: center;
      box-shadow: 0 8px 32px rgba(0,0,0,0.06);
      border: 2px solid transparent;
      transition: border 0.3s, transform 0.3s;
      position: relative; overflow: hidden;
    }
    .special-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 4px;
      background: linear-gradient(90deg, var(--saffron), var(--gold));
    }
    .special-card:hover { border-color: var(--gold); transform: translateY(-4px); }
    .special-emoji { font-size: 3.5rem; margin-bottom: 16px; }
    .special-card h3 { font-family: 'Playfair Display', serif; font-size: 1.3rem; color: var(--maroon); }
    .special-card p { color: #777; font-size: 0.85rem; margin: 10px 0 16px; }
    .special-price { font-size: 1.4rem; font-weight: 800; color: var(--saffron); }
    .special-old { font-size: 0.85rem; color: #aaa; text-decoration: line-through; margin-left: 8px; }
    .ribbon {
      position: absolute; top: 16px; right: -8px;
      background: var(--maroon); color: white;
      font-size: 0.65rem; font-weight: 800;
      padding: 4px 14px; text-transform: uppercase; letter-spacing: 1px;
      border-radius: 4px 0 0 4px;
    }
    .ribbon::after {
      content: '';
      position: absolute; right: 0; bottom: -6px;
      border-left: 8px solid #4A1010;
      border-bottom: 6px solid transparent;
    }

    /* ── OFFERS ── */
    #offers { background: var(--dark); }
    #offers .section-title h2 { color: var(--gold); }
    #offers .section-title p { color: #aaa; }
    .offers-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px; max-width: 1100px; margin: 0 auto;
    }
    .offer-card {
      border-radius: 20px; padding: 32px 28px;
[4/30/2026 2:58 AM] Vijay Mali: border: 1px solid rgba(255,184,48,0.2);
      position: relative; overflow: hidden;
      background: rgba(255,255,255,0.03);
      transition: background 0.3s;
    }
    .offer-card:hover { background: rgba(255,184,48,0.07); }
    .offer-badge {
      display: inline-block;
      background: linear-gradient(90deg, var(--saffron), var(--gold));
      color: white; font-size: 2rem; font-weight: 900;
      padding: 6px 20px; border-radius: 12px;
      margin-bottom: 16px;
    }
    .offer-card h3 { color: white; font-size: 1.1rem; font-weight: 700; }
    .offer-card p { color: #aaa; font-size: 0.82rem; margin-top: 8px; line-height: 1.6; }
    .offer-code {
      display: inline-block; margin-top: 16px;
      border: 2px dashed var(--gold); color: var(--gold);
      padding: 8px 20px; border-radius: 10px;
      font-weight: 700; font-size: 0.85rem; letter-spacing: 2px;
    }

    /* ── DELIVERY ── */
    #delivery {
      background: linear-gradient(135deg, var(--saffron), var(--gold));
      text-align: center; padding: 80px 40px;
    }
    #delivery h2 {
      font-family: 'Yatra One', cursive;
      font-size: 2.8rem; color: white;
    }
    #delivery p { color: rgba(255,255,255,0.9); font-size: 1rem; margin: 16px auto 36px; max-width: 500px; }
    .delivery-cards {
      display: flex; flex-wrap: wrap; justify-content: center; gap: 24px; margin-top: 48px;
    }
    .del-card {
      background: rgba(255,255,255,0.15); backdrop-filter: blur(10px);
      border-radius: 20px; padding: 28px 36px; text-align: center;
      border: 1px solid rgba(255,255,255,0.3); min-width: 180px;
    }
    .del-card .icon { font-size: 2.5rem; margin-bottom: 10px; }
    .del-card h3 { color: white; font-weight: 700; }
    .del-card p { color: rgba(255,255,255,0.8); font-size: 0.8rem; margin-top: 4px; }

    /* ── TIMING ── */
    #timing { background: white; }
    .timing-container {
      max-width: 700px; margin: 0 auto;
      background: var(--cream); border-radius: 24px;
      overflow: hidden; box-shadow: 0 8px 40px rgba(0,0,0,0.08);
    }
    .timing-header {
      background: linear-gradient(135deg, var(--maroon), #5C1111);
      padding: 28px 36px; text-align: center;
    }
    .timing-header h3 {
      font-family: 'Yatra One', cursive;
      color: var(--gold); font-size: 1.6rem;
    }
    .timing-header p { color: rgba(255,255,255,0.7); font-size: 0.85rem; margin-top: 6px; }
    .timing-body { padding: 10px 0; }
    .timing-row {
      display: flex; justify-content: space-between; align-items: center;
      padding: 16px 36px; border-bottom: 1px solid rgba(0,0,0,0.06);
    }
    .timing-row:last-child { border-bottom: none; }
    .timing-row .day { font-weight: 600; color: var(--dark); }
    .timing-row .time { color: var(--saffron); font-weight: 700; font-size: 0.9rem; }
    .timing-row.today { background: rgba(255,107,26,0.05); }
    .today-badge {
      font-size: 0.65rem; background: var(--saffron); color: white;
      padding: 3px 10px; border-radius: 20px; margin-left: 10px;
    }

    /* ── TESTIMONIALS ── */
    #reviews { background: var(--light-gold); }
    .reviews-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px; max-width: 1100px; margin: 0 auto;
    }
    .review-card {
      background: white; border-radius: 20px; padding: 28px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.06);
    }
    .stars { color: var(--gold); font-size: 1.1rem; margin-bottom: 12px; }
    .review-card p { color: #555; font-size: 0.88rem; line-height: 1.7; font-style: italic; }
    .reviewer { display: flex; align-items: center; gap: 14px; margin-top: 20px; }
    .avatar {
      width: 44px; height: 44px; border-radius: 50%;
      background: linear-gradient(135deg, var(--saffron), var(--gold));
      display: flex; align-items: center; justify-content: center;
      font-size: 1.2rem; color: white; font-weight: 700;
    }
    .reviewer-info h4 { font-size: 0.9rem; font-weight: 700; }
    .reviewer-info p { font-size: 0.75rem; color: #aaa; }
[4/30/2026 2:58 AM] Vijay Mali: /* ── CONTACT ── */
    #contact { background: var(--dark); }
    #contact .section-title h2 { color: var(--gold); }
    #contact .section-title p { color: #aaa; }
    .contact-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 28px; max-width: 900px; margin: 0 auto;
    }
    .contact-card {
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,184,48,0.15);
      border-radius: 20px; padding: 32px 24px; text-align: center;
      transition: background 0.3s;
    }
    .contact-card:hover { background: rgba(255,184,48,0.07); }
    .contact-icon { font-size: 2.4rem; margin-bottom: 14px; }
    .contact-card h3 { color: var(--gold); font-size: 0.9rem; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; }
    .contact-card p { color: #ccc; font-size: 0.88rem; margin-top: 8px; line-height: 1.6; }

    /* ── FOOTER ── */
    footer {
      background: #0D0500; padding: 36px 40px;
      text-align: center; border-top: 1px solid rgba(255,184,48,0.1);
    }
    footer .logo { font-size: 1.4rem; }
    footer p { color: #555; font-size: 0.8rem; margin-top: 12px; }
    footer span { color: var(--saffron); }

    /* ── RESPONSIVE ── */
    @media(max-width:768px) {
      nav { padding: 14px 20px; }
      .nav-links { display: none; }
      section { padding: 60px 20px; }
      .feature-item { min-width: 50%; }
    }

    /* ── SCROLL TO TOP ── */
    #scroll-top {
      position: fixed; bottom: 30px; right: 30px;
      background: linear-gradient(135deg, var(--saffron), var(--gold));
      color: white; border: none; width: 50px; height: 50px;
      border-radius: 50%; cursor: pointer; font-size: 1.3rem;
      box-shadow: 0 4px 16px rgba(255,107,26,0.5);
      display: none; align-items: center; justify-content: center;
      transition: transform 0.2s;
    }
    #scroll-top:hover { transform: scale(1.1); }
    #scroll-top.show { display: flex; }
  </style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <div class="logo">🕉 Hotel <span>Om</span></div>
  <ul class="nav-links">
    <li><a href="#menu">Menu</a></li>
    <li><a href="#specials">Specials</a></li>
    <li><a href="#offers">Offers</a></li>
    <li><a href="#delivery">Delivery</a></li>
    <li><a href="#timing">Timings</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div id="live-time">⏱ --:-- --</div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="mandala"></div>
  <div class="mandala2"></div>
  <div class="hero-content">
    <div class="hero-badge">🌿 100% Pure Vegetarian</div>
    <h1>Hotel <span>Om</span></h1>
    <p class="hero-sub">Where every meal is a blessing</p>

    <div id="hero-status" class="status-pill open">
      <span class="status-dot"></span>
      <span id="status-text">We're Open!</span>
    </div>
    <br/>
    <p class="hero-timing">
      Today: <strong>7:00 AM – 10:30 PM</strong> &nbsp;|&nbsp;
      Lunch: <strong>11:30 AM – 3:30 PM</strong> &nbsp;|&nbsp;
      Dinner: <strong>7:00 PM – 10:30 PM</strong>
    </p>
    <div class="cta-row">
      <a href="#menu" class="btn-primary">View Menu 🍽️</a>
      <a href="#offers" class="btn-outline">Today's Offers 🔥</a>
    </div>
  </div>
</section>

<!-- TICKER -->
<div class="offers-ticker">
  <div class="ticker-inner">
    <span>Free Delivery above ₹299</span>
    <span>Thali Special @ ₹99 – Mon to Fri</span>
    <span>Buy 2 Get 1 Free on Desserts – Weekends</span>
    <span>10% Off on Orders above ₹500</span>
    <span>New: Paneer Butter Masala Thali</span>
    <span>Birthday Special Combo – Call Us!</span>
    <span>Free Delivery above ₹299</span>
    <span>Thali Special @ ₹99 – Mon to Fri</span>
    <span>Buy 2 Get 1 Free on Desserts – Weekends</span>
    <span>10% Off on Orders above ₹500</span>
    <span>New: Paneer Butter Masala Thali</span>
    <span>Birthday Special Combo – Call Us!</span>
  </div>
</div>
[4/30/2026 2:58 AM] Vijay Mali: <!-- FEATURES -->
<div class="features">
  <div class="feature-item">
    <div class="feature-icon">🚀</div>
    <h3>Fast Delivery</h3>
    <p>30 min or we discount</p>
  </div>
  <div class="feature-item">
    <div class="feature-icon">🌿</div>
    <h3>Pure Veg</h3>
    <p>100% vegetarian kitchen</p>
  </div>
  <div class="feature-item">
    <div class="feature-icon">👨‍🍳</div>
    <h3>Home Style</h3>
    <p>Authentic family recipes</p>
  </div>
  <div class="feature-item">
    <div class="feature-icon">💯</div>
    <h3>Hygiene First
