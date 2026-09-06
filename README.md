<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

```
<title>Prince Kumar | Student Portfolio</title>

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html {
        scroll-behavior: smooth;
    }

    body {
        font-family: Arial, Helvetica, sans-serif;
        background: #f5f7fb;
        color: #172033;
        line-height: 1.6;
    }

    /* NAVBAR */
    .navbar {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
        background: rgba(10, 18, 35, 0.96);
        padding: 16px 7%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        color: white;
        font-size: 25px;
        font-weight: bold;
    }

    .logo span {
        color: #38bdf8;
    }

    .nav-links {
        display: flex;
        list-style: none;
        gap: 25px;
    }

    .nav-links a {
        color: white;
        text-decoration: none;
        font-size: 15px;
        transition: 0.3s;
    }

    .nav-links a:hover {
        color: #38bdf8;
    }

    .menu-btn {
        display: none;
        color: white;
        font-size: 27px;
        cursor: pointer;
    }

    /* HERO */
    .hero {
        min-height: 100vh;
        padding: 120px 7% 70px;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        color: white;
        background:
            radial-gradient(circle at top left, #2563eb, transparent 35%),
            radial-gradient(circle at bottom right, #0891b2, transparent 35%),
            #0b1220;
    }

    .hero-content {
        max-width: 850px;
    }

    .hello {
        color: #7dd3fc;
        font-size: 18px;
        margin-bottom: 10px;
    }

    .hero h1 {
        font-size: clamp(42px, 8vw, 80px);
        line-height: 1.1;
        margin-bottom: 18px;
    }

    .hero h1 span {
        color: #38bdf8;
    }

    .typing {
        min-height: 38px;
        font-size: 25px;
        color: #e0f2fe;
        margin-bottom: 18px;
    }

    .hero-description {
        max-width: 680px;
        margin: auto;
        color: #cbd5e1;
        font-size: 18px;
    }

    .buttons {
        margin-top: 30px;
    }

    .btn {
        display: inline-block;
        padding: 13px 24px;
        margin: 6px;
        border-radius: 8px;
        text-decoration: none;
        font-weight: bold;
        transition: 0.3s;
    }

    .primary-btn {
        background: #38bdf8;
        color: #082f49;
    }

    .primary-btn:hover {
        transform: translateY(-3px);
        background: #7dd3fc;
    }

    .secondary-btn {
        border: 1px solid #94a3b8;
        color: white;
    }

    .secondary-btn:hover {
        background: white;
        color: #0f172a;
    }

    /* GENERAL */
    section {
        padding: 90px 7%;
    }

    .section-heading {
        text-align: center;
        margin-bottom: 45px;
    }

    .section-heading h2 {
        font-size: 38px;
        margin-bottom: 8px;
        color: #0f172a;
    }

    .section-heading p {
        color: #64748b;
    }

    .container {
        max-width: 1050px;
        margin: auto;
    }

    /* ABOUT */
    .about-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 25px;
    }

    .card {
        background: white;
        border-radius: 16px;
        padding: 30px;
        box-shadow: 0 8px 30px rgba(15, 23, 42, 0.08);
    }

    .card h3 {
        color: #0f172a;
        margin-bottom: 14px;
        font-size: 22px;
    }

    .card p {
        color: #475569;
    }

    /* INFORMATION */
    .info-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 18px;
    }

    .info-item {
        background: white;
        padding: 23px;
        border-radius: 14px;
        box-shadow: 0 6px 25px rgba(15, 23, 42, 0.06);
    }

    .info-item strong {
        display: block;
        color: #2563eb;
        margin-bottom: 5px;
    }

    /* SCHOOL */
    .school-box {
        max-width: 850px;
        margin: auto;
        padding: 40px;
        background: white;
        border-radius: 18px;
        text-align: center;
        box-shadow: 0 8px 30px rgba(15, 23, 42, 0.08);
    }

    .school-icon {
        font-size: 55px;
        margin-bottom: 15px;
    }

    .school-box h3 {
        font-size: 27px;
        margin-bottom: 12px;
    }

    .school-box p {
        color: #475569;
    }

    /* GOAL */
    .goal {
        background: #0f172a;
        color: white;
    }

    .goal .section-heading h2 {
        color: white;
    }

    .goal .section-heading p {
        color: #94a3b8;
    }

    .goal-box {
        max-width: 850px;
        margin: auto;
        padding: 45px;
        text-align: center;
        border: 1px solid #334155;
        border-radius: 20px;
        background: #111c31;
    }

    .goal-icon {
        font-size: 55px;
        margin-bottom: 15px;
    }

    .goal-box h3 {
        font-size: 30px;
        color: #7dd3fc;
        margin-bottom: 15px;
    }

    .goal-box p {
        color: #cbd5e1;
    }

    /* HOBBIES */
    .hobby-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
    }

    .hobby {
        background: white;
        padding: 30px;
        border-radius: 16px;
        text-align: center;
        box-shadow: 0 7px 25px rgba(15, 23, 42, 0.07);
        transition: 0.3s;
    }

    .hobby:hover {
        transform: translateY(-7px);
    }

    .hobby-icon {
        font-size: 40px;
        margin-bottom: 10px;
    }

    .hobby h3 {
        margin-bottom: 8px;
    }

    .hobby p {
        color: #64748b;
    }

    /* SKILLS */
    .skills {
        max-width: 850px;
        margin: auto;
    }

    .skill {
        margin-bottom: 22px;
    }

    .skill-title {
        display: flex;
        justify-content: space-between;
        margin-bottom: 7px;
        font-weight: bold;
    }

    .progress {
        height: 10px;
        background: #dbe3ed;
        border-radius: 20px;
        overflow: hidden;
    }

    .progress-bar {
        height: 100%;
        background: #2563eb;
        border-radius: 20px;
    }

    /* CONTACT */
    .contact {
        background: #eaf6ff;
    }

    .contact-box {
        max-width: 700px;
        margin: auto;
        text-align: center;
        background: white;
        padding: 40px;
        border-radius: 18px;
        box-shadow: 0 8px 30px rgba(15, 23, 42, 0.08);
    }

    .contact-box h3 {
        font-size: 27px;
        margin-bottom: 15px;
    }

    .contact-box p {
        margin: 8px 0;
        color: #475569;
    }

    /* FOOTER */
    footer {
        background: #020617;
        color: #94a3b8;
        text-align: center;
        padding: 25px;
    }

    footer strong {
        color: white;
    }

    /* SCROLL ANIMATION */
    .reveal {
        opacity: 0;
        transform: translateY(30px);
        transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .reveal.show {
        opacity: 1;
        transform: translateY(0);
    }

    /* MOBILE */
    @media (max-width: 768px) {
        .navbar {
            padding: 15px 5%;
        }

        .menu-btn {
            display: block;
        }

        .nav-links {
            display: none;
            position: absolute;
            top: 62px;
            left: 0;
            width: 100%;
            background: #0a1223;
            flex-direction: column;
            text-align: center;
            padding: 20px;
            gap: 18px;
        }

        .nav-links.open {
            display: flex;
        }

        section {
            padding: 70px 5%;
        }

        .about-grid,
        .info-grid,
        .hobby-grid {
            grid-template-columns: 1fr;
        }

        .hero {
            padding-left: 5%;
            padding-right: 5%;
        }

        .hero h1 {
            font-size: 45px;
        }

        .typing {
            font-size: 21px;
        }

        .hero-description {
            font-size: 16px;
        }

        .section-heading h2 {
            font-size: 31px;
        }

        .school-box,
        .goal-box,
        .contact-box {
            padding: 28px 20px;
        }
    }
</style>
```

