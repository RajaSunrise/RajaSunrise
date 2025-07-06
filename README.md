<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RajaSunrise | Backend Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6C63FF;
            --secondary: #FF6584;
            --dark: #121826;
            --darker: #0D1117;
            --light: #F8F9FA;
            --gray: #9CA3AF;
            --transition: all 0.3s ease;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: var(--darker);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        .header {
            background: var(--dark);
            padding: 40px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
            margin-bottom: 60px;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--gradient);
            opacity: 0.1;
            z-index: 0;
        }
        
        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid var(--primary);
            position: relative;
            z-index: 1;
            object-fit: cover;
            background: var(--dark);
            padding: 5px;
            margin: 0 auto 20px;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: var(--gray);
            font-weight: 300;
        }
        
        .typing-effect {
            display: inline-block;
            height: 60px;
            overflow: hidden;
        }
        
        .typing-line {
            display: inline-block;
            animation: typing 4s steps(40, end) infinite;
            white-space: nowrap;
            overflow: hidden;
            border-right: 2px solid var(--primary);
            font-size: 1.8rem;
            font-weight: 600;
            color: var(--light);
        }
        
        @keyframes typing {
            0% { width: 0 }
            25% { width: 100% }
            75% { width: 100% }
            100% { width: 0 }
        }
        
        /* Sections */
        .section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
            font-size: 2.5rem;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }
        
        /* About */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }
        
        .about-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            padding: 30px;
            box-shadow: var(--shadow);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
        }
        
        .about-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .about-card h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .info-item {
            display: flex;
            margin-bottom: 15px;
        }
        
        .info-icon {
            width: 40px;
            height: 40px;
            background: var(--gradient);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            flex-shrink: 0;
        }
        
        .info-content h4 {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }
        
        .info-content p {
            color: var(--gray);
        }
        
        /* Skills */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 25px;
        }
        
        .skill-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .skill-card:hover {
            background: rgba(108, 99, 255, 0.1);
            transform: translateY(-5px);
        }
        
        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .skill-name {
            font-size: 1.2rem;
            font-weight: 600;
        }
        
        /* Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            box-shadow: var(--shadow);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
        }
        
        .stat-card:hover {
            background: rgba(108, 99, 255, 0.1);
        }
        
        .stat-value {
            font-size: 3rem;
            font-weight: 700;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 10px;
        }
        
        .stat-label {
            font-size: 1.2rem;
            color: var(--gray);
        }
        
        /* Connect */
        .connect-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .connect-btn {
            display: flex;
            align-items: center;
            padding: 15px 30px;
            border-radius: 50px;
            background: rgba(255, 255, 255, 0.05);
            color: var(--light);
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .connect-btn:hover {
            background: var(--gradient);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(108, 99, 255, 0.3);
        }
        
        .connect-btn i {
            margin-right: 10px;
            font-size: 1.5rem;
        }
        
        /* Footer */
        .footer {
            background: var(--dark);
            padding: 40px 0;
            text-align: center;
            margin-top: 60px;
            position: relative;
        }
        
        .footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--gradient);
            opacity: 0.05;
            z-index: 0;
        }
        
        .footer-content {
            position: relative;
            z-index: 1;
        }
        
        .footer p {
            color: var(--gray);
            margin-top: 20px;
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .about-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .typing-line {
                font-size: 1.4rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header class="header">
        <div class="container">
            <div class="header-content">
                <img src="https://avatars.githubusercontent.com/u/12345678?v=4" alt="RajaSunrise" class="profile-pic floating">
                <h1>RajaSunrise</h1>
                <p class="tagline">Backend Engineer | System Architect | Problem Solver</p>
                <div class="typing-effect">
                    <span class="typing-line">Building scalable systems</span>
                </div>
            </div>
        </div>
    </header>
    
    <!-- About Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-grid">
                <div class="about-card">
                    <h3>👨‍💻 Profile</h3>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-code"></i>
                        </div>
                        <div class="info-content">
                            <h4>Backend Engineer</h4>
                            <p>Building robust and efficient systems</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="info-content">
                            <h4>Indonesia</h4>
                            <p>Based in Jakarta</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-rocket"></i>
                        </div>
                        <div class="info-content">
                            <h4>Current Focus</h4>
                            <p>Advanced Go, Microservices & System Design</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="info-content">
                            <h4>Contact</h4>
                            <p>indra020204@gmail.com</p>
                        </div>
                    </div>
                </div>
                
                <div class="about-card">
                    <h3>🚀 Bio</h3>
                    <p>Hello! I'm RajaSunrise, a passionate Backend Engineer based in Indonesia with expertise in building efficient and scalable web applications and systems.</p>
                    <br>
                    <p>I specialize in designing robust architectures and solving complex technical challenges. My approach combines deep technical knowledge with a focus on performance and maintainability.</p>
                    <br>
                    <p>🔭 Currently working on <strong>distributed systems architecture</strong></p>
                    <p>🌱 Learning <strong>cloud-native development and advanced system design</strong></p>
                    <p>💬 Ask me about <strong>backend architecture, API design, or database optimization</strong></p>
                    <p>⚡ Fun fact: <strong>I see code as a form of artistic expression</strong></p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Skills Section -->
    <section class="section" style="background: rgba(18, 24, 38, 0.7);">
        <div class="container">
            <h2 class="section-title">Tech Stack</h2>
            <div class="skills-container">
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-golang"></i>
                    </div>
                    <div class="skill-name">Go</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-python"></i>
                    </div>
                    <div class="skill-name">Python</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-node"></i>
                    </div>
                    <div class="skill-name">Node.js</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <div class="skill-name">PostgreSQL</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <div class="skill-name">MySQL</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-database"></i>
                    </div>
                    <div class="skill-name">MongoDB</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-docker"></i>
                    </div>
                    <div class="skill-name">Docker</div>
                </div>
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fab fa-aws"></i>
                    </div>
                    <div class="skill-name">AWS</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Stats Section -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">GitHub Analytics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-value">1.5K+</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">50+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">120+</div>
                    <div class="stat-label">Contributions</div>
                </div>
            </div>
            
            <div class="about-card" style="margin-top: 30px;">
                <h3>📊 Activity Metrics</h3>
                <div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; margin-top: 20px;">
                    <div style="background: #161B22; padding: 15px; border-radius: 10px;">
                        <img src="https://github-readme-stats.vercel.app/api?username=RajaSunrise&show_icons=true&theme=dark&title_color=6C63FF&icon_color=FF6584&text_color=ffffff&bg_color=0D1117&hide_border=true" alt="GitHub Stats">
                    </div>
                    <div style="background: #161B22; padding: 15px; border-radius: 10px;">
                        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=RajaSunrise&layout=compact&theme=dark&title_color=6C63FF&text_color=ffffff&bg_color=0D1117&hide_border=true&langs_count=8" alt="Top Languages">
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Connect Section -->
    <section class="section" style="background: rgba(18, 24, 38, 0.7);">
        <div class="container">
            <h2 class="section-title">Let's Connect</h2>
            <div class="connect-container">
                <a href="https://www.linkedin.com/in/indra-aryadi-961a98243" class="connect-btn">
                    <i class="fab fa-linkedin-in"></i> LinkedIn
                </a>
                <a href="mailto:indra020204@gmail.com" class="connect-btn">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://twitter.com/indra_aryadi" class="connect-btn">
                    <i class="fab fa-twitter"></i> Twitter
                </a>
                <a href="https://github.com/RajaSunrise" class="connect-btn">
                    <i class="fab fa-github"></i> GitHub
                </a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <h3>RajaSunrise</h3>
                <p>Backend Engineer | System Architect</p>
                <p>&copy; 2023 RajaSunrise. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Typing effect with multiple lines
        const lines = [
            "Building scalable systems",
            "Creating efficient solutions",
            "Designing robust architectures",
            "Optimizing backend performance"
        ];
        
        let lineIndex = 0;
        const typingElement = document.querySelector('.typing-line');
        
        function typeLine() {
            let line = lines[lineIndex];
            let charIndex = 0;
            let typing = "";
            
            function type() {
                if (charIndex < line.length) {
                    typing += line.charAt(charIndex);
                    typingElement.textContent = typing;
                    charIndex++;
                    setTimeout(type, 100);
                } else {
                    setTimeout(erase, 1500);
                }
            }
            
            function erase() {
                if (typing.length > 0) {
                    typing = typing.substring(0, typing.length - 1);
                    typingElement.textContent = typing;
                    setTimeout(erase, 50);
                } else {
                    lineIndex = (lineIndex + 1) % lines.length;
                    setTimeout(typeLine, 500);
                }
            }
            
            type();
        }
        
        document.addEventListener('DOMContentLoaded', typeLine);
    </script>
</body>
</html>