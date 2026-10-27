
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b1120">

  <title>Equipo 02 | Presentación</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Glass+Antiqua&family=Playwrite+HU:wght@100..400&display=swap" rel="stylesheet">

  <style>
    :root {
      --background: #080e1b;
      --surface: #101a2d;
      --surface-light: #15233a;
      --primary: #8bbcff;
      --accent: #5a9cff;
      --text: #f0f4fc;
      --muted: #9baac0;
      --border: rgba(164, 193, 235, 0.16);

      --display-font: "Glass Antiqua", serif;
      --hand-font: "Playwrite HU", cursive;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background:
        radial-gradient(
          ellipse at 50% 0%,
          rgba(39, 93, 164, 0.18),
          transparent 45%
        ),
        var(--background);
      color: var(--text);
      font-family: var(--display-font);
      font-size: 18px;
      line-height: 1.8;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1080px, 90%);
      margin: 0 auto;
    }

    /* Navegación */

    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      padding: 24px 0;
      border-bottom: 1px solid var(--border);
    }

    .brand {
      font-family: var(--display-font);
      font-size: 1.8rem;
      letter-spacing: 0.04em;
    }

    .brand span {
      color: var(--primary);
    }

    .nav-label {
      color: var(--muted);
      font-size: 0.85rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    /* Cabecera */

    .hero {
      position: relative;
      overflow: hidden;
      padding: 100px 35px 85px;
      margin-top: 32px;
      text-align: center;
      border: 1px solid var(--border);
      border-radius: 28px;
      background:
        radial-gradient(
          circle at 80% 20%,
          rgba(75, 143, 255, 0.2),
          transparent 35%
        ),
        linear-gradient(
          135deg,
          #111d32 0%,
          #142747 55%,
          #0c1425 100%
        );
    }

    .hero::before {
      content: "02";
      position: absolute;
      right: -10px;
      bottom: -100px;
      font-family: var(--display-font);
      font-size: clamp(220px, 35vw, 440px);
      line-height: 1;
      color: rgba(181, 211, 255, 0.035);
      pointer-events: none;
    }

    .eyebrow {
      position: relative;
      color: var(--primary);
      font-size: 0.8rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
    }

    .hero h1 {
      position: relative;
      margin: 15px 0;
      font-family: var(--display-font);
      font-size: clamp(4rem, 11vw, 8rem);
      font-weight: 400;
      line-height: 1.05;
      letter-spacing: 0.025em;
    }

    .hero h1 span {
      color: var(--primary);
    }

    .hero-description {
      position: relative;
      max-width: 600px;
      margin: 25px auto 0;
      color: #d0dced;
      font-family: var(--hand-font);
      font-size: clamp(0.8rem, 2vw, 1rem);
      line-height: 2.1;
    }

    .hero-meta {
      position: relative;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 12px;
      margin-top: 35px;
    }

    .pill {
      padding: 7px 15px;
      border: 1px solid rgba(172, 204, 255, 0.25);
      border-radius: 100px;
      color: #dceaff;
      font-size: 0.8rem;
      background: rgba(255, 255, 255, 0.035);
    }

    /* Secciones */

    .section {
      padding: 80px 0 0;
      scroll-margin-top: 24px;
    }

    .section-heading {
      display: flex;
      align-items: center;
      gap: 18px;
      margin-bottom: 28px;
    }

    .section-number {
      color: var(--accent);
      font-size: 1.1rem;
      letter-spacing: 0.06em;
    }

    h2 {
      font-family: var(--display-font);
      font-size: clamp(2rem, 5vw, 3rem);
      font-weight: 400;
      line-height: 1.2;
    }

    .section-line {
      height: 1px;
      flex: 1;
      background: var(--border);
    }

    .intro-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 24px;
    }

    .panel {
      padding: 30px;
      border: 1px solid var(--border);
      border-radius: 18px;
      background: var(--surface);
    }

    .panel p {
      color: #c5d0e0;
      font-size: 1rem;
    }

    .panel p + p {
      margin-top: 16px;
    }

    .stat-panel {
      display: flex;
      flex-direction: column;
      justify-content: center;
      min-height: 220px;
      background:
        linear-gradient(
          145deg,
          rgba(55, 108, 184, 0.16),
          transparent
        ),
        var(--surface);
    }

    .stat-number {
      color: var(--primary);
      font-size: 5rem;
      line-height: 1.1;
    }

    .stat-label {
      margin-top: 8px;
      color: var(--muted);
      font-size: 0.85rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .handwritten {
      margin-top: 18px;
      color: var(--primary);
      font-family: var(--hand-font);
      font-size: 0.85rem;
      line-height: 2;
    }

    /* Integrantes */

    .members-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 14px;
    }

    .member-card {
      display: flex;
      align-items: center;
      gap: 20px;
      min-height: 115px;
      padding: 22px;
      border: 1px solid var(--border);
      border-radius: 16px;
      background: linear-gradient(
        115deg,
        var(--surface-light),
        var(--surface)
      );
      transition:
        transform 180ms ease,
        border-color 180ms ease,
        background 180ms ease;
    }

    .member-card:hover {
      transform: translateY(-3px);
      border-color: rgba(139, 188, 255, 0.55);
      background: #172740;
    }

    .member-number {
      display: grid;
      place-items: center;
      flex: 0 0 48px;
      width: 48px;
      height: 48px;
      border: 1px solid rgba(139, 188, 255, 0.3);
      border-radius: 12px;
      color: var(--primary);
      font-size: 1.2rem;
    }

    .member-name {
      font-size: 1.05rem;
      line-height: 1.5;
    }

    .member-role {
      margin-top: 5px;
      color: var(--muted);
      font-size: 0.78rem;
    }

    /* Principios */

    .principles-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 16px;
    }

    .principle-card {
      padding: 25px;
      border: 1px solid var(--border);
      border-radius: 16px;
      background: var(--surface);
    }

    .principle-index {
      color: var(--accent);
      font-size: 0.8rem;
      letter-spacing: 0.12em;
    }

    .principle-card h3 {
      margin: 12px 0;
      font-size: 1.35rem;
      font-weight: 400;
    }

    .principle-card p {
      color: var(--muted);
      font-size: 0.9rem;
      line-height: 1.8;
    }

    /* Compromiso */

    .commitment {
      position: relative;
      overflow: hidden;
      padding: 42px;
      border: 1px solid rgba(139, 188, 255, 0.22);
      border-radius: 20px;
      background: linear-gradient(
        125deg,
        #152b4b,
        #101a2d 75%
      );
    }

    .commitment h3 {
      margin-bottom: 15px;
      color: var(--primary);
      font-size: 1.7rem;
      font-weight: 400;
    }

    .commitment p {
      max-width: 760px;
      color: #d0dced;
    }

    .commitment .handwritten {
      margin-top: 25px;
    }

    /* Pie */

    footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 85px;
      padding: 28px 0;
      border-top: 1px solid var(--border);
      color: var(--muted);
      font-size: 0.78rem;
    }

    .footer-brand {
      color: var(--text);
      font-size: 1.15rem;
    }

    /* Accesibilidad y adaptación */

    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }

      *,
      *::before,
      *::after {
        transition-duration: 0.01ms !important;
      }
    }

    @media (max-width: 700px) {
      .navbar {
        align-items: flex-start;
      }

      .nav-label {
        max-width: 130px;
        text-align: right;
      }

      .hero {
        padding: 75px 20px 65px;
        border-radius: 20px;
      }

      .intro-grid,
      .members-grid {
        grid-template-columns: 1fr;
      }

      .principles-grid {
        grid-template-columns: 1fr;
      }

      .section {
        padding-top: 58px;
      }

      .panel,
      .commitment {
        padding: 24px;
      }

      footer {
        margin-top: 55px;
      }
    }
  </style>
