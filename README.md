<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GP Consultoria Previdenciária</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #FFD700;
            --primary-dark: #E6B800;
            --dark: #1A1A1A;
            --darker: #0D0D0D;
            --light: #F5F5F5;
            --gray: #444;
            --whatsapp: #25D366;
        }
        
        body {
            background-color: var(--darker);
            color: var(--light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--dark) 0%, #2a2a2a 100%);
            padding: 20px 0;
            border-bottom: 3px solid var(--primary);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--primary);
        }
        
        .logo-text {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.1rem;
        }
        
        nav a:hover {
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--primary);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 800px;
            margin: 0 auto 40px;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(to bottom, var(--primary) 0%, var(--primary-dark) 100%);
            color: black;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2rem;
            transition: all 0.3s;
            margin: 10px;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
        }
        
        .btn-whatsapp {
            background: linear-gradient(to bottom, var(--whatsapp) 0%, #128C7E 100%);
            color: white;
        }
        
        /* Services */
        .services {
            padding: 80px 0;
            background-color: var(--dark);
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: var(--primary);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: linear-gradient(135deg, #2a2a2a 0%, var(--dark) 100%);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            border: 2px solid transparent;
            transition: all 0.3s;
        }
        
        .service-card:hover {
            border-color: var(--primary);
            transform: translateY(-10px);
        }
        
        .service-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* About */
        .about {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .about-image {
            flex: 1;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* WhatsApp Section */
        .whatsapp-section {
            background: linear-gradient(135deg, #128C7E 0%, var(--whatsapp) 100%);
            padding: 80px 0;
            text-align: center;
            color: white;
        }
        
        .whatsapp-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .whatsapp-number {
            font-size: 2rem;
            font-weight: bold;
            background: rgba(0, 0, 0, 0.2);
            display: inline-block;
            padding: 15px 30px;
            border-radius: 50px;
            margin: 20px 0;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 80px 0;
            background-color: var(--dark);
        }
        
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .testimonial-card {
            background: linear-gradient(135deg, #2a2a2a 0%, var(--dark) 100%);
            border-radius: 15px;
            padding: 30px;
            border-left: 5px solid var(--primary);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .author-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: black;
        }
        
        /* Contact */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            font-size: 1.5rem;
            color: var(--primary);
            width: 50px;
            height: 50px;
            background: rgba(255, 215, 0, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        /* Footer */
        footer {
            background-color: var(--darker);
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid var(--gray);
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .social-links {
            display: flex;
            gap: 20px;
        }
        
        .social-links a {
            color: var(--light);
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--primary);
        }
        
        /* WhatsApp Float */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 70px;
            height: 70px;
            background-color: var(--whatsapp);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            z-index: 99;
            animation: pulse 2s infinite;
            text-decoration: none;
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
                box-shadow: 0 5px 15px rgba(37, 211, 102, 0.5);
            }
            50% {
                transform: scale(1.1);
                box-shadow: 0 8px 20px rgba(37, 211, 102, 0.7);
            }
            100% {
                transform: scale(1);
                box-shadow: 0 5px 15px rgba(37, 211, 102, 0.5);
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                flex-direction: column;
                gap: 15px;
                text-align: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .whatsapp-number {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- WhatsApp Float Button -->
    <a href="https://wa.me/5511946199334?text=Olá! Gostaria de mais informações sobre a consultoria previdenciária." class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-scale-balanced"></i>
                    </div>
                    <div class="logo-text">GP Consultoria Previdenciária</div>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Início</a></li>
                        <li><a href="#services">Serviços</a></li>
                        <li><a href="#about">Sobre Nós</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Consultoria Previdenciária Especializada</h1>
            <p>Garanta seus direitos com quem entende do assunto. Atendimento personalizado e focado em resultados.</p>
            <a href="#contact" class="btn">Fale Conosco</a>
            <a href="https://wa.me/5511946199334?text=Olá! Gostaria de mais informações sobre a consultoria previdenciária." class="btn btn-whatsapp" target="_blank">
                <i class="fab fa-whatsapp"></i> WhatsApp
            </a>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Nossos Serviços</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-retirement"></i>
                    </div>
                    <h3>Aposentadorias</h3>
                    <p>Assessoria completa para aposentadoria por idade, tempo de contribuição e especial.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <h3>Auxílio Doença</h3>
                    <p>Orientação para obtenção de benefícios por incapacidade temporária ou permanente.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-baby"></i>
                    </div>
                    <h3>Salário Maternidade</h3>
                    <p>Assessoria para garantia do salário maternidade para mães trabalhadoras.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-wheelchair"></i>
                    </div>
                    <h3>LOAS/ BPC</h3>
                    <p>Suporte para obtenção do Benefício de Prestação Continuada para idosos e pessoas com deficiência.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-invoice-dollar"></i>
                    </div>
                    <h3>Revisões de Benefícios</h3>
                    <p>Análise e revisão de benefícios já concedidos para garantir seus direitos.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-hands-helping"></i>
                    </div>
                    <h3>Consultoria Personalizada</h3>
                    <p>Atendimento individualizado para análise de cada caso específico.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>Sobre a GP Consultoria</h2>
                    <p>Com anos de experiência no direito previdenciário, a GP Consultoria é referência em assessoria para obtenção de benefícios junto ao INSS.</p>
                    <p>Nossa missão é simplificar o complexo sistema previdenciário brasileiro, garantindo que nossos clientes tenham acesso a todos os direitos que lhes são devidos.</p>
                    <p>Contamos com uma equipe especializada e atualizada sobre as constantes mudanças na legislação previdenciária, oferecendo sempre o melhor suporte para cada caso.</p>
                    <a href="https://wa.me/5511946199334?text=Olá! Gostaria de agendar uma consultoria." class="btn" target="_blank">
                        Agendar Consultoria
                    </a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1589829545856-d10d557cf95f?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Equipe da GP Consultoria">
                </div>
            </div>
        </div>
    </section>

    <!-- WhatsApp Section -->
    <section class="whatsapp-section">
        <div class="container">
            <h2>Fale Conosco pelo WhatsApp</h2>
            <p>Atendimento rápido e personalizado diretamente pelo WhatsApp</p>
            <div class="whatsapp-number">
                <i class="fab fa-whatsapp"></i> +55 11 94619-9334
            </div>
            <a href="https://wa.me/5511946199334?text=Olá! Gostaria de mais informações sobre a consultoria previdenciária." class="btn" target="_blank">
                Iniciar Conversa
            </a>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <div class="container">
            <h2 class="section-title">O Que Nossos Clientes Dizem</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"A GP Consultoria me ajudou a conseguir minha aposentadoria após anos tentando sozinha. Profissionais extremamente competentes e atenciosos."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">M</div>
                        <div>
                            <h4>Maria Silva</h4>
                            <p>Aposentada</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Consegui meu auxílio doença em tempo recorde graças ao trabalho eficiente da equipe GP. Recomendo a todos!"</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">J</div>
                        <div>
                            <h4>João Santos</h4>
                            <p>Client</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Consultoria completa e transparente. Me explicaram todo o processo e conseguiram o benefício para minha mãe com agilidade."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">A</div>
                        <div>
                            <h4>Ana Oliveira</h4>
                            <p>Filha de beneficiária</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Entre em Contato</h2>
            <div class="contact-grid">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fab fa-whatsapp"></i>
                        </div>
                        <div>
                            <h3>WhatsApp</h3>
                            <p>+55 11 94619-9334</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>contato@gpconsultoria.com.br</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div>
                            <h3>Horário de Atendimento</h3>
                            <p>Segunda a Sexta: 8h às 18h</p>
                            <p>Sábado: 9h às 13
