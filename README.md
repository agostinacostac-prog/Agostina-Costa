# Agostina-Costa
web BDM personal
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Agostina Costa | Business Development Manager - EBC Broker</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #222;
      background-color: #fff;
      line-height: 1.6;
    }
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: #0a1f44;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 30px;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    header h1 {
      font-size: 1.2rem;
      margin: 0;
    }
    nav a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-weight: 500;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #00bcd4;
    }
    .lang-switch {
      background-color: #00bcd4;
      color: white;
      border: none;
      padding: 5px 10px;
      border-radius: 4px;
      cursor: pointer;
      margin-left: 10px;
    }
    section {
      padding: 100px 20px 60px;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      color: #0a1f44;
      border-bottom: 2px solid #00bcd4;
      display: inline-block;
      padding-bottom: 5px;
    }
    .hero {
      background: linear-gradient(to right, #0a1f44, #00bcd4);
      color: white;
      text-align: center;
      padding: 140px 20px;
    }
    .hero h1 {
      font-size: 2rem;
      margin-bottom: 10px;
    }
    .hero p {
      font-size: 1.2rem;
      max-width: 700px;
      margin: auto;
    }
    .services, .products, .promos, .contact {
      background-color: #f9f9f9;
      border-radius: 10px;
      padding: 40px;
      margin-top: 30px;
    }
    footer {
      background-color: #0a1f44;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .card {
      background: white;
      border-radius: 8px;
      padding: 20px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
      margin-top: 20px;
    }
    input, textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
    }
    button[type="submit"] {
      background-color: #00bcd4;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    button[type="submit"]:hover {
      background-color: #0099b3;
    }
    @media (max-width: 768px) {
      nav a { margin: 0 8px; }
      .hero h1 { font-size: 1.5rem; }
      section { padding: 80px 15px; }
    }
  </style>
  <script>
    function switchLang(lang) {
      document.querySelectorAll('[data-lang]').forEach(el => {
        el.style.display = el.dataset.lang === lang ? 'block' : 'none';
      });
    }

    function validateForm(e) {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      if (!name || !email || !message) {
        alert('Por favor completa todos los campos / Please fill all fields.');
        return;
      }
      if (!email.includes('@')) {
        alert('Por favor ingresa un email válido / Please enter a valid email.');
        return;
      }
      alert('Gracias por tu mensaje. Será respondido pronto / Thank you for your message. You will be contacted soon.');
      document.getElementById('contact-form').reset();
    }
  </script>
