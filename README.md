<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday ❤️</title>


<style>

/* =========================================
   CUSTOMIZE EVERYTHING HERE
========================================= */

:root{
--primary:#ff6fa5;
--secondary:#ffd6e7;
--text:#ffffff;
--card:#ffffffdd;
}

constName{}

/* Replace these with your content */
body{
--friend-name:"MAAHHH BABBBYY";
}

/* ========================================= */

*{
margin:0;
padding:0;
box-sizing:border-box;
}

html,body{
width:100%;
height:100%;
overflow:hidden;
font-family:'Poppins',sans-serif;
}

body{
background:linear-gradient(
135deg,
#ff9ec4,
#ffcce0,
#ffdff0
);
}

.page{
position:absolute;
width:100%;
height:100%;
display:none;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
padding:20px;
animation:fadeIn 1s;
}

.page.active{
display:flex;
}

h1,h2{
color:white;
}

button{
border:none;
padding:14px 28px;
border-radius:50px;
font-size:17px;
cursor:pointer;
background:white;
color:#ff4f8f;
font-weight:600;
margin-top:20px;
box-shadow:0 5px 15px rgba(0,0,0,.15);
}

button:hover{
transform:scale(1.05);
}

.title{
font-family:'Pacifico',cursive;
font-size:3.5rem;
animation:glow 2s infinite alternate;
}

.friend{
font-size:2rem;
margin-top:10px;
}

.hearts{
position:absolute;
width:100%;
height:100%;
overflow:hidden;
pointer-events:none;
}

.heart{
position:absolute;
bottom:-20px;
font-size:25px;
animation:floatUp linear infinite;
}

.cake{
margin-top:30px;
}

.candles{
display:flex;
justify-content:center;
gap:35px;
margin-bottom:5px;
}

.flame{
width:18px;
height:35px;
background:orange;
border-radius:50%;
animation:flicker .2s infinite;
}

.cakeBody{
width:220px;
height:120px;
background:#ff7eb3;
border-radius:15px;
position:relative;
}

.cakeBody::before{
content:"";
position:absolute;
top:20px;
left:0;
width:100%;
height:10px;
background:white;
}

.gallery{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:15px;
max-width:600px;
}

.gallery img{
width:100%;
height:180px;
object-fit:cover;
border-radius:20px;
box-shadow:0 5px 15px rgba(0,0,0,.2);
}

.note{
background:var(--card);
padding:25px;
border-radius:20px;
max-width:700px;
color:#444;
font-size:18px;
line-height:1.8;
}

.finalCard{
background:white;
padding:30px;
border-radius:25px;
max-width:700px;
}

.finalCard h2{
color:#ff4f8f;
}

.finalCard p{
margin-top:15px;
color:#444;
line-height:1.8;
}

.musicBtn{
position:fixed;
top:15px;
right:15px;
z-index:1000;
}

@keyframes glow{
from{
text-shadow:0 0 10px white;
}
to{
text-shadow:0 0 35px hotpink;
}
}

@keyframes fadeIn{
from{
opacity:0;
transform:translateY(30px);
}
to{
opacity:1;
transform:translateY(0);
}
}

@keyframes flicker{
50%{
transform:scale(.85);
}
}

@keyframes floatUp{
0%{
transform:translateY(0);
opacity:1;
}
100%{
transform:translateY(-120vh);
opacity:0;
}
}

@media(max-width:700px){

.title{
font-size:2.5rem;
}

.gallery{
grid-template-columns:1fr 1fr;
}

.gallery img{
height:130px;
}

.note{
font-size:16px;
}

}

</style>
</head>

<body>

<div class="hearts" id="hearts"></div>

<button class="musicBtn" onclick="toggleMusic()">
🎵 Music
</button>

<audio id="music" loop>
<source src="Github song final.mpeg" type="audio/mpeg">
</audio>

<!-- PAGE 1 -->

<section class="page active" id="page1">

<h1 class="title">
Happy Birthday 🎉
</h1>

<h2 class="friend" id="TRINISHA">
MAAAHHH BABBYY ❤️
</h2>

<button onclick="startBirthday()">
Start Celebration ✨
</button>

</section>

<!-- PAGE 2 -->

<section class="page" id="page2">

<h1>Make A Wish 🌟</h1>

<div class="cake">

<div class="candles">
<div class="flame"></div>
<div class="flame"></div>
<div class="flame"></div>
</div>

<div class="cakeBody"></div>

</div>

<p style="color:white;margin-top:20px;">
Blow into your microphone 🎤
</p>

<button onclick="blowCandles()">
Blow Candles 🎂
</button>

</section>

<!-- PAGE 3 -->

<section class="page" id="page3">

<h1>MAAAHH CUTTIEPIEE 📸</h1>

<br>

<div class="gallery">

<img src="Photo 2.jpeg">
<img src="HG photo 1.jpeg">
<img src="Photo5.jpeg">
<img src="Photo6.jpeg">

</div>

<button onclick="showPage(4)">
Next ❤️
</button>

</section>

<!-- PAGE 4 -->

<section class="page" id="page4">

<div class="note">

<h2 style="color:#ff4f8f">
Birthday Letter 💌
</h2>

<br>

<p>

Dear BABBYYY(HG)

Happy Birthday to the most special person from my childhood.
Growing up with you is one of the best part of my life From silly conversations to bestest teas and all the memories we made together Every moment still means a lot to me.
No matter how much we grow up or how busy life gets You will always be my most important person i never forget.
Thanks for being there for me and you are the one who supported me a lot, gave me emotional support when i need someone the most.
Am really lucky to have the bestest friend like you.
I just hope this year brings you success,happiness,peace and everything your heart wishes for cuz you truely deserve it all.
Enjoy your day fully,smile a lot(MY CUTTIE PIE)
And Yeah.... Don't forget to send me snaps and fitchecks ❤️ And once again HAPPIEST BIRTHDAY TO YOU.❤️

