# MAPEATE# Mapeate - Landing Page

Este repositorio contiene el código fuente de la landing page para la aplicación **Mapeate**. El proyecto está diseñado con un enfoque moderno, utilizando un tema oscuro, efectos de glassmorphism y animaciones sutiles para ofrecer una experiencia de usuario premium.

## Descripción del Proyecto

Mapeate es una aplicación de navegación inteligente que optimiza rutas y viajes. Esta landing page sirve como punto de entrada para que los usuarios conozcan las características de la app, descarguen el APK y proporcionen feedback a través de una encuesta integrada.

## Características Principales

-   **Diseño Moderno**: Tema oscuro con paleta de colores azul/cian y efectos de cristal.
-   **Responsive**: Totalmente adaptable a dispositivos móviles y de escritorio.
-   **Secciones**:
    -   **Hero**: Presentación principal con llamada a la acción.
    -   **Acerca de**: Destaca las ventajas competitivas (Rutas precisas, Tiempo real, Seguridad).
    -   **Descarga**: Enlace directo al archivo APK.
    -   **Encuesta**: Formulario interactivo para recopilar opiniones de usuarios.
-   **Sin Dependencias Externas**: Construido con HTML5, CSS3 y JavaScript puro (Vanilla).

## Estructura del Repositorio

```
Mapeate/
├── assets/
│   ├── logo.png          # Logo de la aplicación
│   └── app_mockup.png    # Imagen de muestra de la interfaz
├── docs/
│   └── screenshots/      # Capturas de pantalla del proyecto
├── index.html            # Estructura HTML de la página
├── styles.css            # Estilos CSS
├── Mapeate.apk           # Archivo de instalación de la app (Placeholder)
├── README.md             # Documentación del proyecto
└── .gitignore            # Archivos ignorados por git
```

## Código Fuente

A continuación se presenta el código completo del proyecto, debidamente comentado en español.

### `index.html`

