<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Portofolio Gizella Al Zahra</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --background: #f2f8fc;
            --surface: #ffffff;
            --text: #17324d;
            --text-secondary: #667b8f;
            --primary: #78aeda;
            --primary-dark: #4f91c7;
            --border: #d8e8f3;
            --shadow: 0 10px 30px rgba(71, 130, 170, 0.12);
        }

        body.dark-mode {
            --background: #10202e;
            --surface: #183044;
            --text: #f3f8fc;
            --text-secondary: #b7c9d7;
            --primary: #82bce5;
            --primary-dark: #5b9dca;
            --border: #29475d;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--background);
            color: var(--text);
            line-height: 1.6;
            transition: 0.3s;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        button {
            font-family: inherit;
        }

        /* HEADER */
        .header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--surface);
            border-bottom: 1px solid var(--border);
        }

        .navbar {
            width: 90%;
            max-width: 1100px;
            min-height: 70px;
            margin: auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
        }

        .logo span,
        .footer h3 span {
            color: var(--primary-dark);
        }

        .nav-menu {
            display: flex;
            align-items: center;
            gap: 28px;
            list-style: none;
        }

        .nav-menu a {
            font-size: 15px;
            font-weight: bold;
            color: var(--text-secondary);
            transition: 0.3s;
        }

        .nav-menu a:hover {
            color: var(--primary-dark);
        }

        .menu-toggle {
            display: none;
            border: none;
            background: transparent;
            color: var(--text);
            font-size: 28px;
            cursor: pointer;
        }

        .theme-toggle {
            width: 42px;
            height: 42px;
            border: 1px solid var(--border);
            border-radius: 50%;
            background: var(--surface);
            color: var(--text);
            cursor: pointer;
            font-size: 18px;
        }

        /* HERO */
        .hero {
            width: 90%;
            max-width: 1100px;
            min-height: 650px;
            margin: auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
        }

        .hero-content {
            flex: 1;
        }

        .hero-small {
            color: var(--primary-dark);
            font-weight: bold;
            letter-spacing: 3px;
            margin-bottom: 10px;
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 72px);
            line-height: 1.1;
            margin-bottom: 10px;
        }

        .hero h2 {
            font-size: 28px;
            margin-bottom: 20px;
        }

        .hero h2 span {
            color: var(--primary-dark);
        }

        .hero-content > p {
            max-width: 550px;
            color: var(--text-secondary);
            font-size: 17px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }

        .button {
            display: inline-block;
            padding: 13px 24px;
            border-radius: 10px;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary-button {
            background: var(--primary-dark);
            color: white;
        }

        .primary-button:hover {
            background: var(--primary);
            transform: translateY(-2px);
        }

        .secondary-button {
            border: 1px solid var(--border);
            color: var(--text);
        }

        .secondary-button:hover {
            border-color: var(--primary);
            color: var(--primary-dark);
        }

        /* FOTO */
        .hero-image {
            flex: 0 0 350px;
            display: flex;
            justify-content: center;
        }

        .image-circle {
            width: 320px;
            height: 320px;
            padding: 8px;
            border-radius: 50%;
            background: var(--primary);
        }

        .image-circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            display: block;
            background: #dceaf3;
        }

        /* SECTION */
        .section {
            width: 90%;
            max-width: 1100px;
            margin: auto;
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title p {
            color: var(--primary-dark);
            font-weight: bold;
            letter-spacing: 2px;
            font-size: 14px;
        }

        .section-title h2 {
            font-size: 38px;
        }

        /* TENTANG */
        .about-container {
            display: flex;
            align-items: center;
            gap: 60px;
        }

        .about-image {
            flex: 0 0 300px;
        }

        .about-image img {
            width: 100%;
            height: 360px;
            object-fit: cover;
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        .about-content {
            flex: 1;
        }

        .about-content h3 {
            font-size: 30px;
            margin-bottom: 15px;
        }

        .about-content p {
            color: var(--text-secondary);
            margin-bottom: 15px;
        }

        .education {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            margin-top: 25px;
        }

        .education-item {
            padding: 18px;
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 12px;
        }

        .education-item strong {
            display: block;
            color: var(--primary-dark);
        }

        .education-item span {
            color: var(--text-secondary);
            font-size: 14px;
        }

        /* SKILLS */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 25px;
        }

        .skill-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 18px;
            padding: 25px;
            box-shadow: var(--shadow);
            transition: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
        }

        .skill-icon {
            font-size: 40px;
            margin-bottom: 10px;
        }

        .skill-card h3 {
            font-size: 21px;
            margin-bottom: 8px;
        }

        .skill-card p {
            color: var(--text-secondary);
            font-size: 14px;
            margin-bottom: 18px;
        }

        .skill-bar {
            width: 100%;
            height: 9px;
            background: var(--background);
            border-radius: 20px;
            overflow: hidden;
            margin-bottom: 7px;
        }

        .skill-progress {
            height: 100%;
            background: var(--primary-dark);
            border-radius: 20px;
        }

        .html {
            width: 80%;
        }

        .css {
            width: 75%;
        }

        .javascript {
            width: 65%;
        }

        .uiux {
            width: 70%;
        }

        .skill-card > span {
            color: var(--primary-dark);
            font-weight: bold;
            font-size: 13px;
        }

        /* PROYEK */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 18px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-8px);
        }

        .project-icon {
            height: 170px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 65px;
            background: linear-gradient(135deg, #a9d1ed, #6fa9d5);
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .project-content p {
            color: var(--text-secondary);
            font-size: 14px;
            min-height: 70px;
        }

        .project-tags {
            display: flex;
            gap: 8px;
            margin: 15px 0;
            flex-wrap: wrap;
        }

        .project-tags span {
            background: var(--background);
            border: 1px solid var(--border);
            color: var(--primary-dark);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
        }

        .project-button {
            display: block;
            text-align: center;
            padding: 11px;
            background: var(--primary-dark);
            color: white;
            border-radius: 8px;
            font-weight: bold;
        }

        .project-button:hover {
            background: var(--primary);
        }

        /* KALKULATOR */
        .demo-section {
            width: 90%;
            max-width: 1100px;
            margin: 0 auto 30px;
            padding: 70px 20px;
        }

        .demo-box {
            padding: 50px;
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 20px;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .demo-number {
            color: var(--primary-dark);
            font-weight: bold;
        }

        .demo-box h2 {
            font-size: 32px;
            margin: 10px 0;
        }

        .demo-box p {
            color: var(--text-secondary);
            margin-bottom: 25px;
        }

        .calculator {
            max-width: 330px;
            margin: 30px auto 0;
            padding: 20px;
            background: var(--background);
            border: 1px solid var(--border);
            border-radius: 20px;
        }

        #display {
            width: 100%;
            height: 65px;
            margin-bottom: 15px;
            padding: 10px 15px;
            border: 1px solid var(--border);
            border-radius: 10px;
            background: var(--surface);
            color: var(--text);
            font-size: 25px;
            text-align: right;
        }

        .calculator-buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        .calculator-buttons button {
            height: 55px;
            border-radius: 10px;
            background: var(--surface);
            border: 1px solid var(--border);
            color: var(--text);
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }

        .calculator-buttons button:hover {
            background: var(--primary);
            color: white;
        }

        .calculator-buttons .zero {
            grid-column: span 2;
        }

        /* KONTAK */
        .contact-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .contact-card {
            text-align: center;
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 15px;
            padding: 30px 20px;
            transition: 0.3s;
        }

        .contact-card:hover {
            transform: translateY(-5px);
        }

        .contact-icon {
            font-size: 35px;
            margin-bottom: 10px;
        }

        .contact-card h3 {
            margin-bottom: 8px;
        }

        .contact-card a {
            color: var(--primary-dark);
            word-break: break-word;
        }

        .contact-card p {
            color: var(--text-secondary);
        }

        /* FOOTER */
        .footer {
            padding: 45px 20px;
            background: var(--surface);
            border-top: 1px solid var(--border);
            text-align: center;
        }

        .footer h3 {
            font-size: 25px;
        }

        .footer p {
            color: var(--text-secondary);
            font-size: 14px;
        }

        /* TOMBOL ATAS */
        .scroll-top {
            position: fixed;
            right: 25px;
            bottom: 25px;
            width: 45px;
            height: 45px;
            border: none;
            border-radius: 50%;
            background: var(--primary-dark);
            color: white;
            font-size: 22px;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: 0.3s;
            z-index: 999;
        }

        .scroll-top.show {
            opacity: 1;
            visibility: visible;
        }

        /* TABLET */
        @media (max-width: 900px) {

            .hero {
                min-height: auto;
                padding: 100px 0;
            }

            .hero-image {
                flex: 0 0 280px;
            }

            .image-circle {
                width: 270px;
                height: 270px;
            }

            .project-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .contact-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* HP */
        @media (max-width: 600px) {

            .navbar {
                min-height: 65px;
            }

            .menu-toggle {
                display: block;
                margin-left: auto;
            }

            .theme-toggle {
                width: 38px;
                height: 38px;
            }

            .nav-menu {
                position: absolute;
                top: 65px;
                left: 0;
                width: 100%;
                display: none;
                flex-direction: column;
                align-items: flex-start;
                padding: 20px 5%;
                background: var(--surface);
                border-bottom: 1px solid var(--border);
                gap: 18px;
            }

            .nav-menu.active {
                display: flex;
            }

            .hero {
                flex-direction: column-reverse;
                text-align: center;
                padding: 70px 0;
                gap: 35px;
            }

            .hero-image {
                flex: auto;
            }

            .image-circle {
                width: 230px;
                height: 230px;
            }

            .hero h1 {
                font-size: 42px;
            }

            .hero h2 {
                font-size: 23px;
            }

            .hero-content > p {
                font-size: 15px;
            }

            .hero-buttons {
                justify-content: center;
                flex-wrap: wrap;
            }

            .section {
                padding: 70px 0;
            }

            .section-title h2 {
                font-size: 30px;
            }

            .about-container {
                flex-direction: column;
            }

            .about-image {
                width: 100%;
                max-width: 300px;
            }

            .about-image img {
                height: 330px;
            }

            .about-content {
                text-align: center;
            }

            .education {
                grid-template-columns: 1fr;
            }

            .skills-container {
                grid-template-columns: 1fr;
            }

            .project-grid {
                grid-template-columns: 1fr;
            }

            .contact-container {
                grid-template-columns: 1fr;
            }

            .demo-box {
                padding: 35px 20px;
            }

            .demo-box h2 {
                font-size: 26px;
            }

            .demo-section {
                padding: 50px 10px;
            }
        }
    </style>
</head>

<body>

    <!-- HEADER -->
    <header class="header">
        <nav class="navbar">

            <a href="#beranda" class="logo">
                Gizella<span>.</span>
            </a>

            <button class="menu-toggle" id="menu-toggle">
                ☰
            </button>

            <ul class="nav-menu" id="nav-menu">
                <li><a href="#beranda">Beranda</a></li>
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#proyek">Proyek</a></li>
                <li><a href="#demo">Demo</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>

            <button class="theme-toggle" id="theme-toggle">
                🌙
            </button>

        </nav>
    </header>


    <main>

        <!-- BERANDA -->
        <section class="hero" id="beranda">

            <div class="hero-content">

                <p class="hero-small">HALO, SAYA</p>

                <h1>Gizella Al Zahra</h1>

                <h2>Pelajar <span>PPLG</span></h2>

                <p>
                    Saya adalah siswi kelas X RPL 3 yang sedang
                    belajar pengembangan perangkat lunak dan
                    desain UI/UX. Saya tertarik membuat website
                    yang menarik.
                </p>

                <div class="hero-buttons">

                    <a href="#proyek" class="button primary-button">
                        Lihat Proyek
                    </a>

                    <a href="#kontak" class="button secondary-button">
                        Hubungi Saya
                    </a>

                </div>

            </div>


            <div class="hero-image">

                <div class="image-circle">
                    <img src="https://uploads.onecompiler.io/45447qjvv/4544ayvsp/WhatsApp%20Image%202026-09-24%20at%2010.27.10.jpeg" 
                    alt="Foto Gizella Al Zahra">
                </div>

            </div>

        </section>


        <!-- TENTANG -->
        <section class="section" id="tentang">

            <div class="section-title">
                <p>TENTANG SAYA</p>
                <h2>Mengenal Saya</h2>
            </div>

            <div class="about-container">

                <div class="about-image">
                    <img src="https://uploads.onecompiler.io/45447qjvv/4544ayvsp/WhatsApp%20Image%202026-09-24%20at%2010.27.10.jpeg" alt="Foto Gizella Al Zahra">
                </div>

                <div class="about-content">

                    <h3>Gizella Al Zahra</h3>

                    <p>
                        Halo! Saya Gizella Al Zahra, siswi kelas
                        X RPL 3 di SMK Krian 1 Sidoarjo.
                        Saya sedang mempelajari HTML, CSS,
                        JavaScript, serta dasar-dasar UI/UX.
                    </p>

                    <p>
                        Saya ingin mengembangkan kemampuan saya
                        dalam membuat website yang sederhana,
                        menarik, dan mudah digunakan.
                    </p>

                    <div class="education">

                        <div class="education-item">
                            <strong>SD</strong>
                            <span>MI Miftahul Huda</span>
                        </div>

                        <div class="education-item">
                            <strong>SMP</strong>
                            <span> SMP Raden Rahmat</span>
                        </div>

                        <div class="education-item">
                            <strong>SMK</strong>
                            <span>SMK Krian 1 Sidoarjo</span>
                        </div>

                    </div>

                </div>

            </div>

        </section>


        <!-- SKILLS -->
        <section class="section" id="skills">

            <div class="section-title">
                <p>MY SKILLS</p>
                <h2>Kemampuan Saya</h2>
            </div>

            <div class="skills-container">

                <div class="skill-card">

                    <div class="skill-icon">🌐</div>

                    <h3>HTML</h3>

                    <p>
                        Membuat struktur halaman website
                        menggunakan HTML.
                    </p>

                    <div class="skill-bar">
                        <div class="skill-progress html"></div>
                    </div>

                    <span>80%</span>

                </div>


                <div class="skill-card">

                    <div class="skill-icon">🎨</div>

                    <h3>CSS</h3>

                    <p>
                        Membuat tampilan website yang rapi
                        dan responsif.
                    </p>

                    <div class="skill-bar">
                        <div class="skill-progress css"></div>
                    </div>

                    <span>75%</span>

                </div>


                <div class="skill-card">

                    <div class="skill-icon">⚡</div>

                    <h3>JavaScript</h3>

                    <p>
                        Membuat website menjadi lebih
                        interaktif.
                    </p>

                    <div class="skill-bar">
                        <div class="skill-progress javascript"></div>
                    </div>

                    <span>65%</span>

                </div>


                <div class="skill-card">

                    <div class="skill-icon">✨</div>

                    <h3>UI/UX</h3>

                    <p>
                        Membuat desain antarmuka yang
                        sederhana dan mudah digunakan.
                    </p>

                    <div class="skill-bar">
                        <div class="skill-progress uiux"></div>
                    </div>

                    <span>70%</span>

                </div>

            </div>

        </section>


        <!-- PROYEK -->
        <section class="section" id="proyek">

            <div class="section-title">
                <p>PORTOFOLIO</p>
                <h2>Proyek Saya</h2>
            </div>

            <div class="project-grid">

                <div class="project-card">

                    <div class="project-icon">
                        💻
                    </div>

                    <div class="project-content">

                        <h3>Website Portofolio</h3>

                        <p>
                            Website portofolio pribadi yang dibuat
                            menggunakan HTML dan CSS.
                        </p>

                        <div class="project-tags">
                            <span>HTML</span>
                            <span>CSS</span>
                        </div>

                        <a href="#beranda" class="project-button">
                            Lihat Proyek
                        </a>

                    </div>

                </div>


                <div class="project-card">

                    <div class="project-icon">
                        🎨
                    </div>

                    <div class="project-content">

                        <h3>Desain UI/UX</h3>

                        <p>
                            Desain antarmuka sederhana yang
                            mudah digunakan.
                        </p>

                        <div class="project-tags">
                            <span>UI/UX</span>
                            <span>Design</span>
                        </div>

                        <a href="#tentang" class="project-button">
                            Lihat Proyek
                        </a>

                    </div>

                </div>


                <div class="project-card">

                    <div class="project-icon">
                        🧮
                    </div>

                    <div class="project-content">

                        <h3>Kalkulator</h3>

                        <p>
                            Kalkulator sederhana menggunakan
                            HTML, CSS, dan JavaScript.
                        </p>

                        <div class="project-tags">
                            <span>HTML</span>
                            <span>JavaScript</span>
                        </div>

                        <a href="#demo" class="project-button">
                            Lihat Demo
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- DEMO KALKULATOR -->
        <section class="demo-section" id="demo">

            <div class="demo-box">

                <span class="demo-number">
                    PROJECT DEMO
                </span>

                <h2>Kalkulator Sederhana</h2>

                <p>
                    Contoh aplikasi sederhana menggunakan
                    JavaScript.
                </p>

                <div class="calculator">

                    <input
                        type="text"
                        id="display"
                        readonly
                    >

                    <div class="calculator-buttons">

                        <button onclick="clearDisplay()">C</button>
                        <button onclick="deleteLast()">⌫</button>
                        <button onclick="addValue('%')">%</button>
                        <button onclick="addValue('/')">÷</button>

                        <button onclick="addValue('7')">7</button>
                        <button onclick="addValue('8')">8</button>
                        <button onclick="addValue('9')">9</button>
                        <button onclick="addValue('*')">×</button>

                        <button onclick="addValue('4')">4</button>
                        <button onclick="addValue('5')">5</button>
                        <button onclick="addValue('6')">6</button>
                        <button onclick="addValue('-')">−</button>

                        <button onclick="addValue('1')">1</button>
                        <button onclick="addValue('2')">2</button>
                        <button onclick="addValue('3')">3</button>
                        <button onclick="addValue('+')">+</button>

                        <button class="zero" onclick="addValue('0')">
                            0
                        </button>

                        <button onclick="addValue('.')">
                            .
                        </button>

                        <button onclick="calculate()">
                            =
                        </button>

                    </div>

                </div>

            </div>

        </section>


        <!-- KONTAK -->
        <section class="section" id="kontak">

            <div class="section-title">

                <p>HUBUNGI SAYA</p>

                <h2>Kontak</h2>

            </div>

            <div class="contact-container">

                <!-- EMAIL -->
                <div class="contact-card">

                    <div class="contact-icon">
                        📧
                    </div>

                    <h3>Email</h3>

                    <a href="mailto:gizella@example.com">
                        gizellaalzahra8@gmail.com
                    </a>

                </div>


                <!-- INSTAGRAM -->
                <div class="contact-card">

                    <div class="contact-icon">
                        📸
                    </div>

                    <h3>Instagram</h3>

                    <a
                        href="https://instagram.com/usernamekamu"
                        target="_blank">
                        gizella41
                    </a>

                </div>


                <!-- LOKASI -->
                <div class="contact-card">

                    <div class="contact-icon">
                        📍
                    </div>

                    <h3>Lokasi</h3>

                    <p>
                        Sidoarjo, Jawa Timur
                    </p>

                </div>

            </div>

        </section>

    </main>


    <!-- FOOTER -->
    <footer class="footer">

        <h3>
            Gizella<span>.</span>
        </h3>

        <p>
            © 2026 Gizella Al Zahra. All Rights Reserved.
        </p>

    </footer>


    <!-- TOMBOL KE ATAS -->
    <button class="scroll-top" id="scroll-top">
        ↑
    </button>


    <script>

        /* MENU MOBILE */
        const menuToggle =
            document.getElementById("menu-toggle");

        const navMenu =
            document.getElementById("nav-menu");

        menuToggle.addEventListener("click", function () {
            navMenu.classList.toggle("active");
        });


        /* TUTUP MENU */
        document.querySelectorAll(".nav-menu a").forEach(function (link) {

            link.addEventListener("click", function () {
                navMenu.classList.remove("active");
            });

        });


        /* DARK MODE */
        const themeToggle =
            document.getElementById("theme-toggle");

        themeToggle.addEventListener("click", function () {

            document.body.classList.toggle("dark-mode");

            if (document.body.classList.contains("dark-mode")) {

                themeToggle.textContent = "☀️";

            } else {

                themeToggle.textContent = "🌙";

            }

        });


        /* KALKULATOR */
        const display =
            document.getElementById("display");


        function addValue(value) {

            display.value += value;

        }


        function clearDisplay() {

            display.value = "";

        }


        function deleteLast() {

            display.value =
                display.value.slice(0, -1);

        }


        function calculate() {

            try {

                if (display.value === "") {
                    return;
                }

                display.value =
                    eval(display.value);

            } catch (error) {

                display.value = "Error";

            }

        }


        /* TOMBOL KE ATAS */
        const scrollTop =
            document.getElementById("scroll-top");


        window.addEventListener("scroll", function () {

            if (window.scrollY > 300) {

                scrollTop.classList.add("show");

            } else {

                scrollTop.classList.remove("show");

            }

        });


        scrollTop.addEventListener("click", function () {

            window.scrollTo({
                top: 0,
                behavior: "smooth"
            });

        });

    </script>

</body>
</html>
