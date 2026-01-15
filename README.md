<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mustafa Ahmed | Senior Software Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #64748b;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #e2e8f0;
            --accent: #06b6d4;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --radius: 8px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f1f5f9;
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, var(--dark) 0%, #0f172a 100%);
            color: white;
            padding: 3rem 2rem;
            border-radius: var(--radius);
            margin-bottom: 2rem;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
        }

        .name {
            font-size: 2.8rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            background: linear-gradient(90deg, white, var(--gray));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .title {
            font-size: 1.4rem;
            color: var(--gray);
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .tag-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 1.5rem;
        }

        .tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 0.9rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Quote */
        .quote {
            font-style: italic;
            text-align: center;
            color: var(--secondary);
            padding: 1.5rem;
            margin: 2rem 0;
            border-left: 4px solid var(--primary);
            background-color: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        /* Content Layout */
        .content-grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        @media (max-width: 992px) {
            .content-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Cards */
        .card {
            background-color: white;
            border-radius: var(--radius);
            padding: 1.8rem;
            margin-bottom: 1.5rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border-top: 4px solid var(--primary);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        .card-title {
            font-size: 1.4rem;
            color: var(--dark);
            margin-bottom: 1.2rem;
            padding-bottom: 0.7rem;
            border-bottom: 2px solid var(--gray);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card-title i {
            color: var(--primary);
        }

        /* Lists */
        .skill-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1rem;
        }

        .skill-category {
            margin-bottom: 1.5rem;
        }

        .skill-category h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        .skill-items {
            list-style: none;
        }

        .skill-items li {
            padding: 8px 0;
            border-bottom: 1px dashed var(--gray);
            display: flex;
            align-items: center;
        }

        .skill-items li:before {
            content: "▸";
            color: var(--accent);
            margin-right: 10px;
            font-weight: bold;
        }

        /* Contact */
        .contact-card {
            background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary) 100%);
            color: white;
            border-radius: var(--radius);
            padding: 1.8rem;
            margin-top: 1rem;
            box-shadow: var(--shadow);
        }

        .contact-card .card-title {
            color: white;
            border-bottom-color: rgba(255, 255, 255, 0.2);
        }

        .contact-info {
            list-style: none;
        }

        .contact-info li {
            padding: 12px 0;
            display: flex;
            align-items: center;
            gap: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-info li:last-child {
            border-bottom: none;
        }

        .contact-info i {
            width: 24px;
            text-align: center;
        }

        .contact-link {
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }

        .contact-link:hover {
            color: var(--accent);
            text-decoration: underline;
        }

        /* Focus Areas */
        .focus-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 1.2rem;
            padding-bottom: 1.2rem;
            border-bottom: 1px solid var(--gray);
        }

        .focus-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .focus-icon {
            background-color: rgba(37, 99, 235, 0.1);
            color: var(--primary);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            color: var(--secondary);
            font-size: 0.9rem;
            border-top: 1px solid var(--gray);
        }

        /* Badges */
        .badge {
            display: inline-block;
            background-color: var(--gray);
            color: var(--dark);
            padding: 4px 12px;
            border-radius: 50px;
            font-size: 0.8rem;
            margin: 3px;
            font-weight: 500;
        }

        .badge-primary {
            background-color: rgba(37, 99, 235, 0.1);
            color: var(--primary);
        }

        .badge-accent {
            background-color: rgba(6, 182, 212, 0.1);
            color: var(--accent);
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <h1 class="name">Mustafa Ahmed</h1>
            <p class="title">Senior Software Engineer</p>
            <p>Specializing in cloud-native architecture, distributed systems, and infrastructure engineering. I design and build scalable, reliable, and cost-efficient systems with a focus on simplicity and maintainability.</p>
            <div class="tag-container">
                <span class="tag">Cloud-Native Architecture</span>
                <span class="tag">Distributed Systems</span>
                <span class="tag">Infrastructure Engineering</span>
                <span class="tag">Go/TypeScript</span>
                <span class="tag">AWS</span>
                <span class="tag">Kubernetes</span>
            </div>
        </header>

        <!-- Quote -->
        <div class="quote">
            "Simplicity is prerequisite for reliability." – Edsger W. Dijkstra
        </div>

        <!-- Main Content -->
        <div class="content-grid">
            <!-- Left Column -->
            <div class="left-column">
                <!-- Technical Proficiencies -->
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-code"></i> Technical Proficiencies</h2>
                    <div class="skill-list">
                        <div class="skill-category">
                            <h4>Languages & Runtimes</h4>
                            <ul class="skill-items">
                                <li>Go (Golang)</li>
                                <li>TypeScript / JavaScript</li>
                                <li>Node.js Runtime</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h4>Backend & Systems Architecture</h4>
                            <ul class="skill-items">
                                <li>RESTful & GraphQL APIs</li>
                                <li>Microservices Architecture</li>
                                <li>Event-Driven Systems</li>
                                <li>Express.js, Next.js</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h4>Data Management</h4>
                            <ul class="skill-items">
                                <li>PostgreSQL, MySQL, RDS</li>
                                <li>MongoDB, DynamoDB, Redis</li>
                                <li>Elasticsearch</li>
                                <li>Geospatial Data Systems</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h4>Cloud Infrastructure (AWS)</h4>
                            <ul class="skill-items">
                                <li>EC2, Lambda, ECS, EKS</li>
                                <li>S3, RDS, DynamoDB</li>
                                <li>VPC, CloudFront, API Gateway</li>
                                <li>IAM, Security Groups</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h4>DevOps & Infrastructure as Code</h4>
                            <ul class="skill-items">
                                <li>Docker & Kubernetes</li>
                                <li>Terraform, CloudFormation</li>
                                <li>GitHub Actions, Jenkins</li>
                                <li>CI/CD Pipeline Design</li>
                            </ul>
                        </div>
                        <div class="skill-category">
                            <h4>Observability & Reliability</h4>
                            <ul class="skill-items">
                                <li>AWS CloudWatch, Datadog</li>
                                <li>Distributed Tracing</li>
                                <li>Performance Monitoring</li>
                                <li>SLO/SLI Implementation</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Core Competencies -->
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-cogs"></i> Core Competencies</h2>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-server"></i>
                        </div>
                        <div>
                            <h4>Backend Engineering</h4>
                            <p>Designing and implementing high-performance, scalable services in Go and Node.js with emphasis on clean architecture and maintainability.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-cloud"></i>
                        </div>
                        <div>
                            <h4>Cloud Architecture</h4>
                            <p>Architecting cloud-native solutions on AWS, implementing cost-optimized infrastructure with security and scalability as primary considerations.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-robot"></i>
                        </div>
                        <div>
                            <h4>Infrastructure Automation</h4>
                            <p>Building automated CI/CD pipelines and infrastructure using Terraform and IaC principles for consistent, repeatable deployments.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-database"></i>
                        </div>
                        <div>
                            <h4>Database Architecture</h4>
                            <p>Designing and optimizing both SQL and NoSQL data models for performance, scalability, and reliability across distributed systems.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Right Column -->
            <div class="right-column">
                <!-- Current Focus -->
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-bullseye"></i> Current Focus</h2>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-sitemap"></i>
                        </div>
                        <div>
                            <h4>Distributed Systems</h4>
                            <p>Architecting highly available, fault-tolerant distributed systems.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-cubes"></i>
                        </div>
                        <div>
                            <h4>Kubernetes Orchestration</h4>
                            <p>Advanced Kubernetes patterns and cluster management strategies.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-bolt"></i>
                        </div>
                        <div>
                            <h4>Serverless Architecture</h4>
                            <p>Event-driven design and serverless optimization techniques.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <div>
                            <h4>Performance Engineering</h4>
                            <p>Profiling, optimization, and cost engineering for cloud workloads.</p>
                        </div>
                    </div>
                    <div class="focus-item">
                        <div class="focus-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <div>
                            <h4>Resilient Microservices</h4>
                            <p>Building fault-tolerant microservices with Go and cloud-native patterns.</p>
                        </div>
                    </div>
                </div>

                <!-- Professional Development -->
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-graduation-cap"></i> Professional Development</h2>
                    <p>Continuously expanding expertise in:</p>
                    <div style="margin-top: 1rem;">
                        <span class="badge badge-primary">Large-scale System Design</span>
                        <span class="badge badge-accent">Kubernetes Internals</span>
                        <span class="badge badge-primary">Go Concurrency Patterns</span>
                        <span class="badge badge-accent">Cloud Cost Optimization</span>
                        <span class="badge badge-primary">Site Reliability Engineering</span>
                    </div>
                </div>

                <!-- Contact -->
                <div class="contact-card">
                    <h2 class="card-title"><i class="fas fa-envelope"></i> Contact</h2>
                    <ul class="contact-info">
                        <li>
                            <i class="fab fa-linkedin"></i>
                            <a href="https://linkedin.com/in/mustafa-ahmed-012675279" class="contact-link" target="_blank">
                                linkedin.com/in/mustafa-ahmed
                            </a>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <a href="mailto:mustafabukhari333@gmail.com" class="contact-link">
                                mustafabukhari333@gmail.com
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer class="footer">
            <p>© 2023 Mustafa Ahmed. All rights reserved.</p>
            <p>Senior Software Engineer | Cloud-Native Specialist</p>
        </footer>
    </div>

    <script>
        // Simple animation for skill items on hover
        document.addEventListener('DOMContentLoaded', function() {
            const skillItems = document.querySelectorAll('.skill-items li');
            
            skillItems.forEach(item => {
                item.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateX(5px)';
                    this.style.transition = 'transform 0.2s ease';
                });
                
                item.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateX(0)';
                });
            });
            
            // Add current year to footer
            const yearSpan = document.querySelector('.footer p');
            if (yearSpan) {
                const currentYear = new Date().getFullYear();
                yearSpan.innerHTML = yearSpan.innerHTML.replace('2023', currentYear);
            }
        });
    </script>
</body>
</html>
