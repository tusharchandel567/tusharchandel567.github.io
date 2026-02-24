<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Tushar Chandel - Frontend Developer Portfolio. Specializing in React.js, JavaScript, HTML5, CSS3. View my projects and experience.">
    <meta name="keywords" content="Frontend Developer, React Developer, Web Developer, JavaScript, HTML5, CSS3, Portfolio">
    <title>Tushar Chandel - Frontend Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #0066cc;
            --secondary-color: #00a8e8;
            --dark-bg: #0a0f1c;
            --light-bg: #1a1f35;
            --text-primary: #ffffff;
            --text-secondary: #b8c1ec;
            --accent: #00ffcc;
            --card-bg: #1e2642;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--dark-bg);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 15, 28, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 5%;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 102, 204, 0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--accent);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--dark-bg) 0%, var(--light-bg) 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(0, 102, 204, 0.1) 0%, transparent 70%);
            top: -250px;
            right: -250px;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content {
            max-width: 800px;
            z-index: 1;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--accent), var(--primary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero h2 {
            font-size: 1.8rem;
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 102, 204, 0.4);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--accent);
        }

        .btn-secondary:hover {
            background: var(--accent);
            color: var(--dark-bg);
            transform: translateY(-3px);
        }

        /* Section Styling */
        section {
            padding: 5rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent));
            border-radius: 2px;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(0, 168, 232, 0.1);
            transition: all 0.3s;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
            box-shadow: 0 10px 30px rgba(0, 255, 204, 0.1);
        }

        .skill-category h3 {
            color: var(--accent);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .skill-tag {
            background: rgba(0, 102, 204, 0.2);
            color: var(--text-secondary);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(0, 102, 204, 0.3);
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid rgba(0, 168, 232, 0.1);
            transition: all 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 255, 204, 0.2);
            border-color: var(--accent);
        }

        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-content h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }

        .project-content p {
            color: var(--text-secondary);
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .tech-badge {
            background: rgba(0, 255, 204, 0.1);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.85rem;
            border: 1px solid rgba(0, 255, 204, 0.3);
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .project-link:hover {
            color: var(--primary-color);
        }

        /* Experience Section */
        .timeline {
            position: relative;
            padding-left: 3rem;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(180deg, var(--accent), var(--primary-color));
        }

        .timeline-item {
            position: relative;
            margin-bottom: 3rem;
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(0, 168, 232, 0.1);
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -3.5rem;
            top: 2rem;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: var(--accent);
            border: 3px solid var(--dark-bg);
        }

        .timeline-item h3 {
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .timeline-date {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .timeline-item ul {
            list-style: none;
            padding-left: 1rem;
        }

        .timeline-item li {
            color: var(--text-secondary);
            margin-bottom: 0.5rem;
            position: relative;
        }

        .timeline-item li::before {
            content: '▹';
            position: absolute;
            left: -1rem;
            color: var(--accent);
        }

        /* Contact Section */
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .contact-item {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 15px;
            border: 1px solid rgba(0, 168, 232, 0.1);
            transition: all 0.3s;
        }

        .contact-item:hover {
            border-color: var(--accent);
            transform: translateX(5px);
        }

        .contact-item a {
            color: var(--accent);
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
        }

        .contact-item span {
            display: block;
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--card-bg);
            border-radius: 50%;
            color: var(--accent);
            text-decoration: none;
            font-size: 1.5rem;
            border: 2px solid rgba(0, 168, 232, 0.2);
            transition: all 0.3s;
        }

        .social-link:hover {
            background: var(--accent);
            color: var(--dark-bg);
            transform: translateY(-5px);
        }

        /* Footer */
        footer {
            background: var(--light-bg);
            text-align: center;
            padding: 2rem;
            color: var(--text-secondary);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h2 {
                font-size: 1.3rem;
            }

            section {
                padding: 3rem 5%;
            }

            .section-title {
                font-size: 2rem;
            }

            .timeline {
                padding-left: 2rem;
            }

            .timeline-item::before {
                left: -2.5rem;
            }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Loading Animation */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        section {
            animation: fadeIn 0.8s ease-out;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#home" class="logo">TC</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Tushar Chandel</h1>
            <h2>Frontend Developer | React.js Specialist</h2>
            <p>
                Passionate about creating beautiful, responsive, and user-friendly web applications. 
                Specialized in React.js, JavaScript, and modern frontend technologies with 1+ years of experience 
                building production-ready applications.
            </p>
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">View My Work</a>
                <a href="#contact" class="btn btn-secondary">Get In Touch</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2 class="section-title">About Me</h2>
        <div style="max-width: 800px; margin: 0 auto; text-align: center;">
            <p style="font-size: 1.1rem; color: var(--text-secondary); line-height: 1.8; margin-bottom: 1.5rem;">
                I'm a Computer Science student at Meerut Institute of Technology with a strong passion for frontend development. 
                I specialize in building responsive, accessible, and high-performance web applications using modern technologies 
                like React.js, JavaScript ES6+, HTML5, and CSS3.
            </p>
            <p style="font-size: 1.1rem; color: var(--text-secondary); line-height: 1.8;">
                With FreeCodeCamp certifications in Responsive Web Design and Python Programming, I've developed 10+ production-ready 
                web applications, improving performance by 40% through optimization techniques. I'm always eager to learn new 
                technologies and best practices to create exceptional user experiences.
            </p>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2 class="section-title">Technical Skills</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>Frontend Development</h3>
                <div class="skill-tags">
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">JavaScript ES6+</span>
                    <span class="skill-tag">React.js</span>
                    <span class="skill-tag">Redux</span>
                    <span class="skill-tag">TypeScript</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>CSS Frameworks</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Flexbox</span>
                    <span class="skill-tag">CSS Grid</span>
                    <span class="skill-tag">Bootstrap</span>
                    <span class="skill-tag">Tailwind CSS</span>
                    <span class="skill-tag">SASS</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>Tools & Technologies</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Git & GitHub</span>
                    <span class="skill-tag">Webpack</span>
                    <span class="skill-tag">Vite</span>
                    <span class="skill-tag">NPM</span>
                    <span class="skill-tag">VS Code</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>UI/UX & Design</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Figma</span>
                    <span class="skill-tag">Adobe XD</span>
                    <span class="skill-tag">Responsive Design</span>
                    <span class="skill-tag">Accessibility</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>Performance & SEO</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Core Web Vitals</span>
                    <span class="skill-tag">Lazy Loading</span>
                    <span class="skill-tag">Code Splitting</span>
                    <span class="skill-tag">SEO Optimization</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>Backend & APIs</h3>
                <div class="skill-tags">
                    <span class="skill-tag">REST APIs</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">SQL</span>
                    <span class="skill-tag">Node.js Basics</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2 class="section-title">Featured Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-image">🛒</div>
                <div class="project-content">
                    <h3>E-Commerce Dashboard</h3>
                    <p>Full-featured e-commerce product dashboard with shopping cart, checkout flow, and payment integration using Stripe API.</p>
                    <div class="project-tech">
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">Redux</span>
                        <span class="tech-badge">Tailwind CSS</span>
                        <span class="tech-badge">Stripe API</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/tusharchandel567" class="project-link" target="_blank">View Code →</a>
                        <a href="#" class="project-link">Live Demo →</a>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-image">📊</div>
                <div class="project-content">
                    <h3>Data Visualization Dashboard</h3>
                    <p>Real-time analytics dashboard with interactive charts and graphs displaying live data from external APIs.</p>
                    <div class="project-tech">
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">Chart.js</span>
                        <span class="tech-badge">D3.js</span>
                        <span class="tech-badge">REST API</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/tusharchandel567" class="project-link" target="_blank">View Code →</a>
                        <a href="#" class="project-link">Live Demo →</a>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-image">✓</div>
                <div class="project-content">
                    <h3>Task Management App</h3>
                    <p>Full-featured task manager with CRUD operations, drag-and-drop interface, and Local Storage for data persistence.</p>
                    <div class="project-tech">
                        <span class="tech-badge">JavaScript</span>
                        <span class="tech-badge">HTML5</span>
                        <span class="tech-badge">CSS3</span>
                        <span class="tech-badge">LocalStorage</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/tusharchandel567" class="project-link" target="_blank">View Code →</a>
                        <a href="#" class="project-link">Live Demo →</a>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-image">💼</div>
                <div class="project-content">
                    <h3>Portfolio Website</h3>
                    <p>Modern, responsive portfolio with smooth animations, parallax effects, and optimized performance.</p>
                    <div class="project-tech">
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">Framer Motion</span>
                        <span class="tech-badge">CSS Grid</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/tusharchandel567" class="project-link" target="_blank">View Code →</a>
                        <a href="#" class="project-link">Live Demo →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <h2 class="section-title">Experience & Education</h2>
        <div class="timeline">
            <div class="timeline-item">
                <h3>Frontend Developer (Self-Employed)</h3>
                <div class="timeline-date">January 2023 - Present | Remote, India</div>
                <ul>
                    <li>Developed 10+ responsive web applications using React.js, HTML5, CSS3, JavaScript</li>
                    <li>Improved website performance by 40% through code optimization and lazy loading</li>
                    <li>Built reusable React component library with 25+ components</li>
                    <li>Integrated REST APIs for dynamic data fetching and real-time updates</li>
                    <li>Deployed production websites on AWS S3 with CloudFront CDN</li>
                    <li>Applied WCAG 2.1 accessibility standards for inclusive user experiences</li>
                </ul>
            </div>

            <div class="timeline-item">
                <h3>B.Tech in Computer Science & Engineering</h3>
                <div class="timeline-date">2022 - 2026 (Expected) | Meerut Institute of Technology</div>
                <ul>
                    <li>Relevant Coursework: Data Structures, Algorithms, Web Development, Database Management</li>
                    <li>Active participant in coding competitions and hackathons</li>
                    <li>Member of college technical club focusing on web development</li>
                </ul>
            </div>

            <div class="timeline-item">
                <h3>Certifications</h3>
                <div class="timeline-date">2024 | FreeCodeCamp</div>
                <ul>
                    <li>Responsive Web Design Developer Certification (2024)</li>
                    <li>Python Programming Certification (2024)</li>
                    <li>JavaScript Algorithms & Data Structures (In Progress)</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-container">
            <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 2rem;">
                I'm currently open to new opportunities and collaborations. Whether you have a project in mind 
                or just want to connect, feel free to reach out!
            </p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <a href="mailto:Tushar.chandel.cs.2022@mitmeerut.ac.in">Tushar.chandel.cs.2022@mitmeerut.ac.in</a>
                    <span>Email me for opportunities</span>
                </div>

                <div class="contact-item">
                    <a href="tel:+917505873300">+91 7505873300</a>
                    <span>Call or WhatsApp</span>
                </div>

                <div class="contact-item">
                    <a href="https://linkedin.com/in/tusharchandel567" target="_blank">linkedin.com/in/tusharchandel567</a>
                    <span>Connect on LinkedIn</span>
                </div>

                <div class="contact-item">
                    <a href="https://github.com/tusharchandel567" target="_blank">github.com/tusharchandel567</a>
                    <span>Check out my GitHub</span>
                </div>
            </div>

            <div class="social-links">
                <a href="https://linkedin.com/in/tusharchandel567" class="social-link" target="_blank" title="LinkedIn">in</a>
                <a href="https://github.com/tusharchandel567" class="social-link" target="_blank" title="GitHub">gh</a>
                <a href="mailto:Tushar.chandel.cs.2022@mitmeerut.ac.in" class="social-link" title="Email">@</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Tushar Chandel. Built with ❤️ using HTML, CSS & JavaScript</p>
        <p style="margin-top: 0.5rem; font-size: 0.9rem;">Meerut, Uttar Pradesh, India</p>
    </footer>

    <script>
        // Smooth scroll for navigation links
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

        // Add active class to navigation on scroll
        window.addEventListener('scroll', () => {
            let current = '';
            const sections = document.querySelectorAll('section');
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            document.querySelectorAll('.nav-links a').forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
