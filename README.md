<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marinus Bakara - Cybersecurity Professional</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0a192f;
            --secondary: #112240;
            --accent: #64ffda;
            --text-primary: #ccd6f6;
            --text-secondary: #8892b0;
            --transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(10, 25, 47, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--text-primary);
            text-decoration: none;
            font-size: 1rem;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: var(--transition);
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
            background: linear-gradient(to right, var(--primary) 60%, rgba(10, 25, 47, 0.8)), 
                        url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80') no-repeat center right/cover;
        }
        
        .hero-content {
            max-width: 700px;
            padding: 40px 0;
        }
        
        .hero h4 {
            color: var(--accent);
            font-size: 1.2rem;
            margin-bottom: 15px;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.1;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            color: var(--text-secondary);
            margin-bottom: 30px;
        }
        
        .hero p {
            font-size: 1.1rem;
            margin-bottom: 40px;
            max-width: 600px;
            color: var(--text-secondary);
        }
        
        .btn {
            display: inline-block;
            background-color: transparent;
            color: var(--accent);
            border: 1px solid var(--accent);
            padding: 15px 30px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            cursor: pointer;
            margin-right: 15px;
            margin-bottom: 15px;
        }
        
        .btn:hover {
            background-color: rgba(100, 255, 218, 0.1);
            transform: translateY(-3px);
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--primary);
            border: 1px solid var(--accent);
        }
        
        .btn-primary:hover {
            background-color: rgba(100, 255, 218, 0.9);
        }
        
        /* Sections */
        section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 70px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            display: inline-block;
            position: relative;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent);
        }
        
        /* About */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        
        .skills {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }
        
        .skill-item {
            display: flex;
            align-items: center;
        }
        
        .skill-item i {
            color: var(--accent);
            margin-right: 10px;
            font-size: 1.2rem;
        }
        
        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: var(--secondary);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-img {
            height: 200px;
            position: relative;
            overflow: hidden;
            background-color: #1a2c4d;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .project-content {
            padding: 25px;
        }
        
        .project-content h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
        }
        
        .project-content p {
            color: var(--text-secondary);
            margin-bottom: 20px;
            min-height: 60px;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }
        
        .project-tag {
            background-color: rgba(100, 255, 218, 0.1);
            color: var(--accent);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        /* Certifications */
        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .cert-card {
            background-color: var(--secondary);
            border-radius: 10px;
            padding: 30px;
            transition: var(--transition);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            height: 100%;
        }
        
        .cert-card:hover {
            transform: translateY(-5px);
        }
        
        .cert-card i {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 20px;
        }
        
        .cert-card h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
        }
        
        .cert-card p {
            color: var(--text-secondary);
            margin-bottom: 20px;
            flex-grow: 1;
        }
        
        .cert-card .date {
            color: var(--accent);
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        /* Experience */
        .timeline {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background-color: var(--accent);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: var(--secondary);
            position: relative;
            border-radius: 6px;
        }
        
        .timeline-content h3 {
            margin-top: 0;
            color: var(--accent);
        }
        
        .timeline-content .date {
            color: var(--text-secondary);
            font-style: italic;
            margin-bottom: 10px;
        }
        
        /* Contact */
        .contact-content {
            display: flex;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-form {
            flex: 1;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .info-item i {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 15px;
            min-width: 30px;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            background-color: var(--secondary);
            border: 1px solid rgba(204, 214, 246, 0.2);
            border-radius: 4px;
            color: var(--text-primary);
            font-family: inherit;
            transition: var(--transition);
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--accent);
            outline: none;
        }
        
        /* Footer */
        footer {
            background-color: var(--secondary);
            padding: 30px 0;
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
            border-radius: 50%;
            background-color: rgba(100, 255, 218, 0.1);
            color: var(--accent);
            text-decoration: none;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background-color: var(--accent);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero {
                background: var(--primary);
                padding-top: 100px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .about-content,
            .contact-content {
                flex-direction: column;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
        }
        
        /* Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate {
            animation: fadeIn 0.8s ease-out forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Marinus<span style="color: #64ffda;">B</span></div>
                <ul class="nav-links">
                    <li><a href="#about">About</a></li>
                    <li><a href="#certs">Certifications</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content animate">
                <h4>Hello, I'm</h4>
                <h1>Marinus Bakara</h1>
                <h2>Cybersecurity Engineer</h2>
                <p>Dedicated and detail-oriented Cyber security Engineer with hands-on experience in network security, system security vulnerability assessment, and endpoint security.</p>
                <div class="hero-btns">
                    <a href="#projects" class="btn btn-primary">View Projects</a>
                    <a href="#contact" class="btn">Contact Me</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text animate">
                    <h3>Security Engineer & Penetration Tester</h3>
                    <p>I'm a cybersecurity professional from Ghana with expertise in penetration testing, vulnerability assessment, and security architecture. My work spans across web applications, network infrastructure, and cloud environments.</p>
                    <p>With practical experience in security research and ethical hacking, I've developed a comprehensive skill set focused on identifying and mitigating security vulnerabilities before they can be exploited.</p>
                    
                    <div class="skills">
                        <div class="skill-item">
                            <i class="fas fa-shield-alt"></i>
                            <span>Penetration Testing</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-bug"></i>
                            <span>Vulnerability Research</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-lock"></i>
                            <span>Network Security</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-network-wired"></i>
                            <span>Endpoint Security</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-code"></i>
                            <span>SIEM & Wazuh</span>
                        </div>
                        <div class="skill-item">
                            <i class="fas fa-cloud"></i>
                            <span>Incident Response</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certs" style="background-color: #0c1a36;">
        <div class="container">
            <div class="section-title">
                <h2>Certifications</h2>
            </div>
            <div class="cert-grid">
                <!-- Cert 1 -->
                <div class="cert-card animate">
                    <i class="fas fa-user-secret"></i>
                    <h3>Ethical Hacker</h3>
                    <p>Cisco Networking Academy program</p>
                    <div class="date">Issued: Jun 2025</div>
                </div>
                
                <!-- Cert 2 -->
                <div class="cert-card animate delay-1">
                    <i class="fas fa-shield-halved"></i>
                    <h3>Network Defense Essentials (NDE)</h3>
                    <p>EC-Council certification in network defense</p>
                    <div class="date">Issued: May 2024</div>
                </div>
                
                <!-- Cert 3 -->
                <div class="cert-card animate delay-2">
                    <i class="fas fa-laptop-code"></i>
                    <h3>Cisco LABS Crash Course</h3>
                    <p>EC-Council certification for Cisco networking</p>
                    <div class="date">Issued: May 2024</div>
                </div>
                
                <!-- Cert 4 -->
                <div class="cert-card animate">
                    <i class="fas fa-key"></i>
                    <h3>Ethical Hacking Essentials (EHE)</h3>
                    <p>EC-Council foundational ethical hacking certification</p>
                    <div class="date">Issued: May 2024</div>
                </div>
                
                <!-- Cert 5 -->
                <div class="cert-card animate delay-1">
                    <i class="fas fa-credit-card"></i>
                    <h3>MasterCard Cybersecurity</h3>
                    <p>Virtual Experience Program (Phishing Simulation)</p>
                    <div class="date">Issued: Aug 2024</div>
                </div>
                
                <!-- Cert 6 -->
                <div class="cert-card animate delay-2">
                    <i class="fas fa-building"></i>
                    <h3>Commonwealth Bank Cybersecurity</h3>
                    <p>Virtual Experience Program (Penetration Testing)</p>
                    <div class="date">Issued: Aug 2024</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Experience</h2>
            </div>
            <div class="timeline">
                <!-- Experience 1 -->
                <div class="timeline-item animate">
                    <div class="timeline-content">
                        <h3>IT Technician Intern</h3>
                        <div class="date">Ghana Water Limited | Oct 2024</div>
                        <p>Installed, configured, and managed laptops, printers, and network devices for employees. Performed computer repairs, maintenance, and OS installations.</p>
                    </div>
                </div>
                
                <!-- Education 1 -->
                <div class="timeline-item animate delay-1">
                    <div class="timeline-content">
                        <h3>HND Computer Science</h3>
                        <div class="date">Kumasi Technical University | Current</div>
                        <p>Currently studying Higher National Diploma in Computer Science with focus on cybersecurity.</p>
                    </div>
                </div>
                
                <!-- Education 2 -->
                <div class="timeline-item animate delay-2">
                    <div class="timeline-content">
                        <h3>Computer Technology</h3>
                        <div class="date">Don Bosco Technical Institute | 2022-2024</div>
                        <p>Studied computer technology with emphasis on networking and system administration.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Projects</h2>
            </div>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card animate delay-1">
                    <div class="project-img">
                        <div style="background: #1a2c4d; height: 100%; display: flex; align-items: center; justify-content: center; color: #64ffda; font-size: 3rem;">
                            <i class="fas fa-network-wired"></i>
                        </div>
                    </div>
                    <div class="project-content">
                        <h3>Network Vulnerability Assessment</h3>
                        <p>Conducted port scanning and vulnerability assessments using Nmap & Zenmap. Analyzed scan results and recommended mitigation strategies.</p>
                        <div class="project-tags">
                            <span class="project-tag">Nmap</span>
                            <span class="project-tag">Zenmap</span>
                            <span class="project-tag">Network Security</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card animate delay-2">
                    <div class="project-img">
                        <div style="background: #1a2c4d; height: 100%; display: flex; align-items: center; justify-content: center; color: #64ffda; font-size: 3rem;">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                    </div>
                    <div class="project-content">
                        <h3>Threat Detection with Wazuh</h3>
                        <p>Installed and configured Wazuh SIEM to monitor logs for anomalies & security threats on home network. Developed custom detection rules.</p>
                        <div class="project-tags">
                            <span class="project-tag">SIEM</span>
                            <span class="project-tag">Wazuh</span>
                            <span class="project-tag">Threat Detection</span>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card animate delay-3">
                    <div class="project-img">
                        <div style="background: #1a2c4d; height: 100%; display: flex; align-items: center; justify-content: center; color: #64ffda; font-size: 3rem;">
                            <i class="fas fa-lock"></i>
                        </div>
                    </div>
                    <div class="project-content">
                        <h3>Data Encryption & Protection</h3>
                        <p>Configured encrypted volumes with Vera Crypt to safeguard sensitive data. Implemented disk encryption solutions to prevent unauthorized access.</p>
                        <div class="project-tags">
                            <span class="project-tag">Encryption</span>
                            <span class="project-tag">VeraCrypt</span>
                            <span class="project-tag">Data Security</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Get In Touch</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info animate">
                    <h3>Contact Information</h3>
                    <div class="info-item">
                        <i class="fas fa-envelope"></i>
                        <span>bakaramarinus3@gmail.com</span>
                    </div>
                    <div class="info-item">
                        <i class="fas fa-phone"></i>
                        <span>+233 594607512</span>
                    </div>
                    <div class="info-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Ghana</span>
                    </div>
                    <div class="info-item">
                        <i class="fab fa-github"></i>
                        <span>github.com/MarinusBakara</span>
                    </div>
                    <div class="info-item">
                        <i class="fab fa-linkedin"></i>
                        <span>linkedin.com/in/marinusbakara</span>
                    </div>
                </div>
                <div class="contact-form animate delay-1">
                    <h3>Send a Message</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
            </div>
            <p>&copy; 2024 Marinus Bakara. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple animation observer
        document.addEventListener('DOMContentLoaded', function() {
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate');
                    }
                });
            }, {
                threshold: 0.1
            });
            
            document.querySelectorAll('.project-card, .cert-card, .timeline-item, .contact-info, .contact-form').forEach(el => {
                observer.observe(el);
            });
            
            // Form submission (frontend only)
            document.getElementById('contactForm').addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your message! I will get back to you soon.');
                this.reset();
            });
            
            // Smooth scrolling for navigation
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
