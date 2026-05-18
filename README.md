# IPhone-JT
Mayorita de Productos APPLE
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JT Market - Mayorista iPhone</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box;}
  body{font-family:'Segoe UI',Arial,sans-serif;background:#07111f;color:#c8d8ea;}

  nav{background:#0a1828;border-bottom:1px solid #152a42;padding:0 48px;height:68px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100;}
  .logo{display:flex;align-items:center;gap:10px;}
  .logo-icon{width:36px;height:36px;background:#1a4a80;border-radius:8px;display:flex;align-items:center;justify-content:center;color:#a0c8f0;font-weight:800;font-size:14px;letter-spacing:1px;}
  .logo-text{font-size:18px;font-weight:700;color:#a0bcd8;letter-spacing:1px;}
  .logo-text span{color:#4a90d9;}
  .nav-links{display:flex;gap:32px;list-style:none;}
  .nav-links a{color:#4a6888;text-decoration:none;font-size:14px;font-weight:500;transition:color 0.2s;}
  .nav-links a:hover{color:#a0bcd8;}
  .nav-right{display:flex;align-items:center;gap:12px;}
  .nav-tag{font-size:12px;color:#2a4a68;border:1px solid #1a3050;padding:5px 14px;border-radius:20px;}
  .nav-btn{background:#1a3a6a;color:#7ab0e8;padding:9px 22px;border-radius:8px;font-size:13px;font-weight:600;border:1px solid #2a5a9a;cursor:pointer;transition:background 0.2s;}
  .nav-btn:hover{background:#234d8a;}

  .hero{display:grid;grid-template-columns:1fr 1fr;min-height:460px;background:#07111f;}
  .hero-left{padding:64px 48px;display:flex;flex-direction:column;justify-content:center;border-right:1px solid #122030;}
  .hero-pill{display:inline-flex;align-items:center;gap:8px;background:#0d2040;border:1px solid #1a3a60;color:#5090c8;font-size:12px;font-weight:700;letter-spacing:1px;padding:6px 16px;border-radius:20px;margin-bottom:28px;width:fit-content;}
  .pill-dot{width:6px;height:6px;background:#4a90d9;border-radius:50%;}
  .hero-left h1{font-size:44px;font-weight:800;line-height:1.1;color:#c8dff8;margin-bottom:18px;}
  .hero-left h1 em{font-style:normal;color:#4a90d9;}
  .hero-left p{font-size:16px;color:#3a5a78;line-height:1.75;max-width:400px;margin-bottom:36px;}
  .hero-actions{display:flex;gap:12px;flex-wrap:wrap;}
  .btn-primary{background:#1a3a6a;color:#90c0f0;border:1px solid #2a5a9a;padding:13px 28px;border-radius:8px;font-size:14px;font-weight:600;cursor:pointer;transition:background 0.2s;}
  .btn-primary:hover{background:#234d8a;}
  .btn-ghost{background:transparent;color:#3a6080;border:1px solid #1a3050;padding:13px 28px;border-radius:8px;font-size:14px;font-weight:600;cursor:pointer;transition:all 0.2s;}
  .btn-ghost:hover{border-color:#2a5a9a;color:#7ab0e0;}
  .hero-right{background:#0a1828;display:flex;flex-direction:column;justify-content:center;padding:48px;}
  .metrics{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
  .metric{background:#0d2038;border:1px solid #172e4a;border-radius:12px;padding:24px 20px;}
  .metric-num{font-size:36px;font-weight:800;color:#4a90d9;letter-spacing:-1px;}
  .metric-label{font-size:12px;color:#2a4a68;letter-spacing:0.8px;margin-top:6px;text-transform:uppercase;}
  .metric-note{font-size:11px;color:#1a3048;margin-top:4px;}

  .strip{background:#0d2038;border-top:1px solid #152e4a;border-bottom:1px solid #152e4a;padding:13px 48px;display:flex;gap:48px;align-items:center;overflow:hidden;}
  .strip-item{display:flex;align-items:center;gap:10px;white-space:nowrap;}
  .strip-dot{width:5px;height:5px;background:#2a6090;border-radius:50%;flex-shrink:0;}
  .strip-text{font-size:13px;color:#2a5070;font-weight:500;}

  .cats{padding:64px 48px;background:#07111f;}
  .sec-header{display:flex;align-items:flex-end;justify-content:space-between;margin-bottom:36px;}
  .sec-tag{font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#4a90d9;margin-bottom:8px;}
  .sec-title{font-size:28px;font-weight:700;color:#a0c0d8;}
  .sec-link{font-size:13px;color:#3a6888;font-weight:600;cursor:pointer;border-bottom:1px solid #1a3a58;padding-bottom:2px;text-decoration:none;}
  .cats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;}
  .cat-card{background:#0a1828;border:1px solid #152a42;border-radius:14px;padding:28px 22px;cursor:pointer;transition:border-color 0.2s;}
  .cat-card:hover{border-color:#2a5a9a;}
  .cat-emoji{font-size:28px;margin-bottom:16px;}
  .cat-name{font-size:15px;font-weight:700;color:#7a9ab8;margin-bottom:6px;}
  .cat-sub{font-size:13px;color:#2a4a60;line-height:1.5;margin-bottom:14px;}
  .cat-tag{display:inline-block;background:#0d2038;border:1px solid #1a3858;color:#3a6888;font-size:11px;font-weight:600;padding:3px 10px;border-radius:20px;}

  .products{padding:64px 48px;background:#0a1828;border-top:1px solid #122030;}
  .prod-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
  .prod-card{border:1px solid #152a42;border-radius:14px;overflow:hidden;background:#07111f;}
  .prod-top{background:#0d2038;padding:24px 22px 20px;border-bottom:1px solid #122030;}
  .prod-badges{display:flex;gap:6px;margin-bottom:14px;}
  .badge{font-size:10px;font-weight:700;letter-spacing:0.8px;padding:3px 10px;border-radius:20px;}
  .b-new{background:#0d2a50;color:#5090d0;border:1px solid #1a4070;}
  .b-top{background:#2a0d20;color:#d06080;border:1px solid #501030;}
  .b-rep{background:#0d2a18;color:#40b070;border:1px solid #1a5030;}
  .prod-name{font-size:16px;font-weight:700;color:#90b8d8;margin-bottom:6px;}
  .prod-desc{font-size:12px;color:#2a4a60;line-height:1.6;}
  .prod-bottom{padding:20px 22px;background:#07111f;}
  .prod-price{font-size:22px;font-weight:800;color:#4a90d9;}
  .prod-unit{font-size:12px;color:#2a4a60;margin-left:4px;font-weight:400;}
  .prod-min{font-size:12px;color:#1e3a50;margin:4px 0 14px;}
  .prod-btn{width:100%;background:#0d2038;color:#3a7ab8;border:1px solid #1a3a5a;padding:10px;border-radius:8px;font-size:13px;font-weight:600;cursor:pointer;transition:background 0.2s;}
  .prod-btn:hover{background:#122840;}

  .why{padding:64px 48px;background:#07111f;border-top:1px solid #122030;}
  .why-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-top:36px;}
  .why-card{background:#0a1828;border:1px solid #152a42;border-radius:14px;padding:28px 20px;}
  .why-num{font-size:36px;font-weight:800;color:#152a42;margin-bottom:12px;}
  .why-title{font-size:15px;font-weight:700;color:#6a90b0;margin-bottom:8px;}
  .why-text{font-size:13px;color:#2a4a60;line-height:1.65;}

  .cta{padding:0 48px 64px;background:#07111f;}
  .cta-box{background:#0a1828;border:1px solid #152a42;border-radius:16px;padding:52px 48px;display:grid;grid-template-columns:1fr auto;gap:40px;align-items:center;}
  .cta-box h2{font-size:28px;font-weight:700;color:#90b8d8;margin-bottom:10px;}
  .cta-box p{font-size:15px;color:#2a4a60;max-width:480px;line-height:1.7;}
  .cta-right{display:flex;flex-direction:column;gap:12px;align-items:flex-end;}
  .cta-btn{background:#1a4a80;color:#90c0f0;border:1px solid #2a6aaa;padding:14px 32px;border-radius:8px;font-size:14px;font-weight:700;cursor:pointer;white-space:nowrap;transition:background 0.2s;}
  .cta-btn:hover{background:#235a9a;}
  .cta-sub{font-size:12px;color:#1a3050;text-align:right;}

  footer{background:#050d18;border-top:1px solid #0f1e2e;padding:28px 48px;display:flex;align-items:center;justify-content:space-between;}
  .f-logo{font-size:16px;font-weight:700;color:#1a3050;letter-spacing:1.5px;}
  .f-logo span{color:#152840;}
  .f-copy{font-size:12px;color:#0f1e2e;}
</style>
</head>
<body>

<nav>
  <div class="logo">
    <div class="logo-icon">JT</div>
    <div class="logo-text">JT <span>MARKET</span></div>
  </div>
  <ul class="nav-links">
    <li><a href="#">Inicio</a></li>
    <li><a href="#">iPhones</a></li>
    <li><a href="#">Accesorios</a></li>
    <li><a href="#">Repuestos</a></li>
    <li><a href="#">Nosotros</a></li>
  </ul>
  <div class="nav-right">
    <span class="nav-tag">Solo mayoristas</span>
    <button class="nav-btn">Contactar ahora</button>
  </div>
</nav>

<div class="hero">
  <div class="hero-left">
    <div class="hero-pill"><div class="pill-dot"></div>Distribuidor mayorista · Argentina</div>
    <h1>Tu proveedor<br>de tecnología<br><em>Apple</em> confiable</h1>
    <p>iPhones originales, accesorios y repuestos importados con precios mayoristas reales. Para revendedores, locales y emprendedores.</p>
    <div class="hero-actions">
      <button class="btn-primary">Ver catálogo completo</button>
      <button class="btn-ghost">Lista de precios</button>
    </div>
  </div>
  <div class="hero-right">
    <div class="metrics">
      <div class="metric">
        <div class="metric-num">+200</div>
        <div class="metric-label">SKUs disponibles</div>
        <div class="metric-note">Stock permanente</div>
      </div>
      <div class="metric">
        <div class="metric-num">48h</div>
        <div class="metric-label">Envío express</div>
        <div class="metric-note">Todo el país</div>
      </div>
      <div class="metric">
        <div class="metric-num">5★</div>
        <div class="metric-label">Reputación</div>
        <div class="metric-note">+300 revendedores</div>
      </div>
      <div class="metric">
        <div class="metric-num">100%</div>
        <div class="metric-label">Originales</div>
        <div class="metric-note">Con garantía</div>
      </div>
    </div>
  </div>
</div>

<div class="strip">
  <div class="strip-item"><div class="strip-dot"></div><span class="strip-text">iPhone 16 Pro Max disponible</span></div>
  <div class="strip-item"><div class="strip-dot"></div><span class="strip-text">Envío gratis desde 20 unidades</span></div>
  <div class="strip-item"><div class="strip-dot"></div><span class="strip-text">Precios en USD · Transferencia y efectivo</span></div>
  <div class="strip-item"><div class="strip-dot"></div><span class="strip-text">Atención por WhatsApp · Lun–Vie 9–18h</span></div>
  <div class="strip-item"><div class="strip-dot"></div><span class="strip-text">Nuevos modelos cada semana</span></div>
</div>

<section class="cats">
  <div class="sec-header">
    <div>
      <div class="sec-tag">Categorías</div>
      <div class="sec-title">Todo en un solo proveedor</div>
    </div>
    <a class="sec-link">Ver catálogo completo →</a>
  </div>
  <div class="cats-row">
    <div class="cat-card">
      <div class="cat-emoji">📱</div>
      <div class="cat-name">iPhones nuevos</div>
      <div class="cat-sub">Modelos 15 y 16 sellados de fábrica. Todas las capacidades y colores.</div>
      <div class="cat-tag">15 modelos</div>
    </div>
    <div class="cat-card">
      <div class="cat-emoji">🔌</div>
      <div class="cat-name">Cables y cargadores</div>
      <div class="cat-sub">USB-C, Lightning, MagSafe. Carga rápida 20W y 30W. Por unidad o pack.</div>
      <div class="cat-tag">40+ productos</div>
    </div>
    <div class="cat-card">
      <div class="cat-emoji">📦</div>
      <div class="cat-name">Cases y templados</div>
      <div class="cat-sub">Fundas premium y vidrios 9H para iPhone 13 al 16. Alta rotación.</div>
      <div class="cat-tag">80+ productos</div>
    </div>
    <div class="cat-card">
      <div class="cat-emoji">🔧</div>
      <div class="cat-name">Repuestos y partes</div>
      <div class="cat-sub">Pantallas OLED, baterías y componentes internos certificados.</div>
      <div class="cat-tag">60+ piezas</div>
    </div>
  </div>
</section>

<section class="products">
  <div class="sec-header">
    <div>
      <div class="sec-tag">Productos</div>
      <div class="sec-title">Los más solicitados esta semana</div>
    </div>
    <a class="sec-link">Ver todos →</a>
  </div>
  <div class="prod-grid">
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-new">NUEVO</span></div>
        <div class="prod-name">iPhone 16 Pro Max · 256GB</div>
        <div class="prod-desc">Titanio natural · Chip A18 Pro · Cámara 48MP · Sellado de fábrica</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$1.180<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 5 unidades · Envío incluido</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-top">MÁS PEDIDO</span></div>
        <div class="prod-name">iPhone 15 · 128GB</div>
        <div class="prod-desc">Negro / Rosa / Azul / Verde · Stock inmediato · Sellado original</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$780<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 10 unidades · Envío incluido</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-top">MÁS PEDIDO</span></div>
        <div class="prod-name">Pack Accesorios Mix</div>
        <div class="prod-desc">Cargador 20W + Cable USB-C + Funda · Compatible con iPhone 13–16</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$18<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 20 packs · Alta rotación</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-rep">REPUESTO</span></div>
        <div class="prod-name">Pantalla OLED iPhone 14</div>
        <div class="prod-desc">Original remanufacturada · Kit de herramientas incluido · Garantía 90 días</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$95<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 3 unidades</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-rep">REPUESTO</span></div>
        <div class="prod-name">Batería iPhone 13 / 14</div>
        <div class="prod-desc">3.279 mAh · Ciclo 0 · Certificación CE · Compatibilidad 100%</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$22<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 10 unidades</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
    <div class="prod-card">
      <div class="prod-top">
        <div class="prod-badges"><span class="badge b-new">NUEVO</span></div>
        <div class="prod-name">Templado 9H · iPhone 16 series</div>
        <div class="prod-desc">Vidrio antihuella · Compatible 15 / 16 / Pro / Max · Aplicador incluido</div>
      </div>
      <div class="prod-bottom">
        <div class="prod-price">$4,50<span class="prod-unit">USD c/u</span></div>
        <div class="prod-min">Mínimo 50 unidades</div>
        <button class="prod-btn">Consultar disponibilidad</button>
      </div>
    </div>
  </div>
</section>

<section class="why">
  <div class="sec-tag">¿Por qué JT Market?</div>
  <div class="sec-title">Lo que nos diferencia</div>
  <div class="why-grid">
    <div class="why-card">
      <div class="why-num">01</div>
      <div class="why-title">Productos 100% originales</div>
      <div class="why-text">Importación directa con documentación. Todo sellado de fábrica o certificado. Sin copias ni reacondicionados sin declarar.</div>
    </div>
    <div class="why-card">
      <div class="why-num">02</div>
      <div class="why-title">Precios por volumen</div>
      <div class="why-text">Escala de descuentos según cantidad. Cuanto más comprás, mejor precio. Ideal para locales y distribuidores.</div>
    </div>
    <div class="why-card">
      <div class="why-num">03</div>
      <div class="why-title">Envío en 48 horas</div>
      <div class="why-text">Despacho en 24–48h hábiles a todo el país. Embalaje seguro y número de seguimiento en tiempo real.</div>
    </div>
    <div class="why-card">
      <div class="why-num">04</div>
      <div class="why-title">Soporte dedicado</div>
      <div class="why-text">Asesor exclusivo por WhatsApp para cada cliente. Respuesta garantizada en menos de 1 hora en horario comercial.</div>
    </div>
  </div>
</section>

<section class="cta">
  <div class="cta-box">
    <div>
      <h2>¿Listo para ser revendedor?</h2>
      <p>Escribinos y en minutos te enviamos la lista de precios actualizada, mínimos de compra y condiciones especiales para nuevos clientes.</p>
    </div>
    <div class="cta-right">
      <button class="cta-btn">📲 Escribir por WhatsApp</button>
      <div class="cta-sub">Respondemos en menos de 1 hora · Lun–Vie 9 a 18h</div>
    </div>
  </div>
</section>

<footer>
  <div class="f-logo">JT <span>MARKET</span></div>
  <div class="f-copy">© 2026 JT Market · Mayorista de tecnología Apple · Argentina</div>
</footer>

</body>
</html>
