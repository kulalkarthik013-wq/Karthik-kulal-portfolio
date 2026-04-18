<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Karthik | AI Portfolio</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600;800&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: radial-gradient(circle at top, #020617, #000);
  color: white;
  overflow-x: hidden;
}

/* ⭐ Particle Canvas Background */
#particles {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

/* your existing star layer */
body::before {
  content: "";
  position: fixed;
  width: 200%;
  height: 200%;
  background: url('https://www.transparenttextures.com/patterns/stardust.png');
  animation: moveStars 60s linear infinite;
  opacity: 0.2;
}

@keyframes moveStars {
  from { transform: translate(0,0); }
  to { transform: translate(-500px,-500px); }
}

.badge {
  display: inline-block;
  margin-bottom: 15px;
  padding: 8px 15px;
  border-radius: 20px;
  font-size: 13px;
  letter-spacing: 1px;
  text-align:right;

  color: #38bdf8;
  background: rgba(56,189,248,0.1);
  border: 1px solid rgba(56,189,248,0.3);
}
.badge-side {
  font-size: 14px;
  color: #38bdf8;
  margin-top: 10px;
  margin-left: 20px;

  animation: glowPulse 2s infinite ease-in-out;
}

/* Glow animation */
@keyframes glowPulse {
  0% {
    text-shadow: 0 0 5px rgba(56,189,248,0.5);
  }
  50% {
    text-shadow: 0 0 20px rgba(56,189,248,1),
                 0 0 30px rgba(167,139,250,0.8);
  }
  100% {
    text-shadow: 0 0 5px rgba(56,189,248,0.5);
  }
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px; /* reduced from 10% */
   position: sticky;
  top: 0;
  background: rgba(2, 6, 23, 0.7);
  backdrop-filter: blur(10px);
  z-index: 1000;
}
/* LOGO (Karthik) */
nav h2 {
  font-size: 24px;
  font-weight: 800;
  letter-spacing: 1px;
  cursor: pointer;

  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  -webkit-background-clip: text;
  color: transparent;

  transition: 0.3s;
}

/* Hover glow effect */
nav h2:hover {
  transform: scale(1.05);
  text-shadow: 0 0 15px rgba(56, 239, 248, 0.6);
}
nav div a {
  display: inline-block;
  padding: 8px 14px;
  margin-left: 10px;
  border-radius: 20px;
  position: relative;
  color : rgb(104, 185, 250);
  background: white;
  border: 1px solid white;

  transition: all 0.3s ease;
}

/* Hover like card effect */
nav div a:hover {
  transform: translateY(-5px) scale(1.05);
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  color: white;

  box-shadow: 0 0 20px rgba(56,189,248,0.5),
              0 0 35px rgba(167,139,250,0.3);
  border: 1px solid transparent;
}

/* Hero */
.hero {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start; /* LEFT ALIGN */
  text-align: left;
  padding: 30px 10%;
  max-width: 900px;
}

.hero h1 {
  font-size: 100px;
  font-weight: 800;
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  -webkit-background-clip: text;
  color: transparent;
}

.hero p {
  margin-top: 15px;
  color: #94a3b8;
  font-size: 18px;
}

/* Button */
.btn {
  display: inline-block;
  margin-top: 15px;
  margin-right: 10px;
  padding: 10px 18px;
  border-radius: 25px;
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  color: black;
  font-weight: 600;
  text-decoration: none;
  transition: 0.3s;
}

.btn:hover {
  transform: scale(1.1);
}

/* Sections */
.section {
  padding: 60px 10%;
}

.title {
  font-size: 30px;
  margin-bottom: 30px;
  color :#38e8f8
}

/* Cards */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 25px;
}

.card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(12px);
  padding: 20px;
  border-radius: 20px;
  border: 1px solid rgba(255,255,255,0.1);
  transition: 0.3s;
  position: relative;
}

.card:hover {
  transform: translateY(-10px) scale(1.03);
  border: 1px solid #38bdf8;
  box-shadow: 0 0 25px rgba(56,189,248,0.3);
}

.card h3 {
  margin-bottom: 10px;
}

.card p {
  color: #aaa;
  font-size: 14px;
}

.tech {
  font-size: 13px;
  color: #38bdf8;
  margin-top: 10px;
}
/* Certified Button */
.card a.btn {
  display: inline-block;
  margin-top: 10px;

  padding: 8px 16px; /* 👈 smaller */
  border-radius: 20px;

  background: linear-gradient(90deg, #38e8f8, #a78bfa);
  color: black;
  font-weight: 600;
  text-decoration: none;

  transition: 0.3s;
}

.card a.btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 15px rgba(56, 248, 59, 0.6),
              0 0 25px rgba(167,139,250,0.4);
}

/* Certificates Section */
#certificates {
  background: rgba(255,255,255,0.02);
  border-top: 1px solid rgba(255,255,255,0.05);
}

