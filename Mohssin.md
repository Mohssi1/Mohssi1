- 👋 Hi, I’m @Mohssi1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
go to watssap 0680216907
<!---
Mohssi1/Mohssi1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Business Chop</title>

<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Cairo',sans-serif;background:#0f172a;color:white}

/* NAVBAR */
nav{
display:flex;
justify-content:space-between;
padding:20px 10%;
position:fixed;
width:100%;
background:rgba(0,0,0,0.5);
backdrop-filter:blur(10px);
}
nav a{
color:white;
margin:0 10px;
text-decoration:none;
}

/* HERO */
.hero{
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(135deg,#0d47a1,#000);
}
.hero h1{
font-size:50px;
margin-bottom:20px;
}
.hero p{
opacity:0.8;
margin-bottom:30px;
}
.btn{
background:#ff9800;
padding:15px 30px;
border-radius:30px;
color:white;
text-decoration:none;
}

/* SECTIONS */
section{
padding:80px 10%;
}

/* SERVICES */
.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}
.card{
background:#1e293b;
padding:30px;
border-radius:15px;
transition:0.3s;
}
.card:hover{
transform:translateY(-10px);
}

/* CONTACT */
input,textarea{
width:100%;
padding:12px;
margin:10px 0;
border:none;
border-radius:8px;
}
button{
background:#ff9800;
padding:12px;
border:none;
color:white;
width:100%;
}

/* FOOTER */
footer{
text-align:center;
padding:20px;
background:#020617;
}

/* ANIMATION */
.fade{
opacity:0;
transform:translateY(30px);
transition:1s;
}
.show{
opacity:1;
transform:translateY(0);
}
</style>
</head>

<body>

<nav>
<h2>Business Chop</h2>
<div>
<a href="#home">الرئيسية</a>
<a href="#services">الخدمات</a>
<a href="#contact">تواصل</a>
</div>
</nav>

<div class="hero" id="home">
<h1>نطور عملك إلى المستوى التالي 🚀</h1>
<p>خدمات رقمية احترافية تساعدك على النجاح</p>
<a href="#contact" class="btn">ابدأ الآن</a>
</div>

<section id="services">
<h2>الخدمات</h2>
<div class="services">
<div class="card fade">تصميم مواقع احترافية</div>
<div class="card fade">إدارة صفحات التواصل</div>
<div class="card fade">إعلانات ممولة</div>
</div>
</section>

<section id="contact">
<h2>تواصل معنا</h2>
<form id="contactForm">
<input type="text" id="name" placeholder="الاسم">
<input type="email" id="email" placeholder="الإيميل">
<textarea id="message" placeholder="رسالتك"></textarea>
<button type="submit">إرسال</button>
</form>
</section>

<footer>
© 2026 Business Chop
</footer>

<script>
// animation
const elements = document.querySelectorAll('.fade');
window.addEventListener('scroll', ()=>{
elements.forEach(el=>{
const top = el.getBoundingClientRect().top;
if(top < window.innerHeight - 100){
el.classList.add('show');
}
});
});

// form
document.getElementById('contactForm').addEventListener('submit', async function(e){
e.preventDefault();

const data = {
name: name.value,
email: email.value,
message: message.value
};

const res = await fetch('https://YOUR-APP.onrender.com/send',{
method:'POST',
headers:{'Content-Type':'application/json'},
body:JSON.stringify(data)
});

const result = await res.json();

alert(result.success ? 'تم الإرسال ✅' : 'خطأ ❌');
});
</script>

</body>
</html>
console.log.()
