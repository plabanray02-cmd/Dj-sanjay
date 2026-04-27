# Dj-sanjay  
<!DOCTYPE html>
<html lang="en">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DJ Sanjay | Premium DJ</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins;}

body{
background:#050505;
color:white;
overflow-x:hidden;
}

/* 🔥 Loader */
#loader{
position:fixed;
width:100%;
height:100%;
background:black;
display:flex;
justify-content:center;
align-items:center;
z-index:9999;
}
.circle{
width:50px;
height:50px;
border:5px solid #1e90ff;
border-top:5px solid transparent;
border-radius:50%;
animation:spin 1s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg);}}

/* 🔥 Progress Bar */
#progress{
position:fixed;
top:0;
left:0;
height:4px;
background:#1e90ff;
width:0%;
z-index:999;
}

/* 🌈 Animated Background */
body::before{
content:"";
position:fixed;
width:200%;
height:200%;
background:linear-gradient(45deg,#0f0c29,#302b63,#24243e,#1e90ff);
background-size:400% 400%;
animation:gradientMove 12s ease infinite;
z-index:-1;
}
@keyframes gradientMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

/* Header */
header{
padding:90px 20px;
text-align:center;
animation:fadeIn 2s ease;
}
header h1{
font-size:42px;
text-shadow:0 0 25px #1e90ff;
}
header p{opacity:0.8;margin:10px 0;}

/* Buttons */
.btn{
display:inline-block;
padding:12px 28px;
margin:10px;
border-radius:30px;
border:2px solid #1e90ff;
color:#1e90ff;
text-decoration:none;
transition:0.3s;
}
.btn:hover{
background:#1e90ff;
color:white;
box-shadow:0 0 20px #1e90ff;
transform:translateY(-3px);
}

/* Section */
.section{
padding:60px 20px;
text-align:center;
opacity:0;
transform:translateY(60px);
transition:1s;
}
.section.show{
opacity:1;
transform:translateY(0);
}

/* Cards */
.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
gap:20px;
}
.card{
padding:25px;
border-radius:15px;
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(10px);
transition:0.4s;
}
.card:hover{
transform:translateY(-10px) scale(1.05);
box-shadow:0 0 25px #1e90ff;
}

/* Gallery */
.gallery img{
width:100%;
border-radius:12px;
margin:10px 0;
transition:0.5s;
}
.gallery img:hover{
transform:scale(1.05);
box-shadow:0 0 20px #1e90ff;
}

/* Form */
form input, form textarea{
width:90%;
margin:10px;
padding:12px;
border:none;
border-radius:10px;
}
button{
padding:12px 30px;
background:#1e90ff;
border:none;
color:white;
border-radius:25px;
}

/* Footer */
footer{
padding:20px;
text-align:center;
opacity:0.6;
}

/* WhatsApp */
.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
padding:15px;
border-radius:50%;
box-shadow:0 0 15px #25D366;
}

/* Animation */
@keyframes fadeIn{
from{opacity:0;transform:translateY(-30px);}
to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body>

<!-- Loader -->
<div id="loader"><div class="circle"></div></div>

<!-- Progress -->
<div id="progress"></div>

<header>
<h1>DJ SANJAY</h1>
<p>Premium Sound • Light • Event Setup</p>
<a class="btn" href="tel:919832084397">📞 Call</a>
<a class="btn" href="https://wa.me/919832084397">💬 WhatsApp</a>
</header>

<div class="section">
<h2>🔥 Services</h2>
<div class="services">
<div class="card">🎧 DJ Setup</div>
<div class="card">🔊 Sound System</div>
<div class="card">💡 DJ Lights</div>
<div class="card">🎤 Stage Setup</div>
<div class="card">🎉 Wedding</div>
<div class="card">🎂 Birthday</div>
</div>
</div>

<div class="section gallery">
<h2>📸 Gallery</h2>
<img src="https://images.unsplash.com/photo-1507874457470-272b3c8d8ee2">
<img src="https://images.unsplash.com/photo-1492684223066-81342ee5ff30">
<img src="https://images.unsplash.com/photo-1514525253161-7a46d19cd819">
</div>

<div class="section">
<h2>📅 Book Now</h2>
<form>
<input type="text" placeholder="Name" required><br>
<input type="tel" placeholder="Phone" required><br>
<textarea placeholder="Event Details"></textarea><br>
<button>Submit</button>
</form>
</div>

<div class="section">
<h2>⭐ Why Choose Us</h2>
<p>✔ High Bass Sound</p>
<p>✔ Premium Lighting</p>
<p>✔ Affordable Price</p>
<p>✔ Fast Service</p>
</div>

<footer>
<p>© 2026 DJ Sanjay</p>
</footer>

<a class="whatsapp" href="https://wa.me/919832084397">💬</a>

<script>
// Loader
window.onload = () => {
document.getElementById("loader").style.display="none";
};

// Scroll animation
const sections=document.querySelectorAll('.section');
window.addEventListener('scroll',()=>{
sections.forEach(sec=>{
if(sec.getBoundingClientRect().top < window.innerHeight-100){
sec.classList.add('show');
}
});
});

// Progress bar
window.addEventListener("scroll",()=>{
let scrollTop=document.documentElement.scrollTop;
let height=document.documentElement.scrollHeight - document.documentElement.clientHeight;
let scrolled=(scrollTop/height)*100;
document.getElementById("progress").style.width=scrolled+"%";
});
</script>

</body>
</html>
