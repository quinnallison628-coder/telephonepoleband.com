<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Modern Website</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    body{
      font-family:'Poppins',sans-serif;
      background:#0f172a;
      color:white;
      overflow-x:hidden;
    }

    a{
      text-decoration:none;
      color:inherit;
    }

    .container{
      width:90%;
      max-width:1200px;
      margin:auto;
    }

    /* NAVBAR */

    nav{
      position:fixed;
      top:0;
      width:100%;
      z-index:1000;
      backdrop-filter:blur(12px);
      background:rgba(15,23,42,0.75);
      border-bottom:1px solid rgba(255,255,255,0.08);
    }

    .nav-container{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px 0;
    }

    .logo{
      font-size:1.5rem;
      font-weight:700;
      color:#38bdf8;
    }

    .nav-links{
      display:flex;
      gap:30px;
    }

    .nav-links a{
      color:#e2e8f0;
      transition:0.3s;
    }

    .nav-links a:hover{
      color:#38bdf8;
    }

    .menu-btn{
      display:none;
      font-size:2rem;
      cursor:pointer;
    }

    /* HERO */

    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      background:
      linear-gradient(rgba(15,23,42,.8),rgba(15,23,42,.95)),
      url('https://images.unsplash.com/photo-1497366754035-f200968a6e72?q=80&w=1600&auto=format&fit=crop') center/cover;
    }

    .hero-content{
      max-width:700px;
    }

    .hero h1{
      font-size:clamp(3rem,7vw,6rem);
      line-height:1.1;
      margin-bottom:20px;
    }

    .hero h1 span{
      color:#38bdf8;
    }

    .hero p{
      color:#cbd5e1;
      font-size:1.1rem;
      margin-bottom:35px;
      line-height:1.8;
    }

    .btn-group{
      display:flex;
      gap:20px;
      flex-wrap:wrap;
    }

    .btn{
      padding:14px 28px;
      border-radius:999px;
      font-weight:600;
      transition:0.3s;
      display:inline-block;
    }

    .primary-btn{
      background:#38bdf8;
      color:#0f172a;
    }

    .primary-btn:hover{
      transform:translateY(-4px);
      background:#0ea5e9;
    }

    .secondary-btn{
      border:1px solid rgba(255,255,255,.2);
    }

    .secondary-btn:hover{
      background:rgba(255,255,255,.1);
    }

    /* SECTION */

    section{
      padding:100px 0;
    }

    .section-title{
      text-align:center;
      margin-bottom:60px;
    }

    .section-title h2{
      font-size:3rem;
      margin-bottom:15px;
    }

    .section-title p{
      color:#94a3b8;
      max-width:700px;
      margin:auto;
    }

    /* ABOUT */

    .about-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:50px;
      align-items:center;
    }

    .about-img img{
      width:100%;
      border-radius:20px;
      box-shadow:0 20px 50px rgba(0,0,0,.4);
    }

    .about-text h3{
      font-size:2rem;
      margin-bottom:20px;
    }

    .about-text p{
      color:#cbd5e1;
      margin-bottom:20px;
      line-height:1.8;
    }

    /* CARDS */

    .cards{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:25px;
    }

    .card{
      background:#1e293b;
      padding:35px;
      border-radius:20px;
      transition:.3s;
      border:1px solid rgba(255,255,255,.05);
    }

    .card:hover{
      transform:translateY(-10px);
      border-color:#38bdf8;
    }

    .card h3{
      margin-bottom:15px;
      color:#38bdf8;
    }

    .card p{
      color:#cbd5e1;
      line-height:1.7;
    }

    /* PORTFOLIO */

    .portfolio-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:25px;
    }

    .portfolio-item{
      position:relative;
      overflow:hidden;
      border-radius:20px;
    }

    .portfolio-item img{
      width:100%;
      height:320px;
      object-fit:cover;
      transition:.5s;
    }

    .overlay{
      position:absolute;
      inset:0;
      background:rgba(15,23,42,.85);
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      opacity:0;
      transition:.4s;
      padding:20px;
      text-align:center;
    }

    .portfolio-item:hover img{
      transform:scale(1.1);
    }

    .portfolio-item:hover .overlay{
      opacity:1;
    }

    /* CONTACT */

    .contact-wrapper{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
      gap:40px;
    }

    form{
      display:flex;
      flex-direction:column;
      gap:20px;
    }

    input, textarea{
      padding:16px;
      border:none;
      border-radius:12px;
      background:#1e293b;
      color:white;
      font-family:inherit;
    }

    textarea{
      resize:none;
    }

    input:focus,
    textarea:focus{
      outline:2px solid #38bdf8;
    }

    button{
      border:none;
      cursor:pointer;
    }

    footer{
      border-top:1px solid rgba(255,255,255,.08);
      padding:40px 0;
      text-align:center;
      color:#94a3b8;
    }

    /* MOBILE */

    @media(max-width:768px){

      .menu-btn{
        display:block;
      }

      .nav-links{
        position:absolute;
        top:80px;
        right:-100%;
        width:250px;
        background:#0f172a;
        flex-direction:column;
        padding:30px;
        transition:.4s;
      }

      .nav-links.active{
        right:0;
      }

      .hero{
        text-align:center;
      }

      .btn-group{
        justify-content:center;
      }
    }
  </style>
