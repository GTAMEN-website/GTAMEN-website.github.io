<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GTAMEN - GTA V PS5 Community</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background-color: #0a0a0a;
            color: #00ff88;
            line-height: 1.6;
        }

        /* Header */
        header {
            background-color: #1a1a1a;
            padding: 20px 0;
            border-bottom: 3px solid #00ff88;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo img {
            height: 60px;
            width: auto;
        }

        .logo h1 {
            font-size: 2em;
            color: #00ff88;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .tagline {
            color: #888;
            font-size: 0.9em;
            margin-top: 5px;
        }

        /* Navigation */
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav button {
            background: none;
            color: #00ff88;
            border: 2px solid transparent;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: bold;
            padding: 10px 15px;
            transition: all 0.3s;
            cursor: pointer;
            font-family: 'Courier New', monospace;
            font-size: 1em;
        }

        nav button:hover, nav button.active {
            border: 2px solid #00ff88;
            background-color: rgba(0, 255, 136, 0.1);
        }

        /* Main Content */
        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            min-height: calc(100vh - 300px);
        }

        /* Page Sections */
        .page-section {
            display: none;
            animation: fadeIn 0.5s;
        }

        .page-section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, #1a1a1a 0%, #0a3a2a 100%);
            border: 3px solid #00ff88;
            margin-bottom: 40px;
            border-radius: 10px;
        }

        .hero h2 {
            font-size: 3em;
            margin-bottom: 20px;
            text-shadow: 0 0 20px #00ff88;
        }

        .hero p {
            font-size: 1.2em;
            color: #aaa;
            max-width: 800px;
            margin: 0 auto 30px;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background-color: #00ff88;
            color: #0a0a0a;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            border-radius: 5px;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1.1em;
        }

        .cta-button:hover {
            background-color: #00cc6e;
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(0, 255, 136, 0.3);
        }

        /* Section Styles */
        .page-title {
            font-size: 2.5em;
            margin-bottom: 30px;
            text-transform: uppercase;
            border-bottom: 3px solid #00ff88;
            padding-bottom: 10px;
        }

        /* Grid Layout */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .card {
            background-color: #1a1a1a;
            border: 2px solid #00ff88;
            padding: 30px;
            border-radius: 10px;
            transition: all 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.2);
            border-color: #00cc6e;
        }

        .card h3 {
            font-size: 1.8em;
            margin-bottom: 15px;
            color: #00ff88;
        }

        .card p {
            color: #aaa;
            margin-bottom: 15px;
        }

        /* Movie Card Specific */
        .movie-card {
            background-color: #0a2a1a;
            position: relative;
            overflow: hidden;
        }

        .movie-banner {
            width: 100%;
            height: 200px;
            background-size: cover;
            background-position: center;
            margin: -30px -30px 20px -30px;
            border-bottom: 2px solid #00ff88;
        }

        .movie-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid #00ff88;
        }

        .movie-time {
            color: #00ff88;
            font-weight: bold;
        }

        .movie-genre {
            color: #888;
            font-size: 0.9em;
        }

        .status-badge {
            display: inline-block;
            padding: 5px 15px;
            background-color: #00ff88;
            color: #0a0a0a;
            border-radius: 3px;
            font-size: 0.8em;
            font-weight: bold;
            text-transform: uppercase;
        }

        .status-coming {
            background-color: #ff8800;
        }

        /* Event Card */
        .event-card {
            border-left: 5px solid #00ff88;
        }

        .event-date {
            display: inline-block;
            background-color: #00ff88;
            color: #0a0a0a;
            padding: 5px 15px;
            border-radius: 3px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            background-color: #1a1a1a;
            border-top: 3px solid #00ff88;
            padding: 40px 20px;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        footer p {
            color: #888;
            margin-bottom: 10px;
        }

        /* Active Community Banner */
        .active-banner {
            background-color: #0a2a1a;
            border: 2px solid #00ff88;
            padding: 15px;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 5px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 10px rgba(0, 255, 136, 0.3); }
            50% { box-shadow: 0 0 20px rgba(0, 255, 136, 0.6); }
        }

        .active-banner span {
            color: #00ff88;
            font-size: 1.2em;
            font-weight: bold;
        }

        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: 2px solid #00ff88;
            color: #00ff88;
            font-size: 1.5em;
            padding: 10px 15px;
            cursor: pointer;
        }

        /* Image Gallery */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .gallery-item {
            border: 2px solid #00ff88;
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s;
        }

        .gallery-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.3);
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }

        /* Driver Cards */
        .driver-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .driver-card {
            background-color: #1a1a1a;
            border: 2px solid #00ff88;
            border-radius: 10px;
            overflow: hidden;
            text-align: center;
            transition: all 0.3s;
        }

        .driver-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 255, 136, 0.3);
        }

        .driver-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-bottom: 2px solid #00ff88;
        }

        .driver-card h4 {
            color: #00ff88;
            font-size: 1.3em;
            padding: 15px;
            margin: 0;
        }

        .open-spot {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 200px;
            background: linear-gradient(135deg, #1a1a1a 0%, #0a3a2a 100%);
            border-bottom: 2px solid #00ff88;
        }

        .open-spot span {
            font-size: 1.5em;
            color: #00ff88;
            font-weight: bold;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }

            nav {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: #1a1a1a;
                border-top: 2px solid #00ff88;
            }

            nav.active {
                display: block;
            }

            nav ul {
                flex-direction: column;
                gap: 0;
            }

            nav button {
                display: block;
                width: 100%;
                padding: 15px;
                border-bottom: 1px solid #00ff88;
                text-align: left;
            }

            .hero h2 {
                font-size: 2em;
            }

            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo">
                <img src="https://i.postimg.cc/YqhJdqTB/IMG_1697.png" alt="GTAMEN Logo">
                <h1>GTAMEN</h1>
            </div>
            <button class="mobile-menu-btn" onclick="toggleMenu()">☰</button>
            <nav id="mainNav">
                <ul>
                    <li><button onclick="showPage('home')" class="nav-btn active" data-page="home">Home</button></li>
                    <li><button onclick="showPage('about')" class="nav-btn" data-page="about">About Us</button></li>
                    <li><button onclick="showPage('movies')" class="nav-btn" data-page="movies">Movies</button></li>
                    <li><button onclick="showPage('events')" class="nav-btn" data-page="events">Events</button></li>
                    <li><button onclick="showPage('racing')" class="nav-btn" data-page="racing">Racing</button></li>
                    <li><button onclick="showPage('discord')" class="nav-btn" data-page="discord">Discord</button></li>
                    <li><button onclick="showPage('lsn')" class="nav-btn" data-page="lsn">LSN</button></li>
                    <li><button onclick="showPage('summit')" class="nav-btn" data-page="summit">Summit</button></li>
                </ul>
            </nav>
        </div>
        <div class="tagline" style="text-align: center; margin-top: 10px;">GTA V PS5 COMMUNITY // GTAMEN</div>
    </header>

    <main>
        <!-- Home Page -->
        <div id="home" class="page-section active">
            <!-- Active Community Banner -->
            <div class="active-banner">
                <span>🟢 ACTIVE COMMUNITY 🟢</span>
            </div>

            <!-- Hero Section -->
            <div class="hero">
                <h2>Welcome to GTAMEN</h2>
                <p>The premier GTA V PS5 community dedicated to GTAMEN content, epic movie productions, and unforgettable events. Join our thriving community today!</p>
                <a href="https://discord.gg/9GSj6BGACr" target="_blank" class="cta-button">Join Discord</a>
            </div>

            <div class="grid">
                <div class="card">
                    <h3>🎬 Movie Productions</h3>
                    <p>Experience cinematic storytelling with our epic GTAMEN movie series, featuring high-quality productions and engaging narratives.</p>
                </div>
                <div class="card">
                    <h3>🎮 Active Community</h3>
                    <p>Join daily sessions, organized activities, and connect with fellow GTAMEN members on PS5 GTA V.</p>
                </div>
                <div class="card">
                    <h3>🚗 Car Meets</h3>
                    <p>Participate in Summit car meets, showcases, and cruises through Los Santos with the crew.</p>
                </div>
            </div>
        </div>

        <!-- About Us Page -->
        <div id="about" class="page-section">
            <h2 class="page-title">About Us</h2>
            <div class="grid">
                <div class="card">
                    <h3>Our Community</h3>
                    <p>We're a thriving PS5 GTA V community built on quality connections and organized gameplay. While we value meaningful interactions, we maintain close contact with everyone, focusing on creating memorable experiences together.</p>
                </div>
                <div class="card">
                    <h3>Our Approach</h3>
                    <p>We're building a community where every member matters. As we grow, we maintain close contact with everyone, focusing on quality interactions and ensuring each voice is heard in our collaborative environment.</p>
                </div>
                <div class="card">
                    <h3>What We Offer</h3>
                    <p>From epic movie productions to organized events and daily gameplay sessions, GTAMEN provides a complete GTA V experience centered around our legendary community.</p>
                </div>
            </div>

            <div class="card" style="margin-top: 40px;">
                <h3>Our Mission</h3>
                <p>GTAMEN is dedicated to creating the ultimate GTA V PS5 experience. We combine cinematic storytelling, organized gameplay, and a supportive community to build something truly special in Los Santos.</p>
                <p style="margin-top: 15px;">Whether you're interested in participating in our movie productions, joining our events, or simply hanging out with like-minded players, GTAMEN welcomes you!</p>
            </div>
        </div>

        <!-- Movies Page -->
        <div id="movies" class="page-section">
            <h2 class="page-title">Movies & Trailers</h2>
            
            <div class="card" style="text-align: center; padding: 50px; margin-bottom: 40px;">
                <img src="https://i.postimg.cc/Pf4wSdYL/IMG_1700.jpg" alt="Coming Soon" style="max-width: 100%; height: auto; border-radius: 10px; border: 3px solid #00ff88; margin-bottom: 20px;">
                <h3 style="font-size: 2.5em; margin-bottom: 15px;">Movie Productions Coming Soon</h3>
                <p style="font-size: 1.2em; color: #aaa;">We're working on exciting new cinematic projects. Stay tuned for epic GTAMEN movie productions!</p>
            </div>

            <div class="grid">
                <div class="card">
                    <h3>🎬 In Development</h3>
                    <p>Multiple movie projects are currently in pre-production. Casting calls and crew positions will be announced soon in our Discord.</p>
                </div>
                <div class="card">
                    <h3>📹 Behind the Scenes</h3>
                    <p>Follow our Discord for exclusive behind-the-scenes content, production updates, and sneak peeks at upcoming releases.</p>
                </div>
                <div class="card">
                    <h3>⭐ Get Involved</h3>
                    <p>Interested in being part of our productions? Join our Discord to learn about opportunities for actors, directors, and crew members.</p>
                </div>
            </div>
        </div>

        <!-- Events Page -->
        <div id="events" class="page-section">
            <h2 class="page-title">Events</h2>
            
            <div class="card" style="text-align: center; padding: 50px; margin-bottom: 40px;">
                <img src="https://i.postimg.cc/Pf4wSdYL/IMG_1700.jpg" alt="Coming Soon" style="max-width: 100%; height: auto; border-radius: 10px; border: 3px solid #00ff88; margin-bottom: 20px;">
                <h3 style="font-size: 2.5em; margin-bottom: 15px;">Events Coming Soon</h3>
                <p style="font-size: 1.2em; color: #aaa;">We're planning exciting community events. Stay tuned for announcements!</p>
            </div>

            <div class="grid">
                <div class="card">
                    <h3>📅 In Planning</h3>
                    <p>Multiple community events are currently being organized. Event schedules and details will be announced in our Discord.</p>
                </div>
                <div class="card">
                    <h3>🔔 Stay Updated</h3>
                    <p>Join our Discord to be the first to know about upcoming events, activities, and special gatherings.</p>
                </div>
                <div class="card">
                    <h3>🎯 Get Involved</h3>
                    <p>Want to help organize events? Join our Discord to share your ideas and volunteer for event planning roles.</p>
                </div>
            </div>
        </div>

        <!-- Racing Page -->
        <div id="racing" class="page-section">
            <h2 class="page-title">GTAMEN Racing</h2>
            
            <div class="card" style="text-align: center; padding: 40px;">
                <img src="https://i.postimg.cc/J0st7H4J/IMG_1707.png" alt="Gran Turismo 7 Logo" style="max-width: 400px; height: auto; margin: 0 auto 20px; display: block;">
                <h3>Gran Turismo 7 Racing Team</h3>
                <p style="font-size: 1.1em; color: #aaa; margin-top: 15px;">Our elite racing division competing in GT7. Precision, speed, and teamwork define our drivers.</p>
            </div>

            <h3 style="margin-top: 50px; margin-bottom: 20px; font-size: 2em; color: #00ff88; text-align: center;">Our Drivers</h3>
            <div class="driver-grid">
                <div class="driver-card">
                    <img src="https://i.postimg.cc/T2ND8fY2/IMG_1706.jpg" alt="Koomzy">
                    <h4>Koomzy</h4>
                </div>
                <div class="driver-card">
                    <img src="https://i.postimg.cc/L4Q1d26m/IMG_1704.png" alt="Mental">
                    <h4>Mental</h4>
                </div>
                <div class="driver-card">
                    <img src="https://i.postimg.cc/ryZr6MFV/IMG_1705.png" alt="Cobra_ry">
                    <h4>Cobra_ry</h4>
                </div>
                <div class="driver-card">
                    <img src="https://i.postimg.cc/XN1CM477/IMG_1703.png" alt="NURB_DEMOLISHER">
                    <h4>NURB_DEMOLISHER</h4>
                </div>
                <div class="driver-card">
                    <img src="https://i.postimg.cc/SQ1M0kNs/IMG_1702.png" alt="FAZE_PENI3">
                    <h4>FAZE_PENI3</h4>
                </div>
                <div class="driver-card">
                    <div class="open-spot">
                        <span>SPOT OPEN</span>
                    </div>
                    <h4>Join Our Team</h4>
                </div>
            </div>

            <div class="card" style="margin-top: 50px; text-align: center; padding: 40px; background: linear-gradient(135deg, #1a1a1a 0%, #0a2a3a 100%);">
                <img src="https://i.postimg.cc/bwpDkJm5/IMG_1708.png" alt="FIA Logo" style="max-width: 300px; height: auto; margin: 0 auto 20px; display: block;">
                <h3 style="font-size: 2.2em; margin-bottom: 20px;">FIA Competition</h3>
                <p style="font-size: 1.1em; color: #aaa; margin-bottom: 30px;">Our elite drivers competing at the highest level of Gran Turismo 7 motorsport.</p>
                
                <h4 style="color: #00ff88; font-size: 1.5em; margin-bottom: 20px;">FIA Drivers</h4>
                <div class="driver-grid" style="max-width: 600px; margin: 0 auto;">
                    <div class="driver-card">
                        <img src="https://i.postimg.cc/T2ND8fY2/IMG_1706.jpg" alt="Koomzy">
                        <h4>Koomzy</h4>
                    </div>
                    <div class="driver-card">
                        <img src="https://i.postimg.cc/L4Q1d26m/IMG_1704.png" alt="Mental">
                        <h4>Mental</h4>
                    </div>
                </div>
            </div>
        </div>

        <!-- Discord Page -->
        <div id="discord" class="page-section">
            <h2 class="page-title">Join Our Discord</h2>
            <div class="card" style="text-align: center; padding: 50px;">
                <h3>Connect With GTAMEN</h3>
                <p>Join our active Discord community to stay updated on events, participate in movie productions, and connect with fellow GTAMEN members!</p>
                <p style="margin-top: 20px; color: #aaa;">Get access to:</p>
                <div style="margin: 30px 0; display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; text-align: left;">
                    <div>
                        <p style="color: #00ff88;">✓ Event Announcements</p>
                        <p style="color: #00ff88;">✓ Movie Updates</p>
                    </div>
                    <div>
                        <p style="color: #00ff88;">✓ Community Chat</p>
                        <p style="color: #00ff88;">✓ Gaming Sessions</p>
                    </div>
                    <div>
                        <p style="color: #00ff88;">✓ Exclusive Content</p>
                        <p style="color: #00ff88;">✓ Voice Channels</p>
                    </div>
                </div>
                <a href="https://discord.gg/9GSj6BGACr" target="_blank" class="cta-button" style="margin-top: 20px;">Join Discord Server</a>
            </div>
        </div>

        <!-- LSN Page -->
        <div id="lsn" class="page-section">
            <h2 class="page-title">Los Santos Nations (LSN)</h2>
            <div class="card" style="text-align: center;">
                <img src="https://i.postimg.cc/6QqcXYx2/IMG_1701.png" alt="LSN Logo" style="max-width: 300px; height: auto; margin: 0 auto 20px; display: block;">
                <h3>Elite Security Services</h3>
                <p>Los Santos Nations is our premier security division providing professional protection services throughout Los Santos. We offer elite security details, VIP protection, and event security for the GTAMEN community.</p>
                <p style="margin-top: 15px;">Our trained security personnel ensure safety and professionalism at all community events and operations.</p>
                <a href="https://discord.gg/fFTvRURxzd" target="_blank" class="cta-button" style="margin-top: 20px;">Join LSN Discord</a>
            </div>

            <div class="grid" style="margin-top: 30px;">
                <div class="card">
                    <h3>🛡️ VIP Protection</h3>
                    <p>Professional close protection services for high-profile community members and special guests.</p>
                </div>
                <div class="card">
                    <h3>🚨 Event Security</h3>
                    <p>Comprehensive security coverage for car meets, movie premieres, and community gatherings.</p>
                </div>
                <div class="card">
                    <h3>⭐ Elite Training</h3>
                    <p>All LSN security personnel undergo rigorous training to maintain the highest standards of professionalism.</p>
                </div>
            </div>

            <div class="image-gallery">
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/xThBhVVF/IMG_1695.jpg" alt="LSN Security">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/tCYLBC8b/IMG_1694.jpg" alt="LSN Operations">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/WbCxCcPc/IMG_1689.jpg" alt="LSN Team">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/8P9x9gVS/IMG_1688.jpg" alt="LSN Service">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/HsRFR1CY/IMG_1686.jpg" alt="LSN Detail">
                </div>
            </div>
        </div>

        <!-- Summit Page -->
        <div id="summit" class="page-section">
            <h2 class="page-title">Summit - Car Meet Group</h2>
            <div class="card" style="text-align: center; padding: 50px;">
                <h3>Summit Car Meets</h3>
                <p style="font-size: 1.2em; margin-bottom: 30px;">Our exclusive car meet group bringing together the finest rides in Los Santos.</p>
                <p style="color: #aaa;">Join Summit for weekly car showcases, cruises, and automotive excellence. Show off your collection and connect with fellow car enthusiasts!</p>
            </div>

            <div class="grid" style="margin-top: 30px;">
                <div class="card">
                    <h3>🚗 Weekly Meets</h3>
                    <p>Every Saturday we gather for organized car meets featuring the best vehicles in the community.</p>
                </div>
                <div class="card">
                    <h3>🏁 Cruise Events</h3>
                    <p>Organized cruises through Los Santos with the crew. Scenic routes and photo opportunities.</p>
                </div>
                <div class="card">
                    <h3>📸 Showcase Your Rides</h3>
                    <p>Display your custom builds, rare finds, and meticulously tuned vehicles to the community.</p>
                </div>
            </div>

            <div class="image-gallery">
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/L6nrx6GM/IMG_1696.jpg" alt="Summit Car Meet">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/KvwCwhhW/IMG_1693.jpg" alt="Summit Showcase">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/NfSZSvvV/IMG_1692.jpg" alt="Summit Cars">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/65gFgxxD/IMG_1691.jpg" alt="Summit Cruise">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/9FKsKHHK/IMG_1690.jpg" alt="Summit Lineup">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/152b21ZP/IMG_1687.jpg" alt="Summit Collection">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/ncgNgftH/IMG_1685.jpg" alt="Summit Event">
                </div>
                <div class="gallery-item">
                    <img src="https://i.postimg.cc/9FKsKHjX/IMG_1684.jpg" alt="Summit Gathering">
                </div>
            </div>
        </div>
    </main>

    <footer>
        <div class="footer-content">
            <p>&copy; 2024 GTAMEN - GTA V PS5 Community</p>
            <p style="color: #00ff88; margin-top: 15px;">Built with dedication for our community</p>
        </div>
    </footer>

    <script>
        function showPage(pageName) {
            // Hide all pages
            const pages = document.querySelectorAll('.page-section');
            pages.forEach(page => page.classList.remove('active'));

            // Show selected page
            document.getElementById(pageName).classList.add('active');

            // Update nav buttons
            const navBtns = document.querySelectorAll('.nav-btn');
            navBtns.forEach(btn => btn.classList.remove('active'));
            document.querySelector(`[data-page="${pageName}"]`).classList.add('active');

            // Close mobile menu
            document.getElementById('mainNav').classList.remove('active');

            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function toggleMenu() {
            const nav = document.getElementById('mainNav');
            nav.classList.toggle('active');
        }
    </script>
</body>
</html>
