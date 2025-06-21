<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navas Inmobiliaria - La oportunidad de inversión perfecta</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #667eea;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        main {
            margin-top: 80px;
        }

        .hero {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 4rem 0;
            text-align: center;
            color: white;
            margin: 2rem 0;
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0,0,0,0.1);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #ff6b6b, #ee5a24);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 4rem 0;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 32px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
        }

        .contact {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 3rem;
            border-radius: 20px;
            margin: 2rem 0;
            text-align: center;
        }

        .contact h2 {
            color: #667eea;
            margin-bottom: 2rem;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: #667eea;
        }

        .faq {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 3rem;
            border-radius: 20px;
            margin: 2rem 0;
        }

        .faq h2 {
            color: #667eea;
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2.2rem;
        }

        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            margin-bottom: 1rem;
            border: 1px solid #e0e0e0;
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .faq-item:hover {
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .faq-question {
            background: #f8f9fa;
            padding: 1.5rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: background 0.3s ease;
        }

        .faq-question:hover {
            background: #e9ecef;
        }

        .faq-question h3 {
            margin: 0;
            color: #333;
            font-size: 1.1rem;
        }

        .faq-toggle {
            font-size: 1.5rem;
            font-weight: bold;
            color: #667eea;
            transition: transform 0.3s ease;
        }

        .faq-answer {
            padding: 0 1.5rem;
            max-height: 0;
            overflow: hidden;
            transition: all 0.3s ease;
            background: white;
        }

        .faq-item.active .faq-answer {
            padding: 1.5rem;
            max-height: 200px;
        }

        .faq-item.active .faq-toggle {
            transform: rotate(45deg);
        }

        footer {
            background: rgba(0, 0, 0, 0.8);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .services {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <a href="#" class="logo">🏠 Navas Inmobiliaria</a>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li><a href="#preguntas">Preguntas</a></li>
            </ul>
        </nav>
    </header>

    <main class="container">
        <section id="inicio" class="hero">
            <h1>Oportunidades de Inversión en Tacna</h1>
            <p>Invierte en lotes con alta rentabilidad y plusvalía asegurada. Más de 3 años respaldando 6 inversiones exitosas</p>
            <a href="#contacto" class="cta-button">Ver Oportunidades</a>
        </section>

        <section id="servicios" class="services">
            <div class="service-card">
                <div class="service-icon">📈</div>
                <h3>Venta de Lotes</h3>
                <p>Lotes con alta plusvalía en zonas de crecimiento estratégico. Inversión segura y rentable a largo plazo.</p>
            </div>
            
            <div class="service-card">
                <div class="service-icon">🤝</div>
                <h3>Corretaje</h3>
                <p>Intermediación profesional especializada en inversiones inmobiliarias con análisis de rentabilidad incluido.</p>
            </div>
            
            <div class="service-card">
                <div class="service-icon">⚖️</div>
                <h3>Asesoría Legal</h3>
                <p>Protege tu inversión: Titulo matriz, inscripción en registros públicos, contratos blindados y trámites registrales sin complicaciones.</p>
            </div>
            
            <div class="service-card">
                <div class="service-icon">💰</div>
                <h3>Formas de Pago</h3>
                <p>Facilidades de pago que maximizan tu flujo de caja: desde separación mínima hasta financiamiento directo.</p>
            </div>
            
            <div class="service-card">
                <div class="service-icon">🔌</div>
                <h3>Servicios Básicos</h3>
                <p>Lotes con diferentes ubicacioens estrategicas listos para generar valor inmediato.</p>
            </div>
            
            <div class="service-card">
                <div class="service-icon">💡</div>
                <h3>Asesoría de Inversión</h3>
                <p>Te orientamos sobre las mejores oportunidades, proyecciones de crecimiento y estrategias de inversión.</p>
            </div>
        </section>

        <section id="contacto" class="contact">
            <h2>¿Listo para hacer tu mejor inversión?</h2>
            <p>Contáctanos hoy mismo y descubre las mejores oportunidades de inversión en lotes de Tacna</p>
            
            <div style="margin: 2rem 0;">
                <a href="https://wa.me/51983624649?text=Hola,%20estoy%20interesado%20en%20oportunidades%20de%20inversión%20en%20lotes" 
                   class="cta-button" target="_blank" style="margin-right: 1rem;">
                   💬 WhatsApp
                </a>
                <a href="tel:+51983624649" class="cta-button" style="background: linear-gradient(45deg, #667eea, #764ba2);">
                   📞 Llamar Ahora
                </a>
            </div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i>📱</i>
                    <div>
                        <strong>Celular</strong><br>
                        +51 983 624 649
                    </div>
                </div>
                
                <div class="contact-item">
                    <i>📧</i>
                    <div>
                        <strong>Email</strong><br>
                        navasinmobiliaria6@gmail.com
                    </div>
                </div>
                
                <div class="contact-item">
                    <i>📍</i>
                    <div>
                        <strong>Oficinas</strong><br>
                        Calle Zela 873, Tacna<br>
                        Calle Modesto Basadre 895, Tacna
                    </div>
                </div>
                
                <div class="contact-item">
                    <i>🕒</i>
                    <div>
                        <strong>Horarios</strong><br>
                        Lun - Vie: 9:00 AM - 1:00 PM / 3:00 PM - 7:00 PM<br>
                        Sábados: 8:00 AM - 1:00 PM
                    </div>
                </div>
            </div>
        </section>

        <section id="preguntas" class="faq">
            <h2>Preguntas Frecuentes</h2>
            
            <div class="faq-container">
                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Qué documentos necesito para invertir en un lote?</h3>
                        <span class="faq-toggle">+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Necesitas: DNI, voucher de pago inicial y carta de compromiso firmados. Te asesoramos en todo el proceso de inversión.</p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Cuál es la rentabilidad esperada de la inversión?</h3>
                        <span class="faq-toggle">+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Nuestros lotes han mostrado una plusvalía promedio del 15-25% anual. Te proporcionamos análisis detallado de cada oportunidad.</p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Los lotes tienen todos los servicios básicos?</h3>
                        <span class="faq-toggle">+</span>
                    </div> La zona de la Yarada los Palos, especificamente el kilometro 11 y 12 es una zona rural, esto implica que los servicios basicos se ven destinados a adaptaciones, por ejemplo para el tema de luz utilizan paneles solares, cuya destinacion varia por el tipo de uso, asi mismo por la zona es comun comprar agua potable como tambien agua no potable o para riego o construcción, es por ello que tambien implementan biodigestores para la sustutución del desague.
                    <div class="faq-answer">
                        <p>La zona de desarrollo.</p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Puedo revender el lote fácilmente?</h3>
                        <span class="faq-toggle">+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Absolutamente. Los lotes están en zonas de alta demanda y crecimiento, lo que facilita su posterior comercialización.</p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Ofrecen garantías en la inversión?</h3>
                        <span class="faq-toggle">+</span>
                    </div>
                    <div class="faq-answer">
                        <p>Garantizamos saneamiento físico y legal completo, títulos de propiedad matriz registrados y asesoría post-venta por 1 año.</p>
                    </div>
                </div>

                <div class="faq-item">
                    <div class="faq-question">
                        <h3>¿Puedo visitar los lotes antes de invertir?</h3>
                        <span class="faq-toggle">+</span>
                    </div>
                    <div class="faq-answer">
                        <p>¡Por supuesto! Organizamos visitas guiadas gratuitas y te mostramos el potencial de crecimiento de cada zona, completamente gratis.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Navas Inmobiliaria. Todos los derechos reservados.</p>
            <p>Tu confianza, nuestro compromiso</p>
        </div>
    </footer>

    <script>
        // Funcionalidad para las preguntas frecuentes
        document.addEventListener('DOMContentLoaded', function() {
            const faqQuestions = document.querySelectorAll('.faq-question');
            
            faqQuestions.forEach(question => {
                question.addEventListener('click', function() {
                    const faqItem = this.parentElement;
                    const isActive = faqItem.classList.contains('active');
                    
                    // Cerrar todas las preguntas
                    document.querySelectorAll('.faq-item').forEach(item => {
                        item.classList.remove('active');
                    });
                    
                    // Si no estaba activa, abrirla
                    if (!isActive) {
                        faqItem.classList.add('active');
                    }
                });
            });
        });

        // Scroll suave para los enlaces de navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
