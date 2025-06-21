<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WebCraft Studio | Affordable Websites & Mini Games</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #4a6de5;
            --secondary: #ff6b6b;
            --dark: #2d3436;
            --light: #f9f9f9;
            --accent: #00cec9;
        }

        body {
            background-color: #f5f7ff;
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), #6c5ce7);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo i {
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            padding: 5px 10px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        nav a:hover {
            background: rgba(255,255,255,0.2);
        }

        .cta-button {
            background: var(--secondary);
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-block;
            margin-top: 20px;
            border: none;
            cursor: pointer;
        }

        .cta-button:hover {
            background: #ff5252;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255,107,107,0.4);
        }

        /* Hero Section */
        .hero {
            padding: 5rem 0;
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), 
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%234a6de5" fill-opacity="0.05"/></svg>');
            background-size: 20px 20px;
        }

        .hero-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            color: #555;
        }

        .highlight {
            color: var(--secondary);
            font-weight: 700;
        }

        /* Services Section */
        .services {
            padding: 5rem 0;
            background: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--dark);
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .service-card {
            background: var(--light);
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .service-card i {
            font-size: 3.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .service-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .service-card p {
            color: #666;
            margin-bottom: 1.5rem;
        }

        .price-tag {
            background: var(--accent);
            color: white;
            font-weight: 700;
            font-size: 1.5rem;
            padding: 5px 15px;
            border-radius: 20px;
            display: inline-block;
            margin-top: 10px;
        }

        /* Games Section */
        .games {
            padding: 5rem 0;
            background: #f0f5ff;
        }

        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .game-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }

        .game-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .game-img {
            height: 200px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 5rem;
        }

        .game-info {
            padding: 1.5rem;
        }

        .game-info h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .game-info p {
            color: #666;
            margin-bottom: 1rem;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 0;
            background: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .contact-info {
            padding: 2rem;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--dark);
        }

        .contact-detail {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 1.5rem;
        }

        .contact-detail i {
            font-size: 1.5rem;
            color: var(--primary);
            width: 50px;
            height: 50px;
            background: rgba(74, 109, 229, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .contact-form {
            background: var(--light);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(74, 109, 229, 0.2);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-col h4 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
        }

        .footer-col h4::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--accent);
        }

        .footer-col p {
            color: #bbb;
            margin-bottom: 1rem;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #bbb;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
        }

        @media (max-width: 480px) {
            nav ul {
                gap: 0.5rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .service-card, .game-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-code"></i>
                <span>WebCraft Studio</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#games">Our Games</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Professional Websites & Mini Games</h1>
                <p>We create stunning websites for just <span class="highlight">1 BGN</span> and develop engaging mini games that captivate your audience!</p>
                <a href="#services" class="cta-button">Explore Our Services</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>Affordable solutions for your digital needs</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-globe"></i>
                    <h3>Website Creation</h3>
                    <p>Get a professional, responsive website tailored to your business needs. We create modern designs that work perfectly on all devices.</p>
                    <div class="price-tag">Only 1 BGN</div>
                </div>
                
                <div class="service-card">
                    <i class="fas fa-gamepad"></i>
                    <h3>Mini Game Development</h3>
                    <p>Engage your audience with custom mini games. We create fun, interactive experiences that keep visitors coming back.</p>
                    <a href="#contact" class="cta-button">Get A Quote</a>
                </div>
                
                <div class="service-card">
                    <i class="fas fa-sync-alt"></i>
                    <h3>Website Maintenance</h3>
                    <p>Keep your website running smoothly with our maintenance packages. We handle updates, security, and content changes.</p>
                    <a href="#contact" class="cta-button">Learn More</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Games Section -->
    <section class="games" id="games">
        <div class="container">
            <div class="section-title">
                <h2>Our Mini Games</h2>
                <p>Check out some of our engaging creations</p>
            </div>
            
            <div class="games-grid">
                <div class="game-card">
                    <div class="game-img">
                        <i class="fas fa-dice"></i>
                    </div>
                    <div class="game-info">
                        <h3>Lucky Dice</h3>
                        <p>A fun dice rolling game with leaderboards and achievements.</p>
                        <a href="#" class="cta-button">Play Now</a>
                    </div>
                </div>
                
                <div class="game-card">
                    <div class="game-img">
                        <i class="fas fa-puzzle-piece"></i>
                    </div>
                    <div class="game-info">
                        <h3>Puzzle Master</h3>
                        <p>Challenge your brain with our addictive puzzle game.</p>
                        <a href="#" class="cta-button">Play Now</a>
                    </div>
                </div>
                
                <div class="game-card">
                    <div class="game-img">
                        <i class="fas fa-running"></i>
                    </div>
                    <div class="game-info">
                        <h3>Endless Runner</h3>
                        <p>Run, jump, and dodge obstacles in this fast-paced game.</p>
                        <a href="#" class="cta-button">Play Now</a>
                    </div>
                </div>
                
                <div class="game-card">
                    <div class="game-img">
                        <i class="fas fa-chess"></i>
                    </div>
                    <div class="game-info">
                        <h3>Chess Challenge</h3>
                        <p>Test your strategy skills against our smart AI opponent.</p>
                        <a href="#" class="cta-button">Play Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch for a free consultation</p>
            </div>
                            <h4>Email</h4>
                            <p>info@webcraftstudio.com</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" placeholder="Your Name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" placeholder="Your Email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="service">Service Interested In</label>
                            <select id="service" class="form-control">
                                <option value="website">Website Creation (1 BGN)</option>
                                <option value="game">Mini Game Development</option>
                                <option value="maintenance">Website Maintenance</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" rows="5" placeholder="Tell us about your project"></textarea>
                        </div>
                        
                        <button type="submit" class="cta-button">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h4>WebCraft Studio</h4>
                    <p>Creating affordable, high-quality websites and engaging mini games for businesses and individuals.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h4>Services</h4>
                    <ul>
                        <li><a href="#">Website Creation (1 BGN)</a></li>
                        <li><a href="#">Mini Game Development</a></li>
                        <li><a href="#">Website Maintenance</a></li>
                        <li><a href="#">E-commerce Solutions</a></li>
                        <li><a href="#">SEO Optimization</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#games">Our Games</a></li>
                        <li><a href="#contact">Contact</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 WebCraft Studio. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Form submission handling
        const contactForm = document.querySelector('.contact-form form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Get form values
                const name = document.getElementById('name').value;
                const service = document.getElementById('service').value;
                
                // Show success message
                alert(`Thank you ${name}! We've received your inquiry about ${service}. We'll contact you shortly.`);
                
                // Reset form
                this.reset();
            });
        }
    </script>
</body>
</html>