</head>

<body>

  <!-- NAVBAR -->

  <nav>
    <div class="container nav-container">

      <div class="logo">
        YOUR BRAND
      </div>

      <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
      </div>

      <div class="menu-btn" id="menuBtn">
        ☰
      </div>

    </div>
  </nav>

  <!-- HERO -->

  <section class="hero" id="home">

    <div class="container">

      <div class="hero-content">

        <h1>
          Build Websites <span>Without Limits</span>
        </h1>

        <p>
          Fully customizable modern website with no Wix restrictions.
          Edit anything, host anywhere, and scale however you want.
        </p>

        <div class="btn-group">

          <a href="#portfolio" class="btn primary-btn">
            View Projects
          </a>

          <a href="#contact" class="btn secondary-btn">
            Contact Me
          </a>

        </div>

      </div>

    </div>

  </section>

  <!-- ABOUT -->

  <section id="about">

    <div class="container about-grid">

      <div class="about-img">
        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=1200&auto=format&fit=crop">
      </div>

      <div class="about-text">

        <h3>
          Better Than Wix
        </h3>

        <p>
          This template gives you complete ownership and customization.
          No forced subscriptions, locked features, or drag-and-drop limitations.
        </p>

        <p>
          Add ecommerce, blogs, APIs, animations, dashboards,
          CMS systems, and custom integrations easily.
        </p>

        <a href="#contact" class="btn primary-btn">
          Start Now
        </a>

      </div>

    </div>

  </section>

  <!-- SERVICES -->

  <section id="services">

    <div class="container">

      <div class="section-title">

        <h2>Services</h2>

        <p>
          Fully responsive sections you can customize however you want.
        </p>

      </div>

      <div class="cards">

        <div class="card">
          <h3>Web Design</h3>
          <p>
            Modern responsive layouts optimized for all devices.
          </p>
        </div>

        <div class="card">
          <h3>SEO</h3>
          <p>
            Fast loading pages with clean semantic HTML structure.
          </p>
        </div>

        <div class="card">
          <h3>Custom Features</h3>
          <p>
            Integrate forms, APIs, dashboards, ecommerce, and more.
          </p>
        </div>

        <div class="card">
          <h3>Hosting Freedom</h3>
          <p>
            Deploy on Vercel, Netlify, GitHub Pages, or your own server.
          </p>
        </div>

      </div>

    </div>

  </section>

  <!-- PORTFOLIO -->

  <section id="portfolio">

    <div class="container">

      <div class="section-title">

        <h2>Portfolio</h2>

        <p>
          Replace these demo projects with your own work.
        </p>

      </div>

      <div class="portfolio-grid">

        <div class="portfolio-item">

          <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1200&auto=format&fit=crop">

          <div class="overlay">
            <h3>Agency Website</h3>
            <p>Modern business design</p>
          </div>

        </div>

        <div class="portfolio-item">

          <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?q=80&w=1200&auto=format&fit=crop">

          <div class="overlay">
            <h3>Analytics Dashboard</h3>
            <p>Interactive data UI</p>
          </div>

        </div>

        <div class="portfolio-item">

          <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop">

          <div class="overlay">
            <h3>Startup Landing Page</h3>
            <p>High conversion layout</p>
          </div>

        </div>

      </div>

    </div>

  </section>

  <!-- CONTACT -->

  <section id="contact">

    <div class="container">

      <div class="section-title">

        <h2>Contact</h2>

        <p>
          Connect your backend or use any API provider you want.
        </p>

      </div>

      <div class="contact-wrapper">

        <div>

          <h3 style="margin-bottom:20px;">
            Let's Build Something Great
          </h3>

          <p style="color:#cbd5e1; line-height:1.8;">
            This site is pure HTML/CSS/JS and can be expanded infinitely.
            Add authentication, databases, ecommerce, AI tools, blogs,
            memberships, and more.
          </p>

        </div>

        <form id="contactForm">

          <input type="text" placeholder="Your Name" required>

          <input type="email" placeholder="Your Email" required>

          <textarea rows="6" placeholder="Message"></textarea>

          <button class="btn primary-btn">
            Send Message
          </button>

        </form>

      </div>

    </div>

  </section>

  <!-- FOOTER -->

  <footer>

    <div class="container">
      © 2026 Your Brand — Built Without Wix
    </div>

  </footer>

  <script>

    // MOBILE MENU

    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", () => {
      navLinks.classList.toggle("active");
    });

    // CONTACT FORM

    const form = document.getElementById("contactForm");

    form.addEventListener("submit", (e) => {
      e.preventDefault();

      alert("Message sent successfully!");

      form.reset();
    });

    // NAV SHADOW

    window.addEventListener("scroll", () => {

      const nav = document.querySelector("nav");

      if(window.scrollY > 50){
        nav.style.boxShadow = "0 10px 30px rgba(0,0,0,.3)";
      } else {
        nav.style.boxShadow = "none";
      }

    });

  </script>

</body>
</html>
