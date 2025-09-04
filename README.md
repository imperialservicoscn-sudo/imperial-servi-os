<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imperial Serviços CN - Portfólio Profissional</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.0/font/bootstrap-icons.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --imperial-blue: #0c2d48;
            --imperial-gold: #c89720;
            --imperial-light: #f8f9fa;
            --imperial-dark: #2c3e50;
            --imperial-accent: #145da0;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            color: var(--imperial-dark);
            scroll-behavior: smooth;
            line-height: 1.6;
        }
        
        h1, h2, h3, h4, h5, h6, .nav-link {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
        }
        
        .imperial-bg-primary {
            background-color: var(--imperial-blue);
            color: white;
        }
        
        .imperial-bg-light {
            background-color: var(--imperial-light);
        }
        
        .text-imperial-gold {
            color: var(--imperial-gold);
        }
        
        .btn-imperial {
            background-color: var(--imperial-gold);
            color: var(--imperial-dark);
            font-weight: 600;
            border: none;
            padding: 12px 28px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }
        
        .btn-imperial:hover {
            background-color: #b4830e;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(200, 151, 32, 0.3);
        }
        
        .btn-outline-imperial {
            background-color: transparent;
            color: var(--imperial-blue);
            border: 2px solid var(--imperial-blue);
            font-weight: 600;
            padding: 10px 26px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }
        
        .btn-outline-imperial:hover {
            background-color: var(--imperial-blue);
            color: white;
            transform: translateY(-2px);
        }
        
        .navbar {
            background-color: rgba(12, 45, 72, 0.95);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
            padding: 15px 0;
            transition: all 0.3s ease;
        }
        
        .navbar.navbar-scroll {
            padding: 8px 0;
            background-color: var(--imperial-blue);
        }
        
        .page-section {
            padding: 100px 0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .section-title {
            position: relative;
            margin-bottom: 50px;
            font-weight: 700;
            padding-bottom: 15px;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--imperial-gold);
            margin-top: 15px;
            position: absolute;
            left: 0;
            bottom: 0;
        }
        
        .section-title.text-center:after {
            left: 50%;
            transform: translateX(-50%);
        }
        
        .service-card {
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.4s ease;
            height: 100%;
            border: none;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            background: white;
        }
        
        .service-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .service-icon {
            font-size: 3rem;
            margin-bottom: 25px;
            color: var(--imperial-blue);
            transition: all 0.3s ease;
        }
        
        .service-card:hover .service-icon {
            color: var(--imperial-gold);
            transform: scale(1.1);
        }
        
        .project-card {
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s ease;
            height: 100%;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            position: relative;
        }
        
        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
        }
        
        .project-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(12, 45, 72, 0.9) 0%, transparent 100%);
            opacity: 0;
            transition: all 0.4s ease;
            display: flex;
            align-items: flex-end;
            padding: 30px;
        }
        
        .project-card:hover .project-overlay {
            opacity: 1;
        }
        
        .project-img {
            height: 250px;
            object-fit: cover;
            width: 100%;
        }
        
        .logo {
            font-weight: 800;
            font-size: 1.8rem;
            color: white;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--imperial-gold);
        }
        
        .logo-img {
            height: 40px;
            margin-right: 10px;
        }
        
        .cover-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .cover-title {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .cover-subtitle {
            font-size: 1.5rem;
            margin-bottom: 40px;
            color: var(--imperial-gold);
            font-weight: 500;
        }
        
        .value-item {
            padding: 25px;
            border-radius: 10px;
            background-color: white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            margin-bottom: 25px;
            transition: all 0.3s ease;
            height: 100%;
            border-left: 4px solid var(--imperial-gold);
        }
        
        .value-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
        }
        
        .contact-info {
            margin-bottom: 30px;
            padding: 25px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
        }
        
        .contact-icon {
            font-size: 1.8rem;
            color: var(--imperial-gold);
            margin-right: 20px;
            min-width: 40px;
            text-align: center;
        }
        
        footer {
            background-color: var(--imperial-dark);
            color: white;
            padding: 50px 0 25px;
        }
        
        .social-icon {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            margin-right: 10px;
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            background: var(--imperial-gold);
            color: var(--imperial-dark);
            transform: translateY(-3px);
        }
        
        .stats-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--imperial-gold);
            margin-bottom: 5px;
        }
        
        .stats-item {
            text-align: center;
            padding: 20px;
        }
        
        .divider {
            height: 3px;
            width: 50px;
            background: var(--imperial-gold);
            margin: 20px auto;
        }
        
        .testimonial-card {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            margin: 15px;
            position: relative;
        }
        
        .testimonial-card:after {
            content: ''';
            position: absolute;
            top: 15px;
            right: 25px;
            font-size: 5rem;
            color: rgba(200, 151, 32, 0.1);
            font-family: Arial, sans-serif;
        }
        
        .client-logo {
            height: 60px;
            filter: grayscale(100%);
            opacity: 0.7;
            transition: all 0.3s ease;
        }
        
        .client-logo:hover {
            filter: grayscale(0);
            opacity: 1;
        }
        
        .form-control {
            padding: 12px 15px;
            border-radius: 4px;
            border: 1px solid #ddd;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: var(--imperial-blue);
            box-shadow: 0 0 0 3px rgba(12, 45, 72, 0.1);
        }
        
        /* Animações */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .fade-in {
            animation: fadeIn 1s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        
        /* Responsividade */
        @media (max-width: 992px) {
            .cover-title {
                font-size: 2.8rem;
            }
            
            .page-section {
                padding: 80px 0;
            }
        }
        
        @media (max-width: 768px) {
            .cover-title {
                font-size: 2.3rem;
            }
            
            .cover-subtitle {
                font-size: 1.2rem;
            }
            
            .page-section {
                padding: 60px 0;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .stats-number {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navegação -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand logo" href="#">
                <!-- Substitua pelo logo real -->
                <span class="logo-img-placeholder" style="width: 40px; height: 40px; background: var(--imperial-gold); margin-right: 10px; border-radius: 5px;"></span>
                Imperial <span>Serviços CN</span>
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#cover">Início</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">Quem Somos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#services">Serviços</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#projects">Projetos</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#differentials">Diferenciais</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">Contato</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Capa -->
    <section id="cover" class="page-section imperial-bg-light">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-lg-10 cover-content fade-in">
                    <h1 class="cover-title mb-4">Portfólio de Serviços</h1>
                    <p class="cover-subtitle">Qualidade, Segurança e Inovação</p>
                    <div class="mt-5">
                        <a href="#about" class="btn btn-imperial btn-lg me-3">Conheça nossa empresa</a>
                        <a href="#contact" class="btn btn-outline-imperial btn-lg">Fale conosco</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Quem Somos -->
    <section id="about" class="page-section">
        <div class="container">
            <h2 class="section-title fade-in">Quem Somos</h2>
            <div class="row fade-in delay-1">
                <div class="col-lg-6">
                    <p class="lead">A Imperial Serviços CN é uma empresa especializada em soluções técnicas e serviços de engenharia elétrica, automação, segurança do trabalho e projetos de energia.</p>
                    <p>Atuamos em todo o Brasil, com foco em qualidade, segurança, eficiência e inovação. Nossa equipe é formada por engenheiros, técnicos e profissionais experientes, garantindo confiabilidade em todas as etapas.</p>
                    
                    <div class="row mt-5">
                        <div class="col-md-6 stats-item">
                            <div class="stats-number" data-count="150">0</div>
                            <div class="stats-label">Projetos Concluídos</div>
                        </div>
                        <div class="col-md-6 stats-item">
                            <div class="stats-number" data-count="12">0</div>
                            <div class="stats-label">Anos de Experiência</div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="row">
                        <div class="col-md-6 mb-4">
                            <div class="value-item">
                                <h4 class="text-imperial-gold">Missão</h4>
                                <p>Fornecer serviços e soluções de engenharia e segurança com excelência técnica.</p>
                            </div>
                        </div>
                        <div class="col-md-6 mb-4">
                            <div class="value-item">
                                <h4 class="text-imperial-gold">Visão</h4>
                                <p>Ser referência nacional em soluções técnicas integradas.</p>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="value-item">
                                <h4 class="text-imperial-gold">Valores</h4>
                                <div class="row mt-3">
                                    <div class="col-sm-6 mb-2">
                                        <i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Qualidade
                                    </div>
                                    <div class="col-sm-6 mb-2">
                                        <i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Segurança
                                    </div>
                                    <div class="col-sm-6 mb-2">
                                        <i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Ética
                                    </div>
                                    <div class="col-sm-6 mb-2">
                                        <i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Inovação
                                    </div>
                                    <div class="col-sm-6 mb-2">
                                        <i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Atendimento personalizado
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Áreas de Atuação -->
    <section id="services" class="page-section imperial-bg-light">
        <div class="container">
            <h2 class="section-title text-center fade-in">Áreas de Atuação</h2>
            <p class="text-center mb-5 fade-in">Oferecemos soluções completas e integradas para diversas necessidades técnicas</p>
            
            <div class="row g-4">
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-lightning-charge"></i>
                            </div>
                            <h4 class="card-title mb-3">Engenharia Elétrica e Automação</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Montagem e manutenção de painéis elétricos</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Projetos elétricos residenciais, comerciais e industriais</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Sistemas de automação</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Sistemas de proteção elétrica</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Motores de média e alta tensão</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Melhorias em processos industriais</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-1">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-sun"></i>
                            </div>
                            <h4 class="card-title mb-3">Energia Solar e Sustentabilidade</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Projetos fotovoltaicos até 150 kWp</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Sistemas off-grid e grid zero</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Dimensionamento de baterias</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Análise financeira</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Eficiência energética</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Otimização de consumo</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-2">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-shield-check"></i>
                            </div>
                            <h4 class="card-title mb-3">Segurança do Trabalho (NRs)</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> NR10, NR10 SEP</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> NR11, NR20</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> NR34, NR35</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Treinamentos presenciais</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Certificações</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Implementação de normas</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-tools"></i>
                            </div>
                            <h4 class="card-title mb-3">Serviços Técnicos e Consultoria</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Manutenção elétrica preventiva</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Projetos de eficiência energética</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Consultoria para carregadores de VE</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Análise e recuperação de sistemas</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Laudos técnicos e perícias</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Estudos de viabilidade</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-1">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-lightbulb"></i>
                            </div>
                            <h4 class="card-title mb-3">Inovações Tecnológicas</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Automação inteligente</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> IoT industrial</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Sistemas de monitoramento remoto</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Soluções de energia híbrida</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Armazenamento avançado de energia</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Integração de tecnologias</li>
                            </ul>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-2">
                    <div class="card service-card">
                        <div class="card-body p-4">
                            <div class="service-icon">
                                <i class="bi bi-gear"></i>
                            </div>
                            <h4 class="card-title mb-3">Soluções Personalizadas</h4>
                            <ul class="list-unstyled">
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Diagnóstico técnico especializado</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Desenvolvimento de projetos sob medida</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Implementação de soluções customizadas</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Suporte técnico contínuo</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Atualização tecnológica</li>
                                <li><i class="bi bi-check-circle-fill text-imperial-gold me-2"></i> Assessoria técnica especializada</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projetos Realizados -->
    <section id="projects" class="page-section">
        <div class="container">
            <h2 class="section-title text-center fade-in">Projetos Realizados e Cases de Sucesso</h2>
            <p class="text-center mb-5 fade-in">Alguns dos nossos trabalhos que demonstram nossa expertise e compromisso com a excelência</p>
            
            <div class="row g-4">
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #0c2d48, #145da0);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Projeto Fotovoltaico Orkana – 150 kWp</h4>
                                <p class="text-light">Sistema de energia solar com capacidade máxima de 150 kWp, proporcionando economia sustentável e eficiente.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Projeto Fotovoltaico Orkana – 150 kWp</h4>
                            <p class="card-text">Sistema de energia solar com capacidade máxima de 150 kWp, proporcionando economia sustentável e eficiente.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-1">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #2c3e50, #34495e);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Hotéis com Geradores e Energia Solar</h4>
                                <p class="text-light">Integração de 208 painéis de 460 W para sistema híbrido em rede hoteleira, garantindo energia contínua.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Hotéis com Geradores e Energia Solar</h4>
                            <p class="card-text">Integração de 208 painéis de 460 W para sistema híbrido em rede hoteleira, garantindo energia contínua.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-2">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #145da0, #2e86ba);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Banco do Brasil, Chuí/RS</h4>
                                <p class="text-light">Reforma elétrica completa e instalação de padrão trifásico para agência bancária.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Banco do Brasil, Chuí/RS</h4>
                            <p class="card-text">Reforma elétrica completa e instalação de padrão trifásico para agência bancária.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #7d3c98, #9b59b6);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Mineração – AERO, Mina de Vermelhos</h4>
                                <p class="text-light">Sistemas de proteção para equipamentos 440 V em ambiente de mineração.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Mineração – AERO, Mina de Vermelhos</h4>
                            <p class="card-text">Sistemas de proteção para equipamentos 440 V em ambiente de mineração.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-1">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #27ae60, #2ecc71);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Treinamentos NR10 e NR10 SEP</h4>
                                <p class="text-light">Cursos presenciais com certificação para profissionais do setor elétrico.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Treinamentos NR10 e NR10 SEP</h4>
                            <p class="card-text">Cursos presenciais com certificação para profissionais do setor elétrico.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 fade-in delay-2">
                    <div class="card project-card h-100">
                        <div class="project-img" style="background: linear-gradient(45deg, #e74c3c, #e67e22);"></div>
                        <div class="project-overlay">
                            <div>
                                <h4 class="text-white">Laudos Técnicos e Perícias</h4>
                                <p class="text-light">Realização de laudos técnicos e perícias em diferentes empreendimentos, garantindo segurança e conformidade.</p>
                            </div>
                        </div>
                        <div class="card-body">
                            <h4 class="card-title text-imperial-gold">Laudos Técnicos e Perícias</h4>
                            <p class="card-text">Realização de laudos técnicos e perícias em diferentes empreendimentos, garantindo segurança e conformidade.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Diferenciais -->
    <section id="differentials" class="page-section imperial-bg-primary text-white">
        <div class="container">
            <h2 class="section-title text-center text-white fade-in">Nossos Diferenciais</h2>
            <p class="text-center mb-5 fade-in">O que nos torna a escolha certa para seus projetos de engenharia e soluções técnicas</p>
            
            <div class="row">
                <div class="col-md-6 col-lg-4 mb-4 fade-in">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-award-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Experiência Nacional</h4>
                            <p>Atuação em projetos de grande porte em todo o Brasil, com expertise comprovada em diversos segmentos.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in delay-1">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-people-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Equipe Qualificada</h4>
                            <p>Profissionais técnicos qualificados e multidisciplinares, com certificações e treinamentos constantes.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in delay-2">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-puzzle-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Integração de Soluções</h4>
                            <p>Integração completa entre elétrica, automação, segurança e sustentabilidade em um único fornecedor.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-gear-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Soluções Personalizadas</h4>
                            <p>Atendimento e soluções customizadas para cada cliente, considerando necessidades específicas.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in delay-1">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-file-earmark-text-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Treinamentos Certificados</h4>
                            <p>Treinamentos com certificação oficial e reconhecida, ministrados por profissionais experientes.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in delay-2">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-clipboard-data-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Laudos e Perícias</h4>
                            <p>Capacidade de entregar laudos técnicos, perícias e estudos de eficiência energética com credibilidade.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in offset-lg-2">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-lightbulb-fill text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Inovação Tecnológica</h4>
                            <p>Acompanhamento das principais inovações do setor para manter o cliente na vanguarda tecnológica.</p>
                        </div>
                    </div>
                </div>
                
                <div class="col-md-6 col-lg-4 mb-4 fade-in delay-1">
                    <div class="d-flex align-items-start">
                        <i class="bi bi-shield-check text-imperial-gold me-3" style="font-size: 2.2rem;"></i>
                        <div>
                            <h4>Conformidade e Segurança</h4>
                            <p>Todos os serviços realizados seguindo rigorosamente as normas técnicas e de segurança aplicáveis.</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="row mt-5">
                <div class="col-12">
                    <div class="text-center fade-in">
                        <a href="#contact" class="btn btn-imperial btn-lg">Solicitar Orçamento</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contact" class="page-section">
        <div class="container">
            <h2 class="section-title text-center fade-in">Contato</h2>
            <p class="text-center mb-5 fade-in">Entre em contato conosco para solicitar um orçamento ou tirar suas dúvidas</p>
            
            <div class="row">
                <div class="col-lg-5 fade-in">
                    <div class="contact-info">
                        <h3 class="mb-4">Informações de Contato</h3>
                        
                        <div class="d-flex align-items-center mb-4">
                            <i class="bi bi-telephone-fill contact-icon"></i>
                            <div>
                                <h5>Telefone</h5>
                                <p>(84) 99653-3300</p>
                            </div>
                        </div>
                        
                        <div class="d-flex align-items-center mb-4">
                            <i class="bi bi-envelope-fill contact-icon"></i>
                            <div>
                                <h5>E-mail</h5>
                                <p>imperialservicoscn@gmail.com</p>
                            </div>
                        </div>
                        
                        <div class="d-flex align-items-center mb-4">
                            <i class="bi bi-geo-alt-fill contact-icon"></i>
                            <div>
                                <h5>Área de Atuação</h5>
                                <p>Todo o Brasil</p>
                            </div>
                        </div>
                        
                        <div class="mt-5">
                            <h5 class="mb-3">Siga-nos</h5>
                            <a href="#" class="social-icon"><i class="bi bi-linkedin"></i></a>
                            <a href="#" class="social-icon"><i class="bi bi-instagram"></i></a>
                            <a href="#" class="social-icon"><i class="bi bi-facebook"></i></a>
                            <a href="#" class="social-icon"><i class="bi bi-youtube"></i></a>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-7 fade-in delay-1">
                    <div class="contact-info">
                        <h3 class="mb-4">Envie uma Mensagem</h3>
                        <form>
                            <div class="row">
                                <div class="col-md-6 mb-3">
                                    <label for="name" class="form-label">Nome Completo</label>
                                    <input type="text" class="form-control" id="name" required>
                                </div>
                                <div class="col-md-6 mb-3">
                                    <label for="company" class="form-label">Empresa</label>
                                    <input type="text" class="form-control" id="company">
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-md-6 mb-3">
                                    <label for="email" class="form-label">E-mail</label>
                                    <input type="email" class="form-control" id="email" required>
                                </div>
                                <div class="col-md-6 mb-3">
                                    <label for="phone" class="form-label">Telefone</label>
                                    <input type="tel" class="form-control" id="phone">
                                </div>
                            </div>
                            <div class="mb-3">
                                <label for="service" class="form-label">Serviço de Interesse</label>
                                <select class="form-select" id="service">
                                    <option selected>Selecione um serviço...</option>
                                    <option value="engenharia">Engenharia Elétrica e Automação</option>
                                    <option value="solar">Energia Solar e Sustentabilidade</option>
                                    <option value="seguranca">Segurança do Trabalho (NRs)</option>
                                    <option value="consultoria">Serviços Técnicos e Consultoria</option>
                                    <option value="treinamentos">Treinamentos e Certificações</option>
                                    <option value="outros">Outros</option>
                                </select>
                            </div>
                            <div class="mb-4">
                                <label for="message" class="form-label">Mensagem</label>
                                <textarea class="form-control" id="message" rows="5" required></textarea>
                            </div>
                            <button type="submit" class="btn btn-imperial">Enviar Mensagem</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="text-center">
        <div class="container">
            <div class="row justify-content-center">
                <div class="col-lg-8">
                    <p class="mb-3">Imperial Serviços CN – Qualidade, Segurança e Inovação</p>
                    <p class="text-muted">© 2023 Imperial Serviços CN. Todos os direitos reservados.</p>
                </div>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('navbar-scroll');
            } else {
                navbar.classList.remove('navbar-scroll');
            }
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a.nav-link').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // Simple counter animation for stats
        const counters = document.querySelectorAll('.stats-number');
        const speed = 200;
        
        counters.forEach(counter => {
            const target = +counter.getAttribute('data-count');
            const count = +counter.innerText;
            const increment = Math.ceil(target / speed);
            
            if (count < target) {
                let current = count;
                const updateCount = () => {
                    current += increment;
                    counter.innerText = current;
                    
                    if (current < target) {
                        setTimeout(updateCount, 1);
                    } else {
                        counter.innerText = target;
                    }
                };
                updateCount();
            } else {
                counter.innerText = target;
            }
        });
        
        // Animation on scroll
        window.addEventListener('scroll', function() {
            const elements = document.querySelectorAll('.fade-in');
            
            elements.forEach(element => {
                const position = element.getBoundingClientRect();
                
                // If the element is in the viewport
                if(position.top < window.innerHeight - 100) {
                    element.style.opacity = 1;
                    element.style.transform = 'translateY(0)';
                }
            });
        });
        
        // Trigger scroll event on load to check for elements already in view
        window.dispatchEvent(new Event('scroll'));
    </script>
</body>
</html>
