# waleed
all rounder taste with health full food
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Waleed and Burger and Pizza | Fried Chicken & More</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary-red: #E03A3E; /* KFC Red */
            --secondary-white: #FFFFFF;
            --dark-bg: #1A1A1A;
            --light-gray: #F4F4F4;
            --gold-accent: #FFB900;
            --text-dark: #333;
            --text-light: #fff;
            --font-heading: 'Montserrat', sans-serif;
            --font-body: 'Open Sans', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: var(--font-body);
            background-color: var(--secondary-white);
            color: var(--text-dark);
            overflow-x: hidden;
        }

        /* --- TYPOGRAPHY IMPORTS --- */
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700;900&family=Open+Sans:wght@400;600&display=swap');

        /* --- HEADER & NAV --- */
        header {
            background-color: var(--secondary-white);
            padding: 15px 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 24px;
            font-weight: 900;
            color: var(--primary-red);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--text-dark);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 14px;
            text-transform: uppercase;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary-red);
        }

        .cta-btn {
            background-color: var(--primary-red);
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 700;
            font-size: 14px;
            transition: transform 0.3s, background 0.3s;
        }

        .cta-btn:hover {
            background-color: #c22;
            transform: scale(1.05);
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1568901346375-23c9450c58cd?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .hero-content h1 {
            font-family: var(--font-heading);
            font-size: 80px;
            line-height: 1;
            margin-bottom: 20px;
            text-transform: uppercase;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }

        .hero-content h1 span {
            color: var(--primary-red);
            -webkit-text-stroke: 2px white;
        }

        .hero-content p {
            font-size: 20px;
            margin-bottom: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* --- FEATURES / ICONS --- */
        .features {
            display: flex;
            justify-content: space-around;
            padding: 80px 10%;
            background-color: var(--light-gray);
            flex-wrap: wrap;
            gap: 20px;
        }

        .feature-box {
            text-align: center;
            flex: 1;
            min-width: 250px;
        }

        .feature-icon {
            font-size: 40px;
            color: var(--primary-red);
            margin-bottom: 20px;
            background: white;
            width: 80px;
            height: 80px;
            line-height: 80px;
            border-radius: 50%;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .feature-box h3 {
            font-family: var(--font-heading);
            margin-bottom: 10px;
        }

        /* --- MENU SECTION --- */
        .menu-section {
            padding: 80px 10%;
            text-align: center;
        }

        .section-title {
            font-family: var(--font-heading);
            font-size: 40px;
            margin-bottom: 10px;
            color: var(--primary-red);
            text-transform: uppercase;
        }

        .section-subtitle {
            margin-bottom: 50px;
            color: #666;
        }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .menu-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            position: relative;
        }

        .menu-card:hover {
            transform: translateY(-10px);
        }

        .card-image {
            height: 250px;
            width: 100%;
            object-fit: cover;
        }

        .card-content {
            padding: 25px;
            text-align: left;
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .card-title {
            font-family: var(--font-heading);
            font-size: 20px;
            font-weight: 700;
        }

        .price {
            color: var(--primary-red);
            font-weight: 700;
            font-size: 18px;
        }

        .card-desc {
            font-size: 14px;
            color: #666;
            margin-bottom: 20px;
            line-height: 1.5;
        }

        .add-btn {
            width: 100%;
            padding: 12px;
            background-color: var(--dark-bg);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s;
        }

        .add-btn:hover {
            background-color: var(--primary-red);
        }

        /* --- SPECIAL BANNER --- */
        .special-banner {
            background-color: var(--primary-red);
            padding: 60px 20px;
            text-align: center;
            color: white;
            background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAQAAAAECAYAAACp8Z5+AAAAIklEQVQIW2NkQAKrVq36zwjjgzhhYWGMYAEYB8RmROaABADeOQ8CXl/xfgAAAABJRU5ErkJggg=='); /* Simple pattern */
        }

        .special-banner h2 {
            font-family: var(--font-heading);
            font-size: 40px;
            margin-bottom: 20px;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--dark-bg);
            color: #888;
            padding: 60px 10% 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h4 {
            color: white;
            margin-bottom: 20px;
            font-family: var(--font-heading);
            text-transform: uppercase;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col li {
            margin-bottom: 10px;
        }

        .footer-col a {
            color: #888;
            text-decoration: none;
        }

        .footer-col a:hover {
            color: var(--primary-red);
        }

        .copyright {
            text-align: center;
            border-top: 1px solid #333;
            padding-top: 20px;
            font-size: 13px;
        }

        /* --- MOBILE RESPONSIVE --- */
        @media (max-width: 768px) {
            .hero-content h1 { font-size: 50px; }
            nav { display: none; } /* Simplified for demo */
            header { justify-content: center; }
            .logo { text-align: center; }
        }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <header>
        <div class="logo">Waleed <span>& Burger</span></div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#">Deals</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
        <a href="#menu" class="cta-btn">Order Now</a>
    </header>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="hero-content">
            <h1>It's <span>Finger<br>Lickin'</span> Good</h1>
            <p>Welcome to Waleed and Burger and Pizza. Experience the crunch, the taste, and the joy of the perfect combo.</p>
            <a href="#menu" class="cta-btn" style="font-size: 20px; padding: 15px 40px;">View Full Menu</a>
        </div>
    </section>

    <!-- FEATURES -->
    <section class="features">
        <div class="feature-box">
            <div class="feature-icon"><i class="fas fa-drumstick-bite"></i></div>
            <h3>Original Chicken</h3>
            <p>Our secret blend of 11 herbs & spices makes the perfect crispy crunch.</p>
        </div>
        <div class="feature-box">
            <div class="feature-icon"><i class="fas fa-hamburger"></i></div>
            <h3>Giant Burgers</h3>
            <p>Flame-grilled patties stacked with fresh veggies and cheese.</p>
        </div>
        <div class="feature-box">
            <div class="feature-icon"><i class="fas fa-pizza-slice"></i></div>
            <h3>Artisan Pizza</h3>
            <p>Hand-tossed dough with the spiciest Pepperoni in town.</p>
        </div>
    </section>

    <!-- MENU SECTION -->
    <section id="menu" class="menu-section">
        <h2 class="section-title">Our Menu</h2>
        <p class="section-subtitle">Freshly prepared for you every day.</p>
        
        <div class="menu-grid">
            <!-- Item 1: Chicken -->
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1626082927389-6cd097cdc6ec?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Fried Chicken" class="card-image">
                <div class="card-content">
                    <div class="card-header">
                        <div class="card-title">Crispy Bucket</div>
                        <div class="price">$12.99</div>
                    </div>
                    <p class="card-desc">8 pcs of original recipe chicken with mashed potatoes and coleslaw.</p>
                    <button class="add-btn">Add to Cart</button>
                </div>
            </div>

            <!-- Item 2: Burger -->
            <div class="menu-card">
                <img src="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?ixlib=rb
