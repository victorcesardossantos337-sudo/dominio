<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Academia Domínio - Porto dos Padres | Potência & Elegância</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=Playfair+Display:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #0A0F1A;
            color: #E8EDF5;
            overflow-x: hidden;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 32px;
        }

        /* Header */
        header {
            background: rgba(10, 18, 28, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 180, 80, 0.2);
            transition: all 0.3s;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.6rem;
            font-weight: 800;
        }

        .logo i {
            font-size: 2rem;
            color: #FF8C42;
            text-shadow: 0 0 10px rgba(255, 140, 66, 0.5);
        }

        .logo span {
            background: linear-gradient(135deg, #FFFFFF, #FFC085);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #E0E6F0;
            text-decoration: none;
            font-weight: 500;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: #FF8C42;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, #0A121F 0%, #1A2A3F 50%, #0E1A2A 100%);
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 70% 30%, rgba(255, 140, 66, 0.15), transparent 70%);
            pointer-events: none;
        }

        .hero-content {
            text-align: center;
            position: relative;
            z-index: 2;
        }

        .hero-content h1 {
            font-size: 4.5rem;
            font-weight: 800;
            font-family: 'Playfair Display', serif;
            background: linear-gradient(135deg, #FFFFFF, #FFD4A0, #FF9B50);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
        }

        .hero-content h2 {
            font-size: 1.8rem;
            font-weight: 400;
            color: #FFD9A5;
            margin-bottom: 1.5rem;
            letter-spacing: 1px;
        }

        .rating-box {
            display: inline-flex;
            align-items: center;
            gap: 20px;
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(8px);
            padding: 12px 28px;
            border-radius: 60px;
            margin: 1.5rem auto;
        }

        .stars {
            color: #FFB347;
            font-size: 1.3rem;
            letter-spacing: 4px;
        }

        .rating-number {
            background: #FF8C42;
            color: #1A1A2E;
            padding: 6px 18px;
            border-radius: 40px;
            font-weight: 700;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(95deg, #FF8C42, #FF6B35);
            color: #0A0F1A;
            padding: 14px 42px;
            border-radius: 60px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            margin-top: 1.8rem;
            transition: all 0.3s;
            box-shadow: 0 10px 25px -8px rgba(255, 100, 30, 0.4);
            border: none;
            cursor: pointer;
        }

        .btn-primary:hover {
            transform: translateY(-4px);
            box-shadow: 0 18px 30px -10px rgba(255, 100, 30, 0.6);
        }

        .btn-whatsapp {
            background: linear-gradient(95deg, #25D366, #128C7E);
            color: white;
            box-shadow: 0 10px 25px -8px rgba(37, 211, 102, 0.4);
        }

        .btn-whatsapp:hover {
            background: linear-gradient(95deg, #34CE7C, #1BA392);
            box-shadow: 0 18px 30px -10px rgba(37, 211, 102, 0.6);
        }

        .buttons-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        section {
            padding: 90px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.6rem;
            font-weight: 700;
            font-family: 'Playfair Display', serif;
            color: #FFE4C0;
            margin-bottom: 3rem;
        }

        .section-title:after {
            content: '';
            display: block;
            width: 70px;
            height: 4px;
            background: #FF8C42;
            margin: 16px auto 0;
            border-radius: 4px;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .card {
            background: rgba(30, 40, 55, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 28px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s;
            border: 1px solid rgba(255, 140, 66, 0.2);
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 140, 66, 0.6);
            background: rgba(40, 52, 70, 0.8);
        }

        .card i {
            font-size: 3rem;
            color: #FF8C42;
            margin-bottom: 1rem;
        }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 0.8rem;
            color: #FFE0B5;
        }

        .card p {
            color: #B0C4DE;
            line-height: 1.5;
        }

        .testimonials-section {
            background: linear-gradient(135deg, #0E1622, #0A101C);
        }

        .testimonial-card {
            background: rgba(25, 35, 50, 0.8);
            backdrop-filter: blur(8px);
            border-radius: 24px;
            padding: 1.8rem;
            border-left: 4px solid #FF8C42;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 700;
            color: #FFC894;
            margin-bottom: 0.8rem;
        }

        .testimonial-text {
            font-style: italic;
            color: #CCDDE8;
            line-height: 1.5;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2.5rem;
        }

        .contact-card {
            background: rgba(30, 40, 55, 0.6);
            border-radius: 32px;
            padding: 2rem;
            border: 1px solid rgba(255, 140, 66, 0.2);
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 20px;
            margin-bottom: 1rem;
        }

        .contact-item i {
            font-size: 1.8rem;
            color: #FF8C42;
            width: 50px;
        }

        footer {
            background: #050A12;
            padding: 3rem 0 2rem;
            text-align: center;
            border-top: 1px solid rgba(255, 140, 66, 0.2);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }

        .social-links a {
            width: 45px;
            height: 45px;
            background: rgba(255, 140, 66, 0.15);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #FFC084;
            font-size: 1.3rem;
            transition: 0.3s;
            text-decoration: none;
        }

        .social-links a:hover {
            background: #FF8C42;
            color: #0A0F1A;
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .hero-content h1 {
                font-size: 2.5rem;
            }
            .hero-content h2 {
                font-size: 1.2rem;
            }
            .contact-grid {
                grid-template-columns: 1fr;
            }
            .container {
                padding: 0 20px;
            }
            .section-title {
                font-size: 2rem;
            }
            .buttons-group {
                flex-direction: column;
                align-items: center;
            }
            .btn-primary, .btn-whatsapp {
                width: fit-content;
            }
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate {
            animation: fadeUp 0.8s ease forwards;
        }
    </style>
</head>
<body>

<!-- Header -->
<header>
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
        <div class="hero-content animate">
            <h1>Academia Domínio</h1>
            <h2>Porto dos Padres • Onde força encontra elegância</h2>
            <div class="rating-box">
                <div class="stars">
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                </div>
                <span class="rating-number">5.0 ★ (124 avaliações)</span>
            </div>
            <div class="buttons-group">
                <a href="#contato" class="btn-primary"><i class="fas fa-calendar-check"></i> Agende sua visita</a>
                <a href="https://wa.me/5541984995739" target="_blank" class="btn-primary btn-whatsapp"><i class="fab fa-whatsapp"></i> Fale no WhatsApp</a>
            </div>
        </div>
    </div>
</section>

<!-- Sobre -->
<section id="sobre">
    <div class="container">
        <h2 class="section-title">Experiência que transforma</h2>
        <div class="cards-grid">
            <div class="card animate">
                <i class="fas fa-map-marker-alt"></i>
                <h3>Localização</h3>
                <p>Av. Pref. Dr. Roque Vernalha, 2002<br>Vila Itiberê, Paranaguá - PR<br>83221-000</p>
            </div>
            <div class="card animate">
                <i class="fas fa-clock"></i>
                <h3>Horário</h3>
                <p><strong style="color:#FF8C42;">Aberto agora</strong><br>Segunda a Sábado<br>Até <strong>23:00</strong></p>
            </div>
            <div class="card animate">
                <i class="fas fa-phone"></i>
                <h3>Contato</h3>
                <p>(41) 98499-5739</p>
            </div>
        </div>
    </div>
</section>

<!-- Depoimentos -->
<section id="avaliacoes" class="testimonials-section">
    <div class="container">
        <h2 class="section-title">O que nossos alunos dizem</h2>
        <div class="cards-grid">
            <div class="testimonial-card animate">
                <div class="testimonial-author">
                    <i class="fas fa-user-circle"></i> Heaven
                </div>
                <div class="testimonial-text">
                    "Muito boa academia, profissional, ótimos equipamentos e boa estrutura!"
                </div>
            </div>
            <div class="testimonial-card animate">
                <div class="testimonial-author">
                    <i class="fas fa-user-circle"></i> Alexander Gomes
                </div>
                <div class="testimonial-text">
                    "Ótimo lugar, com equipamentos novos e de qualidade, atendimento excelente."
                </div>
            </div>
            <div class="testimonial-card animate">
                <div class="testimonial-author">
                    <i class="fas fa-user-circle"></i> Andrezza Cavalcante
                </div>
                <div class="testimonial-text">
                    "Ambiente maravilhoso para treinar, bastante equipamentos show"
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Contato -->
<section id="contato">
    <div class="container">
        <h2 class="section-title">Entre em Contato</h2>
        <div class="contact-grid">
            <div class="contact-card animate">
                <h3 style="color:#FFC894; margin-bottom: 1rem;">✨ Venha treinar conosco!</h3>
                <p>Horário de pico: <strong>20:00</strong><br>Tempo médio de permanência: 45min a 1h30</p>
                <div class="buttons-group" style="margin-top: 1.5rem; justify-content: flex-start;">
                    <a href="tel:+5541984995739" class="btn-primary" style="margin-top: 0;">
                        <i class="fas fa-phone"></i> Ligar
                    </a>
                    <a href="https://wa.me/5541984995739" target="_blank" class="btn-primary btn-whatsapp" style="margin-top: 0;">
                        <i class="fab fa-whatsapp"></i> WhatsApp
                    </a>
                </div>
            </div>
            <div class="contact-card animate">
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <div><strong>Endereço:</strong><br>Av. Pref. Dr. Roque Vernalha, 2002</div>
                </div>
                <div class="contact-item">
                    <i class="fab fa-whatsapp"></i>
                    <div><strong>WhatsApp:</strong><br>(41) 98499-5739</div>
                </div>
                <div class="contact-item">
                    <i class="fas fa-clock"></i>
                    <div><strong>Horário:</strong><br>Aberto até 23:00</div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="logo" style="justify-content: center; margin-bottom: 1rem;">
            <i class="fas fa-dumbbell"></i>
            <span>DOMÍNIO</span>
        </div>
        <p>Academia Domínio - Porto dos Padres</p>
        <div class="social-links">
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="https://wa.me/5541984995739" target="_blank"><i class="fab fa-whatsapp"></i></a>
            <a href="#"><i class="fab fa-facebook-f"></i></a>
        </div>
        <p style="font-size: 0.8rem; opacity: 0.7;">© 2025 Academia Domínio - Todos os direitos reservados</p>
    </div>
</footer>

<script>
    // Smooth scroll para links internos
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                e.preventDefault();
                target.scrollIntoView({ behavior: 'smooth' });
            }
        });
    });

    // Animação ao scroll
    const animatedElements = document.querySelectorAll('.animate');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.animation = 'fadeUp 0.8s ease forwards';
                observer.unobserve(entry.target);
            }
        });
    }, { threshold: 0.1 });

    animatedElements.forEach(el => {
        el.style.opacity = '0';
        observer.observe(el);
    });
</script>
</body>
</html>
