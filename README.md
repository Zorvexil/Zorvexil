
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ZORVEXIL — Aymen Khaddar</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap');

:root {
    --bg: #080809;
    --panel: #101012;
    --red: #e63946;
    --white: #f5f5f5;
    --muted: #77777f;
    --border: #242428;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: var(--bg);
    color: var(--white);
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
}

/* BACKGROUND */

body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    background-image:
        linear-gradient(#ffffff08 1px, transparent 1px),
        linear-gradient(90deg, #ffffff08 1px, transparent 1px);
    background-size: 45px 45px;
    mask-image: linear-gradient(to bottom, black, transparent 85%);
}

.glow {
    position: fixed;
    width: 400px;
    height: 400px;
    background: #e6394615;
    filter: blur(120px);
    border-radius: 50%;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    pointer-events: none;
}

/* NAVBAR */

nav {
    max-width: 1150px;
    margin: auto;
    padding: 30px 25px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid var(--border);
    position: relative;
    z-index: 2;
}

.logo {
    font-family: 'Space Mono', monospace;
    font-size: 20px;
    font-weight: bold;
    letter-spacing: 3px;
}

.logo span {
    color: var(--red);
}

.nav-label {
    font-family: 'Space Mono', monospace;
    color: var(--muted);
    font-size: 11px;
}

/* MAIN */

.container {
    max-width: 950px;
    margin: 100px auto;
    padding: 0 25px;
    position: relative;
    z-index: 1;
    animation: appear 1s ease;
}

@keyframes appear {
    from {
        opacity: 0;
        transform: translateY(25px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.label {
    color: var(--red);
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    letter-spacing: 3px;
    margin-bottom: 25px;
}

h1 {
    font-size: clamp(48px, 9vw, 100px);
    line-height: .95;
    letter-spacing: -6px;
    font-weight: 700;
}

h1 span {
    color: transparent;
    -webkit-text-stroke: 1px #777;
}

.subtitle {
    color: var(--muted);
    font-size: 16px;
    margin-top: 25px;
    line-height: 1.8;
    max-width: 520px;
}

/* PROFILE CARD */

.profile-card {
    margin-top: 65px;
    background: linear-gradient(135deg, #141416, #0d0d0f);
    border: 1px solid var(--border);
    padding: 30px;
    border-radius: 12px;
    position: relative;
    overflow: hidden;
}

.profile-card::after {
    content: "";
    position: absolute;
    width: 180px;
    height: 180px;
    background: #e6394610;
    filter: blur(70px);
    right: -50px;
    top: -50px;
}

.card-top {
    display: flex;
    align-items: center;
    gap: 22px;
}

.avatar {
    width: 75px;
    height: 75px;
    background: #1b1012;
    border: 1px solid #e6394660;
    display: grid;
    place-items: center;
    border-radius: 10px;
    font-size: 27px;
    font-weight: bold;
    color: var(--red);
}

.name {
    font-size: 23px;
    font-weight: 600;
}

.handle {
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    margin-top: 7px;
}

.description {
    color: #aaa;
    line-height: 1.9;
    font-size: 14px;
    margin-top: 25px;
    max-width: 650px;
}

/* SECTION */

.section {
    margin-top: 65px;
}

.section-heading {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-bottom: 25px;
}

.section-heading h2 {
    font-size: 13px;
    letter-spacing: 3px;
    font-family: 'Space Mono', monospace;
}

.section-heading span {
    color: var(--red);
}

.section-heading::after {
    content: "";
    flex: 1;
    height: 1px;
    background: var(--border);
}

/* SKILLS */

.skills {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
}

.skill {
    padding: 12px 17px;
    border: 1px solid var(--border);
    border-radius: 5px;
    color: #bbb;
    background: #111113;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    transition: .3s;
}

.skill:hover {
    border-color: var(--red);
    color: white;
    transform: translateY(-4px);
}

/* TERMINAL */

.terminal {
    background: #0c0c0e;
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
}

.terminal-header {
    padding: 13px 18px;
    border-bottom: 1px solid var(--border);
    display: flex;
    gap: 7px;
    align-items: center;
}

.dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: #444;
}

.dot:first-child { background: #e05252; }
.dot:nth-child(2) { background: #d5a74a; }
.dot:nth-child(3) { background: #6ba77b; }

.terminal-content {
    padding: 22px;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    line-height: 2.2;
    color: #aaa;
}

.terminal-content .command {
    color: var(--red);
}

.terminal-content .success {
    color: #8bcf9b;
}

/* CONTACT */

.contact {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    flex-wrap: wrap;
    padding: 22px;
    border: 1px solid var(--border);
    border-radius: 8px;
    background: #101012;
}

.contact small {
    display: block;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    margin-bottom: 8px;
}

.discord {
    font-size: 15px;
    font-weight: 600;
}

.discord span {
    color: var(--red);
}

.footer {
    text-align: center;
    color: #555;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    margin-top: 100px;
    padding-bottom: 30px;
    letter-spacing: 2px;
}

@media(max-width: 600px) {
    .container {
        margin-top: 75px;
    }

    h1 {
        letter-spacing: -3px;
    }

    .profile-card {
        padding: 22px;
    }

    .nav-label {
        font-size: 9px;
    }
}
</style>
</head>

<body>

<div class="glow"></div>

<nav>
    <div class="logo">ZORVE<span>XIL.</span></div>
    <div class="nav-label">PERSONAL IDENTITY / 2026</div>
</nav>

<main class="container">

    <div class="label">// INDEPENDENT DEVELOPER</div>

    <h1>AYMEN<br><span>KHADDAR.</span></h1>

    <p class="subtitle">
        Exploring systems, writing code, and building
        things with curiosity. Interested in the
        open-source world and the technology behind it.
    </p>

    <div class="profile-card">

        <div class="card-top">
            <div class="avatar">AK</div>

            <div>
                <div class="name">Aymen Khaddar</div>
                <div class="handle">@Mimoun / Zorvexil</div>
            </div>
        </div>

        <p class="description">
            A programmer and Linux enthusiast focused on
            C programming, system development, networking,
            and cybersecurity. Passionate about open-source
            software and understanding how technology works
            beneath the surface.
        </p>

    </div>

    <section class="section">

        <div class="section-heading">
            <h2><span>01 /</span> INTERESTS</h2>
        </div>

        <div class="skills">
            <div class="skill">C PROGRAMMING</div>
            <div class="skill">LINUX</div>
            <div class="skill">CYBERSECURITY</div>
            <div class="skill">OPEN SOURCE</div>
            <div class="skill">NETWORKING</div>
            <div class="skill">SYSTEMS</div>
            <div class="skill">LOW-LEVEL</div>
        </div>

    </section>

    <section class="section">

        <div class="section-heading">
            <h2><span>02 /</span> SYSTEM</h2>
        </div>

        <div class="terminal">

            <div class="terminal-header">
                <div class="dot"></div>
                <div class="dot"></div>
                <div class="dot"></div>
            </div>

            <div class="terminal-content">
                <div><span class="command">$</span> whoami</div>
                <div>aymen-khaddar</div>

                <div><span class="command">$</span> interests --list</div>
                <div>C / Linux / Open Source / Security</div>

                <div><span class="command">$</span> current_status</div>
                <div class="success">Learning. Building. Exploring.</div>

                <div><span class="command">$</span> _</div>
            </div>

        </div>

    </section>

    <section class="section">

        <div class="section-heading">
            <h2><span>03 /</span> CONTACT</h2>
        </div>

        <div class="contact">
            <div>
                <small>DISCORD</small>
                <div class="discord">
                    <span>@</span>Zorvexill
                </div>
            </div>

            <div>
                <small>IDENTITY</small>
                <div class="discord">ZORVEXIL</div>
            </div>
        </div>

    </section>

    <footer class="footer">
        DESIGNED BY CURIOSITY · ZORVEXIL © 2026
    </footer>

</main>

</body>
</html>
