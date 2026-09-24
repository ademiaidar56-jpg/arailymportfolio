<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Жеке Портфолио</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --accent-color: #38bdf8;
            --accent-hover: #0284c7;
            --text-color: #f8fafc;
            --text-secondary: #94a3b8;
            --border-color: #334155;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--accent-color);
        }

        .nav-links {
            display: flex;
            gap: 1.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-color);
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent-color);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 1rem;
            background: radial-gradient(circle at center, #1e293b 0%, #0f172a 100%);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .hero h1 span {
            color: var(--accent-color);
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.8rem;
            background-color: var(--accent-color);
            color: #0f172a;
            font-weight: 600;
            border-radius: 8px;
            text-decoration: none;
            transition: background 0.3s, transform 0.2s;
        }

        .btn:hover {
            background-color: var(--accent-hover);
            transform: translateY(-2px);
        }

        /* Sections */
        section {
            padding: 5rem 2rem;
            max-width: 1100px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background: var(--accent-color);
            margin: 0.5rem auto 0;
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            background-color: var(--card-bg);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 10px;
            border: 1px solid var(--border-color);
            text-align: center;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
        }

        .skill-card i {
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--border-color);
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h3 {
            margin-bottom: 0.5rem;
        }

        .project-info p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }

        .tags {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .tag {
            background-color: #334155;
            color: var(--accent-color);
            padding: 0.2rem 0.6rem;
            border-radius: 4px;
            font-size: 0.8rem;
        }

        /* Contact Section */
        .contact-content {
            text-align: center;
            background-color: var(--card-bg);
            padding: 3rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .social-links a {
            color: var(--text-color);
            font-size: 1.8rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--accent-color);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid var(--border-color);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .nav-links { display: none; }
        }
    </style>
</head>
<body>

    <!-- Навигация -->
    <nav>
        <div class="logo">Портфолио</div>
        <ul class="nav-links">
            <li><a href="#about">Мен туралы</a></li>
            <li><a href="#skills">Дағдылар</a></li>
            <li><a href="#projects">Жобалар</a></li>
            <li><a href="#contact">Байланыс</a></li>
        </ul>
    </nav>

    <!-- Басты бөлім (Hero) -->
    <section class="hero">
        <h1>Сәлем, мен <span>[Сіздің Есіміңіз]</span></h1>
        <p>[Сіздің мамандығыңыз немесе қызмет бағытыңыз: мысалы, Веб-әзірлеуші / Дизайнер / Студент]</p>
        <a href="#projects" class="btn">Жобаларды көру</a>
    </section>

    <!-- Мен туралы -->
    <section id="about">
        <h2 class="section-title">Мен туралы</h2>
        <div class="about-content">
            <p>Бұл бөлімде өзіңіз туралы қысқаша ақпарат жазасыз. Тәжірибеңіз, мақсаттарыңыз, қызығушылықтарыңыз бен біліміңізді атап өтуге болады.</p>
        </div>
    </section>

    <!-- Дағдылар -->
    <section id="skills">
        <h2 class="section-title">Дағдыларым</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <i class="fa-solid fa-code"></i>
                <h3>HTML & CSS</h3>
                <p>Веб-беттердің құрылымы мен дизайны</p>
            </div>
            <div class="skill-card">
                <i class="fa-solid fa-palette"></i>
                <h3>Дизайн</h3>
                <p>Canva, UI/UX бағытындағы орналасулар</p>
            </div>
            <div class="skill-card">
                <i class="fa-solid fa-laptop-code"></i>
                <h3>JavaScript</h3>
                <p>Интерактивті элементтер жасау</p>
            </div>
            <div class="skill-card">
                <i class="fa-solid fa-folder-open"></i>
                <h3>Жобалау</h3>
                <p>Материалдарды жүйелеу мен құрастыру</p>
            </div>
        </div>
    </section>

    <!-- Жобалар -->
    <section id="projects">
        <h2 class="section-title">Жобаларым</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-info">
                    <h3>Жоба #1</h3>
                    <p>Жобаның қысқаша сипаттамасы. Мұнда оның мақсаты мен атқарылған жұмыстар көрсетіледі.</p>
                    <div class="tags">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                    </div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-info">
                    <h3>Жоба #2</h3>
                    <p>Басқа бір орындалған жұмыс немесе презентация, веб-сайт үлгісі.</p>
                    <div class="tags">
                        <span class="tag">Дизайн</span>
                        <span class="tag">Макет</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Байланыс -->
    <section id="contact">
        <h2 class="section-title">Байланыс</h2>
        <div class="contact-content">
            <p>Жобалар бойынша ұсыныстарыңыз болса немесе хабарласқыңыз келсе:</p>
            <div class="social-links">
                <a href="#"><i class="fa-brands fa-telegram"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
                <a href="#"><i class="fa-brands fa-github"></i></a>
                <a href="mailto:example@email.com"><i class="fa-solid fa-envelope"></i></a>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <p>&copy; 2026 Барлық құқықтар қорғалған.</p>
    </footer>

</body>
</html>
