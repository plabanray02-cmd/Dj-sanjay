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

/* Animated Gradient Background */
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
letter-spacing:2px;
text-shadow:0 0 25px #1e90ff;
}

header p{
opacity:0.8;
margin:10px 0 20px;
}

/* Buttons */
.btn{
display:inline-block;
padding:12px 28px;
margin:10px;
border-radius:30px;
background:transparent;
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

/* Sections */
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

/* Service Cards */
.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
gap:20px;
margin-top:20px;
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
border-color:#1e90ff;
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

/* Why section */
.why p{
margin:8px 0;
}

/* Footer */
footer{
padding:20px;
text-align:center;
opacity:0.6;
}

/* WhatsApp floating */
.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
padding:15px;
border-radius:50%;
font-size:20px;
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

<header>
<h1>DJ SANJAY</h1>
<p>Premium Sound • Light • Event Setup</p>

<a class="btn" href="tel:919832084397">📞 Call Now</a>
<a class="btn" href="https://wa.me/919832084397">💬 WhatsApp</a>
</header>

<div class="section">
<h2>🔥 Our Services</h2>
<div class="services">
<div class="card">🎧 DJ Setup</div>
<div class="card">🔊 Sound System</div>
<div class="card">💡 DJ Lights</div>
<div class="card">🎤 Stage Setup</div>
<div class="card">🎉 Wedding Events</div>
<div class="card">🎂 Birthday Party</div>
</div>
</div>

<div class="section gallery">
<h2>📸 Gallery</h2>
<img src="https://images.unsplash.com/photo-1507874457470-272b3c8d8ee2">
<img src="https://images.unsplash.com/photo-1492684223066-81342ee5ff30">
<img src="https://images.unsplash.com/photo-1514525253161-7a46d19cd819">
</div>

<div class="section why">
<h2>⭐ Why Choose Us</h2>
<p>✔ High Quality Bass Sound</p>
<p>✔ Premium DJ Lighting</p>
<p>✔ Affordable Price</p>
<p>✔ Fast & Reliable Service</p>
</div>

<footer>
<p>© 2026 DJ Sanjay | All Rights Reserved</p>
</footer>

<a class="whatsapp" href="https://wa.me/919832084397">💬</a>

<script>
const sections = document.querySelectorAll('.section');
window.addEventListener('scroll', () => {
sections.forEach(sec => {
const top = sec.getBoundingClientRect().top;
if(top < window.innerHeight - 100){
sec.classList.add('show');
}
});
});
</script>

</body>
</html>
