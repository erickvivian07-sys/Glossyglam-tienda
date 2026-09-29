<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GlossyGlam | Makeup & Fragrances</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <style>
    :root {
      --primary: #a86b6c;
      --primary-dark: #7a4648;
      --secondary: #d4a373;
      --rose-gold: #b38275;
      --accent: #e8d0c5;
      --bg-cream: #faf6f0;
      --bg-white: #ffffff;
      --text-main: #2b2323;
      --text-muted: #736262;
      --border-color: #ede2db;
      --shadow-sm: 0 4px 12px rgba(168, 107, 108, 0.08);
      --shadow-lg: 0 12px 32px rgba(122, 70, 72, 0.15);
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Montserrat', sans-serif;
      background-color: var(--bg-cream);
      color: var(--text-main);
      line-height: 1.5;
    }

    .top-bar {
      background: linear-gradient(90deg, #7a4648, #a86b6c, #7a4648);
      color: #fff;
      text-align: center;
      padding: 8px 15px;
      font-size: 0.82rem;
      letter-spacing: 1px;
      font-weight: 500;
    }

    header {
      background-color: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(8px);
      position: sticky;
      top: 0;
      z-index: 100;
      border-bottom: 1px solid var(--border-color);
      box-shadow: var(--shadow-sm);
    }
    .header-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 12px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .logo-container {
      display: flex;
      align-items: center;
      gap: 12px;
      text-decoration: none;
    }
    .logo-icon {
      width: 45px;
      height: 45px;
      background: radial-gradient(circle, #e8d0c5 0%, #b38275 100%);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-family: 'Cormorant Garamond', serif;
      font-weight: 700;
      font-size: 1.4rem;
      border: 1px solid rgba(255,255,255,0.8);
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .brand-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--primary-dark);
      letter-spacing: 3px;
    }
    .cart-btn {
      position: relative;
      background: var(--bg-cream);
      border: 1px solid var(--border-color);
      padding: 10px 18px;
      border-radius: 25px;
      cursor: pointer;
      font-family: 'Montserrat', sans-serif;
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--primary-dark);
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .cart-badge {
      background-color: var(--primary-dark);
      color: white;
      border-radius: 50%;
      width: 20px;
      height: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
    }

    .hero {
      background: linear-gradient(rgba(43, 35, 35, 0.4), rgba(43, 35, 35, 0.4)), url('https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?auto=format&fit=crop&w=1400&q=80');
      background-size: cover;
      background-position: center;
      color: white;
      text-align: center;
      padding: 60px 20px;
    }
    .hero h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 2.8rem;
      letter-spacing: 3px;
      margin-bottom: 10px;
    }
    .hero p {
      font-size: 1rem;
      max-width: 600px;
      margin: 0 auto;
      font-weight: 300;
    }

    .main-container {
      max-width: 1200px;
      margin: 30px auto;
      padding: 0 20px;
    }

    .controls-section {
      display: flex;
      flex-direction: column;
      gap: 15px;
      margin-bottom: 30px;
      align-items: center;
    }
    .search-box {
      width: 100%;
      max-width: 500px;
      position: relative;
    }
    .search-box input {
      width: 100%;
      padding: 12px 20px 12px 45px;
      border-radius: 30px;
      border: 1px solid var(--border-color);
      font-family: 'Montserrat', sans-serif;
      outline: none;
      font-size: 0.95rem;
    }
    .search-box i {
      position: absolute;
      left: 18px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--text-muted);
    }

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 20px;
    }
    .product-card {
      background-color: var(--bg-white);
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--border-color);
      box-shadow: var(--shadow-sm);
      display: flex;
      flex-direction: column;
      position: relative;
    }
    .badge-discount {
      position: absolute;
      top: 12px;
      right: 12px;
      background: linear-gradient(135deg, var(--primary-dark), var(--primary));
      color: white;
      font-size: 0.75rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 12px;
      z-index: 2;
    }
    .product-img-wrap {
      width: 100%;
      height: 230px;
      background-color: #fff;
      padding: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-bottom: 1px solid var(--border-color);
    }
    .product-img-wrap img {
      max-width: 100%;
      max-height: 100%;
      object-fit: contain;
    }
    .product-details {
      padding: 15px;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }
    .brand-tag {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--rose-gold);
      font-weight: 600;
    }
    .product-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.2rem;
      font-weight: 700;
      color: var(--text-main);
      margin: 4px 0;
    }
    .product-size {
      font-size: 0.8rem;
      color: var(--primary-dark);
      font-weight: 600;
      margin-bottom: 10px;
    }
    .price-box {
      margin-bottom: 12px;
      display: flex;
      align-items: baseline;
      gap: 8px;
    }
    .original-price {
      text-decoration: line-through;
      color: #a09090;
      font-size: 0.85rem;
    }
    .final-price {
      font-size: 1.15rem;
      font-weight: 700;
      color: var(--primary-dark);
    }
    .card-actions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-top: auto;
    }
    .btn-add-cart {
      background-color: var(--bg-cream);
      border: 1px solid var(--border-color);
      color: var(--text-main);
      padding: 8px;
      border-radius: 6px;
      font-family: 'Montserrat', sans-serif;
      font-size: 0.8rem;
      font-weight: 600;
      cursor: pointer;
    }
    .btn-buy-now {
      background-color: #25d366;
      color: white;
      border: none;
      padding: 8px;
      border-radius: 6px;
      font-family: 'Montserrat', sans-serif;
      font-size: 0.8rem;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 4px;
    }

    .cart-overlay {
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      z-index: 200;
      display: none;
    }
    .cart-drawer {
      position: fixed;
      top: 0; right: -420px;
      width: 100%; max-width: 400px;
      height: 100%;
      background-color: var(--bg-white);
      z-index: 201;
      transition: right 0.3s ease;
      display: flex;
      flex-direction: column;
    }
    .cart-drawer.open { right: 0; }
    .cart-header {
      padding: 20px;
      border-bottom: 1px solid var(--border-color);
      display: flex;
      justify-content: space-between;
      align-items: center;
      background-color: var(--bg-cream);
    }
    .cart-body {
      padding: 20px;
      flex-grow: 1;
      overflow-y: auto;
    }
    .cart-footer {
      padding: 20px;
      border-top: 1px solid var(--border-color);
      background-color: var(--bg-cream);
    }
    .btn-checkout-whatsapp {
      width: 100%;
      background-color: #25d366;
      color: white;
      border: none;
      padding: 12px;
      border-radius: 25px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    footer {
      background-color: var(--primary-dark);
      color: white;
      text-align: center;
      padding: 25px 20px;
      margin-top: 50px;
      font-size: 0.85rem;
    }
  </style>
</head>
<body>

  <div class="top-bar">
    ✨ ENVÍOS Y PEDIDOS POR WHATSAPP AL <strong>7206505461</strong> | 10% DE DESCUENTO ✨
  </div>

  <header>
    <div class="header-container">
      <a href="#" class="logo-container">
        <div class="logo-icon">GG</div>
        <span class="brand-title">GLOSSYGLAM</span>
      </a>
      <button class="cart-btn" onclick="toggleCart()">
        <i class="fa-solid fa-bag-shopping"></i>
        <span>Carrito</span>
        <div class="cart-badge" id="cart-count">0</div>
      </button>
    </div>
  </header>

  <section class="hero">
    <h1>GLOSSYGLAM BEAUTY</h1>
    <p>Maquillaje y Fragancias de Lujo con 10% de Descuento sobre Precio Oficial Sephora</p>
  </section>

  <main class="main-container">
    <div class="controls-section">
      <div class="search-box">
        <i class="fa-solid fa-magnifying-glass"></i>
        <input type="text" id="searchInput" placeholder="Buscar productos..." oninput="renderProducts()">
      </div>
    </div>

    <div class="product-grid" id="productGrid"></div>
  </main>

  <div class="cart-overlay" id="cartOverlay" onclick="toggleCart()"></div>
  <div class="cart-drawer" id="cartDrawer">
    <div class="cart-header">
      <h3>Tu Carrito</h3>
      <button style="background:none; border:none; font-size:1.2rem; cursor:pointer;" onclick="toggleCart()"><i class="fa-solid fa-xmark"></i></button>
    </div>
    <div class="cart-body" id="cartBody"></div>
    <div class="cart-footer">
      <div style="display:flex; justify-content:space-between; font-weight:700; margin-bottom:15px;">
        <span>Total:</span>
        <span id="cartTotal">$0 MXN</span>
      </div>
      <button class="btn-checkout-whatsapp" onclick="checkoutWhatsApp()">
        <i class="fa-brands fa-whatsapp"></i> Finalizar Pedido
      </button>
    </div>
  </div>

  <footer>
    <p>© GlossyGlam - Pedidos por WhatsApp al <strong>7206505461</strong></p>
  </footer>

  <script>
    const PHONE = "527206505461";

    const products = [
      { id: 1, brand: 'FENTY BEAUTY', name: "Shake 'N Play Blush", size: "10 ml", originalPrice: 640, img: "https://images.unsplash.com/photo-1596462502278-27bfdc403348?auto=format&fit=crop&w=500&q=80" },
      { id: 2, brand: 'M·A·C', name: "Studio Radiance Primer", size: "30 ml / 1.0 fl. oz.", originalPrice: 790, img: "https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?auto=format&fit=crop&w=500&q=80" },
      { id: 3, brand: 'GIORGIO ARMANI', name: "Acqua Di Giò EDP", size: "100 ml / 3.4 fl. oz.", originalPrice: 3100, img: "https://images.unsplash.com/photo-1523293182086-7651a899d37f?auto=format&fit=crop&w=500&q=80" },
      { id: 4, brand: 'FENTY BEAUTY', name: "Hella Thicc Mascara", size: "10 ml / 0.34 fl. oz.", originalPrice: 500, img: "https://images.unsplash.com/photo-1631214524020-7e18db9a8f92?auto=format&fit=crop&w=500&q=80" },
      { id: 5, brand: 'FENTY BEAUTY', name: "Match Stix Adaptive", size: "5 g / 0.176 oz.", originalPrice: 755, img: "https://images.unsplash.com/photo-1599733589046-10c005739ef9?auto=format&fit=crop&w=500&q=80" },
      { id: 6, brand: 'FENTY BEAUTY', name: "Gloss Bomb Stix", size: "3.6 g / 0.12 oz.", originalPrice: 595, img: "https://images.unsplash.com/photo-1625093742435-6fa192b6fb10?auto=format&fit=crop&w=500&q=80" },
      { id: 7, brand: 'FENTY BEAUTY', name: "Gloss Bomb Luminizer", size: "9 ml / 0.3 fl. oz.", originalPrice: 525, img: "https://images.unsplash.com/photo-1586495777744-4413f21062fa?auto=format&fit=crop&w=500&q=80" },
      { id: 8, brand: 'FENTY BEAUTY', name: "Gloss Bomb Oil", size: "9 ml / 0.3 fl. oz.", originalPrice: 595, img: "https://images.unsplash.com/photo-1617897903246-719242758050?auto=format&fit=crop&w=500&q=80" },
      { id: 9, brand: 'YSL', name: "MYSLF Eau de Parfum", size: "100 ml / 3.3 fl. oz.", originalPrice: 2960, img: "https://images.unsplash.com/photo-1594035910387-fea47794261f?auto=format&fit=crop&w=500&q=80" },
      { id: 10, brand: 'M·A·C', name: "MACximal Matte Lipstick", size: "3.5 g / 0.12 oz.", originalPrice: 490, img: "https://images.unsplash.com/photo-1586495777744-4413f21062fa?auto=format&fit=crop&w=500&q=80" }
    ];

    let cart = [];

    function calculateDiscount(price) { return Math.round(price * 0.90); }

    function renderProducts() {
      const grid = document.getElementById('productGrid');
      const search = document.getElementById('searchInput').value.toLowerCase();
      grid.innerHTML = '';

      products.filter(p => p.name.toLowerCase().includes(search) || p.brand.toLowerCase().includes(search)).forEach(p => {
        const finalPrice = calculateDiscount(p.originalPrice);
        const card = document.createElement('div');
        card.className = 'product-card';
        card.innerHTML = `
          <div class="badge-discount">10% OFF</div>
          <div class="product-img-wrap"><img src="${p.img}" alt="${p.name}"></div>
          <div class="product-details">
            <span class="brand-tag">${p.brand}</span>
            <div class="product-name">${p.name}</div>
            <div class="product-size">Contenido: ${p.size}</div>
            <div class="price-box">
              <span class="original-price">$${p.originalPrice} MXN</span>
              <span class="final-price">$${finalPrice} MXN</span>
            </div>
            <div class="card-actions">
              <button class="btn-add-cart" onclick="addToCart(${p.id})">Agregar</button>
              <button class="btn-buy-now" onclick="buyDirect(${p.id})"><i class="fa-brands fa-whatsapp"></i> Comprar</button>
            </div>
          </div>
        `;
        grid.appendChild(card);
      });
    }

    function addToCart(id) {
      const item = cart.find(c => c.id === id);
      if (item) item.qty++;
      else cart.push({ ...products.find(p => p.id === id), qty: 1 });
      updateCartUI();
    }

    function updateCartUI() {
      document.getElementById('cart-count').textContent = cart.reduce((acc, curr) => acc + curr.qty, 0);
      const cartBody = document.getElementById('cartBody');
      cartBody.innerHTML = '';
      let totalMoney = 0;

      cart.forEach(item => {
        const fp = calculateDiscount(item.originalPrice);
        totalMoney += fp * item.qty;
        cartBody.innerHTML += `
          <div style="display:flex; justify-content:space-between; margin-bottom:12px; align-items:center;">
            <div>
              <div style="font-weight:600; font-size:0.85rem;">${item.name} (${item.size})</div>
              <div style="font-size:0.8rem; color:var(--primary-dark);">${item.qty} x $${fp} MXN</div>
            </div>
          </div>
        `;
      });
      document.getElementById('cartTotal').textContent = `$${totalMoney} MXN`;
    }

    function toggleCart() {
      const drawer = document.getElementById('cartDrawer');
      const overlay = document.getElementById('cartOverlay');
      drawer.classList.toggle('open');
      overlay.style.display = drawer.classList.contains('open') ? 'block' : 'none';
    }

    function buyDirect(id) {
      const p = products.find(item => item.id === id);
      const fp = calculateDiscount(p.originalPrice);
      const msg = `¡Hola GlossyGlam! ✨ Quisiera pedir:\n- *${p.brand} - ${p.name}* (${p.size})\nPrecio Especial (10% OFF): *$${fp} MXN*`;
      window.open(`https://wa.me/${PHONE}?text=${encodeURIComponent(msg)}`, '_blank');
    }

    function checkoutWhatsApp() {
      if (cart.length === 0) return alert('El carrito está vacío');
      let msg = "¡Hola GlossyGlam! ✨ Deseo pedir mi carrito:\n\n";
      let total = 0;
      cart.forEach(i => {
        const fp = calculateDiscount(i.originalPrice);
        total += fp * i.qty;
        msg += `• ${i.qty}x *${i.brand} ${i.name}* (${i.size}) - $${fp} MXN c/u\n`;
      });
      msg += `\n*TOTAL:* $${total} MXN`;
      window.open(`https://wa.me/${PHONE}?text=${encodeURIComponent(msg)}`, '_blank');
    }

    renderProducts();
  </script>
</body>
</html>
