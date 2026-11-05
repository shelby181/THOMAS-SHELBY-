<!DOCTYPE html>
*Peaky blinders* 
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SHELBY | The Personal Universe</title>

<style>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    background: #080808;
    color: white;
    font-family: Georgia, serif;
}

/* HEADER */

header {
    position: fixed;
    top: 0;
    width: 100%;
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(0,0,0,0.88);
    backdrop-filter: blur(10px);
    z-index: 1000;
    border-bottom: 1px solid #292020;
}

.logo {
    font-size: 25px;
    letter-spacing: 6px;
    color: #ddd;
}

nav a {
    color: #ccc;
    text-decoration: none;
    margin-left: 18px;
    font-size: 11px;
    letter-spacing: 2px;
    transition: .4s;
}

nav a:hover {
    color: #a52a2a;
}

/* HERO */

.hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 25px;

    background-image:
    linear-gradient(
        rgba(0,0,0,0.40),
        rgba(0,0,0,0.85)
    ),
    url("./881efc980698fd4e33b79e7abb40cee7.jpg");

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.hero h1 {
    font-size: clamp(55px, 12vw, 120px);
    letter-spacing: 15px;
    text-shadow: 0 5px 25px black;
    animation: appear 2s ease;
}

.hero p {
    color: #ddd;
    letter-spacing: 5px;
    margin-top: 20px;
}

.line {
    width: 90px;
    height: 3px;
    background: #922727;
    margin: 30px auto;
}

/* BUTTON */

.btn {
    padding: 15px 35px;
    border: 1px solid #922727;
    color: white;
    background: transparent;
    text-decoration: none;
    letter-spacing: 3px;
    cursor: pointer;
    transition: .4s;
}

.btn:hover {
    background: #922727;
    box-shadow: 0 0 20px #922727;
}

/* SECTIONS */

section {
    padding: 110px 10%;
    text-align: center;
}

section h2 {
    font-size: 30px;
    letter-spacing: 7px;
}

section p {
    color: #aaa;
    line-height: 2;
    max-width: 700px;
    margin: auto;
}

.dark {
    background: #121212;
}

/* QUOTES */

.quote {
    font-size: 24px;
    font-style: italic;
    color: #ddd;
    margin: 30px auto;
}

/* PROJECTS */

.projects {
    display: grid;
    grid-template-columns: repeat(
        auto-fit,
        minmax(220px, 1fr)
    );
    gap: 25px;
    margin-top: 40px;
}

.card {
    padding: 40px 20px;
    background: #171717;
    border-bottom: 2px solid #922727;
    transition: .4s;
}

.card:hover {
    transform: translateY(-10px);
    background: #222;
}

.card h3 {
    margin-bottom: 20px;
    letter-spacing: 3px;
}

/* SECRET */

.hidden-message {
    display: none;
    margin-top: 30px;
    color: #c78b8b;
    animation: appear 1s ease;
}

/* FOOTER */

footer {
    background: #050505;
    padding: 35px;
    text-align: center;
    color: #666;
    font-size: 12px;
    letter-spacing: 3px;
}

/* ANIMATION */

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* MOBILE */

@media(max-width: 600px) {

    header {
        padding: 18px 4%;
    }

    nav a {
        margin-left: 6px;
        font-size: 9px;
        letter-spacing: 1px;
    }

    .hero h1 {
        letter-spacing: 7px;
    }

    section {
        padding: 85px 7%;
    }

}

</style>
</head>

<body>

<!-- NAVIGATION -->

<header>

    <div class="logo">SHELBY.</div>

    <nav>
        <a href="#home">HOME</a>
        <a href="#about">ABOUT</a>
        <a href="#mindset">MINDSET</a>
        <a href="#projects">PROJECTS</a>
    </nav>

</header>

<!-- HOME -->

<div class="hero" id="home">

    <h1>SHELBY</h1>

    <div class="line"></div>

    <p>DISCIPLINE • SILENCE • POWER</p>

    <br><br>

    <a href="#about" class="btn">
        ENTER MY WORLD
    </a>

</div>

<!-- ABOUT -->

<section id="about">

    <h2>WHO AM I?</h2>

    <div class="line"></div>

    <p>
        I am not here to impress anyone.

        I am here to build something meaningful.

        My journey is private, my ambitions are big,
        and my silence has a purpose.

        I believe in discipline, patience and ambition.
    </p>

</section>

<!-- MINDSET -->

<section class="dark" id="mindset">

    <h2>THE MINDSET</h2>

    <div class="line"></div>

    <p class="quote" id="quote">
        "Sometimes silence is the most powerful answer."
    </p>

    <button class="btn" onclick="changeQuote()">
        NEXT QUOTE
    </button>

</section>

<!-- PROJECTS -->

<section id="projects">

    <h2>MY WORLD</h2>

    <div class="line"></div>

    <div class="projects">

        <div class="card">
            <h3>TECHNOLOGY</h3>
            <p>Creating. Learning. Innovating.</p>
        </div>

        <div class="card">
            <h3>AMBITION</h3>
            <p>My future is my responsibility.</p>
        </div>

        <div class="card">
            <h3>DISCIPLINE</h3>
            <p>Consistency over motivation.</p>
        </div>

    </div>

</section>

<!-- SECRET MESSAGE -->

<section class="dark">

    <h2>ONE LAST THING</h2>

    <div class="line"></div>

    <button class="btn" onclick="revealMessage()">
        DISCOVER
    </button>

    <p class="hidden-message" id="secret">

        The world belongs to those
        who have the courage to create
        their own path.
