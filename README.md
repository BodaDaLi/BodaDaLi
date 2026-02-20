<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Diana & Liz - Nuestra Boda Boho</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600&family=Amatic+SC:wght@400;700&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --terracota: #c17f59;
            --sage: #9caf88;
            --cream: #f5f1e8;
            --sand: #e6ddd0;
            --brown: #5d4e37;
            --rust: #a0522d;
            --olive: #6b7c5c;
            --clay: #d4a373;
            --wheat: #e9edc9;
            --dusty-rose: #d4a5a5;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            color: var(--brown);
            background-color: var(--cream);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Hero Section - Boho Style */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, rgba(193,127,89,0.2) 0%, rgba(156,175,136,0.3) 50%, rgba(212,163,115,0.2) 100%),
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M0,50 Q25,30 50,50 T100,50" fill="none" stroke="%23c17f59" stroke-width="0.5" opacity="0.3"/></svg>');
            background-size: cover, 200px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200"><path d="M40,40 Q60,20 80,40 T120,40" fill="none" stroke="%239caf88" stroke-width="1" opacity="0.2"/><circle cx="150" cy="80" r="2" fill="%23c17f59" opacity="0.3"/><path d="M20,150 Q40,130 60,150" fill="none" stroke="%23a0522d" stroke-width="1" opacity="0.2"/></svg>');
            background-size: 300px;
            animation: drift 20s linear infinite;
        }

        @keyframes drift {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .boho-frame {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .boho-frame::before,
        .boho-frame::after {
            content: '🌿';
            position: absolute;
            font-size: 60px;
            opacity: 0.2;
            animation: sway 8s ease-in-out infinite;
        }

        .boho-frame::before {
            top: 5%;
            left: 3%;
            transform: rotate(-20deg);
        }

        .boho-frame::after {
            bottom: 5%;
            right: 3%;
            transform: rotate(20deg);
            animation-delay: 4s;
        }

        @keyframes sway {
            0%, 100% { transform: rotate(-20deg) translateY(0); }
            50% { transform: rotate(-10deg) translateY(-10px); }
        }

        .hero-content {
            text-align: center;
            z-index: 1;
            padding: 3rem;
            background: rgba(245, 241, 232, 0.95);
            border-radius: 2px;
            box-shadow: 0 10px 40px rgba(93, 78, 55, 0.1);
            max-width: 600px;
            margin: 20px;
            border: 1px solid var(--sand);
            position: relative;
        }

        .hero-content::before {
            content: '';
            position: absolute;
            top: 10px;
            left: 10px;
            right: 10px;
            bottom: 10px;
            border: 1px solid var(--terracota);
            opacity: 0.3;
            pointer-events: none;
        }

        .names {
            font-family: 'Amatic SC', cursive;
            font-size: 5rem;
            color: var(--rust);
            margin-bottom: 0.5rem;
            letter-spacing: 2px;
        }

        .ampersand {
            font-family: 'Cormorant Garamond', serif;
            font-size: 3rem;
            color: var(--olive);
            display: block;
            margin: -15px 0;
            font-style: italic;
        }

        .subtitle {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.1rem;
            color: var(--brown);
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-top: 1.5rem;
            font-weight: 300;
        }

        .date-hero {
            font-family: 'Amatic SC', cursive;
            font-size: 2.5rem;
            color: var(--terracota);
            margin-top: 1rem;
        }

        .boho-icon {
            font-size: 2.5rem;
            margin: 1.5rem 0;
            opacity: 0.7;
        }

        /* Quote Section */
        .quote-section {
            background: var(--sand);
            padding: 5rem 2rem;
            text-align: center;
            position: relative;
        }

        .quote-section::before {
            content: '❧';
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2rem;
            color: var(--terracota);
            opacity: 0.5;
        }

        .quote {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2rem;
            font-style: italic;
            color: var(--brown);
            max-width: 700px;
            margin: 0 auto;
            line-height: 1.4;
        }

        .quote-author {
            margin-top: 1.5rem;
            font-family: 'Amatic SC', cursive;
            font-size: 1.5rem;
            color: var(--rust);
        }

        /* Our Story Section */
        .our-story {
            background: linear-gradient(to bottom, var(--sand) 0%, var(--cream) 100%);
            padding: 5rem 2rem;
            position: relative;
        }

        .story-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .story-intro {
            text-align: center;
            margin-bottom: 4rem;
        }

        .story-text {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.3rem;
            line-height: 1.8;
            color: var(--brown);
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
        }

        .story-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .story-card {
            background: white;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(93, 78, 55, 0.08);
            border: 1px solid var(--sand);
            transition: transform 0.3s ease;
        }

        .story-card:hover {
            transform: translateY(-5px);
        }

        .story-image {
            width: 100%;
            aspect-ratio: 1;
            background: linear-gradient(135deg, var(--sand) 0%, var(--cream) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            margin-bottom: 1rem;
            overflow: hidden;
            position: relative;
        }

        .story-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            filter: sepia(20%) saturate(80%);
            transition: filter 0.3s ease;
        }

        .story-card:hover .story-image img {
            filter: sepia(0%) saturate(100%);
        }

        .story-caption {
            font-family: 'Amatic SC', cursive;
            font-size: 1.5rem;
            color: var(--rust);
            text-align: center;
        }

        .story-date {
            font-size: 0.85rem;
            color: var(--olive);
            text-align: center;
            margin-top: 0.5rem;
            letter-spacing: 1px;
        }

        /* Spotify Section */
        .spotify-section {
            background: var(--brown);
            padding: 4rem 2rem;
            text-align: center;
        }

        .spotify-section h2 {
            font-family: 'Amatic SC', cursive;
            font-size: 2.5rem;
            color: var(--sage);
            margin-bottom: 1rem;
        }

        .spotify-section p {
            color: var(--sand);
            margin-bottom: 2rem;
            font-weight: 300;
        }

        .spotify-container {
            max-width: 600px;
            margin: 0 auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        /* Events Section */
        .events {
            background: var(--cream);
            padding: 5rem 2rem;
            position: relative;
        }

        .events::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 100px;
            background: linear-gradient(to bottom, var(--cream), transparent);
        }

        .section-title {
            font-family: 'Amatic SC', cursive;
            font-size: 3.5rem;
            text-align: center;
            color: var(--rust);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '✦';
            display: block;
            font-size: 1.5rem;
            margin-top: 10px;
            color: var(--olive);
        }

        .timeline {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: linear-gradient(to bottom, var(--terracota), var(--sage));
            opacity: 0.3;
        }

        .event-card {
            background: white;
            padding: 2.5rem;
            margin: 2rem auto;
            max-width: 500px;
            box-shadow: 0 5px 20px rgba(93, 78, 55, 0.08);
            border-left: 3px solid var(--terracota);
            position: relative;
            transition: transform 0.3s ease;
        }

        .event-card:hover {
            transform: translateY(-3px);
        }

        .event-card::before {
            content: '•';
            position: absolute;
            left: -30px;
            top: 50%;
            transform: translateY(-50%);
            font-size: 2rem;
            color: var(--terracota);
        }

        .event-time {
            font-family: 'Amatic SC', cursive;
            font-size: 2.5rem;
            color: var(--rust);
            margin-bottom: 0.5rem;
        }

        .event-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.8rem;
            color: var(--brown);
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: 600;
        }

        .event-details {
            color: var(--brown);
            margin-bottom: 1.5rem;
            line-height: 1.8;
            font-weight: 300;
        }

        .event-location {
            font-style: italic;
            color: var(--olive);
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid var(--sand);
        }

        .btn {
            display: inline-block;
            padding: 12px 35px;
            background: transparent;
            color: var(--rust);
            text-decoration: none;
            border: 1px solid var(--rust);
            font-family: 'Montserrat', sans-serif;
            font-weight: 500;
            letter-spacing: 2px;
            transition: all 0.3s ease;
            text-transform: uppercase;
            font-size: 0.85rem;
            cursor: pointer;
        }

        .btn:hover {
            background: var(--rust);
            color: white;
        }

        /* Venue Section */
        .venue {
            background: linear-gradient(to bottom, var(--cream) 0%, var(--sage) 100%);
            padding: 5rem 2rem;
            text-align: center;
        }

        .venue-content {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(93, 78, 55, 0.1);
        }

        .venue-name {
            font-family: 'Amatic SC', cursive;
            font-size: 3rem;
            color: var(--rust);
            margin-bottom: 1rem;
        }

        .venue-description {
            color: var(--brown);
            line-height: 1.8;
            margin-bottom: 2rem;
            font-weight: 300;
        }

        .venue-features {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }

        .feature {
            text-align: center;
            font-size: 2rem;
        }

        .feature span {
            display: block;
            font-size: 0.8rem;
            margin-top: 5px;
            color: var(--brown);
            font-family: 'Montserrat', sans-serif;
        }

        /* Dress Code & Gifts */
        .info-section {
            background: var(--brown);
            color: var(--cream);
            padding: 5rem 2rem;
            text-align: center;
        }

        .dress-code {
            margin-bottom: 4rem;
        }

        .dress-code h3 {
            font-family: 'Amatic SC', cursive;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--sage);
        }

        .dress-code p {
            font-size: 1.2rem;
            color: var(--sand);
            font-weight: 300;
        }

        .dress-inspiration {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .dress-item {
            text-align: center;
        }

        .dress-icon {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .gifts {
            max-width: 900px;
            margin: 0 auto;
        }

        .gifts h3 {
            font-family: 'Amatic SC', cursive;
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--terracota);
        }

        .gift-text {
            font-style: italic;
            margin-bottom: 2rem;
            color: var(--sand);
            font-weight: 300;
        }

        .bank-accounts {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .account-card {
            background: rgba(245, 241, 232, 0.1);
            padding: 2rem;
            border: 1px solid rgba(193, 127, 89, 0.3);
            text-align: left;
        }

        .account-card h4 {
            color: var(--sage);
            margin-bottom: 1rem;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            border-bottom: 1px solid rgba(193, 127, 89, 0.3);
            padding-bottom: 0.5rem;
        }

        .account-details {
            font-size: 0.9rem;
            line-height: 1.8;
            color: var(--cream);
        }

        /* Accommodations */
        .accommodations {
            background: var(--sand);
            padding: 5rem 2rem;
        }

        .accommodations h2 {
            font-family: 'Amatic SC', cursive;
            font-size: 3rem;
            text-align: center;
            color: var(--rust);
            margin-bottom: 3rem;
        }

        .accommodation-info {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            box-shadow: 0 5px 20px rgba(93, 78, 55, 0.08);
        }

        .accommodation-info p {
            margin-bottom: 1.5rem;
            line-height: 1.8;
            color: var(--brown);
        }

        .highlight {
            color: var(--rust);
            font-weight: 500;
        }

        /* Interactive Section */
        .interactive {
            background: var(--cream);
            padding: 5rem 2rem;
            text-align: center;
        }

        .interactive h2 {
            font-family: 'Amatic SC', cursive;
            font-size: 3rem;
            color: var(--rust);
            margin-bottom: 1rem;
        }

        .interactive > p {
            color: var(--brown);
            margin-bottom: 3rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 300;
        }

        .action-buttons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .btn-filled {
            background: var(--rust);
            color: white;
            border: 1px solid var(--rust);
        }

        .btn-filled:hover {
            background: transparent;
            color: var(--rust);
        }

        /* Footer */
        .footer {
            background: var(--brown);
            color: var(--cream);
            text-align: center;
            padding: 4rem 2rem;
            position: relative;
        }

        .footer::before {
            content: '❦';
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2rem;
            color: var(--terracota);
            opacity: 0.5;
        }

        .footer-text {
            font-family: 'Amatic SC', cursive;
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .footer p {
            opacity: 0.9;
            font-weight: 300;
        }

        .footer-names {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.5rem;
            margin-top: 1rem;
            color: var(--sage);
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .names {
                font-size: 3.5rem;
            }
            
            .quote {
                font-size: 1.5rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
            
            .timeline::before {
                left: 20px;
            }
            
            .event-card::before {
                left: -25px;
            }

            .spotify-container iframe {
                height: 300px;
            }
        }

        /* Decorative elements */
        .leaf-divider {
            text-align: center;
            font-size: 1.5rem;
            color: var(--olive);
            margin: 2rem 0;
            opacity: 0.5;
        }
    </style>
</head>
<body>

    <!-- Hero Section -->
    <section class="hero">
        <div class="boho-frame"></div>
        <div class="hero-content">
            <h1 class="names">Diana</h1>
            <span class="ampersand">&</span>
            <h1 class="names">Liz</h1>
            <div class="boho-icon">🌾</div>
            <p class="subtitle">Nos Casamos</p>
            <p class="date-hero">16 de Mayo de 2026</p>
        </div>
    </section>

    <!-- Quote Section -->
    <section class="quote-section">
        <p class="quote">"En el arte del amor, cada día es una obra maestra en construcción"</p>
        <p class="quote-author">— Diana & Liz</p>
    </section>

    <!-- Our Story Section -->
    <section class="our-story">
        <div class="story-container">
            <h2 class="section-title">Nuestra Historia</h2>
            
            <div class="story-intro">
                <p class="story-text">
                    Somos Diana y Liz, dos almas que se encontraron en el camino del arte y el movimiento. 
                    Entre risas, entrenamientos, noches de luces y momentos simples, construimos un amor 
                    natural, libre y profundo. Nos encanta la naturaleza, nuestras mascotas, y compartir 
                    la vida juntas. El 16 de mayo celebramos nuestro compromiso rodeadas de quienes más queremos.
                </p>
            </div>

            <div class="story-grid">
                <div class="story-card fade-in">
                    <div class="story-image">
                        <img src="/mnt/kimi/upload/1000547049.jpg" alt="Diana y Liz en la naturaleza">
                    </div>
                    <h3 class="story-caption">Nuestro Refugio</h3>
                    <p class="story-date">Entre árboles y amor</p>
                </div>

                <div class="story-card fade-in">
                    <div class="story-image">
                        <img src="/mnt/kimi/upload/1000492095.jpg" alt="Noche de luces">
                    </div>
                    <h3 class="story-caption">Luces de Colores</h3>
                    <p class="story-date">Momentos mágicos juntas</p>
                </div>

                <div class="story-card fade-in">
                    <div class="story-image">
                        <img src="/mnt/kimi/upload/1000537879.jpg" alt="Diana y Liz">
                    </div>
                    <h3 class="story-caption">Complicidad</h3>
                    <p class="story-date">Sonrisas que curan</p>
                </div>

                <div class="story-card fade-in">
                    <div class="story-image">
                        <img src="/mnt/kimi/upload/1000544058.jpg" alt="La propuesta">
                    </div>
                    <h3 class="story-caption">La Propuesta</h3>
                    <p class="story-date">Cuando dijimos Sí</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Spotify Playlist Section -->
    <section class="spotify-section">
        <h2>Nuestra Playlist</h2>
        <p>La música que nos une y acompaña nuestra historia</p>
        <div class="spotify-container">
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/1Ac5Pa9WfbiGvTrXLo9UVT?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
    </section>

    <!-- Events Section -->
    <section class="events">
        <h2 class="section-title">El Gran Día</h2>
        
        <div class="timeline">
            <div class="event-card fade-in">
                <div class="event-time">1:00 p.m.</div>
                <h3 class="event-title">Ceremonia</h3>
                <p class="event-details">
                    Unimos nuestras vidas en una ceremonia íntima al aire libre, rodeadas de la naturaleza que tanto amamos.
                </p>
                <p class="event-location">
                    🌿 Jardines de El Ark de Noé<br>
                    <em>Vía Ibagué - Rovira, Km 10</em>
                </p>
                <a href="https://www.google.com/maps/search/El+Ark+de+Noé+Ibagué" target="_blank" class="btn">Cómo Llegar</a>
            </div>

            <div class="event-card fade-in">
                <div class="event-time">2:00 p.m.</div>
                <h3 class="event-title">Celebración & Almuerzo</h3>
                <p class="event-details">
                    Compartiremos un almuerzo en el salón principal, con comida deliciosa, buena música y la compañía de quienes más queremos.
                </p>
                <p class="event-location">
                    🍃 Salón Principal<br>
                    <em>Dress code: Boho Chic / Elegante Natural</em>
                </p>
                <a href="#" class="btn">Confirmar Asistencia</a>
            </div>

            <div class="event-card fade-in">
                <div class="event-time">6:00 p.m.</div>
                <h3 class="event-title">Fiesta & Celebración</h3>
                <p class="event-details">
                    Cuando caiga el sol, la celebración continúa. Baile, risas y momentos inolvidables hasta que el cuerpo aguante.
                </p>
                <p class="event-location">
                    ✨ Bajo las estrellas<br>
                    <em>Zona BBQ y área de fogata</em>
                </p>
                <a href="#" class="btn">Sugerir Canción</a>
            </div>
        </div>
    </section>

    <!-- Venue Section -->
    <section class="venue">
        <div class="venue-content">
            <h2 class="section-title">El Lugar</h2>
            <h3 class="venue-name">El Ark de Noé</h3>
            <p class="venue-description">
                Hemos elegido este paraíso natural cerca de Ibagué para celebrar nuestro amor. 
                Un espacio mágico donde la naturaleza, el lago y la tranquilidad se unen para crear 
                el ambiente perfecto para nuestra boda boho.
            </p>
            <div class="venue-features">
                <div class="feature">
                    🌲
                    <span>Naturaleza</span>
                </div>
                <div class="feature">
                    🏊
                    <span>Piscina</span>
                </div>
                <div class="feature">
                    🦆
                    <span>Lago</span>
                </div>
                <div class="feature">
                    🔥
                    <span>Fogata</span>
                </div>
                <div class="feature">
                    🌙
                    <span>Noche</span>
                </div>
            </div>
            <p style="margin-top: 2rem; font-style: italic; color: var(--olive);">
                A solo 20 minutos de Ibagué, vía a Rovira (Km 10)
            </p>
        </div>
    </section>

    <!-- Dress Code & Gifts -->
    <section class="info-section">
        <div class="dress-code">
            <h3>Dress Code</h3>
            <p>Boho Chic / Elegante Natural</p>
            <div class="dress-inspiration">
                <div class="dress-item">
                    <div class="dress-icon">🌸</div>
                    <span>Flores silvestres</span>
                </div>
                <div class="dress-item">
                    <div class="dress-icon">👗</div>
                    <span>Telas naturales</span>
                </div>
                <div class="dress-item">
                    <div class="dress-icon">👢</div>
                    <span>Zapato cómodo</span>
                </div>
            </div>
            <p style="margin-top: 2rem; font-size: 1rem; max-width: 600px; margin-left: auto; margin-right: auto;">
                Colores tierra, beige, terracota, verde oliva, marfil. Evita tacones altos (será en jardín). 
                ¡Ven cómodo para disfrutar al máximo!
            </p>
        </div>

        <div class="gifts">
            <p class="gift-text">Su presencia es nuestro mayor regalo. Si desean hacernos un obsequio...</p>
            <h3>Lluvia de Sobres / Datos Bancarios</h3>
            
            <div class="bank-accounts">
                <div class="account-card">
                    <h4>Cuenta de Ahorros</h4>
                    <div class="account-details">
                        <strong>Titular:</strong> Diana Naranjo<br>
                        <strong>Banco:</strong> [Por confirmar]<br>
                        <strong>Cuenta:</strong> [Número]<br>
                        <strong>Cédula:</strong> [Número]
                    </div>
                </div>
                
                <div class="account-card">
                    <h4>Cuenta de Ahorros</h4>
                    <div class="account-details">
                        <strong>Titular:</strong> Liz [Apellido]<br>
                        <strong>Banco:</strong> [Por confirmar]<br>
                        <strong>Cuenta:</strong> [Número]<br>
                        <strong>Cédula:</strong> [Número]
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Accommodations -->
    <section class="accommodations">
        <h2>Hospedaje</h2>
        <div class="accommodation-info">
            <p>
                <span class="highlight">El Ark de Noé</span> cuenta con alojamiento para aproximadamente 
                <strong>20 personas</strong> en la casa principal (camas y espacio para carpas/colchonetas).
            </p>
            <p>
                Para los primeros 15 invitados que confirmen, tenemos reservadas habitaciones 
                la noche del sábado 16 de mayo.
            </p>
            <p>
                <strong>También recomendamos:</strong><br>
                Hoteles en Ibagué (20 minutos en carro) para quienes prefieran regresar a la ciudad.
            </p>
            <div style="margin-top: 2rem;">
                <a href="#" class="btn">Solicitar Hospedaje</a>
            </div>
        </div>
    </section>

    <!-- Interactive Section -->
    <section class="interactive">
        <h2>¡Celebremos Juntos!</h2>
        <p>Queremos que este día sea inolvidable. Ayúdanos a hacerlo realidad.</p>
        
        <div class="action-buttons">
            <a href="#" class="btn btn-filled">Confirmar Asistencia</a>
            <a href="#" class="btn">Sugerir Canción</a>
            <a href="#" class="btn">Compartir Fotos</a>
        </div>

        <div class="leaf-divider">❧ ❧ ❧</div>

        <div style="margin-top: 2rem;">
            <h3 style="color: var(--rust); margin-bottom: 1rem; font-family: 'Amatic SC', cursive; font-size: 2rem;">
                Información Importante
            </h3>
            <p style="color: var(--brown); max-width: 600px; margin: 0 auto; line-height: 1.8;">
                <strong>Invitados:</strong> 50 personas<br>
                <strong>Fecha límite confirmación:</strong> [Fecha]<br>
                <strong>Contacto:</strong> diana.naranjo@somosartenmovimiento.com<br>
                <strong>Teléfono:</strong> [Número de contacto]
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p class="footer-text">¡Gracias por ser parte de nuestra historia!</p>
        <p>Con amor y gratitud</p>
        <p class="footer-names">Diana & Liz</p>
        <p style="margin-top: 2rem; font-size: 0.9rem; opacity: 0.8;">
            16 de Mayo de 2026 · El Ark de Noé · Ibagué
        </p>
    </footer>

    <script>
        // Scroll animation
        const observerOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -50px 0px"
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach((el) => observer.observe(el));

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>

</body>
</html>
