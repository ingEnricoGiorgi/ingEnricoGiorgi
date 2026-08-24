<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Enrico Giorgi | Backend Developer</title>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background:
        radial-gradient(circle at 50% 0%, #18214a 0%, #080d1d 35%, #03060e 100%);
    color: white;
    min-height: 100vh;
}

a {
    color: inherit;
    text-decoration: none;
}

/* =========================
   NAVBAR
========================= */

nav {
    position: sticky;
    top: 0;
    z-index: 1000;

    display: flex;
    justify-content: center;
    gap: 60px;

    padding: 20px;

    background: rgba(3, 6, 14, 0.80);
    backdrop-filter: blur(15px);

    border-bottom: 1px solid rgba(255,255,255,0.08);
}

nav a {
    color: #cfd3e6;
    font-size: 14px;
    text-transform: uppercase;
    letter-spacing: 1px;

    transition: 0.3s;
}

nav a:hover {
    color: #a56cff;
}

/* =========================
   HERO
========================= */

.hero {
    min-height: 620px;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    text-align: center;

    padding: 80px 20px;

    position: relative;
    overflow: hidden;
}

.hero::before {
    content: "";
    position: absolute;

    width: 700px;
    height: 700px;

    background: radial-gradient(
        circle,
        rgba(124, 83, 255, 0.25),
        transparent 70%
    );

    top: -250px;
    left: 50%;
    transform: translateX(-50%);

    pointer-events: none;
}

.hero h1 {
    font-size: clamp(55px, 9vw, 120px);

    font-style: italic;
    font-weight: 900;

    letter-spacing: 5px;

    position: relative;

    text-shadow:
        0 0 30px rgba(122, 92, 255, 0.25);
}

.line {
    width: 100px;
    height: 4px;

    margin: 25px auto;

    border-radius: 20px;

    background: linear-gradient(
        90deg,
        #9c5cff,
        #55aaff
    );
}

.hero h2 {
    font-size: clamp(22px, 3vw, 34px);

    color: #b064ff;

    margin-bottom: 15px;

    text-transform: uppercase;

    letter-spacing: 2px;
}

.hero p {
    color: #e3e5ed;

    font-size: 20px;

    letter-spacing: 2px;
}

.socials {
    display: flex;
    gap: 15px;

    margin-top: 35px;
}

.social-button {
    width: 50px;
    height: 50px;

    border-radius: 50%;

    display: flex;
    align-items: center;
    justify-content: center;

    border: 1px solid rgba(255,255,255,0.18);

    background: rgba(255,255,255,0.05);

    font-size: 21px;

    transition: 0.3s;
}

.social-button:hover {
    transform: translateY(-5px);

    border-color: #a56cff;

    background: rgba(156,92,255,0.18);
}

/* =========================
   GENERAL
========================= */

.container {
    width: min(1150px, 92%);

    margin: auto;

    padding-bottom: 100px;
}

.section {
    margin-bottom: 30px;

    border: 1px solid rgba(255,255,255,0.08);

    background:
        linear-gradient(
            135deg,
            rgba(29, 24, 70, 0.75),
            rgba(7, 15, 34, 0.82)
        );

    border-radius: 18px;

    padding: 35px;

    box-shadow:
        0 20px 50px rgba(0,0,0,0.30);

    backdrop-filter: blur(10px);
}

.section-title {
    font-size: 26px;

    margin-bottom: 25px;

    text-transform: uppercase;
}

.section-title::after {
    content: "";

    display: block;

    width: 40px;
    height: 3px;

    margin-top: 10px;

    border-radius: 10px;

    background: #9b5cff;
}

/* =========================
   ABOUT
========================= */

.about-list {
    list-style: none;
}

.about-list li {
    margin: 16px 0;

    font-size: 17px;

    color: #d9dbea;
}

.about-list li::before {
    content: "✓";

    color: #b268ff;

    margin-right: 12px;

    font-weight: bold;
}

/* =========================
   PRODUCTION
========================= */

.production {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 35px;

    align-items: center;
}

.production-visual {
    min-height: 250px;

    border-radius: 15px;

    display: flex;
    align-items: center;
    justify-content: center;

    background:
        linear-gradient(
            135deg,
            rgba(156,92,255,0.18),
            rgba(70,112,255,0.08)
        );

    border: 1px solid rgba(255,255,255,0.08);

    font-size: 70px;
}