/* Certificate Cards */
#certificates .card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(12px);

  padding: 20px;            /* 👈 smaller */
  max-width: 300px;         /* 👈 compact size */
  border-radius: 40px;        /* 👈 slight right shift */
  margin-left: 10%; 
  border: 1px solid rgba(167,139,250,0.2);
  margin-top: 0%;
  transition: 0.3s;
}

/* Hover effect */
#certificates .card:hover {
  transform: translateY(-8px) scale(1.02);

  border: 1px solid #f48bfa;

  box-shadow: 0 0 20px rgba(167,139,250,0.5),
              0 0 30px rgba(56,189,248,0.3);
}

/* Title */
#certificates .title {
  background: linear-gradient(90deg, #38b8f8, #a78bfa);
  -webkit-background-clip: text;
  color: transparent;
}

/* Optional: smaller text */
#certificates .card h3 {
  font-size: 20px;
  margin-left: 20px;
  
}

#certificates .card p {
  font-size: 12px;
  color: #f7f998;
}
/* Skills */
.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
}
#skills .title {
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  color: transparent;
}

.skills span {
  display: flex;
  align-items: center;
  justify-content: center;

  padding: 12px 18px;
  border-radius: 16px;
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 0.5px;

  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.1);
  color: rgb(119, 234, 234);

  backdrop-filter: blur(10px);

  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

/* Glow highlight effect */
.skills span::before {
  content: "";
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(56,189,248,0.3), transparent);
  transition: 0.5s;
}

/* Hover effect */
.skills span:hover {
  transform: translateY(-6px) scale(1.08);
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  color: black;
  box-shadow: 0 0 20px rgba(56,189,248,0.5),
              0 0 40px rgba(167,139,250,0.3);
}

.skills span:hover::before {
  left: 100%;
}
#experience .card {
  border: 1px solid rgba(167,139,250,0.3);
}

#experience .card:hover {
  box-shadow: 0 0 25px rgba(167,139,250,0.4);
}
.tech-stack {
  margin-top: 10px;
}

.tech-stack span {
  display: inline-block;
  margin: 5px 5px 0 0;
  padding: 6px 12px;
  border-radius: 15px;
  font-size: 12px;

  background: rgba(56,189,248,0.1);
  color: #38bdf8;
  border: 1px solid rgba(56,189,248,0.3);

  transition: 0.3s;
}

.tech-stack span:hover {
  background: #38bdf8;
  color: black;
}
#contact {
  position: relative;
}

/* Align whole card to LEFT */
.contact-wrapper {
  display: flex;
  justify-content: flex-start; /* LEFT SIDE */
}

/* Big main card */
.contact-card {
  width: 100%;
  max-width: 500px;

  padding: 25px;
  border-radius: 25px;

  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.1);

  backdrop-filter: blur(12px);

  box-shadow: 0 0 25px rgba(56,189,248,0.15);
}

/* Small inner boxes */
.contact-item {
  margin: 12px 0;
  padding: 14px 16px;

  border-radius: 14px;

  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);

  color: #e2e8f0;
  font-size: 14px;

  display: flex;
  align-items: center;

  transition: 0.3s;
}

/* Hover effect */
.contact-item:hover {
  transform: translateX(8px);
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  color: black;

  box-shadow: 0 0 20px rgba(56,189,248,0.4),
              0 0 30px rgba(167,139,250,0.3);
}

/* Icons */
.contact-item i {
  margin-right: 10px;
  color: #38bdf8;
  font-size: 16px;
  transition: 0.3s;
}

.contact-item:hover i {
  color: black;
}

/* Title gradient */
#contact .title {
  background: linear-gradient(90deg, #38bdf8, #a78bfa);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 20px;
}




/* Footer */
footer {
  text-align: center;
  padding: 40px;
   color: #94a3b8;
   background: rgba(36, 90, 97, 0.183);
  border-top: 1px solid rgba(56,189,248,0.2);
  backdrop-filter: blur(12px);
}
/* ⭐ ADDED ONLY FOR ANIMATION */
#particles {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -2;
  pointer-events: none;
}
</style>
</head>

<body>
  <!-- ⭐ ONLY ADDITION -->
<canvas id="particles"></canvas>

<nav>
  <h2>Karthik S Kulal</h2>
  <div>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
    <a href="#experience">Experience</a>
  </div>
</nav>

<div class="hero">
     <div class="badge">
    ● Active in Bharat Unnati Fellowship & LearnersByte Internship
  </div>
  <h1>Designing Intelligence</h1>
  <p style="font-size:20px; margin-top:15px;">
    AI Developer & Full Stack Engineer
  </p>

  <p style="margin-top:10px; color:#94a3b8; max-width:600px;">
    I build intelligent applications, AI-powered chatbots, and scalable web apps using React.
    Passionate about automation, machine learning, and creating real-world solutions 
    that improve productivity and user experience.
  </p>

  <div style="margin-top:20px;">
    <a href="#projects" class="btn">View Projects</a>
    <a href="#" class="btn">Download Resume</a>
  </div>
</div>

