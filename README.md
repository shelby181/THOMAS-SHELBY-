<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SHELBY | The Mindset</title>

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

header {
    position: fixed;
    width: 100%;
    top: 0;
    padding: 22px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(0,0,0,.95);
    z-index: 1000;
}

.logo {
    font-size: 25px;
    letter-spacing: 6px;
    color: #b5b5b5;
}

nav a {
    color: #ccc;
    text-decoration: none;
    margin-left: 20px;
    font-size: 12px;
    letter-spacing: 2px;
    transition: .3s;
}

nav a:hover {
    color: #a52a2a;
}

.hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 25px;
    background:
    linear-gradient(rgba(0,0,0,.75),rgba(0,0,0,.95)),
    radial-gradient(circle at center,#292020,#080808 70%);
}

.hero h1 {
    font-size: clamp(55px,12vw,120px);
    letter-spacing: 15px;
    animation: fade 2s ease;
}

.hero p {
    color: #aaa;
    letter-spacing: 5px;
    margin-top: 20px;
}

.line {
    width: 90px;
    height: 3px;
    background: #922727;
    margin: 30px auto;
}

.btn {
    padding: 15px 35px;
    border: 1px solid #922727;
    color: white;
    text-decoration: none;
    letter-spacing: 3px;
    transition: .4s;
    cursor: pointer;
    background: transparent;
}

.btn:hover {
    background: #922727;
    box-shadow: 0 0 20px #922727;
}

section {
    padding: 110px 10%;
    text-align: center;
}

h2 {
    font-size: 32px;
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

.quote {
    font-size: 25px;
    font-style: italic;
    color: #ddd;
    margin: 30px auto;
}

.projects {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
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

.hidden-message {
    display: none;
    margin-top: 30px;
    color: #c78b8b;
    animation: fade 1s ease;
}

footer {
    background: #050505;
    padding: 35px;
    text-align: center;
    color: #666;
    font-size: 12px;
    letter-spacing: 3px;
}

@keyframes fade {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@media(max-width:600px) {
    header {
        padding: 18px 4%;
    }

    nav a {
        margin-left: 7px;
        font-size: 9px;
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

    <a href="#about" class="btn">
        ENTER MY WORLD
    </a>

</div>

<section id="about">

    <h2>WHO AM I?</h2>

    <div class="line"></div>

    <p>
        I am not here to impress anyone.
        I am here to build something meaningful.
        My journey is private, my ambitions are big,
        and my silence has a purpose.
    </p>

</section>

<section class="dark" id="mindset">

    <h2>THE MINDSET</h2>

    <div class="line"></div>

    <p class="quote" id="quote">
        "You can change what you do,
        but you can't change what you want."
    </p>

    <button class="btn" onclick="changeQuote()">
        NEXT QUOTE
    </button>

</section>

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

<section class="dark">

    <h2>ONE LAST THING</h2>

    <div class="line"></div>

    <button class="btn" onclick="revealMessage()">
        DISCOVER
    </button>

    <p class="hidden-message" id="secret">
        "The world belongs to those
        who have the courage to create their own path."
    </p>

</section>

<footer>

    © 2026 SHELBY.

    <br><br>

    BY ORDER OF THE PEAKY BLINDERS.

</footer>

<script>

const quotes = [
    '"You can change what you do, but you can’t change what you want."',
    '"Sometimes silence is the best answer."',
    '"Fear is not an option. Discipline is."',
    '"A man must make his own future."',
    '"Think quietly. Act wisely. Move forward."'
];

let index = 0;

function changeQuote() {

    index++;

    if(index >= quotes.length) {
        index = 0;
    }

    document.getElementById("quote").innerText = quotes[index];

}

function revealMessage() {

    document.getElementById("secret").style.display = "block";

}

console.log("Welcome to Shelby's world.");

</script>

</body>
</html>
