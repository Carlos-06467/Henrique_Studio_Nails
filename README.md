<!DOCTYPE html>        
<html lang="pt-BR">        
<head>        
  <meta charset="UTF-8">        
  <meta name="viewport" content="width=device-width, initial-scale=1.0">        
  <title>Manicure Premium</title>        
        
  <style>        
    body {        
      margin: 0;        
      font-family: Arial;        
      background: #0a0a0a;        
      color: white;        
    }        
        
    header {        
      height: 100vh;        
      display: flex;        
      flex-direction: column;        
      justify-content: center;        
      align-items: center;        
      text-align: center;        
      background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.8)),        
      url('investimentosfoto.png');        
      background-size: cover;        
      background-position: center;        
    }        
        
    h1 {        
      font-size: 1.8rem;        
      color: white;        
    }        
        
    h2 {        
      color: #e6c14a;        
      text-shadow: 0 0 10px rgba(230, 193, 74, 0.25);        
      letter-spacing: 1px;        
      margin-bottom: 15px;        
      transition: 0.3s ease;        
    }        
        
    h2:hover {        
      color: #ffd76a;        
    }        
        
    .insta-link {        
      color: white;        
      text-decoration: none;        
      margin-top: 5px;        
      font-size: 14px;        
    }        
        
    .insta-link:hover {        
      color: gold;        
    }        
        
    .btn {        
      padding: 12px 25px;        
      margin: 6px;        
      border: none;        
      cursor: pointer;        
      font-size: 16px;        
      border-radius: 8px;        
    }        
        
    .btn-primary { background: green; color: white; }        
    .btn-secondary { background: white; color: black; }        
        
    section {        
      padding: 40px 20px;        
      text-align: center;        
    }        
        
    /* ===== CARROSSEL AJUSTADO ===== */  
    .carousel {        
      position: relative;        
      width: 100%;        
      max-width: 600px;        
      margin: auto;        
      height: 480px;        
      overflow: hidden;  
    }        
        
    .carousel img {        
      position: absolute;        
      top: 0;        
      left: 0;        
      width: 100%;        
      height: 100%;        
      object-fit: cover;        
      border-radius: 10px;        
      opacity: 0;        
      transition: opacity 0.6s ease;        
    }        
        
    .carousel img.active {        
      opacity: 1;        
    }        
  
    /* BOTÕES DO CARROSSEL */  
    .carousel-btn {  
      position: absolute;  
      top: 50%;  
      transform: translateY(-50%);  
      background: rgba(0,0,0,0.6);  
      border: none;  
      color: white;  
      font-size: 22px;  
      padding: 10px 14px;  
      cursor: pointer;  
      z-index: 10;  
      border-radius: 8px;  
    }  
  
    .carousel-btn:hover {  
      background: rgba(255,215,0,0.5);  
    }  
  
    .prev { left: 10px; }  
    .next { right: 10px; }  
  
    /* resto original intacto */  
    .style-images {        
      display: flex;        
      justify-content: center;        
      gap: 10px;        
      margin-top: 10px;        
    }        
        
    .style-images img {        
      width: 150px;        
      border-radius: 10px;        
      opacity: 0;        
      transform: translateY(20px);        
      transition: all 0.5s ease;        
    }        
        
    .style-images img.show {        
      opacity: 1;        
      transform: translateY(0);        
    }        
        
    .seta {        
      width: 90px;        
      margin: 10px auto 0 auto;        
      display: block;        
      cursor: pointer;        
      transition: 0.3s ease;        
    }        
        
    .seta:hover {        
      transform: scale(1.1);        
    }        
        
    .services {        
      display: flex;        
      flex-wrap: wrap;        
      justify-content: center;        
      gap: 20px;        
      background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.8)),        
      url('iperoxo.png');        
      background-size: cover;        
      background-position: center;        
    }        
        
    .card {        
      background: #1a1a1a;        
      padding: 20px;        
      border-radius: 12px;        
      width: 200px;        
      border: 1px solid gray;        
      cursor: pointer;        
    }        
        
    .card:hover {        
      border-color: gold;        
    }        
        
    .message-box {        
      margin-top: 20px;        
      padding: 15px;        
      background: #111;        
      border-radius: 10px;        
      display: none;        
    }        
        
    .msg-inner {        
      min-height: 70px;        
    }        
        
    .products {        
      display: flex;        
      overflow-x: auto;        
      gap: 15px;        
      padding: 10px;        
    }        
        
    .product {        
      min-width: 150px;        
      background: #111;        
      padding: 15px;        
      border-radius: 10px;        
      border: 1px solid white;        
      color: #ff7a18;        
      cursor: pointer;
      transition: 0.3s;
    }        

    .product:hover {
      transform: scale(1.05);
      border-color: gold;
    }
        
    .testimonials, .about {        
      max-width: 700px;        
      margin: auto;        
    }        
        
    .testimonial {        
      background: #111;        
      padding: 15px;        
      border-radius: 10px;        
      margin: 10px 0;        
      border: 1px solid gray;        
    }        
        
    footer {        
      background: black;        
      padding: 20px;        
    }        
  
    .btn-whatsapp-footer{  
      white-space: nowrap;  
      text-decoration: none;  
      display: inline-block;  
    }  
        
    .fire-title {        
      position: relative;        
      display: inline-block;        
      font-size: 1.8rem;        
      letter-spacing: 2px;        
      text-align: center;        
        
      background: linear-gradient(        
        120deg,        
        #ffb300,        
        #ff3d00,        
        #ffcc00,        
        #ff3d00        
      );        
      background-size: 300% 100%;        
        
      color: transparent;        
      -webkit-text-fill-color: transparent;        
      -webkit-background-clip: text;        
      background-clip: text;        
        
      animation: fireSweep 1.6s linear infinite;        
        
      text-shadow:        
        0 0 6px rgba(255, 80, 0, 0.6),        
        0 0 14px rgba(255, 30, 0, 0.4);        
    }        
        
    @keyframes fireSweep {        
      0% { background-position: 0% 50%; }        
      50% { background-position: 100% 50%; }        
      100% { background-position: 0% 50%; }        
    }        
        
    .fire-title::before {        
      content: "";        
      position: absolute;       
      inset: -8px;        
      background: radial-gradient(circle, rgba(255, 80, 0, 0.35), transparent 70%);        
      z-index: -1;        
      border-radius: 10px;        
      animation: auraPulse 1.5s infinite ease-in-out;        
    }        
        
    @keyframes auraPulse {        
      0%, 100% { transform: scale(1); opacity: 0.6; }        
      50% { transform: scale(1.15); opacity: 1; }        
    }        
        
    .blue-fire {
      margin: 40px 20px;
      padding: 30px 20px;
      border-radius: 15px;
      cursor: pointer;
      text-align: center;

      background: linear-gradient(
        120deg,
        #00cfff,
        #0044ff,
        #00e0ff,
        #0044ff
      );
      background-size: 300% 100%;

      animation: blueFireMove 2s linear infinite;

      box-shadow:
        0 0 10px rgba(0, 140, 255, 0.6),
        0 0 25px rgba(0, 80, 255, 0.5),
        0 0 40px rgba(0, 150, 255, 0.4);
    }

    .blue-fire h2 {
      color: white;
      text-shadow:
        0 0 8px rgba(0, 200, 255, 0.9),
        0 0 20px rgba(0, 120, 255, 0.8),
        0 0 35px rgba(0, 80, 255, 0.7);
    }

    @keyframes blueFireMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .voice-btn {
      background: #111;
      color: #00cfff;
      border: 1px solid #00cfff;
      padding: 8px 14px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
      font-size: 14px;
    }

    .voice-btn:hover {
      background: #00cfff;
      color: black;
    }

    .blue-fire:hover {
      transform: scale(1.03);
    }
  </style>        