```html
<!-- Definicion del tipo de documento HTML5 -->
<!DOCTYPE html>
<html lang="es">

<!-- Cabecera del documento: contiene metadatos, enlaces a fuentes y hojas de estilo -->
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapeate - Tu Ruta Inteligente</title>
    <meta name="description" content="Descarga Mapeate, la aplicación definitiva para optimizar tus rutas y viajes.">
    <!-- Preconexion a Google Fonts para mejorar el rendimiento de carga -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <!-- Importacion de la fuente Outfit desde Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Icono de la pestaña del navegador (favicon) -->
    <link rel="icon" type="image/png" href="assets/logo.png">
    <!-- Enlace a la hoja de estilos principal -->
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <!-- Barra de navegacion principal: contiene el logo, enlaces y menu movil -->
    <nav class="navbar">
        <!-- Contenedor del logo y nombre de la marca -->
        <div class="logo">
            <img src="assets/logo.png" alt="Mapeate Logo">
            <span>Mapeate</span>
        </div>
        <!-- Lista de enlaces de navegacion para escritorio -->
        <ul class="nav-links">
            <li><a href="#hero">Inicio</a></li>
            <li><a href="#about">Saber más</a></li>
            <li><a href="#download" class="btn-primary">Descargar</a></li>
        </ul>
        <!-- Boton de menu hamburguesa para dispositivos moviles -->
        <div class="hamburger">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </nav>

    <!-- Seccion Hero: Primera vista del usuario con titulo principal y llamada a la accion -->
    <header id="hero" class="hero-section">
        <div class="hero-content">
            <h1>Descubre tu camino con <span class="gradient-text">Mapeate</span></h1>
            <p>La aplicación que transforma la manera en que te mueves. Rutas optimizadas, tiempo real y simplicidad en
                tu bolsillo.</p>
            <div class="hero-buttons">
                <a href="#download" class="btn-primary large">Descargar APK</a>
                <a href="#about" class="btn-secondary">Conocer más</a>
            </div>
        </div>
        <div class="hero-image">
            <img src="assets/app_mockup.png" alt="Mapeate App Interface">
        </div>
    </header>

    <!-- Seccion Acerca de: Explica las caracteristicas principales de la aplicacion -->
    <section id="about" class="about-section">
        <div class="container">
            <h2 class="section-title">¿Por qué Mapeate?</h2>
            <div class="features-grid">
                <!-- Tarjeta de caracteristica: Rutas Precisas -->
                <div class="feature-card">
                    <div class="icon">📍</div>
                    <h3>Rutas Precisas</h3>
                    <p>Encuentra siempre el mejor camino con nuestra tecnología de mapeo avanzada.</p>
                </div>
                <!-- Tarjeta de caracteristica: Tiempo Real -->
                <div class="feature-card">
                    <div class="icon">⚡</div>
                    <h3>Tiempo Real</h3>
                    <p>Actualizaciones al instante sobre el tráfico y condiciones de la vía.</p>
                </div>
                <!-- Tarjeta de caracteristica: Seguridad -->
                <div class="feature-card">
                    <div class="icon">🛡️</div>
                    <h3>Seguro y Confiable</h3>
                    <p>Tus datos y tu ubicación están protegidos con los más altos estándares.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seccion de Descarga: Enlace directo para descargar el archivo APK -->
    <section id="download" class="download-section">
        <div class="download-content">
            <h2>Lleva Mapeate contigo</h2>
            <p>Descarga la última versión de nuestra aplicación para Android y empieza a explorar hoy mismo.</p>
            <a href="Mapeate.apk" download class="btn-primary large glow">Descargar Mapeate APK</a>
            <p class="version-info">Versión 1.0.0 | Android 8.0+</p>
        </div>
    </section>

    <!-- Seccion de Encuesta: Formulario para recopilar opiniones de los usuarios -->
    <section id="survey" class="survey-section">
        <div class="container">
            <h2 class="section-title">Tu Opinión Importa</h2>
            <!-- Formulario con prevencion de envio por defecto para demostracion -->
            <form class="survey-form" onsubmit="event.preventDefault(); alert('¡Gracias por tu opinión!');">

                <!-- Pregunta 1: Satisfaccion General (Rating de estrellas) -->
                <div class="form-group">
                    <label>1. ¿Cómo calificarías tu satisfacción general con Mapeate?</label>
                    <div class="star-rating">
                        <input type="radio" name="satisfaction" id="s5" value="5"><label for="s5">★</label>
                        <input type="radio" name="satisfaction" id="s4" value="4"><label for="s4">★</label>
                        <input type="radio" name="satisfaction" id="s3" value="3"><label for="s3">★</label>
                        <input type="radio" name="satisfaction" id="s2" value="2"><label for="s2">★</label>
                        <input type="radio" name="satisfaction" id="s1" value="1"><label for="s1">★</label>
                    </div>
                </div>

                <!-- Pregunta 2: Facilidad de Uso (Selector desplegable) -->
                <div class="form-group">
                    <label>2. ¿Qué tan fácil fue usar la aplicación?</label>
                    <select name="usability">
                        <option value="" disabled selected>Selecciona una opción</option>
                        <option value="very_easy">Muy fácil</option>
                        <option value="easy">Fácil</option>
                        <option value="neutral">Normal</option>
                        <option value="hard">Difícil</option>
                        <option value="very_hard">Muy difícil</option>
                    </select>
                </div>

                <!-- Pregunta 3: Precision de Rutas (Botones de radio) -->
                <div class="form-group">
                    <label>3. ¿Cómo calificarías la precisión de las rutas?</label>
                    <div class="radio-group">
                        <label><input type="radio" name="accuracy" value="excellent"> Excelente</label>
                        <label><input type="radio" name="accuracy" value="good"> Buena</label>
                        <label><input type="radio" name="accuracy" value="average"> Regular</label>
                        <label><input type="radio" name="accuracy" value="poor"> Mala</label>
                    </div>
                </div>

                <!-- Pregunta 4: Velocidad de la App (Deslizador de rango) -->
                <div class="form-group">
                    <label>4. ¿Cómo percibes la velocidad de la aplicación?</label>
                    <input type="range" min="1" max="5" value="3" class="slider" id="speedRange">
                    <div class="range-labels">
                        <span>Lenta</span>
                        <span>Rápida</span>
                    </div>
                </div>

                <!-- Pregunta 5: Diseño Visual (Rating de estrellas) -->
                <div class="form-group">
                    <label>5. ¿Te gusta el diseño visual de la app?</label>
                    <div class="star-rating">
                        <input type="radio" name="design" id="d5" value="5"><label for="d5">★</label>
                        <input type="radio" name="design" id="d4" value="4"><label for="d4">★</label>
                        <input type="radio" name="design" id="d3" value="3"><label for="d3">★</label>
                        <input type="radio" name="design" id="d2" value="2"><label for="d2">★</label>
                        <input type="radio" name="design" id="d1" value="1"><label for="d1">★</label>
                    </div>
                </div>

                <!-- Pregunta 6: Funcionalidad Favorita (Selector desplegable) -->
                <div class="form-group">
                    <label>6. ¿Cuál es tu funcionalidad favorita?</label>
                    <select name="favorite_feature">
                        <option value="" disabled selected>Selecciona una opción</option>
                        <option value="routes">Optimización de Rutas</option>
                        <option value="traffic">Tráfico en Tiempo Real</option>
                        <option value="maps">Mapas Offline</option>
                        <option value="interface">Interfaz de Usuario</option>
                        <option value="other">Otra</option>
                    </select>
                </div>

                <!-- Pregunta 7: Encontraste destino (Botones de radio Si/No) -->
                <div class="form-group">
                    <label>7. ¿Encontraste tu destino fácilmente?</label>
                    <div class="radio-group">
                        <label><input type="radio" name="found_dest" value="yes"> Sí</label>
                        <label><input type="radio" name="found_dest" value="no"> No</label>
                    </div>
                </div>

                <!-- Pregunta 8: Recomendacion (Entrada numerica) -->
                <div class="form-group">
                    <label>8. ¿Qué tanto recomendarías Mapeate? (0-10)</label>
                    <input type="number" min="0" max="10" placeholder="0-10" class="input-field">
                </div>

                <!-- Pregunta 9: Frecuencia de Uso (Selector desplegable) -->
                <div class="form-group">
                    <label>9. ¿Con qué frecuencia usas apps de navegación?</label>
                    <select name="frequency">
                        <option value="" disabled selected>Selecciona una opción</option>
                        <option value="daily">Diariamente</option>
                        <option value="weekly">Semanalmente</option>
                        <option value="monthly">Mensualmente</option>
                        <option value="rarely">Rara vez</option>
                    </select>
                </div>

                <!-- Pregunta 10: Comentarios (Area de texto) -->
                <div class="form-group full-width">
                    <label>10. ¿Tienes algún comentario o sugerencia de mejora?</label>
                    <textarea rows="4" placeholder="Escribe tu opinión aquí..."></textarea>
                </div>

                <!-- Boton de envio del formulario -->
                <button type="submit" class="btn-primary full-width">Enviar Encuesta</button>
            </form>
        </div>
    </section>

    <!-- Pie de pagina: Derechos de autor -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Mapeate. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- Scripts JavaScript para interactividad -->
    <script>
        /**
         * Elemento del boton de menu hamburguesa.
         * @type {HTMLElement}
         */
        const hamburger = document.querySelector('.hamburger');

        /**
         * Contenedor de los enlaces de navegacion.
         * @type {HTMLElement}
         */
        const navLinks = document.querySelector('.nav-links');

        /**
         * Event listener para alternar la visibilidad del menu en moviles.
         * Agrega o quita la clase 'active' al hacer clic.
         */
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        /**
         * Selecciona todos los enlaces que apuntan a anclas internas.
         * Agrega desplazamiento suave (smooth scroll) al hacer clic.
         */
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>

</html>
```

