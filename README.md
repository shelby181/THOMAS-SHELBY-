<!DOCTYPE html>
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
    animation
