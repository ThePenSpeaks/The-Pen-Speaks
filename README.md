<!DOCTYPE html><script src="/_replco/static/devtools/eruda/3.2.3/eruda.js"></script><script src="/_replco/static/devtools/injected.js"onerror="parent.postMessage({event:'error',payload:'script.onerror: Failed to load '+event.target.src},'https://replit.com')"></script>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Pen Speaks | Advanced Graphology Solutions</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #2A2D4E;
            --accent: #FFD700;
            --ink: #1a1a1a;
            --paper: #fffef7;
            --font-stack: 'Segoe UI', system-ui, sans-serif;
        }

        /* Modern Reset */
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: var(--font-stack);
            line-height: 1.6;
            color: var(--ink);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: 
                radial-gradient(circle at 10% 20%, rgba(255,215,0,0.1) 0%, transparent 50%),
                linear-gradient(45deg, #2A2D4E 0%, #3A3F6D 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M20 50 Q40 30 50 20 Q60 30 80 50 Q60 70 50 80 Q40 70 20 50" fill="none" stroke="%23FFD700" stroke-width="0.5"/></svg>');
            opacity: 0.1;
            animation: float 20s linear infinite;
        }

        @keyframes float {
            from { transform: translateY(0) rotate(0deg); }
            to { transform: translateY(-50%) rotate(360deg); }
        }

        /* Service Cards */
        .service-grid {
            display: grid;
            gap: 2rem;
            padding: 4rem 2rem;
            background: var(--paper);
            position: relative;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        }

        .service-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 215, 0, 0.3);
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px) rotateZ(0.5deg);
        }

        .service-card::after {
            content: '';
            position: absolute;
            inset: -2px;
            z-index: -1;
            background: linear-gradient(45deg, 
                var(--primary), 
                var(--accent), 
                var(--primary));
            border-radius: 22px;
            animation: borderGlow 3s linear infinite;
            opacity: 0.5;
        }

        /* Price Cards */
        .pricing-section {
            background: var(--primary);
            padding: 4rem 2rem;
            position: relative;
        }

        .pricing-grid {
            display: grid;
            gap: 2rem;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            max-width: 1200px;
            margin: 0 auto;
        }

        .price-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2rem;
            color: var(--paper);
            border: 1px solid var(--accent);
            backdrop-filter: blur(10px);
            transition: transform 0.3s ease;
        }

        .price-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.2);
        }

        .price {
            font-size: 3rem;
            color: var(--accent);
            margin: 1rem 0;
        }

        .feature-list {
            list-style: none;
            margin: 2rem 0;
        }

        .feature-list li {
            margin: 0.5rem 0;
        }

        .feature-list li:before {
            content: '⟐';
            color: var(--accent);
            margin-right: 0.5rem;
        }


        @keyframes borderGlow {
            0% { filter: hue-rotate(0deg); }
            100% { filter: hue-rotate(360deg); }
        }

        /* Cyberpunk Effects */
        @keyframes cyberpunk-glitch {
            0% { text-shadow: 0.05em 0 0 rgba(255,0,0,.75), -0.025em -0.05em 0 rgba(0,255,0,.75), -0.025em 0.05em 0 rgba(0,0,255,.75); }
            50% { text-shadow: 0.025em 0.05em 0 rgba(255,0,0,.75), 0.05em 0 0 rgba(0,255,0,.75), 0 -0.05em 0 rgba(0,0,255,.75); }
            100% { text-shadow: -0.025em 0 0 rgba(255,0,0,.75), -0.025em -0.025em 0 rgba(0,255,0,.75), -0.025em -0.05em 0 rgba(0,0,255,.75); }
        }

        .cyber-text {
            animation: cyberpunk-glitch 2s infinite;
        }

        /* Buttons */
        .cyber-button {
            padding: 1rem 2rem;
            background: var(--primary);
            color: var(--accent);
            border: 2px solid var(--accent);
            border-radius: 0;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            clip-path: polygon(10% 0, 100% 0, 90% 100%, 0 100%);
            cursor: pointer;
        }

        .cyber-button:hover {
            transform: scale(1.05);
            box-shadow: 0 0 25px rgba(255,215,0,0.4);
        }

        /* Section Headers */
        .section-header {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--accent);
        }

        .section-header h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        /* Footer */
        footer {
            background: linear-gradient(45deg, #1a1a1a 0%, #2A2D4E 100%);
            color: white;
            padding: 4rem 2rem;
            position: relative;
        }

        footer::before {
            content: '';
            position: absolute;
            top: -50px;
            left: 0;
            width: 100%;
            height: 100px;
            background: var(--paper);
            clip-path: polygon(0 0, 100% 0, 50% 100%, 0 0);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }

            .service-grid, .pricing-grid {
                grid-template-columns: 1fr;
            }

            .price-card {
                margin: 1rem;
            }
        }
        /* Contact Us Styles */
        .contact-section {
            background: var(--primary);
            padding: 4rem 2rem;
            position: relative;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .contact-info {
            display: grid;
            gap: 2rem;
        }

        .contact-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--accent);
            text-align: center;
            color: var(--paper);
        }

        .contact-item h3 {
            color: var(--accent);
            margin: 1rem 0;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid var(--accent);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .cyber-input {
            width: 100%;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid var(--accent);
            color: var(--paper);
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .cyber-input:focus {
            outline: none;
            box-shadow: 0 0 15px rgba(255,215,0,0.3);
            border-color: var(--accent);
        }

        .cyber-input::placeholder {
            color: rgba(255, 255, 255, 0.5);
        }

        select.cyber-input {
            appearance: none;
            cursor: pointer;
        }

        select.cyber-input option {
            background: var(--primary);
            color: var(--paper);
        }

        textarea.cyber-input {
            resize: vertical;
            min-height: 100px;
        }

        @media (max-width: 768px) {
            .contact-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <h1 class="cyber-text" style="font-size: 4rem; color: var(--accent); text-align: center;">
            The Pen Speaks<br>
            <span style="font-size: 2rem; display: block; margin-top: 1rem;">
                Thoughts Between The Lines
            </span>
        </h1>
        <button class="cyber-button" style="margin-top: 2rem;">
            <i class="fas fa-rocket"></i> Start Analysis
        </button>
    </section>

    <!-- Services Grid -->
    <section class="service-grid">
        <div class="service-card">
            <i class="fas fa-briefcase fa-2x" style="color: var(--accent);"></i>
            <h3>Handwriting Analysis</h3>
            <p>Comprehensive personality and career assessment through handwriting</p>
            <button class="cyber-button">Analyze Now</button>
        </div>

        <div class="service-card">
            <i class="fas fa-heart fa-2x" style="color: var(--accent);"></i>
            <h3>Relationship Compatibility</h3>
            <p>Comparative analysis for better relationship understanding</p>
            <button class="cyber-button">Compare Now</button>
        </div>

        <div class="service-card">
            <i class="fas fa-signature fa-2x" style="color: var(--accent);"></i>
            <h3>Signature Analysis</h3>
            <p>Professional signature evaluation and optimization</p>
            <button class="cyber-button">Optimize Now</button>
        </div>

        <div class="service-card">
            <i class="fas fa-users fa-2x" style="color: var(--accent);"></i>
            <h3>HR Solutions</h3>
            <p>Enhance your hiring process with scientific handwriting analysis</p>
            <ul class="feature-list">
                <li>Candidate Screening</li>
                <li>Team Compatibility</li>
                <li>Leadership Assessment</li>
            </ul>
            <button class="cyber-button">Learn More</button>
        </div>

        <div class="service-card">
            <i class="fas fa-chart-line fa-2x" style="color: var(--accent);"></i>
            <h3>Talent Assessment</h3>
            <p>Scientific approach to talent identification and development</p>
            <ul class="feature-list">
                <li>Potential Analysis</li>
                <li>Skill Mapping</li>
                <li>Growth Prediction</li>
            </ul>
            <button class="cyber-button">Explore</button>
        </div>

        <div class="service-card">
            <i class="fas fa-handshake fa-2x" style="color: var(--accent);"></i>
            <h3>Enterprise Packages</h3>
            <p>Customized solutions for large-scale implementations</p>
            <ul class="feature-list">
                <li>Custom Integration</li>
                <li>Bulk Analysis</li>
                <li>Dedicated Support</li>
            </ul>
            <button class="cyber-button">Get Quote</button>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="pricing-section">
        <div class="section-header">
            <h2 class="cyber-text">Analysis Packages</h2>
            <p style="color: var(--paper);">Professional graphology solutions for every need</p>
        </div>
        <div class="pricing-grid">
            <div class="price-card">
                <h3>Single Day Analysis</h3>
                <p style="color: var(--accent); font-size: 0.9em; margin-top: 0.5em;">Includes one free follow-up session</p>
                <ul class="feature-list">
                    <li>Handwriting Analysis
                        <div class="price" style="font-size: 1.8rem;">₹4,000 / $50</div>
                    </li>
                    <li>Signature Analysis
                        <div class="price" style="font-size: 1.8rem;">₹2,000 / $25</div>
                    </li>
                    <li>Relationship Compatibility
                        <div class="price" style="font-size: 1.5rem;">Couples: ₹1,200 / $15</div>
                        <div class="price" style="font-size: 1.5rem;">Individual: ₹750 / $10</div>
                    </li>
                </ul>
                <button class="cyber-button">Get Started</button>
            </div>

            <div class="price-card">
                <h3>Multiple Day Analysis</h3>
                <p style="color: var(--accent); font-size: 0.9em; margin-top: 0.5em;">Minimum 4 Sessions + 2 Free Follow-ups</p>
                <div class="price">₹1,000 / $15</div>
                <p style="color: var(--paper);">per session</p>
                <ul class="feature-list">
                    <li>Comprehensive Handwriting Analysis</li>
                    <li>Career Assessment</li>
                    <li>Personality Profiling</li>
                    <li>Extended Consultation</li>
                </ul>
                <button class="cyber-button">Choose Plan</button>
            </div>

            <div class="price-card">
                <h3>Corporate Solutions</h3>
                <ul class="feature-list">
                    <li>Employee Assessment
                        <div class="price" style="font-size: 1.8rem;">₹4,000 / $50</div>
                        <p style="color: var(--paper);">per employee</p>
                    </li>
                    <li>Logo Analysis
                        <p style="color: var(--accent);">Custom Quote</p>
                        <p style="color: var(--paper); font-size: 0.9em;">Varies based on logo and company</p>
                    </li>
                </ul>
                <button class="cyber-button">Contact Sales</button>
            </div>
        </div>
    </section>

    <!-- Contact Us Section -->
    <section class="contact-section">
        <div class="section-header">
            <h2 class="cyber-text">Connect With Us</h2>
            <p style="color: var(--paper);">Get in touch for personalized analysis</p>
        </div>
        <div class="contact-grid">
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-envelope fa-2x" style="color: var(--accent);"></i>
                    <h3>Email</h3>
                    <p>satyakiadityamitra18@gmail.com</p>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone fa-2x" style="color: var(--accent);"></i>
                    <h3>Phone</h3>
                    <p>+91 9903787384</p>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt fa-2x" style="color: var(--accent);"></i>
                    <h3>Location</h3>
                    <p>Kolkata, India</p>
                    <p style="font-size: 0.9em; margin-top: 0.5em; color: var(--accent);">
                        <i class="fas fa-globe"></i> Online Services Available Worldwide
                    </p>
                </div>
            </div>
            <form class="contact-form">
                <div class="form-group">
                    <input type="text" placeholder="Your Name" required class="cyber-input">
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Your Email" required class="cyber-input">
                </div>
                <div class="form-group">
                    <select class="cyber-input">
                        <option value="">Select Service</option>
                        <option value="handwriting">Handwriting Analysis</option>
                        <option value="signature">Signature Analysis</option>
                        <option value="relationship">Relationship Compatibility</option>
                        <option value="corporate">Corporate Solutions</option>
                    </select>
                </div>
                <div class="form-group">
                    <textarea placeholder="Your Message" required class="cyber-input" rows="4"></textarea>
                </div>
                <button type="submit" class="cyber-button">
                    <i class="fas fa-paper-plane"></i> Send Message
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <section class="about-us">
            <h2><i class="fas fa-pen-nib"></i> About Us</h2>
            <p>Decoding personalities through advanced graphology since 2023</p>
            <button class="cyber-button">
                <i class="fas fa-book-open"></i> Read More
            </button>
        </section>
    </footer>
</body>
</html>
