# Dj-sanjay  
<!DOCTYPE html>
<html lang="en">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DJ SANJAY | Premium DJ</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins;}
body{background:#050505;color:white;overflow-x:hidden;}

/* Loader */
#loader{position:fixed;width:100%;height:100%;background:black;display:flex;justify-content:center;align-items:center;z-index:9999;}
.circle{width:50px;height:50px;border:5px solid #1e90ff;border-top:5px solid transparent;border-radius:50%;animation:spin 1s linear infinite;}
@keyframes spin{to{transform:rotate(360deg);}}

/* Progress */
#progress{position:fixed;top:0;left:0;height:4px;background:#1e90ff;width:0%;z-index:999;}

/* Background */
body::before{
content:"";
position:fixed;
width:200%;height:200%;
background:linear-gradient(45deg,#0f0c29,#302b63,#1e90ff);
background-size:400% 400%;
animation:bgMove 10s ease infinite;
z-index:-2;
}
@keyframes bgMove{
0%{background-position:0%;}
50%{background-position:100%;}
100%{background-position:0%;}
}

/* Particles canvas */
#particles{position:fixed;top:0;left:0;width:100%;height:100%;z-index:-1;}

/* Cursor */
.cursor{
position:fixed;
width:20px;height:20px;
border-radius:50%;
background:#1e90ff;
pointer-events:none;
transform:translate(-50%,-50%);
box-shadow:0 0 20px #1e90ff;
z-index:9999;
}

/* Header */
header{text-align:center;padding:90px 20px;}
header h1{font-size:42px;text-shadow:0 0 20px #1e90ff;}
.btn{padding:12px 25px;margin:10px;border:2px solid #1e90ff;border-radius:30px;color:#1e90ff;text-decoration:none;transition:0.3s;}
.btn:hover{background:#1e90ff;color:white;box-shadow:0 0 15px #1e90ff;}

/* Section */
.section{
padding:60px 20px;
text-align:center;
opacity:0;
transform:translateY(80px) scale(0.95);
filter:blur(5px);
transition:1s;
}
.section.show{
opacity:1;
transform:translateY(0) scale(1);
filter:blur(0);
}

/* Cards */
.services{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:20px;}
.card{padding:20px;border-radius:12px;background:rgba(255,255,255,0.05);transition:0.3s;}
.card:hover{transform:scale(1.05);box-shadow:0 0 20px #1e90ff;}

/* Form */
form input, form textarea{
width:90%;margin:10px;padding:12px;border-radius:10px;border:none;
background:rgba(255,255,255,0.05);color:white;
transition:0.3s;
}
form input:focus{box-shadow:0 0 15px #1e90ff;transform:scale(1.03);}

/* Button */
button{padding:12px 30px;background:#1e90ff;border:none;color:white;border-radius:25px;}

/* WhatsApp */
.whatsapp{position:fixed;bottom:20px;right:20px;background:#25D366;padding:15px;border-radius:50%;}

/* Footer */
footer{text-align:center;padding:20px;opacity:0.6;}
</style>
</head>

<body>

<div id="loader"><div class="circle"></div></div>
<div id="progress"></div>
<canvas id="particles"></canvas>
<div class="cursor"></div>

<header>
<h1></h1>
<p>Premium Sound • Light • Event Setup</p>
<a class="btn" href="tel:919832084397">Call</a>
<a class="btn" href="https://wa.me/919832084397">WhatsApp</a>
</header>

<div class="section">
<h2>Services</h2>
<div class="services">
<div class="card">DJ Setup</div>
<div class="card">Sound</div>
<div class="card">Lights</div>
<div class="card">Wedding</div>
</div>
</div>

<div class="section">
<h2>Book Now</h2>
<form id="bookingForm">
<input type="text" id="name" placeholder="Name" required>
<input type="tel" id="phone" placeholder="Phone" required>
<input type="date" id="date" required>
<input type="time" id="time" required>
<textarea id="details" placeholder="Event Details"></textarea>
<button type="submit">Book Now</button>
</form>
</div>

<footer>© DJ Sanjay</footer>
<a class="whatsapp" href="https://wa.me/919832084397">💬</a>

<script>
// Loader
window.onload=()=>{document.getElementById("loader").style.display="none";};

// Typing
let text="DJ SANJAY";let i=0;
function type(){if(i<text.length){document.querySelector("h1").innerHTML+=text.charAt(i);i++;setTimeout(type,100);}}
type();

// Scroll
const sections=document.querySelectorAll('.section');
window.addEventListener('scroll',()=>{
sections.forEach(sec=>{
if(sec.getBoundingClientRect().top < window.innerHeight-100){
sec.classList.add('show');
}
});
});

// Progress
window.addEventListener("scroll",()=>{
let s=document.documentElement.scrollTop;
let h=document.documentElement.scrollHeight-document.documentElement.clientHeight;
document.getElementById("progress").style.width=(s/h)*100+"%";
});

// Cursor
const cursor=document.querySelector(".cursor");
document.addEventListener("mousemove",e=>{
cursor.style.left=e.clientX+"px";
cursor.style.top=e.clientY+"px";
});

// Particles
const canvas=document.getElementById("particles");
const ctx=canvas.getContext("2d");
canvas.width=innerWidth;canvas.height=innerHeight;
let p=[];for(let i=0;i<50;i++){p.push({x:Math.random()*canvas.width,y:Math.random()*canvas.height});}
function draw(){
ctx.clearRect(0,0,canvas.width,canvas.height);
ctx.fillStyle="#1e90ff";
p.forEach(pt=>{
ctx.beginPath();
ctx.arc(pt.x,pt.y,2,0,Math.PI*2);
ctx.fill();
pt.y+=0.5;if(pt.y>canvas.height)pt.y=0;
});
requestAnimationFrame(draw);
}
draw();

// Disable past date
let today=new Date().toISOString().split("T")[0];
document.getElementById("date").setAttribute("min",today);

// Booking WhatsApp
document.getElementById("bookingForm").addEventListener("submit",function(e){
e.preventDefault();
let msg=`Booking:%0AName:${name.value}%0APhone:${phone.value}%0ADate:${date.value}%0ATime:${time.value}%0ADetails:${details.value}`;
window.open("https://wa.me/919832084397?text="+msg,"_blank");
});
</script>

</body>
</html>
