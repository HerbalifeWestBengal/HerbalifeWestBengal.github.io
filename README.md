<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Herbalife West Bengal - Nutrition for a Better Life</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #ff6b35 0%, #f7931e 100%);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: opacity 0.3s;
        }

        .nav-links a:hover {
            opacity: 0.8;
        }

        .cta-button {
            background: white;
            color: #ff6b35;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s;
        }

        .cta-button:hover {
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23ff6b35" width="1200" height="600"/><text x="50%" y="50%" font-family="Arial" font-size="60" fill="white" text-anchor="middle" dy=".3em">Healthy Lifestyle Background</text></svg>');
            background-size: cover;
            background-position: center;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 600px;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .btn-primary, .btn-secondary {
            padding: 1rem 2rem;
            border-radius: 30px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn-primary {
            background: #ff6b35;
            color: white;
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-primary:hover, .btn-secondary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        /* Sections */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        /* Products Section */
        .products {
            background: #f8f9fa;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
        }

        .product-card img {
            width: 100px;
            height: 100px;
            margin-bottom: 1rem;
        }

        .product-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #ff6b35;
        }

        /* Why Choose Us */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature {
            text-align: center;
            padding: 2rem;
        }

        .feature i {
            font-size: 3rem;
            color: #ff6b35;
            margin-bottom: 1rem;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, #ff6b35 0%, #f7931e 100%);
            color: white;
            text-align: center;
        }

        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 10px;
            font-family: inherit;
        }

        .form-group button {
            width: 100%;
            padding: 1rem;
            background: white;
            color: #ff6b35;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
        }

        .form-group button:hover {
            background: #f0f0f0;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
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

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .section {
                padding: 3rem 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <a href="#" class="logo">Herbalife West Bengal</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#contact" class="cta-button">Get Started</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Nutrition for a Better Life</h1>
            <p>Join thousands of people in West Bengal who are transforming their health with Herbalife's world-class nutrition products and coaching.</p>
            <div class="hero-buttons">
                <a href="#products" class="btn-primary">Explore Products</a>
                <a href="#contact" class="btn-secondary">Start Your Journey</a>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="section products" id="products">
        <h2 class="section-title">Our Premium Products</h2>
        <div class="products-grid">
            <div class="product-card">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect fill='%23ff6b35' width='100' height='100' rx='10'/><text x='50%' y='50%' font-family='Arial' font-size='12' fill='white' text-anchor='middle' dy='.3em'>Formula 1</text></svg>" alt="Formula 1">
                <h3>Formula 1</h3>
                <p>Meal replacement shake packed with protein, vitamins, and minerals for weight management.</p>
            </div>
            <div class="product-card">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect fill='%23f7931e' width='100' height='100' rx='10'/><text x='50%' y='50%' font-family='Arial' font-size='12' fill='white' text-anchor='middle' dy='.3em'>Protein Drink</text></svg>" alt="Protein Drink">
                <h3>Protein Drink Mix</h3>
                <p>High-quality protein supplement to support muscle recovery and growth.</p>
            </div>
            <div class="product-card">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><rect fill='%2333d9b2' width='100' height='100' rx='10'/><text x='50%' y='50%' font-family='Arial' font-size='12' fill='white' text-anchor='middle' dy='.3em'>Tea</text></svg>" alt="Herbal Tea">
                <h3>Herbal Tea Concentrate</h3>
                <p>Delicious tea that boosts metabolism and provides natural energy.</p>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section" id="about">
        <h2 class="section-title">Why Choose Herbalife West Bengal?</h2>
        <div class="features">
            <div class="feature">
                <i class="fas fa-shipping-fast"></i>
                <h3>Fast Delivery</h3>
                <p>Doorstep delivery across West Bengal within 2-3 days.</p>
            </div>
            <div class="feature">
                <i class="fas fa-users"></i>
                <h3>Expert Coaching</h3>
                <p>Personalized nutrition coaching from certified distributors.</p>
            </div>
            <div class="feature">
                <i class="fas fa-award"></i>
                <h3>Proven Results</h3>
                <p>Backed by science with millions of success stories worldwide.</p>
            </div>
            <div class="feature">
                <i class="fas fa-phone"></i>
                <h3>24/7 Support</h3>
                <p>Round-the-clock customer support and guidance.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <h2 class="section-title">Ready to Transform Your Health?</h2>
        <div class="contact-content">
            <div>
                <h3>Get In Touch</h3>
                <p><i class="fas fa-phone"></i> +91 98300 12345</p>
                <p><i class="fas fa-envelope"></i> info@herbalifewb.com</p>
                <p><i class="fas fa-map-marker-alt"></i> West Bengal, India</p>
            </div>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <input type="text" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="tel" placeholder="Phone Number" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Email Address" required>
                    </div>
                    <div class="form-group">
                        <textarea rows="4" placeholder="Tell us about your goals..."></textarea>
                    </div>
                    <button type="submit">Start My Journey</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Herbalife West Bengal. All rights reserved. | Nutrition for a Better Life</p>
    </footer>

    <script>
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
            });
        });

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you! We will contact you soon to start your Herbalife journey!');
        });

        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 107, 53, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'linear-gradient(135deg, #ff6b35 0%, #f7931e 100%)';
                header.style.backdropFilter = 'none';
            }
        });
    </script>
</body>
</html>