<div class="section" id="certificates">
  <h2 class="title">📜 My Certifications</h2>

  <div class="cards">

    <div class="card">
      <h3>🤖 Bharat Unnati AI Fellowship</h3>
      <p>AI Fellowship Program Completion</p>
    </div>

    <div class="card">
      <h3>🏅NPTEL</h3>
     <p>📜 NPTEL Certified – Demonstrating strong foundation in engineering and technology</p>
    </div>

    <div class="card">
      <h3>🧠AI Webinar</h3>
      <p>AI Assisted Coding - AZ Career</p>
    </div>

  </div>
</div>

<!-- PROJECTS -->
<div class="section" id="projects">
  <h2 class="title">Featured Projects</h2>

  <div class="cards">

    <div class="card">
      <h3>🤖 AI Chatbot</h3>
      <p>Real-time chatbot with intelligent responses using OpenAI API.</p>
      <div class="tech">Python • OpenAI • Node.js</div>
      <br>
      <a href="#" class="btn">Live</a>
      <a href="#" class="btn">GitHub</a>
    </div>

    <div class="card">
      <h3>⚙️ n8n AI Automation</h3>
      <p>Automated workflows using AI agents for task execution.</p>
      <div class="tech">n8n • APIs • Webhooks</div>
      <br>
      <a href="#" class="btn">View</a>
    </div>

    <div class="card">
      <h3>🌐 React Web App</h3>
      <p>GYMEXPERT web app with clean UI design.</p>
      <div class="tech">React • JavaScript • UI/UX</div>
      <br>
      <a href="#" class="btn">Live</a>
      <a href="#" class="btn">GitHub</a>
    </div>

  </div>
</div>
<div class="section" id="experience">
  <h2 class="title">⚡Tech Stack</h2>

  <div class="cards">

    <div class="card">
      <h3>💻 Full Stack Development</h3>
      <p>
        Building scalable web applications using modern technologies like React, Node.js, and APIs.
      </p>
       <div class="tech-stack">
    <span>React</span>
    <span>Node.js</span>
    <span>JavaScript</span>
    <span>CSS</span>
    <span>sqlite</span>
  </div>
    </div>

    <div class="card">
      <h3>🧠 Machine Learning</h3>
      <p>
        Developing predictive models and working with data using ML algorithms and Python.
      </p>
      <div class="tech-stack">
  <span>Python</span>
  <span>Scikit-learn</span>
  <span>Pandas</span>

</div>
    </div>

    <div class="card">
      <h3>🤖 Artificial Intelligence</h3>
      <p>
        Creating AI-powered solutions including chatbots, automation systems, and intelligent apps.
      </p>
      <div class="tech-stack">
  <span>OpenAI</span>
  <span>NLP</span>
  <span>Automation</span>
  <span>Notion AI</span>
  <SPAN>n8n</SPAN>
</div>
    </div>
  </div>
</div>
<!-- SKILLS -->
<div class="section" id="skills">
  <h2 class="title">🧠 Skills</h2>
  <div class="skills">
    <span>Python</span>
    <span>JavaScript</span>
    <span>React</span>
    <span>Node.js</span>
    <span>AI</span>
    <span>n8n</span>
  </div>
</div>
<!-- CONTACT -->
<div class="section" id="contact">
  <h2 class="title">📬 Contact</h2>

  <div class="contact-wrapper">

    <div class="contact-card">

      <div class="contact-item">
        <i class="fa-solid fa-envelope"></i>
        Email: kulalkarthik@gmail.com
      </div>

      <div class="contact-item">
        <i class="fa-brands fa-linkedin"></i>
        LinkedIn: linkedin.com/in/karthik-kulal-3b65273a6
      </div>

      <div class="contact-item">
        <i class="fa-brands fa-github"></i>
        GitHub: https://github.com/kulalkarthik013-wq
      </div>

    </div>

  </div>
</div>
</div>
<footer>
  <p>© 2026 Karthik Kulal | Thanks for visiting my portfolio 🙌</p>
</footer>
<!-- ⭐ MOVING STARS SCRIPT -->
<script>
const canvas = document.getElementById("particles");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let stars = [];

class Star {
  constructor() {
    this.x = Math.random() * canvas.width;
    this.y = Math.random() * canvas.height;
    this.size = Math.random() * 2;
    this.speedX = (Math.random() - 0.5) * 0.3;
    this.speedY = (Math.random() - 0.5) * 0.3;
  }

  update() {
    this.x += this.speedX;
    this.y += this.speedY;

    if (this.x < 0) this.x = canvas.width;
    if (this.x > canvas.width) this.x = 0;
    if (this.y < 0) this.y = canvas.height;
    if (this.y > canvas.height) this.y = 0;
  }

  draw() {
    ctx.fillStyle = "rgba(56,189,248,0.8)";
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
    ctx.fill();
  }
}

function init() {
  for (let i = 0; i < 120; i++) {
    stars.push(new Star());
  }
}

function animate() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  stars.forEach(s => {
    s.update();
    s.draw();
  });
  requestAnimationFrame(animate);
}

init();
animate();

window.addEventListener("resize", () => {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
  stars = [];
  init();
});
</script>

</body>
</html>