</head>
<body onload="switchLang('es')">

  <header>
    <h1>Agostina Costa | BDM - EBC Broker</h1>
    <nav>
      <a href="#inicio">Inicio</a>
      <a href="#sobre-mi">Sobre mí</a>
      <a href="#servicios">Servicios</a>
      <a href="#productos">Productos</a>
      <a href="#promociones">Promociones</a>
      <a href="#contacto">Contacto</a>
      <button class="lang-switch" onclick="switchLang('es')">ES</button>
      <button class="lang-switch" onclick="switchLang('en')">EN</button>
    </nav>
  </header>

  <section class="hero" id="inicio">
    <div data-lang="es">
      <h1>Tu Aliada Estratégica en el Mundo del Trading</h1>
      <p>Asesoro a traders, inversionistas e Introducing Brokers para alcanzar resultados sólidos, respaldados por EBC Financial Group, bróker global regulado y premiado internacionalmente.</p>
    </div>
    <div data-lang="en">
      <h1>Your Strategic Partner in the Trading World</h1>
      <p>I assist traders, investors, and Introducing Brokers in achieving consistent results, backed by EBC Financial Group — a globally regulated and award-winning broker.</p>
    </div>
  </section>

  <section id="sobre-mi">
    <div data-lang="es">
      <h2>Sobre mí</h2>
      <p>Soy <strong>Business Development Manager</strong> con experiencia en el sector financiero y de brokerage, especializada en desarrollo de negocios en América Latina. A través de mi colaboración con <strong>EBC Financial Group</strong>, conecto a clientes minoristas, IBs y afiliados con oportunidades de trading confiables y reguladas. Mi enfoque combina integridad, profesionalismo y resultados medibles.</p>
    </div>
    <div data-lang="en">
      <h2>About Me</h2>
      <p>I am a <strong>Business Development Manager</strong> with experience in the financial and brokerage sector, focused on business growth in Latin America. Through my partnership with <strong>EBC Financial Group</strong>, I connect retail clients, IBs, and affiliates with reliable, regulated trading opportunities. My approach is based on integrity, professionalism, and measurable results.</p>
    </div>
  </section>

  <section id="servicios" class="services">
    <div data-lang="es">
      <h2>Servicios</h2>
      <div class="grid">
        <div class="card">
          <h3>Clientes Retail</h3>
          <p>Asesoramiento personalizado para apertura de cuentas, plataformas MT4/MT5 y estrategias de trading. Orientación para nuevos inversores con soporte local y recursos educativos.</p>
        </div>
        <div class="card">
          <h3>Socios e IBs</h3>
          <p>Programas de afiliados, soporte para socios institucionales y soluciones White Label. Ayudo a crear alianzas sólidas y rentables con EBC Broker.</p>
        </div>
      </div>
    </div>
    <div data-lang="en">
      <h2>Services</h2>
      <div class="grid">
        <div class="card">
          <h3>Retail Clients</h3>
          <p>Personalized advice for account opening, MT4/MT5 platforms, and trading strategies. Guidance for new investors with local support and educational resources.</p>
        </div>
        <div class="card">
          <h3>Partners & IBs</h3>
          <p>Affiliate programs, institutional partner support, and White Label solutions. I help build strong and profitable partnerships with EBC Broker.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="productos" class="products">
    <div data-lang="es">
      <h2>Productos</h2>
      <div class="grid">
        <div class="card">
          <h3>Forex</h3>
          <p>Más de 40 pares con spreads competitivos y ejecución rápida respaldada por bancos de primer nivel.</p>
        </div>
        <div class="card">
          <h3>Índices y Acciones</h3>
          <p>Acceda a los principales mercados globales mediante CFDs y diversifique su portafolio de inversión.</p>
        </div>
        <div class="card">
          <h3>Commodities y ETFs</h3>
          <p>Oro, petróleo y más. Oportunidades de cobertura y especulación con transparencia total en costos.</p>
        </div>
      </div>
    </div>
    <div data-lang="en">
      <h2>Products</h2>
      <div class="grid">
        <div class="card">
          <h3>Forex</h3>
          <p>Over 40 currency pairs with competitive spreads and fast execution backed by top-tier banks.</p>
        </div>
        <div class="card">
          <h3>Indices & Stocks</h3>
          <p>Access major global markets via CFDs and diversify your investment portfolio efficiently.</p>
        </div>
        <div class="card">
          <h3>Commodities & ETFs</h3>
          <p>Gold, oil, and more. Opportunities for hedging or speculation with full cost transparency.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="promociones" class="promos">
    <div data-lang="es">
      <h2>Promociones</h2>
      <ul>
        <li><strong>Million Dollar Trading Challenge:</strong> Compite por premios de hasta USD 250.000 y experiencias exclusivas.</li>
        <li><strong>Programa de Referidos:</strong> Gana bonificaciones por cada cliente que invites a EBC.</li>
        <li><strong>Rebates por Volumen:</strong> Beneficios escalonados para traders e IBs activos.</li>
      </ul>
    </div>
    <div data-lang="en">
      <h2>Promotions</h2>
      <ul>
        <li><strong>Million Dollar Trading Challenge:</strong> Compete for prizes up to USD 250,000 and exclusive experiences.</li>
        <li><strong>Referral Program:</strong> Earn bonuses for every client you refer to EBC.</li>
        <li><strong>Volume Rebates:</strong> Tiered benefits for active traders and IBs.</li>
      </ul>
    </div>
  </section>

  <section id="contacto" class="contact">
    <div data-lang="es">
      <h2>Contacto</h2>
      <p>¿Deseas abrir una cuenta o convertirte en socio? Contáctame para asesoría personalizada.</p>
      <form id="contact-form" onsubmit="validateForm(event)">
        <input type="text" id="name" placeholder="Nombre" required>
        <input type="email" id="email" placeholder="Correo electrónico" required>
        <textarea id="message" placeholder="Mensaje" rows="5" required></textarea>
        <button type="submit">Enviar Mensaje</button>
      </form>
    </div>
    <div data-lang="en">
      <h2>Contact</h2>
      <p>Interested in opening an account or becoming a partner? Contact me for personalized assistance.</p>
      <form id="contact-form-en" onsubmit="validateForm(event)">
        <input type="text" id="name" placeholder="Name" required>
        <input type="email" id="email" placeholder="Email" required>
        <textarea id="message" placeholder="Message" rows="5" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Agostina Costa | Business Development Manager - EBC Financial Group</p>
  </footer>

</body>
</html>
