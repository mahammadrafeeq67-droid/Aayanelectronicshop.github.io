<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aayan Electronic Shop</title>

<style>
body{
margin:0;
font-family:Arial, sans-serif;
background:#f2f6fb;
}

/* HEADER */
header{
background:linear-gradient(135deg,#0a74da,#003f88);
color:white;
padding:35px 20px;
text-align:center;
}
header h1{margin:0;font-size:34px;}
header p{margin-top:10px;font-size:17px;}

/* BUTTONS */
.top-buttons, .lang-buttons{
display:flex;
justify-content:center;
gap:15px;
margin-top:15px;
flex-wrap:wrap;
}
.top-buttons a, .lang-buttons button{
padding:12px 22px;
border-radius:8px;
font-size:16px;
font-weight:bold;
text-decoration:none;
border:none;
cursor:pointer;
}
.call-btn{background:#25D366;color:white;}
.dir-btn{background:#ffcc00;color:black;}
.en-btn{background:white;color:#003f88;}
.kn-btn{background:#28a745;color:white;}

/* SECTIONS */
.section{
background:white;
margin:22px auto;
padding:22px;
max-width:1100px;
border-radius:8px;
box-shadow:0 2px 8px rgba(0,0,0,0.1);
}
h2{
color:#0a74da;
border-bottom:2px solid #0a74da;
padding-bottom:5px;
}

/* SERVICES */
.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:15px;
}
.service-box{
background:#eaf1ff;
padding:15px;
border-radius:6px;
text-align:center;
font-weight:bold;
}

/* GALLERY */
.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:15px;
}
.gallery img{
width:100%;
height:220px;
object-fit:cover;
border-radius:8px;
}

/* WHATSAPP */
.whatsapp a{
display:inline-block;
background:#25D366;
color:white;
padding:12px 18px;
border-radius:6px;
text-decoration:none;
margin:6px 10px 0 0;
font-weight:bold;
}

/* FORM */
input, textarea{
width:100%;
padding:10px;
margin:8px 0;
}
button.submit-btn{
background:#25D366;
color:white;
border:none;
padding:12px 20px;
font-size:16px;
border-radius:6px;
cursor:pointer;
}

/* LOCATION */
.location-btn{
display:inline-block;
margin-top:12px;
background:#0a74da;
color:white;
padding:12px 20px;
border-radius:6px;
text-decoration:none;
font-weight:bold;
}

/* FOOTER */
footer{
background:#222;
color:white;
text-align:center;
padding:12px;
}
</style>
</head>

<body>

<header>
<h1 id="title">Aayan Electronic Shop</h1>
<p id="subtitle">All Types of Electronic Items Repairing</p>

<div class="top-buttons">
<a href="tel:+919019425668" class="call-btn">📞 Call Now</a>
<a href="https://maps.app.goo.gl/UawBakPJK86tBZxY9" target="_blank" class="dir-btn">
📍 Get Directions
</a>
</div>

<div class="lang-buttons">
<button class="en-btn" onclick="setEnglish()">English</button>
<button class="kn-btn" onclick="setKannada()">ಕನ್ನಡ</button>
</div>
</header>

<div class="section">
<h2 id="aboutTitle">About Us</h2>
<p id="aboutText">
We provide trusted, fast and affordable repairing services for all kinds
of electronic items. Customer satisfaction is our priority.
</p>
</div>

<div class="section">
<h2 id="serviceTitle">Our Services</h2>
<div class="services">
<div class="service-box">TV Repair</div>
<div class="service-box">Fan Repair</div>
<div class="service-box">Cooler Repair</div>
<div class="service-box">Speaker Repair</div>
<div class="service-box">Weight Machine Repair</div>
<div class="service-box">Mixer Repair</div>
<div class="service-box">Battery Repair</div>
<div class="service-box">LED / Light Repair</div>
</div>
</div>

<div class="section">
<h2>Contact & WhatsApp</h2>
<div class="whatsapp">
<a href="https://wa.me/919019425668" target="_blank">WhatsApp: 90194 25668</a>
<a href="https://wa.me/919845492409" target="_blank">WhatsApp: 98454 92409</a>
</div>
</div>

<div class="section">
<h2>Online Repair Request</h2>
<form onsubmit="sendWhatsApp(); return false;">
<input type="text" id="name" placeholder="Customer Name" required>
<input type="tel" id="phone" placeholder="Mobile Number" required>
<input type="text" id="item" placeholder="Electronic Item" required>
<textarea id="problem" rows="4" placeholder="Problem Description" required></textarea>
<button class="submit-btn" type="submit">Submit Repair Request</button>
</form>
</div>

<div class="section">
<h2>Our Location</h2>
<a class="location-btn" href="https://maps.app.goo.gl/UawBakPJK86tBZxY9" target="_blank">
📍 Open Location in Google Maps
</a>
</div>

<footer>
© 2026 Aayan Electronic Shop | All Rights Reserved
</footer>

<script>
function sendWhatsApp(){
var msg =
"Repair Request%0A"+
"Name: "+name.value+"%0A"+
"Phone: "+phone.value+"%0A"+
"Item: "+item.value+"%0A"+
"Problem: "+problem.value;
window.open("https://wa.me/919019425668?text="+msg,"_blank");
}

function setEnglish(){
title.innerText="Aayan Electronic Shop";
subtitle.innerText="All Types of Electronic Items Repairing";
aboutTitle.innerText="About Us";
aboutText.innerText="We provide trusted, fast and affordable repairing services for all kinds of electronic items. Customer satisfaction is our priority.";
serviceTitle.innerText="Our Services";
photoTitle.innerText="Shop Photos";
}

function setKannada(){
title.innerText="ಅಯಾನ್ ಎಲೆಕ್ಟ್ರಾನಿಕ್ ಶಾಪ್";
subtitle.innerText="ಎಲ್ಲಾ ರೀತಿಯ ಎಲೆಕ್ಟ್ರಾನಿಕ್ ವಸ್ತುಗಳ ದುರಸ್ತಿ";
aboutTitle.innerText="ನಮ್ಮ ಬಗ್ಗೆ";
aboutText.innerText="ನಾವು ಎಲ್ಲಾ ಎಲೆಕ್ಟ್ರಾನಿಕ್ ವಸ್ತುಗಳಿಗೆ ವೇಗವಾದ ಮತ್ತು ವಿಶ್ವಾಸಾರ್ಹ ದುರಸ್ತಿ ಸೇವೆಗಳನ್ನು ಒದಗಿಸುತ್ತೇವೆ.";
serviceTitle.innerText="ನಮ್ಮ ಸೇವೆಗಳು";
photoTitle.innerText="ಅಂಗಡಿ ಚಿತ್ರಗಳು";
}
</script>

</body>
</html>
