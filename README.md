<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MR.DRIVES: HUMANI - AI for Social Change</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700;800;900&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --navy-blue: #001a33;
            --deep-blue: #00264d;
            --accent-blue: #00a8ff;
            --light-blue: #4da6ff;
            --text-light: #e6f2ff;
            --orange: #ff8c00;
        }
        
        body {
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-blue));
            font-family: 'Poppins', sans-serif;
            color: var(--text-light);
            min-height: 100vh;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            border-bottom: 1px solid rgba(0, 150, 255, 0.2);
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo-circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--accent-blue), #0066cc);
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .logo-text {
            text-align: left;
        }
        
        .logo-text h1 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 900;
            font-size: 28px;
            letter-spacing: 1px;
            text-transform: uppercase;
            background: linear-gradient(to right, #ffffff, #a0d2ff);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 5px;
        }
        
        .logo-text h2 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 16px;
            letter-spacing: 2px;
            color: var(--light-blue);
        }
        
        nav ul {
            display: flex;
            gap: 30px;
            list-style: none;
        }
        
        nav a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            font-size: 18px;
            transition: color 0.3s;
            position: relative;
        }
        
        nav a:hover {
            color: var(--accent-blue);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-blue);
            transition: width 0.3s;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        /* YouTube Banner Section */
        .banner {
            background: linear-gradient(135deg, var(--navy-blue), var(--deep-blue));
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            position: relative;
            padding: 80px 40px;
            margin: 40px 0;
            border: 1px solid rgba(0, 150, 255, 0.2);
        }
        
        .banner::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(0, 100, 200, 0.15) 0%, transparent 30%),
                radial-gradient(circle at 90% 80%, rgba(0, 150, 255, 0.1) 0%, transparent 30%);
            z-index: 0;
        }
        
        .banner-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }
        
        .tagline {
            font-size: 24px;
            line-height: 1.6;
            margin: 30px 0;
            color: var(--text-light);
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .tagline span.highlight {
            color: var(--accent-blue);
            font-weight: 600;
        }
        
        .ai-elements {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        
        .ai-element {
            background: rgba(0, 40, 80, 0.5);
            border-radius: 15px;
            padding: 25px;
            width: 220px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(0, 150, 255, 0.3);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .ai-element:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 100, 200, 0.4);
            border-color: rgba(0, 200, 255, 0.6);
        }
        
        .ai-element i {
            font-size: 42px;
            color: var(--accent-blue);
            margin-bottom: 20px;
        }
        
        .ai-element h3 {
            font-size: 20px;
            margin-bottom: 10px;
            color: #a0d2ff;
        }
        
        .ai-element p {
            font-size: 15px;
            color: #cce6ff;
        }
        
        .banner-footer {
            margin-top: 50px;
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        .social-btn {
            background: rgba(0, 60, 120, 0.6);
            border: 2px solid rgba(0, 150, 255, 0.4);
            color: #66c2ff;
            padding: 12px 30px;
            border-radius: 30px;
            font-size: 18px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .social-btn:hover {
            background: rgba(0, 100, 200, 0.8);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 120, 255, 0.4);
        }
        
        .social-btn i {
            font-size: 24px;
        }
        
        .subscribe-btn {
            background: linear-gradient(135deg, #ff4d00, var(--orange));
            color: white;
            border: none;
            padding: 14px 40px;
            border-radius: 30px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(255, 77, 0, 0.4);
        }
        
        .subscribe-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 77, 0, 0.6);
            background: linear-gradient(135deg, #ff5c1a, #ff9a00);
        }
        
        /* Publishing Guide Section */
        .guide-section {
            background: rgba(0, 30, 60, 0.6);
            border-radius: 20px;
            padding: 40px;
            margin: 40px 0;
            border: 1px solid rgba(0, 100, 200, 0.3);
        }
        
        .guide-section h2 {
            text-align: center;
            margin-bottom: 30px;
            color: var(--light-blue);
            font-size: 32px;
        }
        
        .steps-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }
        
        .step-card {
            background: rgba(0, 40, 80, 0.4);
            border-radius: 15px;
            padding: 25px;
            width: 300px;
            border: 1px solid rgba(0, 150, 255, 0.3);
            transition: transform 0.3s;
        }
        
        .step-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent-blue);
        }
        
        .step-number {
            background: var(--accent-blue);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 20px;
            margin-bottom: 20px;
        }
        
        .step-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--text-light);
        }
        
        .step-card p {
            color: #cce6ff;
            margin-bottom: 15px;
        }
        
        .step-link {
            color: var(--accent-blue);
            text-decoration: none;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        
        .step-link:hover {
            text-decoration: underline;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid rgba(0, 150, 255, 0.2);
            margin-top: 40px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 20px 0;
            flex-wrap: wrap;
        }
        
        .footer-links a {
            color: var(--text-light);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--accent-blue);
        }
        
        .copyright {
            color: var(--light-blue);
            margin-top: 20px;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .banner {
                padding: 40px 20px;
            }
            
            .tagline {
                font-size: 20px;
            }
            
            .ai-element {
                width: 100%;
                max-width: 300px;
            }
        }
        
        @media (max-width: 480px) {
            .tagline {
                font-size: 18px;
            }
            
            .banner-footer {
                flex-direction: column;
                align-items: center;
            }
            
            .social-btn, .subscribe-btn {
                width: 100%;
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <div class="logo-circle">
                    <i class="fas fa-brain" style="font-size: 28px; color: white;"></i>
                </div>
                <div class="logo-text">
                    <h1>MRDRIVES</h1>
                    <h2>HUMANI</h2>
                </div>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#"><i class="fas fa-home"></i> Home</a></li>
                    <li><a href="#"><i class="fas fa-video"></i> Videos</a></li>
                    <li><a href="#"><i class="fas fa-music"></i> Music</a></li>
                    <li><a href="#"><i class="fas fa-book"></i> Stories</a></li>
                    <li><a href="#"><i class="fas fa-info-circle"></i> About</a></li>
                </ul>
            </nav>
        </header>
        
        <section class="banner">
            <div class="banner-content">
                <div class="logo" style="justify-content: center; margin-bottom: 30px;">
                    <div class="logo-circle" style="width: 100px; height: 100px; margin-right: 20px;">
                        <i class="fas fa-brain" style="font-size: 48px; color: white;"></i>
                    </div>
                    <div class="logo-text">
                        <h1>MRDRIVES: HUMANI</h1>
                        <h2>MRDRIVES CHANNEL</h2>
                    </div>
                </div>
                
                <p class="tagline">
                    Explore impactful stories, music, and videos that inspire and 
                    <span class="highlight">motivate human connection</span> 
                    through with <span class="highlight">AI technology</span>.
                </p>
                
                <div class="ai-elements">
                    <div class="ai-element">
                        <i class="fas fa-book-open"></i>
                        <h3>Impactful Stories</h3>
                        <p>Narratives that drive social change and inspire action</p>
                    </div>
                    
                    <div class="ai-element">
                        <i class="fas fa-music"></i>
                        <h3>Inspiring Music</h3>
                        <p>Curated playlists that move the soul and motivate change</p>
                    </div>
                    
                    <div class="ai-element">
                        <i class="fas fa-video"></i>
                        <h3>Transformative Videos</h3>
                        <p>Visual content that challenges perspectives and drives impact</p>
                    </div>
                </div>
                
                <div class="banner-footer">
                    <a href="#" class="social-btn">
                        <i class="fab fa-youtube"></i> YouTube Channel
                    </a>
                    <button class="subscribe-btn" id="subscribeBtn">
                        <i class="fas fa-bell"></i> Subscribe
                    </button>
                    <a href="#" class="social-btn">
                        <i class="fas fa-share-alt"></i> Share
                    </a>
                </div>
            </div>
        </section>
        
        <section class="guide-section">
            <h2><i class="fas fa-cloud-upload-alt"></i> How to Publish Your Website for Free</h2>
            <div class="steps-container">
                <div class="step-card">
                    <div class="step-number">1</div>
                    <h3>Create a GitHub Account</h3>
                    <p>Go to github.com and sign up for a free account if you don't have one.</p>
                    <a href="https://github.com/" target="_blank" class="step-link">
                        Visit GitHub <i class="fas fa-external-link-alt"></i>
                    </a>
                </div>
                
                <div class="step-card">
                    <div class="step-number">2</div>
                    <h3>Create a New Repository</h3>
                    <p>Click the "+" icon and select "New repository". Name it your-project-name.</p>
                    <a href="https://github.com/new" target="_blank" class="step-link">
                        Create Repository <i class="fas fa-external-link-alt"></i>
                    </a>
                </div>
                
                <div class="step-card">
                    <div class="step-number">3</div>
                    <h3>Upload Your Files</h3>
                    <p>Click "Add file" → "Upload files". Drag and drop your HTML file (and other assets).</p>
                    <p>Name your main file <strong>index.html</strong></p>
                </div>
                
                <div class="step-card">
                    <div class="step-number">4</div>
                    <h3>Enable GitHub Pages</h3>
                    <p>Go to Settings → Pages. Under "Source", select the branch (main) and folder (root).</p>
                    <p>Click "Save" and wait for deployment.</p>
                </div>
                
                <div class="step-card">
                    <div class="step-number">5</div>
                    <h3>Access Your Website</h3>
                    <p>Your site will be available at:</p>
                    <p><strong>https://your-username.github.io/repository-name</strong></p>
                    <p>It may take a few minutes to become active.</p>
                </div>
                
                <div class="step-card">
                    <div class="step-number">6</div>
                    <h3>Update Your Site</h3>
                    <p>To make changes, edit your files locally and re-upload to GitHub. Your site will automatically update.</p>
                    <p>GitHub Pages is completely free for public repositories.</p>
                </div>
            </div>
        </section>
        
        <footer>
            <div class="footer-links">
                <a href="#"><i class="fab fa-youtube"></i> YouTube</a>
                <a href="#"><i class="fab fa-facebook"></i> Facebook</a>
                <a href="#"><i class="fab fa-instagram"></i> Instagram</a>
                <a href="#"><i class="fab fa-twitter"></i> Twitter</a>
                <a href="#"><i class="fab fa-tiktok"></i> TikTok</a>
            </div>
            
            <p class="copyright">© 2023 MR.DRIVES: HUMANI | AI for Social Change</p>
            <p>Explore impactful stories, music, and videos that inspire and motivate human connection</p>
        </footer>
    </div>

    <script>
        // Subscription button functionality
        document.getElementById('subscribeBtn').addEventListener('click', function() {
            this.innerHTML = '<i class="fas fa-check"></i> Subscribed!';
            this.style.background = 'linear-gradient(135deg, #28a745, #2ecc71)';
            this.style.boxShadow = '0 5px 15px rgba(46, 204, 113, 0.4)';
            
            setTimeout(() => {
                this.innerHTML = '<i class="fas fa-bell"></i> Subscribed';
            }, 2000);
        });
        
        // Animation for step cards
        document.querySelectorAll('.step-card').forEach((card, index) => {
            card.style.animation = `fadeIn 0.5s ease-out ${index * 0.1}s forwards`;
            card.style.opacity = '0';
        });
        
        // Add CSS animation
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes fadeIn {
                from { opacity: 0; transform: translateY(20px); }
                to { opacity: 1; transform: translateY(0); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
