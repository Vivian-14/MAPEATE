# Mapeate - Landing Page

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
├── .gitignore            # Archivos ignorados por git
├── Mapeate.apk           # Archivo de instalación de la app (Placeholder)
└── README.md             # Documentación del proyecto
```

## Código Fuente Completo

A continuación se presenta el código completo de todos los archivos del proyecto.

### 1. `index.html`

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

### 2. `styles.css`

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

### 3. `.gitignore`

```gitignore
# Dependencias
node_modules/
.pnp
.pnp.js

# Pruebas
coverage/

# Produccion
build/
dist/

# Sistema Operativo
.DS_Store
Thumbs.db

# Logs
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Editor
.vscode/
.idea/
*.swp
```

## Código de la Aplicación Android (UNIDAD2)

### 4. `MainActivity.kt`

```kotlin
package mx.edu.utng.avht.unidad2

// Importaciones necesarias para la interfaz de usuario y funcionalidad
import android.content.Context
import android.content.Intent
import android.graphics.Bitmap
import android.net.Uri
import android.os.Bundle
import android.widget.Toast
import androidx.activity.ComponentActivity
import androidx.compose.ui.text.style.TextDecoration
import androidx.activity.compose.setContent
import androidx.activity.compose.rememberLauncherForActivityResult
import androidx.activity.result.contract.ActivityResultContracts
import androidx.core.content.FileProvider
import androidx.compose.foundation.*
import androidx.compose.foundation.layout.*
import androidx.compose.foundation.lazy.LazyColumn
import androidx.compose.foundation.lazy.grid.GridCells
import androidx.compose.foundation.lazy.grid.LazyVerticalGrid
import androidx.compose.foundation.lazy.grid.items
import androidx.compose.foundation.lazy.items
import androidx.compose.foundation.rememberScrollState
import androidx.compose.foundation.shape.CircleShape
import androidx.compose.foundation.shape.RoundedCornerShape
import androidx.compose.material3.*
import androidx.compose.material3.Scaffold
import androidx.compose.runtime.*
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.draw.clip
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.graphics.asImageBitmap
import androidx.compose.ui.layout.ContentScale
import androidx.compose.ui.platform.LocalContext
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.text.input.PasswordVisualTransformation
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp

// Importaciones de iconos y navegacion
import androidx.compose.material.icons.Icons
import androidx.compose.material3.Icon
import androidx.compose.material.icons.filled.ArrowBack
import androidx.navigation.compose.NavHost
import androidx.navigation.compose.composable
import androidx.navigation.compose.rememberNavController
import androidx.navigation.NavController
import androidx.navigation.navArgument
import androidx.navigation.NavType

// Biblioteca Coil para cargar imagenes
import coil.compose.rememberAsyncImagePainter

// Importaciones de ViewModels y Pantallas
import mx.edu.utng.avht.unidad2.screens.MapaPrincipalScreen
import mx.edu.utng.avht.unidad2.screens.NuevoContenidoScreen
import mx.edu.utng.avht.unidad2.screens.UserProfileScreen
import mx.edu.utng.avht.unidad2.viewmodel.LoginViewModel
import mx.edu.utng.avht.unidad2.viewmodel.PerfilViewModel

import java.io.File
import java.io.FileOutputStream
import java.util.*

/**
 * Actividad principal de la aplicacion.
 * Configura la navegacion y el contenido inicial.
 */
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            AppNavigation()
        }
    }
}

/**
 * Definicion de las rutas de navegacion de la aplicacion.
 */
sealed class Screen(val route: String) {
    object Login : Screen("login")
    object Principal : Screen("principal")
    object MapaPrincipal : Screen("mapa_principal")
    object Perfil : Screen("perfil")
    object Comunidad : Screen("comunidad")
    object Contenido : Screen("contenido/{lat}/{lng}") {
        fun createRoute(lat: Double, lng: Double) = "contenido/$lat/$lng"
    }
    object Register : Screen("register_screen")
}

/**
 * Configuracion del grafo de navegacion.
 * Define que pantalla mostrar para cada ruta.
 */
