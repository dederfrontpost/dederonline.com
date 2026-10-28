<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deder Online - Starter Portal</title>
    <style>
        /* Base Reset & Variables */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        :root {
            --primary: #2E7D32; /* Rich Ethiopian Coffee/Agricultural Green */
            --secondary: #EF6C00; /* Warm Harar Sun Orange */
            --dark: #212121;
            --light: #F5F5F5;
        }

        /* Layout & Navigation */
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        header {
            background-color: white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
            text-decoration: none;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(46, 125, 50, 0.85), rgba(33, 33, 33, 0.9)), url('https://unsplash.com') no-repeat center center/cover;
            color: white;
            padding: 6rem 2rem;
            text-align: center;
        }
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.75rem 2rem;
            text-decoration: none;
            border-radius: 4px;
            font-weight: bold;
            transition: background 0.3s;
        }
        .btn:hover {
            background-color: #e65c00;
        }

        /* Main Content & Features */
        .main-container {
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 2rem;
        }
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: var(--secondary);
            margin: 0.5rem auto 0;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        .card {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            border-top: 4px solid var(--primary);
        }
        .card h3 {
            margin-bottom: 1rem;
            color: var(--primary);
        }

        /* Contact Section Form */
        .contact-section {
            background-color: white;
            padding: 4rem 2rem;
            margin-top: 4rem;
        }
        .form-container {
            max-width: 600px;
            margin: 0 auto;
        }
        .form-group {
            margin-bottom: 1.5rem;
        }
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.75rem 2rem;
            font-size: 1rem;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
        }
        .submit-btn:hover {
            background-color: #235F26;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: auto;
        }

        /* Responsive Breakpoint */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
                gap: 1rem;
            }
            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header>
        <nav class="nav-container">
            <a href="#" class="logo">🌿 Deder Online</a>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#agriculture">Agriculture & Trade</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Showcase Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Welcome to Deder Online Portal</h1>
            <p>Your digital hub for East Hararghe's rich history, world-renowned coffee trade, community initiatives, and regional updates.</p>
            <a href="#contact" class="btn">Connect With Us</a>
        </div>
    </section>

    <!-- Main Features Grid -->
    <main class="main-container">
        <section id="services">
            <h2 class="section-title">Explore Our Community</h2>
            <div class="grid">
                <div class="card">
                    <h3>☕ Harar Coffee Hub</h3>
                    <p>Track local market values, coffee harvesting seasons, and connect directly with local farmers and agricultural cooperatives in the Deder district.</p>
                </div>
                <div class="card">
                    <h3>🤝 Debo System Network</h3>
                    <p>Digitally organizing community mutual-aid structures. Post building projects, community farming assistance requests, or volunteer programs.</p>
                </div>
                <div class="card">
                    <h3>📢 Regional News & Culture</h3>
                    <p>Stay up to date with historical overviews, infrastructure updates, and social events rolling out across the East Hararghe Zone.</p>
                </div>
            </div>
        </section>
    </main>

    <!-- Contact & Feedback Form Section -->
    <section id="contact" class="contact-section">
        <div class="form-container">
            <h2 class="section-title">Get In Touch</h2>
            <form action="#" method="POST" onsubmit="alert('Thank you for your message! This is a starter prototype template demo.'); return false;">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" required placeholder="Enter your full name">
                </div>
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" required placeholder="Enter your email address">
                </div>
                <div class="form-group">
                    <label for="message">Message / Inquiry</label>
                    <textarea id="message" rows="5" required placeholder="How can we help your business or community project?"></textarea>
                </div>
                <button type="submit" class="submit-btn">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Deder Online Hub. Built for Community Connectivity.</p>
    </footer>

</body>
</html>
# dederonline.com