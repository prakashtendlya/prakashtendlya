<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prakash Arumugam - Senior Software Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            padding: 60px 20px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin-bottom: 40px;
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
            border: 1px solid rgba(255, 255, 255, 0.18);
            animation: fadeInUp 1s ease-out;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 30px;
            font-size: 60px;
            font-weight: bold;
            color: white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            animation: pulse 2s infinite;
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            color: white;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .title {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 20px;
            font-weight: 300;
        }

        .location {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 30px;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .section {
            background: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            animation: slideInLeft 0.8s ease-out;
        }

        .section:nth-child(even) {
            animation: slideInRight 0.8s ease-out;
        }

        .section-title {
            font-size: 2.2rem;
            color: #2c3e50;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .highlight-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 25px;
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.3);
            animation: fadeIn 1s ease-out;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #ffd700;
            display: block;
        }

        .stat-label {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-top: 5px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .tech-category {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }

        .tech-category h4 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-tag {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .experience-item {
            border-left: 3px solid #667eea;
            padding-left: 20px;
            margin-bottom: 30px;
            position: relative;
        }

        .experience-item::before {
            content: '';
            position: absolute;
            left: -8px;
            top: 0;
            width: 12px;
            height: 12px;
            background: #667eea;
            border-radius: 50%;
        }

        .company-name {
            font-size: 1.3rem;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 5px;
        }

        .role-title {
            font-size: 1.1rem;
            color: #667eea;
            margin-bottom: 5px;
        }

        .duration {
            color: #7f8c8d;
            font-style: italic;
            margin-bottom: 15px;
        }

        .achievements {
            list-style: none;
            padding: 0;
        }

        .achievements li {
            background: #f8f9fa;
            padding: 10px 15px;
            margin-bottom: 8px;
            border-radius: 5px;
            border-left: 3px solid #27ae60;
            position: relative;
        }

        .achievements li::before {
            content: '✓';
            color: #27ae60;
            font-weight: bold;
            margin-right: 10px;
        }

        .project-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 20px;
            box-shadow: 0 8px 25px rgba(240, 147, 251, 0.3);
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .project-duration {
            opacity: 0.8;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }

        .project-description {
            line-height: 1.6;
        }

        .awards-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .award-card {
            background: linear-gradient(45deg, #ffd89b 0%, #19547b 100%);
            color: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(25, 84, 123, 0.3);
        }

        .award-icon {
            font-size: 2rem;
            margin-bottom: 10px;
            display: block;
        }

        .footer {
            text-align: center;
            padding: 40px;
            color: rgba(255, 255, 255, 0.8);
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            backdrop-filter: blur(10px);
            margin-top: 40px;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        @media (max-width: 768px) {
            .name {
                font-size: 2rem;
            }
            
            .section {
                padding: 20px;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="profile-img">PA</div>
            <h1 class="name">Prakash Arumugam</h1>
            <p class="title">Senior Software Development Engineer</p>
            <p class="location">📍 Bangalore, India</p>
            
            <div class="contact-links">
                <a href="mailto:prakashtendlya100@gmail.com" class="contact-link">
                    📧 Email
                </a>
                <a href="tel:+91-7397628546" class="contact-link">
                    📱 +91-7397628546
                </a>
                <a href="https://linkedin.com/in/prakash-arumugam-502a2b194" class="contact-link" target="_blank">
                    💼 LinkedIn
                </a>
            </div>
        </div>

        <!-- About Section -->
        <div class="section">
            <h2 class="section-title">About Me</h2>
            <div class="highlight-card">
                <p style="font-size: 1.2rem; line-height: 1.8;">
                    Senior Software Engineer with <strong>5+ years</strong> of experience in fintech and banking applications. 
                    Specialized in <strong>Java microservices</strong>, <strong>cloud architecture</strong>, and <strong>AI integration</strong>. 
                    Currently driving digital transformation at FreeCharge (Axis Bank), delivering scalable solutions that process 
                    <strong>₹4000+ Crores</strong> in transactions.
                </p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <span class="stat-number">₹4000Cr+</span>
                        <span class="stat-label">Transaction Volume</span>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">150M+</span>
                        <span class="stat-label">Records Processed</span>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">90%</span>
                        <span class="stat-label">Platform Adoption</span>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">5+</span>
                        <span class="stat-label">Years Experience</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Technical Skills Section -->
        <div class="section">
            <h2 class="section-title">Technical Expertise</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h4>Languages</h4>
                    <div class="tech-tags">
                        <span class="tech-tag">Java 8/11/17</span>
                        <span class="tech-tag">JavaScript</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Shell Scripting</span>
                        <span class="tech-tag">SQL</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h4>Frameworks</h4>
                    <div class="tech-tags">
                        <span class="tech-tag">Spring Boot</span>
                        <span class="tech-tag">Spring Security</span>
                        <span class="tech-tag">Spring Data JPA</span>
                        <span class="tech-tag">Ratpack</span>
                        <span class="tech-tag">JUnit</span>
                        <span class="tech-tag">Mockito</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h4>Cloud & DevOps</h4>
                    <div class="tech-tags">
                        <span class="tech-tag">AWS</span>
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">Kubernetes</span>
                        <span class="tech-tag">Nginx</span>
                        <span class="tech-tag">Microservices</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h4>Data & Messaging</h4>
                    <div class="tech-tags">
                        <span class="tech-tag">Apache Kafka</span>
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">DynamoDB</span>
                        <span class="tech-tag">Elasticsearch</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Experience Section -->
        <div class="section">
            <h2 class="section-title">Professional Experience</h2>
            
            <div class="experience-item">
                <div class="company-name">FreeCharge (A subsidiary of Axis Bank)</div>
                <div class="role-title">Senior Software Development Engineer</div>
                <div class="duration">Nov 2022 - Present | Bangalore</div>
                <ul class="achievements">
                    <li>Designed complete Digital Gold loan application workflow with 90%+ adoption, disbursing ₹4000+ Crores</li>
                    <li>Integrated AI solutions for VKYC including face detection and fraud prevention, improving call completion by 27%</li>
                    <li>Built E-signing and E-stamping workflows, reducing customer booking time by 20%</li>
                    <li>Implemented semantic search with Elasticsearch and trending recommendations using CTR analytics</li>
                    <li>Published organization-wide reusable packages for retry mechanisms and AI chatbot functionality</li>
                </ul>
            </div>
            
            <div class="experience-item">
                <div class="company-name">G10x</div>
                <div class="role-title">Software Developer</div>
                <div class="duration">Feb 2020 - Nov 2022 | Kochi</div>
                <ul class="achievements">
                    <li>Developed robust Authentication and Authorization APIs with OAuth 2.0 and JWT implementation</li>
                    <li>Built scalable data processing system transforming 150+ million records using MapReduce</li>
                    <li>Optimized REST API performance achieving 5% reduction in operational costs</li>
                    <li>Maintained comprehensive code coverage using JUnit and integration testing frameworks</li>
                </ul>
            </div>
        </div>

        <!-- Key Projects Section -->
        <div class="section">
            <h2 class="section-title">Key Projects</h2>
            
            <div class="project-card">
                <div class="project-title">🤖 Chanakya - AI Customer Service Platform</div>
                <div class="project-duration">Jul 2023 - Present</div>
                <div class="project-description">
                    Developed AI-powered chatbot for automated customer queries, document processing, and technical verification. 
                    Integrated with banking systems for seamless customer experience.
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-title">🛍️ Scan and Go / MPOS / Amazon JWO</div>
                <div class="project-duration">Aug 2020 - Nov 2022</div>
                <div class="project-description">
                    Developed WHSmith's backend system for seamless checkout experience. Created scalable system 
                    ingesting millions of records into DynamoDB with zero discrepancies.
                </div>
            </div>
            
            <div class="project-card">
                <div class="project-title">🔍 Search and Analytics System</div>
                <div class="project-duration">2024 - Present</div>
                <div class="project-description">
                    Implemented Elasticsearch-based search with real-time trending analytics and user behavior patterns. 
                    Enhanced search relevance and user experience across banking platforms.
                </div>
            </div>
        </div>

        <!-- Awards & Recognition Section -->
        <div class="section">
            <h2 class="section-title">Awards & Recognition</h2>
            <div class="awards-list">
                <div class="award-card">
                    <span class="award-icon">🏗️</span>
                    <h4>Solutions Architect Team Member</h4>
                    <p>FreeCharge | Aug 2023 - Present</p>
                    <small>Strategic technical decisions and architecture design</small>
                </div>
                
                <div class="award-card">
                    <span class="award-icon">🏆</span>
                    <h4>Pat on the Back Awards</h4>
                    <p>G10x | Multiple Quarters</p>
                    <small>Exceptional performance and project contributions</small>
                </div>
                
                <div class="award-card">
                    <span class="award-icon">📦</span>
                    <h4>Organization-wide Contributor</h4>
                    <p>Published reusable packages</p>
                    <small>Used across multiple teams and projects</small>
                </div>
            </div>
        </div>

        <!-- Education Section -->
        <div class="section">
            <h2 class="section-title">Education</h2>
            <div class="experience-item">
                <div class="company-name">Dr. Mahalingam College of Engineering and Technology</div>
                <div class="role-title">Bachelor of Engineering in Electronics and Communication</div>
                <div class="duration">2016 - 2020 | Anna University | CGPA: 7.5/10</div>
                <p style="margin-top: 10px; color: #666;">
                    <strong>Relevant Coursework:</strong> Object Oriented Programming, Databases, Data Structures and Algorithms, 
                    Operating Systems, Computer Networks
                </p>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>💻 Passionate about building scalable, secure, and innovative software solutions</p>
            <p>🚀 Always learning and exploring cutting-edge technologies</p>
            <p style="margin-top: 20px; opacity: 0.7;">
                "Code is like humor. When you have to explain it, it's bad." - Cory House
            </p>
        </div>
    </div>
</body>
</html>
