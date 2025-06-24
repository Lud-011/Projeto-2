# Projeto-2
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio Criativo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #6e45e2;
            --secondary-color: #88d3ce;
            --dark-color: #1a1a2e;
            --light-color: #f9f9f9;
            --accent-color: #ff7e5f;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
        }
        
        /* Títulos */
        .section-title {
            position: relative;
            display: inline-block;
            margin-bottom: 3rem;
            color: var(--dark-color);
            font-weight: 700;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 4px;
            bottom: -10px;
            left: 20%;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
            border-radius: 2px;
        }
        
        /* Cards */
        .portfolio-card {
            border: none;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
            background: white;
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }
        
        .portfolio-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(110, 69, 226, 0.1) 0%, rgba(136, 211, 206, 0.1) 100%);
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .portfolio-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
        }
        
        .portfolio-card:hover::before {
            opacity: 1;
        }
        
        /* Imagem do card */
        .card-img-container {
            height: 220px;
            overflow: hidden;
            position: relative;
        }
        
        .card-img-top {
            height: 100%;
            width: 100%;
            object-fit: cover;
            transition: transform 0.8s ease;
        }
        
        .portfolio-card:hover .card-img-top {
            transform: scale(1.1);
        }
        
        /* Overlay */
        .card-img-overlay {
            background: rgba(26, 26, 46, 0.7);
            opacity: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: opacity 0.5s ease;
            padding: 20px;
        }
        
        .portfolio-card:hover .card-img-overlay {
            opacity: 1;
        }
        
        .overlay-content {
            transform: translateY(20px);
            transition: transform 0.5s ease;
            text-align: center;
        }
        
        .portfolio-card:hover .overlay-content {
            transform: translateY(0);
        }
        
        /* Corpo do card */
        .card-body {
            padding: 25px;
            position: relative;
        }
        
        .card-title {
            font-weight: 700;
            color: var(--dark-color);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .card-text {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }
        
        /* Badges */
        .tech-badge {
            padding: 8px 12px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-right: 8px;
            margin-bottom: 8px;
            display: inline-block;
            transition: all 0.3s ease;
        }
        
        .tech-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Botão */
        .project-btn {
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            border: none;
            border-radius: 30px;
            padding: 10px 25px;
            color: white;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.8rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(110, 69, 226, 0.3);
        }
        
        .project-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(110, 69, 226, 0.4);
            color: white;
        }
        
        /* Efeitos especiais */
        .card-hover-effect {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            background: radial-gradient(circle at center, rgba(255, 255, 255, 0.8) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.5s ease;
            pointer-events: none;
        }
        
        .portfolio-card:hover .card-hover-effect {
            opacity: 0.3;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .card-img-container {
                height: 180px;
            }
            
            .card-body {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Seção de Projetos -->
    <section id="projetos" class="container py-5">
        <div class="text-center">
            <h2 class="section-title">Meus Projetos Criativos</h2>
            <p class="text-muted mb-5">Explore meus trabalhos mais recentes e projetos destacados</p>
        </div>
        
        <div class="row g-4">
            <!-- Projeto 1 -->
            <div class="col-md-6 col-lg-4">
                <div class="portfolio-card">
                    <div class="card-hover-effect"></div>
                    <div class="card-img-container">
                        <img src="https://source.unsplash.com/random/600x400/?web-design" class="card-img-top" alt="Projeto Web">
                        <div class="card-img-overlay">
                            <div class="overlay-content">
                                <h5 class="text-white mb-3">Projeto Web</h5>
                                <a href="#" class="project-btn">Ver Detalhes <i class="fas fa-arrow-right ms-2"></i></a>
                            </div>
                        </div>
                    </div>
                    <div class="card-body">
                        <div class="d-flex justify-content-between align-items-start mb-3">
                            <h5 class="card-title m-0">Sistema de Dashboard</h5>
                            <span class="badge bg-primary rounded-pill">Novo</span>
                        </div>
                        <p class="card-text">Plataforma de análise de dados com visualizações interativas e relatórios personalizados.</p>
                        <div class="tech-tags">
                            <span class="tech-badge" style="background-color: #61dafb; color: #000;">React</span>
                            <span class="tech-badge" style="background-color: #563d7c; color: white;">Bootstrap</span>
                            <span class="tech-badge" style="background-color: #ff6384; color: white;">Chart.js</span>
                            <span class="tech-badge" style="background-color: #f0db4f; color: #000;">JavaScript</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Projeto 2 -->
            <div class="col-md-6 col-lg-4">
                <div class="portfolio-card">
                    <div class="card-hover-effect"></div>
                    <div class="card-img-container">
                        <img src="https://source.unsplash.com/random/600x400/?mobile-app" class="card-img-top" alt="App Mobile">
                        <div class="card-img-overlay">
                            <div class="overlay-content">
                                <h5 class="text-white mb-3">Aplicativo Mobile</h5>
                                <a href="#" class="project-btn">Ver Detalhes <i class="fas fa-arrow-right ms-2"></i></a>
                            </div>
                        </div>
                    </div>
                    <div class="card-body">
                        <div class="d-flex justify-content-between align-items-start mb-3">
                            <h5 class="card-title m-0">App Finanças</h5>
                            <span class="badge bg-success rounded-pill">Popular</span>
                        </div>
                        <p class="card-text">Aplicativo para controle de gastos, investimentos e planejamento financeiro pessoal.</p>
                        <div class="tech-tags">
                            <span class="tech-badge" style="background-color: #02569b; color: white;">Flutter</span>
                            <span class="tech-badge" style="background-color: #ffcb2b; color: #000;">Firebase</span>
                            <span class="tech-badge" style="background-color: #34a853; color: white;">Google API</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Projeto 3 -->
            <div class="col-md-6 col-lg-4">
                <div class="portfolio-card">
                    <div class="card-hover-effect"></div>
                    <div class="card-img-container">
                        <img src="https://source.unsplash.com/random/600x400/?branding" class="card-img-top" alt="Design Gráfico">
                        <div class="card-img-overlay">
                            <div class="overlay-content">
                                <h5 class="text-white mb-3">Design Gráfico</h5>
                                <a href="#" class="project-btn">Ver Detalhes <i class="fas fa-arrow-right ms-2"></i></a>
                            </div>
                        </div>
                    </div>
                    <div class="card-body">
                        <div class="d-flex justify-content-between align-items-start mb-3">
                            <h5 class="card-title m-0">Marca Corporativa</h5>
                            <span class="badge bg-warning rounded-pill">Destaque</span>
                        </div>
                        <p class="card-text">Desenvolvimento completo de identidade visual para startup de tecnologia.</p>
                        <div class="tech-tags">
                            <span class="tech-badge" style="background-color: #ff7c00; color: white;">Illustrator</span>
                            <span class="tech-badge" style="background-color: #31a8ff; color: white;">Photoshop</span>
                            <span class="tech-badge" style="background-color: #000000; color: white;">Figma</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