@Composable
fun AppNavigation() {
    val navController = rememberNavController()

    NavHost(
        navController = navController,
        startDestination = Screen.Login.route
    ) {
        // Pantalla de Login
        composable(Screen.Login.route) {
            LoginScreen(
                onLoginSuccess = {
                    navController.navigate(Screen.Principal.route) {
                        popUpTo(Screen.Login.route) { inclusive = true }
                    }
                },
                onNavigateToRegister = {
                    navController.navigate(Screen.Register.route)
                }
            )
        }

        // Pantalla de Registro
        composable(Screen.Register.route) {
            RegisterScreen(
                onBack = { navController.popBackStack() }
            )
        }

        // Pantalla Principal (Menu)
        composable(Screen.Principal.route) {
            PrincipalGto(
                onExplorarRutas = {
                    navController.navigate(Screen.MapaPrincipal.route)
                },
                onNavigateToPerfil = {
                    navController.navigate(Screen.Perfil.route)
                },
                onNavigateToComunidad = {
                    navController.navigate(Screen.Comunidad.route)
                }
            )
        }

        // Pantalla del Mapa Principal
        composable(Screen.MapaPrincipal.route) {
            mx.edu.utng.avht.unidad2.screens.MapaPrincipalScreen(
                onNavigateBack = { navController.popBackStack() },
                onNavigateToPerfil = { navController.navigate(Screen.Perfil.route) },
                onNavigateToComunidad = { navController.navigate(Screen.Comunidad.route) },
                onNavigateToContenido = { lat, lng ->
                    navController.navigate(Screen.Contenido.createRoute(lat, lng))
                }
            )
        }

        // Pantalla para agregar Nuevo Contenido
        composable(
            route = Screen.Contenido.route,
            arguments = listOf(
                androidx.navigation.navArgument("lat") { type = androidx.navigation.NavType.FloatType },
                androidx.navigation.navArgument("lng") { type = androidx.navigation.NavType.FloatType }
            )
        ) { backStackEntry ->
            val lat = backStackEntry.arguments?.getFloat("lat")?.toDouble() ?: 0.0
            val lng = backStackEntry.arguments?.getFloat("lng")?.toDouble() ?: 0.0
            mx.edu.utng.avht.unidad2.screens.NuevoContenidoScreen(
                lat = lat,
                lng = lng,
                onNavigateBack = { navController.popBackStack() }
            )
        }

        // Pantalla de Perfil de Usuario
        composable(Screen.Perfil.route) {
            PerfilUsuarioScreen(navController = navController)
        }

        // Pantalla de Feed de Comunidad
        composable(Screen.Comunidad.route) {
            FeedComunidadScreen(onNavigateBack = { navController.popBackStack() }, navController = navController)
        }
        
        // Pantalla de Perfil de Otro Usuario
        composable(
            route = "user_profile/{userId}",
            arguments = listOf(navArgument("userId") { type = NavType.StringType })
        ) { backStackEntry ->
            val userId = backStackEntry.arguments?.getString("userId") ?: ""
            UserProfileScreen(
                userId = userId,
                onNavigateBack = { navController.popBackStack() }
            )
        }
    }
}

/**
 * Pantalla de Inicio de Sesion.
 */
