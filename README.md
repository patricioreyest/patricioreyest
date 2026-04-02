<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Portafolio Personal | Desarrollador Full Stack</title>
    <!-- Estilos modernos y limpios -->
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f5f7fc 0%, #eef2f8 100%);
            font-family: 'Segoe UI', 'Poppins', system-ui, -apple-system, 'Inter', 'Helvetica Neue', sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 2rem 1.5rem;
        }

        /* Tarjeta principal con sombra sutil y bordes redondeados */
        .card {
            max-width: 1000px;
            width: 100%;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(0px);
            border-radius: 48px;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.2), 0 2px 8px rgba(0, 0, 0, 0.02);
            overflow: hidden;
            transition: all 0.2s ease;
            border: 1px solid rgba(255, 255, 255, 0.6);
        }

        /* Contenedor superior: nombre centrado con estilo elegante */
        .hero-name {
            text-align: center;
            padding: 2rem 1.5rem 1rem 1.5rem;
            background: rgba(255, 255, 255, 0.5);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        .hero-name h1 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #1A2A3F, #2C3E66, #1E2F45);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            text-shadow: 0 2px 5px rgba(0, 0, 0, 0.02);
            margin-bottom: 0.25rem;
        }

        .hero-name .badge {
            display: inline-block;
            margin-top: 0.5rem;
            background: #e9edf2;
            padding: 0.3rem 1rem;
            border-radius: 60px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #2c3e66;
            letter-spacing: 0.3px;
            backdrop-filter: blur(4px);
        }

        /* Sección del GIF animado - centro visual */
        .gif-section {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 2rem 1.5rem 1.8rem 1.5rem;
            background: #ffffffcc;
        }

        .gif-wrapper {
            max-width: 540px;
            width: 100%;
            border-radius: 32px;
            background: #f8fafd;
            box-shadow: 0 12px 28px -8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .gif-wrapper img {
            display: block;
            width: 100%;
            height: auto;
            object-fit: cover;
            transition: scale 0.3s;
        }

        /* Pequeña descripción personal / área de texto */
        .description {
            padding: 1.2rem 2rem 0.8rem 2rem;
            text-align: center;
            border-top: 1px solid rgba(0, 0, 0, 0.04);
            background: white;
        }

        .description p {
            font-size: 1.05rem;
            color: #2c3e50;
            line-height: 1.5;
            max-width: 600px;
            margin: 0 auto 0.75rem auto;
            font-weight: 450;
        }

        /* SECCIÓN DE ICONOS DE TECNOLOGÍAS (colores originales) */
        .tech-icons-section {
            background: white;
            padding: 1.5rem 1.5rem 1.8rem 1.5rem;
            text-align: center;
            border-top: 1px solid #eef2f8;
        }

        .tech-icons-title {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
            color: #5b6e8c;
            margin-bottom: 1.5rem;
        }

        .icons-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            gap: 1.8rem;
            row-gap: 1.8rem;
        }

        .icon-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
            transition: transform 0.2s ease;
        }

        .icon-item:hover {
            transform: translateY(-5px);
        }

        .icon-item svg {
            width: 48px;
            height: 48px;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.05));
            transition: filter 0.2s;
        }

        .icon-item span {
            font-size: 0.7rem;
            font-weight: 500;
            color: #2c3e50;
            background: #f0f3f9;
            padding: 0.2rem 0.6rem;
            border-radius: 30px;
            letter-spacing: 0.3px;
        }

        /* Versión responsiva: ajustar tamaño y gap */
        @media (max-width: 680px) {
            .icons-grid {
                gap: 1.2rem;
            }
            .icon-item svg {
                width: 38px;
                height: 38px;
            }
            .icon-item span {
                font-size: 0.6rem;
            }
            .hero-name h1 {
                font-size: 2.2rem;
            }
        }

        /* Footer */
        .footer-note {
            text-align: center;
            font-size: 0.8rem;
            padding: 1rem 1rem 1.5rem 1rem;
            background: #f9fbfd;
            color: #5b6e8c;
            border-top: 1px solid #eef2f8;
        }

        .footer-note a {
            color: #2c3e66;
            text-decoration: none;
            font-weight: 500;
            border-bottom: 1px dotted #a0b3ce;
        }

        .footer-note a:hover {
            color: #0f1b2c;
            border-bottom: 1px solid #2c3e66;
        }

        .gif-wrapper:hover {
            transform: scale(1.01);
            box-shadow: 0 20px 30px -12px rgba(0, 0, 0, 0.15);
        }
    </style>
