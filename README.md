<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cuts & Shades | Premium Saloon & Grooming</title>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: #121212;
            color: #ffffff;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* Header / Navbar */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(18, 18, 18, 0.95);
            padding: 20px 10%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 1px solid #2a2a2a;
        }

        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #ffb703;
            letter-spacing: 1px;
        }

        .logo span {
            color: #fff;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #ffb703;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1503951914875-452162b0f3f1?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            font-weight: 700;
            letter-spacing: 2px;
        }

        .hero h1 span {
            color: #ffb703;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: #ccc;
            max-width: 600px;
        }

        .btn {
            background-color: #ffb703;
            color: #121212;
            padding: 12px 30px;
            font-weight: 600;
            border-radius: 5px;
            transition: background 0.3s, transform 0.3s;
        }

        .btn:hover {
            background-color: #fb8500;
            transform: translateY(-2px);
        }

        /* Sections General */
        section {
            padding: 80px 10%;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 60px;
            height: 3px;
            background-color: #ffb703;
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* Packages Section */
        .packages-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .package-card {
            background: #1e1e1e;
            padding: 30px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #2a2a2a;
            transition: transform 0.3s;
        }

        .package-card:hover {
            transform: translateY(-5px);
            border-color: #ffb703;
        }

        .package-card i {
            font-size: 2.5rem;
            color: #ffb703;
            margin-bottom: 20px;
        }

        .package-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .package-price {
            font-size: 1.8rem;
            color: #ffb703;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .package-card p {
            color: #aaa;
            font-size: 0.95rem;
            line-height: 1.6;
        }

        /* Our Work / Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            height: 300px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .gallery-overlay i {
            color: #ffb703;
            font-size: 2rem;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        /* VIDEO REVIEWS SECTION */
        .reviews-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .review-card {
            background: #1e1e1e;
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid #2a2a2a;
            transition: transform 0.3s;
        }

        .review-card:hover {
            transform: translateY(-5px);
            border-color: #ffb703;
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            height: 400px; /* Tik-Tok/Reels style vertical height */
            background: #000;
        }

        .video-wrapper video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .review-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: rgba(0, 0, 0, 0.7);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .review-details {
            padding: 20px;
        }

        .stars {
            color: #ffb703;
            margin-bottom: 10px;
            font-size: 0.9rem;
        }

        .review-text {
            color: #ddd;
            font-size: 0.95rem;
            font-style: italic;
            line-height: 1.5;
            margin-bottom: 15px;
        }

        .client-name {
            font-weight: 600;
            color: #ffb703;
            font-size: 1rem;
        }

        .fa-instagram { color: #e1306c; }
        .fa-facebook { color: #1877f2; }

        /* Contact Section */
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            background: #1e1e1e;
            padding: 40px;
            border-radius: 8px;
            border: 1px solid #2a2a2a;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            background: #121212;
            border: 1px solid #333;
            color: #fff;
            border-radius: 5px;
            outline: none;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: #ffb703;
        }

        /* Footer */
        footer {
            background: #0a0a0a;
            padding: 40px 10%;
            text-align: center;
            border-top: 1px solid #2a2a2a;
        }

        .social-icons {
            margin-bottom: 20px;
        }

        .social-icons a {
            font-size: 1.5rem;
            margin: 0 15px;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: #ffb703;
        }

        footer p {
            color: #777;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2.5rem; }
            section { padding: 60px 5%; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">CUTS <span>& SHADES</span></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#packages">Packages</a></li>
            <li><a href="#work">Our Work</a></li>
            <li><a href="#reviews">Reviews</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Cuts & Shades <span>Saloon</span></h1>
        <p>Your look is our passion. Experience premium haircuts, grooming, and styling services tailored just for you.</p>
        <a href="#contact" class="btn">Book Appointment</a>
    </section>

    <!-- Packages Section -->
    <section id="packages">
        <h2 class="section-title">Our Packages & Services</h2>
        <div class="packages-grid">
            <div class="package-card">
                <i class="fas fa-cut"></i>
                <h3>Classic Haircut</h3>
                <div class="package-price">Rs. 500</div>
                <p>Professional haircut, hair wash, and custom styling according to your face shape.</p>
            </div>
            <div class="package-card">
                <i class="fas fa-user-tie"></i>
                <h3>Beard Styling & Shave</h3>
                <div class="package-price">Rs. 300</div>
                <p>Premium beard trimming, shaping, and hot towel shave for a sharp clean look.</p>
            </div>
            <div class="package-card">
                <i class="fas fa-magic"></i>
                <h3>Premium Hair Color</h3>
                <div class="package-price">Rs. 1,500+</div>
                <p>Top-quality hair coloring, highlights, and damage-free treatment by experts.</p>
            </div>
            <div class="package-card">
                <i class="fas fa-spa"></i>
                <h3>Royal Grooming Combo</h3>
                <div class="package-price">Rs. 2,500</div>
                <p>Includes Haircut, Premium Beard Grooming, Charcoal Facial, and Hair Spa.</p>
            </div>
        </div>
    </section>

    <!-- Our Work Section -->
    <section id="work" style="background-color: #1a1a1a;">
        <h2 class="section-title">Our Work (From Instagram)</h2>
        <div class="gallery-grid">
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Haircut Work">
                <div class="gallery-overlay"><i class="fab fa-instagram"></i></div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1593702295094-aea22597af65?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Beard Grooming">
                <div class="gallery-overlay"><i class="fab fa-instagram"></i></div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1605497746444-ac9da5848ba7?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Hair Styling">
                <div class="gallery-overlay"><i class="fab fa-instagram"></i></div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1517832606589-7a598b647192?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Saloon Interior">
                <div class="gallery-overlay"><i class="fab fa-instagram"></i></div>
            </div>
        </div>
    </section>

    <!-- Video Reviews Section -->
    <section id="reviews">
        <h2 class="section-title">Video Reviews From Clients</h2>
        <div class="reviews-container">
            
            <!-- Video Review 1 -->
            <div class="review-card">
                <div class="video-wrapper">
                    <!-- GitHub par videos upload karke 'src' mein uska naam daal dena, e.g., src="review1.mp4" -->
                    <video src="https://www.w3schools.com/html/mov_bbb.mp4" controls loop muted autoplay></video>
                    <div class="review-badge"><i class="fab fa-instagram"></i> Instagram</div>
                </div>
                <div class="review-details">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="review-text">"Amazing experience! Unka service aur behaviour bohat accha hai. Best fade cut in town."</p>
                    <div class="client-name">Ali Khan</div>
                </div>
            </div>

            <!-- Video Review 2 -->
            <div class="review-card">
                <div class="video-wrapper">
                    <video src="https://www.w3schools.com/html/movie.mp4" controls loop muted autoplay></video>
                    <div class="review-badge"><i class="fab fa-facebook"></i> Facebook</div>
                </div>
                <div class="review-details">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="review-text">"Highly professional staff aur saloon ki hygiene 10/10 hai. Hair transformation boht fit ki."</p>
                    <div class="client-name">Zain Ahmed</div>
                </div>
            </div>

            <!-- Video Review 3 -->
            <div class="review-card">
                <div class="video-wrapper">
                    <video src="https://www.w3schools.com/html/mov_bbb.mp4" controls loop muted autoplay></video>
                    <div class="review-badge"><i class="fab fa-instagram"></i> Instagram</div>
                </div>
                <div class="review-details">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="review-text">"Value for money! Packages boht saste hain aur kaam boht premium level ka karte hain."</p>
                    <div class="client-name">Hamza Malik</div>
                </div>
            </div>

        </div>
    </section>

    <!-- Contact / Appointment Section -->
    <section id="contact" style="background-color: #1a1a1a;">
        <h2 class="section-title">Book An Appointment</h2>
        <div class="contact-container">
            <form action="#">
                <div class="form-group">
                    <input type="text" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <input type="tel" placeholder="Phone Number" required>
                </div>
                <div class="form-group">
                    <input type="datetime-local" required>
                </div>
                <div class="form-group">
                    <textarea rows="4" placeholder="Select Service or Special Instructions"></textarea>
                </div>
                <button type="submit" class="btn" style="width: 100%; border: none; cursor: pointer;">Submit Request</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-icons">
            <a href="https://web.facebook.com/CutsnShades/?_rdc=1&_rdr#" target="_blank"><i class="fab fa-facebook"></i></a>
            <a href="https://www.instagram.com/cutsnshadesofficial/?hl=en" target="_blank"><i class="fab fa-instagram"></i></a>
        </div>
        <p>&copy; 2026 Cuts & Shades Saloon. All Rights Reserved.</p>
    </footer>

</body>
</html>