</head>        
        
<body>        
        
<header>        
  <h1>@henrique_studio_nails</h1>        
  <a href="https://instagram.com/henrique_studio_nails" target="_blank" class="insta-link">📸 Instagram</a>        
        
  <p style="color: gold;">        
    Atendimento para homens e mulheres, "cuidado e detalhes que valorizam sua beleza". 
  </p>        
        
  <button class="btn btn-primary" onclick="agendar()">Agendar Agora</button>        
  <button class="btn btn-secondary" onclick="scrollToSection('galeria')">Ver Trabalhos</button>        
</header>        
        
<section id="galeria">        
  <h2>Valores e Localização</h2>        
        
  <div class="carousel" id="carousel1">        
    <button class="carousel-btn prev" onclick="mudarSlide('carousel1', -1)">‹</button>  
    <button class="carousel-btn next" onclick="mudarSlide('carousel1', 1)">›</button>  
  
    <img src="tabelamanicure.png" class="active">        
    <img src="localmanicure.png">    
    <img src="logoprincipal.png">        
  </div>        
        
  <h2>Sobre meu atendimento</h2>  
  
  <div class="about">        
    <p>        
      Trabalho com atenção aos detalhes, higiene e conforto, proporcionando uma experiência única para cada cliente.        
      Meu objetivo é valorizar sua beleza com cuidado e perfeição.        
    </p>        

    <section class="blue-fire" onclick="window.open('https://instagram.com/henrique_studio_nails', '_blank')">
  <h2>Veja mais sobre meu trabalho. Transformo detalhes em destaque. 💙</h2>