.production h3 {
    margin-bottom: 15px;

    font-size: 24px;
}

.production-link {
    color: #9f79ff;

    display: inline-block;

    margin-bottom: 15px;
}

.production ul {
    list-style: none;
}

.production li {
    margin: 12px 0;

    color: #d7d9e3;
}

.production li::before {
    content: "✓";

    color: #b268ff;

    margin-right: 10px;
}

/* =========================
   PROJECT CARDS
========================= */

.projects {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;
}

.card {
    padding: 28px;

    min-height: 300px;

    border-radius: 14px;

    background:
        linear-gradient(
            160deg,
            rgba(31, 37, 78, 0.78),
            rgba(7, 14, 32, 0.95)
        );

    border: 1px solid rgba(255,255,255,0.07);

    transition: 0.3s;
}

.card:hover {
    transform: translateY(-7px);

    border-color: rgba(165,108,255,0.45);

    box-shadow:
        0 20px 40px rgba(0,0,0,0.35);
}

.card-icon {
    font-size: 45px;

    margin-bottom: 20px;
}

.card h3 {
    margin-bottom: 20px;

    font-size: 20px;
}

.card ul {
    list-style: none;
}

.card li {
    margin: 13px 0;

    color: #d0d2de;

    line-height: 1.5;
}

.card li::before {
    content: "◉";

    color: #9d66ff;

    margin-right: 9px;
}

/* =========================
   TECH STACK
========================= */

.tech-grid {
    display: grid;

    grid-template-columns:
        repeat(6, 1fr);

    gap: 15px;
}

.tech {
    text-align: center;

    padding: 22px 10px;

    border-radius: 12px;

    background: rgba(255,255,255,0.025);

    border: 1px solid rgba(255,255,255,0.05);

    transition: 0.3s;
}

.tech:hover {
    transform: translateY(-5px);

    background: rgba(156,92,255,0.08);
}

.tech-icon {
    font-size: 38px;

    margin-bottom: 10px;
}

.tech span {
    color: #e7e8ef;

    font-size: 14px;
}

/* =========================
   CONTACT
========================= */

.bottom-grid {
    display: grid;

    grid-template-columns:
        1fr 1fr;

    gap: 30px;
}

.contact-link {
    display: inline-block;

    margin-top: 10px;

    color: #a97cff;

    word-break: break-word;
}

.snake-container {
    overflow-x: auto;

    margin-top: 20px;
}

.snake-container img {
    max-width: 100%;
}

/* =========================
   FOOTER
========================= */

footer {
    text-align: center;

    padding: 30px;

    color: #777f9b;

    font-size: 13px;
}

/* =========================
   MOBILE
========================= */

@media(max-width: 850px) {

    nav {
        gap: 20px;
        flex-wrap: wrap;
    }

    .production {
        grid-template-columns: 1fr;
    }

    .projects {
        grid-template-columns: 1fr;
    }

    .tech-grid {
        grid-template-columns:
            repeat(3, 1fr);
    }

    .bottom-grid {
        grid-template-columns: 1fr;
    }
}

@media(max-width: 500px) {

    .hero {
        min-height: 520px;
    }

    .hero h1 {
        font-size: 52px;
        letter-spacing: 1px;
    }

    .hero h2 {
        font-size: 20px;
    }

    .hero p {
        font-size: 16px;
    }

    .section {
        padding: 25px 20px;
    }

    .tech-grid {
        grid-template-columns:
            repeat(2, 1fr);
    }

}

</style>

</head>


<body>


<!-- NAVBAR -->

<nav>

<a href="#about">
ABOUT
</a>

<a href="#projects">
PROJECTS
</a>

<a href="#stack">
TECH STACK
</a>

<a href="#contact">
CONTACT
</a>

</nav>



<!-- HERO -->

<section class="hero">

<h1>
ENRICO GIORGI
</h1>

<div class="line"></div>

<h2>
Junior Backend Developer
</h2>

<p>
PHP · Laravel · Magento
</p>


<div class="socials">