@Composable
fun LoginScreen(
    viewModel: LoginViewModel = androidx.lifecycle.viewmodel.compose.viewModel(),
    onLoginSuccess: () -> Unit = {},
    onNavigateToRegister: () -> Unit = {}
) {
    val state = viewModel.uiState.collectAsState().value

    Scaffold(
        containerColor = Color(0xFFD2D0A6) // color de fondo
    ) { padding ->

        if (state.isLoginSuccessful) {
            LaunchedEffect(Unit) { onLoginSuccess() }
        }

        Column(
            modifier = Modifier
                .fillMaxSize()
                .padding(padding)
                .padding(horizontal = 24.dp),
            horizontalAlignment = Alignment.CenterHorizontally,
            verticalArrangement = Arrangement.Center
        ) {

            Text("🔐", fontSize = 50.sp)
            Spacer(Modifier.height(8.dp))

            Text(
                "Iniciar sesión",
                fontSize = 26.sp,
                fontWeight = FontWeight.Bold
            )

            Spacer(modifier = Modifier.height(40.dp))

            // Campo de Correo Electronico
            OutlinedTextField(
                value = state.email,
                onValueChange = { viewModel.onEmailChange(it) },
                label = { Text("Correo electrónico") },
                modifier = Modifier.fillMaxWidth()
            )

            Spacer(modifier = Modifier.height(16.dp))

            // Campo de Contraseña
            OutlinedTextField(
                value = state.password,
                onValueChange = { viewModel.onPasswordChange(it) },
                label = { Text("Contraseña") },
                visualTransformation = PasswordVisualTransformation(),
                modifier = Modifier.fillMaxWidth()
            )

            Spacer(modifier = Modifier.height(24.dp))

            // Boton de Iniciar Sesion
            Button(
                onClick = { viewModel.onLoginClick() },
                modifier = Modifier
                    .fillMaxWidth()
                    .height(50.dp),
                colors = ButtonDefaults.buttonColors(
                    containerColor = Color(0xFFE4A691) // Color Salmon
                )
            ) {
                Text("Iniciar sesión", color = Color.White)
            }

            // Mensaje de Error
            state.errorMessage?.let {
                Spacer(Modifier.height(12.dp))
                Text(it, color = Color.Red)
            }

            Spacer(Modifier.height(20.dp))

            // Boton para ir al Registro
            TextButton(onClick = { onNavigateToRegister() }) {
                Text("Crear cuenta", fontSize = 16.sp)
            }
        }
    }
}

/**
 * Pantalla de Registro de Usuario.
 */
