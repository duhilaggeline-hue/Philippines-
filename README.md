# Philippines-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Philippine Tourism - Personal EmTech Digital Portfolio">
    <title>Discover Philippines | My EmTech Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            color: #222;
            background: #f7fbff;
            line-height: 1.6;
        }

        /* NAVIGATION */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(0, 55, 100, 0.96);
            padding: 15px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 3px 15px rgba(0,0,0,0.15);
        }

        .logo {
            color: white;
            font-size: 23px;
            font-weight: bold;
        }

        .logo span {
            color: #ffd700;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        nav a:hover {
            color: #ffd700;
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 100px 20px 50px;
            color: white;

            background:
                linear-gradient(rgba(0,50,90,0.55), rgba(0,50,90,0.65)),
                url("https://images.unsplash.com/photo-1518509562904-e7ef99cdcc86?auto=format&fit=crop&w=2000&q=80");

            background-size: cover;
            background-position: center;
        }

        .hero-content {
            max-width: 850px;
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 80px);
            margin-bottom: 15px;
            text-shadow: 3px 3px 8px rgba(0,0,0,0.5);
        }

        .hero h1 span {
            color: #ffd700;
        }

        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            padding: 13px 28px;
            margin: 5px;
            background: #ffd700;
            color: #003764;
            text-decoration: none;
            font-weight: bold;
            border-radius: 30px;
            transition: 0.3s;
        }

        .btn:hover {
            background: white;
            transform: translateY(-3px);
        }

        /* GENERAL */
        section {
            padding: 90px 7%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 45px;
        }

        .section-title h2 {
            color: #004b7c;
            font-size: 38px;
            margin-bottom: 10px;
        }

        .section-title p {
            color: #666;
        }

        /* INTRO */
        .intro {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .intro-text h2 {
            color: #004b7c;
            font-size: 38px;
            margin-bottom: 20px;
        }

        .intro-text p {
            margin-bottom: 15px;
            color: #555;
        }

        .intro-image img {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        /* DESTINATIONS */
        .destinations {
            background: #eef8ff;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 7px 25px rgba(0,0,0,0.1);
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .card-content {
            padding: 22px;
        }

        .card h3 {
            color: #004b7c;
            margin-bottom: 8px;
        }

        .card p {
            color: #666;
        }

        /* CULTURE */
        .culture-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .culture-box {
            padding: 30px;
            background: white;
            text-align: center;
            border-radius: 15px;
            box-shadow: 0 7px 20px rgba(0,0,0,0.08);
        }

        .culture-icon {
            font-size: 50px;
            margin-bottom: 15px;
        }

        .culture-box h3 {
            color: #004b7c;
            margin-bottom: 10px;
        }

        /* GALLERY */
        .gallery {
            background: #f0f7fa;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }

        .gallery-item {
            overflow: hidden;
            border-radius: 12px;
            height: 230px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: 0.5s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* ABOUT */
        .about {
            display: grid;
            grid-template-columns: 300px 1fr;
            gap: 50px;
            align-items: center;
        }

        .profile-img {
            width: 280px;
            height: 280px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid #ffd700;
            display: block;
            margin: auto;
        }

        .about-text h2 {
            color: #004b7c;
            font-size: 38px;
            margin-bottom: 15px;
        }

        .about-text p {
            color: #555;
            margin-bottom: 15px;
        }

        /* PORTFOLIO */
        .portfolio {
            background: #eef8ff;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .portfolio-card {
            background: white;
            padding: 28px;
            border-radius: 15px;
            box-shadow: 0 7px 20px rgba(0,0,0,0.08);
            border-top: 5px solid #005b96;
        }

        .portfolio-card h3 {
            color: #004b7c;
            margin-bottom: 10px;
        }

        .portfolio-card p {
            color: #666;
            margin-bottom: 15px;
        }

        .view-btn {
            display: inline-block;
            padding: 8px 18px;
            background: #005b96;
            color: white;
            text-decoration: none;
            border-radius: 20px;
            font-size: 14px;
        }

        .view-btn:hover {
            background: #003764;
        }

        /* CONTACT */
        .contact {
            text-align: center;
        }

        .contact-box {
            max-width: 700px;
            margin: auto;
            background: #004b7c;
            color: white;
            padding: 45px;
            border-radius: 20px;
        }

        .contact-box h2 {
            margin-bottom: 15px;
        }

        .contact-box a {
            color: #ffd700;
            text-decoration: none;
            font-weight: bold;
        }

        /* FOOTER */
        footer {
            background: #002d4d;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        footer span {
            color: #ffd700;
        }

        /* MOBILE */
        @media (max-width: 900px) {

            nav {
                flex-direction: column;
                gap: 10px;
            }

            nav ul {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .intro,
            .about {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .cards,
            .culture-grid,
            .portfolio-grid {
                grid-template-columns: 1fr 1fr;
            }

            .gallery-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 600px) {

            nav {
                padding: 12px;
            }

            nav ul {
                font-size: 13px;
            }

            section {
                padding: 65px 5%;
            }

            .cards,
            .culture-grid,
            .portfolio-grid,
            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .hero p {
                font-size: 17px;
            }

            .contact-box {
                padding: 30px 20px;
            }
        }
    </style>
</head>

<body>

<!-- NAVIGATION -->
<nav>
    <div class="logo">🇵🇭 Explore<span>PH</span></div>

    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#tourism">Tourism</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#about">About Me</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>


<!-- HOME -->
<section class="hero" id="home">
    <div class="hero-content">

        <h1>Discover <span>Philippines</span></h1>

        <p>
            Explore the beauty, culture, food, traditions, and breathtaking
            destinations of the Pearl of the Orient Seas.
        </p>

        <a href="#tourism" class="btn">Explore Tourism</a>
        <a href="#portfolio" class="btn">My Portfolio</a>

    </div>
</section>


<!-- INTRODUCTION -->
<section>

    <div class="intro">

        <div class="intro-text">

            <h2>Welcome to the Philippines 🇵🇭</h2>

            <p>
                The Philippines is an amazing country located in Southeast Asia.
                It is made up of thousands of islands surrounded by beautiful
                seas and oceans.
            </p>

            <p>
                From white-sand beaches and colorful coral reefs to historic
                cities and magnificent mountains, the Philippines offers
                unforgettable experiences for travelers.
            </p>

            <p>
                This website is my EmTech digital portfolio and a personal
                exploration of Philippine tourism.
            </p>

        </div>

        <div class="intro-image">
            <img
                src="https://images.unsplash.com/photo-1537996194471-e657df975ab4?auto=format&fit=crop&w=1000&q=80"
                alt="Philippine tropical landscape">
        </div>

    </div>

</section>


<!-- TOURISM -->
<section class="destinations" id="tourism">

    <div class="section-title">

        <h2>Philippine Tourism</h2>

        <p>
            Discover some of the country's most beautiful destinations.
        </p>

    </div>


    <div class="cards">

        <!-- PALAWAN -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1516690561799-46d8f74f9abf?auto=format&fit=crop&w=1000&q=80"
                alt="Palawan">

            <div class="card-content">

                <h3>🏝️ Palawan</h3>

                <p>
                    Known for its crystal-clear waters, limestone cliffs,
                    lagoons, and incredible marine life. El Nido and Coron
                    are among its most famous destinations.
                </p>

            </div>

        </div>


        <!-- BORACAY -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=1000&q=80"
                alt="Boracay beach">

            <div class="card-content">

                <h3>🌊 Boracay</h3>

                <p>
                    Famous for its beautiful white sand beaches,
                    turquoise waters, sunsets, and exciting island activities.
                </p>

            </div>

        </div>


        <!-- BOHOL -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1548013146-72479768bada?auto=format&fit=crop&w=1000&q=80"
                alt="Bohol">

            <div class="card-content">

                <h3>⛰️ Bohol</h3>

                <p>
                    Home of the famous Chocolate Hills, beautiful beaches,
                    rivers, and the adorable Philippine tarsier.
                </p>

            </div>

        </div>


        <!-- CEBU -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1518509562904-e7ef99cdcc86?auto=format&fit=crop&w=1000&q=80"
                alt="Cebu">

            <div class="card-content">

                <h3>🌴 Cebu</h3>

                <p>
                    A popular destination offering beaches, waterfalls,
                    historical attractions, delicious food, and adventure.
                </p>

            </div>

        </div>


        <!-- BAGUIO -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1000&q=80"
                alt="Mountain destination">

            <div class="card-content">

                <h3>🏔️ Baguio</h3>

                <p>
                    Known as the Summer Capital of the Philippines,
                    Baguio is famous for its cool climate, pine trees,
                    parks, and mountain scenery.
                </p>

            </div>

        </div>


        <!-- SIARGAO -->
        <div class="card">

            <img
                src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=1000&q=80"
                alt="Island destination">

            <div class="card-content">

                <h3>🏄 Siargao</h3>

                <p>
                    A paradise for surfers and nature lovers, famous for
                    its waves, lagoons, islands, and relaxing atmosphere.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- CULTURE -->
<section>

    <div class="section-title">

        <h2>Filipino Culture & Heritage</h2>

        <p>
            Experience the traditions and identity of the Filipino people.
        </p>

    </div>


    <div class="culture-grid">

        <div class="culture-box">

            <div class="culture-icon">🍲</div>

            <h3>Filipino Food</h3>

            <p>
                Filipino cuisine includes delicious dishes such as
                adobo, sinigang, lechon, pancit, and halo-halo.
            </p>

        </div>


        <div class="culture-box">

            <div class="culture-icon">🎉</div>

            <h3>Festivals</h3>

            <p>
                Colorful festivals such as Sinulog, Ati-Atihan,
                Panagbenga, and Kadayawan showcase Filipino culture.
            </p>

        </div>


        <div class="culture-box">

            <div class="culture-icon">🤝</div>

            <h3>Hospitality</h3>

            <p>
                Filipinos are widely known for their warmth,
                friendliness, respect, and hospitality toward guests.
            </p>

        </div>


        <div class="culture-box">

            <div class="culture-icon">💃</div>

            <h3>Traditional Dance</h3>

            <p>
                Traditional dances such as Tinikling and Cariñosa
                represent Filipino history and cultural heritage.
            </p>

        </div>


        <div class="culture-box">

            <div class="culture-icon">🧺</div>

            <h3>Local Crafts</h3>

            <p>
                Filipino communities create beautiful handicrafts,
                woven products, accessories, and traditional artwork.
            </p>

        </div>


        <div class="culture-box">

            <div class="culture-icon">❤️</div>

            <h3>Family Values</h3>

            <p>
                Strong family relationships, respect for elders,
                and community spirit are important Filipino values.
            </p>

        </div>

    </div>

</section>


<!-- GALLERY -->
<section class="gallery" id="gallery">

    <div class="section-title">

        <h2>Tourism Gallery 📸</h2>

        <p>
            A visual journey through the beauty of the Philippines.
        </p>

    </div>


    <div class="gallery-grid">

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80"
                alt="Beach">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1518509562904-e7ef99cdcc86?auto=format&fit=crop&w=800&q=80"
                alt="Island">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1516690561799-46d8f74f9abf?auto=format&fit=crop&w=800&q=80"
                alt="Ocean">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1537996194471-e657df975ab4?auto=format&fit=crop&w=800&q=80"
                alt="Tropical destination">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1548013146-72479768bada?auto=format&fit=crop&w=800&q=80"
                alt="Nature">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=800&q=80"
                alt="Mountain">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=800&q=80"
                alt="Island scenery">
        </div>

        <div class="gallery-item">
            <img
                src="https://images.unsplash.com/photo-1528127269322-539801943592?auto=format&fit=crop&w=800&q=80"
                alt="Philippine scenery">
        </div>

    </div>

</section>


<!-- ABOUT ME -->
<section id="about">

    <div class="section-title">
        <h2>About Me 👤</h2>
        <p>Get to know the student behind this website.</p>
    </div>


    <div class="about">

        <div>

            <!-- Replace this URL with your own photo -->
            <img
                class="profile-img"
                src="https://via.placeholder.com/400x400.png?text=Your+Photo"
                alt="My profile photo">

        </div>


        <div class="about-text">

            <h2>Hello! I'm Your Name 👋</h2>

            <p>
                I am a student currently taking Empowerment Technologies
                (EmTech). This website was created as my final project
                and digital portfolio.
            </p>

            <p>
                I chose Philippine Tourism as my theme because I want to
                showcase the natural beauty, culture, food, traditions,
                and destinations of our country.
            </p>

            <p>
                Through this project, I learned how technology can be used
                to present information creatively and build an on
