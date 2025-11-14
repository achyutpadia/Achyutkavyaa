<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Anniversary, Kavyaa 💗</title>

<style>
/* PASTEL GRADIENT BACKGROUND */
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffd9fb, #ffeaff, #fce4ff);
    background-size: 400% 400%;
    animation: gradientShift 12s ease infinite;
    scroll-behavior: smooth;
    overflow-x: hidden;
    cursor: none;
}

@keyframes gradientShift {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
}

/* SECTION FADE-IN */
section {
    padding: 80px 20px;
    text-align: center;
    opacity: 0;
    animation: fadeIn 1.4s ease forwards;
}
@keyframes fadeIn {
    from {opacity: 0; transform: translateY(40px);}
    to {opacity: 1; transform: translateY(0);}
}

/* HEADINGS WITH SHINE EFFECT */
h1, h2 {
    color: #ff62c7;
    animation: shine 2.5s infinite;
}
@keyframes shine {
    0% { text-shadow: 0 0 10px #ff9ce6; }
    50% { text-shadow: 0 0 25px #ffbdf2; }
    100% { text-shadow: 0 0 10px #ff9ce6; }
}

/* TEXT */
p {
    color: #5a4a57;
    font-size: 18px;
    line-height: 1.7;
}

/* BUTTONS */
.btn{
    display:inline-block;
    padding:12px 25px;
    background:#ff9ce6;
    color:white;
    border-radius:30px;
    text-decoration:none;
    font-weight:600;
    margin-top:20px;
    animation:bounce 2s infinite;
}
@keyframes bounce {
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-7px);}
}
.btn:hover { background:#ff77da; transform:scale(1.06); }

/* GALLERY */
.gallery img {
    width:80%;
    max-width:330px;
    border-radius:20px;
    margin:15px 0;
    box-shadow:0 5px 15px rgba(255,150,200,0.4);
}

/* SURPRISE TEXT */
.surprise {
    font-size:22px;
    color:#ff6bd6;
    animation:blink 1.3s infinite;
}
@keyframes blink {
    0%{opacity:1;}
    50%{opacity:0.4;}
    100%{opacity:1;}
}

/* FLOATING PETALS */
.petal {
    position: fixed;
    top: -10px;
    animation: fall 6s linear infinite;
    opacity: 0.8;
    font-size: 18px;
}
@keyframes fall {
    0% { transform: translateY(0) rotate(0deg); }
    100% { transform: translateY(120vh) rotate(360deg); }
}

/* CURSOR GLITTER */
.cursor {
    position: fixed;
    width: 12px;
    height: 12px;
    background: #ff8de6;
    border-radius: 50%;
    pointer-events: none;
    box-shadow: 0 0 15px #ffbdf2;
    transform: translate(-50%, -50%);
}
</style>
</head>

<body>

<!-- GLITTER CURSOR -->
<div class="cursor" id="cursor"></div>

<script>
document.addEventListener("mousemove", function(e){
    let cursor = document.getElementById("cursor");
    cursor.style.left = e.clientX + "px";
    cursor.style.top = e.clientY + "px";
});
</script>

<!-- FALLING PETALS -->
<script>
for(let i=0;i<20;i++){
    let petal = document.createElement("div");
    petal.className = "petal";
    petal.innerHTML = "🌸";
    petal.style.left = Math.random()*100 + "vw";
    petal.style.animationDelay = Math.random()*5 + "s";
    document.body.appendChild(petal);
}
</script>

<!-- MUSIC PLAYER -->
<section>
    <h2>🎵 Our Song</h2>
    <p>Perfect — Ed Sheeran</p>
    <audio id="bgmusic" controls autoplay loop>
        <source src="https://aac.saavncdn.com/569/7e90e1f47cfcb0c7a5c7773bc8c79ee1_320.mp4" type="audio/mp4">
    </audio>
    <p style="font-size:14px;">(If autoplay doesn’t work, press play 💗)</p>
</section>

<!-- HOME -->
<section id="home">
    <h1>💗 Happy Anniversary, Kavyaa 💗</h1>
    <p>4 years of us — and it still feels like magic ✨</p>
    <a class="btn" href="#story">Continue</a>
</section>

<!-- STORY -->
<section id="story">
    <h2>🌈 Our Little Love Story</h2>
    <p>
        Four years of memories, laughs, fights, hugs, peace, chaos and love.  
        You make everything feel like home, Kavyaa.
    </p>
    <a class="btn" href="#photos">Next</a>
</section>

<!-- PHOTOS -->
<section id="photos">
    <h2>📸 Our Memories</h2>
    <p>Add your photos here:</p>
    <div class="gallery">
        <img src="YOUR_IMAGE_1">
        <img src="YOUR_IMAGE_2">
        <img src="YOUR_IMAGE_3">
    </div>
    <a class="btn" href="#letter">Next</a>
</section>

<!-- LETTER -->
<section id="letter">
    <h2>💌 A Letter For You</h2>
    <p>
        Dear Kavyaa,<br><br>
        Thank you for being the softest part of my world.  
        Four years with you feel like a dream I never want to wake up from.  
        You’re my calm, my chaos, my comfort, my happiness.<br><br>
        I choose you — today, tomorrow, forever.  
    </p>
    <a class="btn" href="#secret">Next</a>
</section>

<!-- SECRET PAGE BUTTON -->
<section id="secret">
    <h2>🔐 Secret Page</h2>
    <p>Enter the password to see my final message for you 💗</p>

    <input id="pass" placeholder="Enter Password" style="padding:10px; border-radius:10px;">
    <br><br>
    <button class="btn" onclick="checkPass()">Unlock</button>

    <script>
    function checkPass(){
        let pass = document.getElementById("pass").value;
        if(pass === "kavyaa"){
            window.location.href = "#finalsecret";
        } else {
            alert("Wrong password my love 😭 try again!");
        }
    }
    </script>
</section>

<!-- SECRET MESSAGE -->
<section id="finalsecret">
    <h2>💗 My Secret Message</h2>
    <p style="font-size:24px; color:#ff4fb8;">
        I love you forever 💗
    </p>
</section>

<!-- FINAL -->
<section>
    <h2>🌸 Forever & Always 🌸</h2>
    <p>Here’s to 4 years of love — and forever with you, my love 💗</p>
</section>

</body>
</html>