@Composable
fun RegisterScreen(
    viewModel: LoginViewModel = androidx.lifecycle.viewmodel.compose.viewModel(),
    onBack: () -> Unit = {}
) {
    val state = viewModel.uiState.collectAsState().value

    // Estado local para el nombre
    var nombre by remember { mutableStateOf("") }

    Scaffold(
        containerColor = Color(0xFFF7EFD8) // Color Crema
    ) { padding ->

        Column(
            modifier = Modifier
                .fillMaxSize()
                .padding(padding)
                .padding(24.dp),
            horizontalAlignment = Alignment.CenterHorizontally
        ) {

            Row(
                modifier = Modifier.fillMaxWidth(),
                verticalAlignment = Alignment.CenterVertically
            ) {
                IconButton(onClick = { onBack() }) {
                    Icon(Icons.Default.ArrowBack, contentDescription = "Volver")
                }
            }

            Spacer(Modifier.height(10.dp))

            Text("📝", fontSize = 50.sp)
            Text("Regístrate", fontSize = 26.sp, fontWeight = FontWeight.Bold)

            Spacer(Modifier.height(40.dp))

            // Campo de Nombre
            OutlinedTextField(
                value = nombre,
                onValueChange = { nombre = it },
                label = { Text("Nombre de usuario") },
                modifier = Modifier.fillMaxWidth()
            )

            Spacer(Modifier.height(16.dp))

            // Campo de Correo
            OutlinedTextField(
                value = state.email,
                onValueChange = { viewModel.onEmailChange(it) },
                label = { Text("Correo") },
                modifier = Modifier.fillMaxWidth()
            )

            Spacer(Modifier.height(16.dp))

            // Campo de Contraseña
            OutlinedTextField(
                value = state.password,
                onValueChange = { viewModel.onPasswordChange(it) },
                label = { Text("Contraseña") },
                visualTransformation = PasswordVisualTransformation(),
                modifier = Modifier.fillMaxWidth()
            )

            Spacer(Modifier.height(24.dp))

            // Boton de Registro
            Button(
                onClick = {
                    viewModel.onRegisterClick()   // Guardar en Firebase
                    onBack()                      // Regresar al login
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .height(50.dp),
                colors = ButtonDefaults.buttonColors(
                    containerColor = Color(0xFFE4A691) // Color Salmon
                )
            ) {
                Text("Registrarme", color = Color.White)
            }

            state.errorMessage?.let {
                Spacer(Modifier.height(12.dp))
                Text(it, color = Color.Red)
            }
        }
    }
}

/**
 * Pantalla Principal (Menu de Opciones).
 */
@Composable
@Preview(showBackground = true, showSystemUi = true)
fun PrincipalGto(
    onExplorarRutas: () -> Unit = {},
    onNavigateToPerfil: () -> Unit = {},
    onNavigateToComunidad: () -> Unit = {}
) {
    val salmon = Color(0xFFE4A691)
    val crema = Color(0xFFF7EFD8)
    val verdeSuave = Color(0xFFC8C8A9)
    val azulGris = Color(0xFF556270)

    Box(
        modifier = Modifier.fillMaxSize()
    ) {

        // Imagen de fondo
        Image(
            painter = painterResource(id = R.drawable.gto_bonito),
            contentDescription = null,
            modifier = Modifier.fillMaxSize(),
            contentScale = ContentScale.Crop
        )

        // Contenido centrado
        Column(
            modifier = Modifier
                .fillMaxSize()
                .padding(horizontal = 32.dp, vertical = 40.dp),
            horizontalAlignment = Alignment.CenterHorizontally,
            verticalArrangement = Arrangement.Center
        ) {

            // Titulo MAPEATE
            Box(
                modifier = Modifier
                    .clip(RoundedCornerShape(20.dp))
                    .background(verdeSuave.copy(alpha = 0.88f))
                    .padding(horizontal = 28.dp, vertical = 14.dp)
            ) {
                Text(
                    text = "🗺️ MAPEATE",
                    fontWeight = FontWeight.ExtraBold,
                    fontSize = 32.sp,
                    color = Color.Black
                )
            }

            Spacer(modifier = Modifier.height(50.dp))

            // Botones de Navegacion
            Column(
                modifier = Modifier.fillMaxWidth(),
                horizontalAlignment = Alignment.CenterHorizontally
            ) {
                Button(
                    onClick = { onExplorarRutas() },
                    colors = ButtonDefaults.buttonColors(containerColor = crema),
                    shape = RoundedCornerShape(14.dp),
                    modifier = Modifier.fillMaxWidth().height(70.dp)
                ) {
                    Text("📍 Explorar rutas", color = azulGris)
                }

                Spacer(modifier = Modifier.height(16.dp))

                Button(
                    onClick = { onNavigateToComunidad() },
                    colors = ButtonDefaults.buttonColors(containerColor = salmon),
                    shape = RoundedCornerShape(14.dp),
                    modifier = Modifier.fillMaxWidth().height(70.dp)
                ) {
                    Text("\uD83C\uDFD8\uFE0F Comunidad", color = azulGris)
                }

                Spacer(modifier = Modifier.height(16.dp))

                Button(
                    onClick = { onNavigateToPerfil() },
                    colors = ButtonDefaults.buttonColors(containerColor = azulGris),
                    shape = RoundedCornerShape(14.dp),
                    modifier = Modifier.fillMaxWidth().height(70.dp)
                ) {
                    Text("👤 Mi perfil", color = crema)
                }
            }
        }
    }
}

/**
 * Pantalla de Detalle de Ruta (Ejemplo).
 */
@Composable
@Preview(showBackground = true, showSystemUi = true)
fun DetalleRuta() {
    val salmon = Color(0xFFE4A691)
    val crema = Color(0xFFF7EFD8)
    val verdeSuave = Color(0xFFC8C8A9)
    val azulGris = Color(0xFF556270)
    val azulOscuro = Color(0xFF273142)

    Column(
        modifier = Modifier
            .fillMaxSize()
            .background(crema)
            .verticalScroll(rememberScrollState())
            .padding(bottom = 20.dp)
    ) {
        // Encabezado
        Row(
            modifier = Modifier
                .fillMaxWidth()
                .background(crema)
                .padding(horizontal = 16.dp, vertical = 12.dp),
            verticalAlignment = Alignment.CenterVertically
        ) {
            Text(
                text = "←",
                color = azulOscuro,
                fontSize = 22.sp,
                modifier = Modifier.padding(end = 8.dp)
            )
            Text(
                text = "Detalle de Ruta",
                color = azulOscuro,
                fontSize = 20.sp,
                fontWeight = FontWeight.Bold
            )
        }

        // Header imagen
        Box(
            modifier = Modifier
                .fillMaxWidth()
                .height(220.dp)
                .background(salmon),
            contentAlignment = Alignment.Center
        ) {
            Text("Imagen del lugar", color = azulOscuro, fontSize = 16.sp)
        }

        Spacer(modifier = Modifier.height(16.dp))

        // Título
        Box(
            modifier = Modifier
                .fillMaxWidth()
                .padding(horizontal = 16.dp)
                .background(azulOscuro, RoundedCornerShape(6.dp))
                .padding(12.dp),
            contentAlignment = Alignment.CenterStart
        ) {
            Text("Nombre del lugar", color = crema, fontWeight = FontWeight.Bold)
        }

        Spacer(modifier = Modifier.height(8.dp))

        // Ubicación
        Row(
            modifier = Modifier.padding(horizontal = 16.dp),
            verticalAlignment = Alignment.CenterVertically
        ) {
            Text("📍", fontSize = 16.sp)
            Spacer(modifier = Modifier.width(4.dp))
            Box(
                modifier = Modifier
                    .background(verdeSuave, RoundedCornerShape(6.dp))
                    .padding(horizontal = 20.dp, vertical = 6.dp)
            ) {
                Text("Ubicación de la ruta", color = azulOscuro, fontSize = 14.sp)
            }
        }
        // ... (resto de la implementacion de detalle de ruta)
    }
}

/**
 * Pantalla de Meme Local (Ejemplo).
 */
@Composable
@Preview(showBackground = true)
fun MemeLocalScreen() {
    Scaffold(
        topBar = { TopBarMemeLocal() },
        containerColor = Color(0xFFD2D0A6)
    ) { padding ->
        Column(
            modifier = Modifier
                .padding(padding)
                .fillMaxSize()
                .verticalScroll(rememberScrollState())
        ) {
            // Sección del meme o imagen
            Box(
                modifier = Modifier
                    .fillMaxWidth()
                    .height(250.dp)
                    .background(Color.White),
                contentAlignment = Alignment.Center
            ) {
                Column(horizontalAlignment = Alignment.CenterHorizontally) {
                    Text("Meme / Imagen", color = Color.Gray)
                    Text("😂", fontSize = 50.sp)
                }
            }

            // Sección inferior con información
            Column(
                modifier = Modifier
                    .fillMaxWidth()
                    .background(Color(0xFFF3EBD2))
                    .padding(16.dp)
            ) {
                // Autor
                Row(verticalAlignment = Alignment.CenterVertically) {
                    Box(
                        modifier = Modifier
                            .size(40.dp)
                            .clip(CircleShape)
                            .background(Color(0xFFE8A38B))
                    )
                    Spacer(modifier = Modifier.width(10.dp))
                    Column {
                        Text("Nombre de usuario", fontWeight = FontWeight.Bold)
                        Text("📍 Ciudad o ubicación", fontSize = 12.sp, color = Color.Gray)
                    }
                    Spacer(modifier = Modifier.weight(1f))
                    Text("2h", color = Color.Gray, fontSize = 12.sp)
                }
                // ... (resto de la implementacion de meme local)
            }
        }
    }
}

@Composable
fun TopBarMemeLocal() {
    Row(
        modifier = Modifier
            .fillMaxWidth()
            .background(Color.White)
            .padding(16.dp),
        verticalAlignment = Alignment.CenterVertically
    ) {
        Text("←", fontSize = 22.sp)
        Spacer(modifier = Modifier.width(8.dp))
        Text("Meme Local", fontWeight = FontWeight.Bold, fontSize = 18.sp)
    }
}

/**
 * Pantalla de Perfil de Usuario.
 * Permite ver y editar la informacion del perfil y ver las publicaciones del usuario.
 */
@Composable
fun PerfilUsuarioScreen(
    navController: NavController,
    perfilViewModel: PerfilViewModel = androidx.lifecycle.viewmodel.compose.viewModel()
) {
    // Obtenemos username, email y bio desde el ViewModel
    val username by perfilViewModel.username.collectAsState()
    val email by perfilViewModel.email.collectAsState()
    val bio by perfilViewModel.bio.collectAsState()

    // Estado local para el TextField editable
    var bioText by remember { mutableStateOf("") }

    // Sincronizamos bioText con el StateFlow cada vez que cambia
    LaunchedEffect(bio) {
        bioText = bio
    }

    Scaffold(
        topBar = { TopBarPerfil(onNavigateBack = { navController.popBackStack() }) },
        containerColor = Color(0xFFD2D0A6)
    ) { padding ->

        Column(
            modifier = Modifier
                .fillMaxSize()
                .padding(padding)
                .background(Color(0xFFD2D0A6))
        ) {

            // -------- CAJA PRINCIPAL DEL PERFIL ----------
            Box(
                modifier = Modifier
                    .fillMaxWidth()
                    .background(Color.White)
                    .padding(16.dp)
            ) {
                Column(horizontalAlignment = Alignment.CenterHorizontally) {

                    // FOTO - Selector de imagen
                    val context = LocalContext.current
                    val launcher = rememberLauncherForActivityResult(
                        contract = ActivityResultContracts.GetContent()
                    ) { uri: Uri? ->
                        uri?.let {
                            perfilViewModel.updateProfilePicture(it, context)
                        }
                    }
                    
                    val profilePic = perfilViewModel.profilePicture.collectAsState()
                    
                    Box(
                        modifier = Modifier
                            .size(80.dp)
                            .clip(CircleShape)
                            .background(Color(0xFFE8A38B))
                            .clickable { launcher.launch("image/*") },
                        contentAlignment = Alignment.Center
                    ) {
                        if (profilePic.value.isNotEmpty() && profilePic.value.startsWith("data:image")) {
                            val base64String = profilePic.value.substringAfter("base64,")
                            val imageBytes = android.util.Base64.decode(base64String, android.util.Base64.DEFAULT)
                            val bitmap = android.graphics.BitmapFactory.decodeByteArray(imageBytes, 0, imageBytes.size)
                            
                            if (bitmap != null) {
                                Image(
                                    painter = androidx.compose.ui.graphics.painter.BitmapPainter(bitmap.asImageBitmap()),
                                    contentDescription = "Foto de perfil",
                                    modifier = Modifier.fillMaxSize(),
                                    contentScale = androidx.compose.ui.layout.ContentScale.Crop
                                )
                            } else {
                                Text("👤", fontSize = 32.sp)
                            }
                        } else {
                            Text("👤", fontSize = 32.sp)
                        }
                    }

                    Spacer(modifier = Modifier.height(8.dp))

                    // Nombre real / Loading
                    if (username == "Cargando...") {
                        CircularProgressIndicator()
                    } else {
                        Text(
                            text = username,
                            fontWeight = FontWeight.Bold,
                            fontSize = 18.sp
                        )

                        // Email debajo del nombre
                        if (email.isNotBlank()) {
                            Text(
                                text = email,
                                color = Color.Gray,
                                fontSize = 13.sp
                            )
                        }

                        Spacer(modifier = Modifier.height(8.dp))

                        // Campo editable de la descripción/bio
                        OutlinedTextField(
                            value = bioText,
                            onValueChange = { bioText = it },
                            label = { Text("Descripción") },
                            singleLine = false,
                            modifier = Modifier
                                .fillMaxWidth()
                                .height(80.dp)
                        )

                        Spacer(modifier = Modifier.height(8.dp))

                        // Botón para guardar la descripción
                        Button(
                            onClick = { perfilViewModel.updateBio(bioText) },
                            colors = ButtonDefaults.buttonColors(
                                containerColor = Color(0xFFC8C8A9),
                                contentColor = Color.White
                            ),
                            modifier = Modifier.align(Alignment.CenterHorizontally)
                        ) {
                            Text("Guardar descripción")
                        }

                        Spacer(modifier = Modifier.height(16.dp))
                        
                        // Botón cerrar sesión
                        Button(
                            onClick = {
                                com.google.firebase.auth.FirebaseAuth.getInstance().signOut()
                                navController.navigate(Screen.Login.route) {
                                    popUpTo(0) { inclusive = true }
                                }
                            },
                            modifier = Modifier.fillMaxWidth(),
                            colors = ButtonDefaults.buttonColors(
                                containerColor = Color.Red
                            )
                        ) {
                            Text("🚪 Cerrar sesión", color = Color.White)
                        }

                        Spacer(modifier = Modifier.height(16.dp))
                    }
                }
            }

            // -------- PUBLICACIONES DEL USUARIO --------
            Column(
                modifier = Modifier
                    .fillMaxWidth()
                    .background(Color(0xFFF3EBD2))
                    .padding(16.dp)
            ) {
                Text("Mis Publicaciones", fontWeight = FontWeight.Bold, fontSize = 16.sp)
                Spacer(modifier = Modifier.height(12.dp))

                var userPosts by remember { mutableStateOf<List<mx.edu.utng.avht.unidad2.data.ContentModel>>(emptyList()) }
                val contentViewModel: mx.edu.utng.avht.unidad2.viewmodel.ContentViewModel = androidx.lifecycle.viewmodel.compose.viewModel()
                val auth = com.google.firebase.auth.FirebaseAuth.getInstance()
                val currentUserId = auth.currentUser?.uid ?: ""

                DisposableEffect(currentUserId) {
                    if (currentUserId.isNotEmpty()) {
                        contentViewModel.fetchUserPosts(currentUserId) { posts ->
                            userPosts = posts
                        }
                    }
                    onDispose { }
                }

                if (userPosts.isEmpty()) {
                    Box(
                        modifier = Modifier
                            .fillMaxWidth()
                            .height(150.dp),
                        contentAlignment = Alignment.Center
                    ) {
                        Text("No tienes publicaciones aún", color = Color.Gray)
                    }
                } else {
                    var selectedPost by remember { mutableStateOf<mx.edu.utng.avht.unidad2.data.ContentModel?>(null) }
                    
                    LazyVerticalGrid(
                        columns = GridCells.Fixed(3),
                        modifier = Modifier
                            .fillMaxHeight()
                            .padding(top = 4.dp),
                        verticalArrangement = Arrangement.spacedBy(8.dp),
                        horizontalArrangement = Arrangement.spacedBy(8.dp)
                    ) {
                        items(userPosts) { post ->
                            // ... (logica de renderizado de items de post)
                            Box(
                                modifier = Modifier
                                    .aspectRatio(1f)
                                    .clip(RoundedCornerShape(10.dp))
                                    .background(Color(0xFFE8A38B))
                                    .clickable { selectedPost = post },
                                contentAlignment = Alignment.Center
                            ) {
                                // ... (imagen del post)
                                Text("📷", fontSize = 28.sp)
                            }
                        }
                    }
                    
                    // Dialog para mostrar publicación completa
                    selectedPost?.let { post ->
                        // ... (Dialogo de detalle de post)
                    }
                }
            }
        }
    }
}

@OptIn(ExperimentalMaterial3Api::class)
@Composable
fun TopBarPerfil(onNavigateBack: () -> Unit) {
    TopAppBar(
        title = { Text("Perfil") },
        navigationIcon = {
            IconButton(onClick = onNavigateBack) {
                Icon(
                    imageVector = Icons.Filled.ArrowBack,
                    contentDescription = "Atrás"
                )
            }
        },
        colors = TopAppBarDefaults.topAppBarColors(
            containerColor = Color(0xFFD2D0A6),
            titleContentColor = Color.Black,
            navigationIconContentColor = Color.Black,
            actionIconContentColor = Color.Black
        )
    )
}

/**
 * Pantalla de Feed de Comunidad.
 * Muestra las publicaciones de todos los usuarios.
 */
@Composable
fun FeedComunidadScreen(
    onNavigateBack: () -> Unit,
    navController: NavController,
    viewModel: mx.edu.utng.avht.unidad2.viewmodel.ContentViewModel = androidx.lifecycle.viewmodel.compose.viewModel()
) {
    val posts by viewModel.posts.collectAsState()

    Scaffold(
        topBar = { TopBarFeedComunidad(onNavigateBack = onNavigateBack) },
        containerColor = Color(0xFFD2D0A6)
    ) { padding ->
        Column(
            modifier = Modifier
                .fillMaxSize()
                .padding(padding)
                .background(Color(0xFFD2D0A6))
        ) {
            TabsFeed()

            LazyColumn(
                modifier = Modifier
                    .fillMaxSize()
                    .background(Color(0xFFF3EBD2))
            ) {
                items(posts) { post ->
                    FeedPostItem(
                        post = post,
                        viewModel = viewModel,
                        onLikeClick = { viewModel.toggleLike(post) },
                        onCommentSend = { text -> viewModel.addComment(post.id, text) },
                        onUserClick = { userId ->
                            navController.navigate("user_profile/$userId")
                        }
                    )
                    Spacer(modifier = Modifier.height(8.dp))
                }
            }
        }
    }
}

// ... (Resto de componentes auxiliares como FeedPostItem, TopBarFeedComunidad, etc.)
```

### 5. `Components.kt`

```kotlin
package mx.edu.utng.avht.unidad2

import androidx.compose.foundation.background
import androidx.compose.foundation.layout.*
import androidx.compose.foundation.shape.RoundedCornerShape
import androidx.compose.material3.*
import androidx.compose.runtime.Composable
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.draw.clip
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp

// Definicion de colores globales para la aplicacion
val salmon = Color(0xFFE4A691)
val crema = Color(0xFFF7EFD8)
val azulGris = Color(0xFF556270)
val azulOscuro = Color(0xFF273142)

/**
 * Barra superior personalizada.
 * Incluye un campo de busqueda simulado.
 */
@Composable
fun TopBar() {
    Row(
        modifier = Modifier
            .fillMaxWidth()
            .padding(horizontal = 16.dp, vertical = 8.dp)
            .clip(RoundedCornerShape(30.dp))
            .background(Color.White),
        verticalAlignment = Alignment.CenterVertically
    ) {
        // Ícono de búsqueda
        Text("🔍", modifier = Modifier.padding(start = 16.dp), fontSize = 18.sp, color = azulGris)
        Text(
            "Buscar lugar o meme...",
            modifier = Modifier.padding(start = 8.dp, top = 16.dp, bottom = 16.dp),
            color = Color.Gray
        )
        Spacer(modifier = Modifier.weight(1f))
    }
}

/**
 * Barra de navegacion inferior.
 * Permite navegar entre Mapa, Comunidad y Perfil.
 */
@Composable
fun BottomNav(
    onNavigateToPerfil: () -> Unit = {},
    onNavigateToComunidad: () -> Unit = {}
) {
    NavigationBar(containerColor = Color.White) {

        // Item de Mapa
        NavigationBarItem(
            selected = true,
            onClick = {},
            icon = { Text("📍") },
            label = { Text("Mapa") }
        )

        // Item de Comunidad
        NavigationBarItem(
            selected = false,
            onClick = { onNavigateToComunidad() },
            icon = { Text("👥") },
            label = { Text("Comunidad") }
        )

        // Item de Perfil
        NavigationBarItem(
            selected = false,
            onClick = { onNavigateToPerfil() },
            icon = { Text("🏠") },
            label = { Text("Perfil") }
        )
    }
}
```
