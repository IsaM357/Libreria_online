# Libreria_online
 · HTML
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Librerías Andinas</title>
<meta name="description" content="Librerías Andinas: libros, textos escolares y útiles con envíos a todo el Perú.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Alegreya:ital,wght@0,500;0,700;0,800;1,500&family=Alegreya+Sans:wght@400;500;700&display=swap">
<style>
:root{
  --lago:#1C4D57;      /* azul verdoso del Titicaca */
  --lago-2:#2A6B77;
  --grana:#A8323F;     /* rojo cochinilla de los tejidos */
  --maiz:#D99A1E;      /* amarillo maíz */
  --papel:#F2F4F2;
  --superficie:#FFFFFF;
  --tinta:#15252A;
  --tinta-2:#4A5C61;
  --linea:#D5DDDC;
  --burbuja-bot:#E6EEEE;
  --burbuja-yo:#1C4D57;
  --burbuja-yo-txt:#FFFFFF;
  --sombra:0 18px 40px -18px rgba(21,37,42,.35);
  --display:"Alegreya", Georgia, "Times New Roman", serif;
  --texto:"Alegreya Sans", "Segoe UI", system-ui, sans-serif;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    color-scheme:dark;
    --lago:#6FB3BE; --lago-2:#8CC6CF; --grana:#E0707B; --maiz:#E8B34A;
    --papel:#0F1B1E; --superficie:#16262A; --tinta:#E7EEEE; --tinta-2:#A5B6B9;
    --linea:#2B3F44; --burbuja-bot:#1F3237; --burbuja-yo:#6FB3BE; --burbuja-yo-txt:#0F1B1E;
    --sombra:0 18px 40px -18px rgba(0,0,0,.7);
  }
}
:root[data-theme="dark"]{
  color-scheme:dark;
  --lago:#6FB3BE; --lago-2:#8CC6CF; --grana:#E0707B; --maiz:#E8B34A;
  --papel:#0F1B1E; --superficie:#16262A; --tinta:#E7EEEE; --tinta-2:#A5B6B9;
  --linea:#2B3F44; --burbuja-bot:#1F3237; --burbuja-yo:#6FB3BE; --burbuja-yo-txt:#0F1B1E;
  --sombra:0 18px 40px -18px rgba(0,0,0,.7);
}
*{box-sizing:border-box}
body{margin:0;background:var(--papel);color:var(--tinta);font-family:var(--texto);font-size:17px;line-height:1.6}
a{color:var(--lago)}
:focus-visible{outline:3px solid var(--maiz);outline-offset:2px}
.wrap{max-width:1120px;margin:0 auto;padding-inline:20px}
 
/* franja textil: patrón escalonado inspirado en los tejidos andinos */
.tejido{height:14px;background:
  linear-gradient(135deg,var(--grana) 25%,transparent 25%) 0 0/14px 14px,
  linear-gradient(225deg,var(--grana) 25%,transparent 25%) 0 0/14px 14px,
  linear-gradient(315deg,var(--maiz) 25%,transparent 25%) 7px 7px/14px 14px,
  linear-gradient(45deg,var(--maiz) 25%,transparent 25%) 7px 7px/14px 14px,
  var(--lago)}
 
header.top{background:var(--superficie);border-bottom:1px solid var(--linea);position:sticky;top:env(safe-area-inset-top,0px);z-index:20}
.top .wrap{display:flex;align-items:center;justify-content:space-between;gap:16px;padding-block:14px;flex-wrap:wrap}
.marca{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--tinta)}
.marca b{font-family:var(--display);font-size:1.45rem;font-weight:800;letter-spacing:-.01em}
.marca svg{flex:none}
nav.menu{display:flex;gap:20px;flex-wrap:wrap}
nav.menu a{color:var(--tinta-2);text-decoration:none;font-weight:500}
nav.menu a:hover{color:var(--grana)}
 
