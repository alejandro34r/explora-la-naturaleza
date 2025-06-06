# explora-la-naturaleza
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Explora la Naturaleza</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>🌿 Explora la Naturaleza</h1>
    <nav>
      <ul>
        <li><a href="#temas">Temas</a></li>
        <li><a href="#experimentos">Experimentos</a></li>
        <li><a href="#juegos">Juegos</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <section id="bienvenida">
    <h2>¡Bienvenido a tu mundo natural!</h2>
    <p>Aprende sobre plantas, animales, el cuerpo humano, la materia y el universo.</p>
  </section>

  <section id="temas">
    <h2>Temas Principales</h2>
    <div class="temas-grid">
      <div class="tema"><h3>🧬 Biología</h3><p>Células, plantas, animales, ecosistemas.</p></div>
      <div class="tema"><h3>🌡️ Física</h3><p>Fuerzas, energía, movimiento, luz y sonido.</p></div>
      <div class="tema"><h3>🧪 Química</h3><p>Átomos, mezclas, reacciones químicas.</p></div>
      <div class="tema"><h3🌍> Geología</h3><p>Capas de la Tierra, volcanes, rocas, fósiles.</p></div>
    </div>
  </section>

  <section id="experimentos">
    <h2>🔬 Experimentos Caseros</h2>
    <ul>
      <li><strong>Volcán de bicarbonato:</strong> Aprende reacciones químicas usando vinagre y bicarbonato.</li>
      <li><strong>Arcoíris líquido:</strong> Explora densidades con miel, agua y aceite.</li>
    </ul>
  </section>

  <section id="juegos">
    <h2>🎮 Juegos y Quiz</h2>
    <button onclick="mostrarPregunta()">¡Haz clic para jugar!</button>
    <p id="pregunta"></p>
  </section>

  <section id="contacto">
    <h2>✉️ Contáctanos</h2>
    <form>
      <label>Nombre: <input type="text" required /></label><br />
      <label>Email: <input type="email" required /></label><br />
      <label>Mensaje:<br /><textarea required></textarea></label><br />
      <button type="submit">Enviar</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Explora la Naturaleza - Todos los derechos reservados.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f0f9f0;
  color: #333;
}

header {
  background: #4caf50;
  color: white;
  padding: 1em;
  text-align: center;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
  gap: 2em;
  padding: 0;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

section {
  padding: 2em;
}

.temas-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1em;
}

.tema {
  background: white;
  border: 1px solid #ccc;
  padding: 1em;
  border-radius: 10px;
  transition: transform 0.3s;
}

.tema:hover {
  transform: scale(1.05);
  border-color: #4caf50;
}

footer {
  background: #4caf50;
  color: white;
  text-align: center;
  padding: 1em;
}
function mostrarPregunta() {
  const preguntas = [
    "¿Qué parte de la célula contiene el ADN?",
    "¿Qué planeta es conocido como el planeta rojo?",
    "¿Qué tipo de energía se obtiene del sol?",
    "¿Cómo se llama el cambio de sólido a líquido?"
  ];

  const aleatorio = Math.floor(Math.random() * preguntas.length);
  document.getElementById("pregunta").textContent = preguntas[aleatorio];
}
