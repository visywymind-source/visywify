# visywify
Uma empresa com produtos capacitadores , cursos e ebooks que fazem evoluir e farão conquistar seus sonhos e metas
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Visywify — Cursos e Ebooks para aprender e lucrar com Inteligência Artificial</title>
<meta name="description" content="Visywify: cursos e ebooks práticos para aprender habilidades digitais e de Inteligência Artificial. Acesso imediato após a compra.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,500;1,9..144,600&family=Inter:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#1B1030;
    --ink-soft:#4A3F63;
    --violet-900:#3A1671;
    --violet-700:#5B21B6;
    --violet-600:#6D28D9;
    --violet-500:#7C3AED;
    --violet-300:#B79CF0;
    --violet-100:#EDE4FB;
    --lavender-bg:#F6F2FC;
    --paper:#FBFAFE;
    --amber:#F2B84B;
    --amber-dark:#D89A2C;
    --teal-accent:#20B8A6;
    --line:#E3D9F5;
    --white:#FFFFFF;

    --font-display:'Fraunces', serif;
    --font-body:'Inter', sans-serif;
    --font-mono:'IBM Plex Mono', monospace;

    --radius-lg:22px;
    --radius-md:14px;
    --radius-sm:8px;
    --shadow-card: 0 14px 34px -14px rgba(58,22,113,0.28);
    --shadow-soft: 0 8px 24px -12px rgba(58,22,113,0.18);
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    font-family:var(--font-body);
    color:var(--ink);
    background:var(--paper);
    -webkit-font-smoothing:antialiased;
    line-height:1.5;
  }
  img,svg{display:block; max-width:100%;}
  a{color:inherit; text-decoration:none;}
  ul{margin:0; padding:0; list-style:none;}
  h1,h2,h3,h4{margin:0; font-family:var(--font-display); color:var(--ink); font-weight:600;}
  p{margin:0;}
  .container{
    max-width:1180px;
    margin:0 auto;
    padding:0 28px;
  }
  section{padding:96px 0;}
  @media (max-width:720px){
    section{padding:64px 0;}
    .container{padding:0 20px;}
  }

  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-family:var(--font-mono);
    font-size:12.5px;
    letter-spacing:0.08em;
    text-transform:uppercase;
    color:var(--violet-600);
    font-weight:600;
    margin-bottom:16px;
  }
  .eyebrow::before{
    content:"";
    width:7px; height:7px;
    background:var(--amber);
    border-radius:50%;
    display:inline-block;
  }

  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:8px;
    padding:14px 26px;
    border-radius:100px;
    font-family:var(--font-body);
    font-weight:700;
    font-size:15px;
    cursor:pointer;
    border:none;
    transition:transform .18s ease, box-shadow .18s ease, background .18s ease;
    white-space:nowrap;
  }
  .btn:hover{transform:translateY(-2px);}
  .btn:focus-visible{outline:3px solid var(--violet-300); outline-offset:2px;}
  .btn-primary{
    background:var(--amber);
    color:#3A2400;
    box-shadow:0 10px 24px -8px rgba(242,184,75,0.65);
  }
  .btn-primary:hover{background:var(--amber-dark);}
  .btn-ghost{
    background:transparent;
    color:var(--white);
    border:1.5px solid rgba(255,255,255,0.35);
  }
  .btn-ghost:hover{background:rgba(255,255,255,0.1);}
  .btn-outline{
    background:transparent;
    color:var(--violet-700);
    border:1.5px solid var(--violet-300);
  }
  .btn-outline:hover{background:var(--violet-100);}
  .btn-sm{padding:10px 18px; font-size:13.5px;}
  .btn-full{width:100%;}

  /* ---------- NAV ---------- */
  header.nav{
    position:sticky; top:0; z-index:100;
    background:rgba(251,250,254,0.88);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{
    max-width:1180px; margin:0 auto; padding:16px 28px;
    display:flex; align-items:center; justify-content:space-between;
  }
  .logo{display:flex; align-items:center; gap:10px;}
  .logo-word{
    font-family:var(--font-display);
    font-weight:700;
    font-size:22px;
    color:var(--ink);
    letter-spacing:-0.01em;
  }
  .logo-word span{color:var(--violet-600);}
  .nav-links{display:flex; align-items:center; gap:34px;}
  .nav-links a{
    font-size:14.5px; font-weight:600; color:var(--ink-soft);
    transition:color .15s ease;
  }
  .nav-links a:hover{color:var(--violet-600);}
  .nav-cta{display:flex; align-items:center; gap:14px;}
  .nav-toggle{display:none; background:none; border:none; cursor:pointer; padding:6px;}
  .nav-toggle svg{width:26px; height:26px;}

  @media (max-width:900px){
    .nav-links{
      position:fixed; inset:64px 0 0 0; background:var(--paper);
      flex-direction:column; align-items:flex-start; gap:0;
      padding:12px 28px 28px; transform:translateX(100%);
      transition:transform .28s ease; overflow-y:auto;
    }
    .nav-links.open{transform:translateX(0);}
    .nav-links a{padding:16px 0; width:100%; border-bottom:1px solid var(--line); font-size:16.5px;}
    .nav-cta .btn-outline{display:none;}
    .nav-toggle{display:block;}
  }

  /* ---------- HERO ---------- */
  .hero{
    background:linear-gradient(180deg, var(--violet-900) 0%, var(--violet-700) 62%, var(--violet-600) 100%);
    position:relative;
    overflow:hidden;
    padding:88px 0 110px;
  }
  .hero::before{
    content:"";
    position:absolute; inset:0;
    background-image:
      radial-gradient(circle at 14% 18%, rgba(255,255,255,0.10) 0, transparent 40%),
      radial-gradient(circle at 92% 82%, rgba(242,184,75,0.18) 0, transparent 45%);
    pointer-events:none;
  }
  .hero-grid{
    position:relative; z-index:1;
    display:grid; grid-template-columns:1.05fr 0.95fr; gap:56px; align-items:center;
  }
  @media (max-width:940px){
    .hero-grid{grid-template-columns:1fr; text-align:left;}
  }
  .hero-copy .eyebrow{color:var(--amber);}
  .hero-copy .eyebrow::before{background:var(--amber);}
  .hero-copy h1{
    font-size:clamp(34px, 5vw, 54px);
    line-height:1.08;
    color:var(--white);
    max-width:16ch;
  }
  .hero-copy h1 em{
    font-style:italic;
    color:var(--amber);
  }
  .hero-copy p.lead{
    margin-top:22px;
    font-size:17.5px;
    color:rgba(255,255,255,0.82);
    max-width:46ch;
    line-height:1.6;
  }
  .hero-actions{
    margin-top:34px;
    display:flex; gap:14px; flex-wrap:wrap;
  }
  .hero-stats{
    margin-top:48px;
    display:flex; gap:36px; flex-wrap:wrap;
  }
  .hero-stat b{
    display:block; font-family:var(--font-display); font-size:26px; color:var(--white);
  }
  .hero-stat span{
    font-size:12.5px; color:rgba(255,255,255,0.62); font-family:var(--font-mono); letter-spacing:.03em;
  }

  /* fanned product cards (signature element) */
  .hero-visual{
    position:relative; height:390px;
    display:flex; align-items:center; justify-content:center;
  }
  .fan-card{
    position:absolute;
    width:196px; height:266px;
    border-radius:18px;
    box-shadow:0 24px 50px -18px rgba(0,0,0,0.45);
    padding:22px;
    display:flex; flex-direction:column; justify-content:space-between;
    transition:transform .4s ease;
  }
  .fan-card:hover{transform:translateY(-10px) scale(1.02) !important;}
  .fan-card .tag{
    font-family:var(--font-mono); font-size:10px; letter-spacing:.06em; text-transform:uppercase;
    background:rgba(255,255,255,0.18); color:#fff; padding:4px 10px; border-radius:100px; width:fit-content;
  }
  .fan-card h4{color:#fff; font-size:16.5px; line-height:1.28;}
  .fan-card .price{color:rgba(255,255,255,0.85); font-family:var(--font-mono); font-size:13px;}
  .fan-1{ background:linear-gradient(155deg,#7C3AED,#4C1D95); transform:rotate(-11deg) translate(-92px,10px); z-index:1;}
  .fan-2{ background:linear-gradient(155deg,#9D5CF0,#5B21B6); transform:rotate(-2deg) translate(6px,-18px); z-index:3;}
  .fan-3{ background:linear-gradient(155deg,#3A1671,#1B0B3B); transform:rotate(10deg) translate(96px,14px); z-index:2;}

  /* ---------- HOW IT WORKS ---------- */
  .how{background:var(--paper);}
  .section-head{max-width:640px; margin-bottom:52px;}
  .section-head h2{font-size:clamp(26px,3.4vw,36px); line-height:1.16;}
  .section-head p{margin-top:14px; color:var(--ink-soft); font-size:16px; line-height:1.6;}
  .how-steps{
    display:grid; grid-template-columns:repeat(3,1fr); gap:26px;
  }
  @media (max-width:800px){.how-steps{grid-template-columns:1fr;}}
  .step{
    background:var(--white); border:1px solid var(--line); border-radius:var(--radius-lg);
    padding:30px 26px; position:relative;
  }
  .step .num{
    font-family:var(--font-mono); font-size:13px; color:var(--violet-500); font-weight:600;
    letter-spacing:.05em;
  }
  .step h3{font-size:19px; margin-top:14px;}
  .step p{color:var(--ink-soft); margin-top:10px; font-size:14.8px; line-height:1.55;}

  /* ---------- CATALOG ---------- */
  .catalog{background:var(--lavender-bg);}
  .catalog-tabs-head{
    display:flex; align-items:flex-end; justify-content:space-between; flex-wrap:wrap; gap:20px;
    margin-bottom:44px;
  }
  .grid-cards{
    display:grid; grid-template-columns:repeat(4,1fr); gap:22px;
  }
  @media (max-width:980px){.grid-cards{grid-template-columns:repeat(2,1fr);}}
  @media (max-width:560px){.grid-cards{grid-template-columns:1fr;}}
  .card{
    background:var(--white); border-radius:var(--radius-lg); overflow:hidden;
    border:1px solid var(--line); box-shadow:var(--shadow-soft);
    display:flex; flex-direction:column;
    transition:transform .2s ease, box-shadow .2s ease;
  }
  .card:hover{transform:translateY(-4px); box-shadow:var(--shadow-card);}
  .card-cover{
    height:150px; position:relative; display:flex; align-items:flex-start; justify-content:space-between;
    padding:16px; color:#fff;
  }
  .card-cover .kicker{
    font-family:var(--font-mono); font-size:10px; text-transform:uppercase; letter-spacing:.06em;
    background:rgba(255,255,255,0.2); padding:4px 9px; border-radius:100px;
  }
  .card-cover .badge{
    background:var(--amber); color:#3A2400; font-family:var(--font-mono); font-size:10px; font-weight:600;
    padding:4px 9px; border-radius:100px;
  }
  .cov-1{background:linear-gradient(150deg,#6D28D9,#2E1065);}
  .cov-2{background:linear-gradient(150deg,#8B5CF6,#4C1D95);}
  .cov-3{background:linear-gradient(150deg,#3A1671,#160636);}
  .cov-4{background:linear-gradient(150deg,#A78BFA,#5B21B6);}
  .cov-5{background:linear-gradient(150deg,#5B21B6,#20B8A6);}
  .cov-6{background:linear-gradient(150deg,#4C1D95,#7C3AED);}
  .cov-7{background:linear-gradient(150deg,#2E1065,#6D28D9);}
  .card-body{padding:20px 20px 22px; display:flex; flex-direction:column; gap:10px; flex:1;}
  .card-body h4{font-size:17px; line-height:1.3;}
  .card-body p{font-size:13.6px; color:var(--ink-soft); line-height:1.5;}
  .card-foot{
    margin-top:auto; display:flex; align-items:center; justify-content:space-between; padding-top:12px;
    border-top:1px dashed var(--line);
  }
  .price-tag{font-family:var(--font-mono); font-weight:600; font-size:17px; color:var(--violet-700);}
  .price-tag small{display:block; font-size:10.5px; color:var(--ink-soft); font-weight:500;}

  /* ---------- PRICE LIST TABLE ---------- */
  .pricing{background:var(--paper);}
  .price-table-wrap{
    background:var(--white); border:1px solid var(--line); border-radius:var(--radius-lg);
    overflow:hidden; box-shadow:var(--shadow-soft);
  }
  table.price-table{width:100%; border-collapse:collapse;}
  table.price-table thead th{
    text-align:left; font-family:var(--font-mono); font-size:11.5px; text-transform:uppercase; letter-spacing:.06em;
    color:var(--white); background:var(--violet-700); padding:16px 22px; font-weight:600;
  }
  table.price-table tbody td{
    padding:18px 22px; border-bottom:1px solid var(--line); font-size:14.5px; vertical-align:middle;
  }
  table.price-table tbody tr:last-child td{border-bottom:none;}
  table.price-table tbody tr:nth-child(even){background:var(--lavender-bg);}
  .prod-name{font-weight:700; color:var(--ink);}
  .prod-format{
    font-family:var(--font-mono); font-size:11.5px; color:var(--ink-soft);
    background:var(--violet-100); padding:3px 9px; border-radius:100px; display:inline-block;
  }
  .prod-price{font-family:var(--font-mono); font-weight:600; color:var(--violet-700); font-size:15.5px;}
  .prod-price .old{
    display:block; font-size:11.5px; color:#B0A6C6; text-decoration:line-through; font-weight:500;
  }
  @media (max-width:760px){
    table.price-table thead{display:none;}
    table.price-table, table.price-table tbody, table.price-table tr, table.price-table td{display:block; width:100%;}
    table.price-table tbody tr{border-bottom:1px solid var(--line); padding:14px 18px;}
    table.price-table td{padding:6px 0; border:none !important;}
    table.price-table td::before{
      content:attr(data-label); display:block; font-family:var(--font-mono); font-size:10px;
      text-transform:uppercase; color:var(--violet-500); margin-bottom:2px; letter-spacing:.05em;
    }
  }

  .bundle-banner{
    margin-top:26px;
    background:linear-gradient(120deg, var(--violet-700), var(--violet-900));
    border-radius:var(--radius-lg);
    padding:32px 34px;
    display:flex; align-items:center; justify-content:space-between; gap:24px; flex-wrap:wrap;
    color:#fff;
  }
  .bundle-banner h3{color:#fff; font-size:22px;}
  .bundle-banner p{color:rgba(255,255,255,0.78); font-size:14.5px; margin-top:8px; max-width:46ch;}
  .bundle-price{text-align:right;}
  .bundle-price .old{color:rgba(255,255,255,0.55); text-decoration:line-through; font-family:var(--font-mono); font-size:13px;}
  .bundle-price .now{color:var(--amber); font-family:var(--font-display); font-size:34px; font-weight:700;}

  /* ---------- TESTIMONIALS ---------- */
  .testimonials{background:var(--lavender-bg);}
  .test-grid{display:grid; grid-template-columns:repeat(3,1fr); gap:22px;}
  @media (max-width:900px){.test-grid{grid-template-columns:1fr;}}
  .test-card{
    background:var(--white); border:1px solid var(--line); border-radius:var(--radius-lg);
    padding:26px; display:flex; flex-direction:column; gap:16px;
  }
  .stars{color:var(--amber); font-size:14px; letter-spacing:2px;}
  .test-card p.quote{font-size:14.8px; color:var(--ink); line-height:1.6;}
  .test-person{display:flex; align-items:center; gap:12px; margin-top:auto;}
  .avatar{
    width:38px; height:38px; border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    font-family:var(--font-display); font-weight:600; color:#fff; font-size:14px;
  }
  .test-person b{display:block; font-size:13.6px;}
  .test-person span{display:block; font-size:12px; color:var(--ink-soft);}

  /* ---------- FAQ ---------- */
  .faq{background:var(--paper);}
  .faq-list{max-width:820px;}
  .faq-item{border-bottom:1px solid var(--line);}
  .faq-q{
    width:100%; text-align:left; background:none; border:none; cursor:pointer;
    padding:22px 4px; display:flex; align-items:center; justify-content:space-between; gap:20px;
    font-family:var(--font-body); font-weight:700; font-size:16px; color:var(--ink);
  }
  .faq-q .plus{
    width:26px; height:26px; border-radius:50%; border:1.5px solid var(--violet-300);
    display:flex; align-items:center; justify-content:center; flex-shrink:0; position:relative;
    transition:transform .25s ease, background .25s ease;
  }
  .faq-q .plus::before, .faq-q .plus::after{
    content:""; position:absolute; background:var(--violet-600);
  }
  .faq-q .plus::before{width:10px; height:2px;}
  .faq-q .plus::after{width:2px; height:10px; transition:opacity .2s ease;}
  .faq-item.open .faq-q .plus{background:var(--violet-600); transform:rotate(90deg);}
  .faq-item.open .faq-q .plus::before, .faq-item.open .faq-q .plus::after{background:#fff;}
  .faq-item.open .faq-q .plus::after{opacity:0;}
  .faq-a{
    max-height:0; overflow:hidden; transition:max-height .3s ease;
  }
  .faq-a p{padding:0 4px 22px; color:var(--ink-soft); font-size:14.8px; line-height:1.6; max-width:70ch;}

  /* ---------- FINAL CTA ---------- */
  .final-cta{
    background:linear-gradient(135deg, var(--violet-900), var(--violet-700));
    text-align:center; position:relative; overflow:hidden;
  }
  .final-cta::before{
    content:""; position:absolute; inset:0;
    background-image:radial-gradient(circle at 50% 0%, rgba(242,184,75,0.18), transparent 55%);
  }
  .final-cta-inner{position:relative; z-index:1; max-width:640px; margin:0 auto;}
  .final-cta h2{color:#fff; font-size:clamp(26px,4vw,38px);}
  .final-cta p{color:rgba(255,255,255,0.78); margin-top:16px; font-size:16px;}
  .final-cta .hero-actions{justify-content:center; margin-top:30px;}

  /* ---------- FOOTER ---------- */
  footer{background:var(--ink); color:rgba(255,255,255,0.72); padding:64px 0 28px;}
  .footer-grid{
    display:grid; grid-template-columns:1.4fr 1fr 1fr 1.2fr; gap:40px; padding-bottom:40px;
    border-bottom:1px solid rgba(255,255,255,0.1);
  }
  @media (max-width:800px){.footer-grid{grid-template-columns:1fr 1fr;}}
  @media (max-width:520px){.footer-grid{grid-template-columns:1fr;}}
  .footer-grid h5{
    color:#fff; font-family:var(--font-mono); font-size:12px; text-transform:uppercase; letter-spacing:.06em;
    margin-bottom:16px; font-weight:600;
  }
  .footer-grid a, .footer-grid p{
    display:block; font-size:14px; color:rgba(255,255,255,0.62); margin-bottom:10px; line-height:1.5;
  }
  .footer-grid a:hover{color:var(--amber);}
  .footer-logo{color:#fff; font-family:var(--font-display); font-size:22px; font-weight:700; margin-bottom:14px;}
  .footer-logo span{color:var(--amber);}
  .footer-bottom{
    padding-top:26px; display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:14px;
    font-size:12.8px; color:rgba(255,255,255,0.45);
  }
  .pay-methods{display:flex; gap:10px; flex-wrap:wrap;}
  .pay-methods span{
    font-family:var(--font-mono); font-size:11px; border:1px solid rgba(255,255,255,0.18);
    padding:4px 10px; border-radius:6px; color:rgba(255,255,255,0.55);
  }
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <a href="#topo" class="logo">
      <svg width="34" height="34" viewBox="0 0 34 34" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect width="34" height="34" rx="10" fill="#6D28D9"/>
        <path d="M8 10L17 24L26 10" stroke="white" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
        <circle cx="26" cy="9.2" r="2.3" fill="#F2B84B"/>
      </svg>
      <span class="logo-word">visy<span>wify</span></span>
    </a>
    <nav class="nav-links" id="navLinks">
      <a href="#cursos">Cursos</a>
      <a href="#ebooks">Ebooks</a>
      <a href="#precos">Preços</a>
      <a href="#depoimentos">Depoimentos</a>
      <a href="#faq">Dúvidas</a>
    </nav>
    <div class="nav-cta">
      <a href="#precos" class="btn btn-outline btn-sm">Ver preços</a>
      <a href="#cursos" class="btn btn-primary btn-sm">Começar agora</a>
      <button class="nav-toggle" id="navToggle" aria-label="Abrir menu">
        <svg viewBox="0 0 24 24" fill="none" stroke="#1B1030" stroke-width="2" stroke-linecap="round"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
      </button>
    </div>
  </div>
</header>

<main>

  <!-- HERO -->
  <section class="hero" id="topo">
    <div class="container hero-grid">
      <div class="hero-copy">
        <span class="eyebrow">Cursos e ebooks digitais</span>
        <h1>Seu próximo nível <em>começa aqui</em>.</h1>
        <p class="lead">
          Cursos práticos, eBooks exclusivos e conteúdos que impulsionam sua evolução em qualquer
          fase da sua jornada.
        </p>
        <div class="hero-actions">
          <a href="#cursos" class="btn btn-primary">Explorar cursos</a>
          <a href="#precos" class="btn btn-ghost">Ver lista de preços</a>
        </div>
        <div class="hero-stats">
          <div class="hero-stat"><b>+2.400</b><span>ALUNOS ATIVOS</span></div>
          <div class="hero-stat"><b>6</b><span>CURSOS E EBOOKS</span></div>
          <div class="hero-stat"><b>4,8/5</b><span>AVALIAÇÃO MÉDIA</span></div>
        </div>
      </div>
      <div class="hero-visual" aria-hidden="true">
        <div class="fan-card fan-1">
          <span class="tag">Curso</span>
          <h4>IA Criadora</h4>
          <span class="price">R$ 19,98</span>
        </div>
        <div class="fan-card fan-2">
          <span class="tag">Mais vendido</span>
          <h4>Dinheiro com IA</h4>
          <span class="price">R$ 20,00</span>
        </div>
        <div class="fan-card fan-3">
          <span class="tag">Curso</span>
          <h4>Enem na Prática</h4>
          <span class="price">R$ 17,90</span>
        </div>
      </div>
    </div>
  </section>

  <!-- COMO FUNCIONA -->
  <section class="how">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow">Simples assim</span>
        <h2>Da escolha ao acesso, em três passos</h2>
        <p>Sem burocracia: você escolhe o material, finaliza a compra com segurança e recebe acesso na hora.</p>
      </div>
      <div class="how-steps">
        <div class="step">
          <span class="num">01 / ESCOLHA</span>
          <h3>Escolha o curso ou ebook</h3>
          <p>Veja a descrição, o formato e o preço de cada material na lista de preços antes de decidir.</p>
        </div>
        <div class="step">
          <span class="num">02 / COMPRA SEGURA</span>
          <h3>Finalize a compra</h3>
          <p>Pagamento processado por parceiros de confiança, com cartão, Pix ou boleto.</p>
        </div>
        <div class="step">
          <span class="num">03 / ACESSO IMEDIATO</span>
          <h3>Comece a aplicar</h3>
          <p>Receba o acesso por e-mail em minutos e comece a estudar no seu ritmo, sem prazo de expiração.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CURSOS -->
  <section class="catalog" id="cursos">
    <div class="container">
      <div class="catalog-tabs-head">
        <div class="section-head" style="margin-bottom:0;">
          <span class="eyebrow">Catálogo</span>
          <h2>Cursos em destaque</h2>
        </div>
        <a href="#precos" class="btn btn-outline btn-sm">Ver todos os preços</a>
      </div>
      <div class="grid-cards">

        <div class="card">
          <div class="card-cover cov-1">
            <span class="kicker">Renda extra</span>
            <span class="badge">Mais vendido</span>
          </div>
          <div class="card-body">
            <h4>Dinheiro com IA</h4>
            <p>Formas práticas de gerar renda extra usando ferramentas de Inteligência Artificial, mesmo começando do zero.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 20,00<small>pagamento único</small></div>
              <a href="https://pay.kiwify.com.br/4yLt5xi" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

        <div class="card">
          <div class="card-cover cov-2">
            <span class="kicker">Educação</span>
          </div>
          <div class="card-body">
            <h4>Enem na Prática</h4>
            <p>Revisão direta ao ponto das matérias que mais caem no Enem, com exercícios e estratégias de prova.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 17,90<small>pagamento único</small></div>
              <a href="https://pay.kiwify.com.br/Nf8iCBl" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

        <div class="card">
          <div class="card-cover cov-3">
            <span class="kicker">Vídeo com IA</span>
          </div>
          <div class="card-body">
            <h4>IA Criadora</h4>
            <p>Como criar vídeos com Inteligência Artificial e transformar isso em renda extra.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 19,98<small>pagamento único</small></div>
              <a href="https://pay.kiwify.com.br/PVTPemL" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- EBOOKS -->
  <section class="catalog" id="ebooks" style="padding-top:0;">
    <div class="container">
      <div class="catalog-tabs-head">
        <div class="section-head" style="margin-bottom:0;">
          <span class="eyebrow">Leitura rápida</span>
          <h2>Ebooks práticos</h2>
        </div>
      </div>
      <div class="grid-cards">

        <div class="card">
          <div class="card-cover cov-5">
            <span class="kicker">Desenvolvimento pessoal</span>
          </div>
          <div class="card-body">
            <h4>A Virada</h4>
            <p>Um guia direto para identificar o momento certo de mudar de direção e dar o primeiro passo rumo à vida que você quer.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 20,00<small>PDF digital</small></div>
              <a href="https://pay.kiwify.com.br/xVHKNml" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

        <div class="card">
          <div class="card-cover cov-6">
            <span class="kicker">Relacionamentos</span>
          </div>
          <div class="card-body">
            <h4>Amor em Sintonia</h4>
            <p>Reflexões e exercícios práticos para fortalecer a comunicação e a conexão no relacionamento a dois.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 30,00<small>PDF digital</small></div>
              <a href="https://pay.kiwify.com.br/fBT4j9t" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

        <div class="card">
          <div class="card-cover cov-7">
            <span class="kicker">Autoconhecimento</span>
          </div>
          <div class="card-body">
            <h4>O Mapa da Transformação</h4>
            <p>Um passo a passo para sair do piloto automático e conduzir, com clareza, sua própria transformação pessoal.</p>
            <div class="card-foot">
              <div class="price-tag">R$ 16,45<small>PDF digital</small></div>
              <a href="https://pay.kiwify.com.br/h0gmTR0" target="_blank" rel="noopener" class="btn btn-outline btn-sm">Comprar</a>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- LISTA DE PREÇOS -->
  <section class="pricing" id="precos">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow">Transparência total</span>
        <h2>Lista de preços</h2>
        <p>Sem letras miúdas: todos os cursos e ebooks, formato e valor em um só lugar.</p>
      </div>

      <div class="price-table-wrap">
        <table class="price-table">
          <thead>
            <tr>
              <th>Produto</th>
              <th>Formato</th>
              <th>Preço</th>
              <th></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td data-label="Produto"><span class="prod-name">Dinheiro com IA</span></td>
              <td data-label="Formato"><span class="prod-format">Curso · vídeo + PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 20,00</span></td>
              <td><a href="https://pay.kiwify.com.br/4yLt5xi" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
            <tr>
              <td data-label="Produto"><span class="prod-name">Enem na Prática</span></td>
              <td data-label="Formato"><span class="prod-format">Curso · vídeo + PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 17,90</span></td>
              <td><a href="https://pay.kiwify.com.br/Nf8iCBl" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
            <tr>
              <td data-label="Produto"><span class="prod-name">IA Criadora</span></td>
              <td data-label="Formato"><span class="prod-format">Curso · vídeo + PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 19,98</span></td>
              <td><a href="https://pay.kiwify.com.br/PVTPemL" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
            <tr>
              <td data-label="Produto"><span class="prod-name">A Virada</span></td>
              <td data-label="Formato"><span class="prod-format">Ebook · PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 20,00</span></td>
              <td><a href="https://pay.kiwify.com.br/xVHKNml" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
            <tr>
              <td data-label="Produto"><span class="prod-name">Amor em Sintonia</span></td>
              <td data-label="Formato"><span class="prod-format">Ebook · PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 30,00</span></td>
              <td><a href="https://pay.kiwify.com.br/fBT4j9t" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
            <tr>
              <td data-label="Produto"><span class="prod-name">O Mapa da Transformação</span></td>
              <td data-label="Formato"><span class="prod-format">Ebook · PDF</span></td>
              <td data-label="Preço"><span class="prod-price">R$ 16,45</span></td>
              <td><a href="https://pay.kiwify.com.br/h0gmTR0" target="_blank" rel="noopener" class="btn btn-primary btn-sm">Comprar</a></td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="bundle-banner">
        <div>
          <h3>Combo Completo Visywify</h3>
          <p>Todos os 3 cursos e os 3 ebooks, em um único pacote com acesso vitalício.</p>
        </div>
        <div class="bundle-price">
          <span class="old">de R$ 149,20</span>
          <div class="now">R$ 119,97</div>
          <a href="#" class="btn btn-primary btn-sm" style="margin-top:8px;">Quero o combo</a>
        </div>
      </div>
    </div>
  </section>

  <!-- DEPOIMENTOS -->
  <section class="testimonials" id="depoimentos">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow">Quem já estudou</span>
        <h2>O que dizem os alunos</h2>
      </div>
      <div class="test-grid">
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p class="quote">"Comprei o IA Criadora sem saber nada sobre o assunto e em uma semana já tinha
          entregado meu primeiro vídeo para um cliente. Direto ao ponto, sem enrolação."</p>
          <div class="test-person">
            <div class="avatar" style="background:#6D28D9;">M</div>
            <div><b>Marina T.</b><span>Freelancer de conteúdo</span></div>
          </div>
        </div>
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p class="quote">"O ebook de prompts sozinho já valeu o investimento. Uso praticamente todo dia
          no meu trabalho."</p>
          <div class="test-person">
            <div class="avatar" style="background:#8B5CF6;">R</div>
            <div><b>Rafael S.</b><span>Analista de marketing</span></div>
          </div>
        </div>
        <div class="test-card">
          <div class="stars">★★★★★</div>
          <p class="quote">"Comprei o combo completo e recomendo. Material objetivo, com exemplos
          práticos que consegui aplicar no mesmo dia."</p>
          <div class="test-person">
            <div class="avatar" style="background:#4C1D95;">C</div>
            <div><b>Camila R.</b><span>Autônoma</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="faq" id="faq">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow">Dúvidas frequentes</span>
        <h2>Perguntas antes de comprar</h2>
      </div>
      <div class="faq-list">
        <div class="faq-item open">
          <button class="faq-q">Como recebo o acesso após a compra?<span class="plus"></span></button>
          <div class="faq-a"><p>O acesso é enviado por e-mail assim que o pagamento é aprovado, com o link
          de download ou entrada na área de membros, dependendo do produto.</p></div>
        </div>
        <div class="faq-item">
          <button class="faq-q">Quais formas de pagamento são aceitas?<span class="plus"></span></button>
          <div class="faq-a"><p>Cartão de crédito, Pix e boleto bancário, processados por uma plataforma
          de pagamentos parceira, com ambiente seguro.</p></div>
        </div>
        <div class="faq-item">
          <button class="faq-q">O acesso tem prazo de validade?<span class="plus"></span></button>
          <div class="faq-a"><p>Não. Após a compra, o acesso ao curso ou ebook é vitalício, no seu próprio ritmo.</p></div>
        </div>
        <div class="faq-item">
          <button class="faq-q">Existe garantia caso eu não goste do material?<span class="plus"></span></button>
          <div class="faq-a"><p>Sim, todos os produtos contam com garantia de 7 dias. Se o conteúdo não for
          para você, basta solicitar o reembolso dentro desse prazo.</p></div>
        </div>
        <div class="faq-item">
          <button class="faq-q">Preciso de conhecimento prévio para começar?<span class="plus"></span></button>
          <div class="faq-a"><p>Não. Os materiais foram escritos para quem está começando do zero, com
          linguagem simples e exemplos práticos.</p></div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA FINAL -->
  <section class="final-cta">
    <div class="container final-cta-inner">
      <h2>Pronto para aprender algo novo hoje?</h2>
      <p>Escolha um curso ou ebook e comece a aplicar o conteúdo ainda esta semana.</p>
      <div class="hero-actions">
        <a href="#precos" class="btn btn-primary">Ver lista de preços</a>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div>
        <div class="footer-logo">visy<span>wify</span></div>
        <p>Cursos e ebooks práticos para aprender e aplicar habilidades digitais no seu ritmo.</p>
      </div>
      <div>
        <h5>Catálogo</h5>
        <a href="#cursos">Cursos</a>
        <a href="#ebooks">Ebooks</a>
        <a href="#precos">Lista de preços</a>
      </div>
      <div>
        <h5>Suporte</h5>
        <a href="#faq">Dúvidas frequentes</a>
        <a href="mailto:contato@visywify.com">Falar com o suporte</a>
        <a href="#">Política de reembolso</a>
      </div>
      <div>
        <h5>Contato</h5>
        <p>contato@visywify.com</p>
        <p>Atendimento: seg. a sex., 9h às 18h</p>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 Visywify. Todos os direitos reservados.</span>
      <div class="pay-methods">
        <span>Cartão</span><span>Pix</span><span>Boleto</span>
      </div>
    </div>
  </div>
</footer>

<script>
  // menu mobile
  const navToggle = document.getElementById('navToggle');
  const navLinks = document.getElementById('navLinks');
  navToggle.addEventListener('click', () => {
    navLinks.classList.toggle('open');
  });
  navLinks.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', () => navLinks.classList.remove('open'));
  });

  // FAQ accordion
  document.querySelectorAll('.faq-item').forEach(item => {
    const answer = item.querySelector('.faq-a');
    if(item.classList.contains('open')){
      answer.style.maxHeight = answer.scrollHeight + 'px';
    }
    item.querySelector('.faq-q').addEventListener('click', () => {
      const isOpen = item.classList.contains('open');
      document.querySelectorAll('.faq-item').forEach(i => {
        i.classList.remove('open');
        i.querySelector('.faq-a').style.maxHeight = null;
      });
      if(!isOpen){
        item.classList.add('open');
        answer.style.maxHeight = answer.scrollHeight + 'px';
      }
    });
  });
</script>

</body>
</html>
