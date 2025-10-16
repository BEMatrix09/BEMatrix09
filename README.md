<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pranav Salunke - AI & Full Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #7c3aed;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --success: #10b981;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0f172a;
            color: var(--light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 80px 0 60px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid white;
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #e2e8f0, #cbd5e1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: var(--dark);
            position: relative;
            z-index: 1;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 20px;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
            position: relative;
            z-index: 1;
        }
        
        .stat-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }
        
        /* Section Styles */
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .about-text h3 {
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: #cbd5e1;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-item i {
            color: var(--primary);
            width: 20px;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: #1e293b;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
        }
        
        .skill-category h3 {
            margin-bottom: 15px;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .skill-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-item {
            background: rgba(37, 99, 235, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(37, 99, 235, 0.3);
        }
        
        /* Experience Section */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: var(--primary);
        }
        
        .timeline-item {
            margin-bottom: 40px;
            position: relative;
            width: 50%;
            padding: 0 40px;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            background: #1e293b;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .timeline-content h3 {
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .timeline-content .company {
            color: var(--secondary);
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .timeline-content ul {
            padding-left: 20px;
        }
        
        .timeline-content li {
            margin-bottom: 5px;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            top: 20px;
            right: -10px;
            width: 20px;
            height: 20px;
            background: var(--secondary);
            border-radius: 50%;
        }
        
        .timeline-item:nth-child(even)::after {
            left: -10px;
        }
        
        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: #1e293b;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 15px 0;
        }
        
        .tech-tag {
            background: rgba(124, 58, 237, 0.1);
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid rgba(124, 58, 237, 0.3);
        }
        
        /* Education Section */
        .education-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .education-card {
            background: #1e293b;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .education-card h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .education-card .institution {
            color: var(--secondary);
            font-weight: 600;
            margin-bottom: 5px;
        }
        
        .education-card .duration {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Footer */
        footer {
            background: #1e293b;
            padding: 40px 0;
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .timeline::before {
                left: 20px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 50px;
                padding-right: 0;
            }
            
            .timeline-item:nth-child(odd),
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 10px;
            }
            
            .timeline-item:nth-child(even)::after {
                left: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container">
            <div class="profile-img">
                <i class="fas fa-code"></i>
            </div>
            <h1>Pranav Salunke</h1>
            <p class="tagline">AI & Data Science Engineer | Full Stack Developer</p>
            <div class="stats">
                <div class="stat-item">
                    <i class="fas fa-briefcase"></i> 3+ Projects
                </div>
                <div class="stat-item">
                    <i class="fas fa-code-branch"></i> 5+ Technologies
                </div>
                <div class="stat-item">
                    <i class="fas fa-graduation-cap"></i> B.E. AI & DS
                </div>
            </div>
        </div>
    </header>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Creative & Forward-Thinking Developer</h3>
                    <p>I create cutting-edge websites and applications for high-profile clients with challenging demands and visions. Skilled project manager, team leader and analytical problem-solver with top-notch organizational, scheduling and code verification skills.</p>
                    <p><strong>Fact:</strong> I am serious about technology and passionate about making code work right and fast.</p>
                </div>
                <div class="contact-info">
                    <h3>Contact Information</h3>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <span>9579995747</span>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>misalunke09@gmail.com</span>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Nashik, Maharashtra 422003</span>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        <span>linkedin.com/in/pranav-salunke-970594287</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3><i class="fas fa-laptop-code"></i> Frontend</h3>
                    <div class="skill-items">
                        <span class="skill-item">HTML5</span>
                        <span class="skill-item">CSS3</span>
                        <span class="skill-item">JavaScript</span>
                        <span class="skill-item">React.js</span>
                        <span class="skill-item">Bootstrap</span>
                        <span class="skill-item">Responsive Design</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-server"></i> Backend</h3>
                    <div class="skill-items">
                        <span class="skill-item">Node.js</span>
                        <span class="skill-item">Express.js</span>
                        <span class="skill-item">Flask</span>
                        <span class="skill-item">Django</span>
                        <span class="skill-item">API Integration</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-database"></i> Database & Tools</h3>
                    <div class="skill-items">
                        <span class="skill-item">MongoDB</span>
                        <span class="skill-item">MySQL</span>
                        <span class="skill-item">SQL</span>
                        <span class="skill-item">Git</span>
                        <span class="skill-item">AWS</span>
                        <span class="skill-item">SEO</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-cogs"></i> Programming Languages</h3>
                    <div class="skill-items">
                        <span class="skill-item">Python</span>
                        <span class="skill-item">JavaScript</span>
                        <span class="skill-item">C</span>
                        <span class="skill-item">C++</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <div class="container">
            <h2 class="section-title">Professional Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Full Stack Developer Intern</h3>
                        <div class="company">Datamatics Global Services Limited</div>
                        <ul>
                            <li>Collaborated with team members to design and implement software solutions</li>
                            <li>Integrated third-party APIs to enhance application functionality</li>
                            <li>Documented project specifications and technical processes</li>
                            <li>Developed applications following latest coding practices and industry standards</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Frontend Developer</h3>
                        <div class="company">Nxtwave CCBP 4.0</div>
                        <ul>
                            <li>Gained strong foundational skills in creating responsive and semantic web pages</li>
                            <li>Built reusable UI components and managed state effectively in React-based projects</li>
                            <li>Developed responsive websites optimized for both desktop and mobile</li>
                            <li>Focused on modular architecture for scalable web apps</li>
                        </ul>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Founder</h3>
                        <div class="company">Bramha Intelligence (Startup)</div>
                        <ul>
                            <li>Founded Bramha Intelligence; delivered 5+ client websites</li>
                            <li>Handled end-to-end web development: requirements, UI implementation (React), backend (Flask/Django), testing and deployment</li>
                            <li>Clients included retailers, Nyastarang Company and a pest control service</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-content">
                        <h3>E-commerce Website for Herbal Products</h3>
                        <p>Developed a responsive e-commerce platform for herbal product sales</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">MySQL</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-content">
                        <h3>Doctor Appointment Booking Website</h3>
                        <p>Built a responsive appointment system for doctors</p>
                        <div class="project-tech">
                            <span class="tech-tag">HTML</span>
                            <span class="tech-tag">CSS</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">Flask</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-content">
                        <h3>Pest Control Services Website</h3>
                        <p>Designed and deployed a business website showcasing services</p>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Bootstrap</span>
                            <span class="tech-tag">Flask</span>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-content">
                        <h3>AI Model Automation</h3>
                        <p>Created a service-based AI automation tool using Gemini API</p>
                        <div class="project-tech">
                            <span class="tech-tag">AI</span>
                            <span class="tech-tag">API Integration</span>
                            <span class="tech-tag">Automation</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education">
        <div class="container">
            <h2 class="section-title">Education</h2>
            <div class="education-container">
                <div class="education-card">
                    <h3>B.E. Artificial Intelligence and Data Science</h3>
                    <div class="institution">Sandip Institute of Technology and Research Centre (SITRC)</div>
                    <div class="duration">2021 - 2025</div>
                </div>
                <div class="education-card">
                    <h3>Certification in Full Stack Development</h3>
                    <div class="institution">Nxtwave CCBP-4.0</div>
                    <div class="duration">2024</div>
                </div>
                <div class="education-card">
                    <h3>HSC</h3>
                    <div class="institution">74.20%</div>
                    <div class="duration">2021</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://twitter.com/i_honest_09" target="_blank"><i class="fab fa-twitter"></i></a>
                <a href="https://instagram.com/i_honest_0901" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://linkedin.com/in/pranav-salunke-970594287" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="https://github.com/bematrix09" target="_blank"><i class="fab fa-github"></i></a>
            </div>
            <p class="copyright">© 2023 Pranav Salunke. All Rights Reserved.</p>
        </div>
    </footer>
</body>
</html>
