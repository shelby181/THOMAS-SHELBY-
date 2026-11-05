<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SHELBY | Personal Universe</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background: #0b0b0b;
            color: white;
            font-family: Georgia, serif;
        }

        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 22px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(0,0,0,0.9);
            z-index: 1000;
        }

        .logo {
            font-size: 25px;
            letter-spacing: 5px;
            color: #b5b5b5;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-size: 13px;
            letter-spacing: 2px;
        }

        nav a:hover {
            color: #a32626;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            background: linear-gradient(
                rgba(0,0,0,0.65),
                rgba(0,0,0,0.95)
            );
            padding: 30px;
        }

        .hero h1 {
            font-size: clamp(50px, 10vw, 100px);
            letter-spacing: 15px;
            animation: appear 2s ease;
        }

        .hero p {
            color: #999;
            letter-spacing: 5px;
            margin-top: 20px;
        }

        .line {
            width: 100px;
            height: 3px;
            background: #9e2525;
            margin: 30px auto;
        }

        .btn {
            display: inline-block;
            padding: 13px 30px;
            border: 1px solid #8e2525;
            color: white;
            text-decoration: none;
            letter-spacing: 3px;
            transition: 0.4s;
        }

        .btn:hover {
            background: #8e2525;
        }

        section {
            padding: 100px 10%;
            text-align: center;
        }

        section h2 {
            font-size: 32px;
            letter-spacing: 6px;
            margin-bottom: 30px;
        }

        section p {
            color: #aaa;
            line-height: 2;
            max-width: 700px;
            margin: auto;
        }

        .mindset {
            background: #151515;
        }

        .quote {
            font-size: 24px;
            font-style: italic;
            color: #ddd;
            margin-top: 30px;
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .card {
            padding: 35px 20px;
            background: #171717;
            border-bottom: 2px solid #8e2525;
            transition: 0.4s;
        }

        .card:hover {
            transform: translateY(-8px);
            background: #222;
        }

        .card h3 {
            margin-bottom: 15px;
            letter-spacing: 2px;
        }

        footer {
            padding: 30px;
            text-align: center;
            background: #050505;
            color: #666;
            letter-spacing: 2px;
            font-size: 12px;
        }

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

        @media(max-width: 600px) {
            header {
                padding: 18px 5%;
            }

            nav a {
                margin-left: 8px;
                font-size: 10px;
            }

            .hero h1 {
                letter-spacing: 7px;
            }
        }
    </style>
</head>

<body>

<header>
    <div class="logo">SHELBY.</div>

    <nav>
        <a href="#home">HOME</a>
        <a href="#about">ABOUT</a>
        <a href="#mindset">MINDSET</a>
        <a href="#projects">PROJECTS</a>
    </nav>
</header>

<div class="hero" id="home">
    <h1>SHELBY</h1>
    <div class="line"></div>
    <p>DISCIPLINE • SILENCE • POWER</p>
    <br><br>
    <a href="#about" class="btn">ENTER MY WORLD</a>
</div>

<section id="about">
    <h2>ABOUT ME</h2>
    <div class="line"></div>
    <p>
        I don't need to explain who I am.
        My actions will speak for me.
        I believe in discipline, patience,
        ambition and self-control.
        Every day is another opportunity
        to become better than yesterday.
    </p>
</section>

<section class="mindset" id="mindset">
    <h2>MY MINDSET</h2>
    <div class="line"></div>

    <p class="quote">
        "Sometimes silence is the most powerful answer."
    </p>

    <br>

    <p>
        Stay focused. Think deeply.
        Move silently. Work relentlessly.
    </p>
</section>

<section id="projects">
    <h2>MY PROJECTS</h2>
    <div class="line"></div>

    <div class="projects">

        <div class="card">
            <h3>01. TECHNOLOGY</h3>
            <p>Learning, coding and building my future.</p>
        </div>

        <div class="card">
            <h3>02. AMBITION</h3>
            <p>Dream big. Work hard. Never stop.</p>
        </div>

        <div class="card">
            <h3>03. DISCIPLINE</h3>
            <p>Building a stronger version of myself.</p>
        </div>

    </div>
</section>

<footer>
    © 2026 SHELBY. ALL RIGHTS RESERVED.
    <br><br>
    BY ORDER OF THE PEAKY BLINDERS.
</footer>

<script>
    console.log("Welcome to Shelby's world.");

    window.addEventListener("scroll", function() {
        const header = document.querySelector("header");

        if (window.scrollY > 50) {
            header.style.borderBottom = "1px solid #8e2525";
        } else {
            header.style.borderBottom = "none";
        }
    });
</script>

</body>
</html>
