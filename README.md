**# **ali_turan****<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ali TURAN - Web Tasarımcısı</title>
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

        /* Header & Navigation */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
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

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 120px 0 80px;
            text-align: center;
            color: white;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .cta-button {
            display: inline-block;
            background: #fff;
            color: #667eea;
            padding: 15px 35px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .section-white {
            background: white;
        }

        .section-gray {
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .about-image {
            text-align: center;
        }

        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
            margin: 0 auto;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
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
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #333;
        }

        /* Portfolio Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .portfolio-item {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .portfolio-item:hover {
            transform: translateY(-5px);
        }

        .portfolio-img {
            height: 200px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
        }

        .portfolio-content {
            padding: 1.5rem;
        }

        .portfolio-content h3 {
            margin-bottom: 0.5rem;
            color: #333;
        }

        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: start;
        }

        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: #333;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e1e5e9;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
        }

        .submit-btn {
            background: #667eea;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .submit-btn:hover {
            background: #5a6fd8;
        }

        .contact-info {
            padding: 2rem;
        }

        .contact-info h3 {
            margin-bottom: 1.5rem;
            color: #333;
        }

        .contact-item {
            margin-bottom: 1rem;
            font-size: 1.1rem;
        }

        .contact-item i {
            margin-right: 0.5rem;
            color: #667eea;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                padding: 1rem;
                box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .contact-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .profile-img {
                width: 250px;
                height: 250px;
                font-size: 3rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .cta-button {
                padding: 12px 25px;
            }

            .profile-img {
                width: 200px;
                height: 200px;
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="container">
            <a href="#" class="logo">Ali TURAN</a>
            <ul class="nav-links">
                <li><a href="#home">Ana Sayfa</a></li>
                <li><a href="#about">Hakkımda</a></li>
                <li><a href="#services">Hizmetler</a></li>
                <li><a href="#portfolio">Portfolyo</a></li>
                <li><a href="#contact">İletişim</a></li>
            </ul>
            <button class="menu-toggle">☰</button>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1>Ali TURAN</h1>
            <p>Profesyonel Web Tasarımcısı</p>
            <a href="#contact" class="cta-button">Benimle İletişime Geçin</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section-white">
        <div class="container">
            <h2 class="section-title">Hakkımda</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Merhaba! Ben Ali TURAN, modern ve kullanıcı dostu web siteleri tasarlayan profesyonel bir web tasarımcısıyım. Her projede müşteri memnuniyetini ön planda tutarak, işletmenizin dijital dünyada güçlü bir varlık oluşturmasına yardımcı oluyorum.</p>
                    <br>
                    <p>Responsive tasarım, SEO optimizasyonu ve kullanıcı deneyimi konularında uzmanlaşmış olarak, her türlü web sitesi ihtiyacınıza çözüm sunuyorum. Teknolojinin hızla gelişen dünyasında kendimi sürekli güncel tutarak, en yeni trendleri projelerime yansıtıyorum.</p>
                </div>
                <div class="about-image">
                    <div class="profile-img">
                        <!-- Resim buraya eklenecek -->
                        <span style="font-size: 2rem; color: white;">📸</span>
                        <p style="margin-top: 10px; color: white; font-size: 0.9rem;">profil-foto.jpg<br>buraya gelecek</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section-gray">
        <div class="container">
            <h2 class="section-title">Hizmetlerim</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">💻</div>
                    <h3>Web Tasarımı</h3>
                    <p>Modern, responsive ve kullanıcı dostu web siteleri tasarlıyorum. Her cihazda mükemmel görüntü.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🎨</div>
                    <h3>UI/UX Tasarımı</h3>
                    <p>Kullanıcı deneyimini ön planda tutan, görsel olarak etkileyici arayüz tasarımları.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📱</div>
                    <h3>Mobil Uyumlu</h3>
                    <p>Tüm cihazlarda kusursuz çalışan, mobil öncelikli responsive tasarımlar.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🚀</div>
                    <h3>SEO Optimizasyonu</h3>
                    <p>Arama motorlarında üst sıralarda yer almanız için SEO optimizasyonu.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">⚡</div>
                    <h3>Hızlı Yükleme</h3>
                    <p>Kullanıcı deneyimini artıran, hızlı yüklenen optimized web siteleri.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🔧</div>
                    <h3>Bakım & Destek</h3>
                    <p>Sitenizin sürekli güncel ve güvenli kalması için bakım ve destek hizmetleri.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="section-white">
        <div class="container">
            <h2 class="section-title">Portfolyo</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-img">🏢</div>
                    <div class="portfolio-content">
                        <h3>Kurumsal Web Sitesi</h3>
                        <p>Modern kurumsal kimlik yansıtan, profesyonel web sitesi tasarımı.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">🛍️</div>
                    <div class="portfolio-content">
                        <h3>E-Ticaret Sitesi</h3>
                        <p>Kullanıcı dostu alışveriş deneyimi sunan e-ticaret platformu.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">🍽️</div>
                    <div class="portfolio-content">
                        <h3>Restoran Web Sitesi</h3>
                        <p>Lezzetli tasarım ile müşteri çeken restoran web sitesi.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img">👨‍💼</div>
                    <div class="portfolio-content">
                        <h3>Kişisel Portfolyo</h3>
                        <p>Yetenekleri öne çıkaran, etkileyici kişisel portfolyo sitesi.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section-gray">
        <div class="container">
            <h2 class="section-title">İletişim</h2>
            <div class="contact-content">
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Adınız</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">E-posta</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Konu</label>
                            <input type="text" id="subject" name="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Mesajınız</label>
                            <textarea id="message" name="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Gönder</button>
                    </form>
                </div>
                <div class="contact-info">
                    <h3>Benimle İletişime Geçin</h3>
                    <div class="contact-item">
                        <i>📧</i> ali.turan@email.com
                    </div>
                    <div class="contact-item">
                        <i>📱</i> WhatsApp: +90 542 772 46 99
                    </div>
                    <div class="contact-item">
                        <i>📍</i> İstanbul, Türkiye
                    </div>
                    <div class="contact-item">
                        <i>🌐</i> alituran.github.io
                    </div>
                    <div class="contact-item">
                        <i>📘</i> <a href="https://facebook.com/alituran.webdesign" target="_blank" style="color: #667eea; text-decoration: none;">Facebook</a>
                    </div>
                    <div class="contact-item">
                        <i>🐦</i> <a href="https://twitter.com/alituran_web" target="_blank" style="color: #667eea; text-decoration: none;">Twitter</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Ali TURAN. Tüm hakları saklıdır.</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Smooth scrolling for navigation links
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
                navLinks.classList.remove('active');
            });
        });

        // Contact form submission
        document.querySelector('.contact-form form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Mesajınız gönderildi! En kısa sürede sizinle iletişime geçeceğim.');
            this.reset();
        });
    </script>
</body>
</html>
