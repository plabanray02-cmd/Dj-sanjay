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

/* Cursor */
.cursor{
position:fixed;width:20px;height:20px;border-radius:50%;
background:#1e90ff;pointer-events:none;
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

/* Services */
.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
}
.card{
padding:25px;border-radius:15px;
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
transition:0.4s;position:relative;overflow:hidden;
}
.card:hover{
transform:translateY(-10px) scale(1.05);
box-shadow:0 0 25px #1e90ff;
}
.card h3{color:#1e90ff;margin-bottom:10px;}
.card p{font-size:14px;opacity:0.8;}

/* Review */
.review-box{
max-width:400px;margin:auto;padding:20px;
background:rgba(255,255,255,0.05);
border-radius:10px;
}

/* Stars */
.stars span{
font-size:25px;
cursor:pointer;
color:gray;
}
.stars span.active{color:gold;}

/* Form */
form input, form textarea{
width:90%;margin:10px;padding:12px;border-radius:10px;border:none;
background:rgba(255,255,255,0.05);color:white;
}

/* Footer */
footer{text-align:center;padding:20px;opacity:0.6;}

.whatsapp{position:fixed;bottom:20px;right:20px;background:#25D366;padding:15px;border-radius:50%;}
</style>
</head>

<body>

<div id="loader"><div class="circle"></div></div>
<div id="progress"></div>
<div class="cursor"></div>

<header>
<h1></h1>
<p>Premium Sound • Light • Event Setup</p>
<a class="btn" href="tel:919832084397">Call</a>
<a class="btn" href="https://wa.me/919832084397">WhatsApp</a>
</header>

<!-- SERVICES -->
<div class="section">
<h2>🔥 Our Premium Services</h2>
<div class="services">
<div class="card"><h3>🎧 DJ Setup</h3><p>High bass DJ system</p></div>
<div class="card"><h3>🔊 Sound System</h3><p>Crystal clear sound</p></div>
<div class="card"><h3>💡 Lighting</h3><p>LED & laser lights</p></div>
<div class="card"><h3>🎤 Stage Setup</h3><p>Full stage support</p></div>
<div class="card"><h3>🎉 Wedding</h3><p>Wedding DJ package</p></div>
<div class="card"><h3>🎂 Birthday</h3><p>Party DJ setup</p></div>
</div>
</div>

<!-- BOOKING -->
<div class="section">
<h2>📅 Book Now</h2>
<form id="bookingForm">
<input type="text" id="name" placeholder="Name" required>
<input type="tel" id="phone" placeholder="Phone" required>
<input type="date" id="date" required>
<input type="time" id="time" required>
<textarea id="details" placeholder="Details"></textarea>
<button>Book</button>
</form>
</div>

<!-- REVIEW -->
<div class="section">
<h2>⭐ Customer Reviews</h2>

<div class="review-box">
<p id="reviewText">"Best DJ service 🔥"</p>
<div class="stars" id="stars">
<span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
</div>
</div>

</div>

<footer>© DJ Sanjay</footer>
<a class="whatsapp" href="https://wa.me/919832084397">💬</a>

<script>
// Loader
window.onload=()=>{loader.style.display="none";};

// Typing
let t="DJ SANJAY",i=0;
function type(){if(i<t.length){document.querySelector("h1").innerHTML+=t[i++];setTimeout(type,100);}}
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
progress.style.width=(s/h)*100+"%";
});

// Cursor
document.addEventListener("mousemove",e=>{
cursor.style.left=e.clientX+"px";
cursor.style.top=e.clientY+"px";
});

// Disable past date
date.min=new Date().toISOString().split("T")[0];

// WhatsApp booking
bookingForm.onsubmit=e=>{
e.preventDefault();
let msg=`Booking:%0A${name.value}%0A${phone.value}%0A${date.value}%0A${time.value}`;
window.open("https://wa.me/919832084397?text="+msg);
};

// ⭐ Star rating
let stars=document.querySelectorAll("#stars span");
stars.forEach((star,i)=>{
star.onclick=()=>{
stars.forEach(s=>s.classList.remove("active"));
for(let j=0;j<=i;j++)stars[j].classList.add("active");
};
});

// 💬 Auto review slider
let reviews=[
"🔥 Amazing sound quality!",
"🎉 Best DJ in town!",
"💯 Fully satisfied service!"
];
let r=0;
setInterval(()=>{
r=(r+1)%reviews.length;
document.getElementById("reviewText").innerText=reviews[r];
},3000);

</script>

</body>
</html>