</head>

<body>

```
<!-- NAVIGATION -->
<nav class="navbar">
    <div class="logo">Prince<span>.</span></div>

    <div class="menu-btn" id="menuBtn">
        ☰
    </div>

    <ul class="nav-links" id="navLinks">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#school">School</a></li>
        <li><a href="#goal">Goal</a></li>
        <li><a href="#hobbies">Hobbies</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>


<!-- HOME -->
<section class="hero" id="home">
    <div class="hero-content">

        <div class="hello">Hello, I'm</div>

        <h1>Prince <span>Kumar</span></h1>

        <div class="typing" id="typing"></div>

        <p class="hero-description">
            I am a student from Bihar, India, interested in
            technology and website development. I enjoy learning
            new things and building websites.
        </p>

        <div class="buttons">
            <a href="#about" class="btn primary-btn">
                Explore My Portfolio
            </a>

            <a href="#contact" class="btn secondary-btn">
                Contact
            </a>
        </div>

    </div>
</section>


<!-- ABOUT -->
<section id="about" class="reveal">

    <div class="section-heading">
        <h2>About Me</h2>
        <p>Get to know me</p>
    </div>

    <div class="container about-grid">

        <div class="card">
            <h3>Who I Am</h3>

            <p>
                My name is <strong>Prince Kumar</strong>.
                I am a student from Bihar, India. I like learning,
                exploring technology and developing new skills.
            </p>

            <br>

            <p>
                I am curious about how websites work and enjoy
                creating web pages using HTML, CSS and JavaScript.
            </p>
        </div>

        <div class="card">
            <h3>My Mindset</h3>

            <p>
                I believe that every day is an opportunity to learn
                something new. I want to improve my knowledge,
                creativity, communication and problem-solving skills.
            </p>

            <br>

            <p>
                My long-term goal is to use my education and skills
                to make a positive contribution to society.
            </p>
        </div>

    </div>
</section>


<!-- PERSONAL INFORMATION -->
<section class="reveal">

    <div class="section-heading">
        <h2>Personal Information</h2>
        <p>A few details about me</p>
    </div>

    <div class="container info-grid">

        <div class="info-item">
            <strong>👤 Name</strong>
            Prince Kumar
        </div>

        <div class="info-item">
            <strong>📍 Location</strong>
            Bihar, India
        </div>

        <div class="info-item">
            <strong>🎓 Role</strong>
            Student
        </div>

        <div class="info-item">
            <strong>💻 Main Interest</strong>
            Website Development
        </div>

    </div>
</section>


<!-- SCHOOL -->
<section id="school" class="reveal">

    <div class="section-heading">
        <h2>My School</h2>
        <p>My educational journey</p>
    </div>

    <div class="school-box">

        <div class="school-icon">🏫</div>

        <h3>My School</h3>

        <p>
            My school is located approximately one kilometre
            from Hatia Chowk in Bihar.
        </p>

        <br>

        <p>
            Education is an important part of my journey.
            I want to use my school years to build a strong
            foundation of knowledge, discipline and confidence.
        </p>

    </div>
</section>


<!-- GOAL -->
<section class="goal reveal" id="goal">

    <div class="section-heading">
        <h2>My Future Goal</h2>
        <p>The dream I am working toward</p>
    </div>

    <div class="goal-box">

        <div class="goal-icon">🇮🇳</div>

        <h3>Become an IAS Officer</h3>

        <p>
            My goal is to become an Indian Administrative Service
            (IAS) officer. I want to develop strong knowledge,
            discipline, leadership and problem-solving abilities.
        </p>

        <br>

        <p>
            I hope to use these qualities in the future to serve
            people and contribute positively to the country.
        </p>

    </div>
</section>


<!-- HOBBIES -->
<section id="hobbies" class="reveal">

    <div class="section-heading">
        <h2>My Hobbies & Interests</h2>
        <p>Things I enjoy</p>
    </div>

    <div class="container hobby-grid">

        <div class="hobby">
            <div class="hobby-icon">💻</div>
            <h3>Website Development</h3>
            <p>
                I enjoy creating websites and experimenting
                with HTML, CSS and JavaScript.
            </p>
        </div>

        <div class="hobby">
            <div class="hobby-icon">📚</div>
            <h3>Learning</h3>
            <p>
                I enjoy discovering new topics and
                increasing my knowledge.
            </p>
        </div>

        <div class="hobby">
            <div class="hobby-icon">🧠</div>
            <h3>General Knowledge</h3>
            <p>
                I am interested in learning about society,
                the world and different subjects.
            </p>
        </div>

        <div class="hobby">
            <div class="hobby-icon">🚀</div>
            <h3>Technology</h3>
            <p>
                I enjoy exploring technology and discovering
                what I can create with it.
            </p>
        </div>

    </div>
</section>


<!-- SKILLS -->
<section id="skills" class="reveal">

    <div class="section-heading">
        <h2>My Skills</h2>
        <p>Skills I am developing</p>
    </div>

    <div class="skills">

        <div class="skill">
            <div class="skill-title">
                <span>HTML</span>
                <span>Learning</span>
            </div>

            <div class="progress">
                <div class="progress-bar" style="width: 75%;"></div>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>CSS</span>
                <span>Learning</span>
            </div>

            <div class="progress">
                <div class="progress-bar" style="width: 65%;"></div>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>JavaScript</span>
                <span>Learning</span>
            </div>

            <div class="progress">
                <div class="progress-bar" style="width: 50%;"></div>
            </div>
        </div>

        <div class="skill">
            <div class="skill-title">
                <span>Problem Solving</span>
                <span>Developing</span>
            </div>

            <div class="progress">
                <div class="progress-bar" style="width: 60%;"></div>
            </div>
        </div>

    </div>
</section>


<!-- CONTACT -->
<section class="contact reveal" id="contact">

    <div class="section-heading">
        <h2>Contact</h2>
        <p>Thank you for visiting my portfolio</p>
    </div>

    <div class="contact-box">

        <h3>Prince Kumar</h3>

        <p>📍 Bihar, India</p>
        <p>🎓 Student</p>
        <p>💻 Website Development Enthusiast</p>
        <p>🎯 Future Goal: IAS Officer</p>

        <br>

        <p>
            This portfolio is a simple static website created
            with HTML, CSS and JavaScript.
        </p>

    </div>
</section>


<!-- FOOTER -->
<footer>

    <p>
        © <span id="year"></span>
        <strong>Prince Kumar</strong>.
        All rights reserved.
    </p>

    <p>
        Built with HTML, CSS & JavaScript.
    </p>

</footer>


<script>

    /* =========================
       MOBILE MENU
    ========================= */

    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", function () {
        navLinks.classList.toggle("open");
    });

    document.querySelectorAll(".nav-links a").forEach(function (link) {
        link.addEventListener("click", function () {
            navLinks.classList.remove("open");
        });
    });


    /* =========================
       TYPING EFFECT
    ========================= */

    const typing = document.getElementById("typing");

    const words = [
        "Student",
        "Web Developer in Learning",
        "Technology Enthusiast",
        "Future IAS Officer"
    ];

    let wordIndex = 0;
    let letterIndex = 0;
    let deleting = false;

    function typeText() {

        const word = words[wordIndex];

        if (!deleting) {

            typing.textContent =
                word.substring(0, letterIndex + 1);

            letterIndex++;

            if (letterIndex === word.length) {

                deleting = true;

                setTimeout(typeText, 1400);

                return;
            }

        } else {

            typing.textContent =
                word.substring(0, letterIndex - 1);

            letterIndex--;

            if (letterIndex === 0) {

                deleting = false;

                wordIndex++;

                if (wordIndex >= words.length) {
                    wordIndex = 0;
                }
            }
        }

        setTimeout(
            typeText,
            deleting ? 50 : 90
        );
    }

    typeText();


    /* =========================
       SCROLL REVEAL
    ========================= */

    const revealElements =
        document.querySelectorAll(".reveal");

    function revealOnScroll() {

        revealElements.forEach(function (element) {

            const position =
                element.getBoundingClientRect().top;

            if (position < window.innerHeight - 80) {
                element.classList.add("show");
            }
        });
    }

    window.addEventListener(
        "scroll",
        revealOnScroll
    );

    revealOnScroll();


    /* =========================
       CURRENT YEAR
    ========================= */

    document.getElementById("year").textContent =
        new Date().getFullYear();

</script>
```

</body>
</html>
