<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Perfil Minecraft</title>
  <!-- Fuente Pixel estilo Minecraft -->
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: #0d0417;
      font-family: 'Press Start 2P', monospace;
      color: #ffffff;
      overflow-x: hidden;
    }

    /* Contenedor de cada dimensión con TU IMAGEN de fondo */
    .biome-section {
      width: 100%;
      min-height: 420px;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 40px 20px;
      position: relative;
    }

    /* Capa oscura suave para que el texto de enfrente se lea perfecto */
    .biome-section::before {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.35);
      z-index: 1;
    }

    /* Todo el contenido va ENFRENTE de la imagen (z-index: 2) */
    .overlay-content {
      position: relative;
      z-index: 2;
      max-width: 950px;
      width: 100%;
      text-align: center;
    }

    /* TUS 3 IMÁGENES COMO BACKGROUND */
    .overworld-bg {
      background-image: url('./fila-1-columna-1.jpg');
    }
    .nether-bg {
      background-image: url('./fila-2-columna-1.jpg');
    }
    .end-bg {
      background-image: url('./fila-3-columna-1.jpg');
    }

    /* Estilo de Letrero de Madera (Overworld) */
    .mc-wood-sign {
      background: #9c6f44;
      border: 4px solid #4a3219;
      box-shadow: inset 0 0 0 3px #b88655, 0 8px 20px rgba(0,0,0,0.7);
      padding: 18px 25px;
      display: inline-block;
      margin-bottom: 25px;
      text-shadow: 3px 3px 0px #2b1d0e;
    }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
      margin-top: 10px;
    }

    .mc-card {
      background: rgba(156, 111, 68, 0.92);
      border: 4px solid #3d2814;
      padding: 16px;
      font-size: 11px;
      line-height: 1.7;
      text-shadow: 2px 2px 0 #000;
      transition: transform 0.2s, border-color 0.2s;
      cursor: pointer;
    }

    .mc-card:hover {
      transform: translateY(-5px) scale(1.03);
      border-color: #ffff55;
    }

    /* Estilo de Ventana de Inventario Gris (The Nether) */
    .mc-gui-window {
      background: rgba(198, 198, 198, 0.92);
      border: 4px solid #000;
      box-shadow: inset 4px 4px 0px #fff, inset -4px -4px 0px #555, 0 10px 25px rgba(0,0,0,0.8);
      padding: 25px;
      color: #2b2b2b;
    }

    .mc-gui-title {
      font-size: 14px;
      margin-bottom: 20px;
      color: #3f3f3f;
      text-shadow: none;
    }

    /* Casillas interactivas del inventario */
    .inventory-slots {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-bottom: 20px;
    }

    .slot {
      width: 64px;
      height: 64px;
      background: #8b8b8b;
      border-top: 4px solid #373737;
      border-left: 4px solid #373737;
      border-right: 4px solid #ffffff;
      border-bottom: 4px solid #ffffff;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      cursor: pointer;
    }

    .slot:hover {
      background: #a8a8a8;
    }

    .slot img {
      width: 42px;
      height: 42px;
    }

    /* Tooltip estilo Minecraft al pasar el mouse */
    .slot::after {
      content: attr(data-tooltip);
      position: absolute;
      bottom: 110%;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(16, 0, 16, 0.94);
      border: 2px solid #5000ff;
      color: #fff;
      padding: 6px 10px;
      font-size: 9px;
      white-space: nowrap;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.15s;
      z-index: 10;
    }

    .slot:hover::after {
      opacity: 1;
    }

    /* Botones estilo Minecraft (The End) */
    .mc-btn {
      display: inline-block;
      background: #727272;
      border: 3px solid #000;
      box-shadow: inset 3px 3px 0 #aaa, inset -3px -3px 0 #444;
      color: #fff;
      text-decoration: none;
      padding: 14px 22px;
      font-size: 11px;
      margin: 8px;
      text-shadow: 2px 2px 0 #222;
      transition: 0.15s;
    }

    .mc-btn:hover {
      background: #7b52ab;
      border-color: #ffff55;
      color: #ffff55;
    }
  </style>
</head>
<body>

  <!-- 🌳 1. OVERWORLD (Con fila-1-columna-1.jpg de fondo) -->
  <section class="biome-section overworld-bg">
    <div class="overlay-content">
      <div class="mc-wood-sign">
        <h1 style="font-size: 20px; margin-bottom: 10px;">⛏️ ¡HOLA! SOY [TU NOMBRE]</h1>
        <p style="font-size: 11px; color: #ffe082;">Desarrollador Full Stack | Creador de mundos</p>
      </div>

      <div class="cards-grid">
        <div class="mc-card">
          🏡 <b>BASE ACTUAL:</b><br><br>
          [Nombre de tu Proyecto]
        </div>
        <div class="mc-card">
          📚 <b>ENCANTAMIENTOS:</b><br><br>
          [Tecnologías que estudias]
        </div>
        <div class="mc-card">
          💬 <b>ALDEANO EXPERTO:</b><br><br>
          [Tus lenguajes fuertes]
        </div>
      </div>
    </div>
  </section>

  <!-- 🔥 2. THE NETHER (Con tu imagen fila-2-columna-1.jpg de fondo) -->
  <section class="biome-section nether-bg">
    <div class="overlay-content">
      <div class="mc-gui-window">
        <h2 class="mc-gui-title">🔥 INVENTARIO DE HERRAMIENTAS Y STATS</h2>

        <!-- Casillas con íconos reales y nombre flotante al pasar el mouse -->
        <div class="inventory-slots">
          <div class="slot" data-tooltip="JavaScript (Nivel Encantado)">
            <img src="https://skillicons.dev/icons?i=js" alt="JS">
          </div>
          <div class="slot" data-tooltip="TypeScript">
            <img src="https://skillicons.dev/icons?i=ts" alt="TS">
          </div>
          <div class="slot" data-tooltip="React">
            <img src="https://skillicons.dev/icons?i=react" alt="React">
          </div>
          <div class="slot" data-tooltip="Node.js">
            <img src="https://skillicons.dev/icons?i=nodejs" alt="Node">
          </div>
          <div class="slot" data-tooltip="Python">
            <img src="https://skillicons.dev/icons?i=python" alt="Python">
          </div>
          <div class="slot" data-tooltip="Git & GitHub">
            <img src="https://skillicons.dev/icons?i=git" alt="Git">
          </div>
        </div>

        <!-- Estadísticas de GitHub encima del fondo del Nether -->
        <div>
          <img src="https://github-readme-stats.vercel.app/api?username=TU_USUARIO&show_icons=true&theme=gruvbox&hide_border=true" height="140" alt="stats">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=TU_USUARIO&layout=compact&theme=gruvbox&hide_border=true" height="140" alt="langs">
        </div>
      </div>
    </div>
  </section>

  <!-- 🐉 3. THE END (Con fila-3-columna-1.jpg de fondo) -->
  <section class="biome-section end-bg">
    <div class="overlay-content">
      <div class="mc-wood-sign" style="background: #2b153d; border-color: #8c00ff; box-shadow: inset 0 0 0 3px #4a236b;">
        <h2 style="font-size: 16px;">🐉 EL FINAL DEL VIAJE — ¡CONECTEMOS!</h2>
      </div>
      <br>
      <a href="mailto:tu_correo@ejemplo.com" class="mc-btn">📫 ENVIAR CORREO</a>
      <a href="https://github.com/TU_USUARIO" class="mc-btn">💻 GITHUB</a>
      <a href="https://tu-web.com" class="mc-btn">🌐 PORTAFOLIO WEB</a>
    </div>
  </section>

</body>
</html>
