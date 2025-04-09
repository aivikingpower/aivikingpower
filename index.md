<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Viking Power</title>
    <style>
        :root {
            --viking-blue: #1a3c5e;
            --viking-gold: #d4af37;
            --dark-gray: #333333;
            --light-gray: #f5f5f5;
            --white: #ffffff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-gray);
            color: var(--dark-gray);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: var(--viking-blue);
            color: var(--white);
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--white);
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo-icon {
            margin-right: 10px;
            font-size: 2.8rem;
        }
        
        .hero {
            background: linear-gradient(135deg, var(--viking-blue) 0%, #2a5078 100%);
            color: var(--white);
            padding: 80px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: url('/api/placeholder/1200/800');
            background-size: cover;
            background-position: center;
            opacity: 0.15;
            z-index: 0;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--viking-gold);
            color: var(--dark-gray);
            padding: 12px 24px;
            font-size: 1.1rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 4px;
            transition: all 0.3s ease;
            border: 2px solid var(--viking-gold);
        }
        
        .cta-button:hover {
            background-color: transparent;
            color: var(--white);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.2rem;
            color: var(--viking-blue);
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--viking-gold);
        }
        
        .services {
            background-color: var(--white);
        }
        
        .service-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: var(--light-gray);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .service-card-header {
            background-color: var(--viking-blue);
            color: var(--white);
            padding: 20px;
            text-align: center;
        }
        
        .service-card-header h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .service-price {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .service-card-body {
            padding: 20px;
            text-align: left;
        }
        
        .service-card-body p {
            margin-bottom: 20px;
        }
        
        .results {
            background-color: var(--light-gray);
        }
        
        .result-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .result-item {
            background-color: var(--white);
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .result-item h3 {
            color: var(--viking-blue);
            margin-bottom: 10px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }
        
        .check-icon {
            color: green;
            margin-right: 10px;
        }
        
        .advantages {
            background-color: var(--white);
        }
        
        .advantage-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .advantage-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 15px;
        }
        
        .advantage-icon {
            margin-right: 15px;
            color: var(--viking-gold);
            font-size: 1.5rem;
        }
        
        .book-session {
            background: linear-gradient(135deg, var(--viking-blue) 0%, #2a5078 100%);
            color: var(--white);
            text-align: center;
            position: relative;
        }
        
        .book-session::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: url('/api/placeholder/1200/800');
            background-size: cover;
            background-position: center;
            opacity: 0.1;
            z-index: 0;
        }
        
        .book-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .book-session h2 {
            color: var(--white);
        }
        
        footer {
            background-color: var(--viking-blue);
            color: var(--white);
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .footer-logo {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .contact-info {
            margin-bottom: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 10px;
        }
        
        .contact-icon {
            margin-right: 10px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }
        
        .social-link:hover {
            color: var(--viking-gold);
        }
        
        .copyright {
            margin-top: 30px;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 1.5rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.3rem;
            }
            
            .service-cards,
            .result-items,
            .advantage-list {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <span class="logo-icon">⚔️</span>
                AI Viking Power
            </a>
            <nav>
                <!-- Navigation would go here if needed -->
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="container hero-content">
            <h1>Viking Power – Helping Business Owners Master AI Without the Hype</h1>
            <p>I'm Marcus Erickson — a product strategist, software leader, and AI educator with 30+ years of experience. Through AI Viking Power, I help business owners and teams harness the power of AI to save time, sharpen communication, and grow smarter — not harder.</p>
            <p>Whether you're just curious about tools like ChatGPT or ready to integrate AI into your daily operations, I'm here to make it simple and useful.</p>
            <a href="#book" class="cta-button">Book a Session</a>
        </div>
    </section>
    
    <section class="services">
        <div class="container">
            <h2 class="section-title">⚙️ What I Offer</h2>
            <div class="service-cards">
                <div class="service-card">
                    <div class="service-card-header">
                        <h3>AI Jumpstart Session</h3>
                        <div class="service-price">1-on-1 Zoom – $150</div>
                    </div>
                    <div class="service-card-body">
                        <p>Get clear, immediate ideas for how AI can save you time. We'll walk through your business together and I'll give you 3–5 ways to start using AI right away.</p>
                        <p>You'll leave with a custom prompt set tailored to your work.</p>
                        <a href="#book" class="cta-button">Book Now</a>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-card-header">
                        <h3>Team AI Workshop</h3>
                        <div class="service-price">Live Zoom Training – $500–$750</div>
                    </div>
                    <div class="service-card-body">
                        <p>90-minute training for your team. We'll explore real use cases and get hands-on with AI tools like ChatGPT, Claude, or Copilot.</p>
                        <p>Everyone walks away with confidence and ready-to-use prompts.</p>
                        <a href="#book" class="cta-button">Book Now</a>
                    </div>
                </div>
                
                <div class="service-card">
                    <div class="service-card-header">
                        <h3>AI Prompt Partner Plan</h3>
                        <div class="service-price">Ongoing Monthly Support – $600+</div>
                    </div>
                    <div class="service-card-body">
                        <p>Monthly coaching and tool setup support. I'll help build a prompt library for your team, streamline your workflows, and guide you as you scale up your use of AI.</p>
                        <a href="#book" class="cta-button">Book Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="results">
        <div class="container">
            <h2 class="section-title">🔧 Real-World Results</h2>
            <div class="result-items">
                <div class="result-item">
                    <h3><span class="check-icon">✅</span> Time Savings</h3>
                    <p>Saved one local business 4+ hours/week in email writing with custom prompt templates.</p>
                </div>
                
                <div class="result-item">
                    <h3><span class="check-icon">✅</span> Real Estate Automation</h3>
                    <p>Helped a real estate team automate client summaries and listing descriptions.</p>
                </div>
                
                <div class="result-item">
                    <h3><span class="check-icon">✅</span> Nonprofit Support</h3>
                    <p>Guided a nonprofit in using ChatGPT to draft grant applications and reports.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="advantages">
        <div class="container">
            <h2 class="section-title">⚔️ The AI Viking Power Advantage</h2>
            <div class="advantage-list">
                <div class="advantage-item">
                    <span class="advantage-icon">•</span>
                    <div>
                        <p>Straightforward, no-jargon training</p>
                    </div>
                </div>
                
                <div class="advantage-item">
                    <span class="advantage-icon">•</span>
                    <div>
                        <p>Focused on your actual work — not abstract theory</p>
                    </div>
                </div>
                
                <div class="advantage-item">
                    <span class="advantage-icon">•</span>
                    <div>
                        <p>Evening and weekend sessions available</p>
                    </div>
                </div>
                
                <div class="advantage-item">
                    <span class="advantage-icon">•</span>
                    <div>
                        <p>Always tailored to your team, industry, and comfort level</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section class="book-session" id="book">
        <div class="container book-content">
            <h2 class="section-title">🎯 Book a Session or Ask a Question</h2>
            <p>Ready to see what AI can do for you?</p>
            <p>👉 <a href="#" class="cta-button">Book a Session</a></p>
            <p style="margin-top: 20px;">Or email me directly at <a href="mailto:aivikingpower@gmail.com" style="color: var(--viking-gold);">aivikingpower@gmail.com</a></p>
            <p style="margin-top: 20px; font-size: 1.3rem; font-weight: 600;">Let's make AI make sense.</p>
        </div>
    </section>
    
    <footer>
        <div class="container footer-content">
            <div class="footer-logo">
                <span class="logo-icon">⚔️</span>
                AI Viking Power
            </div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span class="contact-icon">📧</span>
                    <a href="mailto:aivikingpower@gmail.com" style="color: var(--viking-gold); text-decoration: none;">marcuse@alumni.rice.edu</a>
                </div>
                
                <div class="contact-item">
                    <span class="contact-icon">📍</span>
                    Missouri City, Texas
                </div>
            </div>
            
            <div class="social-links">
                <a href="#" class="social-link">LinkedIn</a>
            </div>
            
            <div class="copyright">
                <p>Skål to smarter business.</p>
                <p style="margin-top: 10px;">© 2025 AI Viking Power. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
