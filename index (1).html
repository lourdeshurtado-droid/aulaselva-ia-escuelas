<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Prototipo AulaSelva IA</title>
<meta name="description" content="Prototipo interactivo con datos ficticios de AulaSelva IA, una IA que funciona sin internet para docentes y estudiantes de escuelas rurales de Napo. Challenge NAUFest 2026.">
<meta property="og:title" content="Prototipo AulaSelva IA">
<meta property="og:description" content="La inteligencia artificial que sale a la chakra: aprendizaje sin internet para escuelas rurales de Napo.">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Atkinson+Hyperlegible:ital,wght@0,400;0,700;1,400&family=Lexend:wght@500;600&display=swap">
<style>:root{color-scheme:light}html{-webkit-text-size-adjust:100%}body{margin:0}[hidden]:not([hidden=until-found i]){display:none!important}</style>
<style>
  /* Concepto: una aplicación de aula en pantalla pequeña. Barra de estado fija arriba, cuatro pasos como recorrido real
     (planificar, aprender, ver avances, territorio) y en cada paso una línea que separa lo que hace la IA de lo que hace la persona. */
  :root {
    --bg: #F4F8F3; --surface: #FFFFFF; --surface2: #E8F0E9; --fg: #1B2A21; --muted: #53645A;
    --line: #D2DFD4; --line-strong: #8FA796;
    --primary: #1B5E3F; --on-primary: #FFFFFF;
    --accent: #17807F; --accent-bg: #DCEFEF; --accent-fg: #0E5F5E;
    --warn-bg: #FBE9D0; --warn-fg: #7A4608;
    --ok-bg: #DDF0E6; --ok-fg: #14512F;
    --idle-bg: #E8ECE9; --idle-fg: #46544B;
    --font-display: 'Lexend', system-ui, sans-serif;
    --font-body: 'Atkinson Hyperlegible', system-ui, -apple-system, 'Segoe UI', sans-serif;
  }
  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --bg: #0E1713; --surface: #16231D; --surface2: #1E3028; --fg: #E5EEE7; --muted: #9BB0A2;
      --line: #2A3F33; --line-strong: #5A7766;
      --primary: #5CC392; --on-primary: #0B1410;
      --accent: #4CC3C1; --accent-bg: #17383A; --accent-fg: #8FE0DE;
      --warn-bg: #3A2D14; --warn-fg: #F3C27A;
      --ok-bg: #1B3A2A; --ok-fg: #9BE0BB;
      --idle-bg: #243129; --idle-fg: #A9BBAF;
      color-scheme: dark;
    }
  }
  :root[data-theme="dark"] {
    --bg: #0E1713; --surface: #16231D; --surface2: #1E3028; --fg: #E5EEE7; --muted: #9BB0A2;
    --line: #2A3F33; --line-strong: #5A7766;
    --primary: #5CC392; --on-primary: #0B1410;
    --accent: #4CC3C1; --accent-bg: #17383A; --accent-fg: #8FE0DE;
    --warn-bg: #3A2D14; --warn-fg: #F3C27A;
    --ok-bg: #1B3A2A; --ok-fg: #9BE0BB;
    --idle-bg: #243129; --idle-fg: #A9BBAF;
    color-scheme: dark;
  }

  * { box-sizing: border-box; }
  body {
    background: var(--bg); color: var(--fg); font-family: var(--font-body); font-size: 16px; line-height: 1.5;
    padding-block: 0 40px;
    padding-left: max(16px, env(safe-area-inset-left, 0px));
    padding-right: max(16px, env(safe-area-inset-right, 0px));
  }
  .wrap { max-width: 760px; margin: 0 auto; }
  h1, h2, h3 { font-family: var(--font-display); font-weight: 600; line-height: 1.25; text-wrap: balance; margin: 0; }
  h2 { font-size: 1.3rem; }
  h3 { font-size: 1.02rem; }
  p { margin: 0; }
  button, select, textarea { font: inherit; color: inherit; }
  :focus-visible { outline: 3px solid var(--accent); outline-offset: 2px; }

  /* barra superior */
  .top { display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; gap: 10px 16px; padding: 16px 0 12px; }
  .brand { display: flex; flex-direction: column; min-width: 0; }
  .logo { font-family: var(--font-display); font-weight: 600; font-size: 1.25rem; color: var(--primary); }
  .brand .sub { font-size: .82rem; color: var(--muted); }
  .sync { display: flex; flex-wrap: wrap; align-items: center; gap: 8px; }
  .pill { display: inline-flex; align-items: center; gap: 6px; padding: 4px 10px; border-radius: 999px; font-size: .84rem; font-weight: 700; }
  .pill::before { content: ""; width: 8px; height: 8px; border-radius: 50%; background: currentColor; }
  .pill.warn { background: var(--warn-bg); color: var(--warn-fg); }
  .pill.ok { background: var(--ok-bg); color: var(--ok-fg); }
  .pill.idle { background: var(--idle-bg); color: var(--idle-fg); }
  .pill.nodot::before { display: none; }

  .btn { border: 1.5px solid var(--primary); background: var(--primary); color: var(--on-primary); padding: 10px 16px; border-radius: 8px; font-weight: 700; cursor: pointer; }
  .btn:disabled { opacity: .6; cursor: default; }
  .btn.ghost { background: transparent; color: var(--primary); }
  .btn.small { padding: 6px 12px; font-size: .88rem; }

  .intro { color: var(--muted); font-size: .95rem; padding-bottom: 14px; max-width: 62ch; }

  /* recorrido */
  .tabs { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; margin-bottom: 18px; }
  .tab { display: flex; align-items: center; gap: 8px; text-align: left; padding: 10px; border: 1px solid var(--line); background: var(--surface); border-radius: 10px; cursor: pointer; min-width: 0; }
  .tab .n { flex: none; width: 26px; height: 26px; border-radius: 50%; display: grid; place-items: center; font: 600 .85rem var(--font-display); background: var(--surface2); color: var(--fg); }
  .tab .t { display: flex; flex-direction: column; min-width: 0; font: 600 .92rem/1.2 var(--font-display); }
  .tab small { font: 400 .76rem var(--font-body); color: var(--muted); }
  .tab[aria-selected="true"] { background: var(--primary); border-color: var(--primary); color: var(--on-primary); }
  .tab[aria-selected="true"] small { color: var(--on-primary); opacity: .85; }
  .tab[aria-selected="true"] .n { background: var(--on-primary); color: var(--primary); }
  @media (max-width: 560px) { .tabs { grid-template-columns: repeat(2, 1fr); } }

  .panel { display: flex; flex-direction: column; gap: 16px; }
  .lead { color: var(--muted); max-width: 62ch; }

  .roles { display: flex; flex-direction: column; gap: 6px; padding: 12px 14px; background: var(--surface); border: 1px solid var(--line); border-radius: 10px; }
  .role { display: flex; gap: 10px; align-items: baseline; font-size: .95rem; }
  .role span:last-child { min-width: 0; }
  .tag { flex: none; display: inline-block; min-width: 64px; text-align: center; padding: 1px 8px; border-radius: 6px; font-size: .78rem; font-weight: 700; letter-spacing: .04em; text-transform: uppercase; }
  .tag.ia { background: var(--accent); color: #fff; }
  :root[data-theme="dark"] .tag.ia { color: #07211F; }
  @media (prefers-color-scheme: dark) { :root:not([data-theme="light"]) .tag.ia { color: #07211F; } }
  .tag.human { background: var(--ok-bg); color: var(--ok-fg); }

  .box { background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 16px; display: flex; flex-direction: column; gap: 14px; }
  .field { display: flex; flex-direction: column; gap: 6px; }
  .field > label, .field > .lab { font-weight: 700; font-size: .92rem; }
  .static { padding: 9px 12px; background: var(--surface2); border-radius: 8px; }
  .chips { display: flex; flex-wrap: wrap; gap: 8px; }
  .chip { border: 1.5px solid var(--line-strong); background: transparent; border-radius: 999px; padding: 6px 14px; cursor: pointer; font-weight: 700; font-size: .92rem; }
  .chip[aria-pressed="true"], .chip[aria-checked="true"] { background: var(--primary); border-color: var(--primary); color: var(--on-primary); }
  .chip:disabled { opacity: .55; cursor: default; border-style: dashed; }
  textarea, select { width: 100%; padding: 10px 12px; border: 1.5px solid var(--line-strong); border-radius: 8px; background: var(--surface); }
  textarea { min-height: 74px; resize: vertical; }

  .status { font-size: .92rem; color: var(--accent-fg); background: var(--accent-bg); padding: 8px 12px; border-radius: 8px; }

  .res-head { display: flex; flex-direction: column; gap: 2px; }
  .res-head p { color: var(--muted); font-size: .92rem; }
  .cards { display: grid; grid-template-columns: repeat(auto-fit, minmax(min(100%, 280px), 1fr)); gap: 12px; }
  .card { background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 14px; display: flex; flex-direction: column; gap: 8px; min-width: 0; }
  .card .row { display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; gap: 6px 10px; }
  .grade { font: 600 1.05rem var(--font-display); color: var(--primary); }
  .lab-s { font-size: .76rem; font-weight: 700; letter-spacing: .06em; text-transform: uppercase; color: var(--muted); display: block; }
  .pairs { background: var(--accent-bg); color: var(--accent-fg); border-radius: 10px; padding: 12px 14px; display: flex; flex-direction: column; gap: 4px; }
  .pairs strong { font-family: var(--font-display); font-weight: 600; }

  .next { display: flex; justify-content: flex-end; }

  /* estudiante */
  .stu { display: flex; align-items: center; gap: 12px; }
  .avatar { width: 44px; height: 44px; border-radius: 50%; background: var(--primary); color: var(--on-primary); display: grid; place-items: center; font: 600 1.2rem var(--font-display); }
  .stu small { display: block; color: var(--muted); }
  .qprompt { font-size: 1.12rem; max-width: 52ch; }
  .opts { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 12px; }
  .opt { display: flex; flex-direction: column; align-items: stretch; gap: 10px; padding: 14px; border: 2px solid var(--line-strong); border-radius: 10px; background: var(--surface); cursor: pointer; text-align: center; }
  .opt .frac { font: 600 1.6rem var(--font-display); }
  .opt.right { border-color: var(--primary); background: var(--ok-bg); color: var(--ok-fg); }
  .opt.wrong { border-color: var(--line); background: var(--warn-bg); color: var(--warn-fg); cursor: default; }
  .opt:disabled { cursor: default; }
  .bar { width: 100%; height: auto; display: block; }
  .seg { fill: var(--surface2); stroke: var(--line-strong); stroke-width: 1.5; }
  .seg.on { fill: var(--accent); }
  .feedback { padding: 12px 14px; border-radius: 10px; background: var(--surface2); }
  .feedback.ok { background: var(--ok-bg); color: var(--ok-fg); }
  .feedback.hint { background: var(--warn-bg); color: var(--warn-fg); }
  .ia-note { display: flex; gap: 10px; align-items: baseline; font-size: .93rem; color: var(--muted); }
  .dots { display: flex; gap: 6px; align-items: center; font-size: .88rem; color: var(--muted); }
  .dot { width: 10px; height: 10px; border-radius: 50%; border: 2px solid var(--line-strong); }
  .dot.on { background: var(--primary); border-color: var(--primary); }
  .tools { display: flex; flex-wrap: wrap; gap: 8px; }

  /* avances */
  .tiles { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 10px; }
  .tile { border-radius: 10px; padding: 12px; display: flex; flex-direction: column; gap: 2px; }
  .tile b { font: 600 1.8rem/1 var(--font-display); font-variant-numeric: tabular-nums; }
  .tile span { font-size: .86rem; }
  .tile.ok { background: var(--ok-bg); color: var(--ok-fg); }
  .tile.warn { background: var(--warn-bg); color: var(--warn-fg); }
  .tile.idle { background: var(--idle-bg); color: var(--idle-fg); }
  .list { display: flex; flex-direction: column; background: var(--surface); border: 1px solid var(--line); border-radius: 10px; overflow: hidden; }
  .item { display: grid; grid-template-columns: minmax(0, 1fr) auto; gap: 4px 12px; align-items: center; padding: 12px 14px; border-top: 1px solid var(--line); }
  .item:first-child { border-top: 0; }
  .item .who { font-weight: 700; }
  .item .why { grid-column: 1 / -1; color: var(--muted); font-size: .92rem; }
  .suggest { background: var(--accent-bg); color: var(--accent-fg); border-radius: 10px; padding: 14px; display: flex; flex-direction: column; gap: 6px; }

  details.validate { background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 12px 14px; margin-top: 22px; }
  details.validate summary { cursor: pointer; font: 600 1rem var(--font-display); }
  details.validate ol { margin: 10px 0 4px; padding-left: 20px; display: flex; flex-direction: column; gap: 4px; }
  .foot { margin-top: 14px; font-size: .85rem; color: var(--muted); }

  @media (prefers-reduced-motion: reduce) { * { transition: none !important; animation: none !important; } }
  @media (max-width: 420px) { .opts { gap: 8px; } .opt { padding: 10px; } .tile b { font-size: 1.5rem; } }
</style>
</head>
<body>
<div class="wrap">
  <header class="top">
    <div class="brand">
      <span class="logo">AulaSelva IA</span>
      <span class="sub">Prototipo con datos ficticios</span>
    </div>
    <div class="sync">
      <span id="syncPill" class="pill warn">Sin internet · todo se guarda en este equipo</span>
      <button id="syncBtn" class="btn ghost small" type="button">Simular punto con señal</button>
    </div>
  </header>

  <p class="intro">Recorre los cuatro pasos en orden. En cada uno verás qué hace la inteligencia artificial y qué sigue haciendo la persona. Todo funciona sin conexión; solo los avances se envían cuando hay señal.</p>

  <nav class="tabs" role="tablist" aria-label="Recorrido de la solución">
    <button class="tab" role="tab" id="t-planificar" data-tab="planificar" aria-selected="true" aria-controls="p-planificar" type="button"><span class="n">1</span><span class="t">Planificar<small>Docente</small></span></button>
    <button class="tab" role="tab" id="t-aprender" data-tab="aprender" aria-selected="false" aria-controls="p-aprender" type="button"><span class="n">2</span><span class="t">Aprender<small>Estudiante</small></span></button>
    <button class="tab" role="tab" id="t-avances" data-tab="avances" aria-selected="false" aria-controls="p-avances" type="button"><span class="n">3</span><span class="t">Ver avances<small>Docente</small></span></button>
    <button class="tab" role="tab" id="t-territorio" data-tab="territorio" aria-selected="false" aria-controls="p-territorio" type="button"><span class="n">4</span><span class="t">Territorio<small>Comunidad</small></span></button>
  </nav>

  <main>
    <!-- 1. PLANIFICAR -->
    <section class="panel" id="p-planificar" role="tabpanel" aria-labelledby="t-planificar">
      <div>
        <h2>Una lección para toda el aula</h2>
        <p class="lead">Rosa es la única docente de una escuela rural (ficticia). Mañana tiene estudiantes de 2.º a 7.º en el mismo salón.</p>
      </div>
      <div class="roles">
        <p class="role"><span class="tag ia">IA</span><span>Adapta una misma lección a cada grado y sugiere parejas de tutoría.</span></p>
        <p class="role"><span class="tag human">Docente</span><span>Elige el tema, el contexto y los grados, y revisa el resultado.</span></p>
      </div>
      <div class="box">
        <div class="field"><span class="lab">Tema</span><div class="static">Fracciones (Matemática)</div></div>
        <div class="field">
          <span class="lab" id="cropLab">Contexto de la comunidad</span>
          <div class="chips" role="radiogroup" aria-labelledby="cropLab" id="cropChips"></div>
        </div>
        <div class="field">
          <span class="lab" id="gradeLab">Grados presentes en el aula</span>
          <div class="chips" id="gradeChips" aria-labelledby="gradeLab"></div>
        </div>
        <div><button class="btn" id="genBtn" type="button">Generar lección</button></div>
        <p class="status" id="genStatus" role="status" hidden></p>
      </div>
      <div id="lesson" aria-live="polite"></div>
      <div class="next"><button class="btn ghost" data-go="aprender" type="button">Siguiente: Aprender</button></div>
    </section>

    <!-- 2. APRENDER -->
    <section class="panel" id="p-aprender" role="tabpanel" aria-labelledby="t-aprender" hidden>
      <div>
        <h2>Un tutor para cada estudiante</h2>
        <p class="lead">Mateo (ficticio) cursa 4.º. Rosa atiende a otro grupo mientras él practica.</p>
      </div>
      <div class="roles">
        <p class="role"><span class="tag ia">IA</span><span>Elige el siguiente ejercicio y da pistas según cada respuesta.</span></p>
        <p class="role"><span class="tag human">Estudiante</span><span>Observa, decide y responde. Puede escuchar la pregunta en voz alta.</span></p>
      </div>
      <div class="box" id="qbox"></div>
      <div class="next"><button class="btn ghost" data-go="avances" type="button">Siguiente: Ver avances</button></div>
    </section>

    <!-- 3. AVANCES -->
    <section class="panel" id="p-avances" role="tabpanel" aria-labelledby="t-avances" hidden>
      <div>
        <h2>Quién necesita ayuda ahora</h2>
        <p class="lead">Rosa mira el resumen de la clase sin revisar cuaderno por cuaderno. Lo que hizo Mateo en el paso anterior aparece aquí.</p>
      </div>
      <div class="roles">
        <p class="role"><span class="tag ia">IA</span><span>Resume el avance de cada estudiante y propone cómo reagrupar.</span></p>
        <p class="role"><span class="tag human">Docente</span><span>Decide si acepta la sugerencia y a quién atiende primero.</span></p>
      </div>
      <div id="dash"></div>
      <div class="next"><button class="btn ghost" data-go="territorio" type="button">Siguiente: Territorio</button></div>
    </section>

    <!-- 4. TERRITORIO -->
    <section class="panel" id="p-territorio" role="tabpanel" aria-labelledby="t-territorio" hidden>
      <div>
        <h2>Aprender con lo que hay en la chakra</h2>
        <p class="lead">Sofía (ficticia, 6.º) registra un saber de su familia. La escuela lo convierte en clases.</p>
      </div>
      <div class="roles">
        <p class="role"><span class="tag ia">IA</span><span>Propone una actividad por área a partir del saber registrado.</span></p>
        <p class="role"><span class="tag human">Comunidad</span><span>Aporta el saber. Docente y una persona de la comunidad lo revisan antes de usarlo.</span></p>
      </div>
      <div class="box">
        <div class="field"><label for="terrCrop">Planta o cultivo</label><select id="terrCrop"></select></div>
        <div class="field"><label for="terrNote">Lo que cuenta la familia</label><textarea id="terrNote">Mi abuela la prepara por las mañanas, antes de salir a la chakra.</textarea></div>
        <div><button class="btn" id="terrBtn" type="button">Convertir en lecciones</button></div>
        <p class="status" id="terrStatus" role="status" hidden></p>
      </div>
      <div id="terr" aria-live="polite"></div>
    </section>
  </main>

  <details class="validate">
    <summary>Para probar con una o dos personas</summary>
    <p style="margin-top:8px">Muéstrales el prototipo sin explicar y pregúntales:</p>
    <ol>
      <li>¿Qué problema resuelve?</li>
      <li>¿Cómo funciona?</li>
      <li>¿Qué hace la IA?</li>
      <li>¿Qué parte no se entiende con claridad?</li>
    </ol>
  </details>
  <p class="foot">Nombres, escuela y avances de este prototipo son inventados. La voz en kichwa se incorporará cuando la validen hablantes de la comunidad.</p>
</div>

<script>
(function () {
  var $ = function (s, r) { return (r || document).querySelector(s); };
  var $$ = function (s, r) { return Array.prototype.slice.call((r || document).querySelectorAll(s)); };

  var CROPS = {
    guayusa: { label: 'Guayusa', u: 'atados de guayusa', art: 'la guayusa' },
    cacao: { label: 'Cacao', u: 'mazorcas de cacao', art: 'el cacao' },
    yuca: { label: 'Yuca', u: 'yucas', art: 'la yuca' }
  };
  var LESSON = {
    2: { obj: 'Reconocer la mitad.', sup: 'Material real para contar',
         act: function (c) { return 'Reparte 8 ' + c.u + ' en dos montones iguales. ¿Cuántos hay en cada montón? Cada montón es la mitad.'; } },
    3: { obj: 'Entender partes iguales con 1/4.', sup: 'Plantilla con canastos',
         act: function (c) { return 'Dibuja 4 canastos iguales con ' + c.u + ' y pinta uno. ¿Qué fracción pintaste?'; } },
    4: { obj: 'Comparar fracciones.', sup: 'Tiras de papel para comparar',
         act: function (c) { return 'Una familia lleva 1/2 de sus ' + c.u + ' y otra lleva 1/4. ¿Cuál lleva más? Dibuja y explica.'; } },
    5: { obj: 'Sumar fracciones con igual denominador.', sup: 'Guía paso a paso',
         act: function (c) { return 'De un total de ' + c.u + ', el lunes se cosechó 2/8 y el martes 3/8. ¿Qué fracción se cosechó en total?'; } },
    6: { obj: 'Reconocer fracciones equivalentes.', sup: 'Trabajo autónomo con autocorrección',
         act: function (c) { return 'Con un dibujo, muestra que 1/2 del total de ' + c.u + ' es igual a 4/8. Inventa otro par equivalente.'; } },
    7: { obj: 'Resolver problemas con fracciones.', sup: 'Autónomo; guía a un compañero menor',
         act: function (c) { return 'De 40 ' + c.u + ' se venden 3/5. ¿Cuántos quedan? Plantea la operación y explica tu razonamiento.'; } }
  };

  var state = {
    crop: 'guayusa',
    grades: { 2: true, 3: true, 4: true, 5: true, 6: true, 7: true },
    q: 1, wrong: { 1: 0, 2: 0 }, solved: { 1: false, 2: false }, locked: {}, fb: null,
    synced: false
  };

  /* ---------- navegación ---------- */
  function go(id) {
    $$('.tab').forEach(function (b) {
      var on = b.dataset.tab === id;
      b.setAttribute('aria-selected', on ? 'true' : 'false');
      b.tabIndex = on ? 0 : -1;
    });
    $$('.panel').forEach(function (p) { p.hidden = p.id !== 'p-' + id; });
    if (id === 'avances') renderDash();
    try { window.scrollTo({ top: 0 }); } catch (e) {}
  }
  $$('.tab').forEach(function (b) { b.addEventListener('click', function () { go(b.dataset.tab); }); });
  $$('[data-go]').forEach(function (b) { b.addEventListener('click', function () { go(b.dataset.go); }); });

  /* ---------- estado de conexión ---------- */
  var pill = $('#syncPill'), syncBtn = $('#syncBtn');
  function renderSync(mode) {
    if (mode === 'offline') {
      pill.className = 'pill warn'; pill.textContent = 'Sin internet · todo se guarda en este equipo';
      syncBtn.textContent = 'Simular punto con señal'; syncBtn.disabled = false;
    } else if (mode === 'syncing') {
      pill.className = 'pill idle'; pill.textContent = 'Sincronizando avances…';
      syncBtn.disabled = true;
    } else {
      pill.className = 'pill ok'; pill.textContent = 'Con señal · avances sincronizados';
      syncBtn.textContent = 'Volver a modo sin señal'; syncBtn.disabled = false;
    }
  }
  syncBtn.addEventListener('click', function () {
    if (!state.synced) {
      renderSync('syncing');
      setTimeout(function () { state.synced = true; renderSync('online'); }, 1200);
    } else {
      state.synced = false; renderSync('offline');
    }
  });

  /* ---------- 1. planificar ---------- */
  function renderCropChips() {
    var box = $('#cropChips'); box.innerHTML = '';
    Object.keys(CROPS).forEach(function (k) {
      var b = document.createElement('button');
      b.type = 'button'; b.className = 'chip'; b.setAttribute('role', 'radio');
      b.setAttribute('aria-checked', state.crop === k ? 'true' : 'false');
      b.textContent = CROPS[k].label;
      b.addEventListener('click', function () { state.crop = k; renderCropChips(); renderQ(); });
      box.appendChild(b);
    });
  }
  function renderGradeChips() {
    var box = $('#gradeChips'); box.innerHTML = '';
    [2, 3, 4, 5, 6, 7].forEach(function (g) {
      var b = document.createElement('button');
      b.type = 'button'; b.className = 'chip';
      b.setAttribute('aria-pressed', state.grades[g] ? 'true' : 'false');
      b.textContent = g + '.º';
      b.addEventListener('click', function () {
        var count = Object.keys(state.grades).filter(function (k) { return state.grades[k]; }).length;
        if (state.grades[g] && count === 1) return;
        state.grades[g] = !state.grades[g]; renderGradeChips();
      });
      box.appendChild(b);
    });
  }
  function selectedGrades() {
    return [2, 3, 4, 5, 6, 7].filter(function (g) { return state.grades[g]; });
  }
  function pairsOf(list) {
    var out = [], i = 0, j = list.length - 1;
    while (i < j) { out.push(list[j] + '.º guía a ' + list[i] + '.º'); i++; j--; }
    return { out: out, solo: i === j ? list[i] + '.º trabaja con la docente' : null };
  }
  function renderLesson() {
    var c = CROPS[state.crop], gs = selectedGrades(), p = pairsOf(gs);
    var html = '<div class="res-head"><h3>Fracciones con ' + c.u + '</h3><p>Una lección, ' + gs.length + (gs.length === 1 ? ' nivel' : ' niveles') + '. Lista para usar sin conexión.</p></div><div class="cards">';
    gs.forEach(function (g) {
      var L = LESSON[g];
      html += '<article class="card"><div class="row"><span class="grade">' + g + '.º grado</span><span class="pill idle nodot">' + L.sup + '</span></div>' +
        '<div><span class="lab-s">Objetivo</span>' + L.obj + '</div>' +
        '<div><span class="lab-s">Actividad</span>' + L.act(c) + '</div></article>';
    });
    html += '</div>';
    var pairText = p.out.join(' · ') + (p.solo ? (p.out.length ? ' · ' : '') + p.solo : '');
    html += '<div class="pairs" style="margin-top:12px"><strong>Parejas de tutoría sugeridas por la IA</strong><span>' + pairText + '</span></div>';
    $('#lesson').innerHTML = html;
  }
  $('#genBtn').addEventListener('click', function () {
    var btn = this, st = $('#genStatus');
    btn.disabled = true; st.hidden = false; st.textContent = 'La IA está adaptando la lección a cada grado…';
    setTimeout(function () { renderLesson(); st.hidden = true; btn.disabled = false; }, 900);
  });

  /* ---------- 2. aprender ---------- */
  function barSVG(n) {
    var w = 120 / n, s = '<svg class="bar" viewBox="0 0 120 20" role="img" aria-label="1 de ' + n + ' partes iguales">';
    for (var i = 0; i < n; i++) s += '<rect class="seg' + (i === 0 ? ' on' : '') + '" x="' + (i * w) + '" y="1" width="' + w + '" height="18"/>';
    return s + '</svg>';
  }
  function questionFor(n) {
    if (n === 1) return { a: 2, b: 4, ans: 'a', note: null };
    if (state.wrong[1] === 0) return { a: 5, b: 3, ans: 'b', note: 'La IA subió la dificultad porque resolviste el ejercicio anterior a la primera.' };
    return { a: 3, b: 2, ans: 'b', note: 'La IA propone un caso más sencillo para repasar, porque el ejercicio anterior necesitó pistas.' };
  }
  function speak(text) {
    try {
      var u = new SpeechSynthesisUtterance(text); u.lang = 'es-419';
      window.speechSynthesis.cancel(); window.speechSynthesis.speak(u);
    } catch (e) {}
  }
  function renderQ() {
    var box = $('#qbox'), c = CROPS[state.crop];
    if (state.q === 3) {
      var total = state.wrong[1] + state.wrong[2];
      box.innerHTML = '<div class="stu"><div class="avatar" aria-hidden="true">M</div><div><h3>Mateo terminó</h3><small>4.º grado</small></div></div>' +
        '<div class="feedback ok">Resolviste los 2 ejercicios' + (total === 0 ? ' sin usar pistas.' : ' usando ' + total + (total === 1 ? ' pista.' : ' pistas.')) + '</div>' +
        '<p class="ia-note"><span class="tag ia">IA</span><span>Guardó el resumen en este equipo. Se enviará al panel de la docente cuando haya señal.</span></p>' +
        '<div class="tools"><button class="btn" data-go2="avances" type="button">Ver el panel de la docente</button><button class="btn ghost" id="resetQ" type="button">Repetir como Mateo</button></div>';
      $('[data-go2]', box).addEventListener('click', function () { go('avances'); });
      $('#resetQ', box).addEventListener('click', resetQ);
      return;
    }
    var q = questionFor(state.q), text = 'Una familia lleva 1/' + q.a + ' de sus ' + c.u + ' y otra lleva 1/' + q.b + '. ¿Cuál lleva más?';
    var html = '<div class="stu"><div class="avatar" aria-hidden="true">M</div><div><h3>Mateo</h3><small>4.º grado</small></div></div>' +
      '<div class="dots" aria-label="Ejercicio ' + state.q + ' de 2"><span class="dot' + (state.q >= 1 ? ' on' : '') + '"></span><span class="dot' + (state.q >= 2 ? ' on' : '') + '"></span><span>Ejercicio ' + state.q + ' de 2</span></div>';
    if (q.note) html += '<p class="ia-note"><span class="tag ia">IA</span><span>' + q.note + '</span></p>';
    html += '<p class="qprompt">' + text + '</p>' +
      '<div class="tools"><button class="btn ghost small" id="say" type="button">Escuchar en español</button><button class="chip" disabled type="button" title="En validación con la comunidad">Kichwa · en validación</button></div>' +
      '<div class="opts">';
    ['a', 'b'].forEach(function (k) {
      var n = q[k], cls = 'opt', dis = '';
      if (state.locked[state.q + k] === 'wrong') { cls += ' wrong'; dis = ' disabled'; }
      if (state.solved[state.q]) { dis = ' disabled'; if (k === q.ans) cls += ' right'; }
      html += '<button class="' + cls + '" data-k="' + k + '" type="button"' + dis + '><span class="frac">1/' + n + '</span>' + barSVG(n) + '</button>';
    });
    html += '</div>';
    if (state.fb) html += '<div class="feedback ' + state.fb.kind + '" role="status">' + state.fb.text + '</div>';
    if (state.solved[state.q]) html += '<div><button class="btn" id="nextQ" type="button">' + (state.q === 1 ? 'Siguiente ejercicio' : 'Terminar') + '</button></div>';
    box.innerHTML = html;
    $('#say', box).addEventListener('click', function () { speak(text); });
    $$('.opt', box).forEach(function (b) {
      b.addEventListener('click', function () {
        var k = b.dataset.k;
        if (k === q.ans) {
          state.solved[state.q] = true;
          state.fb = { kind: 'ok', text: state.wrong[state.q] === 0 ? 'Correcto, a la primera. Cuando el total se parte en menos partes, cada parte es más grande.' : 'Eso es. Ahora lo ves en las barras: menos partes, partes más grandes.' };
        } else {
          state.wrong[state.q]++; state.locked[state.q + k] = 'wrong';
          state.fb = { kind: 'hint', text: 'Mira las barras: cuando el total se parte en más partes, cada parte se hace más pequeña. Prueba otra vez.' };
        }
        renderQ();
      });
    });
    var nx = $('#nextQ', box);
    if (nx) nx.addEventListener('click', function () { state.q++; state.fb = null; renderQ(); });
  }
  function resetQ() {
    state.q = 1; state.wrong = { 1: 0, 2: 0 }; state.solved = { 1: false, 2: false }; state.locked = {}; state.fb = null; renderQ();
  }

  /* ---------- 3. avances ---------- */
  function renderDash() {
    var total = state.wrong[1] + state.wrong[2], mateo;
    if (state.q === 3) {
      if (total >= 2) mateo = { k: 'warn', s: 'Necesita apoyo', why: 'Usó ' + total + ' pistas al comparar fracciones.' };
      else mateo = { k: 'ok', s: 'Va bien', why: total === 0 ? 'Comparó fracciones sin pistas.' : 'Comparó fracciones con una pista.' };
    } else if (state.solved[1] || state.wrong[1] > 0) mateo = { k: 'idle', s: 'En curso', why: 'Está resolviendo el ejercicio de comparar fracciones.' };
    else mateo = { k: 'idle', s: 'Sin empezar', why: 'Aún no abrió el tutor. Haz el paso 2 para ver su avance aquí.' };
    var rows = [
      { n: 'Carlos', g: '7.º', k: 'ok', s: 'Va bien', why: 'Resolvió el problema de venta sin ayuda.' },
      { n: 'Sofía', g: '6.º', k: 'ok', s: 'Va bien', why: 'Encontró dos fracciones equivalentes.' },
      { n: 'Ana', g: '5.º', k: 'warn', s: 'Necesita apoyo', why: 'Suma los denominadores en lugar de dejarlos iguales.' },
      { n: 'Mateo', g: '4.º', k: mateo.k, s: mateo.s, why: mateo.why },
      { n: 'Lucía', g: '3.º', k: 'warn', s: 'Necesita apoyo', why: 'Todavía no reconoce cuándo las partes son iguales.' },
      { n: 'Kevin', g: '2.º', k: 'idle', s: 'Sin empezar', why: 'Trabaja con material real junto a la docente.' }
    ];
    var cnt = { ok: 0, warn: 0, idle: 0 }; rows.forEach(function (r) { cnt[r.k]++; });
    var need = rows.filter(function (r) { return r.k === 'warn'; }).map(function (r) { return r.n + ' (' + r.g + ')'; });
    var h = '<div class="tiles"><div class="tile ok"><b>' + cnt.ok + '</b><span>Van bien</span></div><div class="tile warn"><b>' + cnt.warn + '</b><span>Necesitan apoyo</span></div><div class="tile idle"><b>' + cnt.idle + '</b><span>Sin empezar o en curso</span></div></div>';
    h += '<div class="list" style="margin-top:12px">';
    rows.forEach(function (r) {
      h += '<div class="item"><span class="who">' + r.n + ' · ' + r.g + '</span><span class="pill ' + r.k + '">' + r.s + '</span><span class="why">' + r.why + '</span></div>';
    });
    h += '</div>';
    h += '<div class="suggest" style="margin-top:12px"><span class="lab-s" style="color:inherit"><span class="tag ia" style="margin-right:6px">IA</span>Sugerencia para la docente</span>' +
      '<span>' + (need.length ? 'Reúne a ' + need.join(', ') + ' durante 10 minutos con tiras de papel para comparar partes. Mientras tanto, Carlos (7.º) puede guiar a Kevin (2.º).' : 'Nadie necesita apoyo por ahora. Carlos (7.º) puede guiar a Kevin (2.º) con material real.') + '</span></div>';
    $('#dash').innerHTML = h;
  }

  /* ---------- 4. territorio ---------- */
  function renderTerrSelect() {
    var s = $('#terrCrop');
    Object.keys(CROPS).forEach(function (k) {
      var o = document.createElement('option'); o.value = k; o.textContent = CROPS[k].label; s.appendChild(o);
    });
  }
  function renderTerr() {
    var c = CROPS[$('#terrCrop').value] || CROPS.guayusa, a = c.art;
    var A = a.charAt(0).toUpperCase() + a.slice(1);
    $('#terr').innerHTML =
      '<div class="res-head"><h3>Lecciones a partir de ' + a + '</h3><p>Propuestas de la IA. Aún no se usan en clase.</p></div>' +
      '<div class="cards" style="margin-top:12px">' +
      '<article class="card"><div class="row"><span class="grade">Matemática</span><span class="pill idle nodot">2.º a 4.º</span></div><div>Contamos y agrupamos ' + c.u + ': ¿cuántos montones iguales podemos armar?</div></article>' +
      '<article class="card"><div class="row"><span class="grade">Ciencias</span><span class="pill idle nodot">5.º a 7.º</span></div><div>¿Dónde crece mejor ' + a + '? Observamos luz, suelo y agua en tres chakras y comparamos.</div></article>' +
      '<article class="card"><div class="row"><span class="grade">Lengua</span><span class="pill idle nodot">Todos los grados</span></div><div>Cada estudiante escribe o cuenta, a su nivel, una historia de su familia con ' + a + '.</div></article>' +
      '</div>' +
      '<div class="pairs" style="margin-top:12px"><strong>Antes de usarlo en clase</strong><span>La docente y una persona de la comunidad revisan que el saber de la familia esté bien representado. ' + A + ' queda registrada en el banco de saberes de la escuela.</span></div>';
  }
  $('#terrBtn').addEventListener('click', function () {
    var btn = this, st = $('#terrStatus');
    btn.disabled = true; st.hidden = false; st.textContent = 'La IA está preparando actividades por área…';
    setTimeout(function () { renderTerr(); st.hidden = true; btn.disabled = false; }, 900);
  });

  /* ---------- arranque en estado de trabajo ---------- */
  renderCropChips(); renderGradeChips(); renderLesson();
  renderQ(); renderTerrSelect(); renderTerr(); renderSync('offline'); renderDash();
  $$('.tab').forEach(function (b, i) { b.tabIndex = i === 0 ? 0 : -1; });
})();
</script>
</body>
</html>
