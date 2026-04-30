<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Academia Domínio | Porto dos Padres - Potência & Elegância</title>
    <!-- Font Awesome 6 (gratuito) -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <!-- Google Fonts: Poppins + Playfair Display para toque charmoso -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #fefcf5;
            color: #1f2a3a;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 32px;
        }

        /* --- Estilo Header refinado --- */
        header {
            background: rgba(15, 25, 45, 0.92);
            backdrop-filter: blur(12px);
            padding: 0.9rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1050;
            transition: all 0.3s ease;
            border-bottom: 1px solid rgba(255, 215, 175, 0.2);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.7rem;
            font-weight: 800;
            display: flex;
            align-items: center;
            gap: 12px;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #FFFFFF 30%, #FFB347 80%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .logo i {
            font-size: 2rem;
            background: none;
            -webkit-background-clip: unset;
            background-clip: unset;
            color: #FFA559;
            text-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.2rem;
        }

        .nav-links a {
            color: #f0ede8;
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: 0.25s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -6px;
            left: 0;
            width: 0%;
            height: 2px;
            background: #FFB347;
            transition: 0.3s;
        }

        .nav-links a:hover::after,
        .nav-links a.active::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: #FFB347;
        }

        /* Hero Section — sofisticado e imponente */
        .hero {
            min-height: 100vh;
            background: linear-gradient(107deg, #0A1828 0%, #1A2F3F 100%);
            position: relative;
            display: flex;
            align-items: center;
            margin-top: 0;
            isolation: isolate;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            inset: 0;
            background: radial-gradient(circle at 70% 30%, rgba(255, 165, 75, 0.12), transparent 70%);
            z-index: 1;
        }

        .hero .container {
            position: relative;
            z-index: 2;
        }

        .hero-content {
            text-align: center;
            max-width: 900px;
            margin: 0 auto;
            color: white;
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 800;
            font-family: 'Playfair Display', serif;
            letter-spacing: -0.5px;
            background: linear-gradient(to right, #FFF9F0, #FFD4A4);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
        }

        .hero-content h2 {
            font-size: 1.8rem;
            font-weight: 400;
            color: #FFD8B0;
            margin-bottom: 1.5rem;
            letter-spacing: 1px;
        }

        .rating {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin: 2rem 0;
            background: rgba(255,255,240,0.08);
            backdrop-filter: blur(4px);
            padding: 12px 28px;
            border-radius: 80px;
            width: fit-content;
            margin-left: auto;
            margin-right: auto;
        }

        .stars {
            color: #FFC107;
            font-size: 1.3rem;
            letter-spacing: 3px;
        }

        .rating-number {
            background: #FFA559;
            padding: 6px 18px;
            border-radius: 40px;
            font-weight: 700;
            font-size: 1rem;
            color: #1F2A3A;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }

        .cta-button {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(95deg, #FFA559, #FF7F3F);
            color: #1F2A3A;
            padding: 14px 38px;
            border-radius: 60px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            margin-top: 1.8rem;
            transition: all 0.3s ease;
            box-shadow: 0 12px 20px -10px rgba(255, 127, 63, 0.4);
            border: none;
            letter-spacing: 0.3px;
        }

        .cta-button i {
            font-size: 1.2rem;
        }

        .cta-button:hover {
            transform: translateY(-5px);
            background: linear-gradient(95deg, #FFB26B, #FF964F);
            box-shadow: 0 20px 28px -12px rgba(255, 100, 30, 0.5);
        }

        /* Sections refinadas */
        section {
            padding: 90px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.6rem;
            font-weight: 700;
            font-family: 'Playfair Display', serif;
            color: #1C2E42;
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 70px;
            height: 4px;
            background: #FFA559;
            margin: 16px auto 0;
            border-radius: 4px;
        }

        /* Info Cards - elegantes */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }

        .info-card {
            background: #FFFFFF;
            padding: 2rem 1.5rem;
            border-radius: 32px;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.08);
            text-align: center;
            transition: all 0.35s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            border: 1px solid rgba(255, 165, 75, 0.2);
            backdrop-filter: blur(2px);
        }

        .info-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 28px 40px -16px rgba(255, 100, 30, 0.25);
            border-color: rgba(255, 165, 75, 0.5);
        }

        .info-card i {
            font-size: 3rem;
            background: linear-gradient(135deg, #FF8C42, #E8622E);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1rem;
        }

        .info-card h3 {
            font-size: 1.6rem;
            margin: 1rem 0 0.8rem;
            font-weight: 700;
            color: #1E2F41;
        }

        .info-card p {
            color: #4a5b6e;
            font-weight: 400;
            line-height: 1.5;
        }

        /* Avaliações - estilo depoimentos premium */
        .reviews-section {
            background: linear-gradient(115deg, #FEF9F0 0%, #FFF5E6 100%);
            border-radius: 80px 0 80px 0;
            margin: 20px 0;
            box-shadow: inset 0 0 0 1px rgba(255,255,240,0.8);
        }

        .review-card {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(8px);
            border-radius: 2rem;
            padding: 2rem;
            transition: 0.2s;
            border: 1px solid rgba(255, 165, 75, 0.3);
            box-shadow: 0 12px 25px -10px rgba(0,0,0,0.05);
        }

        .review-card:hover {
            background: white;
            border-color: #FFA559;
        }

        .review-author {
            font-weight: 700;
            font-size: 1.2rem;
            color: #1F2E3F;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .review-author i {
            color: #FFA559;
            font-size: 1.2rem;
        }

        .review-text {
            font-style: normal;
            color: #2c3e4e;
            margin-top: 12px;
            font-weight: 400;
            line-height: 1.5;
            border-left: 3px solid #FFA559;
            padding-left: 18px;
        }

        /* Contact elegante */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .glass-contact {
            background: #FFFFFF;
            border-radius: 40px;
            padding: 2rem;
            box-shadow: 0 25px 40px -18px rgba(0,0,0,0.15);
            border: 1px solid rgba(255,165,75,0.3);
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.8rem;
            padding: 1rem;
            background: #FEF7EF;
            border-radius: 28px;
            transition: 0.2s;
        }

        .contact-item i {
            font-size: 1.8rem;
            color: #FF7F3F;
            width: 48px;
        }

        .contact-item strong {
            color: #1F2E3F;
        }

        .btn-whatsapp {
            background: #25D366;
            background: linear-gradient(105deg, #25D366, #128C7E);
            color: white !important;
            box-shadow: 0 5px 12px rgba(37, 211, 102, 0.3);
        }

        footer {
            background: #0F1A24;
            color: #E9E2D4;
            border-top: 1px solid #FFB87C30;
        }

        .social-links a {
            background: rgba(255, 165, 75, 0.15);
            width: 44px;
            height: 44px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            transition: 0.2s;
            color: #FFCF9A;
            font-size: 1.4rem;
        }

        .social-links a:hover {
            background: #FFA559;
            color: #1F2A3A;
            transform: scale(1.05);
        }

        /* Animações */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(35px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-up {
            opacity: 0;
            animation: fadeUp 0.8s cubic-bezier(0.2, 0.9, 0.4, 1) forwards;
        }

        /* responsivo */
        @media (max-width: 880px) {
            .nav-links {
                display: none;
            }
            .hero-content h1 {
                font-size: 2.8rem;
            }
            .contact-grid {
                grid-template-columns: 1fr;
            }
            .section-title {
                font-size: 2rem;
            }
            .container {
                padding: 0 24px;
            }
            .rating {
                flex-direction: column;
                gap: 12px;
                padding: 14px 24px;
            }
        }

        @media (max-width: 550px) {
            .hero-content h1 {
                font-size: 2.3rem;
            }
            .cta-button {
                padding: 12px 28px;
            }
        }

        /* detalhe extra: botão flutuante mental? não, mas um toque refinado nos cards */
        .info-card .small-text {
            font-size: 0.9rem;
            font-weight: 500;
            color: #FF7F3F;
            margin-top: 10px;
        }
        .highlight {
            font-weight: 700;
            color: #E65C1E;
        }
    </style>
</head>
<body>

<header id="header">
    <nav class="container">
        <div class="logo">
            <i class="fas fa-dumbbell"></i> 
            <span>DOMÍNIO</span>
        </div>
        <ul class="nav-links">
            <li><a href="#inicio">Início</a></li>
            <li><a href="#sobre">A Academia</a></li>
            <li><a href="#avaliacoes">Depoimentos</a></li>
            <li><a href="#contato">Contato</a></li>
        </ul>
    </nav>
</header>

<!-- Hero Section -->
<section id="inicio" class="hero">
    <div class="container">
        <div class="hero-content fade-up" style="animation-delay: 0.1s;">
            <h1>Academia Domínio</h1>
            <h2>Porto dos Padres • Onde força encontra elegância</h2>
            <div class="rating">
                <div class="stars">
                    <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                </div>
                <span class="rating-number">5.0 ★ (124 avaliações)</span>
            </div>
            <a href="#contato" class="cta-button"><i class="fas fa-calendar-check"></i> Agende sua visita gratuita</a>
        </div>
    </div>
</section>

<!-- Sobre / Informações principais -->
<section id="sobre">
    <div class="container">
        <h2 class="section-title">Experiência que transforma</h2>
        <div class="info-grid">
            <div class="info-card fade-up">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Localização premium</h3>
                <p>Av. Pref. Dr. Roque Vernalha, 2002<br>Vila Itiberê, Paranaguá - PR<br>83221-000</p>
                <div class="small-text"><i class="fas fa-parking"></i> Estacionamento próprio</div>
            </div>
            <div class="info-card fade-up">
                <i class="fas fa-clock"></i>
                <h3>Horário estendido</h3>
                <p><strong class="highlight">Aberto agora</strong> • Segunda a sábado<br>Até <strong>23:00</strong> para você treinar no seu ritmo</p>
                <div class="small-text">Horário de pico: 20h | média 45min-1h30</div>
            </div>
            <div class="info-card fade-up">
                <i class="fas fa-dumbbell"></i>
                <h3>Estrutura de elite</h3>
                <p>Equipamentos modernos, ar condicionado, música envolvente e área funcional completa.</p>
                <div class="small-text"> + de 1500m² de potência</div>
            </div>
        </div>
    </div>
</section>

<!-- Depoimentos - charmoso e autêntico -->
<section id="avaliacoes" class="reviews-section">
    <div class="container" style="padding: 20px 0;">
        <h2 class="section-title">Vozes da nossa tribo</h2>
        <div class="info-grid">
            <div class="review-card fade-up">
                <div class="review-author"><i class="fas fa-user-astronaut"></i> Heaven</div>
                <div class="review-text">“Muito boa academia, profissional, ótimos equipamentos e estrutura impecável. Ambiente que motiva!”</div>
                <div class="small-text" style="margin-top: 12px;"><i class="fas fa-star" style="color:#FFA559;"></i> 5 estrelas</div>
            </div>
            <div class="review-card fade-up">
                <div class="review-author"><i class="fas fa-user-check"></i> Alexander Gomes</div>
                <div class="review-text">“Ótimo lugar, com equipamentos novos e de qualidade, atendimento excelente. A academia mais completa da região.”</div>
                <div class="small-text" style="margin-top: 12px;"><i class="fas fa-star" style="color:#FFA559;"></i> 5 estrelas</div>
            </div>
            <div class="review-card fade-up">
                <div class="review-author"><i class="fas fa-fitness"></i> Andrezza Cavalcante</div>
                <div class="review-text">“Ambiente maravilhoso para treinar, bastante equipamentos show e professores super atenciosos. Me ssegunda casa.”</div>
                <div class="small-text" style="margin-top: 12px;"><i class="fas fa-star" style="color:#FFA559;"></i> 5 estrelas</div>
            </div>
        </div>
        <!-- + depoimento extra (charme) -->
        <div style="text-align: center; margin-top: 2rem;">
            <p style="font-style: italic; color:#6A4E2E;">⭐ mais de 120 clientes satisfeitos só no Google Maps ⭐</p>
        </div>
    </div>
</section>

<!-- Contato elegante com CTA direto -->
<section id="contato">
    <div class="container">
        <h2 class="section-title">Sua jornada começa aqui</h2>
        <div class="contact-grid">
            <div class="glass-contact fade-up">
                <h3 style="color:#1C2E42; margin-bottom: 1rem;"><i class="fas fa-heart" style="color:#FF7F3F;"></i> Vamos conversar?</h3>
                <p style="margin-bottom: 1.8rem;">Treine no ambiente mais acolhedor e sofisticado de Porto dos Padres. Atendimento personalizado, planos flexíveis e primeiro treino experimental gratuito.</p>
                <a href="tel:+5541984995739" class="cta-button" style="background:#1F2E3F; color:white; box-shadow: none;"><i class="fas fa-phone-alt"></i> Ligar agora</a>
                <a href="https://wa.me/5541984995739" target="_blank" class="cta-button btn-whatsapp" style="margin-left: 12px; background: #25D366; color: #1F2A3A;"><i class="fab fa-whatsapp"></i> WhatsApp</a>
            </div>
            <div class="glass-contact fade-up">
                <div class="contact-item">
                    <i class="fas fa-map-pin"></i>
                    <div><strong>Endereço completo</strong><br>Av. Pref. Dr. Roque Vernalha, 2002<br>Vila Itiberê, Paranaguá - PR, 83221-000</div>
                </div>
                <div class="contact-item">
                    <i class="fas fa-mobile-alt"></i>
                    <div><strong>Contato direto</strong><br>(41) 98499-5739<br><span style="font-size:0.85rem;">Atendimento via ligação e WhatsApp</span></div>
                </div>
                <div class="contact-item">
                    <i class="fas fa-clock"></i>
                    <div><strong>Funcionamento</strong><br>Segunda a Sexta: 06h - 23h<br>Sábado: 08h - 18h | Domingo: 09h - 13h</div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Footer refinado -->
<footer>
    <div class="container">
        <div style="display: flex; flex-direction: column; align-items: center; gap: 1rem;">
            <div class="logo" style="background: none; color:#FFCF9A; font-size: 1.5rem;">
                <i class="fas fa-dumbbell"></i> Academia Domínio
            </div>
            <p style="max-width: 500px; opacity: 0.85;">Transformando vidas através do esporte e bem-estar desde 2019. Orgulho em Porto dos Padres.</p>
            <div class="social-links">
                <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="https://wa.me/5541984995739" target="_blank" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
            </div>
            <p style="font-size: 0.85rem; margin-top: 1rem;">© 2025 Academia Domínio - Porto dos Padres. Todos os direitos reservados.</p>
        </div>
    </div>
</footer>

<script>
    // Smooth scroll para links internos + ativar classe ativa no menu
    const links = document.querySelectorAll('a[href^="#"]');
    links.forEach(link => {
        link.addEventListener('click', function(e) {
            const targetId = this.getAttribute('href');
            if (targetId === "#" || targetId === "") return;
            const targetElement = document.querySelector(targetId);
            if (targetElement) {
                e.preventDefault();
                targetElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
                // atualiza URL sem hash jump brusco (opcional)
                history.pushState(null, null, targetId);
            }
        });
    });

    // Observer para animação fade-up quando entrar na viewport
    const fadeElements = document.querySelectorAll('.fade-up');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.animationPlayState = 'running';
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' });

    fadeElements.forEach(el => {
        el.style.opacity = '0';
        el.style.animationPlayState = 'paused';
        observer.observe(el);
    });

    // header efeito de sombra ao rolar
    const header = document.getElementById('header');
    window.addEventListener('scroll', () => {
        if (window.scrollY > 20) {
            header.style.background = 'rgba(10, 22, 38, 0.96)';
            header.style.backdropFilter = 'blur(14px)';
            header.style.boxShadow = '0 8px 20px rgba(0,0,0,0.2)';
        } else {
            header.style.background = 'rgba(15, 25, 45, 0.92)';
            header.style.backdropFilter = 'blur(12px)';
            header.style.boxShadow = 'none';
        }
    });

    // pequeno detalhe: garantir que qualquer clique no botão WhatsApp funcione
    const whatsBtn = document.querySelector('.btn-whatsapp');
    if(whatsBtn) {
        whatsBtn.addEventListener('click', (e) => {
            // já tem href, apenas prevenir propagação se necessário
        });
    }

    // corrigir links sociais para abrir nova aba (placeholder, mas com estilo)
    const socialIcons = document.querySelectorAll('.social-links a');
    socialIcons.forEach(icon => {
        icon.setAttribute('target', '_blank');
        icon.setAttribute('rel', 'noopener noreferrer');
    });
    // melhorar link do whats do footer
    const footerWhats = document.querySelector('.social-links a[href*="whatsapp"]');
    if(footerWhats && footerWhats.getAttribute('href') === '#') {
        footerWhats.setAttribute('href', 'https://wa.me/5541984995739');
    }
</script>
</body>
</html>
