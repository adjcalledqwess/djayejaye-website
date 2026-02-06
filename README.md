<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DJ Aye Jaye - Future Levels | Producer | Mobile DJ | Artist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #ff1493;
            --secondary: #00d4ff;
            --accent: #9d4edd;
            --dark: #0a0a0a;
            --gray: #1a1a1a;
            --light-gray: #2a2a2a;
            --text: #ffffff;
            --text-muted: #aaaaaa;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--dark);
            color: var(--text);
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.98);
            backdrop-filter: blur(10px);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 2px solid rgba(255, 20, 147, 0.3);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo img {
            height: 50px;
            width: auto;
        }

        .logo-text {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            transition: all 0.3s;
            font-weight: 500;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .mobile-menu {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
        }

        .mobile-menu span {
            width: 25px;
            height: 3px;
            background: var(--primary);
            transition: 0.3s;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a0520 50%, #0a0a0a 100%);
            padding: 2rem 5%;
        }

        .hero-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.15;
            background-image: url('E_ABC08007.jpg');
            background-size: cover;
            background-position: center;
            filter: blur(3px);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            max-width: 1200px;
        }

        .hero-logo {
            width: 300px;
            max-width: 80%;
            margin-bottom: 2rem;
            filter: drop-shadow(0 0 30px rgba(255, 20, 147, 0.6));
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 2s ease-in-out infinite alternate;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        @keyframes glow {
            from {
                filter: drop-shadow(0 0 20px rgba(255, 20, 147, 0.5));
            }
            to {
                filter: drop-shadow(0 0 40px rgba(0, 212, 255, 0.5));
            }
        }

        .hero h2 {
            font-size: 1.8rem;
            color: var(--text-muted);
            margin-bottom: 1.5rem;
            font-weight: 300;
        }

        .hero p {
            max-width: 700px;
            margin: 0 auto 2rem;
            color: var(--text-muted);
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border: 2px solid var(--primary);
            background: transparent;
            color: var(--text);
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn:hover {
            background: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255, 20, 147, 0.5);
        }

        .btn-secondary {
            border-color: var(--secondary);
        }

        .btn-secondary:hover {
            background: var(--secondary);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.5);
        }

        /* Stats Section */
        .stats-section {
            background: var(--gray);
            padding: 4rem 5%;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .stat-item {
            padding: 2rem;
            background: rgba(255, 20, 147, 0.05);
            border: 1px solid rgba(255, 20, 147, 0.2);
            transition: all 0.3s;
        }

        .stat-item:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
            box-shadow: 0 10px 30px rgba(255, 20, 147, 0.2);
        }

        .stat-number {
            font-size: 3rem;
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: var(--text-muted);
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        /* Sections */
        section {
            padding: 5rem 5%;
            position: relative;
        }

        .section-title {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .service-card {
            background: var(--gray);
            padding: 2.5rem;
            border: 1px solid var(--light-gray);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            transition: left 0.3s;
        }

        .service-card:hover::before {
            left: 0;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary);
            box-shadow: 0 20px 40px rgba(255, 20, 147, 0.3);
        }

        .service-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .service-card p {
            color: var(--text-muted);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .service-card ul {
            list-style: none;
            color: var(--text-muted);
            line-height: 2;
        }

        .service-card ul li {
            padding-left: 1.5rem;
            position: relative;
        }

        .service-card ul li::before {
            content: '▶';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-size: 0.8rem;
        }

        /* Gallery Section */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .gallery-item {
            height: 350px;
            position: relative;
            overflow: hidden;
            cursor: pointer;
            border: 2px solid transparent;
            transition: all 0.3s;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.6), rgba(0, 212, 255, 0.6));
            opacity: 0;
            transition: opacity 0.3s;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        .gallery-item:hover {
            border-color: var(--primary);
        }

        /* About Section */
        .about-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .about-image {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            margin: 0 auto 2rem;
            display: block;
            border: 5px solid var(--primary);
            box-shadow: 0 20px 60px rgba(255, 20, 147, 0.4);
        }

        .about-content h3 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .about-content p {
            color: var(--text-muted);
            line-height: 2;
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        /* Music Section */
        .music-player {
            background: var(--gray);
            padding: 3rem;
            border: 2px solid var(--primary);
            max-width: 900px;
            margin: 0 auto;
            box-shadow: 0 20px 60px rgba(255, 20, 147, 0.3);
        }

        .music-player h3 {
            font-size: 2rem;
            margin-bottom: 2rem;
            text-align: center;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .track-list {
            list-style: none;
        }

        .track-item {
            padding: 1.5rem;
            margin-bottom: 1rem;
            background: var(--light-gray);
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s;
            border-left: 3px solid transparent;
        }

        .track-item:hover {
            background: rgba(255, 20, 147, 0.1);
            border-left-color: var(--primary);
            transform: translateX(5px);
        }

        .track-info {
            display: flex;
            gap: 1.5rem;
            align-items: center;
        }

        .play-btn {
            width: 50px;
            height: 50px;
            border: 2px solid var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 1.2rem;
        }

        .play-btn:hover {
            background: var(--primary);
            transform: scale(1.1);
        }

        .track-name {
            font-weight: bold;
            font-size: 1.1rem;
        }

        .track-status {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 0.3rem;
        }

        /* Contact Form */
        .contact-form {
            max-width: 700px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.7rem;
            color: var(--text);
            font-weight: 500;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 1rem;
            background: var(--gray);
            border: 2px solid var(--light-gray);
            color: var(--text);
            font-size: 1rem;
            transition: all 0.3s;
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 20px rgba(255, 20, 147, 0.2);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 150px;
        }

        /* Footer */
        footer {
            background: var(--gray);
            padding: 4rem 5%;
            text-align: center;
            border-top: 2px solid var(--primary);
        }

        .footer-logo {
            width: 150px;
            margin-bottom: 2rem;
        }

        .social-links {
            display: flex;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--text);
            font-size: 1.8rem;
            transition: all 0.3s;
        }

        .social-links a:hover {
            color: var(--primary);
            transform: translateY(-5px);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu {
                display: flex;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h2 {
                font-size: 1.3rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .gallery {
                grid-template-columns: 1fr;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s, transform 0.8s;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="logo">
            <img src="DJAYEJAYE_PINK.PNG" alt="DJ Aye Jaye Logo" style="height: 60px;">
        </div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#music">Music</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Book Now</a></li>
        </ul>
        <div class="mobile-menu">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-background"></div>
        <div class="hero-content">
            <img src="DJAYEJAYE_PINK.PNG" alt="DJ Aye Jaye" class="hero-logo">
            <h2>Producer | Mobile DJ | Touring Artist</h2>
            <p>
                16-year-old nationally traveling DJ bringing next-level energy to every stage. 
                From major sports events to intimate celebrations, delivering unforgettable experiences 
                through music and production excellence.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn">Book an Event</a>
                <a href="#music" class="btn btn-secondary">Listen to Music</a>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats-section">
        <div class="stats fade-in">
            <div class="stat-item">
                <div class="stat-number">150+</div>
                <div class="stat-label">Events Performed</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">50+</div>
                <div class="stat-label">Cities Traveled</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">1000+</div>
                <div class="stat-label">Happy Clients</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">6+</div>
                <div class="stat-label">Years Experience</div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2 class="section-title">Services</h2>
        <div class="services-grid fade-in">
            <div class="service-card">
                <h3>🎬 Future Levels Productions</h3>
                <p>
                    Full-service event production for corporate events, conferences, and large-scale gatherings. 
                    Professional sound, lighting, and technical production to elevate your event to the next level.
                </p>
                <ul>
                    <li>Corporate Events & Conferences</li>
                    <li>Sports Events & Halftime Shows</li>
                    <li>Festival Production</li>
                    <li>Professional Sound & Lighting</li>
                    <li>Complete Technical Setup</li>
                </ul>
            </div>
            <div class="service-card">
                <h3>🎧 Mobile DJ Services</h3>
                <p>
                    Professional DJ services for weddings, private parties, school events, and special celebrations. 
                    Custom music curation and MC services to keep your guests entertained all night long.
                </p>
                <ul>
                    <li>Weddings & Receptions</li>
                    <li>Private Parties & Celebrations</li>
                    <li>School Dances & Youth Events</li>
                    <li>Birthday Celebrations</li>
                    <li>Community Events</li>
                </ul>
            </div>
            <div class="service-card">
                <h3>🎵 Artist & Live Performer</h3>
                <p>
                    Original music production and high-energy live performances. Nationally traveling artist 
                    bringing unique sound and infectious energy to clubs, festivals, and special events nationwide.
                </p>
                <ul>
                    <li>Club & Venue Performances</li>
                    <li>Festival Sets & Tours</li>
                    <li>Original Music Production</li>
                    <li>Touring Artist Bookings</li>
                    <li>Special Event Headliner</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" style="background: var(--gray);">
        <h2 class="section-title">Performance Gallery</h2>
        <div class="gallery fade-in">
            <div class="gallery-item">
                <img src="E_A7406981.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="E_A7407050.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="E_ABC08007.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_1834.jpg" alt="DJ Aye Jaye Studio">
            </div>
            <div class="gallery-item">
                <img src="IMG_1836.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_3774.jpg" alt="DJ Aye Jaye Event">
            </div>
            <div class="gallery-item">
                <img src="IMG_9971.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_9976.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_9977.jpg" alt="DJ Aye Jaye Event">
            </div>
            <div class="gallery-item">
                <img src="IMG_9978.jpg" alt="DJ Aye Jaye Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_9979.jpg" alt="DJ Aye Jaye Dodgers Event">
            </div>
            <div class="gallery-item">
                <img src="IMG_9980.jpg" alt="DJ Aye Jaye Baseball Event">
            </div>
            <div class="gallery-item">
                <img src="IMG_9982.jpg" alt="DJ Aye Jaye Stadium Performance">
            </div>
            <div class="gallery-item">
                <img src="IMG_9983.jpg" alt="DJ Aye Jaye with Pro Athlete">
            </div>
            <div class="gallery-item">
                <img src="IMG_3650.jpg" alt="DJ Aye Jaye">
            </div>
            <div class="gallery-item">
                <img src="IMG_4155.jpg" alt="DJ Aye Jaye Performance">
            </div>
        </div>
    </section>

    <!-- Music Section -->
    <section id="music">
        <h2 class="section-title">Music & Releases</h2>
        <div class="music-player fade-in">
            <h3>Coming Soon - New Releases</h3>
            <ul class="track-list">
                <li class="track-item">
                    <div class="track-info">
                        <div class="play-btn">▶</div>
                        <div>
                            <div class="track-name">Summer Vibes (Original Mix)</div>
                            <div class="track-status">Coming Soon 2026</div>
                        </div>
                    </div>
                    <div style="color: var(--text-muted);">3:45</div>
                </li>
                <li class="track-item">
                    <div class="track-info">
                        <div class="play-btn">▶</div>
                        <div>
                            <div class="track-name">Night Drive Remix</div>
                            <div class="track-status">Coming Soon 2026</div>
                        </div>
                    </div>
                    <div style="color: var(--text-muted);">4:12</div>
                </li>
                <li class="track-item">
                    <div class="track-info">
                        <div class="play-btn">▶</div>
                        <div>
                            <div class="track-name">Festival Anthem 2026</div>
                            <div class="track-status">Coming Soon 2026</div>
                        </div>
                    </div>
                    <div style="color: var(--text-muted);">3:28</div>
                </li>
                <li class="track-item">
                    <div class="track-info">
                        <div class="play-btn">▶</div>
                        <div>
                            <div class="track-name">Future Levels (Signature Track)</div>
                            <div class="track-status">Coming Soon 2026</div>
                        </div>
                    </div>
                    <div style="color: var(--text-muted);">3:55</div>
                </li>
            </ul>
            <p style="text-align: center; margin-top: 2rem; color: var(--text-muted); font-size: 1.1rem;">
                🎵 New original music dropping soon! Follow on social media for exclusive previews and release updates.
            </p>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" style="background: var(--gray);">
        <h2 class="section-title">About DJ Aye Jaye</h2>
        <div class="about-content fade-in">
            <img src="IMG_3667.jpg" alt="DJ Aye Jaye" class="about-image">
            <h3>Future Levels</h3>
            <p>
                At just 16 years old, DJ Aye Jaye has already traveled across the nation, bringing passion, 
                energy, and professionalism to every performance. What started as a love for music and mixing 
                has evolved into Future Levels - a complete production company and mobile DJ service that 
                delivers exceptional experiences.
            </p>
            <p>
                From performing at major sporting events like Mamba Mambacita Foundation events to weddings, 
                school dances, and community celebrations, DJ Aye Jaye specializes in reading the crowd and 
                creating unforgettable moments. With professional equipment, technical expertise, and an 
                infectious love for music, every event gets the Future Levels treatment.
            </p>
            <p>
                Currently working on original music releases to share a unique sound with the world. Whether 
                it's a corporate production, intimate wedding, or high-energy festival set, DJ Aye Jaye brings 
                the same dedication, professionalism, and passion to every performance. The future is here, 
                and it's time to take your event to the next level.
            </p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Book Your Event</h2>
        <form class="contact-form fade-in">
            <div class="form-group">
                <label for="name">Name *</label>
                <input type="text" id="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email *</label>
                <input type="email" id="email" required>
            </div>
            <div class="form-group">
                <label for="phone">Phone Number</label>
                <input type="tel" id="phone">
            </div>
            <div class="form-group">
                <label for="service">Service Type *</label>
                <select id="service" required>
                    <option value="">Select a service...</option>
                    <option value="production">Future Levels Production</option>
                    <option value="mobile">Mobile DJ Service</option>
                    <option value="artist">Artist Performance</option>
                    <option value="wedding">Wedding DJ</option>
                    <option value="corporate">Corporate Event</option>
                    <option value="other">Other</option>
                </select>
            </div>
            <div class="form-group">
                <label for="date">Event Date</label>
                <input type="date" id="date">
            </div>
            <div class="form-group">
                <label for="message">Event Details & Special Requests *</label>
                <textarea id="message" required placeholder="Tell us about your event, expected attendance, venue details, and any special requests..."></textarea>
            </div>
            <button type="submit" class="btn" style="width: 100%;">Send Booking Inquiry</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <img src="DJAYEJAYE_PINK.PNG" alt="DJ Aye Jaye" class="footer-logo" style="width: 200px;">
        <div class="social-links">
            <a href="#" title="Instagram">📷</a>
            <a href="#" title="TikTok">🎵</a>
            <a href="#" title="YouTube">📺</a>
            <a href="#" title="SoundCloud">🔊</a>
            <a href="#" title="Spotify">🎧</a>
        </div>
        <p style="color: var(--text-muted); font-size: 1.1rem;">
            <strong>DJ AYE JAYE | FUTURE LEVELS</strong>
        </p>
        <p style="color: var(--text-muted); margin-top: 0.5rem;">
            Professional DJ Services | Production Company | Touring Artist
        </p>
        <p style="color: var(--text-muted); margin-top: 1rem; font-size: 0.9rem;">
            © 2026 DJ Aye Jaye / Future Levels. All rights reserved.
        </p>
    </footer>

    <script>
        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Form submission
        document.querySelector('.contact-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your booking inquiry! We will get back to you within 24 hours to discuss your event.');
            e.target.reset();
        });

        // Track player interaction
        document.querySelectorAll('.track-item').forEach(track => {
            track.addEventListener('click', function() {
                const trackName = this.querySelector('.track-name').textContent;
                alert(`"${trackName}" - Coming Soon! Follow DJ Aye Jaye on social media for release updates and exclusive previews.`);
            });
        });

        // Mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            if (navLinks.style.display === 'flex') {
                navLinks.style.display = 'none';
            } else {
                navLinks.style.display = 'flex';
                navLinks.style.flexDirection = 'column';
                navLinks.style.position = 'absolute';
                navLinks.style.top = '100%';
                navLinks.style.right = '0';
                navLinks.style.background = 'rgba(10, 10, 10, 0.98)';
                navLinks.style.padding = '2rem';
                navLinks.style.borderTop = '2px solid var(--primary)';
            }
        });
    </script>
</body>
</html>djayejaye-website-V1