</section>

  </div>        
</section>        
        
<section>        
  <h2 class="fire-title">Produtos</h2>        
        
  <div class="products">        
    <div class="product" onclick="comprarProduto('Óleo  Reparador de Pontas')">Óleo Reparador de Pontas</div>
<div class="product" onclick="comprarProduto('Hidratante de Cutícula')">Hidratante de Cutícula</div>      
    <div class="product" onclick="comprarProduto('Kit Cuidados das Unhas')">Kit Cuidados das Unhas</div>        
  </div>        
</section>        
        
<footer>        
  <a href="https://wa.me/558894731041" target="_blank" class="btn btn-primary btn-whatsapp-footer">  
    Agende seu horário agora pelo WhatsApp  
  </a>  
</footer>        
        
<script>        
  function agendar() {
    const numero = '558894731041';
    const mensagem = 'Olá! Gostaria de agendar um horário com você. Quais horários disponíveis?';
    const url = `https://wa.me/${numero}?text=${encodeURIComponent(mensagem)}`;
    window.open(url, '_blank');
  }
        
  function scrollToSection(id) {        
    document.getElementById(id).scrollIntoView({ behavior: 'smooth' });        
  }        
        
  function mostrarEstilo(tipo) {        
    let texto = '';        
        
    if (tipo === 'simples') texto = 'Estilo simples, elegante e discreto';        
    if (tipo === 'luxo') texto = 'Estilo luxo com brilho e destaque';        
    if (tipo === 'decorada') texto = 'Estilo criativo, moderno e personalizado';        
        
    document.getElementById('resultado').innerText = texto;        
        
    const imgs = document.querySelectorAll('#styleBox img');        
    imgs.forEach((img, i) => {        
      img.classList.remove('show');        
      setTimeout(() => img.classList.add('show'), i * 300);        
    });        
  }        
  
  /* CARROSSEL CONTROLADO */  
  let slides = {  
    carousel1: 0,  
    carousel2: 0  
  };  
  
  function mudarSlide(id, direction) {  
    const carousel = document.getElementById(id);  
    const images = carousel.querySelectorAll("img");  
  
    images[slides[id]].classList.remove("active");  
  
    slides[id] = (slides[id] + direction + images.length) % images.length;  
  
    images[slides[id]].classList.add("active");  
  }  
  
  let servicoAtual = null;

  function mensagem(tipo) {        
    const box = document.getElementById('msgBox');        
    const text = document.getElementById('msgText');        

    if (servicoAtual === tipo) {
      box.style.display = 'none';
      servicoAtual = null;
      return;
    }

    let mensagemAtual = '';  

    if (tipo === 'manicure') {  
      mensagemAtual = 'Oi! 😊 Quero cuidar das minhas unhas com você. Pode me dizer os horários disponíveis?';  
    }  

    if (tipo === 'pedicure') {  
      mensagemAtual = 'Oi! 😊 Quero deixar meus pés bem cuidados com você. Quais horários você tem disponíveis?';  
    }  

    if (tipo === 'decorada') {  
      mensagemAtual = 'Olá! 💅✨ Quero fazer unhas decoradas com você, adorei seu estilo! Quais horários estão disponíveis?';  
    }  

    text.innerText = mensagemAtual;  
    box.style.display = 'block';  
    servicoAtual = tipo;
  }

  function comprarProduto(nomeProduto) {
    const numero = '558894731041';
    const mensagem = `Olá! 😊 Estou interessado neste produto: "${nomeProduto}". Gostaria de saber mais sobre ele.`;
    const url = `https://wa.me/${numero}?text=${encodeURIComponent(mensagem)}`;
    window.open(url, '_blank');
  }

  function abrirTrabalhos() {
    window.location.href = "trabalhos.html";
  }
</script>        
        
</body>        
</html>
