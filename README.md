# vale-do-macacão
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Associação de Mini Produtores Rurais Vale do Macacão</title>
  <meta name="description" content="Associação de Mini Produtores Rurais Vale do Macacão - Agricultura familiar, produção local e desenvolvimento comunitário." />

  <style>
    :root{
      --orange:#ff6a00;
      --black:#0b0b0b;
      --white:#ffffff;
      --gray:#f3f3f3;
      --text:#1f1f1f;
      --shadow: 0 12px 30px rgba(0,0,0,.12);
      --radius: 18px;
    }

    *{ margin:0; padding:0; box-sizing:border-box; }
    body{
      font-family: Arial, Helvetica, sans-serif;
      background: var(--white);
      color: var(--text);
      line-height: 1.6;
    }
    a{ text-decoration:none; color: inherit; }

    /* Header */
    header{
      position: sticky;
      top: 0;
      z-index: 999;
      background: rgba(255,255,255,.92);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(0,0,0,.06);
    }
    .nav{
      max-width: 1200px;
      margin: 0 auto;
      padding: 14px 18px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 14px;
    }
    .brand{
      display:flex;
      align-items:center;
      gap: 10px;
      font-weight: 800;
      letter-spacing: .3px;
    }
    .logo{
      width: 40px;
      height: 40px;
      border-radius: 12px;
      background: linear-gradient(135deg, var(--orange), #ff9a3c);
      box-shadow: 0 10px 22px rgba(255,106,0,.35);
      display:grid;
      place-items:center;
      color:#fff;
      font-weight:900;
    }
    nav ul{
      list-style:none;
      display:flex;
      gap: 16px;
      align-items:center;
      flex-wrap:wrap;
      justify-content:flex-end;
    }
    nav ul li a{
      padding: 10px 12px;
      border-radius: 12px;
      font-weight: 700;
      color: #222;
      transition: .2s;
    }
    nav ul li a:hover{
      background: rgba(255,106,0,.10);
      color: var(--orange);
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap: 10px;
      padding: 12px 16px;
      border-radius: 14px;
      font-weight: 800;
      transition: .2s;
      border: 2px solid transparent;
      cursor:pointer;
      user-select:none;
    }
    .btn-primary{
      background: var(--orange);
      color: #fff;
      box-shadow: 0 12px 24px rgba(255,106,0,.22);
    }
    .btn-primary:hover{ filter: brightness(.95); transform: translateY(-1px); }
    .btn-outline{
      border-color: rgba(0,0,0,.15);
      background: #fff;
      color: #111;
    }
    .btn-outline:hover{
      border-color: var(--orange);
      color: var(--orange);
      background: rgba(255,106,0,.08);
    }

    /* Hero */
    .hero{
      background:
        radial-gradient(800px 500px at 20% 10%, rgba(255,106,0,.22), transparent 60%),
        radial-gradient(800px 500px at 80% 20%, rgba(0,0,0,.12), transparent 60%),
        linear-gradient(180deg, #fff, #fff);
    }
    .hero-wrap{
      max-width: 1200px;
      margin: 0 auto;
      padding: 64px 18px 30px;
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 26px;
      align-items:center;
    }
    .hero h1{
      font-size: clamp(28px, 4vw, 46px);
      line-height: 1.1;
      margin-bottom: 14px;
      font-weight: 900;
      color: #0f0f0f;
    }
    .hero p{
      font-size: 16px;
      color: #333;
      max-width: 560px;
      margin-bottom: 22px;
    }
    .hero-actions{
      display:flex;
      gap: 12px;
      flex-wrap:wrap;
      margin-bottom: 18px;
    }
    .hero-badges{
      display:flex;
      gap: 10px;
      flex-wrap:wrap;
      margin-top: 8px;
    }
    .badge{
      background: rgba(0,0,0,.06);
      border: 1px solid rgba(0,0,0,.08);
      padding: 8px 12px;
      border-radius: 999px;
      font-weight: 800;
      font-size: 13px;
      color:#222;
    }

    .hero-card{
      background: #fff;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      border: 1px solid rgba(0,0,0,.06);
      overflow:hidden;
    }
    .hero-card-top{
      padding: 18px 18px 10px;
      border-bottom: 1px solid rgba(0,0,0,.06);
      display:flex;
      align-items:flex-start;
      justify-content:space-between;
      gap: 12px;
    }
    .hero-card-top h3{
      font-size: 18px;
      font-weight: 900;
      color:#111;
    }
    .hero-card-top span{
      font-size: 12px;
      font-weight: 900;
      color: #fff;
      background: var(--black);
      padding: 7px 10px;
      border-radius: 999px;
    }
    .hero-card-body{
      padding: 18px;
      display:grid;
      gap: 12px;
    }
    .info{
      display:flex;
      gap: 12px;
      align-items:flex-start;
      padding: 12px;
      border-radius: 14px;
      background: var(--gray);
      border: 1px solid rgba(0,0,0,.06);
    }
    .dot{
      width: 12px;
      height: 12px;
      border-radius: 50%;
      margin-top: 5px;
      background: var(--orange);
      flex: 0 0 auto;
    }
    .info strong{ display:block; font-weight: 900; }
    .info small{ color:#444; }

    /* Sections */
    section{
      max-width: 1200px;
      margin: 0 auto;
      padding: 56px 18px;
    }
    .section-title{
      display:flex;
      align-items:flex-end;
      justify-content:space-between;
      gap: 14px;
      margin-bottom: 22px;
      flex-wrap:wrap;
    }
    .section-title h2{
      font-size: 28px;
      font-weight: 900;
      color:#111;
    }
    .section-title p{
      max-width: 650px;
      color:#444;
      font-weight: 600;
    }

    .grid{
      display:grid;
      gap: 16px;
    }
    .grid-3{ grid-template-columns: repeat(3, 1fr); }
    .grid-2{ grid-template-columns: repeat(2, 1fr); }

    .card{
      background:#fff;
      border-radius: var(--radius);
      border: 1px solid rgba(0,0,0,.06);
      box-shadow: 0 10px 24px rgba(0,0,0,.06);
      padding: 18px;
      transition: .2s;
    }
    .card:hover{
      transform: translateY(-2px);
      box-shadow: 0 14px 30px rgba(0,0,0,.10);
      border-color: rgba(255,106,0,.25);
    }
    .card h3{
      font-size: 18px;
      font-weight: 900;
      margin-bottom: 8px;
    }
    .card p{
      color:#444;
      font-weight: 600;
      font-size: 14px;
    }
    .icon{
      width: 46px;
      height: 46px;
      border-radius: 16px;
      background: rgba(255,106,0,.12);
      border: 1px solid rgba(255,106,0,.20);
      display:grid;
      place-items:center;
      font-size: 20px;
      margin-bottom: 10px;
    }

    /* Products */
    .product{
      display:flex;
      align-items:flex-start;
      justify-content:space-between;
      gap: 12px;
      padding: 14px;
      border-radius: 16px;
      border: 1px solid rgba(0,0,0,.06);
      background: #fff;
    }
    .product strong{ font-weight: 900; }
    .product span{
      font-weight: 900;
      color: var(--orange);
      white-space:nowrap;
    }

    /* Contact */
    .contact{
      background: linear-gradient(135deg, rgba(255,106,0,.12), rgba(0,0,0,.06));
      border-radius: 24px;
      padding: 24px;
      border: 1px solid rgba(0,0,0,.06);
      box-shadow: var(--shadow);
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
      align-items:start;
    }
    .contact h3{
      font-size: 22px;
      font-weight: 900;
      margin-bottom: 10px;
    }
    .contact p{ color:#333; font-weight: 600; }
    .contact-list{
      display:grid;
      gap: 10px;
      margin-top: 14px;
    }
    .contact-item{
      padding: 12px;
      border-radius: 14px;
      background: rgba(255,255,255,.85);
      border: 1px solid rgba(0,0,0,.06);
      font-weight: 800;
    }
    .map{
      border-radius: 20px;
      overflow:hidden;
      border: 1px solid rgba(0,0,0,.06);
      min-height: 280px;
      background:#fff;
    }
    iframe{ width:100%; height:100%; border:0; }

    /* Footer */
    footer{
      background: var(--black);
      color: #fff;
      padding: 26px 18px;
      margin-top: 30px;
    }
    .footer-wrap{
      max-width: 1200px;
      margin: 0 auto;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 14px;
      flex-wrap:wrap;
    }
    .footer-wrap small{ opacity: .85; font-weight: 600; }

    /* Floating WhatsApp */
    .whats{
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 999;
      width: 56px;
      height: 56px;
      border-radius: 18px;
      display:grid;
      place-items:center;
      background: #25D366;
      box-shadow: 0 16px 30px rgba(0,0,0,.22);
      font-size: 26px;
      color: #fff;
      font-weight: 900;
      transition: .2s;
    }
    .whats:hover{ transform: translateY(-2px); filter: brightness(.95); }

    /* Responsive */
    @media (max-width: 920px){
      .hero-wrap{ grid-template-columns: 1fr; padding-top: 44px; }
      .grid-3{ grid-template-columns: 1fr; }
      .grid-2{ grid-template-columns: 1fr; }
      .contact{ grid-template-columns: 1fr; }
      nav ul{ display:none; }
    }
  </style>
</head>

<body>

  <!-- HEADER -->
  <header>
    <div class="nav">
      <div class="brand">
        <div class="logo">VM</div>
        <div>
          <div style="font-size:14px; font-weight:900; line-height:1.1;">Vale do Macacão</div>
          <div style="font-size:12px; opacity:.8; font-weight:700;">Associação de Mini Produtores Rurais</div>
        </div>
      </div>

      <nav>
        <ul>
          <li><a href="#inicio">Início</a></li>
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#produtos">Produção</a></li>
          <li><a href="#projetos">Projetos</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </nav>

      <a class="btn btn-primary" href="#contato">Falar com a Associação</a>
    </div>
  </header>

  <!-- HERO -->
  <div class="hero" id="inicio">
    <div class="hero-wrap">
      <div>
        <h1>Associação de Mini Produtores Rurais<br/>Vale do Macacão</h1>
        <p>
          Somos uma associação voltada para o fortalecimento da <strong>agricultura familiar</strong>,
          geração de renda e desenvolvimento comunitário. Produção local, trabalho sério e compromisso com a comunidade.
        </p>

        <div class="hero-actions">
          <a class="btn btn-primary" id="btnWhatsHero" href="#">📲 Comprar / Falar no WhatsApp</a>
          <a class="btn btn-outline" href="#produtos">🌿 Ver Produção</a>
        </div>

        <div class="hero-badges">
          <div class="badge">🌾 Agricultura Familiar</div>
          <div class="badge">🤝 Comunidade</div>
          <div class="badge">💧 Produção com qualidade</div>
        </div>
      </div>

      <div class="hero-card">
        <div class="hero-card-top">
          <div>
            <h3>Informações rápidas</h3>
            <small style="color:#444; font-weight:700;">Atualizado e pronto para parcerias</small>
          </div>
          <span>Oficial</span>
        </div>
        <div class="hero-card-body">
          <div class="info">
            <div class="dot"></div>
            <div>
              <strong>Objetivo</strong>
              <small>Organizar a produção e fortalecer os mini produtores com apoio técnico e união.</small>
            </div>
          </div>

          <div class="info">
            <div class="dot"></div>
            <div>
              <strong>Atuação</strong>
              <small>Produção rural, comercialização local, capacitações e projetos comunitários.</small>
            </div>
          </div>

          <div class="info">
            <div class="dot"></div>
            <div>
              <strong>Contato rápido</strong>
              <small>WhatsApp oficial e e-mail para parcerias e pedidos.</small>
            </div>
          </div>

          <a class="btn btn-primary" href="#contato">📌 Ver Contato e Localização</a>
        </div>
      </div>
    </div>
  </div>

  <!-- SOBRE -->
  <section id="sobre">
    <div class="section-title">
      <h2>Sobre a Associação</h2>
      <p>
        Trabalhamos com união e transparência para fortalecer os produtores rurais,
        melhorar a renda das famílias e incentivar o desenvolvimento local.
      </p>
    </div>

    <div class="grid grid-3">
      <div class="card">
        <div class="icon">🎯</div>
        <h3>Missão</h3>
        <p>Fortalecer a agricultura familiar, apoiando mini produtores rurais com organização e projetos.</p>
      </div>

      <div class="card">
        <div class="icon">🌱</div>
        <h3>Produção</h3>
        <p>Hortaliças, frutas e produtos locais, com cuidado e responsabilidade para levar qualidade ao consumidor.</p>
      </div>

      <div class="card">
        <div class="icon">🤝</div>
        <h3>Comunidade</h3>
        <p>Realizamos ações comunitárias, capacitações e buscamos parcerias com instituições e programas.</p>
      </div>
    </div>
  </section>

  <!-- PRODUÇÃO -->
  <section id="produtos">
    <div class="section-title">
      <h2>Produção e Produtos</h2>
      <p>Exemplos do que a associação pode oferecer. Você pode editar a lista conforme a produção real.</p>
    </div>

    <div class="grid grid-2">
      <div class="card">
        <div class="icon">🥬</div>
        <h3>Hortaliças</h3>
        <div style="display:grid; gap:10px; margin-top:12px;">
          <div class="product"><strong>Alface</strong> <span>Disponível</span></div>
          <div class="product"><strong>Couve</strong> <span>Disponível</span></div>
          <div class="product"><strong>Coentro / Cebolinha</strong> <span>Disponível</span></div>
          <div class="product"><strong>Rúcula</strong> <span>Sazonal</span></div>
        </div>
      </div>

      <div class="card">
        <div class="icon">🍠</div>
        <h3>Raízes e Outros</h3>
        <div style="display:grid; gap:10px; margin-top:12px;">
          <div class="product"><strong>Mandioca</strong> <span>Disponível</span></div>
          <div class="product"><strong>Batata-doce</strong> <span>Disponível</span></div>
          <div class="product"><strong>Abóbora</strong> <span>Sazonal</span></div>
          <div class="product"><strong>Milho / Feijão</strong> <span>Conforme safra</span></div>
        </div>
      </div>
    </div>

    <div style="margin-top:18px; display:flex; gap:12px; flex-wrap:wrap;">
      <a class="btn btn-primary" id="btnWhatsProdutos" href="#">📲 Fazer Pedido no WhatsApp</a>
      <a class="btn btn-outline" href="#contato">📍 Ver Localização</a>
    </div>
  </section>

  <!-- PROJETOS -->
  <section id="projetos">
    <div class="section-title">
      <h2>Projetos e Ações</h2>
      <p>Área ideal para mostrar ações e atrair parcerias (SEBRAE, SENAR, prefeitura, IF, universidades).</p>
    </div>

    <div class="grid grid-3">
      <div class="card">
        <div class="icon">☀️</div>
        <h3>Irrigação e Energia Solar</h3>
        <p>Projetos de bombeamento solar, irrigação por gotejamento e melhoria na produção.</p>
      </div>

      <div class="card">
        <div class="icon">📚</div>
        <h3>Capacitações</h3>
        <p>Treinamentos sobre produção, controle de gastos, vendas e organização comunitária.</p>
      </div>

      <div class="card">
        <div class="icon">🚚</div>
        <h3>Comercialização</h3>
        <p>Fortalecimento de feiras, entregas locais e parcerias com mercados e restaurantes.</p>
      </div>
    </div>
  </section>

  <!-- CONTATO -->
  <section id="contato">
    <div class="section-title">
      <h2>Contato e Localização</h2>
      <p>Edite os contatos abaixo com os dados oficiais da associação.</p>
    </div>

    <div class="contact">
      <div>
        <h3>Fale com a Associação</h3>
        <p>
          Entre em contato para pedidos, parcerias, projetos e apoio à agricultura familiar.
        </p>

        <div class="contact-list">
          <div class="contact-item">📲 WhatsApp: <span id="whatsNumberText">(61) 90000-0000</span></div>
          <div class="contact-item">📧 E-mail: <span>valedomacacao@email.com</span></div>
          <div class="contact-item">📍 Local: <span>Assentamento Vale do Macacão - (Cidade/UF)</span></div>
        </div>

        <div style="margin-top:14px; display:flex; gap:12px; flex-wrap:wrap;">
          <a class="btn btn-primary" id="btnWhatsContato" href="#">📲 Chamar no WhatsApp</a>
          <a class="btn btn-outline" href="#inicio">⬆️ Voltar ao topo</a>
        </div>
      </div>

      <div class="map" aria-label="Mapa">
        <!-- Troque o mapa depois pelo endereço real -->
        <iframe
          src="https://www.google.com/maps?q=brasilia&output=embed"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="Mapa Vale do Macacão">
        </iframe>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <div class="footer-wrap">
      <div style="display:flex; align-items:center; gap:10px;">
        <div class="logo" style="width:36px; height:36px; border-radius:12px;">VM</div>
        <div>
          <div style="font-weight:900;">Associação Vale do Macacão</div>
          <small>Mini Produtores Rurais • Agricultura Familiar</small>
        </div>
      </div>

      <small>
        © <span id="year"></span> Vale do Macacão • Site institucional
      </small>
    </div>
  </footer>

  <!-- Floating WhatsApp -->
  <a class="whats" id="btnWhatsFloat" href="#" title="WhatsApp">✆</a>

  <script>
    // ==========================
    // CONFIGURAÇÕES (EDITAR AQUI)
    // ==========================
    const WHATSAPP_NUMERO = "5561900000000"; // coloque seu número com DDI 55 e DDD. Ex: 5561999999999
    const WHATSAPP_MENSAGEM = "Olá! Vim pelo site da Associação Vale do Macacão. Gostaria de informações/pedidos.";

    // Atualiza ano
    document.getElementById("year").textContent = new Date().getFullYear();

    // Atualiza texto do WhatsApp
    const whatsText = document.getElementById("whatsNumberText");
    // Se quiser, edite manualmente o texto também
    // whatsText.textContent = "(61) 9XXXX-XXXX";

    // Link WhatsApp
    function makeWhatsLink(){
      const msg = encodeURIComponent(WHATSAPP_MENSAGEM);
      return `https://wa.me/${WHATSAPP_NUMERO}?text=${msg}`;
    }

    const links = ["btnWhatsHero","btnWhatsProdutos","btnWhatsContato","btnWhatsFloat"];
    links.forEach(id=>{
      const el = document.getElementById(id);
      if(el) el.href = makeWhatsLink();
    });
  </script>

</body>
</html>
