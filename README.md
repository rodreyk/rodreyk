<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reykim Rodriguez - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #1a1a1a;
            color: #e0e0e0;
            line-height: 1.6;
            scroll-behavior: smooth;
        }
        html {
            scroll-behavior: smooth;
        }
        a {
            color: #4a90e2;
            text-decoration: none;
        }
        a:hover {
            color: #6bb6ff;
        }
        h1, h2, h3 {
            color: #f0f0f0;
        }
        p {
            margin-bottom: 1rem;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: #2a2a2a;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
            transition: background-color 0.3s;
        }
        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 20px;
        }
        nav h1 {
            font-size: 1.5rem;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin-left: 2rem;
        }
        nav ul li a {
            padding: 0.5rem;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #6bb6ff;
        }
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Sections */
        section {
            padding: 5rem 0;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }
        section:nth-child(even) {
            background-color: #222222;
        }
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Home */
        #home {
            text-align: center;
            background: linear-gradient(135deg, #1a1a1a 0%, #2a2a2a 100%);
        }
        #home h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        #home p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            background-color: #4a90e2;
            color: #fff;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.3s;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #6bb6ff;
            transform: translateY(-2px);
        }

        /* About */
        #about .container {
            max-width: 800px;
        }

        /* Skills */
        #skills ul {
            list-style: none;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }
        #skills li {
            background-color: #333333;
            padding: 1rem;
            border-radius: 5px;
            transition: transform 0.3s;
        }
        #skills li:hover {
            transform: translateY(-5px);
        }
        #skills li i {
            margin-right: 0.5rem;
            color: #4a90e2;
        }

        /* Experience */
        #experience .job {
            margin-bottom: 2rem;
            padding: 1rem;
            background-color: #333333;
            border-radius: 5px;
            transition: transform 0.3s;
        }
        #experience .job:hover {
            transform: translateY(-5px);
        }
        #experience h3 {
            color: #4a90e2;
        }

        /* Education */
        #education .container {
            max-width: 800px;
        }

        /* Contact */
        #contact .container {
            max-width: 800px;
        }
        #contact ul {
            list-style: none;
        }
        #contact li {
            margin-bottom: 1rem;
        }
        #contact li i {
            margin-right: 0.5rem;
            color: #4a90e2;
        }

        /* Mobile Menu */
        @media (max-width: 768px) {
            nav ul {
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: #2a2a2a;
                flex-direction: column;
                display: none;
                padding: 1rem 0;
            }
            nav ul.show {
                display: flex;
            }
            nav ul li {
                margin: 0;
                text-align: center;
                padding: 1rem 0;
            }
            .menu-toggle {
                display: block;
            }
            #home h1 {
                font-size: 2rem;
            }
            #home p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <h1>Reykim Rodriguez</h1>
            <div class="menu-toggle" onclick="toggleMenu()"><i class="fas fa-bars"></i></div>
            <ul id="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section id="home">
        <div class="container fade-in">
            <h1>Welcome to My Portfolio</h1>
            <p>I am Reykim Rodriguez, a dedicated professional based in Bacolod City, Philippines. With a passion for communication, customer service, and innovative technologies, I strive to deliver exceptional results in dynamic environments.</p>
            <a href="#" class="btn" onclick="downloadResume()">My Portfolio</a>
        </div>
    </section>

    <section id="about">
        <div class="container fade-in">
            <h2>About / Career Overview</h2>
            <p>Eager to leverage strong communication skills and a customer-focused mindset to deliver excellent service and support. Passionate about contributing to a dynamic team and growing professionally in fast-paced environments. I bring expertise in social media management, virtual assistance, and emerging technologies like blockchain and cryptocurrency.</p>
        </div>
    </section>

    <section id="skills">
        <div class="container fade-in">
            <h2>Skills</h2>
            <ul>
                <li><i class="fas fa-file-word"></i> <strong>Microsoft Office Suite</strong>: Proficient in Word, Excel, and PowerPoint for efficient document creation and data management.</li>
                <li><i class="fas fa-clock"></i> <strong>Time Management</strong>: Skilled in prioritizing tasks and meeting deadlines in high-pressure settings.</li>
                <li><i class="fas fa-comments"></i> <strong>Verbal & Written Communication</strong>: Excellent at articulating ideas clearly and effectively in both spoken and written forms.</li>
                <li><i class="fas fa-coins"></i> <strong>Blockchain & Cryptocurrency</strong>: Knowledgeable in decentralized technologies, including testing and evaluation of crypto products.</li>
                <li><i class="fas fa-database"></i> <strong>Data Entry</strong>: Accurate and efficient in handling data input and organization.</li>
                <li><i class="fas fa-user-tie"></i> <strong>Virtual Assistance</strong>: Experienced in providing remote support, including administrative tasks and client coordination.</li>
            </ul>
        </div>
    </section>

    <section id="experience">
        <div class="container fade-in">
            <h2>Experience</h2>
            <div class="job">
                <h3>Freelance Crypto Product Tester – TransFi</h3>
                <p>Evaluated user experience, tested payment methods, reviewed support quality, and assessed the P2P trading market to ensure product reliability and user satisfaction.</p>
            </div>
            <div class="job">
                <h3>Social Media Engagement Specialist – Vestion</h3>
                <p>Strengthened brand presence by engaging with online communities and supporting social media strategies to foster audience growth and interaction.</p>
            </div>
            <div class="job">
                <h3>Social Media Manager – AndroTech</h3>
                <p>Developed and executed social media campaigns, created audience-aligned content, and monitored analytics to optimize performance and drive engagement.</p>
            </div>
            <div class="job">
                <h3>B2B Outreach Specialist – LinkedIn Recruiter</h3>
                <p>Managed a LinkedIn account for recruitment and B2B outreach, connecting with professionals and supporting client growth initiatives through targeted networking.</p>
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container fade-in">
            <h2>Education</h2>
            <p><strong>Bachelor of Secondary Education</strong> – Central Philippine Adventist College<br>Focused on educational principles, communication, and leadership skills applicable to various professional fields.</p>
        </div>
    </section>

    <section id="contact">
        <div class="container fade-in">
            <h2>Contact Information</h2>
            <p>Feel free to reach out for collaborations, opportunities, or inquiries.</p>
            <ul>
                <li><i class="fas fa-map-marker-alt"></i> <strong>Location</strong>: Bacolod City, Philippines</li>
                <li><i class="fas fa-phone"></i> <strong>Phone</strong>: 09485725348</li>
                <li><i class="fab fa-whatsapp"></i> <strong>WhatsApp</strong>: 09924364504</li>
                <li><i class="fas fa-envelope"></i> <strong>Email</strong>: <a href="mailto:rodriguezreykim@gmail.com">rodriguezreykim@gmail.com</a></li>
            </ul>
        </div>
    </section>

    <script>
        // Mobile menu toggle
        function toggleMenu() {
            const menu = document.getElementById('nav-menu');
            menu.classList.toggle('show');
        }

        // Fade-in animation on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        });

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // Download resume placeholder
        function downloadResume() {
            // Placeholder: In a real scenario, link to a PDF file
            alert('Download functionality: Replace with actual resume link.');
            // Example: window.open('path/to/resume.pdf', '_blank');
        }
    </script>
</body>
</html>