<a
class="social-button"
href="https://www.linkedin.com/in/enrico-giorgi-1b20bb184/"
target="_blank"
title="LinkedIn"
>
in
</a>


<a
class="social-button"
href="https://github.com/ingEnricoGiorgi"
target="_blank"
title="GitHub"
>
⌘
</a>


<a
class="social-button"
href="#contact"
title="Contact"
>
✉
</a>

</div>

</section>



<div class="container">


<!-- ABOUT -->

<section
class="section"
id="about"
>

<h2 class="section-title">
About Me
</h2>

<ul class="about-list">

<li>
Practical experience on real projects
</li>

<li>
Backend development and database management
</li>

<li>
API integration and debugging
</li>

<li>
Experience with Magento and Laravel
</li>

</ul>

</section>



<!-- PRODUCTION -->

<section class="section">

<h2 class="section-title">
Production Project
</h2>

<div class="production">

<div class="production-visual">
🌐
</div>


<div>

<h3>
Website WordPress in production
</h3>

<a
class="production-link"
href="https://www.avvalessandragiorgi.it/"
target="_blank"
>
www.avvalessandragiorgi.it ↗
</a>


<ul>

<li>
Development and management of a live website
</li>

<li>
Deployment and hosting configuration
</li>

<li>
Content and structure management
</li>

</ul>

</div>

</div>

</section>



<!-- PROJECTS -->

<section
class="section"
id="projects"
>

<h2 class="section-title">
Main Projects
</h2>


<div class="projects">


<!-- LARAVEL -->

<div class="card">

<div class="card-icon">
🔺
</div>

<h3>
CRM Laravel
</h3>

<ul>

<li>
Full CRUD implementation
</li>

<li>
Relational database management
</li>

<li>
Structured backend architecture
</li>

</ul>

</div>



<!-- NODE -->

<div class="card">

<div class="card-icon">
🟢
</div>

<h3>
NodeJS JWT Auth
</h3>

<ul>

<li>
REST API
</li>

<li>
JWT authentication
</li>

<li>
Backend authentication flow
</li>

</ul>

</div>



<!-- MAGENTO -->

<div class="card">

<div class="card-icon">
🟧
</div>

<h3>
Magento eCommerce Platform
</h3>

<a
class="production-link"
href="https://reflexmania.it/"
target="_blank"
>
reflexmania.it ↗
</a>

<ul>

<li>
Contributed to development and maintenance
</li>

<li>
Backend customizations and configuration
</li>

<li>
Debugging and issue resolution in production
</li>

</ul>

</div>


</div>

</section>



<!-- TECH -->

<section
class="section"
id="stack"
>

<h2 class="section-title">
Tech Stack
</h2>


<div class="tech-grid">


<div class="tech">

<div class="tech-icon">
🐘
</div>

<span>
PHP
</span>

</div>


<div class="tech">

<div class="tech-icon">
🔺
</div>

<span>
Laravel
</span>

</div>


<div class="tech">

<div class="tech-icon">
🟧
</div>

<span>
Magento
</span>

</div>


<div class="tech">

<div class="tech-icon">
🐬
</div>

<span>
MySQL
</span>

</div>


<div class="tech">

<div class="tech-icon">
🐳
</div>

<span>
Docker
</span>

</div>


<div class="tech">

<div class="tech-icon">
🟨
</div>

<span>
JavaScript
</span>

</div>


</div>

</section>



<!-- BOTTOM -->

<div class="bottom-grid">


<!-- CONTACT -->

<section
class="section"
id="contact"
>

<h2 class="section-title">
Contact
</h2>

<p>
LinkedIn
</p>

<a
class="contact-link"
href="https://www.linkedin.com/in/enrico-giorgi-1b20bb184/"
target="_blank"
>
linkedin.com/in/enrico-giorgi-1b20bb184
</a>

</section>



<!-- CONTRIBUTIONS -->

<section class="section">

<h2 class="section-title">
Contributions
</h2>


<div class="snake-container">

<img
src="https://raw.githubusercontent.com/ingEnricoGiorgi/ingEnricoGiorgi/output/github-contribution-grid-snake.svg"
alt="GitHub contribution snake"
>

</div>

</section>


</div>


</div>



<footer>

© 2026 Enrico Giorgi

</footer>


</body>
</html>