</head>
<body>
    <div class="card">
        <!-- Nombre centrado en la parte superior -->
        <div class="hero-name">
            <h1>✧ Carlos Méndez ✧</h1>
            <div class="badge">⚡ full-stack developer & creative coder ⚡</div>
        </div>

        <!-- Sección del GIF animado de un desarrollador en movimiento -->
        <div class="gif-section">
            <div class="gif-wrapper">
                <!-- 
                    GIF animado representando a un desarrollador trabajando/codeando.
                    Fuente: GIPHY / "programmer coding" - movimiento fluido.
                    Es el gif clásico de un desarrollador con varias pantallas y código.
                -->
                <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" 
                     alt="Desarrollador programando animación GIF | coding in motion"
                     title="✨ Desarrollador en acción ✨"
                     loading="eager">
            </div>
        </div>

        <!-- Pequeña descripción personal -->
        <div class="description">
            <p>💻 <strong>Construyendo experiencias digitales modernas</strong> con pasión por el código limpio y las bases de datos robustas.<br>
            🚀 Especialista en ecosistemas JavaScript, frameworks CSS y backend escalable.</p>
        </div>

        <!-- SECCIÓN DE ÍCONOS DE TECNOLOGÍAS CON COLORES ORIGINALES (JS, Vue, HTML, CSS, Bootstrap, Tailwind, PHP, Laravel, MySQL, PostgreSQL, VSCode, GitHub) -->
        <div class="tech-icons-section">
            <div class="tech-icons-title">✦ mi stack tecnológico ✦</div>
            <div class="icons-grid">
                <!-- JavaScript (icono oficial JS - amarillo) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#F7DF1E">
                        <path d="M0 0h24v24H0V0z" fill="none"/>
                        <path d="M12 14.579v-1.648c.946.742 2.199 1.197 3.518 1.197 1.207 0 2.027-.484 2.027-1.238 0-.684-.486-1.078-2.062-1.484-1.699-.438-3.035-1.086-3.035-2.578 0-1.5 1.236-2.617 3.215-2.617 1.344 0 2.441.457 3.195 1.102l-.678 1.066c-.57-.477-1.383-.848-2.4-.848-1.129 0-1.809.492-1.809 1.164 0 .75.586 1.043 2.028 1.477 1.648.492 3.086 1.215 3.086 2.727 0 1.547-1.266 2.703-3.336 2.703-1.617 0-2.934-.609-3.734-1.406zM6.754 15.93c.964 0 1.648-.426 2.094-1.043l.922.781c-.673.969-1.714 1.477-3.016 1.477-1.957 0-3.386-1.406-3.386-3.563 0-2.109 1.414-3.563 3.324-3.563 1.75 0 2.852 1.137 2.852 2.91 0 .336-.039.668-.117.98H5.398c.094.977.773 1.543 1.98 1.543zm.008-4.09c-.519 0-.973.352-1.086.914h2.086c-.07-.57-.449-.914-.992-.914z"/>
                    </svg>
                    <span>JavaScript</span>
                </div>
                <!-- VueJS (verde característico) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#42B883">
                        <path d="M24 1.61H14.06L12 5.16 9.94 1.61H0l12 20.78ZM12 14.08 5.16 2.23h4.12L12 8.41l2.72-6.18h4.12Z"/>
                    </svg>
                    <span>Vue.js</span>
                </div>
                <!-- HTML5 (naranja/rojo) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#E34F26">
                        <path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.565-2.438L1.5 0zm7.031 9.75l-.232-2.718 10.059.003.23-2.622L5.412 4.41l.698 8.01h9.126l-.326 3.426-2.91.804-2.955-.81-.188-2.11H6.248l.33 4.171L12 19.351l5.379-1.443.743-8.157H8.531z"/>
                    </svg>
                    <span>HTML5</span>
                </div>
                <!-- CSS3 (azul) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#1572B6">
                        <path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.564-2.438L1.5 0zm17.09 4.413L5.41 4.41l.213 2.622 10.125.002-.255 2.716h-6.64l.24 2.573h6.182l-.366 3.523-2.91.804-2.956-.81-.188-2.11h-2.61l.29 3.855L12 19.288l5.373-1.53L18.59 4.414z"/>
                    </svg>
                    <span>CSS3</span>
                </div>
                <!-- Bootstrap (morado oscuro / violeta) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#7952B3">
                        <path d="M11.77 11.24H9.956V8.202h2.152c1.17 0 1.834.522 1.834 1.466 0 .96-.68 1.572-1.964 1.572h-.208zm3.86 1.954c.76-.486 1.174-1.144 1.174-1.996 0-1.484-1.132-2.488-3.008-2.488H7.928v9.044h6.084c2.094 0 3.274-1.026 3.274-2.664 0-1.008-.542-1.896-1.658-2.396zM12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm2.39 16.87H8.688v-3.41h5.51c1.246 0 2.05.664 2.05 1.672 0 1.008-.76 1.738-1.858 1.738zm.154-5.05H8.688V8.462h4.344c1.07 0 1.74.566 1.74 1.53 0 .994-.694 1.528-1.738 1.528z"/>
                    </svg>
                    <span>Bootstrap</span>
                </div>
                <!-- Tailwind CSS (azul turquesa) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#06B6D4">
                        <path d="M12 6C9.333 6 7.667 7.333 7 10c1-1.333 2.167-1.833 3.5-1.5.761.19 1.305.74 1.907 1.348.982.99 2.115 2.134 4.593 2.134 2.667 0 4.333-1.333 5-4-1 1.333-2.167 1.833-3.5 1.5-.761-.19-1.305-.74-1.907-1.348C15.611 7.152 14.478 6 12 6zm-5 6c-2.667 0-4.333 1.333-5 4 1-1.333 2.167-1.833 3.5-1.5.761.19 1.305.74 1.907 1.348.982.99 2.115 2.134 4.593 2.134 2.667 0 4.333-1.333 5-4-1 1.333-2.167 1.833-3.5 1.5-.761-.19-1.305-.74-1.907-1.348C10.611 13.152 9.478 12 7 12z"/>
                    </svg>
                    <span>Tailwind</span>
                </div>
                <!-- PHP (azul oscuro oficial) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#777BB4">
                        <path d="M7.01 10.207h-.944l-.553 2.65h.88c.706 0 1.204-.14 1.494-.42.29-.28.44-.7.44-1.26 0-.54-.14-.92-.43-1.2-.3-.28-.75-.42-1.35-.42h-.55l.013-.35zm-.79 3.896H4.92l.58-2.78H5.8c1.07 0 1.78.21 2.14.63.36.42.54 1 .54 1.74 0 .74-.18 1.28-.54 1.62-.36.34-.88.51-1.56.51h-.58l.02-.72zm4.86-3.896h-.944l-.553 2.65h.88c.706 0 1.204-.14 1.494-.42.29-.28.44-.7.44-1.26 0-.54-.14-.92-.43-1.2-.3-.28-.75-.42-1.35-.42h-.55l.013-.35zm-.79 3.896H9l.58-2.78h.83c1.07 0 1.78.21 2.14.63.36.42.54 1 .54 1.74 0 .74-.18 1.28-.54 1.62-.36.34-.88.51-1.56.51h-.58l.02-.72zm5.63-3.896h-1.17l-.174.84h1.03c.53 0 .9.11 1.11.33.21.22.31.55.31.99 0 .57-.18.99-.54 1.26-.36.27-.87.4-1.53.4h-1.1l.58-2.78h-1.34l-.58 2.78H12.5l.18-.84h1.09c.72 0 1.24-.14 1.56-.42.32-.28.48-.67.48-1.17 0-.44-.1-.77-.3-1-.2-.23-.53-.34-.99-.34h-1.14l-.2.84h1.34l.56-2.78h1.38l-.56 2.78z"/>
                    </svg>
                    <span>PHP</span>
                </div>
                <!-- Laravel (rojo anaranjado) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#FF2D20">
                        <path d="M24 7.055v9.89c0 .54-.287 1.041-.746 1.317l-8.952 5.164c-.47.27-1.045.27-1.514 0L3.745 18.26c-.458-.276-.745-.776-.745-1.317v-9.89c0-.54.287-1.04.746-1.317l8.952-5.164c.47-.27 1.045-.27 1.514 0l8.952 5.164c.459.276.746.776.746 1.317zm-5.324 1.886l-6.676-3.85-6.676 3.85 6.676 3.85 6.676-3.85zm0 3.408l-6.676 3.85-6.676-3.85v3.77l6.676 3.85 6.676-3.85v-3.77zm0 3.408l-6.676 3.85-6.676-3.85v3.77l6.676 3.85 6.676-3.85v-3.77z"/>
                    </svg>
                    <span>Laravel</span>
                </div>
                <!-- MySQL (azul característico) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#4479A1">
                        <path d="M18.178 7.963c-1.094 0-1.94.42-2.52 1.253v-1.05h-1.8v8.82h1.8v-4.64c0-1.173.54-1.81 1.54-1.81.92 0 1.4.58 1.4 1.68v4.77h1.8v-5.17c0-1.68-.88-2.85-2.22-2.85zM5.084 13.623c0 1.74.87 2.84 2.31 2.84 1.03 0 1.76-.45 2.14-1.2l-1.49-.83c-.23.5-.56.74-1.02.74-.67 0-1.07-.51-1.07-1.53v-4.5h-1.8v4.5h.01zm8.32-5.46v-2.2h-1.8v2.2h-1.22v1.48h1.22v4.5c0 1.42.74 2.15 2.1 2.15.74 0 1.32-.24 1.71-.6l-.82-1.24c-.2.15-.46.25-.77.25-.5 0-.83-.31-.83-.92v-4.14h1.72v-1.48h-1.72zM0 11.173v3.99c0 1.5.98 2.52 2.62 2.52 1.28 0 2.19-.57 2.19-1.9 0-.75-.4-1.27-1.1-1.56l1.2-2.1H3.53L2.7 12.16c-.35-.07-.7-.1-1.07-.1h-.56v-2.95H0v2.06zm1.8 3.23c0 .58-.3.86-.84.86-.52 0-.96-.24-.96-.85v-2.1h.96c.54 0 .84.28.84.83v1.26z"/>
                    </svg>
                    <span>MySQL</span>
                </div>
                <!-- PostgreSQL (azul profundo) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#336791">
                        <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm0 2.4c5.302 0 9.6 4.298 9.6 9.6 0 5.302-4.298 9.6-9.6 9.6-5.302 0-9.6-4.298-9.6-9.6 0-5.302 4.298-9.6 9.6-9.6zm-1.2 2.4v3.6h2.4V4.8h-2.4zm0 6v7.2h2.4v-7.2h-2.4z"/>
                    </svg>
                    <span>PostgreSQL</span>
                </div>
                <!-- Visual Studio Code (azul eléctrico) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#007ACC">
                        <path d="M23.15 2.587L18.21.21a1.494 1.494 0 0 0-1.705.29l-9.46 8.63-4.12-3.128a.999.999 0 0 0-1.276.057L.327 6.9c-.436.436-.436 1.143 0 1.58L3.23 12 .327 15.52c-.436.436-.436 1.143 0 1.58l1.322 1.322c.357.357.89.398 1.276.057l4.12-3.128 9.46 8.63c.457.417 1.12.52 1.705.29l4.94-2.377c.555-.267.9-.83.85-1.44V4.027c.05-.61-.295-1.173-.85-1.44zM19.5 17.7L11.73 12 19.5 6.3v11.4z"/>
                    </svg>
                    <span>VS Code</span>
                </div>
                <!-- GitHub (icono oscuro pero moderno gris/negro) -->
                <div class="icon-item">
                    <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="#181717">
                        <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
                    </svg>
                    <span>GitHub</span>
                </div>
            </div>
        </div>

        <!-- Footer con enlace a GitHub -->
        <div class="footer-note">
            🌐 <strong>Mi universo dev</strong> — <a href="#" target="_blank">github.com/carlosdev</a> · siempre aprendiendo<br>
            <span style="font-size:0.75rem;">✨ sitio personal con íconos oficiales de tecnologías ✨</span>
        </div>
    </div>

    <script>
        // pequeño efecto de bienvenida en consola
        console.log("🚀 Sitio web personal con stack tecnológico completo — íconos con colores oficiales");
        // Si deseas cambiar el nombre, simplemente modifica el texto en .hero-name h1
    </script>
</body>
</html>