</p>

<button onclick="showPage(5)">
Final Surprise 🎁
</button>

</div>

</section>

<!-- PAGE 5 -->

<section class="page" id="page5">

<div class="finalCard">

<h2>
Forever Best Friends MAHHHH BABBYYY 💕
</h2>

<p>

This is your fully customizable page.

Add anything here:


✨ Fireworks

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Promise Reveal</title>

<style>
body{
    font-family: Arial, sans-serif;
    text-align:center;
    margin-top:100px;
}

#promise{
    display:none;
    font-size:22px;
    margin-top:20px;
    animation: fadeIn 1s ease;
}

#fireworks{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    pointer-events:none;
}

@keyframes fadeIn{
    from{opacity:0;}
    to{opacity:1;}
}
</style>
</head>
<body>

<button onclick="revealPromise()">Reveal Promise 💖</button>

<div id="promise">
    No matter where life takes us, I promise to always cherish our friendship and support you through every chapter of life.
</div>

<canvas id="fireworks"></canvas>

<script src="https://cdn.jsdelivr.net/npm/fireworks-js@2.10.8/dist/index.umd.js"></script>

<script>
const container = document.getElementById('fireworks');

const fireworks = new Fireworks.default(container, {
    particles: 100,
    trace: 3,
    explosion: 6
});

function revealPromise() {
    document.getElementById('promise').style.display = 'block';

    fireworks.start();

    setTimeout(() => {
        fireworks.stop();
    }, 8000);
}
</script>

✨ Future promises

<section id="future-promise">
    <h2>💖 Dear Best Friend,

We've known each other since childhood, and through all these years you've been one of the most important people in my life.
We've shared laughter, memories, silly moments, and countless stories that I'll always treasure.

On your special day, I want to make a simple promise to you.
I promise that no matter where life takes us, I'll always value our friendship.
I promise to support you in your dreams, celebrate your successes, and stand by you during difficult times.
Even if distance, busy schedules, or time try to get in the way, our friendship will always have a special place in my heart.

Thank you for being such an amazing friend and for making my childhood and life so much brighter.
I hope your future is filled with happiness, success, good health, and endless reasons to smile.

Happy Birthday, my bestest Friend.

With lots of love and respect,
Your Childhood Best Friend (SIR JII) ❤️</h2>

    <div class="promise-card">
        <p id="customPromise"></p>
    </div>
</section>



✨ Love and friendship quotes

<div style="
    max-width:700px;
    margin:30px auto;
    padding:25px;
    background:#fff0f5;
    border-radius:20px;
    box-shadow:0 4px 15px rgba(0,0,0,0.1);
    text-align:center;
    font-family:Arial, sans-serif;
">
    <h2>❤️ A Special Quote For Mahhh BABBY ❤️</h2>

    <p style="font-size:20px; line-height:1.8;">
    "I think my favorite notification is one from you. ✨"
    </p>

    <p style="font-size:18px;">
        ✨ With lots of appreciation and best wishes ✨
    </p>
</div>

<h2>✨ Anything You Want ✨</h2>
<section class="gifts">
    <h2>🎁 Choose Your Gift 🎁</h2>

    <div class="gift-gallery">
        <img src="Gift 1.jpg" alt="Gift 1">
        <img src="Gift 2.jpg" alt="Gift 2">
        <img src="Gift 3.jpg" alt="Gift 3">
        <img src="Gift 4.jpg" alt="Gift 4">
    </div>
</section>

</div>

</section>

<script>

document.getElementById("TRINISHA(MADAM JIII)").innerText =
"BABBYYY(HG) ❤️";

function showPage(number){

document.querySelectorAll(".page")
.forEach(page=>page.classList.remove("active"));

document.getElementById(
"page"+number
).classList.add("active");

}

function startBirthday(){

showPage(2);

document.getElementById("music")
.play();

startMicDetection();

}

function blowCandles(){

document.querySelectorAll(".flame")
.forEach(flame=>{

flame.style.opacity="0";

});

setTimeout(()=>{

showPage(3);

},1500);

}

function toggleMusic(){

const music =
document. Github song final.mpeg("music");

if(music.paused){

music.play();

}
else{

music.pause();

}

}

function startMicDetection(){

navigator.mediaDevices
.getUserMedia({audio:true})

.then(stream=>{

const audioContext =
new AudioContext();

const analyser =
audioContext.createAnalyser();

const microphone =
audioContext.createMediaStreamSource(stream);

microphone.connect(analyser);

const data =
new Uint8Array(
analyser.frequencyBinCount
);

function detect(){

analyser.getByteFrequencyData(data);

let volume =
data.reduce((a,b)=>a+b,0)
/
data.length;

if(volume > 55){

blowCandles();

return;

}

requestAnimationFrame(detect);

}

detect();

})

.catch(err=>{

console.log(err);

});

}

/* Floating Hearts */

const hearts =
document.getElementById("hearts");

setInterval(()=>{

const heart =
document.createElement("div");

heart.className="heart";

heart.innerHTML=
["💖","💕","💗","💞","🌸"]
[Math.floor(Math.random()*5)];

heart.style.left=
Math.random()*100+"%";

heart.style.animationDuration=
(4+Math.random()*4)+"s";

hearts.appendChild(heart);

setTimeout(()=>{

heart.remove();

},8000);

},400);

</script>

</body>
</html># index....html