</head>

<body>
  <div class="container">

    <nav class="navbar" aria-label="Navegación principal">
      <a class="brand" href="#inicio">EQUIPO <span>02</span></a>
      <div class="nav-label">Presentación del equipo</div>
    </nav>

    <header class="hero" id="inicio">
      <p class="eyebrow">Perfil institucional · 2026</p>

      <h1>Equipo <span>02</span></h1>

      <p class="hero-description">
        Seis integrantes trabajando en el desarrollo
        de un proyecto común.
      </p>

      <div class="hero-meta">
        <span class="pill">06 integrantes</span>
        <span class="pill">Trabajo colaborativo</span>
        <span class="pill">Proyecto académico</span>
      </div>
    </header>

    <main>

      <section class="section" id="presentacion">
        <div class="section-heading">
          <span class="section-number">01</span>
          <h2>Presentación</h2>
          <div class="section-line"></div>
        </div>

        <div class="intro-grid">
          <article class="panel">
            <p>
              El Equipo 02 está conformado por seis integrantes
              que participan conjuntamente en la planificación
              y el desarrollo del proyecto.
            </p>
            <p>
              La organización del trabajo se basa en la
              coordinación de actividades, la distribución
              de responsabilidades y el seguimiento de los
              objetivos establecidos.
            </p>
          </article>

          <aside class="panel stat-panel">
            <span class="stat-number">06</span>
            <span class="stat-label">Integrantes del equipo</span>
            <p class="handwritten">
              Organización · Coordinación · Desarrollo
            </p>
          </aside>
        </div>
      </section>

      <section class="section" id="integrantes">
        <div class="section-heading">
          <span class="section-number">02</span>
          <h2>Integrantes</h2>
          <div class="section-line"></div>
        </div>

        <div class="members-grid">

          <article class="member-card">
            <div class="member-number">01</div>
            <div>
              <h3 class="member-name">Chara Franco, Johan Daymar</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

          <article class="member-card">
            <div class="member-number">02</div>
            <div>
              <h3 class="member-name">Huancas Bereche, Erick Emilio</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

          <article class="member-card">
            <div class="member-number">03</div>
            <div>
              <h3 class="member-name">Pellanne Aro, Carlos Alfredo</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

          <article class="member-card">
            <div class="member-number">04</div>
            <div>
              <h3 class="member-name">Reyes Garcia, Alvaro Pablo</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

          <article class="member-card">
            <div class="member-number">05</div>
            <div>
              <h3 class="member-name">Rivera Garayar, Matias Gabriel</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

          <article class="member-card">
            <div class="member-number">06</div>
            <div>
              <h3 class="member-name">Romero Chac, Luis Antonio</h3>
              <p class="member-role">Integrante del equipo</p>
            </div>
          </article>

        </div>
      </section>

      <section class="section" id="organizacion">
        <div class="section-heading">
          <span class="section-number">03</span>
          <h2>Organización del trabajo</h2>
          <div class="section-line"></div>
        </div>

        <div class="principles-grid">

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 01</span>
            <h3>Responsabilidad</h3>
            <p>
              Cumplimiento de las tareas asignadas y atención
              a los plazos establecidos.
            </p>
          </article>

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 02</span>
            <h3>Coordinación</h3>
            <p>
              Organización de actividades y seguimiento
              de los avances del proyecto.
            </p>
          </article>

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 03</span>
            <h3>Comunicación</h3>
            <p>
              Intercambio oportuno de información y
              colaboración en la resolución de problemas.
            </p>
          </article>

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 04</span>
            <h3>Colaboración</h3>
            <p>
              Participación conjunta en las actividades
              y decisiones relacionadas con el proyecto.
            </p>
          </article>

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 05</span>
            <h3>Calidad</h3>
            <p>
              Revisión de los entregables para verificar
              el cumplimiento de los requisitos.
            </p>
          </article>

          <article class="principle-card">
            <span class="principle-index">PRINCIPIO 06</span>
            <h3>Seguimiento</h3>
            <p>
              Revisión periódica de las tareas y
              de los objetivos pendientes.
            </p>
          </article>

        </div>
      </section>

      <section class="section" id="objetivo">
        <div class="section-heading">
          <span class="section-number">04</span>
          <h2>Objetivo y compromiso</h2>
          <div class="section-line"></div>
        </div>

        <article class="commitment">
          <h3>Objetivo del equipo</h3>

          <p>
            Desarrollar el proyecto de manera organizada
            y colaborativa, atendiendo a los requisitos
            establecidos y procurando el cumplimiento
            de las actividades y los plazos acordados.
          </p>

          <p class="handwritten">
            Equipo 02 · Presentación y documentación
          </p>
        </article>
      </section>

    </main>

    <footer>
      <span class="footer-brand">EQUIPO 02</span>
      <span>Documento de presentación del equipo de trabajo</span>
    </footer>

  </div>
</body>
</html>
