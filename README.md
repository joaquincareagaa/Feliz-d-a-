# Feliz-diaaa
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Feliz Día de la Novia ❤️</title>
  <style>
    /* Estilos Generales */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      /* Imagen de fondo por defecto. Reemplaza 'jazmines.jpg' por la tuya si querés */
      background: url('jazmines.jpg') no-repeat center center / cover, #e8f5e9;
      padding: 20px;
    }

    /* Tarjeta Principal (Overlay blanco semi-transparente) */
    .card {
      background-color: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(5px);
      border-radius: 20px;
      padding: 40px 30px;
      width: 100%;
      max-width: 500px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
      border: 1px solid rgba(255, 255, 255, 0.3);
    }

    /* Título Principal */
    h1 {
      font-family: 'Georgia', serif;
      color: #2e7d32;
      font-size: 2rem;
      margin-bottom: 20px;
    }

    /* Contenedor del Corazón */
    .heart-container {
      margin: 30px 0;
      height: 140px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* Corazón animado con CSS */
    .heart {
      width: 80px;
      height: 80px;
      background-color: #e57373;
      position: relative;
      transform: rotate(-45deg);
      animation: heartbeat 1.2s infinite ease-in-out;
      border: 2px solid #c62828;
    }

    .heart::before,
    .heart::after {
      content: "";
      width: 80px;
      height: 80px;
      background-color: #e57373;
      border-radius: 50%;
      position: absolute;
      border: 2px solid #c62828;
    }

    .heart::before {
      top: -40px;
      left: 0;
      border-bottom: none;
    }

    .heart::after {
      left: 40px;
      top: 0;
      border-left: none;
    }

    /* Animación del latido */
    @keyframes heartbeat {
      0% { transform: rotate(-45deg) scale(0.95); }
      50% { transform: rotate(-45deg) scale(1.25); }
      100% { transform: rotate(-45deg) scale(0.95); }
    }

    /* Mensaje intercalado */
    .message {
      font-size: 1.1rem;
      font-style: italic;
      color: #1b5e20;
      line-height: 1.5;
      margin-bottom: 30px;
    }

    /* Botón interactivo */
    .btn {
      background-color: #ffffff;
      color: #2e7d32;
      border: 2px solid #2e7d32;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 25px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    .btn:hover {
      background-color: #c8e6c9;
      color: #1b5e20;
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }

    /* Ventana emergente (Modal) */
    .modal-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      display: flex;
      justify-content: center;
      align-items: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
      padding: 20px;
    }

    .modal-overlay.active {
      opacity: 1;
      pointer-events: auto;
    }

    .modal-content {
      background: white;
      padding: 30px;
      border-radius: 15px;
      max-width: 400px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .modal-content h2 {
      color: #2e7d32;
      margin-bottom: 15px;
    }

    .modal-content p {
      color: #333;
      font-size: 1rem;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .close-btn {
      background: #2e7d32;
      color: white;
      border: none;
      padding: 8px 20px;
      border-radius: 15px;
      cursor: pointer;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>¡Feliz Día de la Novia!</h1>

    <div class="heart-container">
      <div class="heart"></div>
    </div>

    <p class="message">
      Gracias por iluminar mis días con tu aroma y tu sonrisa ✨
    </p>

    <button class="btn" onclick="openModal()">Toca para ver tu carta 💌</button>
  </div>

  <!-- Modal / Ventana Emergente -->
  <div class="modal-overlay" id="letterModal">
    <div class="modal-content">
      <h2>Para el amor de mi vida</h2>
      <p>
        Como los jazmines en primavera, haces que todo a mi alrededor sea más lindo y especial.<br><br>
        <strong>¡Te amo muchísimo! ❤️</strong>
      </p>
      <button class="close-btn" onclick="closeModal()">Cerrar</button>
    </div>
  </div>

  <script>
    function openModal() {
      document.getElementById('letterModal').classList.add('active');
    }

    function closeModal() {
      document.getElementById('letterModal').classList.remove('active');
    }
  </script>
</body>
</html>

