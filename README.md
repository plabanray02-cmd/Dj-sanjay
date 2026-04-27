# Dj-sanjay  
<!DOCTYPE html>
<html lang="en">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DJ Sanjay | Premium DJ</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins;}
body{background:#0a0a0a;color:#fff;}

header{
background:linear-gradient(135deg,#000,#1e90ff);
padding:70px 20px;
text-align:center;
}

header h1{font-size:35px;}
header p{opacity:0.8;margin:10px 0;}

.btn{
display:inline-block;
margin:10px;
padding:12px 25px;
background:#1e90ff;
color:white;
border-radius:30px;
text-decoration:none;
}

.section{padding:40px 20px;text-align:center;}

.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
gap:15px;
}

.card{
background:#111;
padding:20px;
border-radius:15px;
transition:0.3s;
}

.card:hover{
transform:scale(1.08);
background:#1e90ff;
}

.gallery img{
width:100%;
border-radius:10px;
margin:10px 0;
}

form input, form textarea{
width:90%;
margin:10px;
padding:12px;
border:none;
border-radius:10px;
}

form button{
padding:12px 30px;
border:none;
background:#1e90ff;
color:white;
border-radius:25px;
}

iframe{
width:100%;
height:250px;
border-radius:10px;
margin-top:15px;
}

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
padding:15px;
border-radius:50%;
font-size:20px;
}
</style>
</head>

<body>

<header>
<h1>DJ SANJAY</h1>
<p>Premium Sound • Light • DJ Setup</p>

<a class="btn" href="tel:919832084397">📞 Call</a>
<a class="btn" href="https://wa.me/919832084397">💬 WhatsApp</a>
</header>

<div class="section">
<h2>🔥 Services</h2>
<div class="services">
<div class="card">🎧 DJ Setup</div>
<div class="card">🔊 Sound Box</div>
<div class="card">💡 DJ Light</div>
<div class="card">🎤 Stage Setup</div>
<div class="card">🎉 Wedding</div>
<div class="card">🎂 Birthday</div>
</div>
</div>

<div class="section">
<h2>🎬 Event Video</h2>
<video width="100%" controls autoplay muted loop>
<source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
</video>
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
<input type="text" placeholder="Your Name" required><br>
<input type="tel" placeholder="Phone Number" required><br>
<textarea placeholder="Event Details"></textarea><br>
<button type="submit">Submit</button>
</form>
</div>

<div class="section">
<h2>📍 Location</h2>
<iframe src="https://maps.google.com/maps?q=Alipurduar&t=&z=13&ie=UTF8&iwloc=&output=embed"></iframe>
</div>

<div class="section">
<h2>⭐ Why Choose Us</h2>
<p>✔ High Bass Sound</p>
<p>✔ Premium Lights</p>
<p>✔ Affordable Price</p>
<p>✔ Fast Service</p>
</div>

<a class="whatsapp" href="https://wa.me/919832084397">💬</a>

</body>
</html>