### `styles.css`

```css
:root {
    /* Color de fondo principal de la aplicacion */
    --bg-color: #0f172a;
    /* Color de texto principal para contraste */
    --text-color: #e2e8f0;
    /* Color primario utilizado en botones y elementos destacados */
    --primary-color: #38bdf8;
    /* Color secundario para efectos de degradado */
    --secondary-color: #818cf8;
    /* Color de acento para detalles visuales */
    --accent-color: #22d3ee;
    /* Fondo semitransparente para las tarjetas */
    --card-bg: rgba(30, 41, 59, 0.7);
    /* Borde sutil para crear el efecto de cristal (glassmorphism) */
    --glass-border: rgba(255, 255, 255, 0.1);
    /* Fuente principal de la aplicacion */
    --font-main: 'Outfit', sans-serif;
}

/* Reseteo basico de margenes y relleno para todos los elementos */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Estilos generales del cuerpo del documento */
body {
    font-family: var(--font-main);
    background-color: var(--bg-color);
    color: var(--text-color);
    line-height: 1.6;
    overflow-x: hidden;
}

/* Tipografia: Estilos para encabezados */
h1,
h2,
h3 {
    font-weight: 700;
    line-height: 1.2;
}

/* Clase de utilidad para texto con degradado */
.gradient-text {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Estilos para botones primarios */
.btn-primary {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: #fff;
    padding: 0.8rem 1.5rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    transition: transform 0.3s ease,
        box-shadow 0.3s ease;
    display: inline-block;
    border: none;
}

/* Efecto hover para botones primarios */
.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 20px rgba(56, 189, 248, 0.3);
}

/* Estilos para botones secundarios (bordeado) */
.btn-secondary {
    background: transparent;
    color: var(--text-color);
    padding: 0.8rem 1.5rem;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    border: 2px solid var(--primary-color);
    transition: all 0.3s ease;
    display: inline-block;
}

/* Efecto hover para botones secundarios */
.btn-secondary:hover {
    background: rgba(56, 189, 248, 0.1);
}

/* Clase de utilidad para botones grandes */
.large {
    padding: 1rem 2.5rem;
    font-size: 1.1rem;
}

/* Animacion de resplandor para elementos destacados */
.glow {
    animation: glow 2s infinite alternate;
}

/* Definicion de la animacion de resplandor (keyframes) */
@keyframes glow {
    from {
        box-shadow: 0 0 10px rgba(56, 189, 248, 0.5);
    }

    to {
        box-shadow: 0 0 20px rgba(56, 189, 248, 0.8), 0 0 30px rgba(129, 140, 248, 0.6);
    }
}

/* Barra de navegacion: Estilos y posicionamiento fijo */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    background: rgba(15, 23, 42, 0.8);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--glass-border);
}

/* Estilos para el logo en la barra de navegacion */
.logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary-color);
}

.logo img {
    height: 40px;
}

/* Enlaces de navegacion */
.nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
    align-items: center;
}

.nav-links a {
    color: var(--text-color);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
}

.nav-links a:not(.btn-primary):hover {
    color: var(--primary-color);
}

/* Menu hamburguesa para moviles (oculto en escritorio) */
.hamburger {
    display: none;
    flex-direction: column;
    cursor: pointer;
    gap: 5px;
}

.hamburger span {
    width: 25px;
    height: 3px;
    background-color: var(--text-color);
    border-radius: 2px;
}

/* Seccion Hero: Estilos para la presentacion principal */
.hero-section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 8rem 5% 4rem;
    min-height: 100vh;
    background: radial-gradient(circle at top right, rgba(56, 189, 248, 0.1), transparent 40%);
}

.hero-content {
    flex: 1;
    max-width: 600px;
}

.hero-content h1 {
    font-size: 3.5rem;
    margin-bottom: 1.5rem;
}

.hero-content p {
    font-size: 1.2rem;
    color: #94a3b8;
    margin-bottom: 2.5rem;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
}

/* Imagen del Hero con animacion de flotacion */
.hero-image {
    flex: 1;
    display: flex;
    justify-content: center;
    position: relative;
}

.hero-image img {
    max-width: 100%;
    height: auto;
    max-height: 600px;
    filter: drop-shadow(0 20px 40px rgba(0, 0, 0, 0.5));
    animation: float 6s ease-in-out infinite;
}

/* Definicion de la animacion de flotacion */
@keyframes float {
    0% {
        transform: translateY(0px);
    }

    50% {
        transform: translateY(-20px);
    }

    100% {
        transform: translateY(0px);
    }
}

/* Seccion Acerca de: Estilos generales */
.about-section {
    padding: 6rem 5%;
    background: #1e293b;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}

.section-title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 4rem;
}

/* Cuadricula para las tarjetas de caracteristicas */
.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

/* Estilos de las tarjetas de caracteristicas */
.feature-card {
    background: var(--card-bg);
    padding: 2rem;
    border-radius: 20px;
    border: 1px solid var(--glass-border);
    transition: transform 0.3s;
    text-align: center;
}

.feature-card:hover {
    transform: translateY(-10px);
    background: rgba(30, 41, 59, 0.9);
}

.feature-card .icon {
    font-size: 3rem;
    margin-bottom: 1.5rem;
}

.feature-card h3 {
    margin-bottom: 1rem;
    color: var(--primary-color);
}

/* Seccion de Descarga: Estilos y fondo degradado */
.download-section {
    padding: 8rem 5%;
    text-align: center;
    background: linear-gradient(to bottom, #1e293b, #0f172a);
}

.download-content {
    max-width: 800px;
    margin: 0 auto;
}

.download-content h2 {
    font-size: 3rem;
    margin-bottom: 1.5rem;
}

.download-content p {
    font-size: 1.2rem;
    color: #94a3b8;
    margin-bottom: 3rem;
}

.version-info {
    margin-top: 1.5rem;
    font-size: 0.9rem;
    opacity: 0.7;
}

/* Seccion de Encuesta: Estilos del contenedor */
.survey-section {
    padding: 6rem 5%;
    background: #0f172a;
}

/* Estilos del formulario de encuesta */
.survey-form {
    max-width: 800px;
    margin: 0 auto;
    background: var(--card-bg);
    padding: 3rem;
    border-radius: 20px;
    border: 1px solid var(--glass-border);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
}

/* Grupos de formulario (etiqueta + input) */
.form-group {
    display: flex;
    flex-direction: column;
    gap: 0.8rem;
}

.form-group.full-width {
    grid-column: span 2;
}

.form-group label {
    font-weight: 600;
    color: var(--primary-color);
}

/* Estilos para campos de entrada, selectores y areas de texto */
.input-field,
select,
textarea {
    padding: 1rem;
    border-radius: 10px;
    border: 1px solid var(--glass-border);
    background: rgba(15, 23, 42, 0.6);
    color: var(--text-color);
    font-family: var(--font-main);
    width: 100%;
}

.input-field:focus,
select:focus,
textarea:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 10px rgba(56, 189, 248, 0.2);
}

/* Sistema de calificacion por estrellas */
.star-rating {
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-end;
    gap: 5px;
}

.star-rating input {
    display: none;
}

.star-rating label {
    font-size: 1.5rem;
    color: #475569;
    cursor: pointer;
    transition: color 0.2s;
}

.star-rating input:checked ~ label,
.star-rating label:hover,
.star-rating label:hover ~ label {
    color: #fbbf24;
}

/* Grupo de botones de radio */
.radio-group {
    display: flex;
    gap: 1.5rem;
    align-items: center;
}

.radio-group label {
    color: var(--text-color);
    font-weight: 400;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

/* Deslizador de rango personalizado */
.slider {
    -webkit-appearance: none;
    appearance: none;
    width: 100%;
    height: 8px;
    border-radius: 5px;
    background: #334155;
    outline: none;
}

.slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: var(--primary-color);
    cursor: pointer;
    transition: background .15s ease-in-out;
}

.range-labels {
    display: flex;
    justify-content: space-between;
    font-size: 0.9rem;
    color: #94a3b8;
}

button[type="submit"] {
    grid-column: span 2;
    margin-top: 1rem;
    cursor: pointer;
    font-size: 1.1rem;
}

/* Estilos responsivos para la encuesta en moviles */
@media (max-width: 768px) {
    .survey-form {
        grid-template-columns: 1fr;
        padding: 1.5rem;
    }

    .form-group.full-width,
    button[type="submit"] {
        grid-column: span 1;
    }
}

/* Pie de pagina */
footer {
    padding: 2rem 5%;
    text-align: center;
    border-top: 1px solid var(--glass-border);
    color: #64748b;
}

/* Estilos responsivos generales para moviles */
@media (max-width: 768px) {
    .hero-section {
        flex-direction: column;
        text-align: center;
        padding-top: 6rem;
    }

    .hero-content h1 {
        font-size: 2.5rem;
    }

    .hero-buttons {
        justify-content: center;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: var(--bg-color);
        flex-direction: column;
        padding: 2rem;
        border-bottom: 1px solid var(--glass-border);
    }

    .nav-links.active {
        display: flex;
    }

    .hamburger {
        display: flex;
    }
}
```
