<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Sameer ❤️ Zeenu</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

body {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #2b002b, #ff5f9e);
    color: white;
    overflow-x: hidden;
}

/* Heart Cursor */
body {
    cursor: url('https://cur.cursors-4u.net/nature/nat-2/nat143.cur'), auto;
}

/* Floating Roses */
.rose {
    position: fixed;
    top: 110%;
    color: #ffb3c1;
    font-size: 24px;
    animation: floatUp linear infinite;
    opacity: 0.9;
}
@keyframes floatUp {
    from { transform: translateY(0); }
    to { transform: translateY(-150vh); }
}

/* Hero */
.hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}
.hero h1 {
    font-size: 55px;
    animation: fadeIn 2s;
}
.hero h3 {
    opacity: 0.8;
    font-size: 20px;
    animation: fadeIn 3s;
}
@keyframes fadeIn {
    from {opacity:0;}
    to {opacity:1;}
}

/* Scroll Animations */
section {
    opacity: 0;
    transform: translateY(50px);
    transition: 1.2s;
}
section.visible {
    opacity: 1;
    transform: translateY(0);
}

/* Glass Cards */
.card {
    width: 90%;
    max-width: 720px;
    margin: 40px auto;
    padding: 25px;
    border-radius: 18px;
    background: rgba(255, 255, 255, 0.17);
    backdrop-filter: blur(12px);
    text-align: center;
}

/* Buttons */
.btn {
    background: #ff306c;
    padding: 14px 30px;
    border: none;
    color: white;
    font-size: 20px;
    border-radius: 10px;
    margin-top: 25px;
    cursor: pointer;
    transition: 0.3s;
}
.btn:hover {
    background: #ffd1e8;
    color: black;
}

/* Love Letter Box */
.letter {
    border: 2px dashed #ffc7d9;
    padding: 25px;
    border-radius: 15px;
    animation: fadeIn 2s;
}
.letter h2 {
    color: #ffdedf;
}

/* Final Proposal Page */
#proposalPage {
    display: none;
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.92);
    color: white;
    z-index: 999;
    text-align: center;
    padding-top: 150px;
}

#proposalPage h1 {
    font-size: 48px;
    animation: fadeIn 2s;
}

#proposalPage button {
    padding: 15px 35px;
    font-size: 22px;
    margin-top: 40px;
    border-radius: 12px;
    border: none;
    cursor: pointer;
    background: #ff4081;
    color: white;
}

/* Fireworks */
.firework {
    position: fixed;
    bottom: 0;
    width: 5px;
    height: 5px;
    background: transparent;
    border-radius: 50%;
    animation: explode 1s forwards;
}
@keyframes explode {
    0% {transform: translateY(0);}
    100% {transform: translateY(-300px);}
}

/* Signature */
.signature {
    text-align: center;
    margin-top: 50px;
    font-size: 18px;
    opacity: 0.7;
}
</style>
</head>
<body>

<!-- Background music -->
<audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2023/03/07/audio_8f9d2b3c26.mp3?filename=romantic-soft-melody-140316.mp3" type="audio/mp3">
</audio>

<!-- Falling Roses -->
<script>
setInterval(() => {
    let rose = document.createElement('div');
    rose.innerHTML = "🌹";
    rose.classList.add('rose');
    rose.style.left = Math.random() * 100 + "vw";
    rose.style.animationDuration = (4 + Math.random() * 4) + "s";
    document.body.appendChild(rose);
    setTimeout(() => rose.remove(), 9000);
}, 350);
</script>

<!-- HERO -->
<div class="hero">
    <h1>Sameer ❤️ Zeenu</h1>
    <h3>You are my beginning, my ending, my everything.</h3>
</div>

<!-- SECTION 1 -->
<section class="card">
    <h2>My Love, Zeenu ❤️</h2>
    <p>
        Sameer knows you’re angry…  
        and he understands.  
        But he also knows he cannot imagine his life without you.
    </p>
</section>

<!-- SECTION 2 -->
<section class="card">
    <h2>I Miss You</h2>
    <p>
        I miss your voice,  
        I miss your smile,  
        I miss your drama,  
        I miss your love…  
        I miss *you*, Zeenu.  
    </p>
</section>

<!-- SECTION 3 -->
<section class="card letter">
    <h2>A Letter From Sameer 💌</h2>
    <p>
        “I don’t care about ego.  
        I don’t care about arguments.  
        I only care about you.  
        Please stay with me forever, Zeenu.”
    </p>
</section>

<!-- SECTION 4 -->
<section class="card">
    <h2>Before You Go… 💗</h2>
    <p>Sameer has one last, most important question.</p>
    <button class="btn" onclick="showProposal()">Open ❤️</button>
</section>

<!-- FINAL PROPOSAL PAGE -->
<div id="proposalPage">
    <h1>💍 Zeenu… Will You Marry Sameer? 💖</h1>
    <button onclick="celebrate()">Yes, Forever ❤️</button>
</div>

<script>
function showProposal() {
    document.getElementById("proposalPage").style.display = "block";
}

function celebrate() {
    for (let i = 0; i < 30; i++) {
        let f = document.createElement("div");
        f.classList.add("firework");
        f.style.left = Math.random() * 100 + "vw";
        f.style.background = "hsl(" + Math.random()*360 + ",100%,50%)";
        document.body.appendChild(f);
        setTimeout(() => f.remove(), 1000);
    }
    alert("Sameer is the happiest person right now ❤️💍");
}

// Scroll animation
window.addEventListener("scroll", () => {
    document.querySelectorAll("section").forEach(sec => {
        let top = sec.getBoundingClientRect().top;
        if (top < window.innerHeight - 100) sec.classList.add("visible");
    });
});
</script>

<!-- SIGNATURE -->
<div class="signature">
    Made with ❤️ by Sameer for his only love, Zeenu.
</div>

</body>
</html>