.hero{padding-block:64px 56px}
.hero .wrap{display:grid;grid-template-columns:1.3fr 1fr;gap:48px;align-items:center}
.eyebrow{font-size:.8rem;letter-spacing:.14em;text-transform:uppercase;color:var(--grana);font-weight:700}
h1{font-family:var(--display);font-weight:800;font-size:clamp(2.4rem,5.4vw,4.1rem);line-height:1.02;margin:.3em 0 .35em;text-wrap:balance;letter-spacing:-.02em}
h1 em{font-style:italic;font-weight:500;color:var(--lago)}
.hero p.lead{font-size:1.15rem;color:var(--tinta-2);max-width:34em;margin:0 0 28px}
.acciones{display:flex;gap:12px;flex-wrap:wrap}
.btn{display:inline-flex;align-items:center;gap:8px;border:0;cursor:pointer;font:inherit;font-weight:700;padding:12px 20px;border-radius:999px;text-decoration:none}
.btn-pri{background:var(--grana);color:#fff}
.btn-pri:hover{filter:brightness(1.08)}
.btn-sec{background:transparent;color:var(--tinta);box-shadow:inset 0 0 0 2px var(--linea)}
.btn-sec:hover{box-shadow:inset 0 0 0 2px var(--lago)}
 
/* estante de libros */
.estante{display:flex;align-items:flex-end;gap:6px;height:260px;padding:0 12px;border-bottom:10px solid var(--tinta);max-width:100%}
.lomo{flex:1;border-radius:3px 3px 0 0;position:relative;display:flex;align-items:flex-end;justify-content:center;padding-bottom:14px}
.lomo span{writing-mode:vertical-rl;transform:rotate(180deg);font-family:var(--display);font-weight:700;font-size:.95rem;color:#fff;white-space:nowrap;opacity:.95}
.lomo::before{content:"";position:absolute;left:0;right:0;top:18px;height:5px;background:rgba(255,255,255,.35)}
 
section{padding-block:56px}
h2{font-family:var(--display);font-weight:800;font-size:clamp(1.8rem,3.4vw,2.5rem);line-height:1.1;margin:0 0 10px;text-wrap:balance}
.sub{color:var(--tinta-2);margin:0 0 32px;max-width:40em}
 
.categorias{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:var(--linea);border:1px solid var(--linea)}
.cat{background:var(--superficie);padding:26px 24px}
.cat h3{font-family:var(--display);font-size:1.3rem;margin:0 0 6px}
.cat p{margin:0;color:var(--tinta-2);font-size:.98rem}
.cat .desde{display:block;margin-top:12px;font-size:.85rem;font-weight:700;color:var(--grana);font-variant-numeric:tabular-nums}
 
.banda{background:var(--lago);color:#fff}
:root[data-theme="dark"] .banda{color:var(--papel)}
.banda .wrap{display:grid;grid-template-columns:repeat(4,1fr);gap:24px;padding-block:36px}
.banda b{display:block;font-family:var(--display);font-size:1.25rem}
.banda span{font-size:.95rem;opacity:.85}
 
.sedes{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
.sede{border-top:4px solid var(--maiz);padding-top:14px}
.sede h3{font-family:var(--display);margin:0 0 4px;font-size:1.3rem}
.sede p{margin:0;color:var(--tinta-2)}
 
.contacto{display:grid;grid-template-columns:1fr 1fr;gap:32px;align-items:start}
.dato{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:14px 0;border-bottom:1px solid var(--linea);flex-wrap:wrap}
.dato small{display:block;font-size:.75rem;letter-spacing:.12em;text-transform:uppercase;color:var(--tinta-2)}
.dato strong{font-size:1.15rem;user-select:all;word-break:break-all}
.copiar{background:none;border:1px solid var(--linea);color:var(--tinta);border-radius:8px;padding:6px 12px;cursor:pointer;font:inherit;font-size:.9rem}
.copiar:hover{border-color:var(--lago)}
 
footer{border-top:1px solid var(--linea);padding-block:28px;color:var(--tinta-2);font-size:.92rem}
footer .wrap{display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap}
 
/* ---------- Chatbot ---------- */
.chat-toggle{position:fixed;right:20px;bottom:calc(20px + env(safe-area-inset-bottom,0px));z-index:50;background:var(--grana);color:#fff;border:0;border-radius:999px;padding:14px 20px;font:inherit;font-weight:700;cursor:pointer;box-shadow:var(--sombra);display:flex;align-items:center;gap:10px}
.chat{position:fixed;right:20px;bottom:calc(86px + env(safe-area-inset-bottom,0px));z-index:50;width:380px;max-width:calc(100vw - 32px);height:min(600px,calc(100vh - 120px));background:var(--superficie);border:1px solid var(--linea);border-radius:18px;box-shadow:var(--sombra);display:flex;flex-direction:column;overflow:hidden}
.chat-head{background:var(--lago);color:#fff;padding:14px 16px;display:flex;align-items:center;gap:12px}
:root[data-theme="dark"] .chat-head{color:var(--papel)}
.chat-head .av{width:38px;height:38px;border-radius:50%;background:var(--maiz);display:grid;place-items:center;font-family:var(--display);font-weight:800;color:var(--tinta);flex:none}
.chat-head b{display:block;line-height:1.2}
.chat-head small{opacity:.85}
.chat-head button{margin-left:auto;background:none;border:0;color:inherit;font-size:1.5rem;cursor:pointer;line-height:1}
.chat-body{flex:1;overflow-y:auto;padding:16px;display:flex;flex-direction:column;gap:10px}
.msg{max-width:88%;padding:10px 14px;border-radius:14px;font-size:.96rem;line-height:1.45;white-space:pre-line}
.msg.bot{background:var(--burbuja-bot);border-bottom-left-radius:4px;align-self:flex-start}
.msg.yo{background:var(--burbuja-yo);color:var(--burbuja-yo-txt);border-bottom-right-radius:4px;align-self:flex-end}
.opciones{display:flex;flex-wrap:wrap;gap:6px}
.op{background:var(--superficie);border:1px solid var(--lago);color:var(--lago);border-radius:999px;padding:6px 12px;font:inherit;font-size:.88rem;cursor:pointer;text-align:left}
.op:hover{background:var(--lago);color:var(--superficie)}
.op.asesor{border-color:var(--grana);color:var(--grana)}
.op.asesor:hover{background:var(--grana);color:#fff}
.chat-form{display:flex;gap:8px;border-top:1px solid var(--linea);padding:10px}
.chat-form input{flex:1;min-width:0;border:1px solid var(--linea);border-radius:999px;padding:10px 14px;font:inherit;background:var(--papel);color:var(--tinta)}
.chat-form button{background:var(--lago);color:var(--superficie);border:0;border-radius:999px;padding:0 16px;font:inherit;font-weight:700;cursor:pointer}
.lead-form{display:grid;gap:8px;background:var(--burbuja-bot);padding:12px;border-radius:14px}
.lead-form label{font-size:.8rem;font-weight:700;color:var(--tinta-2)}
.lead-form input,.lead-form textarea{width:100%;border:1px solid var(--linea);border-radius:8px;padding:8px 10px;font:inherit;font-size:.95rem;background:var(--superficie);color:var(--tinta)}
.lead-form textarea{min-height:70px;resize:vertical}
.envios{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.envios a,.envios button{display:flex;justify-content:center;align-items:center;gap:6px;padding:10px;border-radius:10px;font:inherit;font-weight:700;font-size:.9rem;text-decoration:none;border:0;cursor:pointer}
.wa{background:#1E8E4E;color:#fff}
.mail{background:var(--lago);color:var(--superficie)}
.estado{font-size:.85rem;color:var(--tinta-2)}
 
@media (max-width:860px){
  .hero .wrap,.contacto{grid-template-columns:1fr}
  .estante{height:200px}
  .categorias,.sedes{grid-template-columns:1fr 1fr}
  .banda .wrap{grid-template-columns:1fr 1fr}
}
@media (max-width:540px){
  .categorias,.sedes,.banda .wrap{grid-template-columns:1fr}
  nav.menu{display:none}
  .chat{right:16px;left:16px;width:auto;max-width:none}
  .chat-toggle{right:16px}
}
@media (prefers-reduced-motion:no-preference){
  .lomo{transition:transform .25s ease}
  .lomo:hover{transform:translateY(-10px)}
}
</style>
</head>
<body>
 
<div class="tejido" aria-hidden="true"></div>
<header class="top">
  <div class="wrap">
    <a class="marca" href="#inicio" aria-label="Librerías Andinas, inicio">
      <svg width="34" height="34" viewBox="0 0 34 34" aria-hidden="true"><path d="M17 3 L31 29 H3 Z" fill="var(--lago)"/><path d="M17 12 L24 29 H10 Z" fill="var(--maiz)"/><rect x="3" y="29" width="28" height="3" fill="var(--grana)"/></svg>
      <b>Librerías Andinas</b>
    </a>
    <nav class="menu" aria-label="Secciones">
      <a href="#catalogo">Catálogo</a>
      <a href="#sedes">Tiendas</a>
      <a href="#contacto">Contacto</a>
    </nav>
  </div>
</header>
 
<main id="inicio">
  <section class="hero">
    <div class="wrap">
      <div>
        <div class="eyebrow">Librería peruana · Envíos a todo el país</div>
        <h1>Libros que suben <em>desde los Andes</em> hasta tu casa</h1>
        <p class="lead">Literatura peruana y universal, textos escolares, libros universitarios y útiles. Atendemos en tienda, por WhatsApp y con envíos a Lima y provincias.</p>
        <div class="acciones">
          <button class="btn btn-pri" type="button" data-abrir-chat>Pregúntale a Amaru, nuestro asistente</button>
          <a class="btn btn-sec" href="#catalogo">Ver catálogo</a>
        </div>
      </div>
      <div class="estante" aria-hidden="true">
        <div class="lomo" style="height:88%;background:var(--grana)"><span>Los ríos profundos</span></div>
        <div class="lomo" style="height:72%;background:var(--lago)"><span>Tradiciones</span></div>
        <div class="lomo" style="height:96%;background:#3B3A36"><span>Los heraldos negros</span></div>
        <div class="lomo" style="height:64%;background:var(--maiz)"><span>Paco Yunque</span></div>
        <div class="lomo" style="height:82%;background:var(--lago-2)"><span>El mundo es ancho</span></div>
        <div class="lomo" style="height:70%;background:var(--grana)"><span>Comentarios Reales</span></div>
      </div>
    </div>
  </section>
 
  <div class="banda">
    <div class="wrap">
      <div><b>Envíos nacionales</b><span>Lima en 24–48 h, provincias en 2–5 días hábiles</span></div>
      <div><b>Yape y Plin</b><span>También tarjetas, transferencia y contraentrega en Lima</span></div>
      <div><b>Pedidos especiales</b><span>Conseguimos el libro que buscas en 7 a 15 días</span></div>
      <div><b>Boleta o factura</b><span>Comprobante electrónico en cada compra</span></div>
    </div>
  </div>
 
  <section id="catalogo">
    <div class="wrap">
      <h2>Nuestro catálogo</h2>
      <p class="sub">Más de 20 000 títulos entre novedades, clásicos y material educativo. Precios referenciales en soles.</p>
      <div class="categorias">
        <div class="cat"><h3>Literatura peruana</h3><p>Arguedas, Vallejo, Palma, Ciro Alegría y autores contemporáneos.</p><span class="desde">Desde S/ 25.00</span></div>
        <div class="cat"><h3>Textos escolares</h3><p>Inicial, primaria y secundaria. Armamos la lista completa de tu colegio.</p><span class="desde">Desde S/ 35.00</span></div>
        <div class="cat"><h3>Universitarios</h3><p>Derecho, ingeniería, ciencias de la salud, economía y humanidades.</p><span class="desde">Desde S/ 60.00</span></div>
        <div class="cat"><h3>Infantil y juvenil</h3><p>Cuentos, libros ilustrados, lectores iniciales y sagas juveniles.</p><span class="desde">Desde S/ 18.00</span></div>
        <div class="cat"><h3>Historia y cultura andina</h3><p>Arqueología, quechua, gastronomía, arte textil y viajes por el Perú.</p><span class="desde">Desde S/ 40.00</span></div>
        <div class="cat"><h3>Útiles y papelería</h3><p>Cuadernos, arte, oficina y packs escolares listos para marzo.</p><span class="desde">Desde S/ 2.50</span></div>
      </div>
    </div>
  </section>
 
  <section id="sedes" style="padding-top:0">
    <div class="wrap">
      <h2>Nuestras tiendas</h2>
      <p class="sub">Lunes a sábado de 9:00 a.m. a 8:00 p.m. · Domingos y feriados de 10:00 a.m. a 2:00 p.m.</p>
      <div class="sedes">
        <div class="sede"><h3>Lima</h3><p>Tienda principal y almacén de despacho nacional.</p></div>
        <div class="sede"><h3>Cusco</h3><p>Especializada en historia, arqueología y cultura andina.</p></div>
        <div class="sede"><h3>Arequipa</h3><p>Textos escolares, universitarios y útiles.</p></div>
      </div>
    </div>
  </section>
 
  <section id="contacto" style="padding-top:0">
    <div class="wrap contacto">
      <div>
        <h2>Escríbenos</h2>
        <p class="sub">Respondemos por WhatsApp y correo en horario de atención. También puedes dejar tu consulta en el chat.</p>
        <button class="btn btn-pri" type="button" data-abrir-chat data-ir-asesor>Dejar una consulta</button>
      </div>
      <div>
        <div class="dato"><div><small>WhatsApp</small><strong id="txt-wa">+51 954 777 988</strong></div><button class="copiar" type="button" data-copiar="+51954777988">Copiar</button></div>
        <div class="dato"><div><small>Correo</small><strong id="txt-mail">matosolarte@gmail.com</strong></div><button class="copiar" type="button" data-copiar="matosolarte@gmail.com">Copiar</button></div>
        <div class="dato"><div><small>Atención</small><strong>Lun–Sáb 9:00–20:00</strong></div></div>
      </div>
    </div>
  </section>
</main>
 
<footer>
  <div class="wrap">
    <span>© 2026 Librerías Andinas · Perú</span>
    <span>Libro de Reclamaciones disponible en tienda y en línea</span>
  </div>
</footer>
<div class="tejido" aria-hidden="true"></div>
 
<!-- Chatbot -->
<button class="chat-toggle" id="chat-toggle" type="button" aria-controls="chat" aria-expanded="false">
  <svg width="20" height="20" viewBox="0 0 24 24" aria-hidden="true"><path fill="currentColor" d="M4 3h16a2 2 0 0 1 2 2v11a2 2 0 0 1-2 2H9l-5 4v-4H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2z"/></svg>
  ¿Tienes una pregunta?
</button>
 
<div class="chat" id="chat" role="dialog" aria-label="Asistente de Librerías Andinas" hidden>
  <div class="chat-head">
    <div class="av">A</div>
    <div><b>Amaru · Librerías Andinas</b><small>Asistente virtual</small></div>
    <button type="button" id="chat-cerrar" aria-label="Cerrar chat">×</button>
  </div>
  <div class="chat-body" id="chat-body" aria-live="polite"></div>
  <form class="chat-form" id="chat-form">
    <input id="chat-input" type="text" placeholder="Escribe tu pregunta…" autocomplete="off" aria-label="Escribe tu pregunta">
    <button type="submit">Enviar</button>
  </form>
</div>
 
<script>
(function(){
  const WHATSAPP = "51954777988";
  const CORREO = "matosolarte@gmail.com";
 
  const FAQ = [
    {q:"¿Cuál es su horario de atención?", k:["horario","hora","abren","cierran","atienden","domingo","feriado"],
     a:"Atendemos de lunes a sábado de 9:00 a.m. a 8:00 p.m., y domingos y feriados de 10:00 a.m. a 2:00 p.m. Por WhatsApp respondemos en el mismo horario."},
    {q:"¿Dónde están ubicadas sus tiendas?", k:["donde","ubicacion","ubicados","direccion","tienda","sede","local","lima","cusco","arequipa"],
     a:"Tenemos tiendas en Lima (principal), Cusco y Arequipa. Si quieres la dirección exacta de alguna, deja tu consulta y un asesor te la envía por WhatsApp."},
    {q:"¿Hacen envíos a provincias?", k:["envio","envian","provincia","delivery","despacho","mandan","region"],
     a:"Sí, enviamos a todo el Perú. En Lima Metropolitana entregamos por delivery propio y a provincias trabajamos con agencias como Olva Courier y Shalom."},
    {q:"¿Cuánto cuesta el envío y cuánto demora?", k:["costo","cuesta","precio envio","demora","tarda","dias","llega","gratis"],
     a:"Lima: desde S/ 10.00, llega en 24 a 48 horas. Provincias: desde S/ 15.00, llega en 2 a 5 días hábiles. El envío es gratis en Lima por compras desde S/ 150.00."},
    {q:"¿Qué métodos de pago aceptan?", k:["pago","pagar","yape","plin","tarjeta","transferencia","efectivo","contraentrega","visa"],
     a:"Aceptamos Yape, Plin, tarjetas de débito y crédito (Visa y Mastercard), transferencia bancaria (BCP e Interbank) y pago contraentrega en Lima."},
    {q:"¿Venden textos escolares y listas de útiles?", k:["escolar","colegio","lista","utiles","texto","primaria","secundaria","inicial"],
     a:"Sí. Envíanos la lista de tu colegio (foto o PDF) y te cotizamos todo: libros, cuadernos y útiles. Te lo entregamos forrado y etiquetado si lo pides."},
    {q:"¿Pueden conseguir un libro que no tienen?", k:["no tienen","conseguir","pedido","encargo","importar","stock","agotado","buscar libro"],
     a:"Sí, hacemos pedidos especiales. Conseguimos títulos nacionales en unos 7 días y los importados en 10 a 15 días. Se separa con un adelanto del 50 %."},
    {q:"¿Tienen descuentos para colegios o compras al por mayor?", k:["descuento","mayor","mayorista","colegio","institucion","promocion","oferta","docente","profesor"],
     a:"Sí. Colegios, universidades y bibliotecas reciben precios especiales, y los docentes tienen 10 % de descuento mostrando su credencial. Pide tu cotización a un asesor."},
    {q:"¿Cuál es la política de cambios y devoluciones?", k:["cambio","devolucion","devolver","garantia","fallado","reclamo","reclamaciones"],
     a:"Puedes cambiar un libro dentro de los 7 días de la compra, presentando tu boleta y con el libro en buen estado. Si llegó dañado, lo reponemos sin costo. También contamos con Libro de Reclamaciones."},
    {q:"¿Emiten boleta o factura?", k:["boleta","factura","ruc","comprobante","sunat","dni"],
     a:"Sí, emitimos boleta o factura electrónica en todas las compras. Para factura solo necesitamos tu número de RUC y razón social."}
  ];
 
  const $ = s => document.querySelector(s);
  const chat = $("#chat"), body = $("#chat-body"), toggle = $("#chat-toggle");
  const historial = [];
  let iniciado = false;
 
  function norm(t){return t.toLowerCase().normalize("NFD").replace(/[̀-ͯ]/g,"");}
 
  function burbuja(texto, quien){
    const d = document.createElement("div");
    d.className = "msg " + quien;
    d.textContent = texto;
    body.appendChild(d);
    historial.push((quien === "yo" ? "Cliente: " : "Amaru: ") + texto);
    body.scrollTop = body.scrollHeight;
    return d;
  }
 
  function opciones(){
    const w = document.createElement("div");
    w.className = "opciones";
    FAQ.forEach((f,i) => {
      const b = document.createElement("button");
      b.type = "button"; b.className = "op"; b.textContent = f.q;
      b.addEventListener("click", () => responderFAQ(i));
      w.appendChild(b);
    });
    const a = document.createElement("button");
    a.type = "button"; a.className = "op asesor"; a.textContent = "Hablar con un asesor";
    a.addEventListener("click", () => { burbuja("Quiero hablar con un asesor", "yo"); formularioAsesor(); });
    w.appendChild(a);
    body.appendChild(w);
    body.scrollTop = body.scrollHeight;
  }
 
  function responderFAQ(i){
    burbuja(FAQ[i].q, "yo");
    setTimeout(() => {
      burbuja(FAQ[i].a, "bot");
      seguimiento();
    }, 350);
  }
 
  function seguimiento(){
    const w = document.createElement("div");
    w.className = "opciones";
    const mas = document.createElement("button");
    mas.type = "button"; mas.className = "op"; mas.textContent = "Ver otras preguntas";
    mas.addEventListener("click", () => { w.remove(); opciones(); });
    const as = document.createElement("button");
    as.type = "button"; as.className = "op asesor"; as.textContent = "Hablar con un asesor";
    as.addEventListener("click", () => { w.remove(); burbuja("Quiero hablar con un asesor", "yo"); formularioAsesor(); });
    w.append(mas, as);
    body.appendChild(w);
    body.scrollTop = body.scrollHeight;
  }
 
  function buscar(texto){
    const t = norm(texto);
    let mejor = -1, puntos = 0;
    FAQ.forEach((f,i) => {
      let p = 0;
      f.k.forEach(k => { if (t.includes(norm(k))) p += k.length > 6 ? 2 : 1; });
      if (p > puntos){ puntos = p; mejor = i; }
    });
    return mejor;
  }
 
  let contadorForm = 0;
  function formularioAsesor(){
    setTimeout(() => {
      burbuja("Déjame tus datos y tu consulta. Se la enviamos a un asesor por WhatsApp y por correo.", "bot");
      const n = ++contadorForm;
      const f = document.createElement("form");
      f.className = "lead-form";
      f.innerHTML = `
        <div><label for="ld-nombre-${n}">Nombre</label><input id="ld-nombre-${n}" required placeholder="Ej. Rosa Quispe"></div>
        <div><label for="ld-tel-${n}">Celular</label><input id="ld-tel-${n}" type="tel" required placeholder="Ej. 987 654 321"></div>
        <div><label for="ld-correo-${n}">Correo (opcional)</label><input id="ld-correo-${n}" type="email" placeholder="tu@correo.com"></div>
        <div><label for="ld-msg-${n}">Tu consulta</label><textarea id="ld-msg-${n}" required placeholder="Ej. Busco la lista escolar de 3.° de primaria"></textarea></div>
        <div class="envios">
          <button type="submit" class="wa">Enviar por WhatsApp</button>
          <button type="button" class="mail">Enviar por correo</button>
        </div>
        <div class="estado" aria-live="polite">WhatsApp: +51 954 777 988 · Correo: ${CORREO}</div>`;
      body.appendChild(f);
      body.scrollTop = body.scrollHeight;
 
      const campo = id => f.querySelector("#ld-" + id + "-" + n);
      const estado = f.querySelector(".estado");
 
      function mensaje(){
        const nombre = campo("nombre").value.trim(), tel = campo("tel").value.trim(),
              correo = campo("correo").value.trim(), msg = campo("msg").value.trim();
        return {nombre, tel, correo, msg,
          texto: "Nueva consulta desde la web de Librerías Andinas\n\n" +
                 "Nombre: " + nombre + "\nCelular: " + tel + (correo ? "\nCorreo: " + correo : "") +
                 "\nConsulta: " + msg +
                 "\n\n--- Conversación con el asistente ---\n" + historial.join("\n")};
      }
 
      function valido(){
        if (!f.reportValidity()) return false;
        return true;
      }
 
      // WhatsApp
      f.addEventListener("submit", e => {
        e.preventDefault();
        if (!valido()) return;
        const m = mensaje();
        const url = "https://wa.me/" + WHATSAPP + "?text=" + encodeURIComponent(m.texto);
        const a = document.createElement("a");
        a.href = url; a.target = "_blank"; a.rel = "noopener";
        document.body.appendChild(a); a.click(); a.remove();
        estado.textContent = "Se abrió WhatsApp con tu mensaje listo. Pulsa Enviar en WhatsApp para completarlo.";
        burbuja("Gracias, " + m.nombre + ". Un asesor te responderá al " + m.tel + " en horario de atención.", "bot");
      });
 
      // Correo: intenta envío automático (FormSubmit) y si no, abre el cliente de correo
      f.querySelector(".mail").addEventListener("click", async () => {
        if (!valido()) return;
        const m = mensaje();
        estado.textContent = "Enviando…";
        let enviado = false;
        try {
          const r = await fetch("https://formsubmit.co/ajax/" + CORREO, {
            method:"POST",
            headers:{"Content-Type":"application/json","Accept":"application/json"},
            body: JSON.stringify({
              _subject:"Nueva consulta web – " + m.nombre,
              _template:"box",
              Nombre:m.nombre, Celular:m.tel, Correo:m.correo || "—",
              Consulta:m.msg, Conversacion:historial.join("\n")
            })
          });
          const d = await r.json();
          enviado = r.ok && String(d.success) === "true";
        } catch(err){ enviado = false; }
 
        if (enviado){
          estado.textContent = "Consulta enviada al correo de Librerías Andinas.";
          burbuja("Listo, " + m.nombre + ". Recibimos tu consulta por correo y te contactaremos pronto.", "bot");
        } else {
          const url = "mailto:" + CORREO + "?subject=" + encodeURIComponent("Consulta web – " + m.nombre) + "&body=" + encodeURIComponent(m.texto);
          const a = document.createElement("a"); a.href = url;
          document.body.appendChild(a); a.click(); a.remove();
          estado.textContent = "Abrimos tu aplicación de correo con el mensaje listo. Si no se abrió, escríbenos a " + CORREO + ".";
        }
      });
    }, 350);
  }
 
  function iniciar(){
    if (iniciado) return; iniciado = true;
    burbuja("¡Hola! Soy Amaru, el asistente de Librerías Andinas. Elige una pregunta o escríbeme la tuya.", "bot");
    opciones();
  }
 
  function abrir(irAsesor){
    chat.hidden = false; toggle.setAttribute("aria-expanded","true");
    iniciar();
    if (irAsesor){ burbuja("Quiero dejar una consulta", "yo"); formularioAsesor(); }
    setTimeout(() => $("#chat-input").focus(), 50);
  }
  function cerrar(){ chat.hidden = true; toggle.setAttribute("aria-expanded","false"); toggle.focus(); }
 
  toggle.addEventListener("click", () => chat.hidden ? abrir(false) : cerrar());
  $("#chat-cerrar").addEventListener("click", cerrar);
  document.querySelectorAll("[data-abrir-chat]").forEach(b =>
    b.addEventListener("click", () => abrir(b.hasAttribute("data-ir-asesor"))));
  document.addEventListener("keydown", e => { if (e.key === "Escape" && !chat.hidden) cerrar(); });
 
  $("#chat-form").addEventListener("submit", e => {
    e.preventDefault();
    const inp = $("#chat-input"), t = inp.value.trim();
    if (!t) return;
    inp.value = "";
    burbuja(t, "yo");
    const i = buscar(t);
    setTimeout(() => {
      if (i >= 0){ burbuja(FAQ[i].a, "bot"); seguimiento(); }
      else {
        burbuja("No tengo esa respuesta, pero un asesor sí puede ayudarte.", "bot");
        formularioAsesor();
      }
    }, 350);
  });
 
  document.querySelectorAll("[data-copiar]").forEach(b => b.addEventListener("click", async () => {
    try { await navigator.clipboard.writeText(b.dataset.copiar); b.textContent = "Copiado"; }
    catch(e){
      const s = b.parentElement.querySelector("strong");
      const r = document.createRange(); r.selectNodeContents(s);
      const sel = getSelection(); sel.removeAllRanges(); sel.addRange(r);
      b.textContent = "Seleccionado";
    }
    setTimeout(() => b.textContent = "Copiar", 1800);
  }));
 
  // Abrir el chat al cargar para mostrarlo en funcionamiento (en pantallas grandes)
  if (window.matchMedia("(min-width: 900px)").matches) abrir(false);
})();
</script>
</body>
</html>
