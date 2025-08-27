
    <!-- Font Awesome para iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* --- Variables de Diseño (Paleta de Colores) --- */
        :root {
            --primary-color: #0d47a1; /* Azul oscuro principal */
            --secondary-color: #1976d2; /* Azul más claro para acentos */
            --background-color: #f5f7fa; /* Fondo gris muy claro */
            --text-color: #333; /* Color de texto principal */
            --card-bg-color: #ffffff; /* Fondo de las tarjetas */
            --header-bg-color: #0d47a1; /* Fondo del encabezado */
            --shadow-color: rgba(0, 0, 0, 0.1);
        }

        /* --- Estilos Generales y Tipografía --- */
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.7;
            background-color: var(--background-color);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            overflow-x: hidden; /* Evita el desbordamiento horizontal */
        }

        /* --- Encabezado Principal --- */
        header {
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 4rem 1.5rem;
            text-align: center;
            border-bottom-left-radius: 50% 20%;
            border-bottom-right-radius: 50% 20%;
        }

        header h1 {
            margin: 0;
            font-size: 3rem;
            font-weight: 700;
        }

        header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        /* --- Contenedor Principal --- */
        main {
            max-width: 1100px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        /* --- Estilo de las Secciones --- */
        section {
            background-color: var(--card-bg-color);
            margin-bottom: 2.5rem;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: 0 8px 25px var(--shadow-color);
            border-left: 6px solid var(--primary-color);
        }

        section h2 {
            color: var(--primary-color);
            border-bottom: 2px solid #e0e0e0;
            padding-bottom: 0.8rem;
            margin-top: 0;
            font-size: 1.8rem;
            display: flex;
            align-items: center;
        }

        h2 .fas {
            margin-right: 15px;
            font-size: 1.5rem;
        }

        /* --- Estilo de Listas --- */
        ul {
            list-style-type: none;
            padding-left: 0;
        }

        ul li {
            position: relative;
            padding-left: 35px;
            margin-bottom: 1rem;
        }
        
        .card ul li::before {
             content: '\f138'; /* Icono de flecha de Font Awesome */
             font-family: 'Font Awesome 6 Free';
             font-weight: 900;
             position: absolute;
             left: 0;
             top: 4px;
             color: var(--secondary-color);
             font-size: 1.1rem;
        }
        
        #formacion ul li::before {
            content: '\f00c'; /* Icono de check de Font Awesome */
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            position: absolute;
            left: 0;
            top: 4px;
            color: var(--secondary-color);
            font-size: 1.1rem;
        }


        /* --- Grid para las Competencias --- */
        .competencia-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .card {
            background-color: #fdfdfd;
            padding: 2rem;
            border-radius: 10px;
            border: 1px solid #eee;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.12);
        }

        .card h3 {
            color: var(--secondary-color);
            margin-top: 0;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }
        
        .card h3 .fas {
            margin-right: 10px;
        }

        /* --- Pie de Página --- */
        footer {
            background-color: #263238; /* Gris oscuro azulado */
            color: white;
            text-align: center;
            padding: 3rem 1.5rem;
            margin-top: 3rem;
        }

        footer h3 {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .contacto-info {
            display: flex;
            justify-content: center;
            gap: 2.5rem;
            flex-wrap: wrap;
        }

        .contacto-info a {
            color: white;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            font-size: 1.1rem;
            transition: color 0.3s ease;
        }
        
        .contacto-info a:hover {
            color: #90caf9; /* Azul claro para hover */
        }

        .contacto-info .fas {
            margin-right: 10px;
            font-size: 1.3rem;
        }

        /* --- Animación Progresiva --- */
        .hidden {
            opacity: 0;
            filter: blur(5px);
            transform: translateX(-50px);
            transition: all 0.7s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .show {
            opacity: 1;
            filter: blur(0);
            transform: translateX(0);
        }
        
        /* --- Diseño Responsivo --- */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2.2rem;
            }
            section {
                padding: 1.5rem;
            }
            .competencia-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>JONATAN GUERRERO</h1>
        <p>Perfil Polivalente en Automatización, Electrónica y Tecnologías de la Información</p>
    </header>

    <main>
        <section id="perfil" class="hidden">
            <h2><i class="fas fa-user-tie"></i> Perfil Profesional</h2>
            <p>
                Profesional técnico superior con un perfil polivalente, caracterizado por una notable capacidad para el diagnóstico y la resolución de problemas de alta complejidad. La especialización se centra en la convergencia estratégica de la <strong>automatización industrial, la electrónica de precisión y las tecnologías de la información (IT)</strong>.
            </p>
            <p>
                Poseo una sólida base formativa, complementada con una experiencia práctica demostrable en el ciclo de vida completo de proyectos tecnológicos, abarcando desde el diseño conceptual y la implementación hasta el mantenimiento y la optimización de sistemas integrados. La trayectoria profesional engloba la programación a bajo nivel de PLCs y robots, la administración de infraestructuras IT virtualizadas, el desarrollo de hardware a medida para aplicaciones IoT y la implementación de sistemas avanzados de seguridad física y lógica.
            </p>
            <p>
                Paralelamente, gestiono un taller propio que funciona como un laboratorio personal para la investigación y el desarrollo autodidacta, lo que me permite estar en un proceso de aprendizaje y mejora continua.
            </p>
        </section>

        <section id="formacion" class="hidden">
            <h2><i class="fas fa-graduation-cap"></i> Formación Académica</h2>
            <ul>
                <li>Técnico Superior en Automatización y Robótica Industrial</li>
                <li>Técnico en Equipos Electrónicos de Consumo</li>
            </ul>
        </section>

        <section id="competencias" class="hidden">
            <h2><i class="fas fa-cogs"></i> Competencias Técnicas</h2>

            <div class="competencia-grid">
                <article class="card hidden">
                    <h3><i class="fas fa-robot"></i> Automatización y Robótica</h3>
                    <ul>
                        <li><strong>Autómatas Programables (PLCs):</strong> Dominio de la programación avanzada de PLCs <strong>Siemens (S7-1200/1500)</strong> mediante <strong>TIA Portal</strong>. Competencia en lógica de control, HMI y puesta en servicio.</li>
                        <li><strong>Robótica Industrial:</strong> Experiencia en programación y optimización de <strong>robots ABB</strong> con controladores IRC5, incluyendo aplicaciones de manipulación (pick and place).</li>
                        <li><strong>Sistemas de Visión Artificial:</strong> Implementación y calibración para control de calidad, detección de defectos y guiado de robots.</li>
                        <li><strong>Comunicaciones Industriales:</strong> Configuración y diagnóstico de redes <strong>Profinet, Profibus y Modbus (TCP/RTU)</strong> para garantizar la integridad de datos.</li>
                    </ul>
                </article>

                <article class="card hidden">
                    <h3><i class="fas fa-microchip"></i> Electrónica</h3>
                    <ul>
                        <li><strong>Diseño y Desarrollo de Hardware:</strong> Gestión del ciclo completo de diseño de PCBs para pasarelas de comunicación y dispositivos <strong>IoT</strong> de bajo consumo.</li>
                        <li><strong>Software de Diseño (ECAD):</strong> Dominio avanzado de <strong>KiCad</strong> y conocimientos de <strong>Proteus</strong> para diseño de esquemas y enrutado de PCBs.</li>
                        <li><strong>Microcontroladores:</strong> Programación de <strong>Arduino, ESP32 (con FreeRTOS) y Raspberry Pi</strong> para sistemas embebidos y prototipado rápido.</li>
                        <li><strong>Soldadura y Reparación:</strong> Especialización en técnicas de soldadura de alta precisión y micro-soldadura (<strong>SMD</strong> y <strong>THT</strong>) para reparación a nivel de componente.</li>
                        <li><strong>Sistemas IoT y Domótica:</strong> Desarrollo e integración de soluciones IoT con protocolos como MQTT y HTTP/REST, centralizadas en plataformas como <strong>Home Assistant</strong>.</li>
                    </ul>
                </article>

                <article class="card hidden">
                    <h3><i class="fas fa-server"></i> Tecnologías de la Información (IT)</h3>
                    <ul>
                        <li><strong>Sistemas y Virtualización:</strong> Administración de <strong>Windows Server, Linux (Debian, Ubuntu)</strong> y entornos de virtualización con <strong>Proxmox, Hyper-V y VMware ESXi</strong>.</li>
                        <li><strong>Redes y Comunicaciones:</strong> Diseño, instalación y mantenimiento de infraestructuras de red, incluyendo cableado estructurado, Wi-Fi y administración de dominios web.</li>
                        <li><strong>Sistemas de Seguridad y Videovigilancia:</strong> Instalación y mantenimiento de sistemas <strong>CCTV (analógico e IP)</strong>, NVRs y control de accesos. Participación en el diseño de un centro de analítica de vídeo por IA.</li>
                        <li><strong>Desarrollo y Software:</strong> Competencia en <strong>C++</strong> y <strong>Java</strong>. Experiencia en desarrollo web con <strong>WordPress</strong> y gestión de bases de datos <strong>SQL</strong>.</li>
                        <li><strong>Administración de Sistemas:</strong> Gestión de directivas de grupo (<strong>GPO</strong>) en <strong>Microsoft Active Directory</strong> y ensamblaje de equipos a medida.</li>
                    </ul>
                </article>

                <article class="card hidden">
                    <h3><i class="fas fa-bolt"></i> Electricidad y Mantenimiento</h3>
                    <ul>
                        <li><strong>Instalaciones Eléctricas:</strong> Diseño de instalaciones de baja tensión (REBT), mantenimiento de cuadros eléctricos y diagnóstico de incidencias.</li>
                        <li><strong>Diseño Eléctrico (EPLAN):</strong> Elaboración de esquemas eléctricos y documentación técnica completa para proyectos de automatización utilizando <strong>EPLAN Electric P8</strong>.</li>
                        <li><strong>Mantenimiento Integral de Infraestructuras:</strong> Gestión de grupos electrógenos, SAI, centros de transformación, calderas industriales, climatización (HVAC) y sistemas de protección contra incendios (PCI).</li>
                    </ul>
                </article>
            </div>
        </section>

        <section id="otros" class="hidden">
            <h2><i class="fas fa-music"></i> Otros Conocimientos</h2>
            <p>
                Conocimientos en técnicas de <strong>producción musical</strong>, que incluyen grabación, mezcla y masterización de audio. Manejo de software de edición de audio (DAW) en entornos de estudio a nivel no profesional.
            </p>
        </section>
    </main>

    <footer id="contacto">
        <h3>Información de Contacto</h3>
        <div class="contacto-info">
            <a href="mailto:jonipirati@gmail.com"><i class="fas fa-envelope"></i> jonipirati@gmail.com</a>
            <a href="tel:695246140"><i class="fas fa-phone"></i> 695 246 140</a>
            <span><i class="fas fa-map-marker-alt"></i> León, 24009</span>
        </div>
    </footer>

    <script>
        // --- Lógica para la Animación Progresiva ---
        document.addEventListener("DOMContentLoaded", () => {
            // Selecciona todos los elementos que queremos animar
            const hiddenElements = document.querySelectorAll('.hidden');

            // Configura el observador de intersección
            const observer = new IntersectionObserver((entries) => {
                entries.forEach((entry, index) => {
                    if (entry.isIntersecting) {
                        // Añade un pequeño retraso a cada elemento para un efecto escalonado
                        setTimeout(() => {
                            entry.target.classList.add('show');
                        }, index * 100); // 100ms de retraso entre elementos
                        
                        // Una vez que el elemento es visible, dejamos de observarlo para mejorar el rendimiento
                        observer.unobserve(entry.target);
                    }
                });
            }, {
                threshold: 0.1 // El elemento se activa cuando el 10% es visible
            });

            // Pone a cada elemento bajo observación
            hiddenElements.forEach(el => observer.observe(el));
        });
    </script>
</body>
</html>
